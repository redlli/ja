---
title: The Cube 
layout: def
permalink: cube
icon: https://play-lh.googleusercontent.com/BO_CWEtEvXpG5pLiPXm1D2q0P7lgvbz54KHv0Z7VSz3KgLvF1RhuOmFhg0l3ElDb3C_YFUwn7k_ZSr4dOXVlRPk=w240-h480-rw
description: Tap Tap and Tap   
keywords: The Cube, Casual Games, Offline Game, No Net, Tap, Cube game
---
<style>
    .images {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(30px, 1fr));
        gap: 15px;
        margin-top: 20px;
    }
    .images img {
        width: 100%;
        height: auto;
        border-radius: 10px;
        border: 2px solid #ffffff;
        outline: 1px solid rgba(0, 0, 0, 0.1);
        box-shadow: 0px 4px 8px rgba(0,0,0,0.2);
        cursor: pointer;
    }
     .fullscreen {
        position: fixed;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        background: rgba(0, 0, 0, 0.9);
        display: flex;
        align-items: center;
        justify-content: center;
        flex-direction: column;
        z-index: 1000;
    }
    .fullscreen img {
        max-width: 90%;
        max-height: 90%;
        border-radius: 10px;
        border: 3px solid #ffffff;
    }
    .nav-arrow {
        position: absolute;
        top: 50%;
        transform: translateY(-50%);
        font-size: 5vw;
        color: white;
        cursor: pointer;
        user-select: none;
    }
    .prev { left: 20px; }
    .next { right: 20px; }

    /* Store Links & Buttons Custom Styling */
    .store-links a {
        display: inline-flex;
        align-items: center;
        justify-content: center;
        height: 50px; 
        margin: 10px;
        vertical-align: middle;
        border: 2px solid #ffffff; 
        border-radius: 6px;
        box-shadow: 0px 4px 8px rgba(0,0,0,0.2);
        box-sizing: border-box; 
    }

    /* Standardizing the images inside the anchor tags */
    .store-links a img {
        height: 100%;
        width: auto;
        display: block;
        border-radius: 4px; 
    }
</style>

<div class="container">
    <h1>The Cube</h1>
    <h2>Tap as much as you want</h2>

    <div class="features">
        <h2>Key Features:</h2>
        <div class="feature-item">1) Simple and Clean UI.</div>
        <div class="feature-item">2) Not a brainrot.</div>
        <div class="feature-item">3) Lots of levels.</div>

    <div class="images">
        <img src="https://play-lh.googleusercontent.com/z9O7g6Saz7YWDY-o6af-rSrEmkeaxEbJBWjXmdM0F_0mlNWMyGdC9J6Su52QMWAUJZCagPmxuVycVTFxqIUj2A=w2560-h1440-rw" alt="Screenshot 1">
        <img src="https://play-lh.googleusercontent.com/IUKJ3vx3jdAc4gwkj-DJQBcXK45e5Bk6qpWqxoN5gQwhWKukaKxo6xzcr9RGCijESnTWCJDeLBBjApqfP8hi=w2560-h1440-rw" alt="Screenshot 2">
        <img src="https://play-lh.googleusercontent.com/R8uml29NVN9HK57lEUx1_ZpFxT4ClgTm1G4Ws2fBDsZUNiCyRHID_lDJdqKAU6OppBEzUs5Pc3VzZfPzxF2OIQ=w2560-h1440-rw" alt="Screenshot 3">
        <img src="https://play-lh.googleusercontent.com/eq9QzTeTS7C3TFR_5q-sFCmrw8h3KuhAyCwKZFqvSTRi033Zl4RUCZwobwxWuf8MqnolcLDtRX00xjI4xttC=w2560-h1440-rw" alt="Screenshot 4">
    </div>
    
    <div class="store-links" style="margin-top: 20px;">
        <a href="https://play.google.com/store/apps/details?id=com.ja.redlii.cube">
            <img src="/assets/img/icons/GetItOnGooglePlay.png" alt="Get it on Google Play">
        </a>
        
        <a href="https://ja-by-redlii.itch.io">
            <img src="/assets/img/icons/GetItOnItch.svg" alt="Get it on Itch.io">
        </a>

        <a href="https://github.com/redlli">
            <img src="/assets/img/icons/GetItOnGit.svg" alt="Git Code">
        </a>
    </div>

</div>
---
<h2><a class="linkhai" href="/cube/privacy-policy">Privacy Policy</a></h2>
---
<script>
    let images = [];
    let currentIndex = 0;

    function showImage(index) {
        currentIndex = index;
        
        // Create full-screen image container
        let fullscreenDiv = document.createElement("div");
        fullscreenDiv.className = "fullscreen";
        
        // Create image element
        let img = document.createElement("img");
        img.src = images[currentIndex];

        // Create navigation arrows
        let prevArrow = document.createElement("div");
        prevArrow.className = "nav-arrow prev";
        prevArrow.innerHTML = "◀";
        prevArrow.onclick = function() { changeImage(-1); };

        let nextArrow = document.createElement("div");
        nextArrow.className = "nav-arrow next";
        nextArrow.innerHTML = "▶";
        nextArrow.onclick = function() { changeImage(1); };

        // Add event listener to close image when clicked outside
        fullscreenDiv.onclick = function (event) {
            if (event.target === fullscreenDiv) {
                document.body.removeChild(fullscreenDiv);
            }
        };

        // Append elements to full-screen container
        fullscreenDiv.appendChild(prevArrow);
        fullscreenDiv.appendChild(img);
        fullscreenDiv.appendChild(nextArrow);
        document.body.appendChild(fullscreenDiv);
    }

    function changeImage(direction) {
        currentIndex = (currentIndex + direction + images.length) % images.length;
        document.querySelector(".fullscreen img").src = images[currentIndex];
    }

    document.addEventListener("DOMContentLoaded", function () {
        images = Array.from(document.querySelectorAll(".images img")).map(img => img.src);
        document.querySelectorAll(".images img").forEach((img, index) => {
            img.onclick = function () {
                showImage(index);
            };
        });
    });
</script>
