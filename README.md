# Tutorial

This is my tutorial repository.
 ## Stock Quotes

We get stock quotes, like those below, from the consolidated tape.

-  The last trade could have taken place on any exchange. 

-  Input a ticker and get the most recent quote.

```{r, echo=FALSE, message=FALSE, warning=FALSE}
#{{{
library(quantmod)
## library(DT)
inputPanel(
    textInput(inputId = "ticker3", label = "Stock Ticker", value = "AAPL")
    )
div(renderDataTable({
    validate(
        need(input$ticker3 != "", "Input a valid US stock ticker.")
        )

    getQuote(input$ticker3)
}), style = "font-size:60%")
#}}}
```
<div class="MIfooter"><img src="mi.png" style="height:50px;"></div>

