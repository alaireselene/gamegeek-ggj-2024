<script>
	import { onMount } from 'svelte';
	import { FontAwesomeIcon } from '@fortawesome/svelte-fontawesome';
	import { faGoogle } from '@fortawesome/free-brands-svg-icons';
	import {
		faEnvelope,
		faPhone,
		faGraduationCap,
		faUserGear,
		faLightbulb,
		faChessBoard,
		faCube,
		faChevronDown,
		faRightToBracket,
		faPeopleArrows,
		faGears,
		faHandHoldingHeart
	} from '@fortawesome/free-solid-svg-icons';
	import { config, icon } from '@fortawesome/fontawesome-svg-core';
	import '@fortawesome/fontawesome-svg-core/styles.css'; // Import the CSS
	config.autoAddCss = false; // Tell Font Awesome to skip adding the CSS automatically since it's being imported above

	let days = 0;
	let hours = 0;
	let mins = 0;
	let seconds = 0;

	function updateCountdown() {
		const targetTime = new Date('January 26, 2024 00:00:00').getTime();
		const currentTime = new Date();
		const totalSeconds = (targetTime - currentTime) / 1000;

		days = Math.floor(totalSeconds / 3600 / 24);
		hours = Math.floor(totalSeconds / 3600) % 24;
		mins = Math.floor(totalSeconds / 60) % 60;
		seconds = Math.floor(totalSeconds) % 60;
	}

	onMount(() => {
		updateCountdown();
		setInterval(updateCountdown, 1000);
	});
</script>

<svg version="1.1" xmlns="http://www.w3.org/2000/svg" class="svg-settings">
	<defs>
		<linearGradient id="linear">
			<stop class="stop-color-1" offset="0%"></stop>
			<stop class="stop-color-2" offset="100%"></stop>
			<stop class="stop-color-3" offset="100%"></stop>
		</linearGradient>
	</defs>
</svg>

<div class="hero min-h-screen bg-base-200">
	<div class="hero-content flex-col lg:flex-row-reverse">
		<img class="hero-image" src="/image.png" alt="Hero text" />
		<div class="space-y-2">
			<h1 class="text-3xl font-bold">Global GameJam</h1>
			<h2 class="text-7xl font-bold gradient-fill-text hover:animate-fade">Vietnam 2024</h2>
			<p>
				Global Game Jam là một cuộc thi thường niên cho các nhà phát triển Game trên toàn thế giới
				có thể thỏa sức sáng tạo. Với thời gian giới hạn, các Jammers sẽ phải tạo nên một trò chơi
				mới dựa trên một chủ đề chung.
			</p>
			<br />
			<br />
			<h1 class="text-xl">Diễn ra sau</h1>
			<div class="flex gap-5">
				<div>
					<span class="countdown font-mono text-4xl">
						<span style="--value:{days};"></span>
					</span>
					ngày
				</div>
				<div>
					<span class="countdown font-mono text-4xl">
						<span style="--value:{hours};"></span>
					</span>
					giờ
				</div>
				<div>
					<span class="countdown font-mono text-4xl">
						<span style="--value:{mins};"></span>
					</span>
					phút
				</div>
				<div>
					<span class="countdown font-mono text-4xl">
						<span style="--value:{seconds};"></span>
					</span>
					giây
				</div>
			</div>
			<div class="flex gap-5">
				<button class="btn btn-outline btn-warning"
					><a
						href="https://calendar.google.com/calendar/render?action=TEMPLATE&dates=20240125%2F20240128&details=-%20H%C3%ACnh%20th%E1%BB%A9c%20l%C3%A0m%20tham%20gia%3A%20Online%20%2B%20Offline%0A-%20Ph%C3%AD%20%C4%91%C4%83ng%20k%C3%BD%20tham%20gia%3A%2050.000%C4%91%2Fng%C6%B0%E1%BB%9Di%20%C3%A1p%20d%E1%BB%A5ng%20cho%20c%C3%A1c%20b%E1%BA%A1n%20tham%20gia%20l%C3%A0m%20game%20offline%0ADiscord%20Group%3A%20https%3A%2F%2Fdiscord.gg%2Fg3HRdfgGAj%0AFacebook%20Group%3A%20https%3A%2F%2Fwww.facebook.com%2Fgroups%2F1579337842153530&location=2QGM%2BPPV%2C%20Ng.%207%20T%C3%B4n%20Th%E1%BA%A5t%20Thuy%E1%BA%BFt%2C%20D%E1%BB%8Bch%20V%E1%BB%8Dng%20H%E1%BA%ADu%2C%20C%E1%BA%A7u%20Gi%E1%BA%A5y%2C%20H%C3%A0%20N%E1%BB%99i%2C%20Vi%E1%BB%87t%20Nam&text=Gamegeek%20Global%20GameJam"
						><FontAwesomeIcon icon={faGoogle} /> Thêm vào Google Calendar</a
					></button
				>
				<button class="btn btn-warning"
					><a href="/signup"><FontAwesomeIcon icon={faRightToBracket} /> ĐĂNG KÝ THAM GIA</a
					></button
				>
			</div>
			<br />
			<div class="inline-flex">
				<svg class="animate-bounce w-6 h-6 fill-gradient-linear">
					<FontAwesomeIcon icon={faChevronDown} />
				</svg>
				<h2 class="gradient-fill-text font-bold text-xl">Xem thêm</h2>
			</div>
		</div>
	</div>
