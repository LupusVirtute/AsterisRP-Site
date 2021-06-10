<script lang="ts">
    let db = [
        {
            icon: 'fas fa-user',
            link: 'https://discord.gg/gSN97uRPpw'
        },
        {
            icon: 'fab fa-discord',
            link: 'https://discord.gg/gSN97uRPpw'
        }
    ]
</script>
<style lang='sass'>
.links
    margin-left: .11rem
a
    text-decoration: none
    color: inherit
.link
    margin-bottom: 1rem

</style>
<div class="links">
    {#each db as item}
        <a href="{item.link}" class="link">
            <i class="{item.icon}"></i>
        </a>
    
    {/each}
</div>