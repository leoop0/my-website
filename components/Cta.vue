<template>
  <div>
    <div class="cta wrapper" id="contact">
      <div class="container">
        <h2 class="syne">
          An idea or <br />
          <span class="syne">a project ?<img src="/img/gradient-2.png" alt="" /></span>
        </h2>
        <div class="medias">
          <ul>
            <li>
              <a href="https://dribbble.com/Oeleo" target="_blank" rel="noreferrer"
                ><img src="/icons/dribbble.svg" alt="Dribbble" />dribbble.com.Oeleo</a
              >
            </li>
            <li>
              <a href="https://www.linkedin.com/in/leofrati/" target="_blank" rel="noreferrer"
                ><img src="/icons/linkedin.svg" alt="Linkedin" />linkedin.com.in/leofrati</a
              >
            </li>
            <li>
              <a href="https://www.instagram.com/salutcest.leo/" target="_blank" rel="noreferrer"
                ><img src="/icons/insta.svg" alt="Instagram" />@salutcest.leo</a
              >
            </li>
            <li>
              <a href="mailto:hello@salutcestleo.com" target="_blank" rel="noreferrer"
                ><img src="/icons/email.svg" alt="Email" />hello@salutcestleo.com</a
              >
            </li>
          </ul>
        </div>
      </div>
    </div>

    <footer class="wrapper">
      <div class="container">
        <p><span class="syne">salutcestleo</span> · Tous droits réservés</p>
        <img src="/img/Logo.svg" alt="Logo" />
      </div>
    </footer>
  </div>
</template>

<style lang="scss">
.cta {
  margin-top: 150px;
  .container {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    h2 {
      color: var(--blue);
      font-size: 4rem;
      span {
        position: relative;
        margin-left: 50px;
        img {
          position: absolute;
          bottom: 5%;
          left: 0;
          z-index: -1;
          width: 100%;
          height: 25px;
        }
      }
    }
    ul {
      list-style: none;
      li {
        font-size: 1.563rem;
        padding: 13px 10px;
        border-bottom: solid 1px var(--blue);
        &:first-child {
          border-top: solid 1px var(--blue);
        }
        a {
          display: flex;
          color: var(--blue);
          text-decoration: none;
          align-items: center;
          img {
            margin-right: 7px;
          }
        }
      }
    }
  }
}

footer {
  margin-top: 150px;
  .container {
    border-top: solid 1px var(--blue);
    padding: 10px 0;
    display: flex;
    justify-content: space-between;
    p {
      color: var(--blue);
      span {
        font-weight: 700;
      }
    }
    img {
      width: 20px;
    }
  }
}
</style>
