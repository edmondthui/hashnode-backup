## How to create portfolio website with custom domain using Github pages

In the current job market,** I believe that every new developer should have a portfolio showcasing projects they have built.** As someone who doesn't have experience, a portfolio is how you can stand out amongst the thousands of new graduates from college and bootcamps. I built a portfolio just like this when I graduated from bootcamp and got a job in 3 months. You can read [my story here](https://www.blog.edmondhui.com/software-engineer-in-3-months).

Even if the recruiter or hiring manager doesn't read everything on your website, a quick scan is enough to set you apart from everyone else who doesn't have a portfolio site. 

If you are a beginner developer there is no reason why you shouldn't have your own site. It's free, simple, and quick to set up with Github pages. You can even add a custom domain for around $15 a year with no monthly hosting fees for some extra pizazz.

**Here is a step-by-step guide on how to make your own portfolio website.** This tutorial will be for complete beginners or people who do not know how to code who want to create their own portfolio websites. This will be extremely easy to follow, and I would encourage experienced developers to skip steps you already know how to do. You will not need to have any coding skills to follow most of this tutorial. 

## Setting up your Github repo for your page

First, you have to set up your Github repository which is where we will push all of our code. 

My next article is a complete guide for git best practices and using git professionally. You can read my [Git and Github tutorial here](https://www.blog.edmondhui.com/how-to-use-git).

1. Click the "+" button on the top right of the page on Github. There should be a dropdown that shows up, then press "New Repository".
![Screen Shot 2022-08-09 at 8.56.23 PM.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1660093109889/lo6pTfjfZ.png align="center")
2. Use the "Select an owner" dropdown to choose which account will own the repository.
![Screen Shot 2022-08-09 at 9.09.22 PM.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1660093797348/ZYGh2LImA.png align="center")
3. Name your repository using this naming scheme`<user>.github.io`. So since my user name is edmondthui I will name my repository `edmondthui.github.io`.
![Screen Shot 2022-08-09 at 9.13.40 PM.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1660094029966/dCPS0kuwl.png align="center")
4. Make your repository visibility public, check whether you want a read me, and then create your repository.
![Screen Shot 2022-08-09 at 9.18.11 PM.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1660094331092/-lXJP8J0g.png align="center")

## Setting up Git locally

Now that we're past the boring part we can open up our IDE. I like using VS Code but you can use any editor you like. 

1. First we have to set up our Github repository locally. In a new directory type `git init` into the terminal to start tracking your current directory with git. 
![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1660165506041/jT6lpu0ef.png align="center")
2. Copy the quick setup link from Github and run `git remote add origin <your link here>`
![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1660165662820/3yzuSd7Fp.png align="center")
![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1660165719030/2e3VS-5xe.png align="center")
3. Optional - you can rename your branch to "main" by running `git branch -M main`. GitHub uses "main" as the name of your primary branch. Git still defaults your branch to be called "master".

## Choosing a template for your portfolio website

We will be using a template to make our website. **I believe that most developers should use a template when building their personal portfolios. **

The amount of time it takes to make a beautiful website is not worth it, especially since this guide is targeting developers who are trying to break into the industry to get their first tech job. There are more important things to do, such as portfolio projects and improving your interviewing skills. 

What we are looking for is a template that has the following things:

- An easy-to-customize setup
- Eye-catching responsive design
- A contact form

You can browse different free themes [here](https://themewagon.com/theme-tag/portfolio-template/?swoof=1&pa_price=free&paged=1&really_curr_tax=398-product_tag) and choose what you think would work the best for yourself. I will be using this theme called [Profile](https://themewagon.com/themes/best-quality-free-portfolio-resume-bootstrap-template-download-profile/) for this example.

1. Download your theme and unzip the files into the folder where you created your git repository.
![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1660167063951/5dHcq1FwT.png align="center")
2. You should see a file called `index.html`. This will be the file we will be editing and customizing with all your information. Click on it and you should be able to edit the contents of that file.
![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1660167129982/AYSisS8I9.png align="center")
3. You can view your progress by opening the `index.html` file in chrome by double-clicking it. You will want to inspect your changes ever so often to make sure you aren't breaking anything.
4. We will only be editing the information between opening and closing HTML tags. **The vast majority of tags must be opened `<tag>` and closed `</tag>` with the element information such as a title or text resting between the tags.** You can change the information between the tags to whatever text you want to display. Replace all the information on the index page template with your information. Make sure you do not accidentally delete any tags or change the structure of the file.
![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1660167350654/E18hkivAq.png align="center")
![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1660167371389/OAHWTR2Zw.png align="center")
5. Update any links with your personal links. You can do this by replacing wherever it has `href="<your link here>"`
![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1660169129691/59iLyioXg.png align="center")
6. If you need to delete any elements find them in your editor and delete both the tags containing all the information you want to delete.
![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1660169201211/EBFgaEFp9.png align="center")
![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1660169221433/Fzf9AZfD7.png align="center")
7. Replace any images in your image folder with new files making sure you keep the names of the files the same.
![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1660169324412/aUcczaZpA.png align="center")

Once you are happy with how your page looks you're ready for the next step.

## Pushing your code to Github

The next step is getting all your code to Github so we can use Github pages to create a static site so people can see your website. 

1. Run `git status`, this should show all the changes you have made. Confirm there are changes before continuing.
![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1660169883092/HHFVJ7eeW.png align="center")
2. Run `git add .` to add all the changes from your directory to be staged for the next commit. You can rerun `git status` to make sure your files have been added.
![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1660169998336/9ASagrBF0.png align="center")
3. Now that you have staged your changes you have to commit them by running `git commit -m "<any message here>"`
![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1660170494450/jsn3nTybG.png align="center")
4. Push your code to Github by running `git push origin main` if you changed your branch name to main or `git push origin master` if you haven't changed your branch name.
![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1660170336173/zJtEh2pPv.png align="center")
5. You should now see the code in your Github repository!

## Creating a Github page for your repository

The last step is to make a Github page. Your repository needs to be public if you want to have a Github page with a free account.

1. Go to settings for your repository on Github on the top right of the page. 
![Screen Shot 2022-08-10 at 7.12.45 PM.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1660173239251/9sVaDTW11.png align="center")
2. Click pages on the left side of the settings page.
![Screen Shot 2022-08-10 at 7.14.31 PM.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1660173293725/YjlocBizw.png align="center")
3. Select the `main` or `master` branch as the branch for your page, then click save.
![Screen Shot 2022-08-10 at 7.16.01 PM.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1660173429611/X1xrb-CEp.png align="center")
4. Click the checkbox to enforce https.
![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1660173508892/Z0NAsYnrH.png align="center")
5. Thats it! Your site should be live. [Here](http://edmondhui.com/demo.github.io/) is a link to the demo site that I made in this tutorial.

## Optional - Adding a custom domain and sitemap for SEO

**Custom domains are a great way to build a brand around yourself.** It is another factor that can help set you apart from other developers. I do the exact same thing with my blog at https://www.blog.edmondhui.com/.

### Using a custom domain with a Github page

1. On the same page in the repository settings there is a field called custom domain. If you own a domain you can input it there. You can buy a domain on [Godaddy](https://godaddy.com/) or [Google Domains](https://domains.google/) for around $15. Then, click save. 
![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1660173986426/VqffGaWOh.png align="center")
2. Next go to your PROFILE settings and click pages.
![Screen Shot 2022-08-10 at 7.30.12 PM.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1660174244311/XYwmITESG.png align="center")
![Screen Shot 2022-08-10 at 7.31.00 PM.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1660174288377/bOa5q5Y38.png align="center")
3. Click "add domain" and then input your domain.
4. Now go to manage DNS wherever you purchased your domain and add the A records you got from Github. You can copy and paste them here:
```
185.199.108.153
185.199.109.153
185.199.110.153
185.199.111.153
```
![Screen Shot 2022-08-11 at 9.23.09 AM.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1660224206625/_eSwTA0GR.png align="center")

### Using Github actions to automatically create a sitemap

If you want to try to rank your portfolio site you will need to submit a sitemap to Google to index your website. To do this you will need to use a Github action.

1. In your repository click "Actions"
![Screen Shot 2022-08-10 at 10.07.11 PM.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1660183669059/3P84AYmtE.png align="center")
2. Click "New workflow" to create an automated action
![Screen Shot 2022-08-10 at 10.08.17 PM.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1660183759221/UwptHXOw-.png align="center")
3. Then click set up a workflow yourself
![Screen Shot 2022-08-10 at 10.09.33 PM.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1660183828769/-ImO9l1zf.png align="center")
4. In the workflow editor paste this code. Change the branch name in the code to match whatever is your primary branch. Currently, it is set to `[main]`. You will also have to change the base-url-path to point to your url.
```
name: Generate xml sitemap
on:
  push:
    branches: [main]
jobs:
  sitemap_job:
    runs-on: ubuntu-latest
    name: Generate a sitemap

    steps:
      - name: Checkout the repo
        uses: actions/checkout@v2
        with:
          fetch-depth: 0

      - name: Generate the sitemap
        id: sitemap
        uses: cicirello/generate-sitemap@v1.8.4
        with:
          base-url-path: https://edmondhui.com/
          include-pdf: false

      - name: Output stats
        run: |
          echo "sitemap-path = ${{ steps.sitemap.outputs.sitemap-path }}"
          echo "url-count = ${{ steps.sitemap.outputs.url-count }}"
          echo "excluded-count = ${{ steps.sitemap.outputs.excluded-count }}"

      - name: Create Pull Request
        uses: peter-evans/create-pull-request@v3.12.0
        with:
          title: "Automated sitemap update"
          body: >
            Automated changes. Sitemap updated by 
            the [generate-sitemap](https://github.com/cicirello/generate-sitemap) 
            GitHub action.
          commit-message: "Automated sitemap update."
          author: Edmond Hui <edmond.t.hui@gmail.com>
          committer: Edmond Hui <edmond.t.hui@gmail.com>
          branch: create-pull-request/sitemap
          delete-branch: true
```
5. Click "Start commit" and "Create new file" to create this Github action. This will run every time you push to either "main" or "master".
![Screen Shot 2022-08-10 at 10.13.50 PM.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1660184223660/mwBhOkL74.png align="center")
6. Now you can go to [Google Search Console](https://search.google.com/search-console/about) and add your sitemap to your property. 
![Screen Shot 2022-08-10 at 10.18.29 PM.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1660184324919/J3fa9-ym6.png align="center")

## Conclusion

Congratulations on making it to the end of the article! Hopefully, you will have your very own portfolio site that you can proudly share.

**Even if you are not on the job hunt, having a personal portfolio website is extremely useful.** Portfolios can help you professionally or help build your brand. For entrepreneurs, this can unlock opportunities and help you find business partners or investors.

I hope you enjoyed this beginner's guide to creating a personal portfolio. If you are a beginner developer I recommend reading my article about [whether you should join a bootcamp or self study](https://www.blog.edmondhui.com/self-study-or-coding-bootcamp).

![Thank you for Reading.gif](https://cdn.hashnode.com/res/hashnode/image/upload/v1660186835073/VX5YZoijB.gif align="center")
