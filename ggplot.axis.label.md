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
