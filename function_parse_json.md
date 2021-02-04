For part file revisions JSON data.

```
def parse_units(row_json):
    if isinstance(row_json, str):
        row = json.loads(row_json)
    else:
        return None

    units = row["units"]
    value = row["value"]

    if not value or not units:
        return None

    if "mm" in units:
        return value
    elif units == "in":
        return value * 25.4
    elif units == "in^2/":
        return value * 25.4 ** 2
    elif units == "in^3/":
        return value * 25.4 ** 3
```

Use:

```
unit_cols = [
    "surface_area",
    "volume",
    "aabb_volume",
    "max_x_length",
    "max_y_length",
    "max_z_length",
    "obb_volume",
]

df[unit_cols] = df[unit_cols].applymap(parse_units)
```
