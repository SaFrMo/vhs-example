<template>
    <div class="vhs-image">
        <shader-doodle>
            <sd-texture
                src="https://s3-us-west-2.amazonaws.com/s.cdpn.io/476907/noise1.png"
                name="noise"
            ></sd-texture>
            <sd-texture :src="imageSrc" name="image" />
            <script type="x-shader/x-fragment" v-html="fragmentShader" />
        </shader-doodle>
    </div>
</template>

<script>
import 'shader-doodle'
import fragmentShader from 'raw-loader!glslify-loader!./fragment-shader.fs'

export default {
    name: 'VHSImage',
    props: {
        imageSrc: String,
    },
    data() {
        return {
            fragmentShader,
        }
    },
}
</script>

<style scoped>
</style>