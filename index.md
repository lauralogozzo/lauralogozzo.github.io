---
title: 
feature_text: |
 
  
feature_image: "/images/ESSX-landscape.JPG"
excerpt: "Laura Logozzo is a PhD Candidate at Yale University School of the Environment"
---

<p align = "center">
I am a post-doctoral fellow in Dr. Matt Bogard's lab at the University of Lethbridge. Broadly, 
I am interested in carbon cycling in aquatic systems using field- and lab-based approaches. 

</p>
<p align = "center">
  Originally from Brooklyn, NY, I attended Fiorello H. LaGuardia High School, majoring in fine arts.
  I did my PhD with Dr. Pete Raymond at the Yale School of the Environment (YSE), 
  where I studied dissolved organic matter and iron cycling in large rivers.
  I received my B.S. and M.S. from CUNY City College of New York, where I studied Earth 
  and Atmospheric Sciences. My Master's thesis examined the export of colored dissolved 
  organic matter from Chesapeake Bay tidal marshes, and its subsequent photochemical and 
  microbial degradation in estuaries.
</p>

<p align="center" style ="font-family:'Helvetica',sans-serif;"> {% include button.html target="_blank" text="Read my CV" link="/assets/laura-logozzo-cv.pdf" color = "#7C7CD8" %} </p>

---
<h2 align="center" style="font-family:'Helvetica',sans-serif; font-weight:normal"> Featured Publications </h2>


    
<!-- Sticky - add sticky tag to the post you want to highlight here - tags: [sticky] -->
{% for post in site.posts %} 
{% if post.tags contains "sticky" %}
<div class="jumbotron">
    <div class="pl-4 pr-0 h-100 tofront">
    <img src="{{ post.image }}" caption="" position="left" align="left" width="300" height="800" style="padding:10px">

        <div class="row justify-content-between">
            <div class="col-md-6 pt-6 pb-6 pr-lg-4 align-self-center">
                <h4 class="mb-3"> <a href="{{site.baseurl}}{{post.url}}" class="btn btn-dark"> {{post.title}} </a> </h4>
                <p class="mb-3 lead">
                    {{ post.excerpt | strip_html | strip_newlines | truncate: 140 }}
                </p>
            </div>
            <div class="col-md-6 d-none d-md-block pr-0" style="background-size:cover;background-image:{{ post.image }};">	

            </div>
        </div>
    </div>
</div> 
{% endif %}
{% endfor %}

---



<h2 align="center" style="font-family:'Helvetica',sans-serif; font-weight:normal"> News </h2>

<div class="jumbotron">
    <div class="pl-4 pr-0 h-100 tofront">
    <img src="/images/Laura-BUNN-Winter.JPG" caption="" position="left" align="left" width="300" height="800" style="padding:10px">
        <div class="row justify-content-between">
            <div class="col-md-6 pt-6 pb-6 pr-lg-4 align-self-center">
                <h4 class="mb-3"> <a href="https://environment.yale.edu/sites/default/files/2022-07/2022CanopySpring_ForWeb.pdf" class="btn btn-dark" target = "_blank_"> Exploring the Depths of Water's Role in Climate Change </a> </h4>
                <h5> <i> Canopy Magazine </i> &middot; Spring 2022 &middot; pp. 28-35 </h5>
                <p class="mb-3 lead">
                    {{ "Aquatic ecosystems play an essential role in the greenhouse gas emissions cycle. Water bodies can sequester carbon – and they can also release emissions. Reducing these emissions and exploring ways of increasing their potential for carbon uptake is at the center of new climate research at YSE."
 | strip_html | strip_newlines | truncate: 140 }}
                </p>
            </div>
            <div class="col-md-6 d-none d-md-block pr-0" style="background-size:cover;background-image:{{ post.image }};">	

            </div>
        </div>
    </div>
</div> 


<div class="jumbotron">
    <div class="pl-4 pr-0 h-100 tofront">
    <img src="https://environment.yale.edu/sites/default/files/styles/large/public/content/images/4136/new-haven-promise-2.jpg?itok=Xdd3SHxl" caption="" position="left" align="left" width="300" height="800" style="padding:10px">
        <div class="row justify-content-between">
            <div class="col-md-6 pt-6 pb-6 pr-lg-4 align-self-center">
                <h4 class="mb-3"> <a href="https://environment.yale.edu/news/article/new-haven-promise-introduces-students-to-environmental-studies/" class="btn btn-dark" target = "_blank_"> New Haven Promise Inspires New 'Champions' for the Environment </a> </h4>
                <p class="mb-3 lead">
                    {{ "For Johnae McArthur, a University of Connecticut undergraduate and one of five New Haven Promise interns at F&ES this past summer, the experience was more than just a crash course in biogeochemistry or a chance to explore the woods near her hometown. It also set her on a new career path."
 | strip_html | strip_newlines | truncate: 140 }}
                </p>
            </div>
            <div class="col-md-6 d-none d-md-block pr-0" style="background-size:cover;background-image:{{ post.image }};">	

            </div>
        </div>
    </div>
</div> 
