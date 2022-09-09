<template>
  <div class="banner wrapper">
    <div class="container">
      <div class="left">
        <img src="/img/Logo.svg" alt="Logo" />
        <h1 class="syne">
          Leo Frati <br />
          <span class="syne"
            >Product Designer
            <img src="/img/gradient-1.png" alt="" />
          </span>
        </h1>
        <p>
          I’m a french design student in 🎨 Graphic Design, <br />
          specialized in UX/UI Design.
        </p>
        <div class="btns">
          <NuxtLink class="btn" to="/projects">My projects<i data-feather="circle"></i></NuxtLink>
          <a href="mailto=hello@salutcestleo.com" class="btn secondary" to=""
            >Get in touch<i data-feather="circle"></i
          ></a>
        </div>
      </div>
      <img class="right" src="/img/ghost.png" alt="" />
    </div>
  </div>
</template>

<style lang="scss">
.banner {
  height: 100vh;
  .container {
    align-items: center;
    display: grid;
    grid-template-columns: 1.5fr 1.2fr;
    .left {
      img {
        width: 120px;
        height: auto;
      }
      h1 {
        text-transform: uppercase;
        color: var(--blue);
        letter-spacing: 2%;
        font-size: 4.688rem;
        span {
          font-size: 3.75rem;
          position: relative;
          img {
            position: absolute;
            bottom: 0;
            left: 0;
            z-index: -1;
            width: 100%;
          }
        }
      }
      p {
        margin-top: 15px;
        color: var(--blue);
        font-size: 1.25rem;
        line-height: 157%;
      }
      .btns {
        margin-top: 35px;
        display: flex;
        .btn {
          &:first-child {
            margin-right: 15px;
          }
        }
      }
    }
    img.right {
      width: 100%;
      height: 700px;
      object-fit: cover;
      border-radius: 0px 0px 0px 80px;
    }
  }
}
</style>
