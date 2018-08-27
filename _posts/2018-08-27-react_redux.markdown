---
layout: post
title:      "React / Redux "
date:       2018-08-27 19:17:28 +0000
permalink:  react_redux
---

I've always been completely fascinated with how things work. I love things invisible to the naked human eye: human biology, the physical laws, neuroscience, etc. have always lured me from their intristic principles and in-depth research. For this reason, I was intruiged by React due to the instant rendering of the UI without a visible server rendering. It makes sense that constant calls to the database can be taxing on an application and the sophistication of React combined with Redux challenged many things I have learned about good coding practices up until this point. But, I was already sold by how it worked - like invisible browser magic. 

An effective technique I use for learning concepts and memorizing vocabulary and syntax is connecting or associating the new material with known information; abstracting it away into a metaphor my brain can make sense of. When learning React, my brain recieved many 404 HTTP responses: concept not found. Coming from the traditional MVC structure and seperation of concerns by technology, it was extremely strange to mix logic with markup and combine javascript with the familiarity of HTML into JSX. I had to begin to compare concepts I could connect React to in order to understand it from a 360-degree view and convince myself that all I'm not going to challenge this unfamiliar information, but continue to question it until I understand it. 

Basic quantum mechanics states that electrons, viewed as particles or physical mass, display wave-like (or energy-like) behavior. In other words, Einstein deemed correct in his theory that mass and energy are inseperable- they're the same physical entity and can be changed into each other. It's also known that molecules are made up of atoms, which are made up of energy, that combine to produce a unique frequency. This is how I think about React in terms of components, elements and their state. Components are the molecules and their props the atoms that make up the molecule. The atoms contain specific vibrational frequencey at any given time. The components of the DOM, (like the atom's mass), and the DOM's state, (energy), are inseperable and do, in fact, make sense to be within the same entity. 

In Pete Hunt's React explination, seperation of concerns has to do with reducing coupling and increasing cohesion. We want our modules to rely less on each other and each module to contain cohesive information, enforcing the single responsibility principle. It's not necessarily the logic and components that need to be seperated, but for information to remain grouped together until it needs to be seperated out if it exeeds beyond one responsibility. 

The way in which I seperated my components was seperated by navigational links. I maintained organization through seperating logic based on routes. Because I created an eCommerce site, I needed to incoporate a component for the products listing, a dashboard component, as well as home, login, register, and the blog page. For the products and dashboard component, I needed stateless components to handle the markup of the individual rendering of products as well as a users' cart that gets rendered inside of the dashboard component. 

React offers flexibility in the way in which you organize your app, but parameters for assuring you built it correctly is ease of compatability between the JSON API models and the UI, or virtual DOM. Once I was able to connect those two completely seperate levels of the application together, the way in which my components were supposed to be organized became almost obvious. 






