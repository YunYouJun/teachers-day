<template>
  <BlackBoard :msg="msg" />
</template>

<script>
import BlackBoard from "./components/BlackBoard.vue";

export default {
  name: "App",
  components: {
    BlackBoard,
  },
  data() {
    return {
      msg: new URL(document.location).searchParams.get("msg"),
    };
  },
};
</script>
