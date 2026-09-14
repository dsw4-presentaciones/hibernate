---
# You can also start simply with 'default'
theme: seriph
# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
#background: /PORTADA.jpeg
layout: image
image: /portada.jpeg
backgroundSize: contain
# some information about your slides (markdown enabled)
title: Hibernate
info: |
  ## Clase de Hibernate Informática Empresarial, SA-RP
# apply unocss classes to the current slide
class: text-center
# https://sli.dev/features/drawing
drawings:
  persist: false
# slide transition: https://sli.dev/guide/animations.html#slide-transitions
transition: slide-left
# enable MDC Syntax: https://sli.dev/features/mdc
mdc: true
author: Alvaro Mena Monge
hideInToc: true
style: './uno.css'
themeConfig:
  primary: '#005A9C'
---

<br> <br>
<div style="font-size: 30px;">
  ORMs, JPA y Hibernate
</div>
 <br>



IF0009 Desarrollo de software 4
<br>
MSI. Álvaro Mena Monge


<div @click="$slidev.nav.next" class="mt-12 py-1" hover:bg="white op-10">
  Presione espaciadora para avanzar <carbon:arrow-right />
</div>

<div class="abs-br m-6 text-xl">
  <a href="https://github.com/slidevjs/slidev" target="_blank" class="slidev-icon-btn">
    <carbon:logo-github />
  </a>
</div>

<!--
comentario 
-->
---
layout: two-cols
hideInToc: true
showTocNumber: false
---
# Tabla de contenidos 

::right::
<Toc text-sm minDepth="1" maxDepth="1" />
<!--
You can have `style` tag in markdown to override the style for the current page.
Learn more: https://sli.dev/features/slide-scope-style
-->



---
src: ./pages/clase1_orm_jpa_hibernate.md
hide: false
---
---
src: ./pages/clase0_creacion_db.md
hide: false
---
---
src: ./pages/clase2_creacion_proyecto.md
hide: false
---

---
src: ./pages/clase3_jpa_one_to_one_uni_crud.md
hide: false
---

