<script setup></script>

<template>
  <div>
    <article>
      <div class="article-category">
        <h2 class="article-category-text" :class="getCategoryClass(category)">
          {{ category }}
        </h2>
      </div>

      <div
        class="artitle-title-container"
        :class="{ 'article-small': isSmall }"
      >
        <h1 class="article-title">
          <router-link
            to="/"
            @click="
              showData({
                title: title,
                category: category,
                date: date,
              })
            "
            >{{ title }}
          </router-link>
        </h1>
      </div>
      <h3 class="article-release-date">{{ date }}</h3>
    </article>
  </div>
</template>

<script>
export default {
  props: {
    title: String,
    category: String,
    date: String,
    isSmall: Boolean,
  },

  methods: {
    getCategoryClass(category) {
      return {
        "article-category-travel": category == "Travel",
        "article-category-tech": category == "Tech",
      }
    },

    showData(data) {
      console.log(data)
    },
  },
}
</script>
