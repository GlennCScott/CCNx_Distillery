---
author:
  name: Glenn Scott
  email: glenn.scott@parc.com
layout: post
title: "C Code Example"
date: 2016-02-09 20:00
category : blog example
comments: true
tags:
- How to create a blog entry with images and code.
---
Lorem ipsum dolor sit amet, consectetur adipiscing elit. Curabitur at enim urna. Sed dapibus ex eu sapien accumsan, sed tempus purus suscipit. Vestibulum a ipsum nibh. Nulla et lectus non augue placerat vestibulum. Donec lorem augue, fermentum ut leo nec, feugiat gravida urna. Mauris lobortis ut nisl sit amet venenatis. Nulla quis vehicula ligula. Integer orci urna, congue in pharetra in, gravida at nunc. Nam vitae convallis nibh, quis lobortis urna. Donec nec ligula non augue fringilla fermentum. Etiam et est lorem. Integer arcu elit, aliquam ut posuere sed, interdum vel leo. Morbi tincidunt magna vel ullamcorper efficitur. Donec sit amet lectus iaculis dui ornare laoreet quis eu ex.

Place images in a subdirectory within `/images` named the same name as the blog post and reference them directly
<table border="0" align="center">
<tr>
<td><img src="/images/2015-05-10-c-code-example/PPD266-20140818.png" height="400" width="400"/></td>
<td><img src="/images/2015-05-10-c-code-example/PPD267-20140819.png" height="400" width="400"/></td>
</tr>
</table>

{% highlight C %}
uint32_t
parcAtomicInteger_Uint32IncrementGCC(uint32_t *value)
{
    return __sync_add_and_fetch(value, 1);
}

uint32_t
parcAtomicInteger_Uint32DecrementGCC(uint32_t *value)
{
    return __sync_sub_and_fetch(value, 1);
}

uint64_t
parcAtomicInteger_Uint64IncrementGCC(uint64_t *value)
{
    return __sync_add_and_fetch(value, 1);
}

uint64_t
parcAtomicInteger_Uint64DecrementGCC(uint64_t *value)
{
    return __sync_sub_and_fetch(value, 1);
}
{% endhighlight %}
