## Introducing glimpse, a reader's corner to discover new books

Are you an avid reader? Do you wish to have an online catalog of the books you read and want to read? Do you feel that the readers deserve a better alternative to GoodReads? one with a good user experience? Well, Your wish is granted!

Introducing **Glimpse**, a reader's corner to discover new books.

## 🏃 Motivation
Reading is one of the few things that I enjoy outside work life. I read a lot. I mean when Emilia Clarke once quoted ''*My father always told me — Never trust anyone whose TV is bigger than their bookshelf*",
I agreed. 

![My bookshelf.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1646110277176/dTcpJ044o.png)

Over the years I have read books from the genres of fiction, nonfiction, self-help, and more other stuff that interests me. Those books have inspired and helped me become the person I am today.

##  💡Problem statement

> For almost a decade, *GoodReads* has been the dominant platform for readers to discover and rate books. But many of the internet’s most dedicated readers now wish they could share their enthusiasm for books elsewhere.

And I wanted to have that online catalog of books, I wanted to talk about the books I read. I once tried GoodReads and never opened it again because of its bad user experience. *I mean it's 2022!*

I know, there have been built alternatives. My goal was not to try to solve the engineering problem but the **user experience** problem. So I was more focused on the execution, rather than the idea. I wanted to build my own version of this side project.

And here it is.


![glimpseapp.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1646288650475/lyuFhlgiy.png)

Live : [https://glimpseapp.netlify.app/](https://glimpseapp.netlify.app/)

Code : [Frontend](https://github.com/rutikwankhade/glimpse) / [Backend](https://github.com/rutikwankhade/glimpse-backend)



## 🎨 The process

I spent a lot of time exploring how I can build this app before writing the first line of code. I planned the roadmap, tasks, and everything on the notion. This workflow helped me to track my progress.

![roadmap.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1646112991639/j9jz8EXDt.png)

I had to make lots of decisions around the user interface and the overall user experience. Sometimes had to get back to the whiteboard and rethink the whole user flow. But It was exciting and getting better on each iteration.

###  👾 The challenges

- The google books API has its limits. It gives 1000 API calls per day for an IP address. Searching every time user types could have ended up with the limit exceeding. So I used the **debouncing** technique to limit API requests.

- The book API doesn't always give the right response. sometimes, it does not have the properties requested. So I had to handle it on the client-side.
- To make the user profile more personalized, I used `Cloudinary` to store the images.
- As the app became bigger, it got hard to maintain the state. I have used redux before but it felt like writing too much boilerplate code. But the good thing I learned about `redux-toolkit` which is a much more clean and better way to manage the state than the old way of using redux.


###  🛠️ Technologies used
- Next.js - to build frontend
- Redux toolkit - for state management
- TailwindCSS - for styling the app
- Express and Node.js - for setting up the server
- MongoDB - database
- headless UI - for built-in components

###  🚀 Deployment on Netlify
I hosted almost every app I built on [**netlify**](https://www.netlify.com/) when I started coding. I was a beginner and netlify had a smooth, beginner-friendly experience of deploying sites. So I focused more on building the app and letting netlify take care of the deployment.


## 📦 The final product
oh wait, did I forget to mention why the name glimpse?

**glimpse means a quick idea or understanding of what something is like**. 
(or just a fancy word for review 😅)

Here are a few cool features of [Glimpse](https://glimpseapp.netlify.app).

- Instant search for books from the database of thousands of books. You can either search by book name or the author's name.


![searchfeature.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1646236397937/4TY1K0p0d.png)

- Find books based on different categories like fiction, nonfiction, business, technology, and more.


![categories.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1646236168516/a5oDGYVh2.png)

- Share glimpse of the books you read and liked in one click.  Talk about your thoughts, favorite quotes, and favorite things with glimpse.


![review.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1646234927901/w1uVRFt6Z.png)

- Follow other readers and get a glimpse feed based on your following. You might find the next book you want to read right here.
![111.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1646120749766/Y4Vyg0EFZ.png)

- Add books to your collection as currently reading, want to read, and read.


![save2.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1646235737658/DL7qRL3e-.png)
- Create your own online library and manage your books with ease.
![113.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1646121031052/nNEoVeTX4.png)

I have seen a lot of people having a collection of books they read in their portfolios. This could be one of the use cases for glimpse. Just create your profile and add it to your portfolio.

You can check out my profile [here](https://glimpseapp.netlify.app/profile/62185ec259dc133d1a0080e3).

### 👀 What's next

I am so happy I could finish this project in time. I was 🤌 this close to giving up on this. Glad that I didn't.  Glimpse has been my passion project for a long time. And this hackathon has pushed me to finally build and ship it. I know there is a lot of room for improvements and features. And I will keep working on it.

This is my submission for the [#netlifyhackathon](https://hashnode.com/n/netlifyhackathon)



-------------------------------------------



%%[substack]
