## I built an app to crowdsource  internet's best side project ideas


If you are following me for a while you know I love building side projects. And every time I decided to build one, I didn't know how it will turn out in the end.  But one thing is for sure, it all started with a half-baked idea.

half baked idea? what's that?
Well, this little conversation with Joe (my imaginary friend who is always hungry) might add some light to it.



![halfbaked.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1659295683677/sk5-jd0aM.png align="center")

Like when I thought, what if I could replace my browser's new tab with a productivity app, I built [Tabwave](https://tabwave.app). What if I could reduce the hefty process of designing cover images and make it quick and easy, [Coverview](https://coverview.vercel.app) was born. 

You see the pattern right?


## 💡 The idea of half baked idea

- When makers build products they usually launch them on a product hunt. But what if we could validate the idea before you spend hours building it?

- Most of us come up with half-baked ideas but don't have the tools or time or know the tech to build them. What if we could just share the ideas with the world and let others make it?

- After participating in multiple hackathons, at some point, we are running out of ideas. What if there was a place we could get some ideas from?

And so I decided to build an app where we can share our half-baked ideas and vote for them. it's like bringing the internet's best half-baked ideas into one place.


![hero.gif](https://cdn.hashnode.com/res/hashnode/image/upload/v1659320079922/rrNSQbt9K.gif align="center")


## 🍪 The baking/ making process

Once I decided on the idea it was time to bake it. While building the app, I made various decisions on the approach or the tools I used which I will talk about as we move forward.

### 👶 Explain like I am 5
While writing about the copy on the landing page, I wanted to try something different. So I started writing it like users are talking to me and I am explaining it to them. This gave me an idea of making up Joe (yup, the same one we talked with earlier). So I made it like I am explaining to Joe what's this app about like he is 5.

### 🎨 The user interface
I used Nextjs for building and TailwindCSS along with headlessUI for styling the app.


// mobile mockup screenshots

![hero.webp](https://cdn.hashnode.com/res/hashnode/image/upload/v1659326200371/9ViBmBN3r.webp align="left")

### ✅ Authentication
I tried three different approaches for this one. 
#### 1. No account needed
The app was focusing on crowdsourcing the data, so I thought not to make users log in or signup. Anyone can come up and shoot their ideas. 

But there was a problem with this approach. If you give internet options to mess up with your site anonymously, there is a high chance they will. So it might end up with a lot of spam ideas. And I really wanted it to be a genuine source of ideas. Also, making a user profile was on my roadmap so I skipped this.

#### 2.  Account needed only to interact
The second approach was to let everyone see the content and requires login only if they want to post or vote for any idea. 

I implemented this approach and added analytics on site to see how it performs. After 6-8 hours of the launch (on Reddit and Producthunt) and 1k+ page views, I realized only 1-2% of the visiting users are interacting with the app. Why bother signing up when you can see the posts right? And that was the problem. In the initial phase, the app needed ideas to be submitted or voted on. The main goal was to crowdsource ideas and not just the views. So I switched to the next approach.

#### 3. Need to sign up
Now users will need to signup to see all the posts or vote for them. I compared the data and I saw a good (10-15%) improvement in the interaction. I was using Nextjs so next-auth was an obvious choice for me. I only kept google login to make it quick.

### 🪄 Planetscale and Prisma
PlanetScale being the most scalable MySQL platform was my obvious database choice. Tagging along with Prisma made it a perfect combination.

![+sds.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1659327147405/_GPCOCmsv.png align="left")

Getting started with PlanetScale was as easy as it could be. The default free developer plan has 5 GB storage,1 billion row reads/mo
and 10 million row writes/mo which is pretty great for your hobby projects. Also, I liked the idea of branching & merging like Git at the database level.

It introduced me to Prisma (ORM) (object-relational mapper) which I used to create schema and send queries to the database.


## 👀 How does it work?

#### Upvoting ideas
I considered two ways to validate the half-baked ideas. If someone builds a product out of this half-baked idea, would you use it? or would you pay for it to use? This way makers can get validated ideas and won't end up building something no one would use.

![brandbird (13).png](https://cdn.hashnode.com/res/hashnode/image/upload/v1659329687799/LpLWNXAqe.png align="center")



#### Filter and sort ideas
You can sort ideas based on the ✨ latest, 🙋 I would use it and 💸 take my money. Also, You can filter by different categories like social, productivity, health, etc.

![brandbird (12).png](https://cdn.hashnode.com/res/hashnode/image/upload/v1659329533062/_UaV0SY6a.png align="center")

#### User Profile
You can see all the half-baked ideas shared by a user on their profile. 


![brandbird (11).png](https://cdn.hashnode.com/res/hashnode/image/upload/v1659328924039/K9f_uqNjq.png align="left")

shows login popup when user reacts copywriting takes less than so they make the decision

## 🔗 Links
- Demo : [https://halfbakedideas.vercel.app](https://halfbakedideas.vercal.app)
- Github: [https://github.com/rutikwankhade/halfbakedideas](https://github.com/rutikwankhade/halfbakedideas)

## 🔮 What's next?
This was fun, not just the building part but writing about the whole process. It was just a half-baked idea. There is a lot more I can do to make it better. for ex. discussions. And I will continue to work on it.

Also, half baked ideas is [live on Product hunt](https://www.producthunt.com/posts/half-baked-ideas) since yesterday.

What are you waiting for? Go visit [halfbakedideas.vercel.app](https://halfbakedideas.vercel.app) and check out cool half-baked ideas shared by the internet. And if you have one, don't forget to share it with the world.

Cheers!
