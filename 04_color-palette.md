---
title:
permalink: /Color-Palette/
order: 
feature_text: <h1 style="color:#FFFFFF; font-family:sans-serif; font-weight:normal"> Color Palette </h1>
feature_image: "/images/myCols-All.svg"

---
A set of functions to plot the available color palettes (see plotCols) and to load a color
palette into your global environment (see getCols). Load these functions into R using:
<pre>
  <code>
source("https://lauralogozzo.github.io/assets/myCols.R.txt")
  </code>
</pre>

<h3> Functions and Examples </h3>

Function to display all available color palettes, and their names:
<pre>
  <code>
plotCols()
  </code>
</pre>
{% include figure.html image="/images/myCols-Scale.svg" caption="Color Scale Palettes" width="500" height="800" %}
{% include figure.html image="/images/myCols-Discrete.svg" caption="Discrete Color Palettes" width="500" height="800"%}

Function to create color palette by palette name, and a plotting example using ggplot:
<pre>
  <code>
# Load ggplot
library('ggplot2')

# Creates a global environment object named 'myCols' that contains the chosen palette
getCols("nausicaa")

# Get iris data
data(iris)

# Ggplot example
ggplot(data=iris, aes(Petal.Length,Sepal.Length, color = Species)) +
  geom_point(size = 2)+
  scale_color_manual(values = myCols) +
  theme_classic()

  </code>
</pre>

{% include figure.html image="/images/ggplot-Example.svg" caption="Plotted species (categorical) by color using the chosen palette - ggplot" width="500" height="800" %}

An example of a gradient palette for continuous data in ggplot:
<pre>
  <code>
# Load ggplot
library('ggplot2')

# Get color palette
getCols("sunset")

# Plot continuous scale
ggplot(data=iris, aes(Petal.Length,Sepal.Length, color = Petal.Width)) +
  geom_point(size = 2) +
  scale_color_gradientn(colors = rev(myCols)) +
  theme_classic()

  </code>
</pre>

{% include figure.html image="/images/ggplot-Scale-Example.svg" caption="Plotted petal width (continuous) by color using the chosen palette - ggplot" width="500" height="800" %}


