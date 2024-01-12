<script>
	import { FontAwesomeIcon } from '@fortawesome/svelte-fontawesome';
	import { faDiscord, faFacebookF, faGoogle } from '@fortawesome/free-brands-svg-icons';
	import { config, icon } from '@fortawesome/fontawesome-svg-core';
	import '@fortawesome/fontawesome-svg-core/styles.css'; // Import the CSS
	config.autoAddCss = false; // Tell Font Awesome to skip adding the CSS automatically since it's being imported above
</script>

<div class="navbar bg-base-100">
	<div class="navbar-start">
		<a class="btn btn-ghost text-xl" href="/">
			<img src="/gamegeek.png" alt="Gamegeek logo" id="gamegeek-logo" />
			Global GameJam 2024
		</a>
	</div>
	<div class="navbar-center hidden lg:flex">
		<ul class="menu menu-horizontal px-1">
			<li>
				<a href="https://discord.gg/g3HRdfgGAj" id="discord-link"
					><FontAwesomeIcon icon={faDiscord} /> Discord Group</a
				>
			</li>
			<li>
				<a href="https://www.facebook.com/groups/1579337842153530" id="facebook-link"
					><FontAwesomeIcon icon={faFacebookF} />Facebook Group</a
				>
			</li>
		</ul>
	</div>
	<div class="navbar-end">
		<a class="btn bg-orange-400 text-white" href="/signup">Đăng ký ngay</a>
	</div>
</div>
