<script>
	import NavBottomLink from './NavBottomLink.svelte';

	import Modal from '$lib/components/Modal.svelte';
</script>

<ul class="flex w-full items-center justify-between">
	<NavBottomLink IconTest="Home" text="home" link="/" />
	<NavBottomLink IconTest="Bell" text="about" link="/about" />
	<NavBottomLink IconTest="Home" text="about" link="#my-modal-2" />

	<Modal
		modalTtle="Modal Title"
		modalText="This is a single block of text"
		modalStyle="modal-link"
		modalID="my-modal-2"
	/>

	<!-- The button to open modal -->
	<label for="my-modal-3" class="btn">open modal</label>
</ul>
<!-- Put this part before </body> tag -->

<!-- Put this part before </body> tag -->
<input type="checkbox" id="my-modal-3" class="modal-toggle" />
<div class="modal">
	<div class="modal-box relative">
		<label for="my-modal-3" class="btn btn-sm btn-circle absolute right-2 top-2">✕</label>
		<h3 class="text-lg font-bold">Congratulations random Internet user!</h3>
		<p class="py-4">
			You've been selected for a chance to get one year of subscription to use Wikipedia for free!
		</p>
	</div>
</div>
