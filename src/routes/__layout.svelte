<script>
    import "$lib/style/global.scss"
    import Nav from '$lib/components/Nav.svelte';
    import Footer from '$lib/components/Footer.svelte';
</script>

<Nav />
<main>

    <slot />

</main>

<Footer />

<style lang="scss">
    main {
        height: 100vh;
    }
</style>