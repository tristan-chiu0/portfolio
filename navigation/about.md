---
layout: post
title: About
permalink: /about/
comments: true
---

## As a conversation Starter

Hello. My name is Tristan, and here are some places I have lived or traveled to. 

<comment>
Flags are made using Wikipedia images
</comment>

<style>
    /* Style looks pretty compact, 
       - grid-container and grid-item are referenced the code 
    */
    .grid-container {
        display: grid;
        grid-template-columns: repeat(auto-fill, minmax(150px, 1fr)); /* Dynamic columns */
        gap: 10px;
    }
    .grid-item {
        text-align: center;
    }
    .grid-item img {
        width: 100%;
        height: 100px; /* Fixed height for uniformity */
        object-fit: contain; /* Ensure the image fits within the fixed height */
    }
    .grid-item p {
        margin: 5px 0; /* Add some margin for spacing */
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

## Basic Information About Me
- Ethnicity: I am Asian American, specifically Chinese-Japanese American
- Location: I have lived in California for my whole life.
- Favorite Foods: Pasta, Ramen, Strawberries, Pastries
- Grade: I am in 12th Grade
- Age: 17 years old

## My Family
- I have a Mother and a Father, but 0 siblings
- I have 1 Cat named Snuggles
- Used to have another cat named Jet and a dog named Zoe, but they passed away unfortunately

<div class="image-fam">
  <img src="{{site.baseurl}}/images/about/image.png" alt="Snuggles The Cat">
</div>

<style>
.image-fam {
  display: flex;
  text-align: center;
}

.image-fam img {
  height: 300px ;
  width: 300px ;
  /*max-width: 300px;*/
  border-radius: 10px ;
}
</style>

## Hobbies and Interests
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

<style>
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
</style>