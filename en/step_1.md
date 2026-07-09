## Build the page

Choose a theme and create the page structure for your fan website.

Pick something you would enjoy sharing, then choose three options inside that theme. The dinosaur example uses three species, but your project could be about teams, games, films, fashion, or anything else you love.

Update the title, the menu text, and the empty sections that will hold your content.

```html filename="index.html" line_numbers="true" line_number_start="8" line_highlights="8,14-18,24-32"
<title>Dinosaurs: ROAR!</title>
  </head>
  <body>
    <header>
      <nav>
        <div class="dropdown">
          <button onclick="openDropdown()">Choose Dinosaur &#9207;</button>
          <div id="dropdown-options">
            <button onclick="option1()">Tyrannosaurus Rex</button>
            <button onclick="option2()">Triceratops</button>
            <button onclick="option3()">Stegosaurus</button>
          </div>
        </div>
      </nav>
    </header>
    <main>
      <section id="instruction">
        <h1>Select a dinosaur &#129429;</h1>
      </section>
      <section id="content-holder">
        <h1 id="title">Dinosaur</h1>
        <div id="slot-1" class="content"></div>
        <div id="slot-2" class="content"></div>
        <div id="slot-3" class="content"></div>
      </section>
    </main>
```

Replace the dinosaur names with your own choices if you are making a different fan page.

## Now run your code

Run the project and check that your menu is at the top of the page and an instruction heading appears in the middle.
