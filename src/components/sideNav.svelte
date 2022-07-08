<script>
	import CircumIcon from '@klarr-agency/circum-icons-svelte';
	let page = [
		{ title: 'Dashboard', url: '', iconName: 'grid_4-2' },
		{ title: 'Product', url: '', iconName: 'shop' },
		{ title: 'Promotion', url: '', iconName: 'shopping_tag' },
		{ title: 'Shipping', url: '', iconName: 'boxes' },
		{ title: 'Settings', url: '', iconName: 'settings' }
	];
</script>

<nav>
	<ul class="sideNavList">
		{#each page as navItem}
			<li class="sideNavList__item">
				<a class="sideNavList__link" href={navItem.url}>
					<CircumIcon color="#fff" name={navItem.iconName} />
					<h3 class="sideNavList__title">{navItem.title}</h3>
				</a>
			</li>
		{/each}
	</ul>
</nav>

<style lang="scss">
	nav {
		width: 100%;
	}
	.sideNavList {
		list-style-type: none;
		padding: 0;
		margin-top: 100px;
		$self: &;
		&__item {
			border: 1px solid #fff;
			border-radius: 12px;
			margin: 12px;
			transition: all 0.25s ease-out;
			&:hover {
				border: 1px solid #384abe;
				#{ $self }__title {
					transition: all 0.25s ease-out;
					color: #384abe;
				}
				:global(svg) {
					transition: all 0.25s ease-out;
					fill: #384abe;
				}
			}
		}
		&__link {
			display: flex;
			align-items: center;
			text-decoration: none;
			padding: 12px;
			color: #fff;
		}
		&__title {
			margin-left: 12px;
			font-family: 'Inter';
			font-size: 16px;
			font-weight: 500;
		}
	}
</style>
