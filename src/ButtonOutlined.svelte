<script>
	let button;

	function click(event) {
		let ripple = document.createElement('div');
		ripple.classList.add('ripple');
		ripple.style.left = `${event.clientX - button.offsetLeft}px`;
		ripple.style.top = `${event.clientY - button.offsetTop}px`;

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
		border: 2px solid #aaa;
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
</style>