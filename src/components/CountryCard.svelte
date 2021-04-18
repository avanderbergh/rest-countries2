<script lang="ts">
	export let country: any;
</script>

<a href={`/${country.name}`}>
	<article>
		<img src={country.flag} alt="{country.name} flag" />
		<section>
			<h1>{country.name}</h1>
			<p><strong>Population:</strong> {country.population}</p>
			<p><strong>Region:</strong> {country.region}</p>
			<p><strong>Capital:</strong> {country.capital}</p>
		</section>
	</article>
</a>

<style lang="scss">
	article {
		margin: 1rem;
		background-color: var(--elements);

		border-radius: 1rem;
		overflow: hidden;

		box-shadow: var(--shadow-level-1);

		transition: all 1s;

		img {
			width: 100%;
		}

		section {
			padding: 1rem;
			h1 {
				font-size: 1.2rem;
			}
		}
	}
</style>
