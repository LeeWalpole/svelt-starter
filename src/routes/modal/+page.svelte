<!-- ParentComponent.svelte -->
<script>
	import Modal from '$lib/components/Modal.svelte';

	let activeModal = null;

	function openModal(modalId) {
		activeModal = modalId;
	}

	function closeModal() {
		activeModal = null;
	}
</script>

<button on:click={() => openModal('modal1')}>Open Modal 1</button>
<button on:click={() => openModal('modal2')}>Open Modal 2</button>

{#if activeModal}
	<Modal onClose={closeModal} {activeModal}>
		{#if activeModal === 'modal1'}
			<p>Modal 1 Content...</p>
			<button on:click={closeModal}>Close</button>
		{/if}

		{#if activeModal === 'modal2'}
			<p>Modal 2 Content...</p>
			<button on:click={() => openModal('modal3')}>Open Modal 3</button>
			<button on:click={closeModal}>Close</button>
		{/if}

		{#if activeModal === 'modal3'}
			<p>Modal 3 Content...</p>
			<button on:click={closeModal}>Close Both Modals</button><br />
			<button on:click={() => closeModal('modal') && openModal('modal2')}
				>Close Modal 3 and Open Modal 2</button
			>
		{/if}
	</Modal>
{/if}
