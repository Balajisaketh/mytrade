<script>
 import { onMount, onDestroy } from 'svelte';
    
   
    let screenWidth = 0;
    let check="empty";
    onMount(() => {
      screenWidth = window.innerWidth;
      window.addEventListener('resize', updateScreenSize);
    
      // Cleanup event listener when the component is destroyed
      return () => {
        window.removeEventListener('resize', updateScreenSize);
      };
    });
    function updateScreenSize() {
     screenWidth = window.innerWidth;
   }
</script>
<style>
@import 'bootstrap/dist/css/bootstrap.min.css';
</style>

<div class="d-flex flex-row  mt-4 col-12">
    <div class="column col-4 bg-danger">
       <div class="col-4 border-2 border">

       </div>        
        
       </div>
<div class="col-6 rounded border border-2 mx-2">
   
</div>
</div>
<footer>

</footer>