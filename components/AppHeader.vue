<script setup lang="ts">
	const showMenu = ref(false);
</script>

<template>
	<header class="bg-white">
		<nav
			class="mx-auto flex max-w-7xl items-center justify-between p-6 lg:px-8"
			aria-label="Global"
		>
			<div class="flex lg:flex-1">
				<AppLogo />
			</div>
			<div class="flex lg:hidden">
				<button
					@click="showMenu = !showMenu"
					type="button"
					class="-m-2.5 inline-flex items-center justify-center rounded-md p-2.5 text-gray-700"
				>
					<span class="sr-only">Open main menu</span>
					<svg
						class="h-6 w-6"
						fill="none"
						viewBox="0 0 24 24"
						stroke-width="1.5"
						stroke="currentColor"
						aria-hidden="true"
					>
						<path
							stroke-linecap="round"
							stroke-linejoin="round"
							d="M3.75 6.75h16.5M3.75 12h16.5m-16.5 5.25h16.5"
						/>
					</svg>
				</button>
			</div>
			<div class="hidden lg:flex lg:gap-x-12">
				<div class="relative">
					<button
						type="button"
						class="flex items-center gap-x-1 text-sm font-semibold leading-6 text-gray-900"
						aria-expanded="false"
					>
						Product
					</button>
				</div>

				<NuxtLink
					href="#"
					class="text-sm font-semibold leading-6 text-gray-900"
					>Features</NuxtLink
				>
				<NuxtLink
					href="#"
					class="text-sm font-semibold leading-6 text-gray-900"
					>Marketplace</NuxtLink
				>
				<NuxtLink
					href="#"
					class="text-sm font-semibold leading-6 text-gray-900"
					>Company</NuxtLink
				>
			</div>
		</nav>

		<div
			:class="{ hidden: showMenu }"
			class="lg:hidden"
			role="dialog"
			aria-modal="true"
		>
			<div
				class="fixed inset-y-0 right-0 z-10 w-full overflow-y-auto bg-white px-6 py-6 sm:max-w-sm sm:ring-1 sm:ring-gray-900/10"
			>
				<div class="flex items-center justify-between">
					<AppLogo />
					<button
						type="button"
						class="-m-2.5 rounded-md p-2.5 text-gray-700"
						@click="showMenu = !showMenu"
					>
						<span class="sr-only">Close menu</span>
						<svg
							class="h-6 w-6"
							fill="none"
							viewBox="0 0 24 24"
							stroke-width="1.5"
							stroke="currentColor"
							aria-hidden="true"
						>
							<path
								stroke-linecap="round"
								stroke-linejoin="round"
								d="M6 18L18 6M6 6l12 12"
							/>
						</svg>
					</button>
				</div>
				<div class="mt-6 flow-root">
					<div class="-my-6 divide-y divide-gray-500/10">
						<div class="space-y-2 py-6">
							<div class="-mx-3">
								<button
									type="button"
									class="flex w-full items-center justify-between rounded-lg py-2 pl-3 pr-3.5 text-base font-semibold leading-7 text-gray-900 hover:bg-gray-50"
									aria-controls="disclosure-1"
									aria-expanded="false"
								>
									Home
								</button>
							</div>
							<NuxtLink
								to="#"
								class="-mx-3 block rounded-lg px-3 py-2 text-base font-semibold leading-7 text-gray-900 hover:bg-gray-50"
								>Features</NuxtLink
							>
							<NuxtLink
								to="#"
								class="-mx-3 block rounded-lg px-3 py-2 text-base font-semibold leading-7 text-gray-900 hover:bg-gray-50"
								>Marketplace</NuxtLink
							>
							<NuxtLink
								to="#"
								class="-mx-3 block rounded-lg px-3 py-2 text-base font-semibold leading-7 text-gray-900 hover:bg-gray-50"
								>Company</NuxtLink
							>
						</div>
						<div class="py-6">
							<NuxtLink
								to="#"
								class="-mx-3 block rounded-lg px-3 py-2.5 text-base font-semibold leading-7 text-gray-900 hover:bg-gray-50"
							>
								Log in
							</NuxtLink>
						</div>
					</div>
				</div>
			</div>
		</div>
	</header>
</template>
