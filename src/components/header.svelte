<script>
	import CircumIcon from '@klarr-agency/circum-icons-svelte';
	let option = [
		{ aria: 'notification', iconName: 'bell_on' },
		{ aria: 'chat', iconName: 'chat_1' },
		{ aria: 'profil', iconName: 'user' }
	];
</script>

<header>
	<ul class="headerNavList">
		{#each option as item}
			<li class="headerNavList__item">
				<button class="headerNavList__button" aria-label={item.aria}>
					<CircumIcon color="#fff" name={item.iconName} />
				</button>
			</li>
		{/each}
	</ul>
</header>

<style lang="scss">
	header {
		display: flex;
		justify-content: flex-end;
		grid-area: header;
		margin: 24px;
	}
	.headerNavList {
		display: flex;
		text-decoration: none;
		margin: 0;
		padding: 0;
		&__item {
			margin: 0 12px;
		}
		&__button {
			cursor: pointer;
			background-color: transparent;
			border: none;
			:global(svg:hover) {
				transition: all 0.25s ease-out;
				fill: #384abe;
			}
		}
	}
</style>
