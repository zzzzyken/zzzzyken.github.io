---
layout: about
title: about
permalink: /
subtitle: M.S. student in Electrical and Computer Engineering, <a href='https://www.vanderbilt.edu/'>Vanderbilt University</a>

# To show a photo: save it as assets/img/prof_pic.jpg and uncomment the four lines below.
profile:
  align: right
  image: prof_pic.jpg
  image_circular: false # crops the image to make it circular

selected_papers: true # includes a list of papers marked as "selected={true}"
social: true # includes social icons at the bottom of the page

announcements:
  enabled: false # set to true after adding news items to a `_news` folder
  scrollable: true
  limit: 5

latest_posts:
  enabled: false
---

I am a master's student in Electrical and Computer Engineering at [Vanderbilt University](https://www.vanderbilt.edu/), where I work on medical image analysis with [Prof. Yuankai Huo](https://hrlblab.github.io/) and [Prof. He Zhao](https://www.liverpool.ac.uk/people/he-zhao) (University of Liverpool). Before Vanderbilt, I received my B.E. in Electronics and Information Engineering from Huazhong University of Science and Technology, and I spent the summer of 2024 at UC Berkeley as a visiting student.

My research interests are computer vision and medical image analysis, in particular domain generalization, interpretable deep learning and weakly supervised learning. I want models whose predictions can be traced to clinically meaningful evidence and that stay reliable on images from hospitals and devices they have never seen. My recent work studies diabetic retinopathy grading from color fundus photographs: [PARAGraph](/publications/) builds a hierarchical graph over retinal anatomy and lesions, and my latest project learns lesion prototypes from severity labels alone and grades directly from them.

I am applying to Ph.D. programs for Fall 2027.

<!-- Cats. Photos: assets/img/cats/kudryavka.jpg and assets/img/cats/donut.jpg (jpg, jpeg or png); a missing photo is simply skipped.
     Each round avatar is centred on the point (--fx, --fy) of the square-cropped photo and magnified by --zoom; adjust the three numbers per cat below. -->
<style>
  .cats { display: flex; align-items: center; gap: 0.9rem; flex-wrap: wrap; margin-bottom: 1.5rem; }
  .cats figure { margin: 0; flex: none; width: 96px; height: 96px; border-radius: 50%; overflow: hidden; box-shadow: 0 1px 4px rgba(0, 0, 0, 0.3); }
  .cats picture { display: block; width: 100%; height: 100%; }
  .cats img {
    display: block; width: 100%; height: 100%; object-fit: cover;
    transform-origin: var(--fx, 50%) var(--fy, 50%);
    transform: translate(calc(50% - var(--fx, 50%)), calc(50% - var(--fy, 50%))) scale(var(--zoom, 1));
  }
  .cats img[alt="kudryavka"] { --fx: 45%; --fy: 36%; --zoom: 1.6; }
  .cats img[alt="donut"] { --fx: 60%; --fy: 32%; --zoom: 1.75; }
  .cats p { margin: 0; flex: 1 1 16rem; }
</style>
{% assign cat_files = site.static_files | where_exp: "f", "f.path contains '/assets/img/cats/'" %}
{% assign cat_names = "kudryavka,donut" | split: "," %}
<div class="cats">
  {% for cat in cat_names %}
    {% for f in cat_files %}
      {% if f.basename == cat %}
        {% assign cat_path = f.path | remove_first: "/" %}
        {% include figure.liquid loading="lazy" path=cat_path sizes="192px" alt=cat title=cat %}
      {% endif %}
    {% endfor %}
  {% endfor %}
  <p>Outside of research, I live with two cats: <strong>Kudryavka</strong> the Russian Blue and <strong>Donut</strong> the Minuet.</p>
</div>
