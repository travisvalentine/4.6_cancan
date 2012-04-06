!SLIDE full-page
# CanCan #

created with [showoff](http://github.com/schacon/showoff)

!SLIDE full-page
# What Is CanCan? #

!SLIDE full-page
# This? #

<iframe width="640" height="480" src="http://www.youtube.com/embed/HXcieUVLz-I&" frameborder="0" allowfullscreen></iframe>

!SLIDE full-page
# Not quite #

!SLIDE full-page
# CanCan is #

> "An Authorization library that restricts
> what resources a given user is allowed
> to access"

!SLIDE full-page bullets incremental
# Why would I need that? #

* Let's take a random example
* Say you have a project
* Let's call it...

!SLIDE full-page bullets incremental
# Store Engine #

* ...or any app with features targeting specific audiences

!SLIDE full-page bullets incremental
# We need two things #

* to give certain users access
* to keep the rest out

!SLIDE full-page bullets incremental
# Enter CanCan #

* requires `current_user` method
* `gem install cancan`
* `bundle`
* `rails g cancan:ability`

!SLIDE full-page bullets incremental
# What just happened? #

* created an Ability.rb class
* define all abilities for user types
* syntax is easy

!SLIDE full-page bullets incremental
# Example #

* `if user.role? :admin`<br />
*  `can :create, Product`<br />
* `else`<br />
*  `...`<br />
* `end`

!SLIDE full-page bullets incremental
# In the view #

* `<% if can? :create, Product %>`<br />
* `<%= link_to "Add Product", new_product_path %>`<br />
* `<% end %>`

!SLIDE full-page
# But you want more control? #

!SLIDE full-page bullets incremental
# Control the Controller actions #

* can be granular with `unauthorized! if cannot?`
* or broad with `load_and_authorize_resource`
* sets a `before_filter`
* checks controller actions and adds restrictions

!SLIDE full-page 
# Who Created It? #

!SLIDE full-page bullets incremental
# Heard of Railscasts? #

* [Ryan Bates](http://twitter.com/rbates) is the creator of Railscasts
* ...and
* also the author of [cancan](https://github.com/ryanb/cancan)

!SLIDE full-page bullets incremental
# Why the need? #

* We don't want people stumbling upon things they shouldn't

!SLIDE full-page bullets incremental
# What about Declarative Authorization #

* Another popular authorization gem
* actively maintained
* seems more robust
* syntax not as easy
* docs don't seem as thorough

!SLIDE full-page
# You be the judge #

!SLIDE full-page
# Thanks #

Goal for next week: images