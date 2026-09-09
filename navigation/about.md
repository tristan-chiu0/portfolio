---
layout: post
title: About
permalink: /about/
comments: true
---

<h4 class="page-kicker"> AP CSP - 2026-2027</h4>

Hello. My name is Tristan, and here are some places I have lived or traveled to. 

<nav class="toc">
  <a href="#basics">Basics</a>
  <a href="#family">Family</a>
  <a href="#hobbies">Hobbies</a>
</nav>

<p class="flag-attribution"> Flags are attributed to Wikimedia Commons </p>

<style>
    .page-kicker {
        margin: 0 0 6px;
        color: #b8860b;
        font-size: 0.85rem;
        font-weight: bold;
        letter-spacing: 0.04em;
    }

    .toc {
        display: flex;
        flex-wrap: wrap;
        gap: 8px;
        margin: 16px 0 24px;
    }

    .toc a {
        padding: 8px 14px;
        background: #181818;
        border: 1px solid rgba(255, 255, 255, 0.1);
        border-radius: 999px;
        color: #e29ce8;
        font-size: 0.85rem;
        font-weight: bold;
        text-decoration: none;
    }

    .toc a:hover {
        border-color: #e29ce8;
    }

    .flag-attribution {
        margin: 0 0 12px;
        font-size: 0.8rem;
        color: #999;
        font-style: italic;
    }

    .grid-container {
        display: grid;
        grid-template-columns: repeat(auto-fill, minmax(150px, 1fr));
        gap: 10px;
    }
    .grid-item {
        text-align: center;
        padding: 20px;
        background: #181818;
        border: 1px solid rgba(255, 255, 255, 0.1);
        border-radius: 5px;
    }
    .grid-item img {
        width: 100%;
        height: 100px;
        object-fit: contain;
        margin-bottom: 8px;
        border-radius: 6px;
    }
    .grid-item p {
        margin: 4px 0;
        font-size: 0.9rem;
        color: #f0f0f0;
    }
    .grid-item p:first-of-type {
        font-weight: bold;
        color: #ffffff;
    }

    .image-fam {
        display: flex;
        flex-direction: column;
        align-items: center;
        width: fit-content;
        margin: 16px auto;
        padding: 16px;
        background: #181818;
        border: 1px solid rgba(255, 255, 255, 0.1);
        border-radius: 5px;
    }
    .image-fam img {
        height: 300px;
        width: 300px;
        object-fit: cover;
        border-radius: 10px;
    }
    .image-fam-caption {
        margin: 10px 0 0;
        font-size: 0.9rem;
        font-weight: bold;
        color: #e29ce8;
    }

    .image-gallery {
        display: flex;
        flex-wrap: nowrap;
        overflow-x: auto;
        gap: 10px;
    }
    .image-gallery img {
        max-height: 150px;
        object-fit: cover;
        border-radius: 5px;
    }
    .cat-box {
        position: relative;
        width: 100%;
        height: 120px;
        margin: 30px 0;
        background: #181818;
        border: 1px solid rgba(255, 255, 255, 0.1);
        border-radius: 14px;
        overflow: hidden;
    }

    .cat-walker {
        position: absolute;
        bottom: 14px;
        left: 0;
        animation: cat-bob 0.3s infinite alternate;
    }
    .cat-sprite {
        display: inline-block;
        font-size: 2rem;
        transition: transform 0.15s ease;
    }
    @keyframes cat-bob {
        from { transform: translateY(0); }
        to { transform: translateY(-4px); }
    }
</style>

<!-- This grid_container class is used by CSS styling and the id is used by JavaScript connection -->
<div class="grid-container" id="grid_container">
    <!-- content will be added here by JavaScript -->
</div>

<script>
    // 1. Make a connection to the HTML container defined in the HTML div
    var container = document.getElementById("grid_container"); // This container connects to the HTML div

    // 2. Define a JavaScript object for our http source and our data rows for the Living in the World grid
    var http_source = "https://upload.wikimedia.org/wikipedia/commons/";
    var living_in_the_world = [
        {"flag": "0/01/Flag_of_California.svg", 
        "greeting": "California", 
        "description": "My Birthplace"},
        {
        "flag": "9/9e/Flag_of_Japan.svg?utm_source=commons.wikimedia.org&utm_campaign=index&utm_content=original",
        "greeting": "Been Here 2 Times Once in 2024 and Once in 2025",
        "description": "Travel Location"
        },
        {
        "flag": "9/9d/Flag_of_Arizona.svg?utm_source=commons.wikimedia.org&utm_campaign=index&utm_content=original",
        "greeting": "Arizona (Phoenix) - My Aunt Lives Here, Periodic Thanksgiving Visits",
        "description": "Travel Location"
        },
        {
        "flag": "e/ef/Flag_of_Hawaii.svg",
        "greeting": "Hawaii (Honolulu)- My Grandparents Live Here",
        "description": "Travel Location"
        },
    ];

    // 3a. Consider how to update style count for size of container
    // The grid-template-columns has been defined as dynamic with auto-fill and minmax

    // 3b. Build grid items inside of our container for each row of data
    for (const location of living_in_the_world) {
        // Create a "div" with "class grid-item" for each row
        var gridItem = document.createElement("div");
        gridItem.className = "grid-item";  // This class name connects the gridItem to the CSS style elements
        // Add "img" HTML tag for the flag
        var img = document.createElement("img");
        img.src = http_source + location.flag; // concatenate the source and flag
        img.alt = location.flag + " Flag"; // add alt text for accessibility

        // Add "p" HTML tag for the description
        var description = document.createElement("p");
        description.textContent = location.description; // extract the description

        // Add "p" HTML tag for the greeting
        var greeting = document.createElement("p");
        greeting.textContent = location.greeting;  // extract the greeting

        // Append img and p HTML tags to the grid item DIV
        gridItem.appendChild(img);
        gridItem.appendChild(description);
        gridItem.appendChild(greeting);

        // Append the grid item DIV to the container DIV
        container.appendChild(gridItem);
    }
