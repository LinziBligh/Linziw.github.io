---
layout: post
title:      "Update and instance methods"
date:       2019-07-07 01:37:51 -0400
permalink:  update_and_instance_methods
---

Just to start with, a quick update from my last blog post...I accepted voluntary redundancy! Feeling both terrified and excited, but mostly excited, I cant wait to be able be at home and study the rest of the course as close to full time as I can. I'm excited that I'll be able to feel a bit more "in the gang" and be able to actually use the "ask a question" feature, attend community meetups and the live tutorials which currently I can't as I work full-time and the time-zones clash, which has felt very isolating.  Making the decision has also been a real mental boost, I'm going to have to make this career change happen now, thats it, I'm "all-in".

So all being well, in 3 months time when I leave,  I'll be writing a blog post from home, and be somewhere near to halfway though the syllabus and be able to really push through the second half at a much faster pace, rather than shoe-horning  in small sessions at 5am and during my breaks at work as I do currently.

So it's been suggested to me to write about instance methods, so I'm mostly writing this for my own benefit just to get this clearer in my head more than anything.



 Instance Methods

Methods defined within an object's class are called Instance Methods because they are methods that belong to any instance of the class. 

They are built in the same way as ordinary methods, using the def keyword and end, but they are enclosed within the body of the class itself. 

They can only be used with instances of that class, and not in general in the rest of our program, you can't just call the method without the instance.

```
class Unicorn
  def poop
  puts "Your Unicorn pooped glitter"
  end
end

   unicorn = Unicorn.new
=> #<Unicorn:0x000055c20bef5ab0>
   unicorn.poop
Your Unicorn pooped glitter
```



Hope that makes sense!




