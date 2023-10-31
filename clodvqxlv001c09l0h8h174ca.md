---
title: "Building a blog with the powers of headless hashnode"
datePublished: Tue Oct 31 2023 05:20:07 GMT+0000 (Coordinated Universal Time)
cuid: clodvqxlv001c09l0h8h174ca
slug: building-a-blog-with-the-powers-of-headless-hashnode
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1698729561439/0a06e327-4623-4373-ab22-107f1db9a5e8.avif
tags: headlesshashnode, headlesschallenge

---

I have been using Hashnode since its early days. Over the years it has become my go-to platform for writing blogs because of its exceptional features. But this time around Hashnode took blogging to the next level by introducing [**Headless Hashnode**](https://hashnode.com/headless). When it was announced that something new was cooking for Hashnode, I knew it would be something along the lines of customization and taking full control of the blogs. And it did not disappoint.

So I used this opportunity to build the blog, the way I wanted.

### Step 1: Setting up the blog

The good thing was that Hashnode already provided a blog [starter kit](https://github.com/hashnode/starter-kit) which is integrated with hashnode APIs. That made the job easy as I didn't have to build it from scratch.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1698725930180/caec91f8-aca8-4834-8b8f-b10363169bee.png align="center")

So I forked the blog starter kit repository, set environment variables and deployed it on vercel. I chose the enterprise theme.

I was building this blog for Tabwave and I already had a website deployed on the domain [tabwave.app](https://tabwave.app). Thanks to Hashnode now I can deploy my blog on my subpath like [tabwave.app/blog](https://tabwave.app/blog)

This is how you can configure it on your subpath if your main project is deployed on vercel.

```typescript
async rewrites() {
    return [
      {
        source: "/blog",
        destination: "https://starter-kit-rose-seven.vercel.app/blog", -> Replace https://starter-kit-rose-seven.vercel.app with your own Vercel deployment URL from step 1
      },
      {
        source: "/blog/:path*",
        destination: "https://starter-kit-rose-seven.vercel.app/blog/:path*", -> Replace https://starter-kit-rose-seven.vercel.app with your own Vercel deployment URL from step 1
      },
    ];
  },
```

You can read more about setting up your blog on the [started kit repo](https://github.com/hashnode/starter-kit)

Once it was deployed, I enabled the headless mode in my blog dashboard on Hashnode. And that's it. It started treating my blog as a headless blog and sent readers directly to the origin which is [tabwave.app/blog](https://tabwave.app/blog)

![Did You See How Fast That Was Shane Luis GIF - Did You See How Fast That Was Shane Luis Rerez GIFs](https://media.tenor.com/LjZCITZUTGsAAAAd/did-you-see-how-fast-that-was-shane-luis.gif align="left")

### Step 1: Personalize the blog

At this stage, the blog is live and running. It was mind-blowing to see it didn't even took me more than half an hour to set it up. Now that the blog is ready, it is time to customize it.

I started with the headers and footers first and then slowly built the blog cards. At first, I just made normal cards ui for blogs but then I got an idea. This was a blog for a productivity app, so why not make it look like that?

And I ended up making my blog cards look like simple handwritten sticky notes.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1698728027061/ad704f26-c744-4412-83c7-8015e0c9d4b3.png align="center")

I customized everything else to match it with the theme of my website.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1698728334129/1a2fa518-baf5-4920-98da-051a98a5a966.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1698728806622/ca6852d0-ff60-4061-8015-d45ba239f418.png align="center")

Having tags and their respective pages is very useful as I can put all the changelog on a single page.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1698728671072/2415a52c-4459-43d2-abab-3450b012dcfe.png align="center")

And that's it. You can see my blog here at [tabwave.app/blog](https://tabwave.app/blog)

Even I was surprised by how easy and fast it is to build a blog with headless hashnode. I believe it's gonna change the blogging space as it opens the countelss opportunities with it.

Now I can just use the powerful hashnode editors to write a blog any time and publish it. I hope this pushes me to write more often. Nevertheless, I had fun exploring headless hashnode and you should also give it a try.