# axios_issue

Been away from JS for a minute or two working in python and now I want to try to accomplish some of the same tasks I have been working on in python, with JS. I can't get past the stupidest thing! With Axios installed as a dependency,

  "dependencies": {
    "axios": "^0.19.2"
  }

Trying to use axios from line number one of the script:

import axios from 'axios' 
r = axios.get('https://swapi.dev')
console.log(r)

I keep getting:

Uncaught SyntaxError: import declarations may only appear at top level of a module

After having read all the SO posts on this error and after making sure that I am calling the script itself as

<script type="module" src="/main.js"></script>
<script type="module" src="main.js"></script>
<script type="module" src="./main.js"></script>

which produces:

Uncaught TypeError: Error resolving module specifier: axios main.js:1:18

and as:

<script src="./main.js"></script>
<script src="/main.js"></script>
<script src="main.js"></script>

which produces:

 Uncaught SyntaxError: import declarations may only appear at top level of a module :1:18

I have referred to:

https://developer.mozilla.org/en-US/docs/Web/HTML/Element/script

So I have covered most bases before reposting this one.

Also just using code right out of the documentation causing the same error.

   axios.get('https://swapi.dev')
.then(function (response) {

// handle success
   console.log(response);
})
.catch(function (error) {

// handle error
  console.log(error);
})
  .finally(function () {

// always executed
  });

I am publicly shaming myself to get past this stupid issue! This is clearly some kind of "run home to momma" error coming from the browser and I suspect WEBPACK.

I am unaware of any new game changing changes I might not heard about.

I am rusty, I know the good is super basic (I HOPE it's super basic) and I just want an error. The one I am getting is not telling me what's really going on.

Thanks for any help with this!

Fresh install of Windows and VSCode on a new machine 
