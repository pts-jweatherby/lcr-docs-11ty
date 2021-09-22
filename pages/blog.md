---
layout: layouts/blog.njk
title: Blog
metaDescription: A sample Blog page listing various posts and authors.
date: 2017-01-01
permalink: /blog/index.html
eleventyNavigation:
  key: Blog
  order: 2
---
![](/static/img/screen-shot-2021-09-07-at-9.58.40-am.png)

This is a test

```javascript
export default function Template({
  data, // this prop will be injected by the GraphQL query below.
}) {
  const { markdownRemark } = data; // data.markdownRemark holds your post data
  const { frontmatter, html } = markdownRemark;
  return (
    <Layout title={frontmatter.title} showGoHome={true}>
      <div
        className="blog-post-content"
        dangerouslySetInnerHTML={{ __html: html }}
      />
    </Layout>
  );
}
```