---
layout: default
title: Home
---

<div class="archive-intro">
    <h2>📁 Content Archive</h2>
    <p>Welcome to the digital vault! Here's all the content available for AI conversations and training.</p>
</div>

<div class="file-list">
    <h3>📄 Available Files</h3>
    
    {% assign sorted_pages = site.pages | sort: 'name' %}
    {% for page in sorted_pages %}
        {% unless page.name == 'index.md' or page.name contains '404' or page.path contains '_layouts' or page.path contains 'assets' %}
            {% assign display_title = page.title | default: page.name | remove: '.md' | replace: '-', ' ' | replace: '_', ' ' | capitalize %}
            <div class="file-item">
                <span class="file-icon">📄</span>
                <a href="{{ page.url | relative_url }}" class="file-link">
                    {{ display_title }}
                </a>
                <span class="file-meta">
                    {% if page.date %}
                        • {{ page.date | date: "%Y-%m-%d" }}
                    {% endif %}
                </span>
            </div>
        {% endunless %}
    {% endfor %}
    
    {% for post in site.posts %}
        {% assign display_title = post.title | default: post.name | remove: '.md' | replace: '-', ' ' | replace: '_', ' ' | capitalize %}
        <div class="file-item">
            <span class="file-icon">📄</span>
            <a href="{{ post.url | relative_url }}" class="file-link">
                {{ display_title }}
            </a>
            <span class="file-meta">
                • {{ post.date | date: "%Y-%m-%d" }}
            </span>
        </div>
    {% endfor %}
</div>

<div class="stats-box">
    <h3>📊 Archive Stats</h3>
    <p>Total files: {{ site.pages.size | plus: site.posts.size | minus: 1 }}</p>
    <p>Last updated: {{ 'now' | date: "%Y-%m-%d %H:%M" }}</p>
</div>
