<template>
	<div 
		:class="`${showAside ? 'overlay' : ''}`"
		@click="$emit('listenToggle')"
		>
	</div>
</template>

<script>
export default {
	props: ['showAside']
}
</script>