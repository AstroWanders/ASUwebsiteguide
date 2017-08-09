
# [](#header-1)Why should you make a website? 

**Networking!** When collaborators, peers, etc. Google your name after meeting you at a conference or reading your paper, your website should be one of the first results.

# [](#header-1)What goes on a website? 

While your website can be a digital CV, you can also add links to publications, abstracts, etc. Many grad students also include sections for "Recent News" (e.g., I got a grant for X, Y, Z!) or "Hobbies" (e.g., photography).

# [](#header-1)What is an ASU public website?

All grad students, postdocs, and faculty members have a dedicated URL: _http://www.public.asu.edu/~(your ASU ID)/_.  I will show you how to set this up below. 

When you change institutions, it will be trivial to transfer your website. 

# [](#header-1)How do you upload material onto your ASU public website?

## [](#header-2)1. Ensure that your Personal Webpage Hosting subscription is active.

If you tried to access your URL previously and received an error, the following should ameliorate that.

a. Go to _www.asu.edu/selfsub/_

b. If Personal Webpage Hosting is listed as “Active”, proceed to the next step, #2.

![](https://astrowanders.github.io/ASUwebsiteguide/images/SelfSub.png)

c. If Personal Webpage Hosting is _not_ active, then simply click it at the bottom of the webpage and subscribe to it. 
More information is available [here](https://copp-community.asu.edu/content/how-self-subscribe-asurite-domain-computer-service).

## [](#header-2)2. Check out your website: _http://www.public.asu.edu/~(your ASU ID)/_

Since you have yet to upload material onto your website, but you have an active webpage subscription, the following will appear 

![](https://astrowanders.github.io/ASUwebsiteguide/images/PublicASUweb.png)

We will make note of these instructions for later.

## [](#header-2)3. Make your website!

This is the **fun** part! Your website can be anything you want, and now you are working with a blank canvas. 

### [](#header-3)a. Pick your favorite template and download it.

While you can start from scratch with HTML5, in the interest of time - Don’t you have research to do and papers to publish? - we will proceed with templates here. 

*   Free HTML5 website templates are available here: [Styleshout](http://www.styleshout.com/free-templates/)
*   Free CSS3 website templates are available here: [CSS3](http://www.css3templates.co.uk/) 

There are, of course, many other free templates available on the interwebs. **Be sure to _credit_ these sources - You do not want to get into sticky copyright infringement situations.**

You may want to look at websites of other SESE grad students for inspiration:
*   [Wanda Feng](http://www.public.asu.edu/~wfeng20/)
*   [Amanda Truit](http://www.public.asu.edu/~atruitt/)
*   [Alex Spacek](http://www.public.asu.edu/~aspacek/)
*   [Kim Ward-Duong](http://www.public.asu.edu/~kwardduo/)

For this guide, we will download the **[Kreo template](http://www.styleshout.com/free-templates/kreo/)** from Styleshout. This template has been popular amongst grad students of all disciplines and institutions. 

### [](#header-3)b. Take a look around the folder that you just downloaded.

Unzip the Kreo folder in your local Downloads folder. You should find the following folders/files, each serving a specific purpose. 

| Folder/File    | Purpose                                                 |
|:---------------|:--------------------------------------------------------|
| css            | CSS stands for “Cascading Style Sheets”. The css files in this folder define style definitions in this template. You will edit main.css to define the directory your background image is in later. |
| favicon.png    | This is the icon that will appear on your browser, like the blue one on this one. ![](https://astrowanders.github.io/ASUwebsiteguide/images/tab.png) |
| fonts          | As you can gather from the name, this folder contains fonts that will appear on your website. **_It is not necessary to alter this folder._** |
| images         | This is where you will place images that will appear on your website. |
| inc            | There is only one file in this folder: _sendEmail.php_ This is intended for the “Contact” section of your website. |
| **index.html** | **This is the main document - what you want viewers to see. We will be editing this file in the next step. As noted in the instructions for your ASU public website, you will want to upload your homepage as index.html, so do not change the filename.** |
| js             | JS stands for “JavaScript”. The js files in this folder serve functions such as opening links in new tabs, etc. **_It is not necessary to alter this folder._** |
| readme.txt     | This file describes the template, but does _not_ provide instructions. |

You can open index.html in your favorite browser to take a look at the template. 

### [](#header-3)c. Edit the template.

There are many ways to edit the Kreo template. I like Adobe Dreamweaver because you can also use it to connect to a remote server, which will need to do in the next step to publish your website. Dreamweaver comes with an Adobe Creative Cloud subscription, or you can download a [free trial here](https://creative.adobe.com/products/download/dreamweaver?promoid=T32PLZSW&mv=other). This is what index.html should look like when you open it in Dreamweaver, set to “split” screen:

![](https://astrowanders.github.io/ASUwebsiteguide/images/Dreamweaver.png)

The top is the “live” view - it’s the same as what you saw when you opened index.html in your browser. The bottom is the corresponding “code”. When you make changes in the code, it will be reflected in the live view. 

If you do not want to use Dreamweaver, you can use [Google Developer Tools](https://developers.google.com/web/tools/chrome-devtools/), which is free. 

At this point, you can make your website look like what you want. **_Make sure that you save as you edit._** If there are errors, the first thing you should check is whether you’ve correctly ended something (e.g. 
```html
<section>
```
to start, 
```html
</section>
```
to end).

Let’s make some edits together: 

- Under _basic page needs_, change the page title to your name. This is the text that appears on the tab of your browser. 
- As noted in part b, _favicon.png_ is the image that appears on the tab of your browser. You should comment this part out because your ASU public site should have an ASU icon by default. 
```html
<!--    <link rel="shortcut icon" href="favicon.png" > -->
```
  - NOTE: To comment lines, place 
```html
<!-- 
```
before and 
```html
--> 
```
after.
- The header is the very top of the webpage. 
*   The Kreo template has a yellow icon - Let’s comment that out. 
*   Under the part that says _class="nav"_, you can define the sections of your website. I suggest the following: _Home_; _About Me_; _Research_; _Contact_.
*   Under the part that says _class="header-social"_, you can add links and icons for your favorite social media sites. Let’s comment out everything here and add LinkedIn
- The homepage background is set in _main.css_. First, place an **original image (i.e. You either _photographed or designed it_. Like the HTML template, you do not want to get into sticky copyright infringement situations here.)** in your _images_ folder. Then, open _main.css_ in Dreamweaver and change the image name on line 970 
```html
background: #0F1215 url(../images/hero-bg.jpg) no-repeat center;
```
- On the homepage, Kreo has slides for a title. 
  - Let’s comment the last two slides, so the title doesn’t change. 
  - Change the title to your name. 
  - You may want to set the subtitle to a short description of what you study. 
Alternatively, you can change the classes from _flexslider_ and _slides_ to _row banner_ and _row banner_ and _banner-text_.
- At the bottom of the homepage, there’s a red box with _More about us_. Change this to _More about me_.
- Then, the sections are defined. Make sure that the section IDs to correspond to the hrefs that you defined for the header. You may want to know the following to build your sections:
  - To add an image: 
```html
<img  src="images/image.jpg" alt="" />
```
  - To link a website as a hyperlink: 
```html
<a href="website url">text</a>
```
  - To link a file as a hyperlink: 
```html
<a href="images/file.pdf">poster</a>
```
  - To link a file as a button: 
```html
<a href="cv.pdf" class="button"><i class="fa fa-download"></i>View CV</a>
```

### [](#header-3)d. Upload your website from your computer.

If you are using Dreamweaver, you can make an SFTP connection by going to Site → Manage Sites. Straightforward directions are on [Adobe’s website](https://helpx.adobe.com/dreamweaver/using/connect-remote-server.html).

To check that your files have been uploaded, you can go to your files from My ASU
![](https://astrowanders.github.io/ASUwebsiteguide/images/MyFiles.png)

Alternatively, you can upload all of your files directly to your files on My ASU. 

When you go to your files, you will see under a _www_ folder. This is where your website lives. 
![](https://astrowanders.github.io/ASUwebsiteguide/images/MyFilesWWW.png)

All files in your local website folder should be in your _www_ folder. If you encounter any path errors, it is because your directory paths in your local folder do are not the same as the _www_ folder.
![](https://astrowanders.github.io/ASUwebsiteguide/images/MyFilesWWW2.png)

# [](#header-1) About the author

I wrote this guide because I wanted to build my professional website and could not find a pre-existing guide to do so. A previous iteration of this guide may be found [here](https://docs.google.com/document/d/1_loQMuYhhYjqprTG8lOle1nWj5Y6o4mQmV2R_h8bWxY/edit?usp=sharing).   

As an Astrophysics PhD student, I have my own research to do, so I reserve the right to not respond to HTML questions should you write to me. 

If you experience server errors, you may contact [ASU Tech Support](https://asuonline.asu.edu/student-resources/technical-support).

**Updated 9 August 2017**
