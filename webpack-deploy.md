<strong> this is how i deployed my webpack application</strong>

make sure you're on the main branch
insure your app has got a package.json file, which it already is if you're using webpack,
if not (which'd be weird) run npm init -y to set up one with all the default values.

run npm install gh-pages --save-dev 
(--save-dev) simply means you're installing this as a dev dependency

inside package.json
on top add this entry ==> "homepage":"http://KanoCode.github.io/name-of-repository",

add this to your scripts key 
"predeploy":"npm run build"
"deploy":"gh-pages -d build"

After you commit your changes you can run ==>  npm run deploy

<strong> Now for the fun part, the errors 🤗 </strong> 
You might have the terminal screem at you with the error below,

![This is an image](https://myoctocat.com/assets/images/base-octocat.svg)
which has it's own way of hurting your feelings but I solved it like so:



 Add this line to your script
 {
  "scripts": {
    "build": "webpack --config webpack.config.js"
  }
}

 
 
