<script context="module">

    export async function load({fetch,page}) {
        const {id} = page.params
        console.log(id);
        return {props:{id:id}
            }
    }
</script>
<script>
    export let id
</script>

{id}