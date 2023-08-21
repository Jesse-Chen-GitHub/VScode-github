## def
紀錄 `def` 使用方法

def 用於定義函式。函式是一段可以重複使用的程式碼，可以用來執行特定的任務。

def 函式語法如下：

```py
def function_name(parameters):
    # Function body
    return value

```
- `function_name` 是函式的名稱。
- `parameters` 是函式的輸入參數。
- `Function body` 是函式執行的程式碼。
- `return value` 是函式的輸出值。


### 方法 1
下面是一個簡單的函式，它接受兩個數字並返回它們的和：

```py {.line-numbers}
def add(a, b):
    return a + b

result = add(10, 20)
print(result)
```

輸出：`30`