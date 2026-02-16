# FEDev-practical-sample-stage-2

NOTE: A Captioned video work through of this stage has been published at:
- (coming soon)

This document summarises the steps I took when creating my solution to the sample FEDev Practial 1

The stages of development required are:
```
Stage 1. Basic HTML structure for 2 pages: “index.html” and “characters.html”
   a. No CSS
   b. No links
   c. No images

Stage 2. Add images

Stage 3. Add nav links

Stage 4. Add CSS, to make the pages look like the provided screenshots
   a. Using CSS style rules in 1 or more “.css” files

Stage 5. Refactor the website as a Svelte(kit) project
   a. Demonstrate reusable Svelte components, such as:
       i. Nav bar
       ii. page footer

Stage 6. Add a third “merchandise” page
   a. Add a link to this page in the nav bar
   b. Style this in a similar style to the other 2 pages
   c. Find images from the web for several merchandise items
   d. Add a form at the bottom of this page asking for:
       i. Name / email address / postal address
       ii. (you do NOT have to write code to process this forms submission)

Stage 7. For an ‘A’ grade illustrate some/all of the following:
   a. Replacing standard CSS rules with TailWindCSS
   b. Populating the merchandise page contents by looping through JSON data
   (rather than hard coded page content)
   c. Publish the site as static pages via GitHub Actions
```

Stage 2. Add images

To add images we need to add `<img>` elements to our pages.

1. For the home page there are 3 images needed:
   - we'll ensure each of these images is inside an appropriate document element (we already have `<footer>`, we'll add `<header` and `<main>`)
   - we'll addd an appropriate `alt` description of these logos/splash images in the image elements

1. the logo at the top of the page - we'll put this inside a `<header>` element
         
    ```html
    <header>
        <img src="/images/title.png" alt="Rings of power logo" />
    </header>
    ```

1. the main home page image - we'll put this inside a `<main>` element

    ```html
    <main>
        <img src="/images/homeimage.jpg" alt="Rings of power - splash image" />
    </main>
    ```

   
1. the Prime logo in the footer

    ```html
    <header>
        <img src="/images/prime_logo.png" alt="Prime logo" />
    </header>
    ```

1. For the characters page, we can duplicate the `<header>` and `<footer>` elements

1. For each character we need to add an image element for that character
   - since the images' names describe the character image inside, the image name is fine as out `alt` value
     - although if you wish, you could make it more descriptive, such as `alt="image of character "galadriel"`
    
    ```html
    <img src="/images/galadriel.jpg" alt="galadriel.jpg">
    <h3>GALADRIEL</h3>
    <p>
    Galadriel, an Elf is a key part of the story. We meet her in the Lord of the Rings, when she welcomes the Fellowship to Lothlórien. In The Rings of Power, we meet a younger Galadriel who is a very diﬀerent Galadriel: a fierce warrior who we meet on a mission to find Sauron after her brother died at his hands.
    </p>
    
    <img src="images/halbrand.jpg" alt="halbrand.jpg">
    <h3>HALBRAND</h3>
    <p>
    After abandoning her ship to continue her mission to locate Sauron, she’s left adrift in the Sundering Seas before a broken boat full of humans rescue her. Among them is Halbrand who develops an uneasy alliance with Galadriel as the pair begin their journey to the island of Numenor.
    </p>
    
    <img src="images/elrond.jpg" alt="elrond.jpg">
    <h3>ELROND</h3>
    <p>
    Elrond, the half-elf and the future leader of Rivendell. We meet younger version of Elrond as a young politician who finds himself kept out of key discussions as he is not yet a lord. However, Elrond is soon tasked with another mission, helping the legendary smith Celebrimbor.
    </p>
    
    <img src="images/durin.jpg" alt="durin.jpg">
    <h3>PRINCE DURIN IV</h3>
    <p>
    During the Second Age, Khazad-dûm was the home to the dwarven kingdom, long before it falls into ruin. The kingdome is ruled over by King Durin III, who is supported by his son Prince Durin IV. We meet Durin IV burdened with the responsibility of keeping their kingdom thriving, and protecting it from outsiders.
    </p>
    
    <img src="images/disa.jpg" alt="disa.jpg">
    <h3>DISA</h3>
    <p>
    Disa is Durin IV’s wife, who lives with him and their children in Khazad-dûm. Disa is also noted for her beautiful singing voice and fierceness.
    </p>
    
    <img src="images/arondir.jpg" alt="arondir.jpg">
    <h3>ARONDIR</h3>
    <p>
    Arondir is a Silvan Elf soldier stationed in the Southlands, a station set up to keep an eye on the humans of the realm, after they allied with Morgoth during the First Age.
    </p>
    
    <img src="images/gandalf.jpg" alt="gandalf.jpg">
    <h3>THE STRANGER</h3>
    <p>
    A mysterious character for the moment. Nori spots him after a meteor lands in the woods where she lives. But the tall man doesn’t speak their language and is like no one they’ve ever seen before.
    </p>
    
    <img src="images/nori.jpg" alt="nori.jpg">
    <h3>NORI</h3>
    <p>
    Nori is one of the Harfoots, the early predecessors to the Hobbits, who migrate with the seaso
    </p>
    ```

