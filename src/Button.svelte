<script>
	let button;

	function click(event) {
		let ripple = document.createElement('div');
		ripple.classList.add('ripple');
		let buttonBound = button.getBoundingClientRect();
		ripple.style.left = `${event.clientX - buttonBound.left}px`;
		ripple.style.top = `${event.clientY - buttonBound.top}px`;

		const rippleAnimation = [
			{ opacity: 1, width: '0px', height: '0px'},
			{ opacity: 1},
			{},
			{ opacity: 0, width: '400px', height: '400px',
			left: '-100px', top: '-100px'}
		]
		button.appendChild(ripple);

		ripple.animate(rippleAnimation, 400);

		setTimeout(() => {
			button.removeChild(ripple)
		}, 400);

	}
</script>


<button bind:this={button} on:mousedown={click}>
	<slot></slot>
</button>


<style>
	slot {
		-webkit-user-select: none;
	}
	button {
		user-select: none;
		position: relative;
		border: none;
		cursor: pointer;
		box-shadow: 0px 2px 3px #55555580;
		padding: 20px;
		text-transform: uppercase;
		transition: all 100ms ease;
		border-radius: 4px;
		font-size: 1.2rem;
		background-color: #fff;
		overflow: hidden;
		-webkit-user-select: none;
	}
	button:focus {
		background-color: #ddd; 
	}
	button:hover {
		box-shadow: 0px 4px 3px #55555580;
	}
</style>