<template>
  <footer>


    <div class="f1">
      <h5>Popular Posts:</h5>
      <ul>
        <li>
          <a href="/posts/passkeys.html">Passkeys Vs Passwords</a>
        </li>
        <li>
          <a href="/posts/PhishingAttacks.html">Phishing Attacks</a>
        </li>
        <li>
          <a href="/posts/Ransomware.html">What is Ransomware?</a>
        </li>
        <li>
          <a href="/posts/MultiFactorAuthentication.html">Multi Factor Authentication</a>
        </li>
      </ul>
    </div>

    <div class="f2">
      <h5>Other Links:</h5>
      <ul>
        <li>
          <a href="https://github.com/tr1pwyr/wyr-world">Get this Code</a>
        </li>
        <li>
          <a href="https://twitter.com/tr1pwyr">Me on Twitter</a>
        </li>
        <li>
          <a href="https://wlog.app/">WLog.App</a>
        </li>
        <li>
          <a href="https://front-end.us">Front-end.us</a>
        </li>
      </ul>
    </div>

    <div class="f3">
      <img src="/tr1pwyr.webp" width="90" height="90" alt="tr1pwyr's WyrWorld Tech Blog" /> <br />
      Wyr.World v.{{ ver }} by
      <a href="https://github.com/tr1pwyr" target="_blank" title="Tr1pwyr">
        Tr1pwyr
      </a>Copyright &copy; {{ date }}
    </div>


  </footer>
</template>
<script lang="ts" setup>
const date = new Date().getFullYear();
import { ref } from 'vue';

// get this from the backend
const ver = ref("0.0.5");

// will fetch this from the backend

// const logVisit =  async () => {
//   const response = await fetch('https://api.tr1pwyr.com/log', {
//     method: 'POST',
//     headers: {
//       'Content-Type': 'application/json'
//     },
//     body: JSON.stringify({
//       "url": window.location.href,
//       "referrer": document.referrer,
//       "userAgent": navigator.userAgent,
//       "language": navigator.language,
//       "doNotTrack": navigator.doNotTrack,
//       "cookieEnabled": navigator.cookieEnabled,
//       "screenWidth": screen.width,
//       "screenHeight": screen.height,
//       "screenColorDepth": screen.colorDepth,
//       "screenPixelDepth": screen.pixelDepth,
//       "screenOrientation": screen.orientation.type,
//     })
//   });

//   const data = await response.json();
//   console.log(data);
// }

// logVisit();

const logVisit = {
  "url": window.location.href,
  "referrer": document.referrer,
  "userAgent": navigator.userAgent,
  "language": navigator.language,
  "doNotTrack": navigator.doNotTrack,
  "cookieEnabled": navigator.cookieEnabled,
  "screenWidth": screen.width,
  "screenHeight": screen.height,
  "screenColorDepth": screen.colorDepth,
  "screenPixelDepth": screen.pixelDepth,
  "screenOrientation": screen.orientation.type,
}

console.log(logVisit);

</script>

<style scoped>
footer {
  display: block;
  text-align: center;
  position: absolute;
  width: 100%;
  bottom: 50px;
  padding: 0;
}

a {
  color: var(--vp-c-brand);
  font-weight: bold;
}

a:hover {
  text-decoration: none;
  color: var(--vp-c-hover);
}


.f1 {
  /* background: rgb(0, 128, 0, .1); */
  padding: 0;
  margin: 0;
}

.f2 {
  /* background: rgb(255, 192, 203, .1); */
}

.f3 {
  /* background: rgb(0, 0, 255, .1); */
  display: flex;
  justify-content: center;
}

.f3 img {
  margin: 0 auto;
  display: block;
}

.f1,
.f2,
.f3 {
  -moz-box-sizing: border-box;
  box-sizing: border-box;
  display: inline-block;
  text-align: center;
  font-size: 12px;
  padding: 2%;
  min-width: 300px;
  width: 33%;
}


 .dark a:hover{
  color:#4ae994!important;
}

</style>
