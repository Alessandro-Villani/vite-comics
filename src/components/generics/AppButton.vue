<script>
export default {
    props: {
        text: String,
        type: [String, Array]
    }
}
</script>

<template>
    <button :class="type">{{ text }}</button>
</template>

<style scoped lang="scss">
@use '../../assets/styles/partial/variables.scss' as *;

button {
    font-weight: bold;
    cursor: pointer;
    text-transform: uppercase;
    transition: all 0.5s;

    &.primary {
        padding: 0.5rem 3rem;
        color: white;
        background-color: $blue;
        border-color: transparent;

        &:hover {
            filter: brightness(150%);
        }

        &.outline {
            padding: 1rem;
            background-color: transparent;
            border: 2px solid $blue;

            &:hover {
                background-color: $blue;
                filter: brightness(100%);
            }
        }


    }


}
</style>