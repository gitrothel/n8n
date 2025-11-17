<script setup lang="ts"></script>

<template>
	<div class="rodeo-landing">
		<header class="rodeo-header">
			<div class="brand">
				<span class="brand-mark">RR</span>
				<span class="brand-name">Ridge &amp; Rodeo</span>
			</div>
			<nav class="nav-actions">
				<a class="ghost" href="#story">Story</a>
				<a class="ghost" href="#craft">Craft</a>
				<a class="ghost" href="#community">Community</a>
				<button class="primary">Join the ride</button>
			</nav>
		</header>

		<main class="rodeo-content">
			<section class="hero">
				<div class="hero-copy">
					<p class="eyebrow">Handcrafted essentials · Desert inspired</p>
					<h1>Carry the West wherever you wander.</h1>
					<p class="lede">
						Designed for the untamed, our tactile leather finish and playful miniatures capture the
						spirit of wide-open horizons. Built to weather every ride with grace.
					</p>
					<div class="cta-row">
						<button class="primary large">Shop the collection</button>
						<button class="secondary large">View lookbook</button>
					</div>
					<div class="pill-row">
						<span class="pill">Vegetable-tanned leather</span>
						<span class="pill">Limited artist series</span>
						<span class="pill">Free worldwide shipping</span>
					</div>
				</div>

				<div class="hero-visual" aria-hidden="true">
					<div class="sunlight"></div>
					<div class="canvas">
						<div class="wallet">
							<div class="wallet-sheen"></div>
							<div class="wallet-grid"></div>
							<div class="wallet-strap"></div>
						</div>
						<div class="figurines">
							<span class="figurine main">🤠</span>
							<span class="figurine bull">🐂</span>
							<span class="figurine rider">🐴</span>
							<span class="figurine mini">🤎</span>
						</div>
						<div class="dust"></div>
					</div>
				</div>
			</section>

			<section id="craft" class="feature-grid">
				<article class="feature-card">
					<h3>Heritage texture</h3>
					<p>
						Embossed crocodile grain with stitched accents gives each piece a sculptural presence.
					</p>
				</article>
				<article class="feature-card">
					<h3>Scaled storytelling</h3>
					<p>Hand-painted figurines celebrate the rodeo spirit and add whimsy to every scene.</p>
				</article>
				<article class="feature-card">
					<h3>Built to roam</h3>
					<p>
						Premium brass hardware, reinforced corners, and soft suede lining for daily durability.
					</p>
				</article>
			</section>
		</main>
	</div>
</template>

