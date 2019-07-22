---
layout: post
title:  "We've got Titanic Problems"
date:   2019-07-21 16:13:30 -0500
categories: machine-learning historical-disasters Kaggle
---

I joined Kaggle the other day to try to get some exercise for my data science muscles. For those not in the know, Kaggle is a Google-created (or owned) site where teams solve optimization-type problems, presumably with some hot-new machine learning technology and possibly win some prize money given some criteria. I presume. Honestly I haven't dug too deep into how the site actually works. Just kind of dipping my toes in.

After creating a profile, I jumped on in to the starter problem. I'm not a data wizard just yet, so I knew I needed to start from the ground up. I decided that on this first challenge, I'd try some more rudimentary DS techniques (regression) as well as some more traditional machine learning (support vector machines) instead of trying to break out the heavy artillery (deep learning). Also, I wasn't sure the Neural Net stuff was entirely suited for the first problem anyways, given the small size of the training data (overfitting possibly?). Trying to even make judgements about what technique use or the problems I would face was a bit over my head.

## THE PROBLEM
Given data for a subset of passengers on the Titanic create an algorithm that can predict whether a passenger survived or perished.

## WHAT I SHOULD HAVE DONE
Start with familiarizing myself with the data set. Use basic statistics to get a grasp on what the values/ranges of each column was. Get some basic impressions of the data. Get the answers to some basic questions:
<ul>
	<li><i>Were men or women more likely to survive?</i></li>
	<li><i>How likely was any person to survive</i></li>
	<li><i>What is the mean/median/mode for all of the numeric data? What is the distribution for the categorical data?</i></li>
</ul>

I think getting a basic grasp on what your data looks like can really help you decide which direction you want to go with analysis.

Unfortunately, the next step (deciding which analysis technique to use) isn't so easy for me since my grasp of on how to use these techniques and what exactly they can tell you can be a bit tenuous at times.

## WHAT I ENDED UP DOING
I've wanted to figure out what support vector machines are and apply one to a problem ever since I saw a meme involving SVMs. Also the name seems pretty cool. So I set about making one myself, which I would then compare to one that I could probably find in one of python's nice open source DataSciencey libraries(pandas, numpy, scipy) to learn more about how to _actually_ make one.

So, my basic understanding of an SVM is that an SVM pretty much blazes a trail between different categories of data. Its a form of supervised learning, meaning that we already have the categorical information about our data and we are simply attempting to create a line that best separates our data into the categories that they are already in. Once we have that fancy line, we can do a quick calculation on incoming data that may not be explicitly labeled, figure out which side of the line it is using some basic linear algebra, and then label it appropriately.

So the SVM algorithm kind of creates a road that separates our categories of data and the support vectors are the vectors that appear on the edge of the road. The goal is to make the two lanes of the road as wide as possible. Basically, maximize the minimum distance of the lanes. A road where drivers on both sides have as equal amount of driving space as possible is the best road, in SVM land (and probably in the real world too).

So I split up making an SVM into a few tasks:
  - generate a linearly separable dataset to test with
  - 

A couple notes:
Its important that data be linearly seperable for SVMs. Linearly separable data is datasets are datasets that can be divided by a straight line/hyperplane.
