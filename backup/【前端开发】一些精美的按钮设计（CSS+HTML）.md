【前端开发『搬运』】一些精美的按钮设计（CSS+HTML）

## 这里收集了一些精美的按钮设计
![img](https://enashpinal.pages.dev/blog/b5/img1.webp "img")
### CSS code
```css
.button {

	 margin: 0;

	 height: auto;

 	background: transparent;

	 padding: 0;

	 border: none;

	 cursor: pointer;

}



.button {

	 --border-right: 6px;

	 --text-stroke-color: rgba(255,255,255,0.6);

	 --animation-color: #37FF8B;

	 --fs-size: 2em;

	 letter-spacing: 3px;

	 text-decoration: none;

 	font-size: var(--fs-size);

	 font-family: "Arial";

	 position: relative;

	 text-transform: uppercase;

	 color: transparent;

	 -webkit-text-stroke: 1px var(--text-stroke-color);

}

.hover-text {

	 position: absolute;

	 box-sizing: border-box;

 	content: attr(data-text);

	 color: var(--animation-color);

	 width: 0%;

	 inset: 0;

	 border-right: var(--border-right) solid var(--animation-color);

	 overflow: hidden;

	 transition: 0.5s;

	 -webkit-text-stroke: 1px var(--animation-color);

}

.button:hover .hover-text {

	 width: 100%;

	 filter: drop-shadow(0 0 23px var(--animation-color))

} 
```
### HTML code

``` html
<button class="button" data-text="Awesome">

 	 <span class="actual-text"> TITLE </span>

 	 <span aria-hidden="true" class="hover-text"> TITLE </span>

</button> 
```

![img](https://enashpinal.pages.dev/blog/b5/img2.webp)
### CSS code
```CSS
.btn-donate {

	 --clr-font-main: hsla(0 0% 20% / 100);

	 --btn-bg-1: hsla(194 100% 69% / 1);

	 --btn-bg-2: hsla(217 100% 56% / 1);

	 --btn-bg-color: hsla(360 100% 100% / 1);

	 --radii: 0.5em;

	 cursor: pointer;

	 padding: 0.9em 1.4em;

	 min-width: 120px;

	 min-height: 44px;

	 font-size: var(--size, 1rem);

	 font-family: "Segoe UI", system-ui, sans-serif;

	 font-weight: 500;

	 transition: 0.8s;

	 background-size: 280% auto;

	 background-image: linear-gradient(325deg, var(--btn-bg-2) 0%, var(--btn-bg-1) 55%, var(--btn-bg-2) 90%);

	 border: none;

	 border-radius: var(--radii);

	 color: var(--btn-bg-color);

	 box-shadow: 0px 0px 20px rgba(71, 184, 255, 0.5), 0px 5px 5px -1px rgba(58, 125, 233, 0.25), inset 4px 4px 8px rgba(175, 230, 255, 0.5), inset -4px -4px 8px rgba(19, 95, 216, 0.35);

}

.btn-donate:hover {

	 background-position: right top;

}

.btn-donate:is(:focus, :focus-visible, :active) {

 	outline: none;

 	box-shadow: 0 0 0 3px var(--btn-bg-color), 0 0 0 6px var(--btn-bg-2);

}

@media (prefers-reduced-motion: reduce) {

 	.btn-donate {

 		 transition: linear;

	 }

} 
```

### HTML code
``` html
<button class="btn-donate">

 	 click me

</button>
```

![img](https://enashpinal.pages.dev/blog/b5/img3.webp "img")
### CSS code
```CSS
.animated-button {

	 position: relative;

 	display: flex;

	 align-items: center;

 	gap: 4px;

 	padding: 16px 36px;

 	border: 4px solid;

 	border-color: transparent;

 	font-size: 16px;

 	background-color: inherit;

 	border-radius: 100px;

 	font-weight: 600;

 	color: greenyellow;

	 box-shadow: 0 0 0 2px greenyellow;

	 cursor: pointer;

	 overflow: hidden;

	 transition: all 0.6s cubic-bezier(0.23, 1, 0.32, 1);

}

.animated-button svg {

	 position: absolute;

	 width: 24px;

	 fill: greenyellow;

	 z-index: 9;

	 transition: all 0.8s cubic-bezier(0.23, 1, 0.32, 1);

}

.animated-button .arr-1 {

 	right: 16px;

}

.animated-button .arr-2 {

	 left: -25%;

}



.animated-button .circle {

	 position: absolute;

	 top: 50%;

	 left: 50%;

	 transform: translate(-50%, -50%);

	 width: 20px;

	 height: 20px;

	 background-color: greenyellow;

	 border-radius: 50%;

	 opacity: 0;

	 transition: all 0.8s cubic-bezier(0.23, 1, 0.32, 1);

}

.animated-button .text {

	 position: relative;

	 z-index: 1;

	 transform: translateX(-12px);

	 transition: all 0.8s cubic-bezier(0.23, 1, 0.32, 1);

}

.animated-button:hover {

	 box-shadow: 0 0 0 12px transparent;

	 color: #212121;

	 border-radius: 12px;

}

.animated-button:hover .arr-1 {

	 right: -25%;

}

.animated-button:hover .arr-2 {

	 left: 16px;

}

.animated-button:hover .text {

 	transform: translateX(12px);

}

.animated-button:hover svg {

	 fill: #212121;

}

.animated-button:active {

	 scale: 0.95;

	 box-shadow: 0 0 0 4px greenyellow;

}

.animated-button:hover .circle {

	 width: 220px;

	 height: 220px;

 	opacity: 1;

} 
```

### HTML code
``` HTML
<button class="animated-button">

 		<svg viewBox="0 0 24 24" class="arr-2" xmlns="http://www.w3.org/2000/svg">

	  	<path

 		  d="M16.1716 10.9999L10.8076 5.63589L12.2218 4.22168L20 11.9999L12.2218 19.778L10.8076 18.3638L16.1716 12.9999H4V10.9999H16.1716Z"

  		></path>

 	</svg>

 	<span class="text">Modern Button</span>

 	<span class="circle"></span>

		 <svg viewBox="0 0 24 24" class="arr-1" xmlns="http://www.w3.org/2000/svg">

		  <path

 		  d="M16.1716 10.9999L10.8076 5.63589L12.2218 4.22168L20 11.9999L12.2218 19.778L10.8076 18.3638L16.1716 12.9999H4V10.9999H16.1716Z"

		  ></path>

 	</svg>

</button>
```

![img](https://enashpinal.pages.dev/blog/b5/img4.webp "img")
### CSS code
```css
.sparkle-button {

 --active: 0;

 --bg: radial-gradient(

			40% 50% at center 100%,

			hsl(270 calc(var(--active) * 97%) 72% / var(--active)),

			transparent

		),

		radial-gradient(

			80% 100% at center 120%,

			hsl(260 calc(var(--active) * 97%) 70% / var(--active)),

			transparent

		),

		hsl(260 calc(var(--active) * 97%) calc((var(--active) * 44%) + 12%));

 background: var(--bg);

 font-size: 1.2rem;

 font-weight: 500;

 border: 0;

 cursor: pointer;

 padding: 1em 1em;

 display: flex;

 align-items: center;

 gap: 0.25em;

 white-space: nowrap;

 border-radius: 100px;

 position: relative;

 box-shadow: 0 0 calc(var(--active) * 3em) calc(var(--active) * 1em) hsl(260 97% 61% / 0.75),

		0 0em 0 0 hsl(260 calc(var(--active) * 97%) calc((var(--active) * 50%) + 30%)) inset,

		0 -0.05em 0 0 hsl(260 calc(var(--active) * 97%) calc(var(--active) * 60%)) inset;

 transition: box-shadow var(--transition), scale var(--transition), background var(--transition);

 scale: calc(1 + (var(--active) * 0.1));

 transition: .3s;

}



.sparkle-button:active {

 scale: 1;

 transition: .3s;

}



.sparkle path {

 color: hsl(0 0% calc((var(--active, 0) * 70%) + var(--base)));

 transform-box: fill-box;

 transform-origin: center;

 fill: currentColor;

 stroke: currentColor;

 animation-delay: calc((var(--transition) * 1.5) + (var(--delay) * 1s));

 animation-duration: 0.6s;

 transition: color var(--transition);

}



.sparkle-button:is(:hover, :focus-visible) path {

 animation-name: bounce;

}



@keyframes bounce {

 35%, 65% {

  scale: var(--scale);

 }

}



.sparkle path:nth-of-type(1) {

 --scale: 0.5;

 --delay: 0.1;

 --base: 40%;

}



.sparkle path:nth-of-type(2) {

 --scale: 1.5;

 --delay: 0.2;

 --base: 20%;

}



.sparkle path:nth-of-type(3) {

 --scale: 2.5;

 --delay: 0.35;

 --base: 30%;

}



.sparkle-button:before {

 content: "";

 position: absolute;

 inset: -0.2em;

 z-index: -1;

 border: 0.25em solid hsl(260 97% 50% / 0.5);

 border-radius: 100px;

 opacity: var(--active, 0);

 transition: opacity var(--transition);

}



.spark {

 position: absolute;

 inset: 0;

 border-radius: 100px;

 rotate: 0deg;

 overflow: hidden;

 mask: linear-gradient(white, transparent 50%);

 animation: flip calc(var(--spark) * 2) infinite steps(2, end);

}



@keyframes flip {

 to {

  rotate: 360deg;

 }

}



.spark:before {

 content: "";

 position: absolute;

 width: 200%;

 aspect-ratio: 1;

 top: 0%;

 left: 50%;

 z-index: -1;

 translate: -50% -15%;

 rotate: 0;

 transform: rotate(-90deg);

 opacity: calc((var(--active)) + 0.4);

 background: conic-gradient(

		from 0deg,

		transparent 0 340deg,

		white 360deg

	);

 transition: opacity var(--transition);

 animation: rotate var(--spark) linear infinite both;

}



.spark:after {

 content: "";

 position: absolute;

 inset: var(--cut);

 border-radius: 100px;

}



.backdrop {

 position: absolute;

 inset: var(--cut);

 background: var(--bg);

 border-radius: 100px;

 transition: background var(--transition);

}



@keyframes rotate {

 to {

  transform: rotate(90deg);

 }

}



@supports(selector(:has(:is(+ *)))) {

 body:has(button:is(:hover, :focus-visible)) {

  --active: 1;

  --play-state: running;

 }



 .bodydrop {

  display: none;

 }

}



.sparkle-button:is(:hover, :focus-visible) ~ :is(.bodydrop, .particle-pen) {

 --active: 1;

 --play-state: runnin;

}



.sparkle-button:is(:hover, :focus-visible) {

 --active: 1;

 --play-state: running;

}



.sp {

 position: relative;

}



.particle-pen {

 position: absolute;

 width: 200%;

 aspect-ratio: 1;

 top: 50%;

 left: 50%;

 translate: -50% -50%;

 -webkit-mask: radial-gradient(white, transparent 65%);

 z-index: -1;

 opacity: var(--active, 0);

 transition: opacity var(--transition);

}



.particle {

 fill: white;

 width: calc(var(--size, 0.25) * 1rem);

 aspect-ratio: 1;

 position: absolute;

 top: calc(var(--y) * 1%);

 left: calc(var(--x) * 1%);

 opacity: var(--alpha, 1);

 animation: float-out calc(var(--duration, 1) * 1s) calc(var(--delay) * -1s) infinite linear;

 transform-origin: var(--origin-x, 1000%) var(--origin-y, 1000%);

 z-index: -1;

 animation-play-state: var(--play-state, paused);

}



.particle path {

 fill: hsl(0 0% 90%);

 stroke: none;

}



.particle:nth-of-type(even) {

 animation-direction: reverse;

}



@keyframes float-out {

 to {

  rotate: 360deg;

 }

}



.text {

 translate: 2% -6%;

 letter-spacing: 0.01ch;

 background: linear-gradient(90deg, hsl(0 0% calc((var(--active) * 100%) + 65%)), hsl(0 0% calc((var(--active) * 100%) + 26%)));

 -webkit-background-clip: text;

 color: transparent;

 transition: background var(--transition);

}



.sparkle-button svg {

 inline-size: 1.25em;

 translate: -25% -5%;

}
```

### HTML code
``` html
<div class="sp">
  <button class="sparkle-button">
    <span class="spark"></span>
    <span class="backdrop"></span>
    <svg class="sparkle" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
      <path d="M14.187 8.096L15 5.25L15.813 8.096C16.0231 8.83114 16.4171 9.50062 16.9577 10.0413C17.4984 10.5819 18.1679 10.9759 18.903 11.186L21.75 12L18.904 12.813C18.1689 13.0231 17.4994 13.4171 16.9587 13.9577C16.4181 14.4984 16.0241 15.1679 15.814 15.903L15 18.75L14.187 15.904C13.9769 15.1689 13.5829 14.4994 13.0423 13.9587C12.5016 13.4181 11.8321 13.0241 11.097 12.814L8.25 12L11.096 11.187C11.8311 10.9769 12.5006 10.5829 13.0413 10.0423C13.5819 9.50162 13.9759 8.83214 14.186 8.097L14.187 8.096Z" fill="black" stroke="black" stroke-linecap="round" stroke-linejoin="round"></path>
      <path d="M6 14.25L5.741 15.285C5.59267 15.8785 5.28579 16.4206 4.85319 16.8532C4.42059 17.2858 3.87853 17.5927 3.285 17.741L2.25 18L3.285 18.259C3.87853 18.4073 4.42059 18.7142 4.85319 19.1468C5.28579 19.5794 5.59267 20.1215 5.741 20.715L6 21.75L6.259 20.715C6.40725 20.1216 6.71398 19.5796 7.14639 19.147C7.5788 18.7144 8.12065 18.4075 8.714 18.259L9.75 18L8.714 17.741C8.12065 17.5925 7.5788 17.2856 7.14639 16.853C6.71398 16.4204 6.40725 15.8784 6.259 15.285L6 14.25Z" fill="black" stroke="black" stroke-linecap="round" stroke-linejoin="round"></path>
      <path d="M6.5 4L6.303 4.5915C6.24777 4.75718 6.15472 4.90774 6.03123 5.03123C5.90774 5.15472 5.75718 5.24777 5.5915 5.303L5 5.5L5.5915 5.697C5.75718 5.75223 5.90774 5.84528 6.03123 5.96877C6.15472 6.09226 6.24777 6.24282 6.303 6.4085L6.5 7L6.697 6.4085C6.75223 6.24282 6.84528 6.09226 6.96877 5.96877C7.09226 5.84528 7.24282 5.75223 7.4085 5.697L8 5.5L7.4085 5.303C7.24282 5.24777 7.09226 5.15472 6.96877 5.03123C6.84528 4.90774 6.75223 4.75718 6.697 4.5915L6.5 4Z" fill="black" stroke="black" stroke-linecap="round" stroke-linejoin="round"></path>
    </svg>
    <span class="text">Generate Site</span>
  </button>
  <div class="bodydrop"></div>
  <span aria-hidden="true" class="particle-pen">
    <svg class="particle" viewBox="0 0 15 15" fill="none" xmlns="http://www.w3.org/2000/svg">
      <path d="M6.937 3.846L7.75 1L8.563 3.846C8.77313 4.58114 9.1671 5.25062 9.70774 5.79126C10.2484 6.3319 10.9179 6.72587 11.653 6.936L14.5 7.75L11.654 8.563C10.9189 8.77313 10.2494 9.1671 9.70874 9.70774C9.1681 10.2484 8.77413 10.9179 8.564 11.653L7.75 14.5L6.937 11.654C6.72687 10.9189 6.3329 10.2494 5.79226 9.70874C5.25162 9.1681 4.58214 8.77413 3.847 8.564L1 7.75L3.846 6.937C4.58114 6.72687 5.25062 6.3329 5.79126 5.79226C6.3319 5.25162 6.72587 4.58214 6.936 3.847L6.937 3.846Z" fill="black" stroke="black" stroke-linecap="round" stroke-linejoin="round"></path>
    </svg>
    <svg class="particle" viewBox="0 0 15 15" fill="none" xmlns="http://www.w3.org/2000/svg">
      <path d="M6.937 3.846L7.75 1L8.563 3.846C8.77313 4.58114 9.1671 5.25062 9.70774 5.79126C10.2484 6.3319 10.9179 6.72587 11.653 6.936L14.5 7.75L11.654 8.563C10.9189 8.77313 10.2494 9.1671 9.70874 9.70774C9.1681 10.2484 8.77413 10.9179 8.564 11.653L7.75 14.5L6.937 11.654C6.72687 10.9189 6.3329 10.2494 5.79226 9.70874C5.25162 9.1681 4.58214 8.77413 3.847 8.564L1 7.75L3.846 6.937C4.58114 6.72687 5.25062 6.3329 5.79126 5.79226C6.3319 5.25162 6.72587 4.58214 6.936 3.847L6.937 3.846Z" fill="black" stroke="black" stroke-linecap="round" stroke-linejoin="round"></path>
    </svg>
    <!-- More SVGs here -->
  </span>
</div>
```

![img](https://enashpinal.pages.dev/blog/b5/img5.webp "img")
### CSS code
``` css
.button {

 position: relative;

 width: 120px;

 height: 40px;

 background-color: #000;

 display: flex;

 align-items: center;

 color: white;

 flex-direction: column;

 justify-content: center;

 border: none;

 padding: 12px;

 gap: 12px;

 border-radius: 8px;

 cursor: pointer;

}



.button::before {

 content: '';

 position: absolute;

 inset: 0;

 left: -4px;

 top: -1px;

 margin: auto;

 width: 128px;

 height: 48px;

 border-radius: 10px;

 background: linear-gradient(-45deg, #e81cff 0%, #40c9ff 100% );

 z-index: -10;

 pointer-events: none;

 transition: all 0.6s cubic-bezier(0.175, 0.885, 0.32, 1.275);

}



.button::after {

 content: "";

 z-index: -1;

 position: absolute;

 inset: 0;

 background: linear-gradient(-45deg, #fc00ff 0%, #00dbde 100% );

 transform: translate3d(0, 0, 0) scale(0.95);

 filter: blur(20px);

}



.button:hover::after {

 filter: blur(30px);

}



.button:hover::before {

 transform: rotate(-180deg);

}



.button:active::before {

 scale: 0.7;

}
```

### HTML code
```html
<button class="button">
 Click me
</button>
```

![img](https://enashpinal.pages.dev/blog/b5/img6.webp "img")
### CSS code
```css
.btn {

 display: flex;

 justify-content: center;

 align-items: center;

 width: 13rem;

 overflow: hidden;

 height: 3rem;

 background-size: 300% 300%;

 backdrop-filter: blur(1rem);

 border-radius: 5rem;

 transition: 0.5s;

 animation: gradient_301 5s ease infinite;

 border: double 4px transparent;

 background-image: linear-gradient(#212121, #212121), linear-gradient(137.48deg, #ffdb3b 10%,#FE53BB 45%, #8F51EA 67%, #0044ff 87%);

 background-origin: border-box;

 background-clip: content-box, border-box;

}



#container-stars {

 position: absolute;

 z-index: -1;

 width: 100%;

 height: 100%;

 overflow: hidden;

 transition: 0.5s;

 backdrop-filter: blur(1rem);

 border-radius: 5rem;

}



strong {

 z-index: 2;

 font-family: 'Avalors Personal Use';

 font-size: 12px;

 letter-spacing: 5px;

 color: #FFFFFF;

 text-shadow: 0 0 4px white;

}



#glow {

 position: absolute;

 display: flex;

 width: 12rem;

}



.circle {

 width: 100%;

 height: 30px;

 filter: blur(2rem);

 animation: pulse_3011 4s infinite;

 z-index: -1;

}



.circle:nth-of-type(1) {

 background: rgba(254, 83, 186, 0.636);

}



.circle:nth-of-type(2) {

 background: rgba(142, 81, 234, 0.704);

}



.btn:hover #container-stars {

 z-index: 1;

 background-color: #212121;

}



.btn:hover {

 transform: scale(1.1)

}



.btn:active {

 border: double 4px #FE53BB;

 background-origin: border-box;

 background-clip: content-box, border-box;

 animation: none;

}



.btn:active .circle {

 background: #FE53BB;

}



#stars {

 position: relative;

 background: transparent;

 width: 200rem;

 height: 200rem;

}



#stars::after {

 content: "";

 position: absolute;

 top: -10rem;

 left: -100rem;

 width: 100%;

 height: 100%;

 animation: animStarRotate 90s linear infinite;

}



#stars::after {

 background-image: radial-gradient(#ffffff 1px, transparent 1%);

 background-size: 50px 50px;

}



#stars::before {

 content: "";

 position: absolute;

 top: 0;

 left: -50%;

 width: 170%;

 height: 500%;

 animation: animStar 60s linear infinite;

}



#stars::before {

 background-image: radial-gradient(#ffffff 1px, transparent 1%);

 background-size: 50px 50px;

 opacity: 0.5;

}



@keyframes animStar {

 from {

  transform: translateY(0);

 }



 to {

  transform: translateY(-135rem);

 }

}



@keyframes animStarRotate {

 from {

  transform: rotate(360deg);

 }



 to {

  transform: rotate(0);

 }

}



@keyframes gradient_301 {

 0% {

  background-position: 0% 50%;

 }



 50% {

  background-position: 100% 50%;

 }



 100% {

  background-position: 0% 50%;

 }

}



@keyframes pulse_3011 {

 0% {

  transform: scale(0.75);

  box-shadow: 0 0 0 0 rgba(0, 0, 0, 0.7);

 }



 70% {

  transform: scale(1);

  box-shadow: 0 0 0 10px rgba(0, 0, 0, 0);

 }



 100% {

  transform: scale(0.75);

  box-shadow: 0 0 0 0 rgba(0, 0, 0, 0);

 }

}
```
### HTML code
```html
<button class="btn" type="button">
  <strong>CLICK ME</strong>
  <div id="container-stars">
    <div id="stars"></div>
  </div>
  <div id="glow">
    <div class="circle"></div>
    <div class="circle"></div>
  </div>
</button>
```

![img](https://enashpinal.pages.dev/blog/b5/img7.webp "img")
### CSS code
```css
.Btn {

 display: flex;

 align-items: center;

 justify-content: flex-start;

 width: 45px;

 height: 45px;

 border: none;

 border-radius: 50%;

 cursor: pointer;

 position: relative;

 overflow: hidden;

 transition-duration: .3s;

 box-shadow: 2px 2px 10px rgba(0, 0, 0, 0.199);

 background-color: rgb(255, 65, 65);

}



.sign {

 width: 100%;

 transition-duration: .3s;

 display: flex;

 align-items: center;

 justify-content: center;

}



.sign svg {

 width: 17px;

}



.sign svg path {

 fill: white;

}

/* text */

.text {

 position: absolute;

 right: 0%;

 width: 0%;

 opacity: 0;

 color: white;

 font-size: 1.2em;

 font-weight: 600;

 transition-duration: .3s;

}

/* hover effect on button width */

.Btn:hover {

 width: 125px;

 border-radius: 40px;

 transition-duration: .3s;

}



.Btn:hover .sign {

 width: 30%;

 transition-duration: .3s;

 padding-left: 20px;

}

/* hover effect button's text */

.Btn:hover .text {

 opacity: 1;

 width: 70%;

 transition-duration: .3s;

 padding-right: 10px;

}

/* button click effect*/

.Btn:active {

 transform: translate(2px ,2px);
```

###HTML code
```html
<button class="Btn">
  <div class="sign"><svg viewBox="0 0 512 512"><path d="M377.9 105.9L500.7 228.7c7.2 7.2 11.3 17.1 11.3 27.3s-4.1 20.1-11.3 27.3L377.9 406.1c-6.4 6.4-15 9.9-24 9.9c-18.7 0-33.9-15.2-33.9-33.9l0-62.1-128 0c-17.7 0-32-14.3-32-32l0-64c0-17.7 14.3-32 32-32l128 0 0-62.1c0-18.7 15.2-33.9 33.9-33.9c9 0 17.6 3.6 24 9.9zM160 96L96 96c-17.7 0-32 14.3-32 32l0 256c0 17.7 14.3 32 32 32l64 0c17.7 0 32 14.3 32 32s-14.3 32-32 32l-64 0c-53 0-96-43-96-96L0 128C0 75 43 32 96 32l64 0c17.7 0 32 14.3 32 32s-14.3 32-32 32z"></path></svg></div>
  <div class="text">Click</div>
</button>
``` 

![img](https://enashpinal.pages.dev/blog/b5/img8.webp "img")
### CSS code
```css
.btn {

 font-size: 1.2rem;

 padding: 1rem 2.5rem;

 border: none;

 outline: none;

 border-radius: 0.4rem;

 cursor: pointer;

 text-transform: uppercase;

 background-color: rgb(14, 14, 26);

 color: rgb(234, 234, 234);

 font-weight: 700;

 transition: 0.6s;

 box-shadow: 0px 0px 60px #1f4c65;

 -webkit-box-reflect: below 10px linear-gradient(to bottom, rgba(0,0,0,0.0), rgba(0,0,0,0.4));

}



.btn:active {

 scale: 0.92;

}



.btn:hover {

 background: rgb(2,29,78);

 background: linear-gradient(270deg, rgba(2, 29, 78, 0.681) 0%, rgba(31, 215, 232, 0.873) 60%);

 color: rgb(4, 4, 38);

}
```

###HTML code
```html
<button class="btn">
  Click me
</button>
```

![img](https://enashpinal.pages.dev/blog/b5/img9.webp "img")
### CSS code
```css
.button {

 position: relative;

 font-size: 24px;

 font-weight: 600;

 padding: 15px 30px;

 color: #cfef00;

 background-color: transparent;

 border: 2px solid #cfef00;

 border-radius: 10px;

 cursor: pointer;

 transition: all 0.4s cubic-bezier(0.23, 1, 0.320, 1);

 overflow: hidden;

}



.button::before {

 content: '';

 position: absolute;

 width: 100%;

 height: 100%;

 background: #cfef00;

 top: 0%;

 left: -100%;

 scale: 1;

 border-radius: inherit;

 transition: all 0.6s cubic-bezier(0.23, 1, 0.320, 1);

}



.button span {

 transition: all 0.7s;

 position: relative;

 overflow: hidden;

}



.button span::before {

 position: absolute;

 content: 'CLICK';

 top: 0;

 left: 0;

 color: #212121;

 width: 0;

 overflow: hidden;

}



.button:hover span::before {

 width: 100%;

 transition: all 0.6s cubic-bezier(0.23, 1, 0.320, 1);

 transition-delay: 0.4s;

}



.button:hover::before {

 scale: 1;

 top: 0%;

 left: 0%;

}



.button:hover {

 border-color: transparent;

}



.button:active {

 scale: 0.9;

}
```

### HTML code
```html
<button class="button">
  <span>CLICK</span>
</button>
```

![img](https://enashpinal.pages.dev/blog/b5/img10.webp "img")
### CSS code
```css
.button {

 position: absolute;

 top: 50%;

 left: 50%;

 transform: translate(-50%, -50%)

}



.button a {

 display: block;

 height: 50px;

 width: 200px;

 background: #00b7ea;

 color: white;

 font: 17px/50px Helvetica, Verdana, sans-serif;

 text-decoration: none;

 text-align: center;

 text-transform: uppercase;

 -webkit-border-radius: 10px;

 -moz-border-radius: 10px;

 border-radius: 10px;

 -webkit-box-shadow: 2px 2px 8px rgba(0,0,0,0.2);

 -moz-box-shadow: 2px 2px 8px rgba(0,0,0,0.2);

 box-shadow: 2px 2px 8px rgba(0,0,0,0.2);

 background: -moz-linear-gradient(top, #00b7ea 0%, #009ec3 100%);

 background: -webkit-gradient(linear, left top, left bottom, color-stop(0%,#00b7ea), color-stop(100%,#009ec3));

 background: -webkit-linear-gradient(top, #00b7ea 0%,#009ec3 100%);

 background: -o-linear-gradient(top, #00b7ea 0%,#009ec3 100%);

 background: -ms-linear-gradient(top, #00b7ea 0%,#009ec3 100%);

 background: linear-gradient(top, #00b7ea 0%,#009ec3 100%);

 filter: progid:DXImageTransform.Microsoft.gradient( startColorstr='#00b7ea', endColorstr='#009ec3',GradientType=0 );

}



b {

 background: #222;

 display: block;

 height: 40px;

 width: 180px;

 margin: -50px 0 0 10px;

 text-align: center;

 font: 12px/45px Helvetica, Verdana, sans-serif;

 color: #fff;

 position: absolute;

 z-index: -1;

 -webkit-border-radius: 5px;

 -moz-border-radius: 5px;

 border-radius: 5px;

 -webkit-box-shadow: 2px 2px 8px rgba(0,0,0,0.2);

 -moz-box-shadow: 2px 2px 8px rgba(0,0,0,0.2);

 box-shadow: 2px 2px 8px rgba(0,0,0,0.2);

 -webkit-transition: all 0.5s ease;

 -moz-transition: all 0.5s ease;

 -o-transition: all 0.5s ease;

 -ms-transition: all 0.5s ease;

 transition: all 0.5s ease;

}



.button a, b {

 -webkit-border-radius: 10px;

 -moz-border-radius: 10px;

 border-radius: 10px;

 -webkit-box-shadow: 2px 2px 8px rgba(0,0,0,0.2);

 -moz-box-shadow: 2px 2px 8px rgba(0,0,0,0.2);

 box-shadow: 2px 2px 8px rgba(0,0,0,0.2);

}



.button:hover .top {

 margin: -80px 0 0 10px;

 line-height: 35px;

}



.button:hover .bottom {

 margin: -10px 0 0 10px;

}



.button a:active {

 background: #00b7ea;

 background: -moz-linear-gradient(top, #00b7ea 36%, #009ec3 100%);

 background: -webkit-gradient(linear, left top, left bottom, color-stop(36%,#00b7ea), color-stop(100%,#009ec3));

 background: -webkit-linear-gradient(top, #00b7ea 36%,#009ec3 100%);

 background: -o-linear-gradient(top, #00b7ea 36%,#009ec3 100%);

 background: -ms-linear-gradient(top, #00b7ea 36%,#009ec3 100%);

 background: linear-gradient(top, #00b7ea 36%,#009ec3 100%);

 filter: progid:DXImageTransform.Microsoft.gradient( startColorstr='#00b7ea', endColorstr='#009ec3',GradientType=0 );

}



.button:active .bottom {

 margin: -20px 0 0 10px;

}



.button:active .top {

 margin: -70px 0 0 10px;

}
```

### HTML code
```html
<div class="button">
  <a href="#">点击下载</a>
  <b class="top">点击下载</b>
  <b class="bottom">1.2MB .zip</b>
</div>
```

![img](https://enashpinal.pages.dev/blog/b5/img11.webp "img")
### CSS code
```css
.button {

 font-size: 1rem;

 background-color: #F2E1C1 !important;

 transform: translateY(-0.10em);

 box-shadow: 3px 3px 0px rgba(55, 22, 22, 0.67);

 border: 1px solid rgba(55, 22, 22, 0.67);

 border-radius: 50px;

 padding: 0.75em 1.5em;

 transition: 0.2s;

 cursor: pointer;

}



button:hover {

 box-shadow: 4px 6px 0px rgba(55, 22, 22, 0.67);

 transform: translateY(-0.4em);

}



button:active {

 box-shadow: none;

 transform: translateY(0);

}

```

### HTML code
```html
<button class="button">
 Button
</button>
```

## 感谢阅读！
_收集不易，转载请注明出处_