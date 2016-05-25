<!--

- [ ] Embed videos
- [ ] QUIZ?
- [ ] Lato / Lekton?
- [ ] make sure we're using Chrome.
- [ ] Animated gif

-->


- [ ] **Intro**. Why the Web is great and why being Web-literate is fundamental these days.
- [ ] **Sketch** out your portfolio. Checklist: images, texts (name, blurb, project description, links, contact details)


# Build your own Web portfolio

The aims of today are:

* Organise your work to **tell the story** of your projects
* Start building an **online one-page portfolio** for your work
* [Learn **HTML & CSS**](#html-css-crash-course)
* **Publish and host** your portfolio online

Bringing storytelling and coding together to make something that is useful to you, today.

<!-- 
* as a creative, you'll be telling the story of your work and your process for the rest of your working life 
* is there a jump in the story of your process (remember story lines?)
-->


# HTML & CSS crash course

We're going to learn how to:

* Write HTML to **structure** your content 
	* Create several types of **text** (paragraphs, headings, quotes)
	* Create **links** to other Web pages (eg: your blog)
	* Add **images** (eg: of your work)
	* **Embed** other media (eg: YouTube videos, tweets etc.)
	 
* Write CSS to **style** your content
	* Design your page's **typography**
	* Set your page's **colours**
	* Get images to fill up the whole browser's window, without loosing their original aspect ratio
	* Position elements in the horizontal and vertical centre of the page
	* Create a *curtain reveal* effect

The **demo** is at [j.mp/html-css-portfolio-demo](http://j.mp/html-css-portfolio-demo). Click `Remix` to reveal all its **source code**.

## Step by step

> Go to [thimble.mozilla.org](https://thimble.mozilla.org/) and sign up (it's free). 

> Then log in and click on `Start a project from scratch`.

### 1. Content first

It's good practice to build the **HTML** first, and then make it _stylish_ with CSS. This approach is called *content first*.

#### HTML skeleton

Thimble created an HTML skeleton for us, containing the basic **building blocks**: `html`, `head` and `body` tags.

Every HTML document, at the bare bones, needs to have this structure

```html
<!doctype html>
<html>
	<head>
		...
	</head>
	<body>
		...
	</body>
</html>	
```

#### Head

> In the `head` you can change the `title`.  
	
Later, you'll add links to external resources like *stylesheets* and *meta* information.

What you put in the `head` is not visible in the page.

#### Body

We're dividing our page into sections.

> Create a few empty `section` tags inside the `body`.
	
> ```html
...
	<body>
		<section></section>
		<section></section>
		<section></section>
		<section></section>
		<section></section>
	</body>
</html>	
``` 

#### Headings

> In the **first section** add a `div`. Inside that, add a **heading** (`h1`) and a **sub-heading** (`h2`). 
 
> ```html
...
<body>
	<section>
		<div>
			<h1>Your name</h2>
			<h2>Your specialties, eg: film maker</h2>
		</div>
	</section>
...
```

These will be the most important pieces of information in your page (for search engines like Google).

#### Images

Images are worth thousands of words, they say. So let's upload one to start with.

> To upload an image to Thimble, click on the green `+` on the top-left and the `Upload...`

The **image** to upload could be your logo or your profile picture.

> Once you've uploaded your picture, in that same `div`, underneath the headings, add an `<img>` code and set its `src` (source) to your image file, like so

> ```html
	...
	<h2>Your specialties, eg: film maker</h2>
	<img src="YOUR_IMAGE_FILE.jpg" alt="DESCRIBE THIS IMAGE">
</div>
...	
```

#### Text

> In the second section we'll have **textual content**, so let's write something in there.  
	
> ```html
...
<section> ... this is the first section ... </section>
<section>
	<p>Write something here to introduce your project and the ideas behind it.</p>
	<p>A little information about the process you took from research through to the development.</p>
	<p>You process is important!</p>
</section>
...
```

`p` is for *paragraph*.

#### Hyperlinks

> Add **hyperlinks** to your content using the `a` element (`a` is for *anchor*).
	
> ```html
<a href="http://example.com">the clickable text</a>
```

For instance:
```html
<section>
	<p>Influenced by the playful approaches to image-making used by Dadaist <a href="http://www.whitechapelgallery.org/exhibitions/hannah-hoch/">Hannah Höch</a>, I gathered a collection of portraits (Vogue portraits from the 1920's-40's and more current artist portraits) to create a collage of anonymous parts.</p>
</section>
```

#### Contact details

> Add your **contact details** to the last section.
 
```html
...
	<section>
		<div>
			<h3>Say hello!</h3>
			<p>YOUR_EMAIL@example.com</p>
		</div>	
	</section>
</body>
</html>	
```

### 2. Style later

Now the fun part: **CSS**!

#### Normalize

We want to tell the browser not to mess with our style.   
  
So we're going to use a little CSS utility called [**normalize.css**](https://necolas.github.io/normalize.css/), which resets the default browser's styles and provides a consistent common ground for our own styles. 

> Search `normalize.css` in Google and click on the first link. 

> Click the `Download` button and save the file by going to *File* and *Save Page As...*.

> Now upload that file to Thimble.

In order for your page to pick up the Normalize stylesheet, you'll need to add a `link` in the `head`, which will point to the `normalize.css` file.  
 
> ```html
...
<head>
	...
	<link rel="stylesheet" href="normalize.css">
	<link rel="stylesheet" href="style.css">
</head>
```

#### Your style

As you can see, `normalize.css` has flattened your page. Now you can start building your own style. 

There's a `link` in your `head` which points to another CSS file called **style.css**. This is where you add your styles.

#### Typography

We are going start with **typography**. 
	
> Go to [Google Fonts](https://www.google.com/fonts).

> Choose a typeface you like by clicking on the `Quick-use` button (arrow pointing right). 

> Then grab the `link` code for it and paste it in your page's head. 

> Where? Between `normalize.css` and  `style.css`

> ```html
...
<head>
	...
	<link rel="stylesheet" href="normalize.css">
	<link href='https://fonts.googleapis.com/css?family=Source+Code+Pro:400,300,700,900' rel='stylesheet' type='text/css'>
	<link rel="stylesheet" href="style.css">
</head>
```

Let's give some ground rules to our page, by applying them to the `body` element. Then we can set the rules for headings, paragraphs and bold elements.

> ```css
body
{
	font-family: 'Lato', sans-serif;
}
```

#### Readability

To center the content sections and make them easier to read, we add `class="content"` to all the `section` elements that contain text in HTML.

Then in CSS we create a rule for those `section` elements *classified* as `content`. 


```css
.content 
{
	margin: 2rem auto;
	max-width: 40rem;
	padding: 0 1rem;
}
```

`.` is a shortcut for `class`.

#### Full-size

Let's work on the **full-size images**.   
  
First we want to get some `section` elements in our page to take the full browser height. So we create a `.full` class and give it a `height: 100%;` property.

```css
.full
{
	height: 100%;
}
```

This is not enough though. 

It is important to understand what `height: 100%;`means: _the full height of the parent element_. It doesn't magically mean *the height of the browser window*. So if you want your main container to have the height of the browser window, setting `height: 100%;` isn’t enough.

_Why?_ Because the parent of your `section` (`body`) has its height set by default to `auto`, which means it is sized according to its _content_. You can try adding `height: 100%;` to the `body` element to see… it is still not enough.

_Why?_ Because the parent of `body` (`html`) has also its height set by default to `auto`. Now what if you try to add `height: 100%;` to the `html` element? It works!

```css
html, body
{
	height: 100%;	
}
```

#### Background images

Now onto the **images**. We're going to use `background-image` to define a few images that will be applied to the background of our `.full` elements. 

We are going to add our `background-image` directly into our HTML. For each `section` with the class `.full` add in `style="background-image: url('image.jpg')"`

For example:
```html
<section class="full" style="background-image: url('image.jpg')">
	<div>
		<h1>Your name</h2>
		<h2>Your specialties, eg: film maker</h2>
		<img src="profilepic.jpg" alt="Describe this image">
	</div>
</section>
```

By default background-images *tile*, but we want them to take up the whole available screen space, without losing their aspect ratio (no squashing). 

We can achieve that with `background-size`. This property can take various values: pixel sizes, percentages, and then a couple of interesting keywords. 

* `contain` will scale the image so as to be as large as possible providing that it is **contained** within the background positioning area. 
* `cover` instead, will scale the image, this time to be as large as possible so that the background positioning area is completely **covered** by the background image.

We're going to add `background-size: cover;` to the `.full` rule (so that it will apply to all sections with the `full` class).
```css
.full
{
	height: 100%;
 		background-size: cover;
}
```

#### Image sizes

Next we're styling the **logo** or **profile picture**.

By default images will be added to the top-left corner of their *parent*.

If we want it to be centred, we need CSS. 

Let's give the `img` a class `profile`.
```html
<img class="profile" src="profilepic.jpg" alt="Describe this image">
```

We can set a height and width for our image
```css
.profile 
{
	height: 10rem;
	width: 10rem;
}
```

We also can make sure that the `img` is not bigger than its container

```css
.profile 
{
	height: 10rem;
	width: 10rem;
	max-width: 100%;
}
```

#### Aligning stuff
	
To center the image, we create two classes `h-centred` and `v-centred`.

```css
.h-centred
{
	display: flex;
	justify-content: center;
}
.v-centred
{
	display: flex;
	align-items: center;
}
```

Let's add them to our HTML `section`.

```html
<section class="full h-centred v-centred" style="background-image: url('image.jpg')">
	<div>
		<h1>Your name</h2>
		<h2>Your specialties, eg: film maker</h2>
		<img class="profile" src="profilepic.jpg" alt="Describe this image">
	</div>
</section>
```

We can see the `div` has moved into the centre of the screen, but the content inside it is still aligned to the left. Let's add some CSS to fix that. Add some style into the `div`.

```html
<div style="text-align: center">
	<h1>Your name</h2>
	<h2>Your specialties, eg: film maker</h2>
	<img class="profile" src="profilepic.jpg" alt="Describe this image">
</div>
```

#### Scrolling effect

Now we want to get the **curtain reveal effect**, so that instead of scrolling with the rest of the page, the background-images will be revealed as we scroll up and down. That makes our page more interesting.

We can achieve this with another CSS property, `background-attachment`. With this property we have two options: 

* `scroll` (default): the background image will scroll with the rest of the content.
* `fixed`: the background image will remain stationary as the rest of the content is scrolled

Which one do we want? Obviously `fixed`.

Add `background-attachment: fixed;` to `.full`

```css
.full
{
	height: 100%;
 	background-size: cover;
 	background-attachment: fixed;
}
```

This **demo** is at [j.mp/html-css-portfolio-demo](http://j.mp/html-css-portfolio-demo). Click `Remix` to reveal all its **source code**.	



<!--- [ ] cropping images and saving them for Web-->


### License

[![](https://i.creativecommons.org/l/by-nc-sa/4.0/88x31.png)](http://creativecommons.org/licenses/by-nc-sa/4.0)

This work is licensed under a [Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License ](http://creativecommons.org/licenses/by-nc-sa/4.0)