</script>

<h2 id="basics">Basic Information About Me</h2>
- Ethnicity: I am Asian American, specifically Chinese-Japanese American
- Location: I have lived in California for my whole life.
- Favorite Foods: Pasta, Ramen, Strawberries, Pastries

<h2 id="family">My Family</h2>
- I have a Mother and a Father, but 0 siblings
- I have 1 Cat named Snuggles
- Used to have another cat named Jet and a dog named Zoe, but they passed away unfortunately

<div class="image-fam">
  <img src="{{site.baseurl}}/images/about/image.png" alt="Snuggles The Cat">
  <p class="image-fam-caption"> This is my cat! He is around 4-5 years old. </p>
</div>

<h2 id="hobbies">Hobbies and Interests</h2>
- I like to play video games, draw, play the piano, and listen to music
- Some video games I've played are Hollow Knight (and Silksong), Don't Starve Together, Terraria, Slime Rancher, Undertale, and OMORI just to name a few.
- My taste in music includes Jpop, instrumentals, music from video games, and an assortment of other random pieces. 

<div class="image-gallery">
  <img src="{{site.baseurl}}/images/about/HK_header.png" alt="Hollow Knight">
  <img src="{{site.baseurl}}/images/about/terraria_tree.png" alt="Terraria Tree">
  <img src="{{site.baseurl}}/images/about/slimerancher_slimes.jpg" alt="Slime Rancher slimes">
  <img src="{{site.baseurl}}/images/about/omor_whitespace.png" alt="OMORI White Space">
  <img src="{{site.baseurl}}/images/about/bird.png" alt="Bird Drawing">
  <img src="{{site.baseurl}}/images/about/undertale_souls.jpg" alt="Undertale Souls">
  <img src="{{site.baseurl}}/images/about/Apple-Cinnamon-Pastries.jpg" alt="Cinnamon Pastries">
</div>

<div class="cat-box" id="cat-box">
  <div class="cat-walker" id="cat-walker">
    <span class="cat-sprite" id="cat-sprite">🐈‍⬛</span>
  </div>
</div>

<script>
    var box = document.getElementById("cat-box");
    var walker = document.getElementById("cat-walker");
    var cat = document.getElementById("cat-sprite");
    
    var position = 0;
    var direction = 1;
    var speed = 1;
    
    var actions = ["walk", "idle", "sleep"];
    var currentAction = "walk";

    var lookInterval = null;

    var catFacing = 1; // shared, single source of truth for orientation

    function startLooking() {
        catFacing = catFacing === 1 ? -1 : 1;
        cat.style.transform = "scaleX(" + catFacing + ")";
    }



    function pickNewAction() {
        currentAction = actions[Math.floor(Math.random() * actions.length)];
        var nextAction;
        do {
            nextAction = actions[Math.floor(Math.random() * actions.length)];
        } while (nextAction === currentAction);

        currentAction = nextAction;
        // actions for the cat
        if (currentAction === "sleep") {
            cat.textContent = "🍞";
            walker.style.animationPlayState = "paused";
        } else if (currentAction === "idle") {
            cat.textContent = "🐈‍⬛";
            walker.style.animationPlayState = "paused";
            startLooking();
        } else {
            cat.textContent = "🐈‍⬛";
            walker.style.animationPlayState = "running";
            catFacing = direction === -1 ? 1 : -1;
            cat.style.transform = "scaleX(" + catFacing + ")";
        }

        var nextDelay = 2500 + Math.random() * 3000;
        setTimeout(pickNewAction, nextDelay);
    }

    pickNewAction();

    function walk() {
        var boxWidth = box.clientWidth;
        var catWidth = cat.offsetWidth;

        if (currentAction === "walk") {
            position += speed * direction;

            if (position <= 0) {
                direction = 1;
            } else if (position + catWidth >= boxWidth) {
                direction = -1;
            }

            walker.style.left = position + "px";
            catFacing = direction === -1 ? 1 : -1;
            cat.style.transform = "scaleX(" + catFacing + ")";
        }

        requestAnimationFrame(walk);
    }

    walk();
</script>