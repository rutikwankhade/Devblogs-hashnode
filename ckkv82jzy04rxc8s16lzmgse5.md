## devspace : get top posts from the best developer platforms

After an awesome experience with Hashnode ***ChristmasHackathon***, Hashnode announced a new hackathon in partnership with Vercel. This time it was a 3 week-long hackathon. I wanted to build a full-stack app this time, but I didn't know a thing about how the backend works, so I started learning it.

More than 2 weeks passed and I didn't even start working on the project. Everything was new and a bit intimidating and I couldn't build it in time.


> 
But I still wanted to participate!
So I decided to pivot at the last moment and come up with something else. I was running out of both ideas and time. What should I build? a recipe app? a movie app? Nope. It had to be something that would be useful for me in my life.

### 💡 The idea
Did you hear of daily.dev ? It's a new tab extension that curates blogs and news for developers from different platforms. I have used it. But it was too much content for me. I realized I check only 4-5 developer platforms daily. And sometimes I don't stay for long, I just want to peek, see top posts and get back to my work. 
![joeyy.gif](https://cdn.hashnode.com/res/hashnode/image/upload/v1612695927859/H0zu8AUAF.gif)


Wait, what if I build something so that I won't need to search and switch tabs for these websites? Well, that sounds like a good idea.




### 🚀 Introducing devspace
Get top posts from the best developer platforms in one place.

%[https://youtu.be/83dKsOsx4as]


The app is deployed on Vercel and the code is open-sourced on Github.

 ### Demo
See live : https://devspace.vercel.app/  
Github :  https://github.com/rutikwankhade/devspace


### 📰 UI/UX
Even though it was a small app, creating a basic design prototype is always a plus. It helps to move in the right direction. I used
[excalidraw](https://excalidraw.com/). it's a great tool to create quick sketches.

![devspace.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1612699423754/F_u3l4i3t.png)

#### Layout
For the layout, I divided the screen into two parts. One for navigation and another for the main content. I thought of it as an open book.

#### Colors
I tried to be consistent with the colors and used colors that complement each other. Also, made it super clean and intuitive.

### Screenshots

![devspace.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1612791874769/w8gxy7bT7.png)


![devspace (1).png](https://cdn.hashnode.com/res/hashnode/image/upload/v1612791901745/ur77edDl2.png)

![devspace (2).png](https://cdn.hashnode.com/res/hashnode/image/upload/v1612791914469/cKQWDclDU.png)



### 👩‍💻 Technologies used
- React 
- TailwindCSS
- APIs - Hashnode, dev, HackerNews, Github, and Product Hunt 
- [svg-loaders-react](https://www.npmjs.com/package/svg-loaders-react) for displaying  a loader while the app fetches data 
- [react-reveal](https://www.react-reveal.com/)  for smooth animation on scroll

### 🌧 Challenges faced
-  Implementing the APIs was a bit frustrating. Reading the docs thoroughly helped a lot.
APIs of Hashnode, Dev, and Product Hunt was easy to use and implement. But Github doesn't have any endpoint for getting trending repositories in its official API. Luckily, I found an unofficial API. Thanks to the open-source developer community. 

- HackerNews API provides an endpoint to get only the ids of top posts. So I had to fetch individual posts with these ids.

- Few blog posts didn't have a cover image, so I used [Lorem Picsum's API](https://picsum.photos/) to set random images for default.

### ✨ Conclusion
I built this in a very short period of time and still made it look good and useful, at least for me. That's an achievement! So this is my submission for the **#VercelHashnode** Hackathon. 🙌 Cheers!

I keep writing about the things I learned and applied. So you can connect with me on [Twitter](https://twitter.com/WankhadeRutik), [Github](https://github.com/rutikwankhade)  or [Linkedin](https://www.linkedin.com/in/rutik-wankhade). Also, subscribe to my newsletter and stay up-to-date with my latest blog posts.

⚡ Happy learning!

%%[substack]










