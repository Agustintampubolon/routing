<template>
  <div class="py-4">
    <div class="card">
      <div class="container">
        <div v-for="article in articles" :key="article.id">
          <div
            class="item-task d-flex align-items-start border-bottom pt-3 pb-4"
            v-if="article.title == paramId"
          >
            <div class="entry clearfix">
              <div class="title-task mb-2 text-center">
                <h1>{{ article.title }}</h1>
              </div>
              <hr />
              <div class="entry-image text-center mb-3">
                <img
                  alt=""
                  :src="article.img"
                  style="width: 800px; height: 500px"
                />
              </div>
              <div
                class="description-task small mb-5"
                style="text-align: justify !important"
              >
                &nbsp;&nbsp;
                {{ article.content }}
              </div>
            </div>
          </div>
        </div>

        <div class="action mt-4">
          <div
            class="btn btn-outline-danger btn-sm mb-3"
            @click="$router.go(-1)"
          >
            Kembali
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      paramId: this.$route.params.id,
      articles: [
        {
          id: 1,
          title: "Monument Valley I",
          content:
            "Monument Valley is an indie puzzle game developed and published by Ustwo Games. The player leads the princess Ida through mazes of optical illusions and impossible objects while manipulating the world around her to reach various platforms. Monument Valley was developed over ten months beginning in early 2013 based on concept drawings by company artist Ken Wong. Its visual style was inspired by Japanese prints, minimalist sculpture, and indie games Windosill, Fez, and Sword & Sworcery, and was compared by critics to M. C. Escher drawings and Echochrome. The art was designed such that each frame would be worthy of public display. After a closed beta test, it was released for iOS on April 3, 2014, and was later ported to Android and Windows Phone. The game received generally favorable reviews. Critics praised its art and sound design, but noted its lack of difficulty and short length. It won a 2014 Apple Design Award, was named Apple's best iPad game of 2014, and sold over two million copies by January 2015; by May 2016, sales of the game exceeded 26 million.",
          img: "https://images.unsplash.com/photo-1649282806617-c51bb282899c?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=2070&q=80",
        },
        {
          id: 2,
          title: "Monument Valley II",
          content:
            "Monument Valley was developed by Ustwo, a digital design firm founded in 2004 that has produced iPhone apps since 2007. Their Whale Trail game received millions of downloads, and their other apps include design app Granimator and photo sharing app Rando. Monument Valley was conceived as a touch game for tablets. Its development began in the beginning of 2013, and lasted 10 months. It was developed under the working title, Tower of Illusion. It began with a piece of concept art drawn in the style of M. C. Escher, and the final design did not deviate far from this original. Ustwo management did not give the development team a timeline or budget, and instead told them to focus on making a high-quality product. Games development is not a large portion of Ustwo's revenue, so the company focuses its games development on producing great products that reflect well on the company, rather than highly profitable apps.",
          img: "https://images.unsplash.com/photo-1635732646038-0a1a2fe3f2d6?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1074&q=80",
        },
        {
          id: 3,
          title: "Monument Valley III",
          content:
            "Of the art style, game designer and artist Ken Wong said he aspired to make each frame of the gameplay worthy of public display. The project began as Wong's concept drawings before it became a game project. The visual style was inspired by Japanese prints, minimalist sculpture, and indie games Windosill, Fez, and Superbrothers: Sword & Sworcery EP. Wong added that the gameplay was designed to let the player find the object of the game through exploration, without direct guidance. The game uses colors to signify where the player can interact, similar to Mirror's Edge. Wong compared the gameplay experience to a cross between the wonder of a toy shop and the world of The Lion, the Witch, and the Wardrobe, and its story to a symbolic song rather than a narrative book. The game was designed to be completed by most players, a style uncommon for games designed for popular audiences. It was intended to be a premium experience rather than a difficult challenge.",
          img: "https://images.unsplash.com/photo-1640006807976-a6127e9d6fa0?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1171&q=80",
        },
      ],
    };
  },
};
</script>
