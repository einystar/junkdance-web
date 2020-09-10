<template>
  <Layout>
    <div class="container">
      <Hero />
      <ProjectsGrid :projects="$page.projects.edges" />
    </div>
  </Layout>
</template>

<page-query>
query Posts {
	projects: allProjectPost {
    edges {
      node {
        id
        date (format: "YYYY")
        title
        thumbnail (quality: 90)
        path
      }
    }
  },
  journals: allJournalPost (perPage: 4) {
    edges {
      node {
        id
        path
        title
      }
    }
  }
}
</page-query>

<script>
import Hero from "@/components/Hero"
import ProjectsGrid from "@/components/ProjectsGrid"
import LatestUpdates from "@/components/LatestUpdates"

export default {
  components: {
    Hero,
    ProjectsGrid,
    LatestUpdates
  }
}
</script>
