<template>
	<nav class="level">
		<div class="level-item">
			<div>
				<h1 class="title is-size-4-mobile">Top Rated Games</h1>
				<h2 class="subtitle content is-size-6-mobile">
				  <ol>
				    <li v-for="game in ranked" :key="game.id">
				    	<router-link :to="{name: 'Game', params: { id: game.id }}">
								<b-tooltip :label="game.synopsis" type="is-light" position="is-bottom" size="is-large" multilined animated>
									{{ game.title }}
								</b-tooltip>
							</router-link>
			    	</li>
				  </ol>
				</h2>
			</div>
		</div>
		<div class="level-item">
			<div>
				<h1 class="title is-size-4-mobile">Most Popular Games</h1>
				<h2 class="subtitle content is-size-6-mobile">
				  <ol>
				    <li v-for="game in popular" :key="game.id">
				    	<router-link :to="{name: 'Game', params: { id: game.id }}">
								<b-tooltip :label="game.synopsis" type="is-light" position="is-bottom" size="is-large" multilined animated>
									{{ game.title }}
								</b-tooltip>
							</router-link>
				    </li>
				  </ol>
				</h2>
			</div>
		</div>
	</nav>
</template>

<script>
export default {
    props: ['ranked', 'popular']
}
</script>