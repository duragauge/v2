---
title: "Tufte"
description: Testing Tufte style side notes
image: pic10.jpg
noindex: true
draft: true
---

There should be a margin note associated with this line of text.  {{% marnote "some_id" %}}  image and text inside margin note ![](/img/chapter-1/arrow_diagram_sandwiches_1.svg) {{% /marnote %}}

There should be a numbered side note associated with this line of text.  {{% sidenote "unique_id" %}}  text inside a sidenote {{% /sidenote %}}


In his later books{{% sidenote "sn-in-his-later"%}}<a href="http://www.edwardtufte.com/tufte/books_be">_Beautiful Evidence_</a>{{% /sidenote %}}, Tufte starts each section with a bit of vertical space, a non-indented paragraph, and the first few words of the sentence set in small caps. For this we use a span with the class `newthought`, as demonstrated at the beginning of this paragraph. Vertical spacing is accomplished separately through `<section>` tags. Be consistent: though we do so in this paragraph for the purpose of demonstration, do not alternate use of header elements and the `newthought` technique. Pick one approach and stick to it.
