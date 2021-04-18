<script context="module">
	/**
	 * @type {import('@sveltejs/kit').Load}
	 */
	export async function load({ page, fetch, session, context }) {
		const url = `https://restcountries.eu/rest/v2/name/${page.params.name}`;
		const res = await fetch(url);

		if (res.ok) {
			const countries = await res.json();
			const country = countries[0];
			return {
				props: {
					country
				}
			};
		}

		return {
			status: res.status,
			error: new Error(`Could not load ${url}`)
		};
	}
</script>

<script>
	export let country;
	console.log(country);
</script>

{country.name}
