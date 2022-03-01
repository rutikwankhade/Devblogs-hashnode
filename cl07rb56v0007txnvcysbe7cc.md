## Introducing glimpse, a reader's corner to discover new books.

Are you an avid reader? Do you wish to have an online catalog of the books you read and want to read? Do you feel that the readers deserve a better alternative to GoodReads? one with a good user experience? Well, Your wish is granted!

Introducing Glimpse, a reader's corner to discover new books.

## Motivation
Reading is one of the few things that I really enjoy outside work life. I read a lot. I mean when Emilia Clarke once quoted ''My father always told me — Never trust anyone whose TV is bigger than their bookshelf",
I agreed. 

![My bookshelf.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1646110277176/dTcpJ044o.png)


And I wanted to have that online catalog of books, I wanted to talk about the books I read. I once tried GoodReads and never opened it again because of its bad user experience. I mean it's 2022!


> For almost a decade, GoodReads has been the dominant platform for readers to discover and rate books. But many of the internet’s most dedicated readers now wish they could share their enthusiasm for books elsewhere.

I know, there have been built alternatives. My goal was not to try to solve the engineering problem but the user experience problem. So I was more focused on the execution, rather than the idea. I wanted to build my version of this side project.

And here it is.

Live : [https://glimpseapp.netlify.app/](https://glimpseapp.netlify.app/)

Code : [Frontend](https://github.com/rutikwankhade/glimpse) / [Backend](https://github.com/rutikwankhade/glimpse-backend)



## 🎨 The process

I spent a lot of time exploring how I can build this app before writing the first line of code. I planned the roadmap, tasks, and everything on the notion. This workflow really helped me to track my progress.

![roadmap.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1646112991639/j9jz8EXDt.png)

I had to make lots of decisions around the user interface and the overall user experience. Sometimes had to get back to the whiteboard and rethink the whole user flow. But It was exciting and getting better on each iteration.

### 🛠️ The challenges

- The google books API has its limits. It gives 1000 API calls per day for an IP address. Searching every time user types could have ended up with the limit exceeding. So I used debouncing technique to limit API requests.

- The book API doesn't always give the right response. sometimes, it does not have the properties requested. So I had to handle it on the client-side.
- To make the user profile more personalized, I used Cloudinary to store the images.


### Technologies used
- Next.js - to build frontend
- TailwindCSS - for styling the app
- Express and Node.js - for setting up server
- MongoDB - database
- headles UI - for built-in components

### Deployment on Netlify
I hosted almost every app I built on netlify when I started coding. I was a beginner and netlify had a really smooth, beginner-friendly experience of deploying sites. So I focused on building the app and letting netlify take care of it.





## 📦 The final product
oh wait, did I forget to mention why the name glimpse?
glimpse means a quick idea or understanding of what something is like. 

Here are a few cool features of [Glimpse](https://glimpseapp.netlify.app).

- Quick search for books by name or author

- Find books based on categories

- Share glimpse of the books you read and liked. Share your thoughts and favorite quotes with glimpse.

- Create your library by adding books to the collection as currently reading, want to read and read.

- Create your own glimpse profile that you can share with your friends.

- Follow other readers and get suggestions from them.




### Wrapping up
I am so happy I could finish this project in time. I was 🤌 this close to giving up on this. Glad that I didn't.  Glimpse has been my passion project for a long time. And this hackathon has pushed me to finally build and ship it. I know there is a lot of room for improvements and features. And I will keep working on it.

This is my submission for the [#netlifyhackathon](https://hashnode.com/n/netlifyhackathon)



-------------------------------------------



%%[substack]
