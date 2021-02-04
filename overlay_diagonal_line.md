Original version
```
def scatter_predictions(model, X_test, y_test):
    predicted = model.predict(X_test)
    fig, ax = plt.subplots()
    ax.scatter(y_test, predicted, edgecolors=(0, 0, 0))
    ax.plot([y_test.min(), y_test.max()], [y_test.min(), y_test.max()], "k--", lw=4)
    ax.set_xlabel("Measured")
    ax.set_ylabel("Predicted")
    plt.show()
```

Modified to remove model
```
def scatter_predictions(X_test, y_test):
    predicted = X_test
    fig, ax = plt.subplots()
    ax.scatter(y_test, predicted, edgecolors=(0, 0, 0))
    ax.plot([y_test.min(), y_test.max()], [y_test.min(), y_test.max()], "k--", lw=4)
    ax.set_xlabel("X Vector")
    ax.set_ylabel("Y Vector")
    plt.show()
```
This will draw a diagonal line up the scatter when you pass `scatter_predictions(df['column'], df['column'])`
