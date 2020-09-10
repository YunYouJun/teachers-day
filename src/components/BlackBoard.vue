<template>
  <svg
    id="scene"
    width="700"
    height="500"
    viewBox="0 0 700 500"
    xmlns="http://www.w3.org/2000/svg"
    style="background-color: #ffecb3; display: block; margin: auto"
  >
    <defs>
      <linearGradient id="blackboard-gradient" x1="0" x2="0" y1="0" y2="1">
        <stop offset="0%" stop-color="#444" />
        <stop offset="100%" stop-color="111" />
      </linearGradient>
      <rect id="chalk" width="40" height="6" fill="white" />
      <g id="book">
        <rect x="0" y="0" width="80" height="2" />
        <rect x="0" y="2" width="80" height="1" fill="#555" />
        <rect x="5" y="3" width="70" height="7" fill="white" />
        <rect x="0" y="10" width="80" height="1" fill="#555" />
        <rect x="0" y="11" width="80" height="2" />
      </g>
      <path id="leaf" d="M0 0 Q 50 -40 100 0 Q 50 40 0 0" fill="green" />
      <g id="plant-stem">
        <path
          d="M0 0 Q 0 -60 40 -90"
          stroke="#1a1a00"
          stroke-width="4"
          fill="transparent"
        />
        <use xlink:href="#leaf" x="38" y="-88" transform="rotate(-40 38 -88)" />
        <use
          xlink:href="#leaf"
          x="15"
          y="-74"
          transform="scale(0.7)rotate(-10 15 -74)"
        />
        <use
          xlink:href="#leaf"
          x="20"
          y="-90"
          transform="scale(0.7)rotate(-90 20 -90)"
        />
      </g>
      <g id="spitball">
        <ellipse
          cx="10"
          cy="10"
          rx="12"
          ry="20"
          fill="white"
          transform="rotate(-35 10 10)"
        />
        <ellipse
          cx="10"
          cy="10"
          rx="12"
          ry="20"
          fill="white"
          transform="rotate(25 10 10)"
        />
        <ellipse
          cx="14"
          cy="6"
          rx="16"
          ry="10"
          fill="white"
          transform="rotate(-10 14 6)"
        />
        <ellipse
          cx="6"
          cy="11"
          rx="16"
          ry="10"
          fill="white"
          transform="rotate(-35 6 11)"
        />
        <ellipse cx="17" cy="4" rx="8" ry="6" fill="#99ccff" />
        <ellipse
          cx="15"
          cy="2"
          rx="8"
          ry="6"
          fill="#99ccff"
          transform="rotate(-70 15 2)"
        />
        <ellipse cx="6" cy="20" rx="4" ry="4" fill="#99ccff" />
      </g>
    </defs>
    <rect id="floor" x="0" y="370" width="700" height="130" fill="#804000" />
    <g id="awning">
      <rect x="0" y="350" width="700" height="20" fill="white" />
      <rect
        x="0"
        y="350"
        width="700"
        height="5"
        fill="black"
        fill-opacity="0.3"
      />
    </g>
    <g id="blackboard">
      <rect x="75" y="35" width="550" height="280" fill="#996633" />
      <rect
        x="90"
        y="50"
        width="520"
        height="250"
        fill="url(#blackboard-gradient)"
      />
      <rect x="65" y="310" width="570" height="10" fill="#664400" />
      <rect x="65" y="320" width="570" height="5" fill="#4d3300" />
      <text
        x="350"
        y="130"
        class="chalk-words fadeIn"
        text-anchor="middle"
        fill="rgba(238, 238, 238, 0.7)"
      >
        {{ msg }}
      </text>
      <text
        x="350"
        y="210"
        class="chalk-words fadeIn delay"
        text-anchor="middle"
        fill="rgba(238, 238, 238, 0.7)"
      >
        {{ greeting }}
      </text>
    </g>
    <use xlink:href="#chalk" x="230" y="304" />
    <g id="duster">
      <rect x="285" y="308" width="45" height="2" fill="black" />
      <polygon points="282,303 333,303 330,308 285,308" fill="#444" />
      <polygon points="283,294 331,294 333,303 282,303" fill="#888" />
    </g>
    <g id="cup">
      <use xlink:href="#chalk" x="332" y="285" transform="rotate(80 352 282)" />
      <use xlink:href="#chalk" x="338" y="286" transform="rotate(88 358 283)" />
      <use xlink:href="#chalk" x="344" y="284" transform="rotate(92 364 281)" />
      <use xlink:href="#chalk" x="349" y="286" transform="rotate(97 369 283)" />
      <polygon points="340,275 370,275 365,310 345,310" fill="#aaa" />
    </g>
    <g id="front-desk">
      <rect x="330" y="330" width="330" height="15" fill="#4d3300" />
      <rect x="345" y="345" width="300" height="120" fill="#d6d6c2" />
      <rect x="330" y="345" width="15" height="140" fill="#c2c2a3" />
      <rect x="645" y="345" width="15" height="140" fill="#c2c2a3" />
      <polygon points="345,465 355,465 345,485" fill="#222" />
      <polygon points="635,465 645,465 645,485" fill="#222" />
    </g>
    <g id="books">
      <use xlink:href="#book" x="560" y="317" fill="red" />
      <use xlink:href="#book" x="567" y="304" fill="orange" />
      <use xlink:href="#book" x="563" y="291" fill="yellow" />
      <use xlink:href="#book" x="561" y="278" fill="orange" />
    </g>
    <g id="apple">
      <path
        d="M 506 308 Q 504 298 512 288"
        stroke="#333300"
        stroke-width="5"
        fill="transparent"
      />
      <ellipse
        cx="502"
        cy="314"
        rx="12"
        ry="16"
        fill="red"
        transform="rotate(-20 502 314)"
      />
      <ellipse
        cx="510"
        cy="314"
        rx="12"
        ry="16"
        fill="red"
        transform="rotate(20 510 314)"
      />
      <ellipse
        cx="497"
        cy="308"
        rx="3"
        ry="5"
        fill="white"
        fill-opacity="0.5"
      />
    </g>
    <g id="pot-plant">
      <use xlink:href="#plant-stem" x="85" y="350" />
      <use
        xlink:href="#plant-stem"
        x="100"
        y="400"
        transform="translate(145,100)scale(0.6)scale(-1,1)"
      />
      <polygon points="50,345 120,345 110,415 60,415" fill="#66ccff" />
      <rect x="45" y="335" width="80" height="10" fill="#66ccff" />
      <rect
        x="45"
        y="335"
        width="80"
        height="10"
        fill="black"
        fill-opacity="0.5"
      />
    </g>
    <g id="shooter">
      <rect x="325" y="380" width="30" height="140" fill="#99ffff" />
      <polygon points="315,390 325,380 325,520 315,520" fill="#ccffff" />
      <polygon points="355,380 365,390 365,520 355,520" fill="#ccffff" />
      <rect
        x="330"
        y="385"
        width="20"
        height="130"
        rx="335"
        ry="390"
        fill="white"
        fill-opacity="0.5"
      />
    </g>
  </svg>
</template>

<script>
export default {
  name: "BlackBoard",
  props: {
    msg: String,
  },
  data() {
    return {
      greeting: "教师节快乐",
    };
  },
};
</script>

<style scoped>
#scene {
  width: 100vw;
  height: 100vh;
  position: relative;
}

.chalk-words {
  font-family: "Permanent Marker", "Ma Shan Zheng", cursive;
  color: rgba(238, 238, 238, 0.7);
  text-align: center;
  width: 100%;
  z-index: 10;
  font-size: 2.5rem;
  opacity: 0;
}

.fadeIn {
  animation: fadeIn 2s;
  animation-fill-mode: forwards;
}

.delay {
  animation-delay: 1s;
}

@keyframes fadeIn {
  0% {
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}
</style>
