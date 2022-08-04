## I built an app to crowdsource  internet's best side project ideas


If you are following me for a while you know I love building side projects. And every time I decided to build one, I didn't know how it will turn out in the end.  But one thing is for sure, it all started with a **half-baked idea**.

half baked idea? what's that?
Well, this little conversation with Joe (*my imaginary friend who is always hungry*) might add some light to it.



![halfbaked.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1659295683677/sk5-jd0aM.png align="center")

Like when I thought, what if I could replace my browser's new tab with a productivity app, I built [Tabwave](https://tabwave.app). What if I could reduce the hefty process of designing cover images and make it quick and easy, [Coverview](https://coverview.vercel.app) was born. 

You see the pattern right?


## 💡 The idea of half baked idea

- When makers build products they usually launch them on a product hunt. But what if we could validate the idea before you spend hours building it?

- Most of us come up with half-baked ideas but don't have the tools, resources, or time to build them. What if we could just share the ideas with the world and let others make it?

- After participating in multiple hackathons, at some point, we are running out of ideas. What if there was a place we could get some ideas from?

And so I decided to build an app where we can share our half-baked ideas and vote for them. it's like bringing the internet's best half-baked ideas into one place.


![hero.gif](https://cdn.hashnode.com/res/hashnode/image/upload/v1659320079922/rrNSQbt9K.gif align="center")


## 🍪 The baking/ making process

Once I decided on the idea it was time to bake it. Oh sorry, make it. While building the app, I made various decisions on the approach or the tools I used which I will talk about as we move forward.

### 👶 Explain like I am 5
While writing about the copy on the landing page, I wanted to try something different. So I started writing it like users are talking to me and I am explaining it to them. This gave me an idea of making up Joe (yup, the same one we talked with earlier). So I made it like I am explaining to Joe what's this app about like he is 5.

### 🎨 The user interface
I used **Nextjs** for building and **TailwindCSS** along with **headlessUI** for styling the app.


![hero.webp](https://cdn.hashnode.com/res/hashnode/image/upload/v1659326200371/9ViBmBN3r.webp align="left")

### ✅ Authentication
I tried three different approaches for this one. Let me explain.
#### 1. No account needed
The app was focusing on crowdsourcing the data, so I thought not to make users log in or signup. Anyone can come up and shoot their ideas. 

But there was a problem with this approach. If you give internet options to mess up with your site anonymously, there is a high chance they will. So it might end up with a lot of spam ideas. And I really wanted it to be a genuine source of ideas. Also, making a user profile was on my roadmap so I skipped this.

#### 2.  Account needed only to interact
The second approach was to let everyone see the content and requires login only if they want to post or vote for any idea. 

I implemented this approach and added analytics on site to see how it performs. After 6-8 hours of the launch (on Reddit and Producthunt) and 1k+ page views, I realized only 1-2% of the visiting users are interacting with the app. Why bother signing up when you can see the posts right? And that was the problem. In the initial phase, the app needed ideas to be submitted or voted on. The main goal was to crowdsource ideas and not just the views. So I switched to the next approach.

#### 3. Need to sign up
Users will need to signup to see all the posts or vote for them. I compared the data and I saw a good (10-15%) improvement in the interaction. After enough ideas get added on site I can switch back to the previous approach. I was using Nextjs so **next-auth** was an obvious choice for me. I only kept google login to make it quick.

### 🪄 Planetscale and Prisma
**PlanetScale** being the *most scalable MySQL platform* was my obvious database choice. Tagging along with **Prisma** made it a perfect combination.

![+sds.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1659327147405/_GPCOCmsv.png align="left")

Getting started with PlanetScale was as easy as it could be. The default free developer plan has 5 GB storage,1 billion row reads/mo and 10 million row writes/mo which is pretty great for your hobby projects. Also, I liked the idea of branching & merging like Git at the database level.

It introduced me to Prisma (ORM) (object-relational mapper) which I used to create schema and send queries to the database.


## 👀 How does it work?

#### Sharing ideas
Users can share their half-baked ideas. I know it's hard to come up with ideas, so added a few tips on the side.

![brandbird (15).png](https://cdn.hashnode.com/res/hashnode/image/upload/v1659349735781/G5hP02YnP.png align="left")

#### Upvoting ideas
I considered two ways to validate the half-baked ideas. If someone builds a product out of this half-baked idea, would you use it? or would you pay for it to use? This way makers can get validated ideas and won't end up building something no one would use.

![brandbird (13).png](https://cdn.hashnode.com/res/hashnode/image/upload/v1659329687799/LpLWNXAqe.png align="center")



#### Filter and sort ideas
You can sort ideas based on the ✨ latest, 🙋 I would use it and 💸 take my money. Also, You can filter by different categories like social, productivity, health, etc.

![brandbird (12).png](https://cdn.hashnode.com/res/hashnode/image/upload/v1659329533062/_UaV0SY6a.png align="center")

#### User Profile
You can see all the half-baked ideas shared by a user on their profile. 


![brandbird (11).png](https://cdn.hashnode.com/res/hashnode/image/upload/v1659328924039/K9f_uqNjq.png align="center")

User profiles are public and can be accessed with a link.  So I added a popup when unauthenticated users try to react to the posts.

![brandbird (14).png](https://cdn.hashnode.com/res/hashnode/image/upload/v1659333051837/bHU2cES6c.png align="center")

## 🔗 Links
- Demo : [https://halfbakedideas.vercel.app](https://halfbakedideas.vercel.app)
- Github: [https://github.com/rutikwankhade/halfbakedideas](https://github.com/rutikwankhade/halfbakedideas)

*update day 2*

## 📈 Stats after 48 hours
The simple idea of sharing half-baked ideas got a great response from the internet. I shared it on Reddit, Twitter and launched it on Product hunt. Here's what happened in the next 48 hours.


![halfbakedideas-vercel-app-‒-Dashboard-‒-Pirsch-Analytics (5).png](https://cdn.hashnode.com/res/hashnode/image/upload/v1659428074717/qCI6IY2BH.png align="left")


![ph launch.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1659428939744/UTosFipa0.png align="left")
**3.8k unique visitors** , **8k page views** , **800+ sign-ups** and so many creative ideas!


*update day 4*

Now, this is getting wild. 200+ half baked ideas and I am amazed by how creative people can get while coming up with ideas.


![halfbakedideas-vercel-app-‒-Dashboard-‒-Pirsch-Analytics (8).png](https://cdn.hashnode.com/res/hashnode/image/upload/v1659591229447/IR93JDRYP.png align="left")



## 🔮 What's next?
This was fun, not just the building part but writing about the whole process. It was just a half-baked idea. There is a lot more I can do to make it better. And I am already getting feature requests from the users. for ex. discussions. I want to continue working on it.

What are you waiting for? Go visit [halfbakedideas.vercel.app](https://halfbakedideas.vercel.app) and check out cool half-baked ideas shared by the internet. And if you have one, don't forget to share it with the world.

Cheers!
