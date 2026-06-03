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
        box-shadow: 0px 4px 8px rgba(0,0,0,0.2);
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

    /* GitHub Button Styling */
    .github-btn {
        display: inline-flex;
        align-items: center;
        background-color: #24292e;
        color: white;
        padding: 10px 20px;
        font-size: 16px;
        font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, Arial, sans-serif;
        font-weight: 600;
        border-radius: 6px;
        text-decoration: none;
        margin: 3%;
        vertical-align: middle;
        height: 40px; /* Aligns visually with the play store badge height */
        box-shadow: 0px 4px 8px rgba(0,0,0,0.2);
        transition: background-color 0.2s;
    }
    .github-btn:hover {
        background-color: #2c3238;
    }
    .github-btn svg {
        margin-right: 8px;
        fill: white;
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
    
    <a href="https://play.google.com/store/apps/details?id=com.ja.redlii.cube">
        <img style="height: 60px; width: auto; margin:3%; vertical-align: middle;" src="/assets/img/icons/GetItOnGooglePlay.png" alt="Get it on Google Play">
    </a>

    <a href="https://github.com/redlli/The-Cube" target="_blank" class="github-btn">
        <svg height="24" viewBox="0 0 16 16" width="24"><path d="M8 0C3.58 0 0 3.58 0 8c0 3.54 2.29 6.53 5.47 7.59.4.07.55-.17.55-.38 0-.19-.01-.82-.01-1.49-2.01.37-2.53-.49-2.69-.94-.09-.23-.48-.94-.82-1.13-.28-.15-.68-.52-.01-.53.63-.01 1.08.58 1.23.82.72 1.21 1.87.87 2.33.66.07-.52.28-.87.51-1.07-1.78-.2-3.64-.89-3.64-3.95 0-.87.31-1.59.82-2.15-.08-.2-.36-1.02.08-2.12 0 0 .67-.21 2.2.82.64-.18 1.32-.27 2-.27.68 0 1.36.09 2 .27 1.53-1.04 2.2-.82 2.2-.82.44 1.1.16 1.92.08 2.12.51.56.82 1.27.82 2.15 0 3.07-1.87 3.75-3.65 3.95.29.25.54.73.54 1.48 0 1.07-.01 1.93-.01 2.2 0 .21.15.46.55.38A8.013 8.013 0 0016 8c0-4.42-3.58-8-8-8z"></path></svg>
        View Code on GitHub
    </a>

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
