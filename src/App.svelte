<script>
	import Button from './Button.svelte';
	import IconButton from './IconButton.svelte';
	import ButtonFlat from './ButtonFlat.svelte';
	import ButtonOutlined from './ButtonOutlined.svelte';
	import IconButtonFlat from './IconButtonFlat.svelte';
	import IconButtonOutlined from './IconButtonOutlined.svelte';
</script>

<section>
	<div>
		<IconButtonFlat src='./add.svg' alt=''/>
		<Button>Play</Button>
		<IconButton src='./chat.svg' alt=''/>
		<ButtonFlat>Open</ButtonFlat>
		<IconButton src='./code.svg' alt=''/>
		<Button>Close</Button>
	</div>

	<div>
		<IconButton src='./crop.svg' alt=''/>
		<Button>Pause</Button>
		<IconButton src='./chat_bubble.svg' alt=''/>
		<Button>Save</Button>
		<IconButtonOutlined src='./http.svg' alt=''/>
		<Button>Reload</Button>
	</div>

	<div>
		<IconButton src='./arrow_forward.svg' alt=''/>
		<ButtonOutlined>Forward</ButtonOutlined>
		<IconButton src='./chat_bubble_outline.svg' alt=''/>
		<Button>Save as</Button>
		<IconButton src='./open_in_browser.svg' alt=''/>
		<Button>Restart</Button>
	</div>
</section>


<section>
	<div>
		<IconButtonFlat src='./add.svg' alt=''/>
		<Button>Play</Button>
		<IconButton src='./chat.svg' alt=''/>
		<ButtonFlat>Open</ButtonFlat>
		<IconButton src='./code.svg' alt=''/>
		<Button>Download</Button>
	</div>

	<div>
		<IconButton src='./crop.svg' alt=''/>
		<Button>Pause</Button>
		<IconButton src='./chat_bubble.svg' alt=''/>
		<Button>Save</Button>
		<IconButtonOutlined src='./http.svg' alt=''/>
		<Button>Reload</Button>
	</div>

	<div>
		<IconButton src='./arrow_forward.svg' alt=''/>
		<ButtonOutlined>Forward</ButtonOutlined>
		<IconButton src='./chat_bubble_outline.svg' alt=''/>
		<Button>Save as</Button>
		<IconButton src='./open_in_browser.svg' alt=''/>
		<Button>Restart</Button>
	</div>
</section>


<section>
	<div>
		<IconButtonFlat src='./add.svg' alt=''/>
		<Button>Play</Button>
		<IconButton src='./chat.svg' alt=''/>
		<ButtonFlat>Open</ButtonFlat>
		<IconButton src='./code.svg' alt=''/>
		<Button>Download</Button>
	</div>

	<div>
		<IconButton src='./crop.svg' alt=''/>
		<Button>Pause</Button>
		<IconButton src='./chat_bubble.svg' alt=''/>
		<Button>Save</Button>
		<IconButtonOutlined src='./http.svg' alt=''/>
		<Button>Reload</Button>
	</div>

	<div>
		<IconButton src='./arrow_forward.svg' alt=''/>
		<ButtonOutlined>Forward</ButtonOutlined>
		<IconButton src='./chat_bubble_outline.svg' alt=''/>
		<Button>Save as</Button>
		<IconButton src='./open_in_browser.svg' alt=''/>
		<Button>Restart</Button>
	</div>
</section>



<style>
	section {
		width: 97vw;
		padding-left: 0.5vw;
		padding-right: 0.5vw;
		height: fit-content;
		display: flex;
		flex-direction: row;
		align-items: center;
		justify-content: space-evenly;
	}
	div {
		width: fit-content;
		height: fit-content;
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: space-evenly;
	}
</style>