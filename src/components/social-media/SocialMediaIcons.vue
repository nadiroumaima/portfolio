<template>
  <div :class="classes">
    <AppLink
      isExternal
      to="https://github.com/nadiroumaima"
      aria-label="My Github"
      title="My Github"
    >
      <svg
        width="41"
        height="41"
        viewBox="0 0 44 44"
        fill="none"
        xmlns="http://www.w3.org/2000/svg"
      >
        <path
          d="M21.9805 0.725586C9.90527 0.720703 0.125 10.4961 0.125 22.5615C0.125 32.1025 6.24316 40.2129 14.7637 43.1914C15.9111 43.4795 15.7354 42.6641 15.7354 42.1074V38.3232C9.10938 39.0996 8.84082 34.7148 8.39648 33.9824C7.49805 32.4492 5.37402 32.0586 6.00879 31.3262C7.51758 30.5498 9.05566 31.5215 10.8379 34.1533C12.127 36.0625 14.6416 35.7402 15.916 35.4229C16.1943 34.2754 16.79 33.25 17.6104 32.4541C10.7451 31.2236 7.88379 27.0342 7.88379 22.0537C7.88379 19.6367 8.67969 17.415 10.2422 15.623C9.24609 12.6689 10.335 10.1396 10.4814 9.76367C13.3184 9.50977 16.2676 11.7949 16.4971 11.9756C18.1084 11.541 19.9492 11.3115 22.0098 11.3115C24.0801 11.3115 25.9258 11.5508 27.5518 11.9902C28.1035 11.5703 30.8379 9.60742 33.4746 9.84668C33.6162 10.2227 34.6807 12.6934 33.7432 15.6084C35.3252 17.4053 36.1309 19.6465 36.1309 22.0684C36.1309 27.0586 33.25 31.2529 26.3652 32.4639C26.9549 33.0438 27.4232 33.7354 27.7426 34.4983C28.062 35.2612 28.2262 36.0801 28.2256 36.9072V42.4004C28.2646 42.8398 28.2256 43.2744 28.958 43.2744C37.6055 40.3594 43.8311 32.1904 43.8311 22.5664C43.8311 10.4961 34.0459 0.725586 21.9805 0.725586Z"
          fill="#F4F4F4"
        />
      </svg>
    </AppLink>
    <AppLink
      isExternal
      to="https://www.linkedin.com/in/oumaima-nadir-662896229/"
      aria-label="My LinkedIn Account"
      title="My LinkedIn"
    >
      <svg
        width="41"
        height="41"
        viewBox="0 0 41 41"
        fill="none"
        xmlns="http://www.w3.org/2000/svg"
      >
        <path
          d="M38.8281 0.578125H2.17188C1.29033 0.578125 0.578125 1.29033 0.578125 2.17188V38.8281C0.578125 39.7097 1.29033 40.4219 2.17188 40.4219H38.8281C39.7097 40.4219 40.4219 39.7097 40.4219 38.8281V2.17188C40.4219 1.29033 39.7097 0.578125 38.8281 0.578125ZM12.3968 34.53H6.48496V15.5146H12.3968V34.53ZM9.44336 12.9147C8.76565 12.9147 8.10316 12.7138 7.53966 12.3373C6.97617 11.9608 6.53698 11.4256 6.27763 10.7995C6.01828 10.1733 5.95042 9.48438 6.08264 8.81969C6.21485 8.15501 6.5412 7.54445 7.02041 7.06524C7.49963 6.58602 8.11018 6.25968 8.77487 6.12746C9.43956 5.99525 10.1285 6.0631 10.7546 6.32245C11.3808 6.5818 11.9159 7.02099 12.2924 7.58449C12.669 8.14798 12.8699 8.81047 12.8699 9.48818C12.8649 11.3808 11.331 12.9147 9.44336 12.9147ZM34.53 34.53H28.6231V25.2812C28.6231 23.0749 28.5833 20.241 25.5502 20.241C22.4772 20.241 22.0041 22.6416 22.0041 25.1219V34.53H16.1022V15.5146H21.77V18.1144H21.8497C22.6366 16.6202 24.5641 15.0414 27.4428 15.0414C33.4293 15.0414 34.53 18.981 34.53 24.1009V34.53Z"
          fill="#F4F4F4"
        />
      </svg>
    </AppLink>
    <AppLink
      isExternal
      to="mailto:nadiroumaima17@gmail.com"
      aria-label="Email Me"
      title="Email Me"
    >
      <svg
        width="41"
        height="41"
        viewBox="0 0 41 41"
        fill="none"
        xmlns="http://www.w3.org/2000/svg"
      >
<image
    width="43"
    height="47"
    
    xlink:href="https://static.vecteezy.com/system/resources/previews/020/009/614/non_2x/email-and-mail-icon-black-free-png.png"
  />
      </svg>
    </AppLink>
    
    
       
  </div>
</template>

<script setup>
import { computed, defineProps } from 'vue'

const props = defineProps({
  boxed: {
    type: Boolean,
    default: false,
  },
})

const classes = computed(() => ({
  'social-media-icons': true,
  'social-media-icons--boxed': props.boxed,
}))
</script>

<style scoped>
.social-media-icons {
  display: flex;
  align-items: center;

  & a {
    --shadow-opacity: 0;
    --shadow-h: 0;
    --shadow-s: 0%;
    --shadow-l: 0%;

    border-radius: var(--radius-default);
    background-color: var(--color-gray-800);
    padding: 0.25rem  0.5rem;
    box-shadow: 1px 4px 8px 1px
      hsla(
        var(--shadow-h),
        var(--shadow-s),
        var(--shadow-l),
        var(--shadow-opacity)
      );
    outline: 0;

    &:hover {
      --shadow-opacity: 0.25;
      transform: translateY(-8px);
    }

    &:hover svg,
    &:hover svg path {
      fill: var(--color-primary);
    }

    &:focus {
      --shadow-h: 187;
      --shadow-s: 78%;
      --shadow-l: 46%;
      --shadow-opacity: 0.5;
    }
  }

  & a + a {
    margin-inline-start: 20px;
  }

  & :is(a, svg, path) {
    transition-duration: 400ms;
    transition-timing-function: cubic-bezier(0.22, 0.61, 0.36, 1);
    transition-property: transform, fill, box-shadow;
    will-change: transform;
  }
}

.social-media-icons--boxed {
  a {
    display: inline-block;
  }
}

@media (--vw-sm) {
  .social-media-icons {
    justify-content: center;
  }
}

body[data-theme='light'] {
  .social-media-icons a {
    background-color: var(--bg-color-lighter);

    &:hover {
      --shadow-opacity: 0.05;
      transform: translateY(-8px);
    }

    svg, svg path {
      fill: var(--color-default-black);
    }
  }
}
</style>
