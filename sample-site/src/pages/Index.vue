<template>
  <Layout>
    <header class="header">
      <h1>Welcome Minecraft</h1>
      <p>let's enjoy the game and our community</p>
    </header>
    <section class="posts">
      <PostList v-for="edge in $page.allPost.edges" :key="edge.node.id" :post="edge.node" />
    </section>
  </Layout>
</template>


<script>
import PostList from "@/components/PostList";
export default {
  components: {
    PostList
  },
  metaInfo: {
    title: "Welcome Minecraft"
  }
};
</script>
<page-query>

query {
  metadata {
    siteName
    siteDescription
  }
  allPost {
    totalCount
    edges {
      node {
        id
        title
        timeToRead
        description
        date (format: "D MMMM YYYY")
        path
      }
    }
  }
}
</page-query>

<style>
.header {
  font-family: "Gill Sans", sans-serif;
  font-size: 35px;
  text-align: center;
  line-height: 20px;
  padding: 0.7em;
}
.header h2 {
  font-weight: 200;
  font-size: 35px;
}
.header p {
  
}
</style>