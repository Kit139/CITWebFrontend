<template>
  <div class="container">

    {% if page.url == "/" %}

    <!-- Begin post excerpts, let's highlight the first 4 posts on top -->
    <div class="row remove-site-content-margin">

      <!-- latest post -->
      <!-- {% assign latest_post = site.posts[0] %} -->
      <div class="col-md-6">
        <div class="card border-0 mb-4 box-shadow">
          <a href="#">
            <div class="topfirstimage"
                 style="background-image: url(/a.jpeg); height: 200px;    background-size: cover;    background-repeat: no-repeat;"></div>
          </a>
          <div class="card-body px-0 pb-0 d-flex flex-column align-items-start">
            <h2 class="h4 font-weight-bold">
              <a class="text-dark"
                 href="#">标题</a>
            </h2>
            <p class="excerpt">
              啊啊啊啊啊啊啊啊啊啊啊啊
            </p>
            <div>
              <small class="d-block text-muted">
                In <span class="catlist">
                  <!-- {% for category in latest_post.categories %} -->
                  <a class="text-capitalize text-muted smoothscroll"
                     href="#">{{ category }}</a><span class="sep">, </span>
                  <!-- {% endfor %} -->
                </span>
              </small>
              <small class="text-muted">
                date
              </small>
            </div>
          </div>
        </div>
      </div>

      <div class="col-md-6">

        <!-- second latest post -->
        <!-- {%- assign second_post = site.posts[1] -%}         -->
        <div class="mb-3 d-flex align-items-center">
          <!-- {% if second_post.image %} -->
          <div class="col-md-4">
            <a href="#">
              <img class="w-100"
                   src="/a.jpeg"
                   alt="#">
            </a>
          </div>
          <!-- {% endif %}                 -->
          <div>
            <h2 class="mb-2 h6 font-weight-bold">
              <a class="text-dark"
                 href="#">标题</a>
            </h2>
            <small class="d-block text-muted">
              In <span class="catlist">
                <!-- {% for category in second_post.categories %} -->
                <a class="text-capitalize text-muted smoothscroll"
                   href="#">{{ category }}</a><span class="sep">, </span>
                <!-- {% endfor %} -->
              </span>
            </small>
            <small class="text-muted">
              date
            </small>
          </div>
        </div>

        <!-- third latest post -->
        <!-- {%- assign third_post = site.posts[2] -%}         -->
        <div class="mb-3 d-flex align-items-center">
          <!-- {% if third_post.image %} -->
          <div class="col-md-4">
            <a href="#">
              <img class="w-100"
                   src="/a.jpeg"
                   alt="">
            </a>
          </div>
          <!-- {% endif %}                 -->
          <div>
            <h2 class="mb-2 h6 font-weight-bold">
              <a class="text-dark"
                 href="#">标题</a>
            </h2>
            <small class="d-block text-muted">
              In <span class="catlist">
                <!-- {% for category in third_post.categories %} -->
                <a class="text-capitalize text-muted smoothscroll"
                   href="#">{{ category }}</a><span class="sep">, </span>
                <!-- {% endfor %} -->
              </span>
            </small>
            <small class="text-muted">
              date
            </small>
          </div>
        </div>

        <!-- fourth latest post -->
        <!-- {%- assign fourth_post = site.posts[3] -%}         -->
        <div class="mb-3 d-flex align-items-center">
          <!-- {% if fourth_post.image %} -->
          <div class="col-md-4">
            <a href="#">
              <img class="w-100"
                   src="/a.jpeg"
                   alt="">
            </a>
          </div>
          <!-- {% endif %}                 -->
          <div>
            <h2 class="mb-2 h6 font-weight-bold">
              <a class="text-dark"
                 href="#">标题</a>
            </h2>
            <small class="d-block text-muted">
              In <span class="catlist">
                <!-- {% for category in fourth_post.categories %} -->
                <a class="text-capitalize text-muted smoothscroll"
                   href="#">{{ category }}</a><span class="sep">, </span>
                <!-- {% endfor %} -->
              </span>
            </small>
            <small class="text-muted">
              date
            </small>
          </div>
        </div>

      </div>

    </div>

    <!-- Sticky - add sticky tag to the post you want to highlight here - tags: [sticky] -->
    <!-- {% for post in site.posts %} 
{% if post.tags contains "sticky" %} -->
    <div class="jumbotron jumbotron-fluid jumbotron-home pt-0 pb-0 mt-3 mb-2rem bg-lightblue position-relative">
      <div class="pl-4 pr-0 h-100 tofront">
        <div class="row justify-content-between">
          <div class="col-md-6 pt-6 pb-6 pr-lg-4 align-self-center">
            <h1 class="mb-3">标题</h1>
            <p class="mb-3 lead">
              文章简要
            </p>
            <a href="#"
               class="btn btn-dark">Read More</a>
          </div>
          <div class="col-md-6 d-none d-md-block pr-0"
               style="background-size:cover;background-image:url(/a.jpeg);">
          </div>
        </div>
      </div>
    </div>
    <!-- {% endif %}
{% endfor %} -->

    <!-- {% endif %} endif page url is / -->

    <!-- Now the rest of the posts with the usual loop but with an offset:4 on the first page so we can skeep the first 4 posts displayed above -->

    <div class="row mt-3">

      <div class="col-md-8 main-loop">

        <h4 class="font-weight-bold spanborder"><span>All Stories</span></h4>

        <!-- {% for post in paginator.posts %} -->

        <!-- {% include main-loop-card.html %} -->
          <MainLoopCard />

        <!-- {% endfor %} -->

        <div class="mt-5">
          <!-- Pagination links -->
          <!-- {% if paginator.total_pages > 1 %} -->
          <ul class="pagination">
            <!-- {% if paginator.previous_page %} -->
            <li class="page-item"><a class="page-link"
                 href="#">&laquo; Prev</a></li>
            <!-- {% else %} -->
            <li class="page-item disabled"><span class="prev page-link">&laquo;</span></li>
            <!-- {% endif %} -->

            <!-- {% for page in (1..paginator.total_pages) %}
                {% if page == paginator.page %} -->
            <li class="page-item disabled"><span class="webjeda page-link">{{ page }}</span></li>
            <!-- {% elsif page == 1 %} -->
            <li class="page-item"><a class="page-link"
                 href="#">{{ page }}</a></li>
            <!-- {% else %} -->
            <li class="page-item"><a class="page-link"
                 href="#">{{ page }}</a></li>
            <!-- {% endif %}
              {% endfor %}

              {% if paginator.next_page %} -->
            <li class="page-item"><a class="page-link"
                 href="#">Next &raquo;</a></li>
            <!-- {% else %} -->
            <li class="page-item disabled"><span class="next page-link">&raquo;</span></li>
            <!-- {% endif %} -->
          </ul>
          <!-- {% endif %}       -->
        </div>

      </div>

      <div class="col-md-4">
        <!-- {% include sidebar-featured.html %} -->
        <SiderBarFeatured />
      </div>

    </div>

  </div>
</template>

<script>
import SiderBarFeatured from "./SidebarFeatured"
import MainLoopCard from "./Mainloopcard"
export default {
    components:{
        SiderBarFeatured,
        MainLoopCard
    }
}
</script>