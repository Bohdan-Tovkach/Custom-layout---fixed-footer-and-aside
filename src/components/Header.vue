<template>
	<div class="header">
		<span>Header</span>
		<span class="toggle-nav__wrapper">
			<button 
				@click="$emit('listenToggle')" 
				class="toggle-nav"
				>Ok
			</button>
		</span>
	</div>
</template>