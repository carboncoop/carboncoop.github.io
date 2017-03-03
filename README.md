# Energise Festival Website

Development Set Up
------------------

Make sure you have the following installed:

- npm — http://blog.npmjs.org/post/85484771375/how-to-install-npm
- Sass — http://sass-lang.com/install
- Jekyll — https://jekyllrb.com/docs/installation/

And the latest versions:

```
npm install npm@latest -g
gem update sass
gem update jekyll
```

Checkout the dev branch:

```
git checkout dev
```

Open two terminal windows, and run this in the first:

```
npm start
```

And this in the second:

```
npm run build:watch
```

Visit: http://127.0.0.1:4000/

Adding Content
--------------

To add a section to the page:

```
<section class="page-section page-section--green">

    <div class="grid">
        <h2 class="grid__col5 page-section__title">… Section Title …</h2>
        <p class="grid__col7 page-section__intro">… Section intro …</p>
    </div>

    … items …

</section>
```

Then add items inside the section:

```
<div class="page-item page-item--green">
    <div class="grid">
        <div class="grid__col5">
            <div class="page-item__image">
                <img src="… your img url …" alt="">
            </div>
        </div>
        <div class="grid__col7">
            <div class="page-item__header">
                <h3>… Item Title …</h3>
                <p>… Date … <br />… Time …</p>
            </div>
            <div class="page-item__body">
                <p>… Item description …</p>
            </div>
        </div>
    </div>
</div>
```

If the item doesn’t have an image, you can drop the `<img>` element and you’ll get a fallabck background pattern:

```
<div class="page-item page-item--green">
    <div class="grid">
        <div class="grid__col5">
            <div class="page-item__image">
            </div>
        </div>
        …
    </div>
</div>
```


Deployment
----------

This is a quick helper command. It should work, but it’s untested.

```
npm run deploy
```

To run the steps manually instead:

```
npm run build
git checkout master
git merge dev 
  (or another branch, if your changes aren’t in dev)
git push origin master
```
