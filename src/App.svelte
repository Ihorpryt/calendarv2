<script>
  import Sidebar from './lib/Sidebar.svelte';
  import Header from './lib/Header.svelte';
    import Calendar from './lib/Calendar.svelte';
</script>

<main>
  <Sidebar />
  <div class="content">
    <Header />
    <Calendar />
  </div>
</main>

<style>
  main {
    display: flex;
    flex-direction: row;
    width: 100%;
    height: 100%;
    min-height: 100%;
    overflow: hidden;
    -webkit-box-align: stretch;
    align-items: stretch;
  }
  .content {
    display: flex;
    flex-direction: column;
    width: 100%;
    height: 100vh;
  }
</style>
