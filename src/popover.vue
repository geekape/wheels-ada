<template>
    <div class="popover" @click="xxx">
        <div class="content-wrapper" v-if="visible">
            <slot name="content"></slot>
        </div>
        <slot></slot>
    </div>
</template>

<script>
    export default {
        name: "WheelsPopover",
        data() {
            return {visible: false}
        },
        methods: {
            xxx() {
                this.visible = !this.visible
            }
        }
    }
</script>

<style scoped lang="scss">
    .popover {
        display: inline-block;
        position: relative;
        vertical-align: top;
        .content-wrapper {
            position: absolute;
            bottom: 100%;
            left: 0;
            border: 1px solid #ddd;
            box-shadow: 0 0 3px rgba(0, 0, 0, 0.75);
        }
    }
</style>