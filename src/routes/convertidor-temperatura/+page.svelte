<script lang="ts">
	class Temperatura {
		#celsius = $state(0);
		#fahrenheit = $state(0);

		get celsius() {
			return this.#celsius;
		}
		set celsius(valor: number) {
			this.#celsius = valor;
			this.#fahrenheit = (this.#celsius * 9) / 5 + 32;
		}

		get fahrenheit() {
			return this.#fahrenheit;
		}
		set fahrenheit(valor: number) {
			this.#fahrenheit = valor;
			this.#celsius = ((this.#fahrenheit - 32) * 9) / 5;
		}
	}

	const temperatura = new Temperatura();
</script>

<fieldset role="group">
	<input type="number" bind:value={temperatura.celsius} /> celsius =
	<input type="number" bind:value={temperatura.fahrenheit} /> fahrenheit
</fieldset>
