<script lang="ts">
    import "../app.postcss";
    import Nav from "./Nav.svelte";
    import Search from "./Search.svelte";
</script>

<div class="main-grid">
    <header>
        <div class="logo"></div>
        <aside>
            <Search/>
            <Nav/>
        </aside>
    </header>

    <slot>

    </slot>

</div>


<style>
:global(:root){
        --brand-color: #FFA63E;
        --brand-dark: #202238;
        --brand-light: #FFFDF5;
        --metro-red: #EE352E;
        --metro-blue: #003986;
        --metro-green: #00933C;

        --container-margins: 0;
    }

    .main-grid {
        display: grid;
        grid-template-columns: 1fr;
        grid-template-rows: 6rem;
        height: calc(100vh - 1rem);
        max-width: 1200px;
        margin: auto;
    }

    aside{
        display: grid;
        grid-template-columns:1fr;
    }

    .logo{
        background-image: url('logos/logo_wide_light.svg');
        background-size: contain;
        background-position: center;
        background-repeat: no-repeat;
        margin-top: 10px;

        height: 3rem;
    }

    @media (min-width: 700px) {
        .main-grid {
            display: grid;
            grid-template-columns: 1fr 3fr;
            grid-template-rows: 1fr;
            height: calc(100vh - 1rem);
            max-width: 1200px;
            margin: auto;

            border-style: solid;
            border-right-width: 2px;
            border-bottom-width: 2px;
            border-color: var(--brand-dark);
        }
        header{
            border-style: solid;
            border-left-width: 2px;
            border-right-width: 2px;
            border-color: var(--brand-dark);
        }

        aside{
            display: grid;
            grid-template-columns:1fr;
        }

        .logo{
            background-image: url('logos/logo_header.svg');
            image-orientation: flip;
            background-size: cover;
            background-position: center;
            aspect-ratio: 1;

            height: auto;
            margin-top: 0;
        }

    }

</style>