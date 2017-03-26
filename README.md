![GA icon](https://raw.github.com/generalassembly/ga-ruby-on-rails-for-devs/master/images/ga.png)
# Smart Coding 101
Coding is good in theory but it's even better in practice, so let's get coding!

We are going to use an online code editor called Codepen to write our HTML and CSS. We've already made a template project for you, with all the best settings! [Click here to go to the template](http://codepen.io/ga-sg/pen/GWMwOE).

So that you can save your progress, hit the `FORK` button on the header bar. This will create your own copy of the template - you can also change the title if you like.

## Part 1: Describing Content with HTML (30 minutes)
Below is some placeholder text for our website - you can update this later with your own details.

```txt
Your Full Name

This is your personal statement. A short intro that summarises you, your major achievements and your life objectives. Give it some character and reflect your personality.

About Me

This is a more detail section where you can write a few paragraphs that describe you in much more detail. Depending on how you want to use this site, this could be about your craft (e.g. music, art, coding), your studies or your passions (e.g. travel, food, games).

Lorem ipsum is random latin text that designers often use to fill space until they get some real text... Here's some: Lorem ipsum dolor sit amet, consectetur adipisicing elit. Perferendis praesentium exercitationem asperiores consequatur vero necessitatibus, nulla assumenda magnam a quam quidem laudantium voluptatibus fugit reprehenderit in, ipsa consequuntur ea provident.


© 2017 Your Name. Find me on facebook
Made in 2hrs in General Assembly's Smart Coding 101

```

Copy and paste the above into your HTML tab in Codepen. Oh my, all of our formatting has disappeared, to get it back we need to mark-it-up with HTML.

### Header

Our site has three main components:
1. the header - where we display your name

Let's wrap each section in the coresponding html tag:  __header__ for the header, __main__ for the main, and footer for the footer.

```html
<header>
  Your Full Name
</header>


```

### Headings

Wrap Your name in a __h1 tag__ as it is our main page title.

```html
<header class="main-header">
  <h1>Your <span class="alternate-color">Full</span> Name</h1>
</header>
```

Next we wrap the 'About Me' titles in __h2 tags__. We also put them inside their own __header__ tags.

```html
<header class="section-header">
  <h2>About <span class="alternate-color">Me</span></h2>
</header>

... (the rest of the content is here)

```

### Sections

Now that we have our headings in place, let's wrap the three sub sections inside the main in __section tags__.

```html
<section class="intro">
This is your personal statement. A short intro that summarises you, your major achievements and your life objectives. Give it some character and reflect your personality.
</section>
<header>
  <h2>About Me</h2>
</header>
<section>
  This is a more detail section where you can write a few paragraphs that describe you in much more detail. Depending on how you want to use this site, this could be about your craft (e.g. music, art, coding), your studies or your passions (e.g. travel, food, games).

  ... (the rest of the content is here)
</section>  
```

### Paragraphs
Inside of our two longer sections, we have a number of paragraphs of text, so that the browser will format them correctly, let's wrap each one in __p tags__.

For example, the first section has four paragraphs...

```html
<header>
  <h2>About Me</h2>
</header>
<section>
  <p>
    This is a more detail section where you can write a few paragraphs that describe you in much more detail. Depending on how you want to use this site, this could be about your craft (e.g. music, art, coding), your studies or your passions (e.g. travel, food, games).
  </p>
  <p>
    Lorem ipsum is random latin text that ... (the rest of the content is here)
  </p>
</section>
```

#### `<a href="...">` for links
Let's turn our facebook link into an __a tag__ so that users can click on it to follow it to our profiles. Don't worry if you don't have a Github Profile, we will set one up later and you can come back and edit this link.

> **Top Tip.** If we set the 'target' attribute to '\_blank' it will open the link in a new tab/window rather than changing the current page.

```html
  <a href="www.facebook.com" target="_blank">Find me on Facebook</a>
```

#### Creator Info
Let's make the copyright notice more important using a __strong tag__. Let's also add a new line between the copyright notice and the creator info by using a __br tag__.

```html
© 2017 Your Name
<br>
```

This footer information is not as important as the main site content, so let's wrapping it in a __small tag__.

```html
<small>
  © 2017 Your Name. Find me on <a href="www.facebook.com">facebook</a>
  <br>
  Made in 2hrs in General Assembly's Smart Coding 101
</small>
```

### Review

Next we'll learn about CSS. If you've finished early, spend some time personalizing the content with your details,name, about, education etc.

#### Part 1 - final code

```html
<header class="main-header">
  <h1>Your <span class="alternate-color">Full</span> Name</h1>
</header>

  <section class="intro">
    This is your personal statement. A short intro that summarises you, your major achievements and your life objectives. Give it some character and reflect your personality.
  </section>
  <header class="section-header">
    <h2>About <span class="alternate-color">Me</span></h2>
  </header>
  <section>
    <p>
      This is a more detail section where you can write a few paragraphs that describe you in much more detail. Depending on how you want to use this site, this could be about your craft (e.g. music, art, coding), your studies or your passions (e.g. travel, food, games).
    </p>
    <p>
      Lorem ipsum is random latin text that designers often use to fill space until they get some real text... Here's some: Lorem ipsum dolor sit amet, consectetur adipisicing elit. Perferendis praesentium exercitationem asperiores consequatur vero necessitatibus, nulla assumenda magnam a quam quidem laudantium voluptatibus fugit reprehenderit in, ipsa consequuntur ea provident.
    </p>
  </section>
  <section>
    <small>
      © 2017 Your Name. Find me on <a href="www.facebook.com">facebook</a>
      <br>
      Made in 2hrs in General Assembly's Smart Coding 101
    </small>
  </section>
```

---

## Part 2: Adding Style To Content With CSS (30 minutes)
Now that we've learnt about CSS, let's add some style to our site. In your CSS file or CSS tab in Codepen let's add the following rules.

### Basic CSS

#### body
Let's make our font a little nicer, by giving it a `font-family` of `Futura`.
```
body {
  font-family: Futura
}
```

#### h1
Let's make our main heading a bit fancy, by giving it a black `background-color` and white text `color`. We can make the `font-size` bigger than normal and also increase the `line-height` and `letter-spacing` to give it a bit more of a wow factor. Finally, let's center out `text-align`. Also, let's set the `margin` to 0, so that our h1 fits more snugly.

```css
h1 {
  background-color: black;
  color: white;
  font-size: 30px;
  line-height: 50px;
  letter-spacing: 5px;
  text-align: center;
  margin: 0;
}
```

#### h2
For our section headers we're just going to increase the `font-size` and also `text-align` to the center. Finally, let's change all the text to uppercase with a `text-trasform`.

```css
h2 {
  font-size: 45px;
  text-align: center;
  text-transform: uppercase;
}
```

#### section
For our sections, we want to apply some `padding` so the text doesn't touch the edge of the screen. We can also set a `max-width` so that on large screens it doesn't stretch out too much. If we also set the `margin` to 'auto' then the correct amount of margin to keep it centered will also be applied. Finally, whilst the gradient is cool, it makes our text less readable, so let's set the `background-color` to white.

```css
section {
  padding: 10px;
  max-width: 960px;
  margin: auto;
  background-color: white;
}
```

---

### Advanced CSS
To take our design even further, we'll need to go back and add some class attributes to our HTML. We can then select these classes in our CSS and add more specific styling. You'll need to alternate between the HTMl and CSS tabs for the steps below.

#### Main Header
Let's add a `main-header` class to the first header on the page, so we know it is the main one.

We can also do something fancy by wrapping every odd word in our name in a __span tag__ tag with the class `alternate-color`.

```html
<header class="main-header">
  <h1>Your <span class="alternate-color">Full</span> Name</h1>
</header>
```

In our CSS, let's add styles for those two new classes. First we can tell the browser that anything with the `alternate-color` class should have it's text `color` be that of a dark golden rod - super cool!

```css
.alternate-color {
  color: darkgoldenrod;
}
```

Next, let's get our main-header to be a fixed `height` of 230px. We can then give it a `background-image` and adjust the `background-size` so that it is fully covers the image (i.e. shrink it down if needed). As our image is a square it will repeat, so let's set the `background-position` to center, so it stays nicely in the middle.

```css
.main-header {
  height: 230px;
  background-image: url("https://raw.githubusercontent.com/wdi-sg/smart-coding-101/master/images/avatar.png");
  background-size: cover;
  background-position: center;
}
```

#### Intro Section
The first section of our site is an intro, so let's give it a class attribute called `intro`, so that we can select it and style it in CSS.

```html
<section class="intro">
  This is your personal statement. A short intro that summarises you, your major achievements and your life objectives. Give it some character and reflect your personality.
</section>
```

Let's add some CSS to increase the `font-size`, `text-align` to the center and also add a bit of `padding`.

```css
.intro {
  font-size: 1.4em;
  text-align: center;
  padding: 20px;
}
```

#### Section Headers
We can now update our section headers to make them more WOW. Let's add a class called `section-header` to each, so that we can select them. Let's also add __span tags__ with the `alternate-color` class to the odd words in our section headings

```html
<header class="section-header">
  <h2>About <span class="alternate-color">Me</span></h2>
</header>
```

Time for some magic! Let's add some CSS to make the header a fixed `height` with a `background-image` just like the main header but this time we'll set its `background-size` to cover the full space and its `background-attachment` to be fixed in place, so the image doesn't move when the page scrolls - this creates a really awesome parallax effect. Finally, we can get our heading text to vertically center by setting the `display` property to flex and the `justify-content` and `align-items` to center all children - these work with the display type set to flex.

```css
.section-header {
  height: 200px;
  border-top: 3px solid grey;
  background-image: url("https://raw.githubusercontent.com/wdi-sg/smart-coding-101/master/images/bgs/3.png");
  background-size: cover;
  background-attachment: fixed;
  display: flex;
  justify-content: center;
  align-items: center;
}
```

### Review

HTML & CSS done!

Next we'll learn how to deploy it online. If you've finished early, spend some time customising the designing. This [HTML Color List](https://www.w3schools.com/colors/colors_names.asp) and [Font Awesome Icons List](http://fontawesome.io/icons/) might be useful. Also, we've included 10 different backgrounds, named `1.png` through to `10.png`, try changing the `3.png` part of the background-url in your section-header e.g. `background-image: url("https://raw.githubusercontent.com/wdi-sg/smart-coding-101/master/images/bgs/7.png");` - you can also use your own images that you have online, you just need to copy the link to them.

#### Part 2 - final code

**html**

```html
<header class="main-header">
  <h1>Your <span class="alternate-color">Full</span> Name</h1>
</header>

  <section class="intro">
    This is your personal statement. A short intro that summarises you, your major achievements and your life objectives. Give it some character and reflect your personality.
  </section>
  <header class="section-header">
    <h2>About <span class="alternate-color">Me</span></h2>
  </header>
  <section>
    <p>
      This is a more detail section where you can write a few paragraphs that describe you in much more detail. Depending on how you want to use this site, this could be about your craft (e.g. music, art, coding), your studies or your passions (e.g. travel, food, games).
    </p>
    <p>
      Lorem ipsum is random latin text that designers often use to fill space until they get some real text... Here's some: Lorem ipsum dolor sit amet, consectetur adipisicing elit. Perferendis praesentium exercitationem asperiores consequatur vero necessitatibus, nulla assumenda magnam a quam quidem laudantium voluptatibus fugit reprehenderit in, ipsa consequuntur ea provident.
    </p>
  </section>
  <section>
    <small>
      © 2017 Your Name. Find me on <a href="www.facebook.com">facebook</a>
      <br>
      Made in 2hrs in General Assembly's Smart Coding 101
    </small>
  </section>
```

**css**

```css
body {
  font-family: Futura
}

h1 {
  background-color: black;
  color: white;
  font-size: 30px;
  line-height: 50px;
  letter-spacing: 5px;
  text-align: center;
  margin: 0;
}

h2 {
  font-size: 45px;
  text-align: center;
  text-transform: uppercase;
}

section {
  padding: 10px;
  max-width: 960px;
  margin: auto;
  background-color: white;
}

.alternate-color {
  color: darkgoldenrod;
}

.main-header {
  height: 230px;
  background-image: url("http://ahwmrc.com/images/rabbit-2/rabbit-216.jpg");
  background-size: cover;
  background-position: center;
}

.intro {
  font-size: 1.4em;
  text-align: center;
  padding: 20px;
}

.section-header {
  height: 200px;
  border-top: 3px solid grey;
  background-image: url("https://raw.githubusercontent.com/wdi-sg/smart-coding-101/master/images/bgs/3.png");
  background-size: cover;
  background-attachment: fixed;
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;
  -webkit-box-pack: center;
      -ms-flex-pack: center;
          justify-content: center;
  -webkit-box-align: center;
      -ms-flex-align: center;
          align-items: center;
}

.alternate-color:hover {
  color: brown;
}

```

---

## Part 3 - Get It Online (15 minutes)

Ok, so we've built our website and now we're going to deploy it online. As this is a 'smart' coding class, we're going to do that in a very clever and easy way. The first step is to setup an account on Github.com.

### Setting Up Your Github Account
Sign in to github using the account we've set up for this workshop:
```
GitHub username: smartgen-ga-user
password: Smartgen1
```

### Exporting Your Website From Codepen
Now we're ready to upload your website but we need actual html and css files files. Fortunately, we can export them directly from Codepen, just hit the export button in the bottom right corner and chose the Export .zip option. **Make sure you hit the save button first, otherwise your changes won't be exported**

![Export From Codepen](./readme-images/export-codepen.png)

We now, have the html and css files we need in order to upload.

### Create A New Github Repository
We're going to deploy our website to Github, and the first thing we need to do is create a new Repository (you can think of repository as another word for project). Hit the new Repository button in the top right corner of the header bar.

![New Repo on Github](./readme-images/new-repo.png)

You want to:
* name your repository `your-github-username.github.io`, where your-github-username is actual github username that you just created
* add a simple description
* tick the box to create a README file
* you can leave the rest of the options as default

![New Repo on Github](./readme-images/new-repo-part2.png)

Once you've have done that you want hit the `upload` button and then drag and drop the `index.html` file and the `css` folder on to the upload window. Once they have uploaded, you can hit the commit button.

![Upload on Github](./readme-images/upload.png)

![Upload Files to Github](./readme-images/upload-part2.png)

### Review

That's it! It usually takes about 10 minutes (if you're lucky it might be instant) but your website should now be online at `https://your-github-username.github.io/` where your-github-username is actual github username ;-)

---

## The End

Well done! View your results with pride, smile and play around with some styling ideas of your own :-)

We hope you enjoyed the session.

### Example Solution
The finished [HTML & CSS Files can be downloaded here](https://github.com/wdi-sg/smart-coding-101/archive/master.zip) and [an online example can be seen here](https://wdi-sg.github.io/smart-coding-101).

---

## Licensing
1. All content is licensed under a CC-BY-NC-SA 4.0 license.
2. All software code is licensed under GNU GPLv3. For commercial use or alternative licensing, please contact legal@ga.co.
