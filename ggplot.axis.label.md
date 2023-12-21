[Superscript and subscript axis labels in ggplot2 in R](https://www.geeksforgeeks.org/superscript-and-subscript-axis-labels-in-ggplot2-in-r/)

```
# Load ggplot2 Package 
library("ggplot2") 
  
# Create a DataFrame For Plotting 
DF <- data.frame(X = rnorm(10),                         
                 Y = rnorm(10)) 
  
# Create ggplot2 ScatterPlot with SuperScripted  
# value of Label of Axis. 
ggplot(DF,aes(X, Y))+ 
  geom_point(size = 8, fill = "green",  
             color = "black", shape = 21)+ 
  xlab(bquote(X-Axis^superscript))+ 
  ylab(bquote(Y-Axis^superscript))
```
[Math Notation for R Plot Titles: expression and bquote](https://www.r-bloggers.com/2018/03/math-notation-for-r-plot-titles-expression-and-bquote/)
```
## A variable to pass in
cor <- -.321
cor2 <- '-.321'
par(mfrow = c(1, 2))
plot(1:10, 1:10, main = bquote("Hello" ~ r[xy] == .(cor) ~ "and" ~ B^2))
plot(1:10, 1:10, main = bquote("Hello" ~ r[xy] == .(cor2) ~ "and" ~ B^2))

plot(1:10, 1:10, main = parse(text = paste0('"Hello"', ' ~ r[xy] == ', cor2, '~ B^2')))
```
[data analytics](https://www.dataanalytics.org.uk/axis-labels-in-r-plots-using-expression/)

The expression() command
The expression() command takes regular characters and uses them in a special way, allowing you to build more complicated strings. You don’t need quotes (most of the time) as the usual letters and numbers are not “interpreted”. R usually takes strings that are un-quoted and tries to interpret them as objects or commands.

What the expression() command does do though, is to look for certain characters or phrases, which are treated as “switches” that do something, like turn on superscript or bold font.

~ Acts as a space character (actual spaces are ignored in R commands).
* Acts as a connector, this allows you to join several elements.
“” Quotes are used to enclose items that would otherwise be treated as a special character (like ~ or *).
So, type a ~ when you want a space and “~” when you want a ~. The * is a connector, which can be used to join sections of the expression. This allows you to “turn off” superscript for example, or switch font face.

There are various “reserved” characters e.g. + – / * ? ^ (mostly they are not letters or numbers), and these should be inside quotes. Items in quotes should be bracketed by ~ and/or * characters.

When you type an expression() any spaces you type are ignored. You can type spaces to help yourself see clearly what you have typed but they are all stripped out. If you display an expression() result R will place a single space (for clarity) between various elements of your expression().


[Hao LAb](https://www.haowulab.org/computing/Rtips/plotmath.html)

{Rstudio](https://rstudio-pubs-static.s3.amazonaws.com/607873_cd3b916b5d534899a88f271e8afc3827.html)


# less than or equal to \u2264  AND greater than or equal to \u2265 symbols
```
ggplot(DF,aes(X, Y))+ 
  geom_point(size = 8, fill = "green",  
             color = "black", shape = 21)+ 
  xlab(bquote(X-Axis^superscript))+ 
  ylab(expression("Fraction of gene(\u2264"~log[2]*(CPM)*")"))
```
