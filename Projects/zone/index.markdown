---
title: ZONE 
layout: def
permalink: zone
icon: https://play-lh.googleusercontent.com/5ODAnjAehOyiFoGQHW42R-HLYh7yxEz3OwzkW-rGhKkHDKtOlRvvshOYIYIHx85QMu0=w240-h480
description: Lets get into the ZONE  
keywords: ZONE app, productivity, focus timer, to-do list, study sessions, App to focus, app for better study, fix attntion span, let you focus more
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
</style>

<div class="container">
    <h1>ZONE</h1>
    <h2>Stay Focused, Get Productive</h2>

    <div class="features">
        <h2>Key Features:</h2>
        <div class="feature-item">1) Track your productivity effortlessly.</div>
        <div class="feature-item">2) Receive weekly statistics and insights.</div>
        <div class="feature-item">3) Keep your to-do list organized and in check.</div>
        <div class="feature-item">4) Smart Focus Timer: Start with 25-minute study sessions, increasing automatically based on usage.</div>
    </div>

    <div class="images">
        <img src="https://play-lh.googleusercontent.com/vGR7aCmwxPmMJ7kDfAzfjwNLguB4U49RPPy2_11qdZNZhKdnqX4YSpW_cmdjzhOMnkM=w2560-h1440" alt="Screenshot 1">
        <img src="https://play-lh.googleusercontent.com/kmv3FoBb1ku2Fgt1jivlBmkjH7W_ISf1dGUS6ZreCzvl7KKEEVbfiYSPxz-u64RXCLzN=w2560-h1440" alt="Screenshot 2">
        <img src="https://play-lh.googleusercontent.com/kdzKNvOJhUQ3AKQ7rsTuH3JiYy8_4brQeCuVHR8fZ4uhH7QSq5NzwAUeSxSt-9GGsAI=w2560-h1440" alt="Screenshot 3">
        <img src="https://play-lh.googleusercontent.com/XraDPVtywQbgyFk5H0nC3cdjd62c41p2RKq91Tr2NrebO_TtwU8G6T88253yPWHfSN8=w2560-h1440" alt="Screenshot 4">
    </div>
    <a href="https://play.google.com/store/apps/details?id=com.jallc.zone">
        <img style="height: 80px; width: auto; margin:3%;" src="/assets/img/icons/GetItOnGooglePlay.png"></a>

</div>
---
<h2><a class="linkhai" href="/zone/privacy-policy">Privacy Policy</a></h2>
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
        prevArrow.innerHTML = "&#9664;";
        prevArrow.onclick = function() { changeImage(-1); };

        let nextArrow = document.createElement("div");
        nextArrow.className = "nav-arrow next";
        nextArrow.innerHTML = "&#9654;";
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
