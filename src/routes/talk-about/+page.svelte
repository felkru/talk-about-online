<!-- fun svelte component -->
<script>
	// give back string of time between dates
	function timeBetweenDates(date1, date2) {
		// get total seconds between the times
		var delta = Math.abs(date2 - date1) / 1000;

		// calculate (and subtract) whole days
		var days = Math.floor(delta / 86400);
		delta -= days * 86400;

		// calculate (and subtract) whole hours
		var hours = Math.floor(delta / 3600) % 24;
		delta -= hours * 3600;

		// calculate (and subtract) whole minutes
		var minutes = Math.floor(delta / 60) % 60;
		delta -= minutes * 60;

		// what's left is seconds
		var seconds = Math.round(delta % 60); // in theory the modulus is not required

		return days + ' days, ' + hours + ' hours, ' + minutes + ' minutes, ' + seconds + ' seconds';
	}

	console.log(timeBetweenDates(new Date('2021-01-01T00:00:00.000Z'), new Date()));
</script>

<h1>Hello, World!</h1>
