<template>
  <div id="app">
    <VHSImage :imageSrc="image" />
  </div>
</template>

<script>
import VHSImage from "./components/VHSImage";

const imageUrl =
  "https://images.prismic.io/tcs-v2/OTJiMzBmY2ItMTBmNC00NTg4LWI3MWUtMGJhYTU5NjEyNGMx_d60c82fe-0984-4530-b866-aabd28076350_mule.jpg?auto=compress,format";

export default {
  name: "App",
  components: {
    VHSImage,
  },
  data() {
    return {
      image: imageUrl,
    };
  },
};
</script>

<style>
shader-doodle {
  position: absolute;
  top: 0;
  left: 0;
  height: 100vh;
  width: 100vw;
}
</style>
