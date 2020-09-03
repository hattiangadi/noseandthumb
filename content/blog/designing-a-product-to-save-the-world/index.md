---
title: Designing a product to save the world
date: 2020-09-02T22:14:42.024Z
description: an approach to a better app for covid-19
tags:
  - productmanagement
  - economics
  - usercentereddesign
  - covid19
thumbnail: daily-new-cases-covid-19.jpeg
---
## How not to design a product to save the world
Google and Apple have released their contact notification apps. And... they look like they were designed by - at best - an epidemiologist. 

https://www.google.com/covid19/exposurenotifications/

First the name - Exposure Notifications. We'll just leave that right there. 

Here's the selling point: "The benefits of contact tracing". Oh wait, that's not something that the user gets to do with the app. For benefits, you have to get to the next paragraph: "How Exposure Notifications can help". That's right! As a user of this app, you are installing something that "can help" something something that has benefits to society. Click here! With this impressive call to action it's hard to see why people aren't lined up around the block to install this thing.

But wait - the standard template for product pages follows up the hero with sections for user benefits (always 3!) and user testimonial... surely there's more to the pitch? There is... a long description of the technology. Scintillating paragraphs entitled: "How this technology works" and "Exposure Notifications and your privacy"

One thing missing in this whole page? The app is *useful primarily if the people around you are using the app*. If some altruistic user decides to install the app, they might be a good candidate to tell people around them about it! But no, missed opportunity.

## What would be better? 

Instead of making an app (that by the way is an unattributed rip off of equally unsuccessful apps in Singapore and other places...) to fit the requirements of some technology, standard product management and design tells you to start with a user. Sometimes it's kind of hard to build a model of the user of such an app. Not here - we all are that user. 

## What do users want? Users (especially consumers) want to make good choices.
In the immortal words of Jamie Lee Curtis in Freaky Friday: "Make good choices". Good advice for Lindsey Lohan, and really for any person navigating our world. If you want be invaluable - help people make choices. Pick a better restaurant? Pick a better dish at a restaurant? Delete the article you've been working on? Choosing which link to click to read about llamas? Choosing where to put your money for retirement.

Note that this doesn't mean simply showing a user *all* choices - usually seeing all choices means occasionally picking bad choices. Banerjee and Duflo argue that one of the headwinds facing people in poverty is that they don't have enough help - defaults - for the choices they have to make. Nor does it mean gratuitously reducing choice... Users want to be better off, and this means both having choices and help making *good* choices.

## A slight detour into decision analysis 

A good decision is one that results in the highest expected return given for the preferences of the decision maker given the alternatives and uncertainties at the time. 

Note that a good decision is defined by the outcome - you can make poor decisions and (occasionally) have good results. People do win the lottery.

Note also that a good decision is about the preferences of the decision maker. If someone really gets a lot of entertainment from buying lottery tickets... it might worth a few bucks. 

As a decision maker using a tool, I know my preferences. And these are going to be different from yours! What I need help with is gauging the alternatives and uncertainties, and hopefully a nudge in the right direction... 

## Decisions I'd like to make in our Covid-19 reality
So what decisions do I want to make as a user living with the risk of Covid-19? Do I want an "Exposure Notification" about Covid19? Having been exposed to Covid-19 is an outcome. So you want me to install an app that promises to tell me about bad outcomes without helping me avoid them? From a decision analysis point of view, only a very altruistic person would do this. 

What I want is to be able to make reasonable risk assessments given the best data available. Here are some pretty standard choices that I have to make. 

