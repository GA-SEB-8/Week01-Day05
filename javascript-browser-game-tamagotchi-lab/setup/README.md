<h1>
  <span class="headline">Tamagotchi Lab</span>
  <span class="subhead">Setup</span>
</h1>

## Setup

Open your Terminal application and navigate to your `~/code/ga/labs` directory:

```bash
cd ~/code/ga/labs
```

Navigate to [GitHub](https://github.com/) and create a new repository named `javascript-browser-game-tamagotchi-lab`.

- Make sure the repo is set to `public`
- You do not need a `README.md`
- You do not need a `.gitignore`

Using the `Quick Setup` option, clone your newly created repo into your `~/code/ga/labs` directory with the `git clone` command:

```bash
git clone https://github.com/<your-username>/javascript-browser-game-tamagotchi-lab.git
```

> 🚨 Do not use the above command exactly. It will not work. Replace `<github-username>` (including the `<` and `>`) in the URL above with your username.

Next, `cd` into the new cloned directory:

```bash
cd javascript-browser-game-tamagotchi-lab
```

Then, create a `js` directory, a `css` directory, and an `assets` directory. You can make these directories with one line by adding a space between them after the `mkdir` command!

```bash
mkdir js css assets
```

Next, create an `app.js` file in the `js` directory, a `style.css` file in the `css` directory, and an `index.html` file in the root of the project. Create these files in one line by adding a space between them after the `touch` command. These files will hold your work for this lab:

```bash
touch ./js/app.js ./css/style.css index.html
```

With the files created, open the contents of the directory in VS Code:

```bash
code .
```

Next, [download this image](../assets/tomato.png?raw=true) and add it to the `assets` directory in your project.

### Starter code

There is some starter code associated with this lab. First, the HTML for your `index.html` file:

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Tamagotchi</title>
    <link rel="stylesheet" href="./css/style.css" />
    <script src="./js/app.js" defer></script>
  </head>

  <body>
    <header>
      <h1>Tamagotchi</h1>
    </header>
    <main>

      <!-- game interface / UI section -->
      <section class="button-wrapper">
        <button id="play">play</button>
        <button id="feed">feed</button>
        <button id="sleep">sleep</button>
      </section>

      <!-- game data section -->
      <section class="stats-wrapper">
        <p>Boredom: 
          <span id="boredom-stat">...</span>
        </p>
        <p>Hunger: 
          <span id="hunger-stat">...</span>
        </p>
        <p>Sleepiness:
          <span id="sleepiness-stat">...</span>
        </p>
      </section>

      <!-- game display / messaging section -->
      <section class="game-state-wrapper">
        <h2 id="message" class="hidden">
          Oh no! You Lose!
        </h2>
        <img 
          class="game-graphic" 
          alt="a tomato monster" 
          src="./assets/tomato.png" 
        />
        <button id="restart" class="hidden">Play Again</button>
      </section>
      
    </main>
  </body>
</html>
```

Next, add this CSS to your `css/style.css` file:

```css
/* global styles  */
* {
  box-sizing: border-box;
}

body {
  font-size: 16px;
  min-height: 100vh;
  background-color: #e6e6e6;
  font-family: system-ui, sans-serif;
}

/* element styles */
h1 {
  font-size: 3.5rem;
}

h2 {
  font-size: 1.7rem;
}

/* headings */
header {
  text-align: center;
}

/* layout */
main {
  max-width: 90vw;
  margin: 0 auto;
}

.button-wrapper {
  display: flex;
  justify-content: space-around;
}

.stats-wrapper {
  display: grid;
  text-align: center;
  grid-template-columns: repeat(3, 1fr);
}

.game-state-wrapper {
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
}

/* button styling*/
button {
  padding: 1.5rem;
  line-height: 1em;
  font-size: 1.5rem;

  border: 0;
  border-radius: 0.5rem;
  
  color: white;
  background-color: #4597f8;
  transition: background-color 2s cubic-bezier(0.075, 0.82, 0.165, 1);
}

button:hover {
  background-color: #3880d7;
}

button:active {
  background-color: #2e6bb6;
}

/* images */
.game-graphic {
  max-height: 33vmin;
  margin-bottom: 32px;
}

.hidden {
  visibility: hidden;
}

```

Finally, you can add a bit of optional boilerplate to your JavaScript to make it easier to find sections inside of it. Add it to your `js/app.js` if you'd like.

```javascript
/*-------------------------------- Constants --------------------------------*/



/*---------------------------- Variables (state) ----------------------------*/



/*------------------------ Cached Element References ------------------------*/



/*-------------------------------- Functions --------------------------------*/



/*----------------------------- Event Listeners -----------------------------*/


```

## Start the app

Open the `index.html` file in your browser and access the console output in your browser's dev tools.
