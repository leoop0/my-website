<template>
  <div class="project-page wrapper">
    <div class="container">
      <div class="title">
        <div class="text">
          <img src="/icons/arro.svg" alt="" />
          <h1 class="syne">Halto</h1>
        </div>
        <img src="/thumbnails/halto.png" class="thumbnail" alt="" />
      </div>
      <div class="content">
        <div class="desc">
          <p>
            The starting postulate: Create a 1v1 shooter entirely playable in a browser in 2 weeks.
          </p>
          <p>
            We were 15 people to realize this project, UI/UX Designer, Developers, Graphic
            designers, etc. and each one was able to bring his stone to the building.
          </p>
          <span>Project realized within the context of the Digital Event of the ESD Bordeaux.</span>
        </div>
        <div class="details">
          <div class="item">
            <h6>ROLE</h6>
            <p>Web developer</p>
          </div>
          <div class="item">
            <h6>CLIENT</h6>
            <a href="https://ecole-du-digital.com/campus/bordeaux/" target="_blank" rel="noreferrer"
              >ESD Bordeaux</a
            >
          </div>
          <div class="item">
            <h6>STACK</h6>
            <p>React, Firebase, Figma</p>
          </div>
        </div>
      </div>
      <div class="gallery">
        <img src="/projects/halto/1.png" alt="Halto's homescreen" />
        <img src="/projects/halto/2.png" alt="Halto's matchmaking" />
      </div>
      <a class="btn secondary" href="https://haltogame.com/" target="_blank" rel="noreferrer"
        >Click here to try the game</a
      >
    </div>
  </div>
</template>

<script>
export default {
  head: {
    title: "Halto - salutcestleo",
  },
};
</script>

<style lang="scss">
.project-page {
  .title {
    padding-top: 120px;
    display: grid;
    grid-template-columns: 1fr 2fr;
    align-items: flex-end;
    .text {
      h1 {
        color: var(--blue);
        font-size: 4.688rem;
        letter-spacing: 2%;
      }
      img {
        width: 45px;
      }
    }
    .thumbnail {
      object-fit: cover;
      width: 100%;
      height: 500px;
    }
  }

  .content {
    margin: 130px 0;
    display: grid;
    grid-template-columns: 1.5fr 1fr;
    grid-gap: 40px;
    .desc {
      p {
        font-size: 1.25rem;
        line-height: 157%;
        color: var(--blue);
        margin-bottom: 15px;
      }
      span {
        font-size: 1rem;
        opacity: 0.6;
        color: var(--blue);
        font-style: italic;
      }
    }
    .details {
      border: solid 1px var(--blue);
      padding: 20px;
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      .item {
        h6 {
          font-family: "Syne";
          font-size: 1rem;
          color: var(--blue);
          margin-bottom: 5px;
        }
        p,
        a {
          color: var(--blue);
        }
      }
    }
  }
  .gallery {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    grid-gap: 20px;
    img,
    iframe {
      width: 100%;
    }
    iframe {
      min-height: 400px;
      height: 100%;
    }
  }

  .btn {
    margin: 30px auto 10px auto;
  }
}
</style>
