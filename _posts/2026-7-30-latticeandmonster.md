---
layout: post
title: "格点与最密堆积"
subtitle: "以及一点魔群和顶点代数"
header-img: "img/post-bg-infinity.jpg"
header-mask: 0.3
math: true
tags:
  - 格点
  - 最密堆积
  - 模形式
  - 群论
  - 魔群
  - 顶点代数
  - 代数
---

<div id="pdf-gallery" class="pdf-images"></div>
<script>
  const prefix = "{{ site.baseurl }}/img/格点__最密堆积__魔群以及顶点代数/格点__最密堆积__魔群以及顶点代数_page-";
  const totalPages = 16;
  const container = document.getElementById('pdf-gallery');
  container.style.lineHeight = "0";
  container.style.fontSize = "0";
  container.style.margin = "0";
  container.style.padding = "0";
  
  for (let i = 1; i <= totalPages; i++) {
    const pageNum = i.toString().padStart(4, '0');
    const imgSrc = prefix + pageNum + '.jpg';
    const picture = document.createElement('picture');
    const img = document.createElement('img');
    img.src = imgSrc;
    img.alt = `Page ${i}`;
    img.loading = 'lazy';
    img.style.display = "block";
    img.style.margin = "0";
    img.style.padding = "0";
    img.style.border = "none";
    img.style.verticalAlign = "top";
    img.style.width = "100%";
    img.style.height = "auto";
    picture.style.display = "block";
    picture.style.margin = "0";
    picture.style.padding = "0";
    picture.style.lineHeight = "0";
    picture.style.fontSize = "0";
    picture.appendChild(img);
    container.appendChild(picture);
  }
</script>

pdf:<a href="{{ site.baseurl }}/pdf/格点__最密堆积__魔群以及顶点代数.pdf">格点, 最密堆积, 魔群以及顶点代数</a>.
