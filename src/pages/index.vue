<template>
  <v-app id="inspire">
    <v-system-bar>
      <v-spacer></v-spacer>

      <v-icon>mdi-square</v-icon>

      <v-icon>mdi-circle</v-icon>

      <v-icon>mdi-triangle</v-icon>
    </v-system-bar>

    <v-navigation-drawer v-model="drawer">
      <v-sheet class="pa-4" color="grey-lighten-4">
        <v-avatar class="mb-4" color="grey-darken-1" size="64"></v-avatar>

        <div>john@google.com</div>
      </v-sheet>

      <v-divider></v-divider>

      <v-list>
        <v-list-item
          v-for="[icon, text, component] in links"
          :key="icon"
          :prepend-icon="icon"
          :title="text"
          link
          @click="currentComponent = component"
        ></v-list-item>
      </v-list>
    </v-navigation-drawer>

    <v-main>
      <v-container class="py-8 px-6" fluid>
        <v-slide-x-transition mode="out-in">
          <component :is="currentComponent" />
        </v-slide-x-transition>
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
import AboutMe from '@/components/AboutMe.vue';
import Skills from '@/components/Skills.vue';
import EducationAndCertifications from '@/components/EducationAndCertifications.vue';
import Links from '@/components/Links.vue';

export default {
  components: {
    AboutMe,
    Skills,
    EducationAndCertifications,
    Links,
  },
  data: () => ({
    drawer: null,
    currentComponent: 'AboutMe', // Default component
    links: [
      ['mdi-account', 'About Me', 'AboutMe'],
      ['mdi-tools', 'Skills', 'Skills'],
      ['mdi-school', 'Education and Certifications', 'EducationAndCertifications'],
      ['mdi-link-variant', 'Links', 'Links'],
    ],
  }),
};
</script>
