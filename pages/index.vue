<template>
  <div class="main-container">
    <div class="container">
      <div class="image-main-container">
        <div class="image-container">
          <!-- <img
            src="@/assets/img/hero-bg-2.jpg"
            width="400"
            alt="not found"
            class="image"
          /> -->
          <video id="bg-video" autoplay muted loop>
            <source src="@/assets/img/bg.mp4" type="video/mp4" />
            Your browser does not support HTML5 video.
          </video>
          <div class="video-overlay"></div>
        </div>
      </div>
      <div class="hero-content">
        <div class="content">
          <p class="text-one">Welcome to</p>
          <p class="text-two">O.P Jindal University</p>
          <p class="text-third">
            Central India's Biggest Technical And Cultural Fest
          </p>
          <p class="techno-title">Technorollix'23</p>

          <div class="reg-btn">
            <span>Register ></span>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'IndexPage',
}
</script>

<style lang="scss" scoped>
.main-container {
  .container {
    position: relative;

    .image-main-container {
      position: absolute;
      top: 0;
      left: 0;
      height: 100vh;
      width: 100vw;

      .image-container {
        height: 100vh;
        background: rgb(131, 58, 180);
        background: linear-gradient(
          90deg,
          rgba(131, 58, 180, 1) 0%,
          rgba(253, 29, 29, 1) 50%,
          rgba(252, 176, 69, 1) 100%
        );
        overflow-x: hidden;

        .video-overlay {
          position: absolute;
          top: 0;
          left: 0;
          height: 100vh;
          width: 100%;
          background: rgb(2, 0, 36);
          background: rgb(2, 0, 36);
          background: linear-gradient(
            209deg,
            rgba(2, 0, 36, 1) 0%,
            rgba(9, 9, 121, 0.5270483193277311) 35%,
            rgba(0, 212, 255, 1) 100%
          );

          opacity: 0.8;
        }

        #bg-video {
          width: 100%;
          height: 100%;
          object-fit: cover;
          // display: none;
        }
      }
    }

    .hero-content {
      position: absolute;
      top: 0;
      left: 0;
      height: 100vh;
      width: 100vw;
      display: flex;
      justify-content: center;
      align-items: center;

      .content {
        .text-one {
          font-family: 'Gruppo', cursive;
          font-size: 1.8rem;
          font-weight: bolder;
          letter-spacing: 0.1em;
          text-align: center;
          color: #fff;
        }

        .text-two {
          font-family: 'Source Sans Pro', sans-serif;
          font-size: 2rem;
          font-weight: bolder;
          letter-spacing: 0.2em;
          padding: 0.5rem 0;
          text-align: center;
          color: #fff;
        }

        .text-third {
          padding: 0 0 0.5rem 0;
          font-family: 'Poppins', sans-serif;
          font-size: 1.7rem;
          color: #ff9601;
          letter-spacing: 0.1rem;
        }

        .techno-title {
          position: relative;
          font-size: 5rem;
          font-family: 'Kaushan Script', cursive;
          color: #fff;
          text-align: center;
          letter-spacing: 0.1rem;

          // text-shadow: -0.1rem -0.1rem 0.5rem #fff, 0.1rem 0.1rem 0.5rem #fff;
        }

        .reg-btn {
          display: block;
          margin-top: 1.4rem;
          font-size: 1.7rem;
          position: relative;
          text-align: center;

          span {
            background: #fff;
            padding: 0.3rem 1rem;
            font-family: 'Caveat', cursive;
            border: 0.2px solid #fff;
            border-radius: 2px;
            cursor: pointer;
          }
        }
      }
    }
  }
}
</style>