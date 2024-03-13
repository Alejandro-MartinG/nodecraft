<script>
    import Footer from "../components/footer.svelte";
    import Navbar from "../components/navbar.svelte";
</script>

<main>
    <Navbar></Navbar>

    <slot />

    <Footer></Footer>
</main>

<style>
    body {
        font-family: Oxygen, Ubuntu, Cantarell, "Open Sans", "Helvetica Neue";
        line-height: 1.6;
        margin-left: 0px;
        padding: 0;
        width: 100%;
        height: 100%;
    }
</style>
