<template>
  <v-card class="skill-card" :color="cardColor" variant="tonal">
    <v-card-item>
      <v-row align="center">
        <v-col cols="auto">
          <v-avatar :color="iconColor" size="48">
            <v-icon size="32" :icon="icon"></v-icon>
          </v-avatar>
        </v-col>
        <v-col>
          <v-card-title class="text-h6">{{ name }}</v-card-title>
        </v-col>
      </v-row>
    </v-card-item>

    <v-card-text>
      <v-progress-linear
        :model-value="level"
        :color="progressBarColor"
        height="10"
        rounded
      ></v-progress-linear>
      <div class="text-caption mt-1 text-right">
        {{ level }}%
      </div>
    </v-card-text>
  </v-card>
</template>

<script>
export default {
  name: 'SkillCard',
  props: {
    name: {
      type: String,
      required: true,
    },
    icon: {
      type: String,
      required: true,
    },
    level: {
      type: Number,
      required: true,
      validator: (value) => value >= 0 && value <= 100,
    },
    cardColor: {
      type: String,
      default: 'grey-lighten-4',
    },
    iconColor: {
      type: String,
      default: 'primary',
    },
    progressBarColor: {
      type: String,
      default: 'primary',
    },
  },
};
</script>

<style scoped>
.skill-card {
  margin-bottom: 16px;
  border-radius: 12px;
}
</style>
