## Building a bucket list ideas API with Hasura and GraphQL

Did you know you can create GraphQL APIs within minutes without writing a single line of code? Well, I didn't. Thanks to the **[Hasura X Hashnode hackathon](https://townhall.hashnode.com/hasura-hackathon)**. Now I know and so you will.

Hi there, In this blog post I will talk about why and how I built a public API for my open-sourced side project with GraphQL and Hasura. 

## 🗺️ A little backstory
When I was in college, I wanted to do lots of stuff outside my studies and college life. I wanted to explore more and try different things out. Things that I didn't even imagine I would ever be able to do. So I started researching and found out about the thing called **bucket list**.

> I loved the idea of the bucket list. It's like a number of experiences or achievements that a person hopes to accomplish during their lifetime.

So I created my own bucket list which had around 20 things. And I am so glad that I was able to cross a few items from my bucket list. Like Solving a Rubik's cube, meeting my favorite Indian author, or visiting Marine Drive, Mumbai.


![bucket-list.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1648733995627/PprV7uXC9A.png)

## 👀 So what's the deal?
Okay, we got it Rutik, enough with the story. How is it relative here? 

So a few months back I actually built a bucket list app for myself. I was trying out different tech stacks and thought of building bucket, an app to create and track my bucket lists again. But this time digitally. Now I do realize every other side project I built is somehow a solution for my own real problems.


![bucketlistapp.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1648736632242/ThzddNRs9.png)

It was nothing complex. Just a simple todo like app disguised as a bucket list app. It's built with React, TailwindCSS, and Firebase.

## 💡 The problem
 When Hashnode announced the Hasura hackathon, I started brainstorming ideas to build something. And I realized one of the pain points I had in my side project. While creating my own bucket list, I was running out of ideas. And I wished there was an API that gives a bucket list idea. Unfortunately, I couldn't find any good. 

So what would a developer like me do? I built one. 

## 🛠️ Hasura and GraphQL
So one weekend I started learning about Hasura and GraphQL. I have used GraphQL APIs before but never built one. And I was blown away by the fact that one can build APIs without much prior knowledge of the technology.

![Hasura.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1648738228698/d0QAJk11Z.png)

Hasura is an open-source project that connects your databases and instantly gives you a production-ready GraphQL API. It really does what it says. While the main idea of GraphQL is to POST a "query" to an HTTP endpoint, instead of hitting different HTTP endpoints for different resources.

I loved how It takes no time to get started. You don't have to go through hours of tutorials to build something with Hasura. To be honest, building APIs with Hasura seems like magic.


## 🤖 Building the API
- After signing up for the Hasura Cloud, created a new project for building API. We can either connect an existing database or create a new one. I created a new Postgres database by connecting with Heroku. 

![database.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1648739756972/v1k9OnUMd.png)

- Now the first step was to create a table by adding the required columns. For the bucket list API, I added id, idea, and category columns respectively.


![table-craetion.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1648740139405/ISUaUXzzq.png)

- After adding some data to the database manually, we are all set to use the API. Hasura cloud provides an integrated GraphQL playground called GraphiQL where we can run queries and test our API.

Here is a simple query that gives bucket list ideas with category creative

```
query MyQuery {
  ideas(where: {category: {_eq: "creative"}}) {
    id,
    idea
  }
}

```


![graphi.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1648740466987/-1uqSvYO2.png)

And that's it. Without writing a single line of code, I built the API in no time.

## 📍 Challenges
- Once I built the API, I was able to use it in the GraphiQL playground but it still wasn't accessible to the public. After reading some docs I figured out that using the `HASURA_GRAPHQL_UNAUTHORIZED_ROLE` env variables and user roles.

- Also to test and try out the API one could use the GraphQL playground. But to make things easier and reduce the step of copy-pasting the endpoint and all, I deployed the integrated playground using graphql-playground-react.


![api playground.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1648793705139/MKDI70qZ2.png)

Demo:  [https://bucketlist-api-playground.vercel.app/](https://bucketlist-api-playground.vercel.app/)

Code:  [https://github.com/rutikwankhade/bucketlist-api-playground](https://github.com/rutikwankhade/bucketlist-api-playground)



## 🚀 Using the API
Here comes the good part. Now I integrated this bucket list API in my side project that suggests different bucket list ideas based on different categories.

![bucket-explore-ideas.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1648741117760/ArPHrjjYw.png)


![list.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1648741141533/bC3UeLaDF.png)

You can try it out here [https://bucket.vercel.app/explore-ideas](https://bucket.vercel.app/explore-ideas)




## ✨ Wrapping up
It was fun implementing this simple application in my side project. I am definitely going to learn more about GraphQL and Hasura after this. This is my submission for the > [Hasura Hackathon](https://hashnode.com/n/hasurahackathon). See you next time.