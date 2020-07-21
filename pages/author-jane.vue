<template>
<div class="container">
    <div class="row justify-content-center">
        <div class="col-md-8">
            <div class="row align-items-center mb-5">
                <div class="col-md-9">
                    <h2 class="font-weight-bold">标题<span
                            class="small btn btn-outline-success btn-sm btn-round"><a
                                href="#">Follow</a></span></h2>
                    <p><a href="#">site</a></p>
                    <p class="excerpt">作者简介</p>
                </div>
                <div class="col-md-3 text-right">
                    <img alt="名称" src="/a.jpeg"
                        class="rounded-circle" height="100" width="100">
                </div>
            </div>
            <h4 class="font-weight-bold spanborder"><span>标题</span></h4>
            <!-- {% assign posts = site.posts | where:"author","jane" %}
            {% for post in posts %}
            {% include main-loop-card.html %}
            {% endfor %} -->
        </div>
    </div>
</div>
</template>