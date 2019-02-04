---
title: "Example to post in Hugo"
date: 2019-02-03T14:22:20+05:30
draft: false
writer: "Example Author"
# Keep it a secret but the real author here is Swarnim :P

---
<!-- I recommend using default MD FORMATTING -->

Using some sample gist,
{{< gist spf13 7896402 >}}

<!-- For a specific file {{< gist spf13 7896402 "img.html" >}} -->

<hr/>
<hr/>

Highlighting code,
{{< highlight html >}}
<section id="main">
  <div>
   <h1 id="title">{{ .Title }}</h1>
    {{ range .Pages }}
        {{ .Render "summary"}}
    {{ end }}
  </div>
</section>
{{< /highlight >}}

<hr/>
<hr/>

Instagram linking,,,
{{< instagram BZBHr4Pg5Wd hidecaption >}}

<hr/>
<hr/>


Twitter,,
{{< tweet 989198118666162176 >}}
{{< tweet 960992715579125760 >}}