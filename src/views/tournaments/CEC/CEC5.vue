<template>
  <main>
    <Banner
      :title="$t('tournaments.CEC.5.self')"
      src="assets/img/carousel/CEC/CEC5.webp"
    />

    <div>
      <article id="sponsors" class="content">
        <img src="@/assets/img/sponsors/FullLife.webp" alt="FullLife" />
        <img
          src="@/assets/img/sponsors/Drone_Process.webp"
          alt="Drone Process"
        />
        <img src="@/assets/img/sponsors/Noctua.webp" alt="Noctua" />
        <img
          src="@/assets/img/sponsors/Coeur_de_Chartreuse.webp"
          alt="Coeur de Chartreuse"
        />
        <img
          src="@/assets/img/sponsors/Saint_Laurent_du_Pont.webp"
          alt="Saint Laurent du Pont"
        />
      </article>

      <article id="presentation" class="content">
        <h2>{{ $t("presentation") }}</h2>
        <p>{{ $t("tournaments.CEC.5.presentation") }}</p>
      </article>

      <Table img="Rocket_League" alt="Rocket League" :data="ranking.rl" />

      <Table
        img="CSGO"
        alt="Counter Strike: Global Offensive"
        :data="ranking.cs"
      />

      <Table
        img="League_of_Legends"
        alt="League of Legends"
        :data="ranking.lol"
      />

      <!--<Gallery :directory="gallery.directory" :images="gallery.images" />-->
    </div>
  </main>
</template>

<script>
import Banner from "@/components/other/banner";
import Table from "@/components/other/table";
import rl from "@/assets/json/CEC/CEC5/rocket_league.json";
import cs from "@/assets/json/CEC/CEC5/counter_strike.json";
import lol from "@/assets/json/CEC/CEC5/league_of_legends.json";

export default {
  name: "CEC5View",
  title() {
    return this.$t("tournaments.CEC.5.self");
  },
  components: {
    Banner,
    Table,
  },
  data() {
    return {
      ranking: {
        rl: rl,
        cs: cs,
        lol: lol,
      },
      gallery: {
        directory: "https://unpkg.com/vue-my-photos@1.0.0/src/assets/",
        images: [
          {
            name: "mountains.jpg",
            alt: "The Dolomites",
            id: "image1",
          },

          {
            name: "bird.jpg",
            alt: "It is a bird on a tree!",
            id: "image2",
          },

          {
            name: "alps.jpg",
            alt: "I will live here someday",
            id: "image3",
          },

          {
            name: "bear.jpg",
            alt: "Friendly bear",
            id: "image4",
          },

          {
            name: "canyon.jpg",
            alt: "A worthy hike",
            id: "image5",
          },

          {
            name: "monumentvalley.jpg",
            alt: "Monument Valley",
            id: "image6",
          },

          {
            name: "puppy.jpg",
            alt: "Puppy with a feather",
            id: "image7",
          },

          {
            name: "redwoods.jpg",
            alt: "Foggy evening in the Redwoods",
            id: "image8",
          },
        ],
      },
    };
  },
};
</script>

<style scoped lang="scss">
#sponsors {
  padding: 20px 16px;
  max-width: 1100px;
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  justify-content: space-evenly;
  gap: 30px;
  background-color: var(--bg-color);
  border-radius: 8px;
  box-shadow: rgba(0, 0, 0, 0.4) 0 8px 24px 0;

  img {
    max-width: 150px;
    max-height: 110px;
    padding: 8px;

    @media only screen and (max-width: 600px) {
      max-width: 120px;
      max-height: 90px;
    }
  }
}

#presentation {
  padding-bottom: 1rem;

  p {
    margin-bottom: 10px;
    font-size: 1.05em;

    &:last-of-type {
      margin-bottom: 0;
    }
  }
}
</style>
