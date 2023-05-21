<script>
	import NavLeftLink from './NavLeftLink.svelte';
	import Modal from '$lib/components/Modal.svelte';
</script>

<div class=" mx-auto flex-col justify-center gap-3.5 p-3.5 text-center align-middle tablet:flex">
	<img
		src="https://www.flames.agency/wp-content/uploads/flames-agency-icon-large.png"
		alt=""
		height={44}
		width={44}
		class="mx-auto desktop:mx-0"
	/>
	<NavLeftLink IconTest="Home" text="home" link="/" />

	<NavLeftLink IconTest="Bell" text="about" link="/about" />

	<NavLeftLink IconTest="Home" text="about" link="#my-modal-2" />

	<Modal
		modalTtle="Modal Title"
		modalText="This is a single block of text"
		modalStyle="modal-link"
		modalID="my-modal-2"
	/>

	<label for="my-modal-4" class="btn">open modal</label>

	<Modal
		modalTtle="Modal Title"
		modalText="This is a single block of text"
		modalStyle="modal-bottom"
		modalID="my-modal-4"
	/>
</div>
