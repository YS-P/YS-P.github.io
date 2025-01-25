---
layout: page
title: About the Author
permalink: /about
comments: False
---

<div class="row justify-content-between">
  <!-- Left Column: Author 소개 -->
  <div class="col-md-4">
    <div class="sticky-top sticky-top-80 text-center">
      <img
        src="{{ site.baseurl }}/assets/images/2han_prof.jpg"
        alt="Author Avatar"
        class="rounded-circle shadow-lg mb-3"
        style="width: 150px; height: 150px; object-fit: cover;"
      />
      <h5 class="mt-3">{{ site.authors.2han.name }}</h5>
      <p>
        BSc. Cryptography & InfoSec<br>
        MSc. Data Science (In Progress)</p>

      <!-- Divider -->
      <hr style="width: 30px; margin: 10px auto; border: 1px solid #ccc;">

      <!-- GitHub & Email Icons -->
      <div class="social-icons d-flex justify-content-center mt-3">
        <!-- GitHub Icon -->
        <a href="{{ site.authors.2han.github }}" target="_blank" class="mx-2">
          <i class="fab fa-github fa-lg text-secondary"></i>
        </a>
        <!-- Email Icon with Tooltip -->
        <a href="mailto:{{ site.authors.2han.email }}" data-toggle="tooltip" data-original-title="{{ site.authors.2han.email }}" class="mx-2">
            <i class="fas fa-envelope fa-lg text-secondary"></i>
        </a>
      </div>
    </div>
  </div>

  <!-- Main Content -->
  <div class="col-md-8 pr-5">
    <p>
      This website was created to study and organize topics of my interest. As a result, the subjects might be a bit all over the place🤣.<br>Most of the code will be shared via GitHub, and while the content will be written in English, some topics may be written in Korean depending on the subject. For more details, please read below!
    </p>
    <h4>Interests</h4>
      <p class="mb-3 text-center">
        <img class="shadow-lg" src="{{ site.baseurl }}/assets/images/interests.png"
            alt="jekyll template mediumish" />
      </p>
      <p class="mb-3" style="text-align: left;">
        This word cloud was generated from my previous CV, so it may contain some unrelated topics 😅. Along with the topics shown here, I also have a strong interest in app development and other related fields.
      </p>
    <div class="preferred-languages">
    <h4>Preferred Languages</h4>
    <ul class="languages-list">
      <li>
        <i class="fab fa-python"></i> Python
      </li>
      <li>
        <i class="fas fa-code"></i> C++
      </li>
      <li>
        <i class="fas fa-code"></i> C
      </li>
      <li>
        <i class="fas fa-code"></i> Java
      </li>
    </ul>
    </div>
