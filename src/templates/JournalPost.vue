<template>
  <Layout>
    <div class="journal">
      <div class="container journal-container">
        <JournalContent :content="$page.post.content" />
      </div>
    </div>
  </Layout>
</template>

<page-query>
query JournalPost ($path: String!) {
  post: journalPost (path: $path) {
    title
    author
    date (format: "MMMM D, YYYY")
    timeToRead
    content
  }
}
</page-query>

<script>
import JournalContent from "@/components/JournalContent"

export default {
  components: {
    JournalContent
  },
  metaInfo () {
    return {
      title: this.$page.post.title
    }
  }
}
</script>

<style scoped>
.journal-container {
  max-width: 840px;
  padding: 5rem 0 2rem 0;
}

.journal-header {
  padding: 5rem 0 2rem 0;
}
.journal-title {
  font-size: 4rem;
  margin: 0 0 4rem 0;
  padding: 0;
}
.journal-meta {
  display: flex;
  flex-wrap: wrap;
  font-size: 0.8rem;
}
.journal-meta > div {
  margin-right: 4rem;
}
.journal-meta > div:last-of-type {
  margin: 0;
}
</style>
