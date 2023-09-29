<script>
	import {Chessground} from 'svelte-chessground';
	import {Chess} from 'chess.js';
	import {onMount} from 'svelte';
	import {toDests,playOtherSide} from '../lib/util.js';

    console.log("test");
	const chess = new Chess();

	let chessground;

	let config = {
		movable: {
			color: 'white',
			free: false,
			dests: toDests(chess),
		}
	};

	
	onMount(async () => {
		chessground.set( {
			movable: { events: { after: playOtherSide( chessground, chess ) } }
		});
	});

</script>

<Chessground bind:this={chessground} {config}/>