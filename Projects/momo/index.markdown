---
title: momo 
layout: def
permalink: momo
icon: https://play-lh.googleusercontent.com/vUxFBXPEK5ZGkru2Sal3SV91jguyZUwhw1f5kzL7gZHoa7VVe2gD5pjf25Alnpw5rw=w240-h480
description: Join the adventure of momo
keywords: momo game, fun to play, casual
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
    <h1>momo</h1>
    <h2>Join the adventure of momo where is gathres coins to buy a cat for his wife/girlfriend.</h2>

    <div class="images">
        <img src="https://play-lh.googleusercontent.com/A3xRgRtnZylBsviruFEx5Ic74cQez8fqan5oHO9ACkr_Sr_DTPIzrNeswa5YV6bLM-M=w2560-h1440" alt="Screenshot 1">
        <img src="https://play-lh.googleusercontent.com/E2d-9XkA71BOT1ZQSekdIAUPentJ1RMgaeewVcz2xfb_rmbyuEEonmj07iyy1sORE9s=w2560-h1440" alt="Screenshot 2">
        <img src="https://play-lh.googleusercontent.com/9_yV19lLgS50uJyuGqIfh4IE8Dk3Vqt9yr6S1i7B2HNa5ZhnyvF03cN8lUu4pa5DcqM=w2560-h1440" alt="Screenshot 3">
    </div>
    <div class="store-links" style="margin-top: 20px;">
        <a href="https://play.google.com/store/apps/details?id=com.jallc.momo">
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
<h2><a class="linkhai" href="/momo/privacy-policy">Privacy Policy</a></h2>
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
