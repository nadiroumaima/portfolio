<template>
  <div class="container">
    <aside>
      <HeroAvatar>
        <img
          src="@/assets/img/profile.jpeg"
          alt="me"
          width="140"
          loading="lazy"
        />
      </HeroAvatar>
      <BinaryTextSVG />
    </aside>
    <main id="main-content">
      <article class="about-content">
        <h1 class="about-content__headline">About me</h1>
        <p>👋 Hey! How are you?</p>
        <p>
          I'm Oumaima. I'm a
          <strong>software engineer student</strong> dedicated to
          <em> crafting </em> things for the web through coding.
        </p>
        <p>
          I'm on my second year at ENSIAS (École Nationale Supérieure d'Informatique et d'Analyse des Systèmes)

        </p>
        <p>
        Always looking to learn new technologies to enrich my skills and improve my good practices as a developer.



          
        </p>
        <p>I'm into coding  and  i'm a bookwormie (of course) :P</p>
        <SocialMediaIcons boxed />
      </article>
    </main>
  </div>
</template>

<script setup>
import { useRoute } from 'vue-router'
import config from '../config/siteconfig.json'

const title = 'About me • NADIR Oumaima'
const { description } = config
const route = useRoute()

useHead({
  title,
  meta: [
    {
      name: 'description',
      content: description,
    },
    { property: 'og:type', content: 'website' },
    { property: 'og:title', content: title },
    { property: 'og:description', content: description },
    { property: 'og:url', content: `${config.siteUrl}${route.path}` },
    {
      property: 'twitter:title',
      content: title,
    },
    {
      property: 'twitter:description',
      content: description,
    },
  ],
})
</script>

<route lang="yaml">
meta:
  layout: default
</route>

<style lang="css" scoped>
.container {
  flex-flow: row wrap;
  padding: 3rem 0;
  gap: 2.4rem;
}

.about-content {
  & .about-content__headline {
    font-size: var(--text-2xl);
  }

  & p {
    font-size: var(--text-lg);
    opacity: 0.8;
    max-width: 71ch;
  }
}

.hero-avatar {
  opacity: 0;
  animation: tilt-in 900ms 1s cubic-bezier(0.250, 0.460, 0.450, 0.940) both;
}

@keyframes tilt-in {
  0% {
    transform: rotateY(20deg) rotateX(35deg) translate(300px, -300px) skew(-35deg, 10deg);
    opacity: 0;
  }
  100% {
    transform: rotateY(0) rotateX(0deg) translate(0, 0) skew(0deg, 0deg);
    opacity: 1;
  }
}

.binary-text-svg {
  font-family: var(--font-mono);
  font-size: var(--text-xl);
  position: absolute;
  left: 282px;
  top: 387px;
  opacity: 0.3;

  & :deep(tspan) {
    --text-delay: 500ms;

    opacity: 0;
    animation: pulse-spread 3s var(--text-delay) ease-out infinite alternate;

    &:nth-child(1) {
      --text-delay: 500ms;
    }

    &:nth-child(2) {
      --text-delay: 1s;
    }

    &:nth-child(3) {
      --text-delay: 1.5s;
    }

    &:nth-child(4) {
      --text-delay: 2s;
    }

    &:nth-child(5) {
      --text-delay: 2.5s;
    }

    &:nth-child(6) {
      --text-delay: 3s;
    }
  }
}

@keyframes pulse-spread {
  0% {
    opacity: 0;
  }

  100% {
    opacity: 0.3;
  }
}

@media screen and (min-width: 26.625em) and (max-width: 48em) {
  aside {
    margin-inline-start: 40px;
    padding: 0 2.4rem 0 0;
  }
}

@media (--vw-sm) {
  aside {
    padding: 0 1rem;
  }

  .container {
    height: 100%;
  }

  .binary-text-svg {
    top: 50%;
    left: 0;
    bottom: 0;
  }
}
</style>
