<template>
  <div class="projects-page">
    <transition name="home"></transition>
    <div class="projects wrapper">
      <div class="container">
        <h1 class="syne">My Projects <img src="/img/gradient-3.png" alt="" /></h1>
        <div class="projects-container">
          <NuxtLink class="project" to="/projects/halto">
            <img src="/thumbnails/halto.png" alt="" />
            <div class="dom">
              <p>UI Design - Web Development</p>
              <p>Client Project</p>
            </div>
            <div class="name">
              <p class="syne">Halto</p>
              <p>2022</p>
            </div>
          </NuxtLink>
          <NuxtLink to="/projects/newgo" class="project">
            <img src="/thumbnails/newgo.png" alt="" />
            <div class="dom">
              <p>Product Design</p>
              <p>Internship</p>
            </div>
            <div class="name">
              <p class="syne">Newgo</p>
              <p>2021-?</p>
            </div>
          </NuxtLink>
          <NuxtLink to="/projects/doritos" class="project">
            <img src="/thumbnails/doritos.png" alt="" />
            <div class="dom">
              <p>Artistic Direction</p>
              <p>Client Project</p>
            </div>
            <div class="name">
              <p class="syne">Doritos</p>
              <p>2022</p>
            </div>
          </NuxtLink>
          <NuxtLink to="/projects/meyze" class="project">
            <img src="/thumbnails/meyze.png" alt="" />
            <div class="dom">
              <p>UI/UX Design</p>
              <p>School Project</p>
            </div>
            <div class="name">
              <p class="syne">Meyze</p>
              <p>2022</p>
            </div>
          </NuxtLink>
          <!-- <NuxtLink to="/projects/forecast" class="project">
            <img src="/thumbnails/forecast.png" alt="" />
            <div class="dom">
              <p>UI/UX Design</p>
              <p>School Project</p>
            </div>
            <div class="name">
              <p class="syne">Forecast</p>
              <p>2021</p>
            </div>
          </NuxtLink>
          <NuxtLink to="/projects/horror" class="project">
            <img src="/thumbnails/horror.png" alt="" />
            <div class="dom">
              <p>UI Design</p>
              <p>School Project</p>
            </div>
            <div class="name">
              <p class="syne">Horror Vacui</p>
              <p>2021</p>
            </div>
          </NuxtLink> -->
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  head: {
    title: "Projects - salutcestleo",
  },
};
</script>

<style lang="scss">
.projects {
  padding-top: 150px;
  .container {
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
    .projects-container {
      padding-top: 100px;
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      grid-gap: 30px;
      .project {
        text-decoration: none;
        img {
          width: 100%;
        }
        p {
          font-size: 1.063rem;
          font-weight: 300;
        }
        .dom {
          display: flex;
          justify-content: space-between;
          border-bottom: solid 1px var(--blue);
          padding-bottom: 5px;
        }
        .name {
          padding-top: 5px;
          display: flex;
          justify-content: space-between;
          .syne {
            font-weight: 600;
            font-size: 1.563rem;
          }
        }
      }
    }
  }
}
</style>