</div>

<div
	class="relative isolate overflow-hidden bg-base-200 px-6 py-24 sm:py-32 lg:overflow-visible lg:px-0"
>
	<div class="absolute inset-0 -z-10 overflow-hidden">
		<svg
			class="absolute left-[max(50%,25rem)] top-0 h-[64rem] w-[128rem] -translate-x-1/2 stroke-gray-200 [mask-image:radial-gradient(64rem_64rem_at_top,white,transparent)]"
			aria-hidden="true"
		>
			<defs>
				<pattern
					id="e813992c-7d03-4cc4-a2bd-151760b470a0"
					width="200"
					height="200"
					x="50%"
					y="-1"
					patternUnits="userSpaceOnUse"
				>
					<path d="M100 200V.5M.5 .5H200" fill="none" />
				</pattern>
			</defs>
			<svg x="50%" y="-1" class="overflow-visible fill-gray-50">
				<path
					d="M-100.5 0h201v201h-201Z M699.5 0h201v201h-201Z M499.5 400h201v201h-201Z M-300.5 600h201v201h-201Z"
					stroke-width="0"
				/>
			</svg>
			<rect
				width="100%"
				height="100%"
				stroke-width="0"
				fill="url(#e813992c-7d03-4cc4-a2bd-151760b470a0)"
			/>
		</svg>
	</div>
	<div
		class="mx-auto grid max-w-2xl grid-cols-1 gap-x-8 gap-y-16 lg:mx-0 lg:max-w-none lg:grid-cols-2 lg:items-start lg:gap-y-10"
	>
		<div
			class="lg:col-span-2 lg:col-start-1 lg:row-start-1 lg:mx-auto lg:grid lg:w-full lg:max-w-7xl lg:grid-cols-2 lg:gap-x-8 lg:px-8"
		>
			<div class="lg:pr-4">
				<div class="lg:max-w-lg">
					<h1
						class="mt-2 text-3xl font-bold tracking-tight gradient-fill-text sm:text-4xl text-center"
					>
						THÔNG TIN GAME JAM
					</h1>
					<br />
					<div class="lg:pr-4">
						<div class="max-w-xl text-base leading-7 text-white lg:max-w-lg">
							<p><strong>Thời gian:</strong> 26/01/2024 - 28/01/2024</p>
							<p><strong>Hình thức:</strong> Hybrid (Online + Offline)</p>
							<p>
								<strong>Địa điểm:</strong> 
                                                               <strong>Tại Hà Nội:</strong>  Toà nhà NIC Hà Nội - Số 6 ngõ 7 Tôn Thất Thuyết, Dịch Vọng Hậu, Cầu Giấy, Hà Nội
                                                        </p>
                                                        <p>
                                                               <strong>Tại TP HCM:</strong>  Board Game Era, 13 đường số 7, Cư xá Đô Thành, Phường 4, Quận 3, TP HCM
							</p>
                                                       
						</div>
					</div>
					<br />
					<br />
					<h1
						class="mt-2 text-3xl font-bold tracking-tight gradient-fill-text sm:text-4xl text-center"
					>
						LỊCH THI ĐẤU
					</h1>
					<br />
					<ul class="timeline timeline-snap-icon max-md:timeline-compact timeline-vertical">
						<li>
							<div class="timeline-middle">
								<FontAwesomeIcon icon={faCube} />
							</div>
							<div class="timeline-start md:text-end mb-10">
								<time class="font-mono">19:30, 26/01/2024</time>
								<div class="text-lg font-black text-orange-300">Khai mạc</div>
							</div>
							<hr class="bg-orange-400" />
						</li>
						<li>
							<hr class="bg-orange-400" />
							<div class="timeline-middle">
								<div class="timeline-middle">
									<FontAwesomeIcon icon={faCube} />
								</div>
							</div>
							<div class="timeline-end mb-10">
								<time class="font-mono">20:00, 26/01/2024</time>
								<div class="text-lg font-black text-orange-300">GameJam</div>
								Giới hạn thời gian<strong>36 tiếng</strong> cho các Jammers thỏa sức sáng tạo.
							</div>
							<hr class="bg-orange-400" />
						</li>
						<li>
							<hr class="bg-orange-400" />
							<div class="timeline-middle">
								<FontAwesomeIcon icon={faCube} />
							</div>
							<div class="timeline-start md:text-end mb-10">
								<time class="font-mono">08:00, 28/01/2024</time>
								<div class="text-lg font-black text-orange-300">Pitching</div>
							</div>
							<hr class="bg-orange-400" />
						</li>
						<li>
							<hr class="bg-orange-400" />
							<div class="timeline-middle">
								<FontAwesomeIcon icon={faCube} />
							</div>
							<div class="timeline-end md:text-end mb-10">
								<time class="font-mono">10:30, 28/01/2024</time>
								<div class="text-lg font-black text-orange-300">Bế mạc</div>
							</div>
						</li>
					</ul>
					<br />
				</div>
			</div>
		</div>
		<div
			class="-ml-12 -mt-12 p-12 lg:sticky lg:top-4 lg:col-start-2 lg:row-span-2 lg:row-start-1 lg:overflow-hidden"
		>
			<img
				class="w-[48rem] max-w-none rounded-xl bg-gray-900 shadow-xl ring-1 ring-gray-400/10 sm:w-[57rem]"
				src="/event.jpg"
				alt=""
			/>
		</div>
	</div>
