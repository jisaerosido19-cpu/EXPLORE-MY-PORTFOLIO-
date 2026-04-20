<div class="tutorial" data-video="https://www.youtube.com/embed/vecnvtvWmXk?autoplay=1">
<img src="https://img.youtube.com/vi/vecnvtvWmXk/hqdefault.jpg">
</div>

<div class="tutorial" data-video="https://www.youtube.com/embed/XKSNDxp-I14?autoplay=1">
<img src="https://img.youtube.com/vi/XKSNDxp-I14/hqdefault.jpg">
</div>

<div class="tutorial" data-video="https://www.youtube.com/embed/emWedfQiP1A?autoplay=1">
<img src="https://img.youtube.com/vi/emWedfQiP1A/hqdefault.jpg">
</div>

</div>
</section>

<!-- OUTPUTS -->
<section id="outputs">
<h2>Outputs</h2>
<div class="output-box">Canva Portfolio</div>
<div class="output-box">Figma Design</div>
</section>

<!-- CONTACT -->
<section id="contact">
<h2>Contact</h2>
<p>Email: jisaerosido@gmail.com</p>
</section>

<footer style="text-align:center;padding:20px;background:#222;color:#fff;">
© 2025 Portfolio
</footer>

<!-- MODAL -->
<div id="modal" class="modal">
<span class="close">&times;</span>
<img id="modalImg" style="display:none;">
<iframe id="modalVideo" style="display:none;" frameborder="0" allowfullscreen></iframe>
</div>

<script>
const modal=document.getElementById("modal");
const modalImg=document.getElementById("modalImg");
const modalVideo=document.getElementById("modalVideo");
const close=document.querySelector(".close");

/* IMAGE ZOOM */
document.querySelectorAll("figure img").forEach(img=>{
img.onclick=()=>{
modal.style.display="flex";
modalImg.style.display="block";
modalVideo.style.display="none";
modalImg.src=img.src;
}
});

/* VIDEO PLAY */
document.querySelectorAll(".tutorial").forEach(v=>{
v.onclick=()=>{
modal.style.display="flex";
modalImg.style.display="none";
modalVideo.style.display="block";
modalVideo.src=v.getAttribute("data-video");
}
});

/* CLOSE */
close.onclick=()=>{modal.style.display="none";modalVideo.src="";}
window.onclick=e=>{if(e.target==modal){modal.style.display="none";modalVideo.src="";}}
</script>
</body>
</html>


