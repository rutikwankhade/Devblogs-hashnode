## How I built my own productivity app


Before I started learning React, I had a goal. I wanted to build an MVP (*minimum viable product*) and experience the whole process of turning ideas into products. But I would always find a way to postpone it. But this time with  [#christmashackathon](https://hashnode.com/n/christmashackathon), I decided to use the magical powers of coding and push myself to build my own productivity app, the one I wish I had.





![tabwave-full.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1609504825859/4RvGUGCMh.png)

### 🤹‍♂️ Being productive
We often try to achieve more in less time. I used to think, the more I work, the more productive I become. But I was wrong. There is a big difference between *being busy* and *being productive*. I was always looking for ways to be more productive. I read multiple books, used different tools and techniques. But deep down I felt I need a  simple, minimal productivity tool and the idea of tabwave was born.

### 💡 The idea

The idea was quite simple. All I wanted was a bunch of productivity tools like a Pomodoro clock, a to-do list, sticky notes altogether. Nothing fancy and complicated. 

I wanted to have all these tools somewhere I can see all day. And I thought what's better than a browser's new tab. Also, I never knew how browser extensions were made so this was a learning opportunity for me to explore it closely.

### 🎨 The design process

I am no designer, but I feel I have a good taste in design. I looked for inspiration and started visualizing the structure of the design. I spent hours figuring out the layout. I kept improving it little by little as I progressed with its development. It was an iterative process. These are the steps I followed.

- Divide the whole app into different components.
- Create a minimal user interface for a single component.
- Work on the functionality of that component.
- Improve its UI to give it an aesthetic look.
- Repeat

#### Technologies used
- React
- Tailwindcss


### 🌊The challenges
The biggest challenge was turning a react app into a chrome extension. The problem comes when react creates multiple chunks of js files in the production build by default. And it violates the CSP (*Content Security Policy*) of the chrome extension. 

I was stuck. I thought I won't be able to fix this. I spent the next few days looking for a way to make it work. Eventually, I tried everything I could find. Creating a  `.env` file with `INLINE_RUNTIME_CHUNK=false` worked but it wasn't the best solution. Finally, I found another way by configuring the craco. I am glad **I didn't give up.**

### 📦 The final product
I am very happy with the final outcome. This is exactly what I wanted to build. Here are a few cool features of [Tabwave](https://tabwave.vercel.app).

- I wanted it to be a new tab chrome extension without losing the default feature of adding shortcuts in chrome. So you can add shortcuts to your favorite sites.


![shortcuts-tabwave.gif](https://cdn.hashnode.com/res/hashnode/image/upload/v1609506631381/jiNQug56p.gif)

- Can I call it a productivity app without a to-do list? No way. Get things done by managing your daily tasks.

![taskapp-tabwave.gif](https://cdn.hashnode.com/res/hashnode/image/upload/v1609506772706/5JigTpNiV.gif)



- A Pomodoro clock to increase your productivity. Trust me, I am following the Pomodoro technique and it's awesome. 
 - Focus for 25 min on your tasks 
 - Take 5 min break.
 - Repeat


![pomodoro-tabwave.gif](https://cdn.hashnode.com/res/hashnode/image/upload/v1609506866437/DJBuTbLsn.gif)

- Sticky notes to keep your brainstorming ideas and important stuff.

![notes.gif](https://cdn.hashnode.com/res/hashnode/image/upload/v1609507357034/jYj7wRIy_.gif)



- If you keep working all day, you might get tired or bored and might want something different to do. Well, I got you covered. Get a random activity idea in just one click. 

![activity-tabwave.gif](https://cdn.hashnode.com/res/hashnode/image/upload/v1609507028333/jyhJQTW7C.gif)


Unfortunately due to certain issues in my international transaction, I wasn't able to publish it in time on the chrome web store. So it will take some time to get it published. I will let you know when it's live. 

> 
*Subscribe [here](https://tabwave.vercel.app) to get notified.*

### 🤩 Good news
Wait, I have good news too. You can try it right now. I have deployed its web version at **[tabwave.now.sh](https://tabwave.now.sh)**. So go try it and let me know your feedback. Also, feel free to reach out with your ideas and suggestions.

### 🎉 Update
The Tabwave extension is now available on firefox. 
> 
You can download it from [here](https://addons.mozilla.org/en-US/firefox/addon/tabwave/).  


### Wrapping up
This has been a great experience for me. The excitement of building something I always wanted to build was awesome. I can't explain how joyful I felt after fixing that nasty bug or completing that small feature. It's so satisfying. Sometimes it got frustrating, but eventually, I somehow ended up solving the problem. 

It's not just about coding. It's about problem-solving. The more you do it, The better you become. I have always believed in learning by building and I will encourage you to do the same.

-------------------------------------------

I keep writing about the things I learned and applied. So you can connect with me on [Twitter](https://twitter.com/WankhadeRutik), [Github](https://github.com/rutikwankhade)  or [Linkedin](https://www.linkedin.com/in/rutik-wankhade). Also, subscribe to my newsletter and stay up-to-date with my latest blog posts.

⚡ Happy learning!

%%[newsletter]