1. Comparing relative risk \
Should I get takeout, which involves less risk, but is more frequent? Or should I go to the grocery store which involves additional risk but is less frequent? 
1. Risk vs. cost \
Should I get delivery, which is more expensive, or go to the restaurant for pick up which has more risk?
1. Risk vs. preferences \
Should I get takeout, which I like less, or should I eat outdoors at the restaurant, which I would enjoy more? Or indoors at a restaurant, which I would enjoy the most? 
1. Risk budgeting \
Can I minimize my risk in other areas (dining, etc) and save up risk for dinner indoors at a restaurant? 
1. Social\ethical choices
What would happen to society as a whole if everyone made my choices? (Taking a simplistic Kantian framework here, but it's probably the LCD of ethics). 

## But we don't have data for this

If you're still thinking about contact tracing (bad Product Designer! Stop that!) the data you're thinking of is about whether someone with the disease is actually at the restaurant right now, and if you're likely to catch the disease from them. You're throwing up a little about the loss of privacy. Or maybe you're thinking - the person with the disease at the restaurant who does have the disease doesn't even know they have it, so how can I have this data to help the user?

That's not the data we need. 

## First we build a model

Instead of working with data about confirmed cases of the disease, we work with the probability of disease. 

One interesting aspect of a disease is that the behavior and prevalence are two independent aspects of risk of catching the disease. It's really easy to confuse these two. For example, I heard the following argument - "I'm pretty sure I got it in February, because I was taking the train a lot and if it's that contagious, I'm pretty sure I would have gotten it." The problem with the argument is that the likelihood was low that there was a person with Covid19 in the train in the first place. Over time, as prevalence increased the likelihood that there'd be someone on the train with the disease would increase. (Not to pick on trains, there's some articles that trains and planes actually have pretty effective HVAC systems).

If there aren't actually many people who are sick, you can engage in risky behavior and the chances you'd get sick are slim. You'd have to be unlucky to interact with someone who is sick. However, if everyone is engaged in such risky behavior, then the chances are high that *someone* is going to interact with a sick person in a way that results in transmission. So in order to make good choices, I need to know both the relative riskiness of my behavior *and* the relative likelihood of other people having the disease. 

In terms of risk of transmission, we know that the following things matter:
1. density - how close are people to each other? 
2. duration - how much time do people tend to spend in contact with each other?
3. activity - singing and speaking seem to result in more transmissions
4. environment - small enclosed spaces vs large enclosed spaces vs. outdoor spaces, particular HVACs, etc.

Most of this data is in some manner already available in google maps. It would be relatively easy to pull it together into a simple "traffic" model of relative risk. 

But! I hear you protest - this doesn't take into account prevalence! And it's true - you don't get a good sense of absolute risk from a model that is purely based on "traffic". On the other hand, the transmission rate is related purely to behavior, and not to prevalence, so you can get an idea of the social impact of your behavior.

On the other hand, with a general sense of how many people are currently asymptomatic/infected in a region, it should be possible to create a model of absolute risk, and possibly even correlate it with actual observed infections. 

A simple model like this would answer almost all the questions listed above - it would *provide users with real value, without making any demands on privacy*. Once you provide real value, you could ask for something in return - possibly contact tracing. 

## SHIP IT!
Or not. We might be making the same error as the Exposure Notifications people. You don't just go about making a product, you need to start off by figuring out where your product thinking might be mistaken.

A pretty obvious pitfall of the way I've worked on this idea is that I've based it on my own experience enhanced with some theoretical models of decision making. I might be a user base of 1. An obvious way to mitigate this risk is to build some mockups and to see if other users would find it useful. 

Another approach is to see how people currently deal with similar problems. My neighborhood is currently pretty much surrounded by 3 significant fires, and we have had rather smoky air for the past few days. Given the detail with which my neighbors in a few days have grown to understand the intimate differences between purpleair and AQI and airnow and all the other air quality indicators, I'd say that there is some hunger for information that helps make better choices.

## Other issues

"It's just a model". We deal with models all the time - maps estimate time to destination, which I live by... but it's just a model. It might be important to be transparent about the uncertainty in the model, especially in the beginning. This combined with a commitment to marking the model to market might assuage concerns.

Gamification: The careful reader would have noticed that the model I've describe provides information to the user but doesn't actually help guide "good" choices. Gamification - perhaps enabling people to post on facebook how low risk they have been - to compare risk profiles with friends - could provide incentives to select the good of society. Comparing to local averages and work categories (obviously, if you work in a grocery store you're going to have a higher risk profile than the average person)...  
