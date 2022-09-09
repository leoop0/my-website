<template>
  <nav class="wrapper">
    <div class="container">
      <div class="left">
        <NuxtLink class="logo" to="/">
          <img src="/img/Logo.svg" alt="Logo" />
          <span class="mgc_search_line"></span>
          <span class="syne">salutcestleo</span>
        </NuxtLink>
        <ul>
          <li>
            <NuxtLink to="/">Home</NuxtLink>
          </li>
          <li>
            <NuxtLink to="/projects">Projects</NuxtLink>
          </li>
          <li>
            <NuxtLink to="/about">About</NuxtLink>
          </li>
        </ul>
      </div>
      <div class="right">
        <ul>
          <li>
            <NuxtLink><img src="/icons/dribbble.svg" alt="Dribbble" /></NuxtLink>
          </li>
          <li>
            <NuxtLink><img src="/icons/linkedin.svg" alt="Linkedin" /></NuxtLink>
          </li>
          <li>
            <NuxtLink><img src="/icons/insta.svg" alt="Instagram" /></NuxtLink>
          </li>
          <li>
            <NuxtLink><img src="/icons/email.svg" alt="Email" /></NuxtLink>
          </li>
        </ul>
      </div>
    </div>
  </nav>
</template>

<style lang="scss">
nav {
  position: absolute;
  width: 100%;
  z-index: 200;
  .container {
    padding: 35px 0px;
    display: flex;
    justify-content: space-between;
    .left {
      display: flex;
      align-items: center;
      .logo {
        display: flex;
        align-items: center;
        text-decoration: none;
        margin-right: 25px;
        img {
          transition: all 0.3s;
          height: 20px;
          width: auto;
          margin-right: 5px;
        }
        span {
          color: var(--blue);
          font-size: 1.063rem;
          font-weight: 800;
        }
        &:hover {
          img {
            transform: rotate(25deg);
          }
        }
      }
      ul {
        display: flex;
        list-style: none;
        gap: 15px;
        li {
          font-weight: 500;
          font-size: 1.063rem;
          a {
            color: var(--blue);
            text-decoration: none;
          }
        }
      }
    }
    .right {
      ul {
        display: flex;
        list-style: none;
        gap: 13px;
        li {
          a {
            cursor: pointer;
            img {
              transition: all 0.3s;
            }
          }
          &:hover {
            a {
              img {
                transform: scale(1.1);
              }
            }
          }
        }
      }
    }
  }
}
</style>
