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
  // data: {
  //   items: [
  //     { lang: "Php" },
  //     { lang: "Laravel" },
  //     { lang: "Java" },
  //     { lang: "c" },
  //     { lang: "c#" },
  //     { lang: "python" },
  //   ],
  // },
});
</script>
