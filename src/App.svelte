<script>
	import Card from "./components/Card.svelte"

	let cars = [
		{
			type: "Sedans",
			description: "Choose a sedan for its affordability and excellent fuel economy. Ideal for cruising in the city or on your next road trip.",
			icon: "/images/icon-sedans.svg",
			color: "hsl(31, 77%, 52%)"
		},
		{
			type: "Suvs",
			description: "Take an SUV for its spacious interior, power, and versatility. Perfect for your next family vacation and off-road adventures.",
			icon: "/images/icon-suvs.svg",
			color: "hsl(184, 100%, 22%)"
		},
		{
			type: "Luxury",
			description: "Cruise in the best car brands without the bloated prices. Enjoy the enhanced comfort of a luxury rental and arrive in style.",
			icon: "/images/icon-luxury.svg",
			color: "hsl(179, 100%, 13%)"
		}
	]
</script>

<main class="wrapper">
	<h1></h1>
	{#each cars as car, i}
		<Card
			carIcon={car.icon}
			carType={car.type}
			carDescription={car.description}
			color={car.color}
			index={i} />
	{/each}
</main>

<style lang="scss">
	@media screen and (min-width: 768px) {
		.wrapper {
			display: flex;
			padding: 15rem 25rem;
		}
	}
</style>