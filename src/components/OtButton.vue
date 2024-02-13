<template>
    <div class="button-wrapper">
        <button type="button">{{ message }}</button>
    </div>
</template>

<script setup lang="ts">
import { computed } from 'vue'

type Props = {
    disabled?: boolean,
    loading?: boolean,
}

defineProps<Props>();

// TODO: propagate the click event to the app wrapper
// TODO: add a loading state with a spinning icon by changing the class of the button to .is-loading and removing the text.
const message = computed(() => {
    return "Fetch list";
})

</script>

<style scoped lang="scss">
.button-wrapper {
    position: relative;

    & .is-loading:after {
        animation: spinAround 1s infinite linear;
        border-radius: 3rem;
        font-family: "OpenTicketIcons" !important;
        border-right-color: transparent;
        border-top-color: transparent;
        content: "\f145";
        display: block;
        position: absolute;
        height: 1em;
        width: 1em;
        top: calc(50% - (0.5em));
        left: calc(50% - (0.8em));
    }

    & .disabled {
        cursor: not-allowed;
        opacity: 0.7;
        color: grey;
        pointer-events: none;
    }
}


</style>
