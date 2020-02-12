# Mini_Project1_SDS192
```{r setup, include=FALSE}
knitr::opts_chunk$set(echo = TRUE)
```

```{r}
library(fivethirtyeight)
library(ggthemes)
library(tidyverse)
data("drug_use")
drug_usage <- ggplot(drug_use, aes(y = cocaine_use, x = age, fill = cocaine_freq))

drug_usage + 
  geom_col() +
  theme_solarized() + 
  scale_fill_distiller(palette = "Greens", direction = 1, name = "Cocaine 
Consumption
Frequency
(median times
last year)") + 
  scale_x_discrete(name = "Age (12 to 65)") + 
  scale_y_continuous(name = "Percentage Surveyed Who Used Cocaine")

view(drug_use)

--
