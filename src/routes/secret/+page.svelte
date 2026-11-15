<script lang="ts">
	import { SMART_LINK_TWO, BRAND_NAME } from '../../lib/config';
</script>

<svelte:head>
	<title>The Secret Everyone Is Talking About — {BRAND_NAME}</title>
	<meta
		name="description"
		content="You'll see why in 10 seconds. Tap below to reveal the secret."
	/>
</svelte:head>

<main class="dot-bg min-h-screen">
	<!-- HERO SECTION -->
	<section class="relative flex min-h-[85vh] flex-col items-center justify-center px-6 py-12 text-center">
		<!-- radial purple glow (Updated to purple) -->
		<div class="pointer-events-none absolute inset-0 -z-10" style="background: radial-gradient(60% 50% at 50% 40%, rgba(139,92,246,0.18) 0%, rgba(11,15,20,0) 70%);"></div>

		<!-- pill -->
		<span class="mb-6 inline-flex items-center gap-2 rounded-full border border-purple-accent/30 bg-purple-soft px-4 py-1.5 text-xs font-medium text-purple-accent">
			<span class="h-1.5 w-1.5 rounded-full bg-purple-accent"></span>
			Exclusive Access
		</span>

		<!-- headline -->
		<h1 class="max-w-xl text-4xl font-bold tracking-tight text-white sm:text-5xl">
			The Link Everyone Is <span class="text-purple-accent">Whispering About</span>
		</h1>

		<!-- subheadline -->
		<p class="mt-4 max-w-sm text-base text-muted sm:text-lg">
			You'll see why in 10 seconds. Tap below to reveal the secret.
		</p>

		<!-- CTA (One-click) -->
		<a href={SMART_LINK_TWO} rel="external"
			class="cta-glow-purple cta-pulse mt-10 flex w-full max-w-sm items-center justify-center gap-2 rounded-2xl bg-purple-accent px-8 py-4 text-lg font-semibold text-white transition hover:brightness-110">
			Reveal The Secret →
		</a>

		<p class="mt-4 text-xs text-muted">100% Free · Takes 10 Seconds</p>
	</section>

	<!-- HOW IT WORKS (Updated for Mystery) -->
	<section class="mx-auto max-w-2xl px-6 pb-14">
		<div class="grid gap-4 sm:grid-cols-3">
			{#each [{ n: '1', t: 'Tap the button', d: 'One tap to open the link.' }, { n: '2', t: 'See what it is', d: 'Find out what everyone is talking about.' }, { n: '3', t: 'Decide for yourself', d: 'No strings attached.' }] as step (step.n)}
				<div class="rounded-2xl border border-white/5 bg-surface p-5 text-left">
					<div
						class="mb-3 flex h-9 w-9 items-center justify-center rounded-full bg-purple-soft text-sm font-bold text-purple-accent"
					>
						{step.n}
					</div>
					<h3 class="text-sm font-semibold text-white">{step.t}</h3>
					<p class="mt-1 text-xs text-muted">{step.d}</p>
				</div>
			{/each}
		</div>

		<!-- TRUST ROW -->
		<div class="mt-8 flex flex-wrap items-center justify-center gap-x-6 gap-y-3 text-xs text-muted">
			<span>🔒 100% Secure</span>
			<span>👀 100% Anonymous</span>
			<span>✓ No Payment</span>
		</div>

		<!-- REPEAT CTA -->
		<div class="mt-10 text-center">
			<a href={SMART_LINK_TWO} rel="external" class="cta-glow-purple inline-flex w-full max-w-sm items-center justify-center rounded-2xl bg-purple-accent px-8 py-4 text-lg font-semibold text-white transition hover:brightness-110">
				Reveal The Secret →
			</a>
		</div>
	</section>

	<!-- FAQ (Updated for Curiosity) -->
	<section class="mx-auto max-w-xl px-6 pb-14">
		<h2 class="mb-6 text-center text-xl font-semibold text-white">Quick questions</h2>
		<div class="space-y-3">
			{#each [{ q: 'What exactly is it?', a: 'You will see the full details as soon as you tap the button.' }, { q: 'Why is it a secret?', a: 'Because the platform wants to reward early adopters before it goes mainstream.' }, { q: 'Is it safe?', a: 'Yes, it is completely secure and 100% free to check out.' }] as item (item.q)}
				<details
					class="group rounded-2xl border border-white/5 bg-surface p-5 transition-colors open:border-purple-accent/50 open:bg-surface/80"
				>
					<summary
						class="flex cursor-pointer list-none items-center justify-between text-sm font-medium text-white"
					>
						{item.q}
						<span class="text-purple-accent transition group-open:rotate-45">+</span>
					</summary>
					<p class="mt-3 text-xs leading-relaxed text-muted">{item.a}</p>
				</details>
			{/each}
		</div>

		<!-- FINAL CTA -->
		<div class="mt-10 text-center">
			<a href={SMART_LINK_TWO} rel="external" class="cta-glow-purple inline-flex w-full max-w-sm items-center justify-center rounded-2xl bg-purple-accent px-8 py-4 text-lg font-semibold text-white transition hover:brightness-110">
				Reveal The Secret →
			</a>
			<p class="mt-4 text-xs font-medium text-purple-accent">✨ Spots are limited this week.</p>
		</div>
	</section>

	<!-- FOOTER -->
	<footer class="border-t border-white/5 px-6 py-8 text-center">
		<p class="text-xs text-muted">
			© {new Date().getFullYear()}
			{BRAND_NAME}. All rights reserved.
		</p>
	</footer>
</main>
