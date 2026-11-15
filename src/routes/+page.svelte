<script lang="ts">
	import { SMART_LINK, BRAND_NAME } from '../lib/config';
</script>

<svelte:head>
	<title>Claim Your Free Reward — {BRAND_NAME}</title>
	<meta
		name="description"
		content="Limited spots available. Claim your free reward in 30 seconds."
	/>
</svelte:head>

<main class="dot-bg min-h-screen">
	<!-- HERO SECTION (Tightened spacing) -->
	<section
		class="relative flex min-h-[85vh] flex-col items-center justify-center px-6 py-12 text-center"
	>
		<!-- radial green glow -->
		<div
			class="pointer-events-none absolute inset-0 -z-10"
			style="background: radial-gradient(60% 50% at 50% 40%, rgba(34,197,94,0.18) 0%, rgba(11,15,20,0) 70%);"
		></div>

		<!-- pill -->
		<span
			class="mb-6 inline-flex items-center gap-2 rounded-full border border-accent/30 bg-accent-soft px-4 py-1.5 text-xs font-medium text-accent"
		>
			<span class="h-1.5 w-1.5 rounded-full bg-accent"></span>
			Limited spots available
		</span>

		<!-- headline -->
		<h1 class="max-w-xl text-4xl font-bold tracking-tight text-white sm:text-5xl">
			Claim Your <span class="text-accent">Free Reward</span>
		</h1>

		<!-- subheadline (removed duplicate "limited spots") -->
		<p class="mt-4 max-w-sm text-base text-muted sm:text-lg">
			Takes just 30 seconds. No payment needed.
		</p>

		<!-- CTA (One-click) -->
		<a
			href={SMART_LINK}
			rel="external"
			class="cta-glow cta-pulse mt-10 flex w-full max-w-sm items-center justify-center gap-2 rounded-2xl bg-accent px-8 py-4 text-lg font-semibold text-white transition hover:brightness-110"
		>
			Claim My Reward →
		</a>

		<p class="mt-4 text-xs text-muted">Takes 30 seconds · No payment needed</p>
	</section>

	<!-- HOW IT WORKS -->
	<section class="mx-auto max-w-2xl px-6 pb-14">
		<div class="grid gap-4 sm:grid-cols-3">
			{#each [{ n: '1', t: 'Tap the button', d: 'One tap to get started.' }, { n: '2', t: 'Complete a quick step', d: 'Takes about 30 seconds.' }, { n: '3', t: 'Unlock your reward', d: 'That’s it. You’re done.' }] as step (step.n)}
				<div class="rounded-2xl border border-white/5 bg-surface p-5 text-left">
					<div
						class="mb-3 flex h-9 w-9 items-center justify-center rounded-full bg-accent-soft text-sm font-bold text-accent"
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
			<span>🔒 Secure</span>
			<span>⏱ 30 seconds</span>
			<span>✓ No payment</span>
		</div>

		<!-- REPEAT CTA -->
		<div class="mt-10 text-center">
			<a
				href={SMART_LINK}
				rel="external"
				class="cta-glow inline-flex w-full max-w-sm items-center justify-center rounded-2xl bg-accent px-8 py-4 text-lg font-semibold text-white transition hover:brightness-110"
			>
				Claim My Reward →
			</a>
		</div>
	</section>

	<!-- FAQ -->
	<section class="mx-auto max-w-xl px-6 pb-14">
		<h2 class="mb-6 text-center text-xl font-semibold text-white">Quick questions</h2>
		<div class="space-y-3">
			{#each [{ q: 'Is it really free?', a: 'Yes — you just need to complete one quick step.' }, { q: 'How long does it take?', a: 'About 30 seconds from tap to unlock.' }, { q: 'What do I get?', a: 'Your reward unlocks right after the quick step.' }] as item (item.q)}
				<details
					class="group rounded-2xl border border-white/5 bg-surface p-5 transition-colors open:border-accent/50 open:bg-surface/80"
				>
					<summary
						class="flex cursor-pointer list-none items-center justify-between text-sm font-medium text-white"
					>
						{item.q}
						<span class="text-accent transition group-open:rotate-45">+</span>
					</summary>
					<p class="mt-3 text-xs leading-relaxed text-muted">{item.a}</p>
				</details>
			{/each}
		</div>

		<!-- FINAL CTA -->
		<div class="mt-10 text-center">
			<a
				href={SMART_LINK}
				rel="external"
				class="cta-glow inline-flex w-full max-w-sm items-center justify-center rounded-2xl bg-accent px-8 py-4 text-lg font-semibold text-white transition hover:brightness-110"
			>
				Claim My Reward →
			</a>
			<p class="mt-4 text-xs font-medium text-amber-400">⚠️ Only a few spots left.</p>
		</div>
	</section>

	<!-- FOOTER -->
	<footer class="border-t border-white/5 px-6 py-8 text-center">
		<p class="text-xs text-muted">
			© {new Date().getFullYear()}
			{BRAND_NAME}. Rewards subject to availability. Terms apply.
		</p>
	</footer>
</main>