<script lang="ts">
    let db = [
        {
            icon: 'fa-user',
        }
    ]
</script>
<style lang='sass'>
.links
    margin-left: .11rem
</style>
<div class="links">
    {#each db as item}
        <i class="fas {item.icon}"></i>
    
    {/each}
</div>