<script>
    export let src;
    export let alt;

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
            { opacity: 0, width: '200px', height: '200px',
            left: '-50px', top: '-50px'}
        ]
        button.appendChild(ripple);

        ripple.animate(rippleAnimation, 300);

        setTimeout(() => {
            button.removeChild(ripple)
        }, 300);

    }

</script>

<button on:mousedown={click} bind:this={button}>
    <img src={src} alt={alt}>
</button>



<style>
    :global(.ripple) {
        position: absolute;
        width: 0px;
        height: 0px;
        border-radius: 50%;
        background-color: #22222280;
        transition: 200ms ease cubic-bezier(0.4, 0, 0.2, 1);
        z-index: 0;
    }
	img {
		width: 40px;
		height: 40px;
        z-index: 1;
        user-select: none;
        -webkit-user-drag: none;
		-webkit-user-select: none;
	}
	button {
        user-select: none;
        position: relative;
		width: 80px;
		height: 80px;
		border: none;
		cursor: pointer;
		padding: 20px;
		text-transform: uppercase;
		transition: all 100ms ease;
		border-radius: 50%;
		border: 2px solid #aaa;
		background-color: #fff;
		display: flex;
		align-items: center;
		justify-content: center;
        overflow: hidden;
		-webkit-user-select: none;
	}
	button:focus {
        background-color: #ddd; 
	}
</style>