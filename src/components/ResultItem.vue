<script>
export default {
  props: {
    category: String,
    score: Number,
    icon: String,
  },
  methods: {
    getImageUrl(path) {
      return new URL(`../assets/images/${path}`, import.meta.url).href;
    },
  },
  computed: {
    class() {
      return this.category.toLowerCase();
    },
  },
};
</script>

<template>
  <li :class="class">
    <span class="category">
      <img :src="getImageUrl(icon)" :alt="`${category} icon`" />
      {{ category }}
    </span>
    <span class="score"
      ><strong>{{ score }}</strong> / 100
    </span>
  </li>
</template>

<style scoped>
li {
  --reaction: hsl(0, 100%, 67%);
  --reaction-bg: hsla(0, 100%, 67%, 5%);
  --memory: hsl(39, 100%, 56%);
  --memory-bg: hsla(39, 100%, 56%, 5%);
  --verbal: hsl(166, 100%, 37%);
  --verbal-bg: hsla(166, 100%, 37%, 5%);
  --visual: hsl(234, 85%, 45%);
  --visual-bg: hsla(234, 85%, 45%, 5%);
  padding: 1rem;
  border-radius: 12px;
  display: flex;
  align-items: center;
  justify-content: space-between;
  font-size: var(--fs-sm);
}

.category {
  display: flex;
  align-items: center;
  gap: 0.75rem;
}

.score {
  color: #303b59;
  word-spacing: 5px;
}

.reaction {
  background-color: var(--reaction-bg);
  .category {
    color: var(--reaction);
  }
}

.memory {
  background-color: var(--memory-bg);
  .category {
    color: var(--memory);
  }
}

.verbal {
  background-color: var(--verbal-bg);
  .category {
    color: var(--verbal);
  }
}

.visual {
  background-color: var(--visual-bg);
  .category {
    color: var(--visual);
  }
}
</style>
