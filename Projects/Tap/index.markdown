---
title: Tap 
layout: def
permalink: tap
icon: https://play-lh.googleusercontent.com/5ofHorRsNG1TlWgC5oBJpBDOMnzPp1G1RGHXUwWuVUav_DyFkrhDQxau-sH9kfCPOH4=w240-h480
description: Simple tap game
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
        z-index: 1000;
    }
    .fullscreen img {
        max-width: 90%;
        max-height: 90%;
        border-radius: 10px;
    }

</style><style>
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
    <h1>tap</h1>
    <h2>Simple tap game with some awesome art work.</h2>

    <div class="images">
        <img src="https://play-lh.googleusercontent.com/zX4LTa63UeOtZISaXQveES4y5DKyKpnPjc3p-xV5wefz2y2hZ93BVjSMVyqfybWeFw=w2560-h1440" alt="Screenshot 1">
        <img src="https://play-lh.googleusercontent.com/-9SbAsxUTPT4VGbZymh6bbO1bAyVvjywaReOlGCI75faA_uZ-lNjiWm22Ynb_bxyQEk=w2560-h1440" alt="Screenshot 2">
        <img src="https://play-lh.googleusercontent.com/AkXcAZJbRVuZPm5MSHuxn3cegf51YlvA4Zyed2rgf9E8QwEc_HegVsGEsVWlVfM5cA=w2560-h1440" alt="Screenshot 3">
    </div>
    <a href="https://play.google.com/store/apps/details?id=com.japvtltd.tap&pcampaignid=web_share">
        <img style="height: 80px; width: auto; margin:3%;" src="/assets/img/icons/GetItOnGooglePlay.png"></a>

</div>
---
<h2><a class="linkhai" href="/tap/privacy-policy">Privacy Policy</a></h2>
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
