<script>
	import { FontAwesomeIcon } from '@fortawesome/svelte-fontawesome';
	import { faEnvelope, faPhone, faLocationDot } from '@fortawesome/free-solid-svg-icons';
	import { config, icon } from '@fortawesome/fontawesome-svg-core';
	import '@fortawesome/fontawesome-svg-core/styles.css'; // Import the CSS
	config.autoAddCss = false; // Tell Font Awesome to skip adding the CSS automatically since it's being imported above
</script>

<footer class="footer p-10 bg-yellow-200 text-gray-600">
	<aside>
		<img src="/logo_big.png" alt="Gamegeek Logo" />
	</aside>
	<nav>
		<header class="footer-title text-black">Contact</header>
		<ul role="list" class="mt-2 space-y-2 text-gray-600">
			<li class="flex ml-4 gap-x-2">
				<span
					><FontAwesomeIcon icon={faEnvelope} />
					<strong class="font-semibold text-gray-900">Email: </strong>
					<a href="mailto:support@gamegeek.asia">support@gamegeek.asia</a></span
				>
			</li>
			<li class="flex ml-4 gap-x-2">
				<span
					><FontAwesomeIcon icon={faPhone} />
					<strong class="font-semibold text-gray-900">Hotline: </strong>
					<a href="tel:0902122120">(+84) 902 122 120</a></span
				>
			</li>
			<li class="flex ml-4 gap-x-2">
				<span
					><FontAwesomeIcon icon={faLocationDot} />
					<strong class="font-semibold text-gray-900">Location: </strong>
					<a href="https://maps.app.goo.gl/ZX4HQUruvJcf6xx69"
						>NIC Building, No 6 Lane 7 Ton That Thuyet, Cau Giay, Hanoi</a
					></span
				>
			</li>
		</ul>
		<div class="space-y-4">
			<br />
			<br />
			<br />
		</div>
	</nav>
</footer>
