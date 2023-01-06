## tips

1. post中的文件名不要重复，可以随便起，无所谓

2. 去掉右侧panel的最近更新和热门标签，去layouts-page.html，搜trending即可

3. 更改所有中文名，比如sidebar里tag的名字，去zh-CN文件里改

4. 在首页增加摘要，需要在/_layouts/home.html 增加

   ```
       <div class="post-excerpt">
       {{ post.excerpt }}
       </div>
   ```

   且删除

   ```
       <div class="post-content">
         <p>
           {% include no-linenos.html content=post.content %}
           {{ content | markdownify | strip_html | truncate: 200 | escape }}
         </p>
       </div>
   ```

   

5. 调整首页的摘要布局，需要把/_sass/layout/home.scss里的

   

   ```
         .post-content {
         margin-top: 0.6rem;
         margin-bottom: 0.6rem;
         color: var(--post-list-text-color);
         }
   ```

   替换为

   ```
   .post-excerpt {
         margin-top: 1.6rem;
         margin-bottom: 0.6rem;
         color: var(--sidebar-active-color);
         font-size:1.2rem;
         font-weight:500;
         }
   ```

   

6. post页删除摘要，需要删除在/_layouts/post.html 里的

   ```
   <div class="post-meta text-muted">
   ```

   整个部分

7. 增大post页右侧导航的字号，在/_sass/layout/post.scss 里增加

   ```
   #toc li a {
     font-size: 1rem;
     
     &.nav-link:not(.active) {
       color: #ababab;
     }
   }
   ```

   

   <div class="post-meta text-muted">

