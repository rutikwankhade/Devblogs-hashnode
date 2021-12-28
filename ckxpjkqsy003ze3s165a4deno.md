## How I built an app to reflect on your year 2021

Last year I wrote my [year-end reflection for 2020](https://blog.rutikwankhade.dev/2020-a-year-end-reflection). Reflecting on your year is to look back and note down the highs and lows, the things you liked, moments you experienced, and the lessons you learned. And I felt really good after reviewing my year. So this time I thought why not create something that will make this process break into small, simple steps. 

> 
And so I built [myyearinreview](https://myyearinreview.vercel.app/)


%[https://youtu.be/fTVEq0fJC-o]


____________________

# How it started

%[https://twitter.com/WankhadeRutik/status/1473657950338048001?s=20]

It all started last week when I finally decided to learn **Next.js**. It was on my list for a very long time now. 
So I picked some crash course on Youtube and I got hooked to it. Eventually, I jumped on reading the Next.js docs. I was about to build a demo app or something while learning. But then I thought If I am going to spend time on this, why not spend it on building something cool. *A win-win situation right!*.

But I had to build it in less than a week because this year is about to end and my idea was focused on year-end reflections.


____________________

## Next.js + Supabase

I was already blown away by all the built-in features Next.js provides like file-system based routing and server-side rendering.

The next step was to choose a database. I was hearing a lot about Supabase lately and wanted to give it a try. [**Supabase**](https://supabase.com/) is an open-source Firebase alternative. It provides all the backend services you need to build a product. And I am impressed with how quickly I was able to make the MVP. 


> 
Participating in hackathons has helped me get better at picking up new technologies quickly and building stuff.

- [Quickstart: Next.js + Supabase](https://supabase.com/docs/guides/with-nextjs)

____________________

So this is what I had in mind. The app will have a google login. Once the user logs in, a user profile will be created. The review will have various curated questions, after completing their review, the review page will be public for everyone. All the profiles will be shown on a separate reflections page. Also, users will have an option to choose if they want it to be featured on the reflections page or not. Pretty simple right.

Let's see this in brief but with the tech part now.

______________

## Authentication

To make things easy I enabled Google Auth for my project and just implemented login with google in the app. Check out [this guide](https://supabase.com/docs/guides/auth/auth-google) for a better understanding. 


After setting it up all I had to do was create these functions and connect them to UI.

```
async function signInWithGoogle() {
  const { user, session, error } = await supabase.auth.signIn({
    provider: 'google',
  })
}

async function signout() {
  const { error } = await supabase.auth.signOut()
}
``` 
______________

## Creating user profiles
Once the user is signed in, I had to create user profiles. But before that, I used the response data from google OAuth and created a username for the user. This will be used for the review page of that user later.

For creating user profiles, I could do it in two ways
1. Upsert the profiles table in the Supabase with data as soon as the user logs in.
2. Using `triggers` and `functions` in Supabase, We can trigger a function to create a profile on user creation in Supabase.

I chose the second one as it will create a user profile automatically once the user is created in Supabase.
_____________


## The review form
I curated a few good questions from multiple resources to reflect on the year. But If I kept all those questions on a single page, it would have looked like a tedious task to fill it and one might even just leave it. So to make things interesting I decided to make it a **multi-step** form. I broke those questions into small steps.

First I tried a few npm packages to do it, but couldn't style it accordingly, so I ended up building it on my own. 


![form demo.gif](https://cdn.hashnode.com/res/hashnode/image/upload/v1640633402406/NLAiTqU9p.gif)

✨ You see I even added a progress bar at the top so that every answer user writes, takes one step closer to completing their review.

## Where the magic happens
Once the user submits his review, with some 🪄 CSS magic, it will look something like this.


![review-demo.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1640633837930/BSKWJ-PuL.png)

This is just one section. There is a lot more. See it by yourself.

> 
Check out my review of 2021 here.
[https://myyearinreview.vercel.app/rutikwankhade](https://myyearinreview.vercel.app/rutikwankhade)

_________________

## Dynamic open graph images
At this point, if someone shares their review link somewhere on the internet, it won't look like it's their own thing. So to make the URL preview more personalized and clickable I leveraged the power of **Meta tags**. Next.js provides a built-in component `Head` for the meta tags.

Now using **Cloudinary API**, I made the open graph images for every review page dynamic and appended them in the Meta tags. 


![tweet.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1640635862274/BLNBq23LO.png)

Glad I bookmarked @[Braydon Coyer](@braydoncoyer)'s post about the dynamic open graph images. It was really helpful. *And yes, I do check my bookmarks. all of them*.

______________________

## Conclusion
And that's it for today. Try it yourself, create your review for the year 2021 and share it with your friends. Also,  **myyearinreview** is live on Producthunt. Check it out.

%[https://www.producthunt.com/posts/my-year-in-review]


%[https://twitter.com/WankhadeRutik/status/1475765928142852097?s=20]


_______________________

### References
- [Adding a user profile to our Supabase user](https://h.daily-dev-tips.com/adding-a-user-profile-to-our-supabase-user)
- [Supabase automatically create user profiles on sign up](https://h.daily-dev-tips.com/supabase-automatically-create-user-profiles-on-sign-up)
- [How to Dynamically Create Open Graph Images with Cloudinary and Next.js](https://blog.braydoncoyer.dev/how-to-dynamically-create-open-graph-images-with-cloudinary-and-nextjs)

________________________

%%[substack]






