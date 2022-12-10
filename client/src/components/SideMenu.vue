<template>
  <div>
    <button class="side-menu-btn" @click="toogleMenu">
      <svg width="32px" height="32px">
        <image
          v-if="!toogle"
          href="../assets/images/right-arrow.svg"
          width="24px"
        />
        <image v-else href="../assets/images/left-arrow.svg" width="24px" />
      </svg>
    </button>

    <div v-if="toogle" class="side-menu">
      <svg>
        <image href="../assets/images/logo.svg" />
      </svg>

      <div class="side-nav">
        <ul>
          <li><router-link to="/">Home</router-link></li>
          <li><router-link to="/">About</router-link></li>
          <li><router-link to="/">Contact</router-link></li>
          <li><router-link to="/">Features</router-link></li>
          <li><router-link to="/">Login</router-link></li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "SideMenu",
  data: () => ({
    toogle: false,
  }),

  methods: {
    toogleMenu() {
      this.toogle ? (this.toogle = false) : (this.toogle = true)
    },
  },
}
</script>
