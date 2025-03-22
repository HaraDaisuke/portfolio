<template>
  <v-container>
    <v-row>
      <v-col cols="12" sm="6" md="4" lg="3" v-for="skill in skills" :key="skill.name">
        <SkillCard
          :name="skill.name"
          :icon="skill.icon"
          :level="skill.level"
          :cardColor="skill.cardColor"
          :iconColor="skill.iconColor"
          :progressBarColor="skill.progressBarColor"
        />
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import SkillCard from './SkillCard.vue'

export default {
  components: {
    SkillCard,
  },
  data() {
    return {
      skills: [
        {
          name: 'JavaScript',
          icon: 'mdi-language-javascript',
          level: 80,
          cardColor: 'yellow-lighten-4',
          iconColor: 'yellow-darken-2',
          progressBarColor: 'yellow-darken-2'
        },
        {
          name: 'Vue.js',
          icon: 'mdi-vuejs',
          level: 70,
          cardColor: 'green-lighten-4',
          iconColor: 'green-darken-2',
          progressBarColor: 'green-darken-2'
        },
        {
          name: 'HTML',
          icon: 'mdi-language-html5',
          level: 90,
          cardColor: 'red-lighten-4',
          iconColor: 'red-darken-2',
          progressBarColor: 'red-darken-2'
        },
        {
          name: 'CSS',
          icon: 'mdi-language-css3',
          level: 85,
          cardColor: 'blue-lighten-4',
          iconColor: 'blue-darken-2',
          progressBarColor: 'blue-darken-2'
        },
        // Add more skills here...
      ],
    };
  },
};
</script>
