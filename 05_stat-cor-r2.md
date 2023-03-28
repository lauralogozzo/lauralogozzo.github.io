---
title:
permalink: /stat-cor-r2/
order: 
feature_text: <h1 style="color:#FFFFFF; font-family:sans-serif; font-weight:normal"> stat_cor_r2 </h1>
feature_image: "/assets/orange-color.svg"

---
A function modified from the stat_cor() function in <em>ggpubr</em> to add the 
R<font size = 2><sup>2</sup></font> value and <em>p</em>-value to <em>ggplot</em>
for a linear model.

Requires the packages <em>ggplot2</em>, <em>ggpubr</em>, and <em>finalfit</em>.

<h3> Load Function into Global Environment </h3>
<pre>
  <code>
source("https://lauralogozzo.github.io/assets/stat_cor_r2.R.txt")
  </code>
</pre>

<h3> Documentation </h3>

<pre>
  <code>
stat_cor_r2(
  mapping = NULL,
  data = NULL,
  label.x.npc = "left",
  label.y.npc = "top",
  output.type = "expression",
  digits = 2,
  r.digits = digits,
  p.digits = digits,
  geom = "text",
  position = "identity",
  na.rm = FALSE,
  show.legend = NA,
  inherit.aes = TRUE,
  ...
)
  </code>
</pre>

See documentation for stat_cor() from <em>ggpubr</em>.

<h3> Examples </h3>
<pre>
  <code>
# Load required packages
library("ggplot2")
library("ggpubr")
library("finalfit")

# Load iris data
data(iris)

# Plot scatterplot and add r2 and p-value
ggplot(data = iris, aes(x = Sepal.Length, y = Petal.Length)) + 
  geom_point(size = 2) + 
  geom_smooth(method = "lm") + 
  theme_classic(base_size = 14) +
  stat_cor_r2(size = 5)
  </code>
</pre>
{% include figure.html image="/images/stat-cor-r2.svg" caption="Default is to add 
R<sup><font size = 1>2</font></sup> and <em>p</em>-value to the top-left" width="500" height="800"%}


<pre>
  <code>
# Load ggplot
library("ggplot2")
library("ggpubr")
library("finalfit")

# Get iris data
data(iris)

# Ggplot example
ggplot(data = iris, aes(x = Sepal.Length, y = Sepal.Width)) + 
  geom_point(size = 2) + 
  geom_smooth(method = "lm") + 
  theme_classic(base_size = 14) + 
  stat_cor_r2(size = 6, label.x.npc = "center", r.digits = 3)

  </code>
</pre>

{% include figure.html image="/images/stat-cor-r2-v2.svg" caption="Move to top-right quadrant and change R<sup><font size = 1>2</font></sup> significant figures to three." width="500" height="800" %}


<pre>
  <code>
# Load ggplot
library("ggplot2")
library("ggpubr")
library("finalfit")

# Get iris data
data(iris)

# Ggplot example
ggplot(data = iris, aes(x = Sepal.Length, y = Sepal.Width, color = Species)) + 
  geom_point(size = 2) + 
  geom_smooth(method = "lm", se = F) + 
  theme_classic(base_size = 14) + 
  stat_cor_r2(size = 5, label.x.npc = "center", show.legend = F)
  </code>
</pre>

{% include figure.html image="/images/stat-cor-r2-species.svg" caption="" width="500" height="800" %}