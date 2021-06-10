<script>
  import About from './lib/About.svelte';
  import MainLogo from './lib/MainLogo.svelte';
  import Navbar from './lib/Navbar.svelte';
  import Squad from './lib/Squad.svelte';
  import logo from './assets/logo.png'
  let metaDesc = "Asteris RP najlepszy serwer RP FiveM jaki znajdziesz";
</script>
<svelte:head>
  <meta name="author" content="LupusVirtute"/>
  <meta name="description" content="AsterisRP server Page"/>
  <meta name="keywords" content="FiveM, Serwer, Serwer FiveM"/>
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <meta name="twitter:card" content="summary" />
  <meta name='twitter:title' content="Asteris RP"/>
  <meta name='twitter:description' content="{metaDesc}"/>
  <meta name='twitter:image' content="{logo}"/>
  <meta property="og:title" content="AsterisRP.pl"/>
  <meta property="og:type" content="website"/>
  <meta property="og:url" content="AsterisRP.pl"/>
  <meta property="og:locale" content="pl_PL"/>
  <meta property="og:description" content="{metaDesc}"/>
  <meta property="og:image" content="{logo}" />
  <meta property="og:image:alt" content="Asteris RP Server Logo"/>
  <meta property="og:image:type" content="image/png"/>

  <script src="https://kit.fontawesome.com/c0ff61a66a.js" crossorigin="anonymous"></script>
  <link rel="preconnect" href="https://fonts.gstatic.com">
  <link href="https://fonts.googleapis.com/css2?family=Inconsolata:wght@300&display=swap" rel="stylesheet">
</svelte:head>
<main>
  <Navbar/>
  <MainLogo/>
  <About/>
  <Squad/>
</main>
<style lang="sass" global>
body,html
  margin: 0
  padding: 0
  font-size: 3vh
  -ms-overflow-style: none
  scrollbar-width: none
body::-webkit-scrollbar
  display: none
@import url('https://fonts.googleapis.com/css2?family=Iceberg&display=swap')

</style>