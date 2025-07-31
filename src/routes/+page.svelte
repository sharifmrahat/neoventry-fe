<script lang="ts">
	import * as Tabs from '$lib/components/ui/tabs/index.js';
	import { setLocale } from '$lib/paraglide/runtime';
	import { m } from '$lib/paraglide/messages.js';
</script>

<main class="flex h-[100vh] w-full flex-col justify-between">
	<header class="flex items-center justify-between bg-sky-700 px-5 py-4 text-white">
		<div>
			<h1 class="text-base font-semibold text-white lg:text-4xl">NEOVENTRY</h1>
		</div>
		<div>
			<div class="flex w-full max-w-sm flex-col gap-6">
				<Tabs.Root value="account">
					<Tabs.List>
						<Tabs.Trigger value="account" onclick={() => setLocale('en')}>EN</Tabs.Trigger>
						<Tabs.Trigger value="password" onclick={() => setLocale('bn')}>BN</Tabs.Trigger>
					</Tabs.List>
				</Tabs.Root>
			</div>
		</div>
	</header>

	<div class="my-20 px-4 text-center text-2xl font-semibold lg:px-16">
		<h1>{m.hello_world({ name: 'SvelteKit User' })}</h1>
		<p>{m.t1()}</p>
		<p>{m.t2()}</p>
	</div>

	<footer class="flex flex-col justify-end">All Right reserved.</footer>
</main>
