<template>
  <div class="container mt-5">
    <h1 class="mb-4">Search</h1>
    <div class="search-form">
      <input
        type="text"
        v-model="searchTerm"
        class="form-control"
        id="search"
        placeholder=""
      />
      <i
        class="bi bi-x-circle clear"
        v-if="searchTerm.length > 0"
        @click="clearSearch"
      ></i>
    </div>

    <list-posts :posts="posts" :searchTerm="searchTerm" />
  </div>
</template>

<script>
import ListPosts from "./ListPosts.vue";
export default {
  components: { ListPosts },
  name: "SearchPosts",
  data() {
    return {
      searchTerm: "",
      posts: [
        {
          id: 1,
          title: "Learning Vue.js",
          description:
            "Vue.js is a progressive JavaScript framework for building user interfaces.",
          date: "2024-10-01",
        },
        {
          id: 2,
          title: "JavaScript Best Practices",
          description:
            "This post covers best practices for writing clean and efficient JavaScript code.",
          date: "2024-09-30",
        },
        {
          id: 3,
          title: "Getting Started with Node.js",
          description: "An introduction to building backends with Node.js.",
          date: "2024-09-29",
        },
        {
          id: 4,
          title: "Understanding CSS Grid",
          description: "CSS Grid is a powerful layout system available in CSS.",
          date: "2024-09-28",
        },
        {
          id: 5,
          title: "Vue.js vs React",
          description:
            "A comparison between two popular JavaScript frameworks: Vue.js and React.",
          date: "2024-09-27",
        },
        {
          id: 6,
          title: "Functional Programming in JavaScript",
          description:
            "Explore the concepts of functional programming in JavaScript.",
          date: "2024-09-26",
        },
        {
          id: 7,
          title: "Building Responsive Websites",
          description:
            "Learn how to build responsive websites that work on any device.",
          date: "2024-09-25",
        },
        {
          id: 8,
          title: "JavaScript ES6 Features",
          description: "A guide to new features introduced in ES6.",
          date: "2024-09-24",
        },
        {
          id: 9,
          title: "Mastering Git and GitHub",
          description:
            "A comprehensive guide to using Git and GitHub for version control.",
          date: "2024-09-23",
        },
        {
          id: 10,
          title: "Understanding JavaScript Closures",
          description:
            "An in-depth look at closures in JavaScript and how they work.",
          date: "2024-09-22",
        },
        {
          id: 11,
          title: "Working with APIs in Vue.js",
          description:
            "Learn how to integrate APIs into your Vue.js applications.",
          date: "2024-09-21",
        },
        {
          id: 12,
          title: "Advanced Vue.js Directives",
          description:
            "Learn about advanced directives in Vue.js and how to create custom ones.",
          date: "2024-09-20",
        },
        {
          id: 13,
          title: "Intro to TypeScript",
          description:
            "An introduction to TypeScript and its benefits for JavaScript developers.",
          date: "2024-09-19",
        },
        {
          id: 14,
          title: "Building Single Page Applications (SPAs)",
          description: "A guide to building SPAs using Vue.js.",
          date: "2024-09-18",
        },
        {
          id: 15,
          title: "Debugging JavaScript Code",
          description: "Techniques for effectively debugging JavaScript code.",
          date: "2024-09-17",
        },
        {
          id: 16,
          title: "Understanding Vue.js Lifecycle Hooks",
          description:
            "A deep dive into Vue.js lifecycle hooks and how to use them.",
          date: "2024-09-16",
        },
        {
          id: 17,
          title: "Asynchronous JavaScript: Promises and Async/Await",
          description: "Understanding asynchronous programming in JavaScript.",
          date: "2024-09-15",
        },
        {
          id: 18,
          title: "State Management in Vue.js with Vuex",
          description:
            "How to manage state in large-scale Vue.js applications using Vuex.",
          date: "2024-09-14",
        },
        {
          id: 19,
          title: "Optimizing Performance in JavaScript Apps",
          description:
            "Tips for improving the performance of your JavaScript applications.",
          date: "2024-09-13",
        },
        {
          id: 20,
          title: "Vue Router: Building Dynamic Routes",
          description:
            "How to set up and configure dynamic routes in Vue.js using Vue Router.",
          date: "2024-09-12",
        },
        {
          id: 21,
          title: "Deploying Vue.js Applications",
          description:
            "Best practices for deploying Vue.js apps to production.",
          date: "2024-09-11",
        },
        {
          id: 22,
          title: "JavaScript Design Patterns",
          description:
            "An overview of common design patterns in JavaScript development.",
          date: "2024-09-10",
        },
        {
          id: 23,
          title: "Unit Testing in Vue.js",
          description: "How to write unit tests for your Vue.js components.",
          date: "2024-09-09",
        },
        {
          id: 24,
          title: "Securing Your Vue.js Application",
          description:
            "A guide to securing your Vue.js application from common vulnerabilities.",
          date: "2024-09-08",
        },
        {
          id: 25,
          title: "Introduction to Progressive Web Apps (PWAs)",
          description: "What are PWAs and how to build them using Vue.js.",
          date: "2024-09-07",
        },
      ],
    };
  },
  methods: {
    clearSearch() {
      this.searchTerm = "";
    },
  },
};
</script>

<style scoped>
.search-form {
  position: relative;
}
.clear {
  position: absolute;
  right: 15px;
  top: 7px;
  cursor: pointer;
}
</style>
