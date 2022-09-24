<script lang="ts">
    const links = [
        {title: "Charts & Graphs", link: "#"},
        {title: "Articles", link: "#"},
        {title: "About Me", link: "#"},
        {title: "FAQ", link: "#"},
    ];
</script>

<nav>
    <ul>
    {#each links as link }
        <li><a href="{link.link}">{link.title}</a></li>
    {/each}
    </ul>
</nav>

<style>

    nav {
        padding-left: 10%;
    }
    li {
        margin-bottom: 10%;
    }

</style>