<script lang="ts">
    import { scrollto } from "svelte-scrollto";
    let db = [
        {
            icon: 'fas fa-question-circle',
            link: '',
            scroll: '#About'
        },
        {
            icon: 'fas fa-users',
            link: '',
            scroll: '#Squad'
        },
        {
            icon: 'fab fa-discord',
            link: 'https://discord.gg/gSN97uRPpw',
            scroll: ''
        }
    ]
</script>
<style lang='sass'>
.links
    margin-left: .11rem
    z-index: 3
a
    text-decoration: none
    color: inherit
.link
    margin-bottom: 1rem

</style>
<div class="links">
    {#each db as item}
        <a href="{item.link}" class="link" use:scrollto={item.scroll}>
            <i class="{item.icon}"></i>
        </a>
    
    {/each}
</div>