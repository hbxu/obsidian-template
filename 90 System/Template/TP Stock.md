<%*
let symbolName = await tp.system.prompt("Enter stock symbol")
let type = await tp.system.suggester(["Portfolio", "Watchlist"], ["Portfolio", "Watchlist"])
await tp.file.move("/90 System/Stock/" + symbolName);
-%>
---
tags: [ctx-stock-symbol]
---
links:: [[<% type %>]]
`="<iframe src=\"https://www.tradingview-widget.com/embed-widget/mini-symbol-overview/?locale=en&colorTheme=dark&symbol=" + this.file.name + "\" width=\"200\" frameborder=\"0\" scrolling=\"no\" allowfullscreen></iframe>"`
