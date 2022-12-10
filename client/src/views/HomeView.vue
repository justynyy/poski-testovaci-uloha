<script setup>
import Article from "../components/Article.vue"
import Title from "../components/Title.vue"
</script>

<template>
  <main>
    <Title :title="'Testovací úloha - Radim Scholaster'" />
    <div class="wrapper">
      <div class="articles-container">
        <div class="grid-item-1 grid-item">
          <Article
            title="Etiam quis quam. Nemo enim ipsam voluptatem quia"
            category="Travel"
            date="May 25, 2048 / 9 min."
          />
        </div>

        <div class="grid-item-2 grid-item">
          <svg>
            <image href="../assets/images/space-station-moon-alt-duotone.svg" />
          </svg>

          <div class="grid-2-title">
            <h1>Discover content from different universe</h1>
          </div>
        </div>

        <div class="grid-item-3 grid-item">
          <Article
            title="Etiam quis quam. Nemo enim ipsam voluptatem quia"
            category="Travel"
            date="January 10, 2048 / 4 min."
            :isSmall="true"
          />
        </div>
        <div class="grid-item-4 grid-item">
          <Article
            title="Etiam quis quam. Nemo enim ipsam voluptatem quia"
            category="Tech"
            date="October 20, 2047 / 5 min."
            :isSmall="true"
          />
        </div>
        <div class="grid-item-5 grid-item">
          <Article
            title="Etiam quis quam. Nemo enim ipsam voluptatem quia"
            category="Travel"
            date="August 20, 2047 / 8 min."
          />
        </div>
      </div>
    </div>
  </main>
</template>
