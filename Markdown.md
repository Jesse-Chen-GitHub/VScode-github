# Markdown 撰寫

## 標題
要創建標題，請在標題文本前添加一至六個 符號。 你使用的 數量將決定層次結構級別和標題的大小。`#` `#`
 - # 我是標題
 - ## 我是標題
 - ### 我是標題
 - #### 我是標題

使用兩個或多個標題時，GitHub 會自動生成一個目錄，可以通過按兩下檔標題中的 來訪問該目錄。 每個標題都列在目錄中，可以按下某個標題導航到所選部分

## 文本樣式
可以在評論欄位和檔中以粗體、斜體、刪除線、下標或上標文本表示強調。`.md`
![Alt text](./.images/image-2.png)

## 文件中使用連結
**書籤連結**
若要讓書籤連結到「目前」檔案中的標題，請使用井字符號，後面接著小寫標題文字。 移除標題中的標點符號，並以破折號取代空格：

```Markdown
[Managed Disks](#managed-disks)
```
若要連結到另一篇文章中的書籤標題，請使用檔案相對或網站相對連結加上井字符號，後面接著標題文字。 移除標題中的標點符號，並以破折號取代空格：

```Markdown
[Managed Disks](../../linux/overview.md#managed-disks)
```
- 參考資料：[在文件中使用連結](https://learn.microsoft.com/zh-tw/contribute/content/how-to-write-links)

## 引用文本
可以使用 來引用文本。`>`
    
    Text that is not a quote

    > Text that is a quote
    
## 參考資料
- [基本撰寫和格式語法 - GitHub 文檔](https://docs.github.com/zh/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax#styling-text)
- [瞭解 Markdown 參考 - Microsoft](https://learn.microsoft.com/zh-tw/contribute/content/markdown-reference)

