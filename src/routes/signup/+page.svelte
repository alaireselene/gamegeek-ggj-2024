<script>
	import { copy } from 'svelte-copy';
	import { FontAwesomeIcon } from '@fortawesome/svelte-fontawesome';
	import { faCircleCheck, faArrowLeft, faArrowRight } from '@fortawesome/free-solid-svg-icons';
	import { config, icon } from '@fortawesome/fontawesome-svg-core';
	import '@fortawesome/fontawesome-svg-core/styles.css'; // Import the CSS
	config.autoAddCss = false; // Tell Font Awesome to skip adding the CSS automatically since it's being imported above
	let cursteps = [1];
	let curstep = 1;
	let link = '';
	let content = '';

	let name = '';
	let phone = '';

	const goBack = () => {
		if (curstep > 1) {
			curstep--;
		}
		if (!cursteps.includes(curstep)) {
			cursteps = [...cursteps, curstep];
		}
	};

	const goNext = () => {
		if (curstep < 2) {
			curstep++;
		}
		if (!cursteps.includes(curstep)) {
			cursteps = [...cursteps, curstep];
		}
		linkGen();
	};
	function removeAccents(str) {
		return str
			.normalize('NFD')
			.replace(/[\u0300-\u036f]/g, '')
			.replace(/đ/g, 'd')
			.replace(/Đ/g, 'D');
	}

	function linkGen() {
		content = 'Gamejam2024 ' + removeAccents(name) + ' ' + phone;
		link =
			'https://img.vietqr.io/image/BIDV-1261407442-qr_only.png?amount=50000&addInfo=' +
			escape(content);
		console.log(link);
	}
</script>

<div>
	<div class="hero min-h-screen">
		<div class="max-h-2xl max-w-2xl space-y-6">
			{#if curstep === 1}
				<div class="step-info card">
					<h2 class="text-3xl font-bold gradient-fill-text">Thông tin người tham gia</h2>
					<label class="form-control w-full max-w-xs">
						<div class="label">
							<span class="label-text">Tên bạn là gì?</span>
						</div>
						<input
							type="text"
							placeholder="Nhập vào đây"
							class="input input-bordered w-full max-w-xs"
							bind:value={name}
						/>
					</label>
					<label class="form-control w-full max-w-xs">
						<div class="label">
							<span class="label-text">Số điện thoại của bạn?</span>
						</div>
						<input
							type="text"
							placeholder="Nhập vào đây"
							class="input input-bordered w-full max-w-xs"
							bind:value={phone}
						/>
					</label>
				</div>
			{:else}
				<div class="step-info">
					<h2 class="text-3xl font-bold gradient-fill-text">
						Thông tin chuyển khoản cho đội Offline/Hybrid
					</h2>
					<div class="mt-4 flex flex-wrap">
						<img class="h-48 ml-4" src={link} alt="" />
						<div class="self-center ml-4">
							<p><strong>Tên tài khoản:</strong> Vũ Minh Hạnh</p>
							<p>
								<strong>Số tài khoản:</strong> 1261407442
								<button use:copy={'1261407442'} class="btn btn-info btn-xs">Sao chép</button>
							</p>
							<p><strong>Ngân hàng:</strong> BIDV</p>
							<p>
								<strong>Nội dung:</strong>
								{content}
								<button use:copy={content} class="btn btn-info btn-xs">Sao chép</button>
							</p>
							<p><strong>Số tiền:</strong> 50000đ</p>
						</div>
					</div>
				</div>
			{/if}
			<div class="flex justify-between gap-2">
				{#if curstep > 1}
					<button class="btn btn-sm btn-outline btn-warning" type="submit" on:click={() => goBack()}
						><FontAwesomeIcon icon={faArrowLeft} />Quay lại
					</button>
				{/if}
				{#if curstep < 2}
					<button class="btn btn-sm btn-info" type="submit" on:click={() => goNext()}
						>Kế tiếp <FontAwesomeIcon icon={faArrowRight} />
					</button>
				{/if}
				{#if curstep === 2}
					<button class="btn btn-sm btn-success"
						><a href="https://forms.gle/BKAXonRcxGN8QzyX8"
							>Hoàn tất bước cuối <FontAwesomeIcon icon={faCircleCheck} /></a
						>
					</button>
				{/if}
			</div>
		</div>
	</div>
</div>
