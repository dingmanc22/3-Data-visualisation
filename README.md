# 3-Data-visualisation
R for Data Science 

install.packages("tidyverse")
library(tidyverse)

mpg
#> # A tibble: 234 x 11
#>   manufacturer model displ  year   cyl trans      drv     cty   hwy fl    class 
#>   <chr>        <chr> <dbl> <int> <int> <chr>      <chr> <int> <int> <chr> <chr> 
#> 1 audi         a4      1.8  1999     4 auto(l5)   f        18    29 p     compa…
#> 2 audi         a4      1.8  1999     4 manual(m5) f        21    29 p     compa…
#> 3 audi         a4      2    2008     4 manual(m6) f        20    31 p     compa…
#> 4 audi         a4      2    2008     4 auto(av)   f        21    30 p     compa…
#> 5 audi         a4      2.8  1999     6 auto(l5)   f        16    26 p     compa…
#> 6 audi         a4      2.8  1999     6 manual(m5) f        18    26 p     compa…
#> # … with 228 more rows

ggplot(data = mpg) + 
   geom_point(mapping = aes(x = class, y = drv))
  
ggplot(data = mpg) + 
  geom_point(mapping = aes(x = displ, y = hwy, color = class))  
  
  ggplot(data = mpg) + 
  geom_point(mapping = aes(x = displ, y = hwy, size = class))
 
 ggplot(data = mpg) + 
  geom_point(mapping = aes(x = displ, y = hwy, alpha = class)) 

 ggplot(data = mpg) + 
  geom_point(mapping = aes(x = displ, y = hwy, shape = class)) 

ggplot(data = mpg) + 
  geom_point(mapping = aes(x = displ, y = hwy), color = "blue")
  
ggplot(data = mpg) + 
  geom_point(mapping = aes(x = displ, y = hwy, color = "blue"))
  
?function_name

ggplot(data = mpg) + 
  geom_point(mapping = aes(x = displ, y = hwy)) + 
  facet_wrap(~ class, nrow = 2)
  
  # week-1-github-and-r-coding-dingmanc22
