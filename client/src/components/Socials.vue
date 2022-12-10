<template>
  <div>
    <div class="socials">
      <button
        class="socials-btn"
        @click="openLink('https://www.facebook.com/')"
      >
        <svg>
          <image href="../assets/images/facebook-f-brands.svg" width="12px" />
        </svg>
      </button>

      <button class="socials-btn" @click="openLink('https://twitter.com/home')">
        <svg>
          <image href="../assets/images/twitter-brands.svg" width="16px" />
        </svg>
      </button>

      <button
        class="socials-btn"
        @click="openLink('https://www.instagram.com/')"
      >
        <svg>
          <image href="../assets/images/instagram-brands.svg" width="16px" />
        </svg>
      </button>

      <button class="socials-btn" @click="openLink('https://www.google.com/')">
        <svg>
          <image href="../assets/images/share-alt-solid.svg" width="16px" />
        </svg>
      </button>
    </div>
  </div>
</template>

<script>
export default {
  methods: {
    openLink(url) {
      window.open(url, "_blank", "noreferrer")
    },
  },
}
</script>
