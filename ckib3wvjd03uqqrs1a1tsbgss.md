## Reflection of Week 4 at FullStack Camp

It's been 4 weeks since I joined the FullStackCamp program, an initiative to help students grow and level up their skills. And I can see the difference in the clarity of my thoughts.

When you are starting your career, having a good mentor helps a lot. Someone who has gone through the same path you are about to start can make things easy for you. I have always tried to learn from experienced people by asking the right questions. You can learn a lot just by watching them, listening to their stories and experiences.

### 🤯 The Trap of failure 
I have failed multiple times in the past because I tried to learn everything all at once. The problem is that we want to achieve more in less time. I want to learn about UI/UX, JavaScript, react, node, data structures, algorithms, aptitude, and a lot of stuff. But we need to understand that we can't learn everything all at once. We have to respect the process. There are no shortcuts. 

So what I am doing right now? How I am taking this?. one-word priority. I know what are my priorities. *Everything is important but the question is what's more important.* The trick is to delay the less important stuff.

### 📅 This week I learned
This week I learned about react hooks and worked on a few small projects. Also, I started working on a side project I was thinking of for a long time. Will share about it once it is completed.

#### Absolute Imports
Do you know you can configure your `create-react-app` application to support importing modules using absolute paths?

Just create a jsconfig.json file like this in the root directory. [jsconfig.json reference](https://code.visualstudio.com/docs/languages/jsconfig)
 ```javascript
//jsconfig.json
{
  "compilerOptions": {
    "baseUrl": "src"
  },
  "include": ["src"]
}

```

And now you can get rid of `../.../ ` and import modules like
```javascript
// import Navbar from '../../components/Navbar';
import Navbar from 'components/Navbar';

```


### 🎉 Project hunt
Wait, do you mean product hunt? No. We in the FullStackCamp community have started working on an open-source community project similar to product hunt. Here rather than products we share projects. 😅 So project hunt. 


![projecthunt.gif](https://cdn.hashnode.com/res/hashnode/image/upload/v1607104601740/uNh9kGj--.gif)

I am working on mostly the frontend part with react and tailwindcss. And the good thing is the mentors share valuable feedback on each PR which is helping me learn from my mistakes and get better at writing quality code.

> Learn more about [FullStackCamp](https://www.notion.so/Frontbench-fdbe59767b1741d6857efa2ce3a06ebc)


%[https://twitter.com/WankhadeRutik/status/1334082668980527104]


____________________________________________
I keep writing about the things I learned and applied. So you can connect with me on [Twitter](https://twitter.com/WankhadeRutik), [Github](https://github.com/rutikwankhade)  or [Linkedin](https://www.linkedin.com/in/rutik-wankhade). Also, subscribe to my newsletter and stay up-to-date with my latest blog posts.

⚡ Happy learning!



