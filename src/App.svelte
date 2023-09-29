<script>
  import Chessboard from './components/Chessboard.svelte';
  // generate a random name
  const name = ['World', 'Svelte', 'JavaScript', 'TypeScript', 'React', 'Vue', 'Angular'][Math.floor(Math.random() * 7)] //prettier-ignore
</script>

<!-- <HelloWorld {name} /> -->
<div style="display: flex; align-items: center; justify-content: center;">
	<div style="width: 100vh; height: 100vh;">
		<Chessboard />
	</div>

</div>