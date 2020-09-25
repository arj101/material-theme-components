<script>
	import Button from './Button.svelte';
	import IconButton from './IconButton.svelte';
</script>

<div>
	<IconButton src='./add.svg' alt=''/>
	<IconButton src='./crop.svg' alt=''/>
	<IconButton src='./arrow_forward.svg' alt=''/>
</div>

<div>
	<Button>Play</Button>
	<Button>Pause</Button>
	<Button>Forward</Button>
</div>

<div>
	<IconButton src='./chat.svg' alt=''/>
	<IconButton src='./chat_bubble.svg' alt=''/>
	<IconButton src='./chat_bubble_outline.svg' alt=''/>
</div>

<div>
	<Button>Open</Button>
	<Button>Save</Button>
	<Button>Save as</Button>
</div>

<div>
	<IconButton src='./code.svg' alt=''/>
	<IconButton src='./http.svg' alt=''/>
	<IconButton src='./open_in_browser.svg' alt=''/>
</div>


<div>
	<Button>Download</Button>
	<Button>Reload</Button>
	<Button>Restart</Button>
</div>

<style>
	div {
		width: 97vw;
		padding-left: 0.5vw;
		padding-right: 0.5vw;
		height: fit-content;
		display: flex;
		flex-direction: row;
		align-items: center;
		justify-content: space-around;
	}
</style>