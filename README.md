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
