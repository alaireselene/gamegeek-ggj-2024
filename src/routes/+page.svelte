<script>
    import { onMount } from 'svelte';
    import { FontAwesomeIcon } from '@fortawesome/svelte-fontawesome'
    import { faDiscord, faFacebookF, faGoogle } from '@fortawesome/free-brands-svg-icons'
    import { faEnvelope, faPhone, faLocationDot, faGraduationCap, faUserGear, faLightbulb, faChessBoard } from '@fortawesome/free-solid-svg-icons'
    import { config, icon } from '@fortawesome/fontawesome-svg-core'
    import '@fortawesome/fontawesome-svg-core/styles.css' // Import the CSS
    config.autoAddCss = false // Tell Font Awesome to skip adding the CSS automatically since it's being imported above
    
    let days = 0;
    let hours = 0;
    let mins = 0;
    let seconds = 0;

    function updateCountdown() {
        const targetTime = new Date("January 26, 2024 00:00:00").getTime();
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

<div class="navbar bg-base-100">
    <div class="navbar-start">
      <a class="btn btn-ghost text-xl" href="https://gamegeek.asia">
        <img src="/gamegeek.png" alt="Gamegeek logo" id="gamegeek-logo"/>
        Global GameJam 2024
      </a>
    </div>
    <div class="navbar-center hidden lg:flex">
      <ul class="menu menu-horizontal px-1">
        <li><a href="https://discord.gg/g3HRdfgGAj" id="discord-link"><FontAwesomeIcon icon={faDiscord}/> Discord Group</a></li>
        <li><a href="https://www.facebook.com/groups/1579337842153530" id="facebook-link"><FontAwesomeIcon icon={faFacebookF}/>Facebook Group</a></li>
      </ul>
    </div>
    <div class="navbar-end">
      <a class="btn bg-orange-400 text-white" href="https://forms.gle/BKAXonRcxGN8QzyX8">Đăng ký ngay</a>
    </div>
</div>
<div class="hero min-h-screen bg-base-200">
    <div class="hero-content text-center">
      <div class="max-w-md space-y-2">
        <img src="/hero-icon.png" alt="Hero text">
        <h1 class="text-3xl font-bold">Global GameJam sẽ bắt đầu sau</h1>

        <div class="flex gap-5 justify-center">
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
        <button class="btn btn-outline btn-warning"><a href="https://calendar.google.com/calendar/render?action=TEMPLATE&dates=20240125%2F20240128&details=-%20H%C3%ACnh%20th%E1%BB%A9c%20l%C3%A0m%20tham%20gia%3A%20Online%20%2B%20Offline%0A-%20Ph%C3%AD%20%C4%91%C4%83ng%20k%C3%BD%20tham%20gia%3A%2050.000%C4%91%2Fng%C6%B0%E1%BB%9Di%20%C3%A1p%20d%E1%BB%A5ng%20cho%20c%C3%A1c%20b%E1%BA%A1n%20tham%20gia%20l%C3%A0m%20game%20offline%0ADiscord%20Group%3A%20https%3A%2F%2Fdiscord.gg%2Fg3HRdfgGAj%0AFacebook%20Group%3A%20https%3A%2F%2Fwww.facebook.com%2Fgroups%2F1579337842153530&location=2QGM%2BPPV%2C%20Ng.%207%20T%C3%B4n%20Th%E1%BA%A5t%20Thuy%E1%BA%BFt%2C%20D%E1%BB%8Bch%20V%E1%BB%8Dng%20H%E1%BA%ADu%2C%20C%E1%BA%A7u%20Gi%E1%BA%A5y%2C%20H%C3%A0%20N%E1%BB%99i%2C%20Vi%E1%BB%87t%20Nam&text=Gamegeek%20Global%20GameJam"><FontAwesomeIcon icon={faGoogle}/> Thêm vào Google Calendar</a></button>
      </div>
    </div>
</div>
<div class="relative isolate overflow-hidden bg-white px-6 py-24 sm:py-32 lg:overflow-visible lg:px-0">
    <div class="absolute inset-0 -z-10 overflow-hidden">
      <svg class="absolute left-[max(50%,25rem)] top-0 h-[64rem] w-[128rem] -translate-x-1/2 stroke-gray-200 [mask-image:radial-gradient(64rem_64rem_at_top,white,transparent)]" aria-hidden="true">
        <defs>
          <pattern id="e813992c-7d03-4cc4-a2bd-151760b470a0" width="200" height="200" x="50%" y="-1" patternUnits="userSpaceOnUse">
            <path d="M100 200V.5M.5 .5H200" fill="none" />
          </pattern>
        </defs>
        <svg x="50%" y="-1" class="overflow-visible fill-gray-50">
          <path d="M-100.5 0h201v201h-201Z M699.5 0h201v201h-201Z M499.5 400h201v201h-201Z M-300.5 600h201v201h-201Z" stroke-width="0" />
        </svg>
        <rect width="100%" height="100%" stroke-width="0" fill="url(#e813992c-7d03-4cc4-a2bd-151760b470a0)" />
      </svg>
    </div>
    <div class="mx-auto grid max-w-2xl grid-cols-1 gap-x-8 gap-y-16 lg:mx-0 lg:max-w-none lg:grid-cols-2 lg:items-start lg:gap-y-10">
      <div class="lg:col-span-2 lg:col-start-1 lg:row-start-1 lg:mx-auto lg:grid lg:w-full lg:max-w-7xl lg:grid-cols-2 lg:gap-x-8 lg:px-8">
        <div class="lg:pr-4">
          <div class="lg:max-w-lg">
            <p class="text-base font-semibold leading-7 text-indigo-600">Thông tin sự kiện</p>
            <h1 class="mt-2 text-3xl font-bold tracking-tight text-gray-900 sm:text-4xl">GAMEGEEK GLOBAL GAMEJAM 2024</h1>
            <p class="mt-6 text-xl leading-8 text-gray-700">Global Game Jam là một cuộc thi thường niên cho các nhà phát triển Game trên toàn thế giới có thể thỏa sức sáng tạo. Với thời gian giới hạn, các Jammers sẽ phải tạo nên một trò chơi mới dựa trên một chủ đề chung.</p>
          </div>
        </div>
      </div>
      <div class="-ml-12 -mt-12 p-12 lg:sticky lg:top-4 lg:col-start-2 lg:row-span-2 lg:row-start-1 lg:overflow-hidden">
        <img class="w-[48rem] max-w-none rounded-xl bg-gray-900 shadow-xl ring-1 ring-gray-400/10 sm:w-[57rem]" src="/event.jpg" alt="">
      </div>
      <div class="lg:col-span-2 lg:col-start-1 lg:row-start-2 lg:mx-auto lg:grid lg:w-full lg:max-w-7xl lg:grid-cols-2 lg:gap-x-8 lg:px-8">
        <div class="lg:pr-4">
          <div class="max-w-xl text-base leading-7 text-gray-700 lg:max-w-lg">
            <p><strong>Thời gian:</strong> 26/01/2024 - 28/01/2024</p>
            <p><strong>Hình thức:</strong> Hybrid (Online + Offline)</p>
            <p><strong>Địa điểm:</strong> Toà nhà NIC Hà Nội - Số 6 ngõ 7 Tôn Thất Thuyết, Dịch Vọng Hậu, Cầu Giấy, Hà Nội</p>
            <p><strong>Phí đăng ký:</strong> 50.000đ/người, áp dụng cho các bạn tham gia làm game offline</p>
            <p><strong>Đối tượng tham gia GameJam:</strong></p>
            <ul role="list" class="mt-2 space-y-2 text-gray-600">
              <li class="flex ml-4 gap-x-2">
                <span><FontAwesomeIcon icon={faGraduationCap}/> <strong class="font-semibold text-gray-900">Sinh viên ngành CNTT, Art, Design, ...</strong> mong muốn thử sức với ngành làm Game</span>
              </li>
              <li class="flex ml-4 gap-x-2">
                <span><FontAwesomeIcon icon={faUserGear}/> <strong class="font-semibold text-gray-900">Người đang làm việc trong ngành Game</strong> mong muốn có sản phẩm mới, sản phẩm nằm ngoài giới hạn bản thân.</span>
              </li>
              <li class="flex ml-4 gap-x-3">
                <span><FontAwesomeIcon icon={faLightbulb} /> <strong class="font-semibold text-gray-900">Nhân sự ngoài ngành</strong> muốn được trải nghiệm và thử sức với việc làm Game đầy thú vị và sáng tạo.</span>
              </li>
              <li class="flex ml-4 gap-x-3">
                <span><FontAwesomeIcon icon={faChessBoard} /> <strong class="font-semibold text-gray-900">Nhân sự yêu thích làm Board Game</strong></span>
              </li>
            </ul>
            <p class="mt-2"><strong>Thông tin liên hệ:</strong></p>
            <ul role="list" class="mt-2 space-y-2 text-gray-600">
              <li class="flex ml-4 gap-x-2">
                <span><FontAwesomeIcon icon={faEnvelope}/> <strong class="font-semibold text-gray-900">Email: </strong> support@gamegeek.asia</span>
              </li>
              <li class="flex ml-4 gap-x-2">
                <span><FontAwesomeIcon icon={faPhone}/> <strong class="font-semibold text-gray-900">Hotline: </strong> 0902.122.120 (Mr. Hải)</span>
              </li>
            </ul>
            <h2 class="mt-16 text-2xl font-bold tracking-tight text-gray-900">Còn chần chờ gì nữa, tham gia ngay Global Game Jam 2024 để thử thách sự sáng tạo của bản thân!</h2>
            
          </div>
        </div>
      </div>
    </div>
  </div>
  
  <footer class="footer p-10 bg-yellow-200 text-gray-600">
    <aside>
      <img src="/logo_big.png" alt="Gamegeek Logo"/>
    </aside> 
    <nav>
      <header class="footer-title text-black">Contact</header> 
      <ul role="list" class="mt-2 space-y-2 text-gray-600">
        <li class="flex ml-4 gap-x-2">
          <span><FontAwesomeIcon icon={faEnvelope}/> <strong class="font-semibold text-gray-900">Email: </strong> <a href="mailto:support@gamegeek.asia">support@gamegeek.asia</a></span>
        </li>
        <li class="flex ml-4 gap-x-2">
          <span><FontAwesomeIcon icon={faPhone}/> <strong class="font-semibold text-gray-900">Hotline: </strong> <a href="tel:0902122120">(+84) 902 122 120</a></span>
        </li>
        <li class="flex ml-4 gap-x-2">
          <span><FontAwesomeIcon icon={faLocationDot}/> <strong class="font-semibold text-gray-900">Location: </strong> <a href="https://maps.app.goo.gl/ZX4HQUruvJcf6xx69">NIC Building, No 6 Lane 7 Ton That Thuyet, Cau Giay, Hanoi</a></span>
        </li>
      </ul>
      <div class="space-y-4">
        <br/>
        <br/>
        <br/>
      </div>
    </nav>
  </footer>