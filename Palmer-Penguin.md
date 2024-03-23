Palmer Penguins
================
James Jeberson
2024-03-23

## Setting up my environment

Notes: Setting up my environment by loading the ‘tidyverse’ and
‘palmerpenguins’ packages

``` r
library(tidyverse)
library(palmerpenguins)
```

\#Visualizations Here we will go through a series of visualizations

## Flipper Length vs Body Mass by Species

Here we plot flipper length against body mass and look at the breakdown
by species

``` r
ggplot(penguins) +
  geom_point(mapping = aes(x = flipper_length_mm, y = body_mass_g, color = species, shape = species)) +
  labs("text", x = "Flipper Length in mm", y = "Body Mass in g")
```

![](Palmer-Penguin_files/figure-gfm/unnamed-chunk-1-1.png)<!-- -->

## Flipper Length vs Body Mass by Species

Here we plot flipper length against body mass and look at the breakdown
in sex for each species

### Adelie Species

Here we plot flipper length against body mass and look at the breakdown
in sex for **Adelie** species

``` r
penguins %>% 
  filter(species == "Adelie") %>% 
  ggplot() + 
  geom_point(mapping = aes(x = flipper_length_mm, y = body_mass_g, color = sex, shape = sex)) +
  labs("text", x = "Flipper Length in mm", y = "Body Mass in g")
```

![](Palmer-Penguin_files/figure-gfm/unnamed-chunk-2-1.png)<!-- -->

### Chinstrap Species

Here we plot flipper length against body mass and look at the breakdown
in sex for **Chinstrap** species

``` r
penguins %>% 
  filter(species == "Chinstrap") %>% 
  ggplot() + 
  geom_point(mapping = aes(x = flipper_length_mm, y = body_mass_g, color = sex, shape = sex)) +
  labs("text", x = "Flipper Length in mm", y = "Body Mass in g")
```

![](Palmer-Penguin_files/figure-gfm/unnamed-chunk-3-1.png)<!-- -->

### Gentoo Species

Here we plot flipper length against body mass and look at the breakdown
in sex for **Gentoo** species

``` r
penguins %>% 
  filter(species == "Gentoo") %>% 
  ggplot() + 
  geom_point(mapping = aes(x = flipper_length_mm, y = body_mass_g, color = sex, shape = sex)) +
  labs("text", x = "Flipper Length in mm", y = "Body Mass in g")
```

![](Palmer-Penguin_files/figure-gfm/unnamed-chunk-4-1.png)<!-- -->

## Flipper Length vs Body Mass by Species & Island

Here we plot flipper length against body mass and look at the breakdown
in species & island

``` r
ggplot(penguins) +
  geom_point(mapping = aes(x = flipper_length_mm, y = body_mass_g, color = species, shape = species)) +
  labs("text", x = "Flipper Length in mm", y = "Body Mass in g") +
  facet_wrap(~island)
```

![](Palmer-Penguin_files/figure-gfm/unnamed-chunk-5-1.png)<!-- -->