</div>
<div class="px-8 py-8 bg-base-200">
	<h1 class="text-3xl font-bold text-center gradient-fill-text">
		Tại sao không nên bở lỡ<br /> Global Game Jam 2024
	</h1>
	<div class="flex flex-col md:flex-row justify-center items-center gap-1 md:gap-10">
		<div class="card w-96 hover:bg-orange-400 shadow-xl">
			<div class="card-body">
				<FontAwesomeIcon
					icon={faPeopleArrows}
					class="text-3xl fill-gradient-linear hover:fill-white"
				/>
				<h2 class="text-center font-bold text-white text-xl">KẾT NỐI</h2>
				<p class="text-center text-white">
					Gặp gỡ và kết nối với những người cùng chung sở thích, mở rộng kiến thức và kỹ năng về
					game.
				</p>
			</div>
		</div>
		<div class="card w-96 hover:bg-orange-400 shadow-xl">
			<div class="card-body">
				<FontAwesomeIcon icon={faGears} class="text-3xl fill-gradient-linear hover:fill-white" />
				<h2 class="text-center font-bold text-white text-xl">THỬ SỨC</h2>
				<p class="text-center text-white">
					Thử sức với việc lập trình và thiết kế Game, nâng cao kỹ nẵng chuyên môn
				</p>
			</div>
		</div>
		<div class="card w-96 hover:bg-orange-400 shadow-xl">
			<div class="card-body">
				<FontAwesomeIcon
					icon={faHandHoldingHeart}
					class="text-3xl fill-gradient-linear hover:fill-white"
				/>
				<h2 class="text-center font-bold text-white text-xl">QUÀ TẶNG</h2>
				<p class="text-center text-white">
					Nhận quà tặng hấp dẫn và hỗ trợ để thương mại hóa sản phẩm game, giúp bạn tiếp cận người
					chơi trên toàn cầu.
				</p>
			</div>
		</div>
	</div>
