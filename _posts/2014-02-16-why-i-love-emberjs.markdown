---
layout: post
title: Why I Love EmberJS
published: true
---

I've fallen in love with EmberJS recently and to be completely open, I'm
surprised at myself. I don't like Javascript, I detest it. It is not that I
don't like the langauge (I don't), it is more that I've found that when working
with large amounts of it on a web page, it tends to be the source of a large
number of bugs. I've worked with apps that use a 'large' amount of jQuery,
some that use server-rendered Javascript and even Backbone apps and none have
thrilled me. They all seem to have javscript as a second thought, even those
that are 'Single Page Apps'. You have to constantly 'think' about the fact that
you are doing something that is not normal. You have to constantly think about
the fact that you are rewriting the DOM and has to be at the front of everything
you do. Ember changes all of this, Ember takes over and you can (almost) forget
that you are writing a web app!

# Stop thinking about the Web!
Ember takes over your entire page. I don't think about needing to remove or add
a DOM element, I think about removing or showing content based on something. I
don't think about redrawing the screen because the user clicked a link, I think
about rendering a new page. Ember makes this all seamless. I don't think about
working in Javascript! Ember comes very close to building an desktop
application and just makes it accessible via the web. I think about all my
interactivity in the app in one place, and just like I would in Rails, I think
about my data store seperately. I access that all through Ember-Data. Now, in
truth, I do have to spend a bit more time thinkinng about that because it isn't
just 'magic' as ActiveRecord is, you still have to build an API, but it at least
puts a layer of seperation between your data and your interactions.

# Why does this matter?
Interaction is the key to any application, we all know this. Making it trivial
to add or remove elements on the page, update them in realtime or modify them
quickly means you can create better, more fluid and more user friendly
interfaces. Previously this has come at the huge cost of bugs, additional time
to develop and a lot of extra thinking and management. Ember solves a fair
number of these problems. By abstracting out a large amount of your work, Ember
allows you to build your application as an application, not as a conglamaration
of small bits and pieces. This makes the code much easier to read. It also tends
to lead to a lot less bugs, at least in my experience. The performance is a
debate that I refuse to go into. Sometimes Single Page Apps are faster,
sometimes they aren't. Caching is harder. This post isn't about that and if
performance is large concern, please do the research on all parts and make the
best decision.

With any positive, there are downsides; you are still working in a split model.
You will now be developing one application that is your UI and one application
that is your API. For testing I've found this to be a huge blessing. I can write
feature specs that are only in javascript but given me nearly full test coverage
and write my API specs seperately. I write a feature 'integration' tests that
hit the entire application together and all told, my spec suite speeds up
considerably. Unfortunately, you still have two apps. Two applications to
maintain, two languages to be familiar with and two paradigms to think about.
This is definitely a tradeoff but in Ember, I've found it to be less of a
problem. Rails is ONLY my API. It will serve no other purpose. I am only
rendering a single page and from that point, Ember takes over. Rails is my
datasource and my background worker. I personally really enjoy this layer of
abstraction.

# A Different Kind of Thinking
Your users don't care if your app is Ember, Angular, Backbone, Rails or Django.
They don't know and they don't care. They only care about the interactions and
how things work. When I'm working in Ember, I feel like I am much more willing
to design the application with interactions that users may prefer. I'm willing
to hide and show elements quickily or replace an entire area. If I were doing
the same in another framework there is a 'cost' of time, pain and possibly bugs
but when working in Ember, I don't have these concerns. I think being allowed to
think like that from the beginning instead of saying, "That would be nice, but
we could do this and it will take 4 hours less", will allow me to write much
better user interfaces.

# Final Thoughts
There is still a timecost. At this point, I think that most apps I'm writing in
Ember will probably add a 30% overhead in time cost. For most apps, I'm ok with
that because I think we are adding a lot of value in that 30%, other apps may
not benefit from that 30% and in that case, I'll stick with 'Rails, straight
up'.

I think that in the future we will all develop our applications like a desktop
application and not consider whether or not it is a 'single page app' or a
'server render app'. We want to be able to interact with our users quickly and
effectively. Ember comes really close to allowing me to do that and I hope that
it continues down that same path. I can't believe I'm saying this but I think
that my default choice for new applications, at least personally, will be Ember
on the front and Rails on the back.
