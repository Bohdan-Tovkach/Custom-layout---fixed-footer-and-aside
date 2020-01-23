<template>
	<div class="content">
		<section 
			v-for="(item, i) in Data"
			:key="i"
			:id="`section-${i}`"
			>
			<h2>{{ item.header }}</h2>
			<p>
				{{ item.text }}
			</p>
		</section>
	</div>
</template>

<script>
import { data } from '../data'
export default {
	data: () => ({
		Data: data,
	})
}
</script>