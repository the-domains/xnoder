---
inFeed: true
description: >-
  I needed to generate a random, 32 character string to use as an encryption
  “secret” for an API that I’m working on, and came up with the following
  snippet:
dateModified: '2016-12-19T06:31:05.728Z'
datePublished: '2016-12-19T06:31:06.839Z'
title: A random string
author: []
publisher: {}
via: {}
hasPage: true
starred: false
datePublishedOriginal: '2016-12-19T06:31:04.007Z'
sourcePath: _posts/2016-12-19-a-random-string.md
url: a-random-string/index.html
_type: Article

---
# A random string

---

I needed to generate a random, 32 character string to use as an encryption "secret" for an API that I'm working on, and came up with the following snippet:

    import random
    import string
    
    randomish = ''.join(random.SystemRandom().choice(string.ascii_uppercase + string.digits) for _ in range(32))
    print(randomish)

It works well enough insofar as creating the said string is concerned, but I'll likely have to revisit the logic and the thoughts behind the idea when I actually get to the part of the code that needs to implement the secret.