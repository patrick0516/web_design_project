## HTML 
### HTML簡介
HTML（HyperText Markup Language，超文本標記語言）是打造網頁的基石。它表述並定義網頁的內容。伴隨 HTML 而來的技術還有描述網頁外觀（CSS）及功能性的程式語言（JavaScript）。

「超文本」（HyperText）是指從某個網頁連到其他網頁的連結，不管它連結到站內或站外。藉由撰寫與上載網頁到網際網路中，我們就積極參與了全球資訊網（World Wide Web) 這個資訊系統。

HTML 使用「標記」（markup）來詮釋文字、圖像、或是其他能在瀏覽器裡面顯示的內容。
### HTML結構
一個HTML標籤包含：

1. 起始標籤(opening tag)：它包含了元素的名字，夾在一對 <、> (brackets)之間。它指明元素從何開始生效。
2. 結束標籤(closing tag)：結束標籤和起始標籤長得差不多，只不過它在名字前面還多加了一條斜線 (forward slash) 。它表示元素結束的地方。忘記加上結束標籤是初學者常犯的錯誤，這將導致奇怪的結果。
3. 內容(content): 元素的內容。
4. 元素(element): 以上三者加起來就是元素。通常我們會說標籤是HTML element。

![image](https://hackmd.io/_uploads/SkedJcZFa.png)

*. 某些HTML標籤只有opening tag，這種標籤被稱為self-closing tag。
### 巣狀元素(Nesting elements)
你可以把元素放進另一個元素裡面 — 這叫做巢套(nesting)。例如，p tag內部可放入strong tag。

小心注意， 這些元素必須要正確地開啟與關閉，它們與其他元素的內外關係要相當明確。若沒有正確的語法，可能導致網頁瀏覽器將無法解讀，只能盡可能地猜測我們的意思，因此我們很有可能會得到一個不如預期的結果。所以，別這樣做！！

*. W3C提供的HTML Validator可以確認HTML程式碼的正確性。

### 物件導向(Object-Oriented)
HTML標籤的設計方式是採用物件導向的想法。現實生活中的物件包含兩個部分：

1. 屬性(Attributes)
2. 行為(Methods)

例如，一台汽車的屬性包含廠牌、出廠年份、顏色、價格等等靜態屬性。動態行為則包含直走、亮燈、左轉、右轉、鳴喇叭等等。同理，每個 HTML標籤都有各自可以設定的屬性與行為。

### HTML Skeleton
基本的 HTML Skeleton是構建的每個 HTML 網頁所需的一組標籤。 HTML Skeleton的標籤告訴瀏覽器它正在讀取什麼類型的文件，沒有Skeleton的 HTML 文件將無法在 Web 瀏覽器中正確呈現。

在 HTML 中，`<head>` 標籤用於包含有關網頁的特定信息，通常是 meta data 。 這些信息包括文檔標題`<title>` tag（這是強制性的）、 script 或 script linking 以及 CSS 文件等內容。​

`<body>` 標籤定義文檔的正文。 `<body>` 元素包含 HTML 文檔的所有內容，例如標題、段落、圖像、超鏈接、表格、列表等。

### HTML常用標籤
* `<h1>` 到 `<h6>` 標籤用於定義 HTML 標題。 `<h1>` 定義最重要的標題。 `<h6>` 定義最不重要的標題。 注意：每頁只使用一個 `<h1>` - 這應該代表整個頁面的主要標題/主題。
:::danger
特別注意！！HTML標籤在瀏覽器有預設樣式，但預設樣式不應該被用來當作選擇標籤的依據！樣式可用CSS來做修改。HTML標籤的任務是定義整個網頁的架構，並非樣式。正確的使用HTML標籤可以讓網頁做到SEO (Search Engine Optimization)。
:::
* `<p>` 標籤定義了一個段落。 瀏覽器會自動在每個 `<p>` 元素之前和之後添加一個空行。
* HTML 中的 `<a>` 標籤(anchor tag)用於在網頁上創建超鏈接。 此超鏈接用於將網頁鏈接到其他網頁或同一網頁的某些部分。 它用於提供absolute linking或relative linking作為其“href” (hyptertext reference)值。 `<a>`標籤可以設定target屬性，來決定新頁面是否會開啟新的瀏覽器分頁。我們也可以用`<base>`標籤來定義所有`<a>`標籤的target。
* `<img>` 標籤用於在 HTML 頁面中嵌入圖像。src是圖片來源，alt是圖片無法顯示時使用的替代文字。
* `<ul>` 代表unordered list，而`<ol>`代表ordered list。

### 絕對路徑與相對路徑
絕對路徑使用完整的URL當作連結對象。當我們需要連結到不在我們伺服器內的資源時，就需要使用絕對路徑。

相對路徑可以連結到相對於目前文件的檔案。”.”代表目前html文件所在資料夾位置，”..” 代表上層的資料夾位置。

若使用”/”，則可從root directory向下連結。
:::danger
特別注意！文件與檔案名稱不建議中間留空白鍵，不然路徑設定很容易抓不到。
:::

### Block vs Inline elements
在 HTML 中有兩種重要元素類別 — block elements 和 inline elements 。

1. block elements 在頁面中組成一個可見區塊 — 它在頁面中單獨佔據一行，在它前後的內容都將以一個換行分隔。區塊級元素傾向於作為頁面上的結構化元素(structural elements)，舉凡段落、列表、導航選單(navigation menus)、頁尾(footers)等等皆是。區塊級元素不會巢套在 inline elements 中，但有可能會巢套其他 block elements 中。例如：`<div>`標籤。
2. inline elements 指的是放在 block elements 之中的內容，這些元素只由文件內容的一小部分組成，而非由完整段落或群組式內容組成。一個行內元素不會在文件中產生新的一行，它們通常只會出現在一段文字中，舉例來說，`<a>` 元素(超連結)就是其中一種，`<span>`也是。

### 表格製作
要製作表格，必須使用`<table>` 、 `<tr>` 、 `<th>`以及`<td>`標籤。`<table>` 標籤定義了整個表格，而 `<tr>` 標籤用於構建每一行。 `<td>`標籤定義實際數據，而`<th>`標籤定義 HTML 表格中的標題單元格。

另外， colspan 屬性定義表格單元格應跨越的列數。rowspan 則定義表格單元格應跨越的行數。

下列的標籤則是選擇性使用：`<thead>`、`<tbody>`以及`<tfoot>`。

### 表單製作
前端的HTML表單內資料通常會被傳送到後端伺服器，而伺服器把收到的資料存放到資料庫後，再回傳一個回應給客戶端。

HTML `<form>` 標籤的action屬性定義了在 HTML 文檔中提交表單時將表單數據發送到何處。

`<form>` 標籤的method 屬性告訴瀏覽器如何將表單數據發送到服務器。 使用GET的話， form data 會被附加到 action 指定的URL，並且用?分隔數據。GET通常用來向伺服器發送非隱密資料，或向伺服器請求資料。POST method 則會把資料隱藏起來。 POST通常用來向伺服器寄出隱密的資料（例如密碼），或用來向伺服器寄送需要被儲存或處理的資料。

在 `<form>` 標籤內的所有內容，有設定 name 屬性的資料才會被送到後端伺服器。

常見的 `<input>` 標籤的 type 屬性有 checkbox、email、file、number、password、radio、range。其他的屬性則包含 checked、max、min、maxlength、minlength、placeholder、required、value 等等。

`<button>`標籤若放在`<form>`標籤內，則預設的 type 是 submit。

### 其他資訊
1. HTML 中的註釋以 ==<! -- 開頭並以 -->== 結尾。
2. `<br>` 標籤插入一個換行符。此元素主要用於想要換行但不想要開始一個新的`<p>`標籤的時候，例如寫詩或寫住址，同個`<p>`內部會需要換行。`<hr>`標籤代表段落之間的主題中斷：例如，故事中的場景變化，或章節內的主題轉移。
3. 普通鍵盤上不存在數學運算符、箭頭、技術符號和形狀等符號。要將這些符號添加到 HTML 頁面，我們可以使用 HTML entity。 HTML entity 使用與號 (&) 開頭並以分號 (;) 結尾。
4. ==index.html== 是伺服器在目錄中查找的默認文件。
5. self-closing tag 和所有其他標籤之間的重要區別是自閉合標籤代表 void element。 img 和 br 等 void element 不能包含任何 content。 所有其他標籤可能（但不是必須）包含 content。
6. Favicon 是 favorites icon 的縮寫，瀏覽器可以將 favicon 顯示於瀏覽器的網址列中，也可置於書籤列表的網站名前。通常來說，icon 的檔案名稱會設定為==favicon.ico==。

### HTML Validators
通常來說，使用錯誤的HTML語法並不會造成整個瀏覽器無法將頁面顯示出來。即使HTML語法有錯，網頁瀏覽器仍然會盡可能的顯示網頁內容。然而，每個瀏覽器使用的排版引擎不盡相同，也許在某個瀏覽器上可以被容忍的問題，在其他瀏覽器上就會發生跑版或是無法顯示頁面的問題。

因此，為了確認HTML程式碼有符合規範，W3C有提供線上的HTML驗證器，連結為：[wsl驗證器](https://validator.w3.org/#validate_by_uri)。

若有發現紅色的錯誤，則從第一個錯誤開始處理。
