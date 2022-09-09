<template>
  <div>
    <div class="about wrapper">
      <div class="container">
        <h1 class="syne">About Me <img src="/img/gradient-4.png" alt="" /></h1>
        <div class="bio">
          <div class="left">
            <p>
              Hello 👋, I'm a french student in 🎨 Graphic Design, specialized in UX/UI Design.
              <br />
              <br />
              I'm currently in my 1st year of Master Digital Design at the Ecole Supérieure du
              Digital of Bordeaux. In parallel, I'm working at Newgo, a SaaS in the e-sport & gaming
              ecosystem.
              <br />
              <br />
              I'm ⛰ mountains lover.
            </p>
          </div>
          <div class="right">
            <img src="/img/me.png" alt="" />
          </div>
        </div>
      </div>
    </div>
    <div class="exp wrapper">
      <div class="container">
        <h2 class="syne">Work Experience</h2>
        <div class="experiences">
          <div class="experience">
            <img src="/img/Logo.svg" alt="Logo" />
            <h4>UI Designer / Web dev · <span>Freelance</span></h4>
            <p>
              UI Designer / Web Dev · Freelance Realization of various websites, most often via
              Wordpress to facilitate the update. Creation of all kinds, posters, logos etc, but I
              prefer to focus on UI/UX Design.
            </p>
          </div>
          <div class="experience">
            <img src="/img/exp/newgo.png" alt="Newgo Logo" />
            <h4>
              Product Designer ·
              <a href="https://newgo.io/" target="_blank" rel="noreferrer">Newgo</a>
            </h4>
            <p>
              At Newgo, I am in charge of all the application design, UX & UI. I'm also a developer
              for the website. User testing, acceptance, accessibility etc. are part of my missions.
            </p>
          </div>
          <div class="experience">
            <img src="/img/exp/oplus.png" alt="Oplus Logo" />
            <h4>
              Web developer ·
              <a href="https://oplus-urbanistes.fr/" target="_blank" rel="noreferrer"
                >0+ Urbanistes</a
              >
            </h4>
            <p>
              My 2nd year internship. I had the opportunity to realize it in a cabinet of town
              planning, for which I had the opportunity to realize various sites for customers as
              Domofrance.
            </p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  head: {
    title: "About - salutcestleo",
  },
};
</script>

<style lang="scss">
.about {
  padding-top: 150px;
  .container {
    height: 100vh;
    h1 {
      position: relative;
      font-size: 4.063rem;
      width: fit-content;
      img {
        position: absolute;
        bottom: 0;
        left: 0;
        z-index: -1;
        width: 100%;
        height: 28px;
      }
    }
    h1,
    h2,
    p {
      color: var(--blue);
    }
    .bio {
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      .left {
        padding: 50px 0;
        width: 100%;
        display: flex;
        align-items: center;
        justify-content: center;
        p {
          width: 70%;
          font-size: 1.1rem;
          line-height: 157%;
        }
      }
      .right {
        width: 100%;
        display: flex;
        align-items: center;
        justify-content: center;
        img {
          width: 70%;
          border-radius: 0 80px 0 80px;
          margin-top: -50px;
        }
      }
    }
  }
}

.exp {
  h2 {
    color: var(--blue);
    font-size: 3.125rem;
    text-transform: uppercase;
    margin-bottom: 50px;
  }

  .experiences {
    width: 70%;
    margin-left: 7%;
    .experience {
      margin-bottom: 25px;
      h4 {
        color: var(--blue);
        span,
        a {
          font-weight: 400;
          color: var(--blue);
        }
        a {
          text-decoration: underline;
        }
      }
      p {
        color: var(--blue);
        line-height: 157%;
        margin-top: 10px;
      }
      img {
        height: 35px;
      }
    }
  }
}
</style>
