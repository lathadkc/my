<script  context="module">
console.log("within script module joshna index.svelte");
 export async function load ({fetch,page}) {

const res= await fetch("/products.json") 
if (res.ok) {
   

    return {
       props:{pro: await res.json()}
      }

   return {
      status:res.status,
      error: new Error()
   }

   }
 }
</script>

<script> export let pro</script>

{ #each pro as {id,name,quantity}}

<h4>{id}  {name} <a href="/" {quantity} </h4>
{/each}
