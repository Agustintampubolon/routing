<template>
  <div :class="['item-task d-flex align-items-start border-bottom pt-3 pb-4']">
    <div class="card mb-3 text-left">
      <div class="row no-gutters">
        <div class="col-sm-2">
          <nuxt-link :to="'artikel/detail/' + article.title">
            <img alt="" :src="article.img" style="width: 100%; height: 100%" />
          </nuxt-link>
        </div>
        <div class="col-md-10">
          <div class="card-body">
            <h5 class="card-title">
              <nuxt-link
                :to="'artikel/detail/' + article.title"
                style="text-decoration: none"
              >
                {{ article.title }}
              </nuxt-link>
            </h5>
            <template v-if="article.content">
              <p class="card-text" style="text-align: justify !important">
                {{ getArticleText(article.content) }}
              </p>
            </template>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    article: {
      type: Object,
      default: "Untitled",
    },
  },
  methods: {
    getArticleText(text) {
      const limitedText = text.substr(0, 200);
      if (limitedText.slice(-3) === ".....") {
        return limitedText;
      }
      return limitedText + ".....";
    },
  },
};
</script>
