<script>
  import About from './lib/About.svelte';
  import MainLogo from './lib/MainLogo.svelte';
  import Navbar from './lib/Navbar.svelte';
  import Squad from './lib/Squad.svelte';
  import Footer from './lib/Footer.svelte';
</script>
<svelte:head>
  <script>
    if ('serviceWorker' in navigator) {
      navigator.serviceWorker.register('./sw.js');
    }
  </script>
  <script src="https://kit.fontawesome.com/c0ff61a66a.js" crossorigin="anonymous"></script>
  <link rel="preconnect" href="https://fonts.gstatic.com">
  <link href="https://fonts.googleapis.com/css2?family=Inconsolata:wght@300&display=swap" rel="stylesheet">
</svelte:head>
<main>
  <Navbar/>
  <MainLogo/>
  <About/>
  <Squad/>
  <Footer/>
</main>
<style lang="sass" global>
body,html
  margin: 0
  padding: 0
  font-size: 3vw
  -ms-overflow-style: none
  scrollbar-width: none
  background-color: #0b0b0b
body::-webkit-scrollbar
  display: none
@import url('https://fonts.googleapis.com/css2?family=Iceberg&display=swap')

</style>