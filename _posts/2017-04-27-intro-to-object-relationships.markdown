---
layout: post
title: "Intro to Object Relationships"
author: Max
tags: OO_Ruby Update
subtitle: Update
category: Update
date: 2017-04-27T12:49:23-04:00
comments: true
---

So far, I've gone through over half of the Object-Oriented Ruby lesson track. However, I got stuck on Object Relationships and took a break from studying. I've recently gotten unstuck. So, that's what we will go over today: object relationships.  

<h2>Intro to Object Relationships</h2>

Everything in programming serves to model a real-world situation. These real-world situatiosn are translated into the domain model. The domain model is made up of objects such as Classes. 

For example, users in a social networking applicaiton end up being associated with each other based on friendships. 

Another example that is used on the Flatiron curriculum is in music. For example, one song belongs to an artist, while an artist may have many songs, a song may only have one artist for the purpose of this example atleast.

This leads us to the first relationship between objects that we will explore.  

<h2>"Belongs To" Relationship</h2>

One song belongs to one artist in this continued example. How do we represent this in code? 

``` Class Song
attr_accessor :title, :artist

def initialize(title)
	@title = title
	end
	end

	Class Artist
	attr_accessor :name, :genre

	def initialize(name, genre)
		@name = name
		@genre = genre
		end

		end```

Great! Now we can explore that relationship. 

``` michael_ray = Artist.new("Michael Ray", "Country")
	kiss_you_in_the_morning = Song.new("Kiss You In The Morning")
	kiss_you_in_the_morning.artist = michael_ray```

So, if we try to find out the artist genre or name, we can simply use the song name like this: 

``` kiss_you_in_the_morning.artist.genre #=> "Country"
kiss_you_in_the_morning.artist.name #=> "Michael Ray"```

To quote the Flatiron curriculum, "a song can only have on artist (atleast in our domain model), so we say that a song "belongs to" an artist." 

So, what if we want to represent the relationship that Artist have in the real-world to songs? What can we use in code to represent an artist having many different songs? 

<h2>"Has Many" Relationship</h2>

The answer is to use the inverse of the "belongs to" relationship, the "has many" relationship. 


<h2>"Has Many Object" Lab</h2>