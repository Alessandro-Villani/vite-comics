<script>

export default {

}

</script>

<template>
    <main>
        <div class="content container">
            <p> --&gt Content goes here &lt-- </p>
        </div>
    </main>
</template>

<style lang="scss" scoped>
@use '../assets/styles/partial/mixins.scss' as *;
@use '../assets/styles/partial/variables.scss' as *;

main {
    background-color: $black;
    min-height: 150px;


    p {
        color: white;
        font-size: 30px;
        line-height: 150px;
    }
}
</style>