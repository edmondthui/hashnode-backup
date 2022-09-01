## I made an automated blog writer powered by OpenAI and it was terrible

Writing blog articles is one of the most tedious and difficult things I have done. I'm sure a lot of you can relate if you're on Hashnode. If you don't know I also run another blog called Coffee Informer where I write articles about coffee. I've tried hiring writers to create content for me, but the quality wasn't there. A lot of the time I would hire someone to write an article and have to provide them with an outline, topic, and related articles about the topic. Afterward, I would still have to proofread and edit the articles to may sure they were publishable. I thought "there has to be a better way that is fully automated". **That's when I had the idea to try automating the blog writing process with AI.**

With that, [filler.ai](https://www.filler.ai/) was born. This was my first attempt trying to create a SAAS product and I definitely learned a lot of things when building the project that I want to revisit in the future.

Currently, it is functional but there are many improvements that need to be made. **You can put in a topic and generate blog subheadings, full blog articles, article ideas, and video scripts. **It does this using OpenAI's GPT-3. 

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1661997670747/RECwyhYsP.png align="center")

**GPT-3 is a language generator that can produce human-like text with different parameters to fine-tune the results.** My goal was to have it generate human-readable blog articles targeting specific SEO keywords in articles that were 1000 - 2000 words long. 

I did this by first allowing the user to generate multiple headlines using a topic which GPT-3 would then generate an outline for targeting specific SEO keywords based on the inputted topic. Next GPT-3 would make an article based on the headline generated and then combine it all into a single article. This would be displayed to the user in an editable rich text editor so users can customize and change the article. 

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1661998165573/DVWjaZJ24.png align="center")

Once the users were happy with the article they could download it as a PDF to send it to an editor or copy and paste it onto their blog. There is a possibility I could add an export as a markdown button in the future. 

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1661998196934/m9Edqonjr.png align="center")

## Where it all went wrong

When I launched it and a few people used it.** I immediately got feedback about the quality of the articles.
** It also was not getting indexed by Google which was very concerning. These two issues were valuable learning experiences that I will share with you to take into your next project.

### Problems with Articles
**While the articles may look "readable" the content would be questionable.** A lot of the time the AI could generate an article about a topic and state random incorrect statements as facts. The AI had no knowledge of whether it was right or wrong, and a lot of time it looked very authoritative until you tried fact-checking the article. Then you would realize that the AI had no idea what it was talking about. 

![unnamed.gif](https://cdn.hashnode.com/res/hashnode/image/upload/v1662055597384/D-QXKsPbK.gif align="center")

**The AI would also repeat patterns and make very similar articles. **This is because it was trained on a set of examples and it would reuse patterns in the training data. As a result, different articles would end up looking very similar and may have repeated patterns or phrases.

**GPT-3 also does not have any memory of previous articles that it has created. **Suppose you want to generate two different articles about the same topic. The problem is that if you use the same topic with the same headings there is a very high possibility the article that is generated would look very similar to the previous article that was created. 

I think there is still a lot of potential for AI-generated articles, but there would need to be a human touch. The article cannot be fully created by AI and would at least need to be edited by someone. 

**In my opinion, the best use for GPT-3 for blogging at the moment would be creating short sentences about topics to insert into your articles so you don't have to write every single line. **This could help you improve the word count while still looking like a human wrote the article.

### Not using server-side rendering
**Another thing that I didn't account for was the lack of server-side rendering because I am using React. **If I could go back and restart the project I would probably use Next.js to have server-side rendering. 

Because React does not have server-side rendering Google does not rank it highly since it is responding with JavaScript instead of HTML. JavaScript is slower than HTML and as a result, a slower page will lower the ranking on Google Search. 

![sloth-slow.gif](https://cdn.hashnode.com/res/hashnode/image/upload/v1662055580644/_4sOKQ7B6.gif align="center")

**I think server-side rendering would help grow the website by allowing Google to index the pages better. **I could automatically generate articles that would be posted into the blog article route which would automatically create new blog posts with a press of a button. 

The code is very similar and there doesn't seem to be a very big difference between the two. You will still have components, but your pages will be located in a `pages` folder which would represent a resource and a page for your website. To convert from a simple React app to Next.js app all you would have to do is do a few simple steps:

1. Convert React router links to Next.js links
```
import { Link } from "react-router-dom";
```
to:
```
import Link from 'next/link'
```
2. Convert CSS to the Next.js styled-components 

3. Convert code to take advantage of Next.js, for example, this would be using `getStaticProps` or `getServerSideProps`

## Conclusion
**It was a learning process and it was my first attempt at a commercial product, and the journey definitely isn't over.** The next step would be converting the site over to Next.js and trying to improve the article generation. I'm not giving up and I hope you all follow me on my journey!

If you don't know my story I am a software engineer who used to be a commercial real estate broker in NYC. I quit my job to follow my passions and now I am 2 years into my career as a software engineer and loving it! If you want to know how I became a software engineer in only 3 months you can read that article [here](https://www.blog.edmondhui.com/software-engineer-in-3-months).

![Copy of Thank you for Reading (3).gif](https://cdn.hashnode.com/res/hashnode/image/upload/v1662054945411/UXAmiOIlI.gif align="center")
