<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <link rel="icon" href="logo.png" type="image/png" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Timesheet Management Application</title>
    <style>
      /*=============== GOOGLE FONTS ===============*/
      @import url("https://fonts.googleapis.com/css2?family=Montserrat:wght@400;600&display=swap");

      /*=============== VARIABLES CSS ===============*/
      :root {
        /*========== Colors ==========*/
        /*Color mode HSL(hue, saturation, lightness)*/
        --body-color: #393937;
        --accent-color: #03e9f4;
        --white-color: #fff;
        --box-shadow: 0 0 5px #03e9f4, 0 0 25px #03e9f4, 0 0 50px #03e9f4,
          0 0 100px #03e9f4;

        /*========== Font and typography ==========*/
        /*.5rem = 8px | 1rem = 16px ...*/
        --body-font: "Montserrat", sans-serif;
        --normal-font-size: 1rem;

        /*========== Font weight ==========*/
        --font-regular: 400;
        --font-semi-bold: 600;

        /*========== z index ==========*/
        --z-tooltip: 10;
        --z-fixed: 100;
      }

      /*=============== BASE ===============*/
      * {
        box-sizing: border-box;
        padding: 0;
        margin: 0;
      }

      body {
        font-family: var(--body-font);
        font-size: var(--normal-font-size);
        background: #000;
        min-height: 120vh;
        display: flex;
        justify-content: center;
        align-items: center;
      }

      ul {
        list-style: none;
      }

      a {
        text-decoration: none;
      }

      .button-animation {
        position: relative;
        display: inline-block;
        padding: 20px 30px;
        color: var(--accent-color);
        text-transform: uppercase;
        overflow: hidden;
        letter-spacing: 4px;
        transition: 0.5s;
      }

      .button-animation span {
        position: absolute;
        display: block;
      }

      .button-animation span:nth-child(1) {
        top: 0;
        left: -100%;
        width: 100%;
        height: 2px;
        background: linear-gradient(90deg, transparent, var(--accent-color));
        animation: btn-anim1 1s linear infinite;
      }

      @keyframes btn-anim1 {
        0% {
          left: -100%;
        }
        50%,
        100% {
          left: 100%;
        }
      }

      .button-animation span:nth-child(2) {
        top: -100%;
        right: 0;
        width: 2px;
        height: 100%;
        background: linear-gradient(180deg, transparent, var(--accent-color));
        animation: btn-anim2 1s linear infinite;
        animation-delay: 0.25s;
      }

      @keyframes btn-anim2 {
        0% {
          top: -100%;
        }
        50%,
        100% {
          top: 100%;
        }
      }

      .button-animation span:nth-child(3) {
        bottom: 0;
        right: -100%;
        width: 100%;
        height: 2px;
        background: linear-gradient(270deg, transparent, var(--accent-color));
        animation: btn-anim3 1s linear infinite;
        animation-delay: 0.5s;
      }

      @keyframes btn-anim3 {
        0% {
          right: -100%;
        }
        50%,
        100% {
          right: 100%;
        }
      }

      .button-animation span:nth-child(4) {
        bottom: -100%;
        left: 0;
        width: 2px;
        height: 100%;
        background: linear-gradient(360deg, transparent, var(--accent-color));
        animation: btn-anim4 1s linear infinite;
        animation-delay: 0.75s;
      }

      @keyframes btn-anim4 {
        0% {
          bottom: -100%;
        }
        50%,
        100% {
          bottom: 100%;
        }
      }

      .button-animation:hover {
        background-color: var(--accent-color);
        color: var(--white-color);
        border-radius: 5px;
        box-shadow: var(--box-shadow);
      }
      .page-text {
        text-align: center;
        color: var(--white-color);
        font-size: 1.5rem;
        margin-top: 10px;
        position: absolute;
        top: 150px;
        left: 50%;
        transform: translateX(-50%);

        /* Additional styles */
        background-color: var(--body-color); /* Background color */
        padding: 10px; /* Add some padding for better readability */
        border-radius: 5px; /* Rounded corners */
        box-shadow: 0 0 10px rgba(3, 233, 244, 0.5); /* Box shadow */
        color: #03e9f4; /* Change text color to #03e9f4 */
      }
    </style>
  </head>
  <body>
    <a
      class="box__link button-animation"
      href="https://drive.google.com/file/d/1dSjV0SLgc-BXZlFEGQqjRl5wag4Oxric/view?usp=sharing"
    >
      Download
      <span></span>
      <span></span>
      <span></span>
      <span></span>
    </a>
    <p class="page-text">
      Click Download To Install Timesheet Management Application
    </p>
  </body>
</html>
