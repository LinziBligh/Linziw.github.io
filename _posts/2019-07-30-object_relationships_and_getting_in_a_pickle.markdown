---
layout: post
title:      "Object Relationships and getting in a pickle."
date:       2019-07-30 20:15:27 +0000
permalink:  object_relationships_and_getting_in_a_pickle
---

So I got myself in a right old pickle whilst trying to complete the Has Many Objects through lab, and once I realised what my error was it was kind of embarrasingly simple, so I thought I would share it!

The premise of this lab was to understand "Has-Many-Through" relationships  and to construct relationships between models of Customers, Waiters, and Meals.

```
  def initialize (patient, date, doctor)
    @patient = patient
    @date = date
    @doctor = doctor
    @@all << self
    end
```


```
 def new_appointment(patient, date)
    Appointment.new(patient, date, self)
  end
```

```
def new_appointment(doctor, date)
  Appointment.new(self, date, doctor)
end
```

This is a snippet from each of my three classes that needed to talk to each other, unfortunately, before I reached this point I didnt realise that the order in which i listed my arguements in would make any difference between classes, but thats what was causing me all the errors! Any reference to each other (such as Appointment.new) needed them kept in the same order, "patient, date, appointment" or it would cause all sorts of errors!

Since realizing this it made the second half of the lab, with Songs, Artists and Albums much easier to work through!
I have since learnt about keyword arguments and how, if you use them it doesnt matter if you pass them in in the wrong order...handy!





