<template>
  <div id="main" :class="{ dark: isDark }">
    <Header :isDark="isDark" :toggleTheme="toggleTheme" />
  </div>
</template>

<script>
  import Header from './components/Header.vue';

  export default {
    name: 'App',
    components: { Header },
    data() {
      return {
        isDark: false,
      };
    },
    methods: {
      toggleTheme() {
        this.isDark = !this.isDark;
        if (this.isDark) {
          document.body.style.background = '#14141a';
        } else {
          document.body.style.background = '#fff0e5';
        }
      },
    },
  };
</script>

<style lang="scss">
  .dark {
    background-color: #14141a;
    color: #fff;

    header {
      background-color: #21212b;

      svg {
        fill: #fff !important;
      }
    }

    svg.tre {
      background-image: radial-gradient(#35353d 0.8px, #ffffff00 0.8px);

      text {
        fill: #fff;
      }
    }

    .card {
      background-color: #21212b !important;
      color: #585669;

      label {
        color: rgb(241, 241, 241);
      }
    }

    input {
      border: 0.1rem solid #585669 !important;
      background-color: transparent;
      color: rgb(241, 241, 241);
    }

    .tag {
      color: #ffd789;
    }

    #polygon {
      fill: #e3fbae !important;
    }

    footer {
      background-color: #21212b;
    }
  }
</style>
