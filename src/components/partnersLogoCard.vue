<template>

    <div class="ms_partner-logo-img">
        <img class="w-100" :src="require(`../assets/img/${singleLogo.img}`)" alt="company logo">
    </div>

</template>

<script>
export default {
    props: ['singleLogo'],

}
</script>

<style lang="scss">
@import "../styles/general.scss";
@import "../styles/variables.scss";
@import "../styles/mixins.scss";

.ms_partners-logo {
    display: flex;
    justify-content: space-around;
    align-items: center;
    margin-top: 160px;

    .ms_partner-logo-img {
        width: calc(100% / 5 - 80px);
        padding: 40px;
    }
}
</style>