<style scoped lang="scss">
.rodeo-landing {
	min-height: 100vh;
	color: #2c1b0f;
	background: radial-gradient(circle at 10% 10%, rgba(255, 221, 188, 0.35), transparent 35%),
		radial-gradient(circle at 90% 20%, rgba(255, 238, 215, 0.45), transparent 30%),
		linear-gradient(145deg, #f3e0c8, #e6c99f 45%, #d8ad78 85%);
	padding: 48px clamp(24px, 4vw, 64px) 72px;
	font-family:
		'Inter',
		system-ui,
		-apple-system,
		BlinkMacSystemFont,
		'Segoe UI',
		sans-serif;
}

.rodeo-header {
	display: flex;
	align-items: center;
	justify-content: space-between;
	gap: 24px;
	margin-bottom: 56px;
}

.brand {
	display: flex;
	align-items: center;
	gap: 12px;
	font-weight: 700;
	letter-spacing: 0.04em;
	text-transform: uppercase;
}

.brand-mark {
	width: 44px;
	height: 44px;
	display: inline-flex;
	align-items: center;
	justify-content: center;
	background: linear-gradient(160deg, #8b4f24, #d5843c);
	color: #fff9f2;
	border-radius: 14px;
	box-shadow: 0 12px 30px rgba(139, 79, 36, 0.35);
}

.brand-name {
	font-size: 14px;
	color: #4b2b18;
}

.nav-actions {
	display: flex;
	align-items: center;
	gap: 12px;
}

.nav-actions a {
	font-weight: 600;
	color: #5c3a22;
	text-decoration: none;
	padding: 10px 12px;
	border-radius: 12px;
	transition:
		background-color 0.25s ease,
		transform 0.2s ease;
}

.nav-actions a:hover {
	background: rgba(92, 58, 34, 0.1);
	transform: translateY(-1px);
}

button {
	border: none;
	cursor: pointer;
	font-weight: 700;
	border-radius: 14px;
	padding: 12px 18px;
	transition:
		transform 0.2s ease,
		box-shadow 0.2s ease,
		background 0.3s ease;
}

button.primary {
	background: linear-gradient(150deg, #ad652c, #d48b45);
	color: #fffaf6;
	box-shadow: 0 14px 30px rgba(173, 101, 44, 0.35);
}

button.secondary {
	background: transparent;
	color: #744423;
	border: 2px solid rgba(116, 68, 35, 0.2);
	box-shadow: 0 12px 20px rgba(82, 50, 30, 0.1);
}

button.ghost {
	background: transparent;
	color: #744423;
}

button.primary:hover {
	transform: translateY(-1px);
	box-shadow: 0 18px 32px rgba(173, 101, 44, 0.4);
}

button.secondary:hover {
	border-color: rgba(116, 68, 35, 0.45);
	transform: translateY(-1px);
}

button.large {
	padding: 14px 22px;
	font-size: 15px;
}

.hero {
	display: grid;
	grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
	align-items: center;
	gap: clamp(32px, 5vw, 64px);
}

.hero-copy h1 {
	font-size: clamp(32px, 4vw, 48px);
	margin: 10px 0 16px;
	line-height: 1.1;
}

.hero-copy .eyebrow {
	font-weight: 700;
	letter-spacing: 0.08em;
	text-transform: uppercase;
	color: #7a4a24;
}

.hero-copy .lede {
	font-size: 17px;
	line-height: 1.7;
	color: #4a2e1c;
	max-width: 540px;
}

.cta-row {
	display: flex;
	flex-wrap: wrap;
	gap: 12px;
	margin: 22px 0 10px;
}

.pill-row {
	display: flex;
	flex-wrap: wrap;
	gap: 10px;
	margin-top: 10px;
}

.pill {
	display: inline-flex;
	align-items: center;
	padding: 10px 14px;
	border-radius: 999px;
	background: rgba(116, 68, 35, 0.08);
	color: #5c3a22;
	font-weight: 600;
	border: 1px solid rgba(116, 68, 35, 0.1);
}

.hero-visual {
	position: relative;
	display: grid;
	place-items: center;
	min-height: 420px;
}

.sunlight {
	position: absolute;
	inset: 0;
	background: radial-gradient(circle at 40% 30%, rgba(255, 214, 171, 0.9), transparent 60%),
		radial-gradient(circle at 70% 20%, rgba(255, 239, 210, 0.8), transparent 40%);
	filter: blur(60px);
	opacity: 0.9;
}

.canvas {
	position: relative;
	width: min(520px, 100%);
	aspect-ratio: 3 / 2.3;
	background: linear-gradient(180deg, rgba(255, 255, 255, 0.7), rgba(244, 226, 205, 0.85));
	border-radius: 36px;
	box-shadow:
		0 30px 70px rgba(79, 47, 27, 0.25),
		inset 0 0 0 1px rgba(255, 255, 255, 0.45);
	overflow: hidden;
	padding: 32px;
	display: grid;
	place-items: center;
}

.wallet {
	position: relative;
	width: 72%;
	aspect-ratio: 1 / 0.8;
	background: linear-gradient(130deg, #b7672c 0%, #8a4f21 38%, #d4873f 100%);
	border-radius: 20px;
	overflow: hidden;
	box-shadow:
		0 30px 45px rgba(95, 54, 25, 0.35),
		0 0 0 8px rgba(120, 68, 31, 0.08);
}

.wallet-grid {
	position: absolute;
	inset: 0;
	background-image: linear-gradient(rgba(255, 255, 255, 0.08) 1px, transparent 1px),
		linear-gradient(90deg, rgba(255, 255, 255, 0.08) 1px, transparent 1px);
	background-size: 40px 40px;
	mix-blend-mode: soft-light;
}

.wallet-sheen {
	position: absolute;
	inset: 0;
	background: linear-gradient(115deg, rgba(255, 255, 255, 0.16), transparent 50%);
}

.wallet-strap {
	position: absolute;
	top: 12px;
	left: 14px;
	right: 14px;
	height: 16px;
	background: linear-gradient(180deg, rgba(59, 31, 16, 0.7), rgba(40, 24, 14, 0.6));
	border-radius: 12px;
	box-shadow: inset 0 1px 3px rgba(255, 255, 255, 0.3);
}

.figurines {
	position: absolute;
	inset: 0;
	display: grid;
	place-items: center;
	pointer-events: none;
}

.figurine {
	position: absolute;
	font-size: 20px;
	filter: drop-shadow(0 12px 8px rgba(53, 29, 16, 0.2));
}

.figurine.main {
	font-size: 32px;
	top: 24%;
	left: 52%;
	transform: translate(-50%, -50%);
}

.figurine.bull {
	bottom: 18%;
	left: 28%;
}

.figurine.rider {
	bottom: 16%;
	right: 26%;
}

.figurine.mini {
	bottom: 26%;
	left: 52%;
}

.dust {
	position: absolute;
	bottom: 16%;
	left: 18%;
	right: 18%;
	height: 30%;
	background: radial-gradient(circle at 30% 60%, rgba(140, 84, 42, 0.15), transparent 40%),
		radial-gradient(circle at 70% 60%, rgba(84, 52, 28, 0.18), transparent 38%),
		radial-gradient(circle at 50% 40%, rgba(255, 213, 171, 0.15), transparent 30%);
	filter: blur(6px);
}

.feature-grid {
	margin-top: 64px;
	display: grid;
	gap: 18px;
	grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
}

.feature-card {
	background: rgba(255, 255, 255, 0.7);
	padding: 20px;
	border-radius: 16px;
	box-shadow: 0 18px 40px rgba(85, 52, 30, 0.14);
	border: 1px solid rgba(139, 79, 36, 0.12);
	backdrop-filter: blur(6px);
}

.feature-card h3 {
	margin: 0 0 8px;
	font-size: 18px;
	color: #5c321b;
}

.feature-card p {
	margin: 0;
	color: #4c311e;
	line-height: 1.6;
}

@media (max-width: 780px) {
	.rodeo-header {
		flex-direction: column;
		align-items: flex-start;
	}

	.nav-actions {
		width: 100%;
		justify-content: flex-start;
		flex-wrap: wrap;
	}

	.hero {
		grid-template-columns: 1fr;
	}

	.hero-visual {
		order: -1;
	}
}
</style>
