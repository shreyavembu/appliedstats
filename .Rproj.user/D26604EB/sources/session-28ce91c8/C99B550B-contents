library(tidyverse)
data()
View(mpg)
?mpg
?mean

glimpse(mpg)

?filter

filter(mpg, cty>=20) #subsetting by rows
mpg_efficient<- filter(mpg, cty>=20)
View(mpg_efficient) #displaying all cars that have cty>=20

mpg_ford <- filter(mpg,manufacturer=="ford") #use ==
View(mpg_ford)

#add a column
#converting to mpg to km/l
mpg_metric <- mutate(mpg, cty_metric=0.425144*cty)
glimpse(mpg_metric)

#to make typing easier, %-%(pipe). all commands below will reflect on mpg ds.
# %>% (command+shift+m)

mpg_metric<- mpg %>% 
  mutate(cty_metric=0.425144*cty)

#how is the avg city milage(cty column) different in classes(class column)
#very long process to filter each and use mean. so use groupby 
mpg %>% 
  group_by(class) %>% 
  summarise(mean(cty), median(cty))

#data visualization with ggplot2

ggplot(mpg, aes(x=cty)) +
  geom_histogram()+
  labs(x="city mileage")

ggplot(mpg, aes(x=cty)) +
  geom_freqpoly()+
  labs(x="city mileage")

ggplot(mpg, aes(x=cty)) +
  geom_histogram()+
  geom_freqpoly()+
  labs(x="city mileage")

#city vs highway mileage

ggplot(mpg, aes(x=cty, y=hwy))+
  geom_point() + #scatter plot
  geom_smooth(method="lm") #a regression line

#class variable as colour
ggplot(mpg, aes(x=cty, y=hwy,color=class))+ 
  geom_point()+ 
  scale_color_brewer(palette="Dark2")


 



  