</div>
<div class="flex flex-col md:flex-row-reverse justify-between px-28 bg-base-200">
	<div
		class="w-full md:max-w-xl grid place-items-center bg-brand-gradient-section rounded-2xl md:rounded-3xl"
	>
		<div class="mx-4 my-2 md:m-12">
			<img src="IMG_0249.JPG" alt="" class="shadow-img rounded-lg" />
		</div>
	</div>
	<div class="px-8 py-8 self-center">
		<h1 class="gradient-fill-text text-4xl font-bold">Game Jam đặc biệt phù hợp với</h1>
		<ul role="list" class="mt-8 space-y-4">
			<li class="flex ml-8 gap-x-2">
				<span
					><FontAwesomeIcon icon={faGraduationCap} />
					<strong class="font-semibold">Sinh viên ngành CNTT, Art, Design, ...</strong> mong muốn thử
					sức với ngành làm Game</span
				>
			</li>
			<li class="flex ml-8 gap-x-2">
				<span
					><FontAwesomeIcon icon={faUserGear} />
					<strong class="font-semibold">Người đang làm việc trong ngành Game</strong> mong muốn có sản
					phẩm mới, sản phẩm nằm ngoài giới hạn bản thân.</span
				>
			</li>
			<li class="flex ml-8 gap-x-3">
				<span
					><FontAwesomeIcon icon={faLightbulb} />
					<strong class="font-semibold">Nhân sự ngoài ngành</strong> muốn được trải nghiệm và thử sức
					với việc làm Game đầy thú vị và sáng tạo.</span
				>
			</li>
			<li class="flex ml-8 gap-x-3">
				<span
					><FontAwesomeIcon icon={faChessBoard} />
					<strong class="font-semibold">Nhân sự yêu thích làm Board Game</strong></span
				>
			</li>
		</ul>
	</div>
</div>
<div class="px-20 py-8 bg-base-200 max-h-30">
	<h1 class="text-4xl font-bold text-center pb-4 gradient-fill-text">Cơ cấu giải thưởng</h1>
	<div class="flex flex-wrap gap-4 items-stretch place-items-center justify-center">
		<div class="card md:w-96 w-52 bg-base-100 shadow-xl image-full">
			<figure>
				<img class="w-full" src="/digital-game.jfif" alt="" />
			</figure>
			<div class="card-body self-center">
				<h2 class="card-title font-semibold text-orange-200">Hạng mục DIGITAL GAME</h2>
				<ul>
					<li>1 Giải nhất: 5.000.000đ</li>
					<li>1 Giải nhì: 3.000.000đ</li>
					<li>2 Giải ba: 1.500.000đ</li>
				</ul>
			</div>
		</div>
		<div class="card md:w-96 w-52 bg-base-100 shadow-xl image-full">
			<figure>
				<img class="w-full" src="/board-game.jfif" alt="" />
			</figure>
			<div class="card-body self-center">
				<h2 class="card-title font-semibold text-orange-200">Hạng mục BOARD GAME</h2>
				<ul>
					<li>1 Giải nhất: 5.000.000đ</li>
					<li>1 Giải nhì: 3.000.000đ</li>
					<li>2 Giải ba: 1.500.000đ</li>
				</ul>
			</div>
		</div>
		<div class="card md:w-96 w-52 bg-base-100 shadow-xl image-full">
			<figure>
				<img class="w-full" src="/voting.jfif" alt="" />
			</figure>
			<div class="card-body self-center">
				<h2 class="card-title font-semibold text-orange-200">Giải bình chọn</h2>
				<ul>
					<li>1.500.000đ</li>
				</ul>
			</div>
		</div>
	</div>
</div>
