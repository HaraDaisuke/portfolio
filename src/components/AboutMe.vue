<template>
  <v-card>
    <v-card-title>About Me</v-card-title>
    <v-card-text>
      <p>Here's a timeline of my work experience and key milestones:</p>

      <v-timeline density="comfortable">
        <v-timeline-item
          v-for="(item, index) in timelineItems"
          :key="index"
          :dot-color="item.color"
          size="small"
          class="timeline-item"
          :class="{ 'fade-in': item.isVisible }"
          @intersect="onIntersect($event, item)"
        >
          <template v-slot:opposite>
            <span v-text="item.date" class="font-weight-bold"></span>
          </template>
          <v-card :color="item.color" class="mb-6">
            <v-card-title class="text-white">
              {{ item.title }}
            </v-card-title>
            <v-card-text class="text-white">
              {{ item.description }}
            </v-card-text>
          </v-card>
        </v-timeline-item>
      </v-timeline>
    </v-card-text>
  </v-card>
</template>

<script>
export default {
  name: 'AboutMe',
  data() {
    return {
      timelineItems: [
        {
          date: "2023 - Present",
          title: "Current Role",
          description:
            "Working on exciting projects and contributing to the team's success.",
          color: "primary",
          isVisible: false,
        },
        {
          date: "2021 - 2023",
          title: "Previous Company",
          description:
            "Developed and maintained web applications using modern technologies.",
          color: "blue-darken-1",
          isVisible: false,
        },
        {
          date: "2019 - 2021",
          title: "Junior Developer",
          description:
            "Gained experience in software development and learned new skills.",
          color: "green-darken-1",
          isVisible: false,
        },
        {
          date: "2017 - 2019",
          title: "University Studies",
          description:
            "Studied Computer Science and developed a strong foundation in programming.",
          color: "orange-darken-1",
          isVisible: false,
        },
        {
          date: "2000 - 2001",
          title: "High School",
          description:
            "Completed high school and began exploring my interest in technology.",
          color: "purple-darken-1",
          isVisible: false,
        },
      ],
    };
  },
  methods: {
    onIntersect(entries, item) {
      // Check if the item is visible in the viewport
      if (entries.isIntersecting) {
        item.isVisible = true;
      }
    },
  },
};
</script>

<style scoped>
.timeline-item {
  opacity: 0;
  transition: opacity 0.5s ease-in-out;
}

.timeline-item.fade-in {
  opacity: 1;
}
</style>
