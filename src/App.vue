<template>
  <BlackBoard :msg="msg" :greeting="greeting" />
</template>

<script>
import BlackBoard from "./components/BlackBoard.vue";
const params = new URL(document.location).searchParams;
export default {
  name: "App",
  components: {
    BlackBoard,
  },
  data() {
    return {
      msg: params.get("msg") || "祝老师",
      greeting: params.get("greeting") || "教师节快乐",
    };
  },
};
</script>
