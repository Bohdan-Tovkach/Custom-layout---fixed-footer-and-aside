<template>
	<div :class="`aside ${showAside ? 'aside-show' : ''}`">
			<div class="nav">
				<ul>
					<li><a href="#section-0">Section 1</a></li>
					<li><a href="#section-1">Section 2</a></li>
					<li><a href="#section-2">Section 3</a></li>
					<li><a href="#section-3">Section 4</a></li>
					<li><a href="#section-4">Section 5</a></li>
				</ul>
			</div>
		</div>
</template>

<script>
export default {
	props: ['showAside']
}
</script>
