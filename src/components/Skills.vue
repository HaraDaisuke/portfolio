<template>
  <v-container>
    <v-row>
      <v-col cols="12">
        <h2 class="text-h5 mb-4">Frontend Development</h2>
        <v-divider class="mb-4"></v-divider>
      </v-col>

      <v-col cols="12">
        <h3 class="text-h6 mb-2">Frameworks / Libraries</h3>
      </v-col>
      <v-col cols="12" sm="6" md="4" lg="3" v-for="skill in frontendFrameworkSkills" :key="skill.name">
        <SkillCard
          :name="skill.name"
          :icon="skill.icon"
          :level="skill.level"
          :cardColor="skill.cardColor"
          :iconColor="skill.iconColor"
          :progressBarColor="skill.progressBarColor"
        />
      </v-col>

      <v-col cols="12">
        <h3 class="text-h6 mt-4 mb-2">Styling / Component Frameworks</h3>
      </v-col>
      <v-col cols="12" sm="6" md="4" lg="3" v-for="skill in frontendComponentSkills" :key="skill.name">
        <SkillCard
          :name="skill.name"
          :icon="skill.icon"
          :level="skill.level"
          :cardColor="skill.cardColor"
          :iconColor="skill.iconColor"
          :progressBarColor="skill.progressBarColor"
        />
      </v-col>

      <v-col cols="12">
        <h3 class="text-h6 mt-4 mb-2">Styling / CSS Frameworks</h3>
      </v-col>
      <v-col cols="12" sm="6" md="4" lg="3" v-for="skill in frontendCSSFrameworkSkills" :key="skill.name">
        <SkillCard
          :name="skill.name"
          :icon="skill.icon"
          :level="skill.level"
          :cardColor="skill.cardColor"
          :iconColor="skill.iconColor"
          :progressBarColor="skill.progressBarColor"
        />
      </v-col>

      <v-col cols="12">
        <h2 class="text-h5 mt-8 mb-4">Backend Development</h2>
        <v-divider class="mb-4"></v-divider>
      </v-col>

      <v-col cols="12">
        <h3 class="text-h6 mb-2">Frameworks</h3>
      </v-col>
      <v-col cols="12" sm="6" md="4" lg="3" v-for="skill in backendFrameworkSkills" :key="skill.name">
        <SkillCard
          :name="skill.name"
          :icon="skill.icon"
          :level="skill.level"
          :cardColor="skill.cardColor"
          :iconColor="skill.iconColor"
          :progressBarColor="skill.progressBarColor"
        />
      </v-col>

      <v-col cols="12">
        <h3 class="text-h6 mt-4 mb-2">Servers</h3>
      </v-col>
      <v-col cols="12" sm="6" md="4" lg="3" v-for="skill in backendServerSkills" :key="skill.name">
        <SkillCard
          :name="skill.name"
          :icon="skill.icon"
          :level="skill.level"
          :cardColor="skill.cardColor"
          :iconColor="skill.iconColor"
          :progressBarColor="skill.progressBarColor"
        />
      </v-col>

      <v-col cols="12">
        <h3 class="text-h6 mt-4 mb-2">Authentication</h3>
      </v-col>
      <v-col cols="12" sm="6" md="4" lg="3" v-for="skill in backendAuthSkills" :key="skill.name">
        <SkillCard
          :name="skill.name"
          :icon="skill.icon"
          :level="skill.level"
          :cardColor="skill.cardColor"
          :iconColor="skill.iconColor"
          :progressBarColor="skill.progressBarColor"
        />
      </v-col>

      <v-col cols="12">
        <h2 class="text-h5 mt-8 mb-4">Database</h2>
        <v-divider class="mb-4"></v-divider>
      </v-col>

      <v-col cols="12">
        <h3 class="text-h6 mb-2">RDBMS</h3>
      </v-col>
      <v-col cols="12" sm="6" md="4" lg="3" v-for="skill in databaseRDBMSSkills" :key="skill.name">
        <SkillCard
          :name="skill.name"
          :icon="skill.icon"
          :level="skill.level"
          :cardColor="skill.cardColor"
          :iconColor="skill.iconColor"
          :progressBarColor="skill.progressBarColor"
        />
      </v-col>

      <v-col cols="12">
        <h3 class="text-h6 mt-4 mb-2">Search Engines</h3>
      </v-col>
      <v-col cols="12" sm="6" md="4" lg="3" v-for="skill in databaseSearchSkills" :key="skill.name">
        <SkillCard
          :name="skill.name"
          :icon="skill.icon"
          :level="skill.level"
          :cardColor="skill.cardColor"
          :iconColor="skill.iconColor"
          :progressBarColor="skill.progressBarColor"
        />
      </v-col>

      <v-col cols="12">
        <h2 class="text-h5 mt-8 mb-4">DevOps / Infrastructure</h2>
        <v-divider class="mb-4"></v-divider>
      </v-col>

      <v-col cols="12">
        <h3 class="text-h6 mb-2">Containers and Orchestration</h3>
      </v-col>
      <v-col cols="12" sm="6" md="4" lg="3" v-for="skill in devopsContainerSkills" :key="skill.name">
        <SkillCard
          :name="skill.name"
          :icon="skill.icon"
          :level="skill.level"
          :cardColor="skill.cardColor"
          :iconColor="skill.iconColor"
          :progressBarColor="skill.progressBarColor"
        />
      </v-col>

      <v-col cols="12">
        <h3 class="text-h6 mt-4 mb-2">CI/CD</h3>
      </v-col>
      <v-col cols="12" sm="6" md="4" lg="3" v-for="skill in devopsCICDSkills" :key="skill.name">
        <SkillCard
          :name="skill.name"
          :icon="skill.icon"
          :level="skill.level"
          :cardColor="skill.cardColor"
          :iconColor="skill.iconColor"
          :progressBarColor="skill.progressBarColor"
        />
      </v-col>

      <v-col cols="12">
        <h2 class="text-h5 mt-8 mb-4">Machine Learning / Data Science</h2>
        <v-divider class="mb-4"></v-divider>
      </v-col>

      <v-col cols="12">
        <h3 class="text-h6 mb-2">Frameworks</h3>
      </v-col>
      <v-col cols="12" sm="6" md="4" lg="3" v-for="skill in mlFrameworkSkills" :key="skill.name">
        <SkillCard
          :name="skill.name"
          :icon="skill.icon"
          :level="skill.level"
          :cardColor="skill.cardColor"
          :iconColor="skill.iconColor"
          :progressBarColor="skill.progressBarColor"
        />
      </v-col>

      <v-col cols="12">
        <h3 class="text-h6 mt-4 mb-2">Libraries</h3>
      </v-col>
      <v-col cols="12" sm="6" md="4" lg="3" v-for="skill in mlLibrarySkills" :key="skill.name">
        <SkillCard
          :name="skill.name"
          :icon="skill.icon"
          :level="skill.level"
          :cardColor="skill.cardColor"
          :iconColor="skill.iconColor"
          :progressBarColor="skill.progressBarColor"
        />
      </v-col>

      <v-col cols="12">
        <h2 class="text-h5 mt-8 mb-4">Cloud</h2>
        <v-divider class="mb-4"></v-divider>
      </v-col>
      <v-col cols="12" sm="6" md="4" lg="3" v-for="skill in cloudSkills" :key="skill.name">
        <SkillCard
          :name="skill.name"
          :icon="skill.icon"
          :level="skill.level"
          :cardColor="skill.cardColor"
          :iconColor="skill.iconColor"
          :progressBarColor="skill.progressBarColor"
        />
      </v-col>

      <v-col cols="12">
        <h2 class="text-h5 mt-8 mb-4">Version Control / Team Collaboration</h2>
        <v-divider class="mb-4"></v-divider>
      </v-col>

      <v-col cols="12">
        <h3 class="text-h6 mb-2">Version Control</h3>
      </v-col>
      <v-col cols="12" sm="6" md="4" lg="3" v-for="skill in versionControlSkills" :key="skill.name">
        <SkillCard
          :name="skill.name"
          :icon="skill.icon"
          :level="skill.level"
          :cardColor="skill.cardColor"
          :iconColor="skill.iconColor"
          :progressBarColor="skill.progressBarColor"
        />
      </v-col>

      <v-col cols="12">
        <h3 class="text-h6 mt-4 mb-2">Repository Hosting</h3>
      </v-col>
      <v-col cols="12" sm="6" md="4" lg="3" v-for="skill in repositoryHostingSkills" :key="skill.name">
        <SkillCard
          :name="skill.name"
          :icon="skill.icon"
          :level="skill.level"
          :cardColor="skill.cardColor"
          :iconColor="skill.iconColor"
          :progressBarColor="skill.progressBarColor"
        />
      </v-col>

      <v-col cols="12">
        <h3 class="text-h6 mt-4 mb-2">Project Management</h3>
      </v-col>
      <v-col cols="12" sm="6" md="4" lg="3" v-for="skill in projectManagementSkills" :key="skill.name">
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
        // Frontend Development
        { name: 'React', icon: 'mdi-react', level: 75, cardColor: 'blue-lighten-4', iconColor: 'blue-darken-2', progressBarColor: 'blue-darken-2', category: 'frontend', subcategory: 'framework' },
        { name: 'Vue.js', icon: 'mdi-vuejs', level: 80, cardColor: 'green-lighten-4', iconColor: 'green-darken-2', progressBarColor: 'green-darken-2', category: 'frontend', subcategory: 'framework' },
        { name: 'Nuxt.js', icon: 'mdi-nuxt', level: 65, cardColor: 'blue-grey-lighten-4', iconColor: 'blue-grey-darken-2', progressBarColor: 'blue-grey-darken-2', category: 'frontend', subcategory: 'framework' },
        { name: 'Vuetify', icon: 'mdi-vuetify', level: 70, cardColor: 'purple-lighten-4', iconColor: 'purple-darken-2', progressBarColor: 'purple-darken-2', category: 'frontend', subcategory: 'component' },
        { name: 'Material-UI', icon: 'mdi-material-ui', level: 60, cardColor: 'blue-lighten-4', iconColor: 'blue-darken-2', progressBarColor: 'blue-darken-2', category: 'frontend', subcategory: 'component' },
        { name: 'Bootstrap', icon: 'mdi-bootstrap', level: 85, cardColor: 'purple-lighten-4', iconColor: 'purple-darken-2', progressBarColor: 'purple-darken-2', category: 'frontend', subcategory: 'css' },
        { name: 'Bulma', icon: 'mdi-view-grid-outline', level: 70, cardColor: 'info-lighten-4', iconColor: 'info-darken-2', progressBarColor: 'info-darken-2', category: 'frontend', subcategory: 'css' },

        // Backend Development
        { name: 'Express', icon: 'mdi-nodejs', level: 70, cardColor: 'green-lighten-4', iconColor: 'green-darken-2', progressBarColor: 'green-darken-2', category: 'backend', subcategory: 'framework' },
        { name: 'Django', icon: 'mdi-language-python', level: 60, cardColor: 'blue-grey-lighten-4', iconColor: 'blue-grey-darken-2', progressBarColor: 'blue-grey-darken-2', category: 'backend', subcategory: 'framework' },
        { name: 'Flask', icon: 'mdi-flask', level: 65, cardColor: 'grey-lighten-4', iconColor: 'grey-darken-2', progressBarColor: 'grey-darken-2', category: 'backend', subcategory: 'framework' },
        { name: 'FastAPI', icon: 'mdi-api', level: 55, cardColor: 'blue-lighten-4', iconColor: 'blue-darken-2', progressBarColor: 'blue-darken-2', category: 'backend', subcategory: 'framework' },
        { name: 'Nginx', icon: 'mdi-engine', level: 75, cardColor: 'green-lighten-4', iconColor: 'green-darken-2', progressBarColor: 'green-darken-2', category: 'backend', subcategory: 'server' },
        { name: 'Keycloak', icon: 'mdi-key', level: 50, cardColor: 'orange-lighten-4', iconColor: 'orange-darken-2', progressBarColor: 'orange-darken-2', category: 'backend', subcategory: 'auth' },

        // Database
        { name: 'MySQL', icon: 'mdi-database', level: 80, cardColor: 'blue-lighten-4', iconColor: 'blue-darken-2', progressBarColor: 'blue-darken-2', category: 'database', subcategory: 'rdbms' },
        { name: 'PostgreSQL', icon: 'mdi-database', level: 70, cardColor: 'blue-lighten-4', iconColor: 'blue-darken-2', progressBarColor: 'blue-darken-2', category: 'database', subcategory: 'rdbms' },
        { name: 'MariaDB', icon: 'mdi-database', level: 65, cardColor: 'blue-lighten-4', iconColor: 'blue-darken-2', progressBarColor: 'blue-darken-2', category: 'database', subcategory: 'rdbms' },
        { name: 'SQLServer', icon: 'mdi-database', level: 55, cardColor: 'blue-lighten-4', iconColor: 'blue-darken-2', progressBarColor: 'blue-darken-2', category: 'database', subcategory: 'rdbms' },
        { name: 'Elasticsearch', icon: 'mdi-magnify', level: 60, cardColor: 'orange-lighten-4', iconColor: 'orange-darken-2', progressBarColor: 'orange-darken-2', category: 'database', subcategory: 'search' },
        { name: 'Azure AI Search', icon: 'mdi-microsoft-azure', level: 45, cardColor: 'blue-lighten-4', iconColor: 'blue-darken-2', progressBarColor: 'blue-darken-2', category: 'database', subcategory: 'search' },

        // DevOps / Infrastructure
        { name: 'Docker', icon: 'mdi-docker', level: 75, cardColor: 'blue-lighten-4', iconColor: 'blue-darken-2', progressBarColor: 'blue-darken-2', category: 'devops', subcategory: 'container' },
        { name: 'Kubernetes', icon: 'mdi-kubernetes', level: 60, cardColor: 'blue-lighten-4', iconColor: 'blue-darken-2', progressBarColor: 'blue-darken-2', category: 'devops', subcategory: 'container' },
        { name: 'GitLab CI', icon: 'mdi-gitlab', level: 65, cardColor: 'orange-lighten-4', iconColor: 'orange-darken-2', progressBarColor: 'orange-darken-2', category: 'devops', subcategory: 'cicd' },

        // Machine Learning / Data Science
        { name: 'scikit-learn', icon: 'mdi-chart-scatter-plot', level: 50, cardColor: 'green-lighten-4', iconColor: 'green-darken-2', progressBarColor: 'green-darken-2', category: 'ml', subcategory: 'framework' },
        { name: 'pandas', icon: 'mdi-table', level: 70, cardColor: 'blue-grey-lighten-4', iconColor: 'blue-grey-darken-2', progressBarColor: 'blue-grey-darken-2', category: 'ml', subcategory: 'library' },
        { name: 'Matplotlib', icon: 'mdi-chart-line', level: 60, cardColor: 'purple-lighten-4', iconColor: 'purple-darken-2', progressBarColor: 'purple-darken-2', category: 'ml', subcategory: 'library' },

        // Cloud
        { name: 'Azure', icon: 'mdi-microsoft-azure', level: 55, cardColor: 'blue-lighten-4', iconColor: 'blue-darken-2', progressBarColor: 'blue-darken-2', category: 'cloud', subcategory: 'service' },

        // Version Control / Team Collaboration
        { name: 'Git', icon: 'mdi-git', level: 85, cardColor: 'orange-lighten-4', iconColor: 'orange-darken-2', progressBarColor: 'orange-darken-2', category: 'version', subcategory: 'control' },
        { name: 'GitHub', icon: 'mdi-github', level: 80, cardColor: 'grey-lighten-4', iconColor: 'grey-darken-2', progressBarColor: 'grey-darken-2', category: 'version', subcategory: 'hosting' },
        { name: 'GitLab', icon: 'mdi-gitlab', level: 70, cardColor: 'orange-lighten-4', iconColor: 'orange-darken-2', progressBarColor: 'orange-darken-2', category: 'version', subcategory: 'hosting' },
        { name: 'Redmine', icon: 'mdi-clipboard-text-multiple', level: 60, cardColor: 'red-lighten-4', iconColor: 'red-darken-2', progressBarColor: 'red-darken-2', category: 'version', subcategory: 'management' },
      ],
    };
  },
  computed: {
    frontendFrameworkSkills() {
      return this.skills.filter(skill => skill.category === 'frontend' && skill.subcategory === 'framework');
    },
    frontendComponentSkills() {
      return this.skills.filter(skill => skill.category === 'frontend' && skill.subcategory === 'component');
    },
    frontendCSSFrameworkSkills() {
      return this.skills.filter(skill => skill.category === 'frontend' && skill.subcategory === 'css');
    },
    backendFrameworkSkills() {
      return this.skills.filter(skill => skill.category === 'backend' && skill.subcategory === 'framework');
    },
    backendServerSkills() {
      return this.skills.filter(skill => skill.category === 'backend' && skill.subcategory === 'server');
    },
    backendAuthSkills() {
      return this.skills.filter(skill => skill.category === 'backend' && skill.subcategory === 'auth');
    },
    databaseRDBMSSkills() {
      return this.skills.filter(skill => skill.category === 'database' && skill.subcategory === 'rdbms');
    },
    databaseSearchSkills() {
      return this.skills.filter(skill => skill.category === 'database' && skill.subcategory === 'search');
    },
    devopsContainerSkills() {
      return this.skills.filter(skill => skill.category === 'devops' && skill.subcategory === 'container');
    },
    devopsCICDSkills() {
      return this.skills.filter(skill => skill.category === 'devops' && skill.subcategory === 'cicd');
    },
    mlFrameworkSkills() {
      return this.skills.filter(skill => skill.category === 'ml' && skill.subcategory === 'framework');
    },
    mlLibrarySkills() {
      return this.skills.filter(skill => skill.category === 'ml' && skill.subcategory === 'library');
    },
    cloudSkills() {
      return this.skills.filter(skill => skill.category === 'cloud' && skill.subcategory === 'service');
    },
    versionControlSkills() {
      return this.skills.filter(skill => skill.category === 'version' && skill.subcategory === 'control');
    },
    repositoryHostingSkills() {
      return this.skills.filter(skill => skill.category === 'version' && skill.subcategory === 'hosting');
    },
    projectManagementSkills() {
      return this.skills.filter(skill => skill.category === 'version' && skill.subcategory === 'management');
    },
  },
};
</script>
