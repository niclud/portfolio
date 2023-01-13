<script lang="ts">
	interface Posiciones {
		isTaken: boolean;
		player: string;
	}
	let posiciones: Posiciones[] = [
		{ isTaken: false, player: '' },
		{ isTaken: false, player: '' },
		{ isTaken: false, player: '' },
		{ isTaken: false, player: '' },
		{ isTaken: false, player: '' },
		{ isTaken: false, player: '' },
		{ isTaken: false, player: '' },
		{ isTaken: false, player: '' },
		{ isTaken: false, player: '' }
	];
	console.log(posiciones);
	let winResults: number[][] = [
		[0, 1, 2],
		[3, 4, 5],
		[6, 7, 8],
		[0, 3, 6],
		[1, 4, 7],
		[2, 5, 8],
		[0, 4, 8],
		[2, 4, 6]
	];

	const setPos = (pos: number, player: string) => {
		posiciones[pos].isTaken = true;
		posiciones[pos].player = player;
		return;
	};
	const getPos = (pos: number, option: number) => {
		if (option === 1) return posiciones[pos].isTaken;
		if (option === 2) return posiciones[pos].player;
	};

	const checkBox = (pos: number) => {
		if (posiciones.every((posi) => posi.isTaken)) {
			return;
		}
		if (posiciones[pos].isTaken === true) {
			return;
		}
		setPos(pos, 'player');
		checkBoxMachine(pos);
		checkWin2();
		console.log(posiciones);
	};
	const checkBoxMachine = (pos: number) => {
		if (!getPos(4, 1)) {
			setPos(4, 'comp');
		} else {
		}
	};
	const checkWin2 = () => {
		let aux2: string[] = [];
		winResults.map((res) => {
			res.map((pos, indice) => {
				if (posiciones[pos].isTaken) {
					if ((aux2 && aux2.every((a) => posiciones[pos].player === a)) || indice === 0) {
						aux2.push(posiciones[pos].player);
					}
				}
			});
			if (aux2.every((a) => a === 'player') && aux2.length === 3) {
				console.log('lo lograste nico');
				return;
			}
			aux2 = [];
		});
	};
</script>

<div class="grid grid-cols-3">
	{#each posiciones as posicion, pos}
		<button on:click={() => checkBox(pos)}>
			<div class="h-40 w-40 {pos % 2 === 0 ? 'bg-white' : 'bg-black'} grid place-content-center">
				{#if posicion.isTaken}
					{#if posicion.player == 'player'}
						<i class="fa-regular fa-circle text-6xl text-red-600" />
					{:else}
						<i class="fa-solid fa-xmark text-6xl text-red-600" />
					{/if}
				{/if}
			</div>
		</button>
	{/each}
</div>
