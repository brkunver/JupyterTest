### simple linear regression calculator in python

[check main.ipynb file for details](https://github.com/brkunver/simple-linear-reg-python/blob/main/main.ipynb)

```python
    def simple_lin_reg(x : pd.Series,y :pd.Series):
    mean_x : int = x.mean()
    mean_y : int = y.mean()

    sum_num = 0
    sum_denum = 0
    for i in range(len(x)):
        sum_num += (x.iloc[i] - mean_x) * (y.iloc[i] - mean_y)
        sum_denum += (x.iloc[i] - mean_x) ** 2

    b1 : float = sum_num / sum_denum if sum_denum != 0 else 0
    print("b0 =>", mean_y - b1 * mean_x )
    print("b1 =>" , b1 )

```
