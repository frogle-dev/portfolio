---
layout: post 
title: About Me
description: About me (Jonah Larsson)
menu: nav/home.html
---

## As a conversation Starter

Here are some places I have lived.

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
	    {"flag": "b/b9/Flag_of_Oregon.svg", "greeting": "Greeting - Hi", "description": "Oregon - 5 years"},
        {"flag": "0/01/Flag_of_California.svg", "greeting": "Greeting - Hey", "description": "California - 9 years and counting"}
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

### Journey through Life

Here is what I did at these places

- 🏫 Preschool in Portland, Oregon
- ✈️ Moved to California to get closer to most of my family
- 🏫 Stone Ranch Elementary School in San Diego, California
- 🏫 Oak Valley Middle School in San Diego, California
- 🏫 Del Norte High School in San Diego, California

### Friends, Family, and Fun

The things I care about the most are my family and my friends. I try to live my life to the fullest and have a lot of fun.

- My mom is a first generation Filipino in the USA
- My mom's mom had 12 siblings and she had to work with them to slowly get each sibling to the US
- My dad is Swedish and he moved to the US more than 20 years ago
- My family is really big because my grandma on my mom's side had 12 siblings and my dad had 3 siblings

<comment>
Gallery of Pics, these are photos of my travels and hanging out with my friends
</comment>
<div class="image-gallery">
  <img src="{{site.baseurl}}/images/about/IMG_3414.jpg" alt="Image 1">
  <img src="{{site.baseurl}}/images/about/IMG_3616.jpg" alt="Image 2">
  <img src="{{site.baseurl}}/images/about/IMG_3762.jpg" alt="Image 3">
  <img src="{{site.baseurl}}/images/about/IMG_3874.jpg" alt="Image 4">
  <img src="{{site.baseurl}}/images/about/IMG_4239.jpg" alt="Image 5">
  <img src="{{site.baseurl}}/images/about/IMG_5722.jpg" alt="Image 6">
  <img src="{{site.baseurl}}/images/about/IMG_6127.jpg" alt="Image 7">
</div>
