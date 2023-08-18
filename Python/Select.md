
## Select
紀錄 `select` 使用方法

### 方法 1
說明此方法
    `read_socks, write_socks, err_socks = select.select([s], [], [], 1)`

這段程式碼使用了 `select` 函數來監聽一個節點 `s` 的讀取狀態，並將結果分別存儲在 `read_socks`、`write_socks` 和 `err_socks` 中。

- `read_socks`：包含所有可讀取的節點。
- `write_socks`：包含所有可寫入的節點。
- `err_socks`：包含所有發生錯誤的節點。

而 `1` 是 `select` 函數的超時時間，這裡設定為 1 秒。這意味著如果在 1 秒內沒有讀取到任何數據，`select` 函數會超時並返回三個空的列表。

可以根據 `read_socks`、`write_socks` 和 `err_socks` 的值執行相應的操作。例如，如果 `read_socks` 列表不為空，則表示有待讀取的數據。您可以使用 `read_socks` 中的節點進行相應的讀取操作。

以下是一個例子，顯示如何使用這些變量：

```python
import socket
import select

# 創建一個套接字
s = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
s.connect(('localhost', 12345))

# 使用 select 監聽套接字讀取狀態
read_socks, write_socks, err_socks = select.select([s], [], [], 1)

# 檢查是否有可讀取的數據
if read_socks:
    # 從套接字讀取數據
    data = s.recv(1024)
    print('Received:', data.decode())
else:
    print('Timeout')
```

在這個例子中，我們創建一個套接字並連接到本地主機的 12345 端口。然後，我們使用 `select` 函數監聽套接字的讀取狀態，並在超時之前等待 1 秒。如果在超時之前收到數據，則從套接字讀取數據並打印到控制台。否則，打印 "Timeout"。hg

### 方法 2
`select()` 是一個在 Python 3.11.4 中引入的語言功能，可讓你在多個輸入中進行選擇。它接受任意數量的輸入，並返回輸入中第一個可用輸入的索引。如果所有輸入都不可用，則它返回 -1。

`select()` 語言功能的語法如下：
`select(input1, input2, ..., inputN)`

`select()` 語言功能可用於多種場景。例如，你可以在多個文件中進行選擇，或者你可以在多個網路連接中進行選擇。

以下是使用 `select()` 語言功能的一些示例：
``` py
# 在多個文件中進行選擇
with open("file1.txt") as f1, open("file2.txt") as f2:
  input = select(f1, f2)

if input == 0:
  # 使用 f1 進行操作
elif input == 1:
  # 使用 f2 進行操作

# 在多個網路連接中進行選擇
with socket.socket() as s1, socket.socket() as s2:
  input = select(s1, s2)

if input == 0:
  # 使用 s1 進行操作
elif input == 1:
  # 使用 s2 進行操作
```