# JAVASCRIPTMAS

<html>
   <head>
      <link rel="stylesheet" href="index.css">
   </head>
   <body>
      <div class="snowman">
         <div class="head">
            <div class="eyes">
               <div class="eye">
                  <div class="pupil"></div>
               </div>
               <div class="eye">
                  <div class="pupil"></div>
               </div>
            </div>
            <div class="nose"></div>
            <div class="mouth"></div>
         </div>
         <div class="snowman-body">
            <div class="button"></div>
            <div class="button"></div>
            <div class="button"></div>
         </div>
      </div>
      <div class="controls">
         <div>
            <input id="color" type="color" name="color" value="#99bbff"/>
            <label for="color">Eye Color</label>
         </div>
         <div>
            <input id="color3" type="color" name="color3" value="#ffa500"/>
            <label for="color3">Nose Color</label>
         </div>
         <div>
            <input id="color2" type="color" name="color2" value="#000"/>
            <label for="color2">Button Color</label>
         </div>
      </div>
      <script src="index.pack.js"></script>
   </body>
</html>

## INDEX.JS

  const inputs = document.querySelectorAll(".controls input");

// Task:
// Write a function to update the snowman colors according to the colors selected from the pickers.

// Stretch goals:
// - Add other items eg scarf, arms, etc.
// - Add different options for nose shape, or hats.
// - Check for contrast between pupils and eye color.

## INDEX.CSS

html, body {
    margin: 0;
    padding: 0;
}

:root {
  --color: #99bbff;
  --color2: #000;
  --color3: #ffa500;
}

body {
  --gold: #FAC57D;
  --snow: #F0F4F7;
  justify-content: center;
  align-items: center;
  height: 100vh;
  background-color: var(--gold)
}

.controls {
  order: -1;
  padding: 20px;
}

input,
.head,
.snowman-body,
.button {
  box-shadow: rgba(0, 0, 0, 0.1) 0px 4px 6px -1px, rgba(0, 0, 0, 0.06) 0px 2px 4px -1px;  
}

body,
.snowman-body,
.eyes {
    display: flex;
}

input {
  margin: 0.25em;
  border: none;
  cursor: pointer;
}

.head {
  margin-left: 30px;
  background: var(--snow);
  height: 10em;
  width: 10em;
  border-radius: 50%;
}

.snowman-body {
  flex-direction: column;
  justify-content: space-around;
  align-items: center;
  position: relative;
  margin-top: -18px;
  background: var(--snow);
  height: 14em;
  width: 14em;
  border-radius: 50%;
}

.button {
  height: 25px;
  width: 25px;
  border-radius: 50%;
  background-color: var(--color2);
}

.eye {
  border-top-left-radius: 75px;
  border-top-right-radius: 75px;
  height: 1em;
  width: 1em;
  background: var(--color);
  margin: 2.2em 2em 0;
}

.pupil {
  border-top-left-radius: 75px;
  border-top-right-radius: 75px;
  height: 0.5em;
  width: 0.5em;
  background: black;
  margin: 0.5em 0.25em;
}

.nose {
  width: 0;
  height: 0;
  border-style: solid;
  border-width: 10px 0 10px 40px;
  border-color: transparent transparent transparent var(--color3);
  margin: 2em 4.4em;  
}

.mouth {
  height: 0.25em;
  width: 2em;
  background: darkgray;
  border-radius: 50%;
  margin: 2em 4em;
}
