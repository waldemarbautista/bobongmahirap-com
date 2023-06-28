---
title: "I Code When I'm Sad"
date: 2008-06-16
tags: ["Frustrations"]
---

```
<?php

define('MESSAGE', '@Y2F0IDxmaWxlbmFtZT4gfCBncmVwICI#gPSAiIHwgY3V0IC1mMSAtZCIgIiB8IG$N1dCAtZjEgLWQiXyIgfCBjdXQgLWYxI%C1kInIiIHwgY3V0IC1mMiAtZCIkIg==');

$i = 0;

$miss_chars = array('@', '#', '$', '%');

$your_output = '';
while (count($miss_chars) > 0) {
    $your_output .= substr(MESSAGE, strpos(MESSAGE, $miss_chars[$i]) + 1, 31);
    unset($miss_chars[$i]);
    $i++;
}

echo "$your_output\n";

?>
```

---

> Waldemar Bautista said...  
> Ay sumabog ang layout.  
> Monday, June 16, 2008 1:16:00 AM 

> Wigi Vei ウィジヴェイ said...  
> ANAK NG TOKWA! MAHUSAY!  
> Monday, June 16, 2008 2:05:00 AM 

> Tonio SM said...  
> Ang bangis!  
> Monday, June 16, 2008 5:57:00 PM 

> Ardee Aram said...  
> mahoosaid!  
> Monday, June 16, 2008 9:52:00 PM 

> Waldemar Bautista said...  
> Ibibigay ko ang sagot kapag nasa mood na ako. Hehe.  
> Monday, June 16, 2008 11:46:00 PM 

> Wigi Vei ウィジヴェイ said...  
> Ang tanong eh kanino mo ibibigay ang sagot! Hahaha!  
> Tuesday, June 17, 2008 1:41:00 AM 

> Waldemar Bautista said...  
> Gagawan ko yan ng bagong code. Hehe.  
> Tuesday, June 17, 2008 12:05:00 PM 