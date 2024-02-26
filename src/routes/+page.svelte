<script lang="ts">
  import Button from "../lib/components/button.svelte";
</script>

<div class="container">
  <div class="wrapper">
    <nav class="navbar">
      <div class="logo nav__item">
        <h3>ANIME</h3>
        <h3>GEN</h3>
      </div>
      <ul class="nav__link__container">
        <li class="nav__links">
          <a class="nav__link" href="/guideline">Guideline</a>
          <a class="nav__link" href="/faq">Faq</a>
          <a
            class="nav__link"
            href="https://github.com/Fantasy-programming/AnimeGen">Github</a
          >
          <a class="nav__link" href="https://twitter.com/ridyrich">Twitter</a>
        </li>
      </ul>
      <Button classList="nav__item">
        <a href="/generate"> Create Now </a>
      </Button>
    </nav>
    <section class="presentation">
      <div class="hero__1">
        <div class="title">
          <h1 class="title-1">Anime characters</h1>
          <h1 class="title-2">Generator</h1>
        </div>
      </div>
      <div class="presentation__bottom">
        <div class="image-wrapper-2">
          <div class="image_float-2">
            <div class="image-2" />
            <!-- <div class="image_toggle">create randomly</div> -->
          </div>
        </div>
        <div class="announce__card">
          <div class="announce__card__header">Images generated on device</div>
          <div class="announce__card__content">
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Sed non
            minus similique. Illum aliquam corporis aliquid veniam corrupti quam
            doloremque, quasi dolore reprehenderit iure laudantium iste
            dignissimos eveniet, ipsam facere.
          </div>
        </div>
      </div>
    </section>
    <footer></footer>
    <svg
      style="visibility: hidden; position: absolute;"
      width="0"
      height="0"
      xmlns="http://www.w3.org/2000/svg"
      version="1.1"
    >
      <defs>
        <filter id="round">
          <feGaussianBlur in="SourceGraphic" stdDeviation="5" result="blur" />
          <feColorMatrix
            in="blur"
            mode="matrix"
            values="1 0 0 0 0  0 1 0 0 0  0 0 1 0 0  0 0 0 19 -9"
            result="goo"
          />
          <feComposite in="SourceGraphic" in2="goo" operator="atop" />
        </filter>
      </defs>
    </svg>
  </div>
</div>

<style>
  .container {
    padding: 10px;
    background-color: rgba(24, 24, 24, 1);
  }
  .wrapper {
    width: 100%;
    height: 100%;
    padding: 0px 40px;
    background-color: rgb(var(--primary-color));
    border-radius: 10px;
  }

  .nav__link__container {
    color: rgb(var(--base-color));
    background-color: rgba(24, 24, 24, 1);
    align-self: flex-start;
    flex: 0 1 75%;
    clip-path: polygon(0 0, 100% 0, 86% 100%, 14% 100%);
    filter: url(#round);
  }

  .nav__links {
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 40px;
    padding: 16px 0px;
  }

  .navbar {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  .nav__item {
    margin-top: 20px;
  }

  .presentation {
    padding: 8vh 0;
  }

  .logo {
    font-weight: 600;
    color: rgba(24, 24, 24, 1);
    font-size: 1.2rem;
  }

  .title {
    color: rgba(24, 24, 24, 1);
    font-family: var(--font-secondary);
    font-weight: 500;
    text-transform: uppercase;
    line-height: 2.5ch;
    font-size: clamp(1.5rem, 4vw, 10vh);
  }

  .hero__1 {
    display: flex;
    justify-content: space-between;
    gap: 20px;
    margin-bottom: 50px;
  }

  .image-wrapper-2 {
    background: rgb(var(--base-color));
    position: relative;
    flex: 1 0 100%;
    max-width: 550px;
    min-height: 350px;
    clip-path: polygon(
      0 0,
      85% 0%,
      100% 14%,
      100% 100%,
      70% 100%,
      15% 100%,
      0 86%,
      0% 30%
    );
    filter: url(#round);
  }

  .image_float-2 {
    position: absolute;
    display: flex;
    width: 99%;
    height: 99%;
    top: 2.5px;
    left: 3px;
    clip-path: polygon(
      0 0,
      85% 0%,
      100% 14%,
      100% 100%,
      70% 100%,
      15% 100%,
      0 86%,
      0% 30%
    );
  }
  .image-2 {
    background: url("/images/pics2.png") center/cover no-repeat;
    width: 100%;
    height: 100%;
    border-radius: 10px 0 10px 0;
  }

  .presentation__bottom {
    display: flex;
    gap: 60px;
    justify-content: space-between;
  }

  .announce__card {
    align-self: flex-end;
    background: rgb(var(--primary-color));
  }

  .announce__card__header {
    position: relative;
    width: clamp(10%, 40%, 50%);
    padding: 15px 20px;
    border: solid 2px #000;
    border-bottom: 0;
    text-transform: uppercase;
    font-weight: 600;
    font-size: 1.2rem;
    border-radius: 10px 10px 0px 0px;
    background: rgb(var(--base-color));
  }
  .announce__card__header::after {
    content: "";
    width: 100%;
    height: 4px;
    bottom: -2px;
    left: 0;
    position: absolute;
    background: rgb(var(--base-color));
  }

  .announce__card__content {
    padding: 15px 20px 10px 20px;
    border: solid 2px #000;
    border-radius: 0px 10px 10px 10px;
    background: rgb(var(--base-color));
  }
</style>
