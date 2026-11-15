<script lang="ts">
	import { SMART_LINK, BRAND_NAME } from '../../lib/config';
</script>

<svelte:head>
	<title>Earn Extra Income — {BRAND_NAME}</title>
	<meta
		name="description"
		content="A simple way to earn extra income in your spare time. No experience needed."
	/>
</svelte:head>

<main class="dot-bg min-h-screen">
	<!-- HERO SECTION -->
	<section
		class="relative flex min-h-[85vh] flex-col items-center justify-center px-6 py-12 text-center"
	>
		<!-- radial gold glow -->
		<div
			class="pointer-events-none absolute inset-0 -z-10"
			style="background: radial-gradient(60% 50% at 50% 40%, rgba(245,158,11,0.15) 0%, rgba(11,15,20,0) 70%);"
		></div>

		<!-- pill -->
		<span
			class="mb-6 inline-flex items-center gap-2 rounded-full border border-gold-accent/30 bg-gold-soft px-4 py-1.5 text-xs font-medium text-gold-accent"
		>
			<span class="h-1.5 w-1.5 rounded-full bg-gold-accent"></span>
			New Opportunities Available
		</span>

		<!-- headline -->
		<h1 class="max-w-xl text-4xl font-bold tracking-tight text-white sm:text-5xl">
			A Simple Way to <span class="text-gold-accent">Earn Extra Income</span>
		</h1>

		<!-- subheadline -->
		<p class="mt-4 max-w-sm text-base text-muted sm:text-lg">
			Start today. No experience needed.
		</p>

		<!-- CTA (One-click) -->
		<a
			href={SMART_LINK}
			rel="external"
			class="cta-glow-gold cta-pulse mt-10 flex w-full max-w-sm items-center justify-center gap-2 rounded-2xl bg-gold-accent px-8 py-4 text-lg font-semibold text-bg transition hover:brightness-110"
		>
			Start Earning →
		</a>

		<p class="mt-4 text-xs text-muted">Free to join · Takes 2 minutes</p>
	</section>

	<!-- HOW IT WORKS -->
	<section class="mx-auto max-w-2xl px-6 pb-14">
		<div class="grid gap-4 sm:grid-cols-3">
			{#each [{ n: '1', t: 'Tap the button', d: 'Open the opportunity.' }, { n: '2', t: 'Pick a simple task', d: 'Choose what works for you.' }, { n: '3', t: 'Get paid', d: 'Withdraw your earnings.' }] as step (step.n)}
				<div class="rounded-2xl border border-white/5 bg-surface p-5 text-left">
					<div
						class="mb-3 flex h-9 w-9 items-center justify-center rounded-full bg-gold-soft text-sm font-bold text-gold-accent"
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
			<span>💳 Fast Payouts</span>
			<span>⏱ Flexible Hours</span>
			<span>✓ Free to Join</span>
		</div>

		<!-- REPEAT CTA -->
		<div class="mt-10 text-center">
			<a
				href={SMART_LINK}
				rel="external"
				class="cta-glow-gold inline-flex w-full max-w-sm items-center justify-center rounded-2xl bg-gold-accent px-8 py-4 text-lg font-semibold text-bg transition hover:brightness-110"
			>
				Start Earning →
			</a>
		</div>
	</section>

	<!-- FAQ -->
	<section class="mx-auto max-w-xl px-6 pb-14">
		<h2 class="mb-6 text-center text-xl font-semibold text-white">Quick questions</h2>
		<div class="space-y-3">
			{#each [{ q: 'Is this a get-rich-quick scheme?', a: 'No. It is a simple opportunity to earn extra cash in your spare time.' }, { q: 'How much can I make?', a: 'It depends on how much time you put in, but many people use it for side income.' }, { q: 'How do I get paid?', a: 'You will see the payout options as soon as you tap the button.' }] as item (item.q)}
				<details
					class="group rounded-2xl border border-white/5 bg-surface p-5 transition-colors open:border-gold-accent/50 open:bg-surface/80"
				>
					<summary
						class="flex cursor-pointer list-none items-center justify-between text-sm font-medium text-white"
					>
						{item.q}
						<span class="text-gold-accent transition group-open:rotate-45">+</span>
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
				class="cta-glow-gold inline-flex w-full max-w-sm items-center justify-center rounded-2xl bg-gold-accent px-8 py-4 text-lg font-semibold text-bg transition hover:brightness-110"
			>
				Start Earning →
			</a>
			<p class="mt-4 text-xs font-medium text-gold-accent">🚀 Start your side hustle today.</p>
		</div>
	</section>

	<!-- FOOTER -->
	<footer class="border-t border-white/5 px-6 py-8 text-center">
		<p class="text-xs text-muted">
			© {new Date().getFullYear()}
			{BRAND_NAME}. Earnings vary. Terms apply.
		</p>
	</footer>
</main>