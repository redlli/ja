---
title: Save Jeny 
layout: def
permalink: save-jeny
icon: /Projects/save_jeny/img/icon.png
description: Save Jeny While trying to save a cat, Jeny fell into a dungeon-like pit. She broke her leg, so she cannot climb out. She is not alone down there; the pit is filled with huge, hungry lizards. Her only way to survive the day is to keep moving, stay alert, and avoid getting attacked by the lizards.
keywords: SaveJenny, Survival, IndieDev, MobileGaming, GamingCommunity, Rotate, IndieGame, LizardPit
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
    <h1>Save Jeny</h1>
    <h2>While trying to save a cat, Jeny fell into a dungeon-like pit. She broke her leg, so she cannot climb out. She is not alone down there; the pit is filled with huge, hungry lizards. Her only way to survive the day is to keep moving, stay alert, and avoid getting attacked by the lizards.</h2>

    <div class="features">
        <h2>Key Features:</h2>
        <div class="feature-item">1) Simple and Clean UI.</div>
        <div class="feature-item">2) Not a brainrot.</div>
        <div class="feature-item">3) Lots of levels.</div>
    </div> 
    
    <div class="images">
        <img src="/Projects/save_jeny/img/0.png" alt="Screenshot 1">
        <img src="/Projects/save_jeny/img/1.png" alt="Screenshot 2">
        <img src="/Projects/save_jeny/img/2.png" alt="Screenshot 3">
    </div>

    <div class="store-links" style="margin-top: 20px;">
        <a href="https://play.google.com/store/apps/details?id=com.ja.redlii.savejeny">
            <img src="/assets/img/icons/GetItOnGooglePlay.png" alt="Get it on Google Play">
        </a>
        
        <a href="https://ja-by-redlii.itch.io/save-jeny">
            <img src="/assets/img/icons/GetItOnItch.svg" alt="Get it on Itch.io">
        </a>

        <a href="https://github.com/redlli/The-Cube">
            <img src="/assets/img/icons/GetItOnGit.svg" alt="Git Code">
        </a>
    </div>
</div>

<hr>
<h2><a class="linkhai" href="/save-jeny/privacy-policy">Privacy Policy</a></h2>
<hr>

<script>
    let images = [];
    let currentIndex = 0;

    function showImage(index) {
        currentIndex = index;
        
        let fullscreenDiv = document.createElement("div");
        fullscreenDiv.className = "fullscreen";
        
        let img = document.createElement("img");
        img.src = images[currentIndex];

        let prevArrow = document.createElement("div");
        prevArrow.className = "nav-arrow prev";
        prevArrow.innerHTML = "◀";
        prevArrow.onclick = function(e) { 
            e.stopPropagation(); 
            changeImage(-1); 
        };

        let nextArrow = document.createElement("div");
        nextArrow.className = "nav-arrow next";
        nextArrow.innerHTML = "▶";
        nextArrow.onclick = function(e) { 
            e.stopPropagation(); 
            changeImage(1); 
        };

        fullscreenDiv.onclick = function (event) {
            if (event.target === fullscreenDiv) {
                document.body.removeChild(fullscreenDiv);
            }
        };

        fullscreenDiv.appendChild(prevArrow);
        fullscreenDiv.appendChild(img);
        fullscreenDiv.appendChild(nextArrow);
        document.body.appendChild(fullscreenDiv);
    }

    function changeImage(direction) {
        currentIndex = (currentIndex + direction + images.length) % images.length;
        const fullImg = document.querySelector(".fullscreen img");
        if (fullImg) {
            fullImg.src = images[currentIndex];
        }
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
