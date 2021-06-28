<template>
  <div class="container mx-auto px-6 pt-6">
    <BlogPage />
  </div>
</template>
<script>
import { defineComponent } from "vue";
import BlogPage from "@/components/BlogPage.vue";

export default defineComponent({
  components: { BlogPage },
});
</script>
