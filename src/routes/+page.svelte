<script lang="ts">
	import { onMount } from 'svelte';

	let scrollY = 0;

	// Mock data for the features
	const features = [
		{
			label: "SPLIT INBOX",
			title: "Prioritize what's important.",
			description: "Split your inbox so you can focus on what matters, when it matters. Never miss an urgent email again.",
			type: "split-inbox"
		},
		{
			label: "MODERN TEXT EDITOR",
			title: "Write faster.",
			description: "The text editor you love in your docs, now in your email. Typing has never felt this good before.",
			type: "editor-simple"
		},
		{
			label: "MODERN TEXT EDITOR",
			title: "Write faster.",
			description: "The text editor you love in your docs, now in your email. Typing has never felt this good before.",
			type: "editor-toolbar"
		},
		{
			label: "SPEED",
			title: "Say goodbye to lag.",
			description: "With <50ms interactions, Tatem delivers unmatched speed. Reach new heights with a new standard for responsiveness.",
			type: "speed"
		},
		{
			label: "SEAMLESS DESIGN",
			title: "Make it your own.",
			description: "Light mode. Dark mode. Elegant transitions. Minimal, yet stunning. Designed to be beautiful. Designed to inspire.",
			type: "design"
		},
		{
			label: "SHORTCUTS",
			title: "Built for your keyboard.",
			description: "Fly through your inbox with rapid-fire shortcuts for every action. Don't worry, you already know our keystrokes.",
			type: "shortcuts"
		},
		{
			label: "SECURITY",
			title: "Enterprise-grade security and privacy.",
			description: "We don't store any of your emails, passwords, or payment information in our database. Ever.",
			type: "security"
		}
	];
</script>

<svelte:window bind:scrollY />

<div class="min-h-screen bg-[#050505] text-white font-sans overflow-x-hidden selection:bg-white/30 selection:text-white">
	<!-- Top Banner -->
	<div class="fixed top-0 left-0 right-0 z-50 flex justify-center items-center py-2.5 transition-colors duration-300 {scrollY > 50 ? 'bg-[#050505]/90 backdrop-blur-md border-b border-white/5' : 'bg-transparent'}">
		<span class="text-[13px] font-medium text-white/60">Join 10,000+ rethinking their email.</span>
	</div>

	<!-- Navigation -->
	<nav class="fixed top-[45px] left-0 right-0 z-40 px-6 py-4 flex justify-between items-center max-w-7xl mx-auto w-full transition-all duration-300 {scrollY > 50 ? 'py-2' : 'py-4'}">
		<div class="flex items-center gap-2.5">
			<div class="w-5 h-5 bg-white rounded-[2px]"></div> <!-- Logo placeholder -->
			<span class="font-semibold text-lg tracking-tight">tatem</span>
		</div>
		<div class="hidden md:flex items-center gap-8 text-sm font-medium text-white/60">
			<a href="#" class="hover:text-white transition-colors">Pricing</a>
			<a href="#" class="hover:text-white transition-colors">Changelog</a>
			<a href="#" class="hover:text-white transition-colors">Sign in</a>
			<a href="#" class="text-white bg-white/10 px-5 py-2 rounded-full hover:bg-white/20 transition-colors border border-white/10">Get started</a>
		</div>
	</nav>

	<!-- Hero Section -->
	<header class="relative pt-48 pb-20 px-6 flex flex-col items-center text-center overflow-hidden">
		<!-- Background Gradient -->
		<div class="absolute top-0 left-0 right-0 h-[1000px] bg-gradient-to-b from-[#8CA8C8] via-[#1a253a] to-[#050505] -z-10 opacity-60"></div>
		
		<div class="max-w-4xl mx-auto z-10">
			<p class="text-sm font-medium text-white/50 mb-8">Now in early access.</p>
			<h1 class="text-5xl md:text-[80px] font-semibold tracking-tight leading-[1.05] mb-12">
				The email experience<br>you've been waiting for.
			</h1>
			
			<div class="flex flex-col md:flex-row items-center justify-center gap-6 mb-24">
				<button class="bg-white/5 backdrop-blur-md border border-white/20 text-white px-8 py-3.5 rounded-full font-medium hover:bg-white/10 transition-all text-sm">
					Get started
				</button>
				<span class="text-sm text-white/40 font-medium">Fast, beautiful, simple.</span>
			</div>
		</div>

		<!-- 3D Interface Placeholder -->
		<div class="relative w-full max-w-6xl mx-auto h-[400px] md:h-[700px] perspective-1000">
			<div class="w-full h-full bg-[#0a0a0a] rounded-xl border border-white/10 shadow-2xl transform rotate-x-20 rotate-y-[-5deg] rotate-z-[2deg] scale-95 translate-y-10 overflow-hidden relative group transition-transform duration-700 hover:scale-[0.97] hover:rotate-x-10">
				<!-- Mock UI Header -->
				<div class="h-14 border-b border-white/5 flex items-center px-6 gap-6 bg-[#0a0a0a]">
					<div class="flex gap-2">
						<div class="w-3 h-3 rounded-full bg-white/10"></div>
						<div class="w-3 h-3 rounded-full bg-white/10"></div>
						<div class="w-3 h-3 rounded-full bg-white/10"></div>
					</div>
					<div class="w-64 h-8 bg-white/5 rounded-md"></div>
					<div class="flex-1"></div>
					<div class="w-8 h-8 rounded-full bg-white/5"></div>
				</div>
				<!-- Mock UI Body -->
				<div class="flex h-full">
					<!-- Sidebar -->
					<div class="w-64 border-r border-white/5 p-6 space-y-6 hidden md:block bg-[#0a0a0a]">
						<div class="space-y-3">
							<div class="h-4 bg-white/10 rounded w-20 mb-4"></div>
							<div class="h-3 bg-white/5 rounded w-full"></div>
							<div class="h-3 bg-white/5 rounded w-full"></div>
							<div class="h-3 bg-white/5 rounded w-3/4"></div>
						</div>
						<div class="space-y-3 pt-4">
							<div class="h-4 bg-white/10 rounded w-16 mb-4"></div>
							<div class="h-3 bg-white/5 rounded w-full"></div>
							<div class="h-3 bg-white/5 rounded w-5/6"></div>
						</div>
					</div>
					<!-- Main Content -->
					<div class="flex-1 p-0 bg-[#050505]">
						{#each Array(10) as _, i}
							<div class="h-16 border-b border-white/5 flex items-center px-6 gap-4 hover:bg-white/[0.02] transition-colors">
								<div class="w-4 h-4 rounded border border-white/10"></div>
								<div class="w-8 h-8 rounded-full bg-white/10"></div>
								<div class="w-32 h-3 bg-white/10 rounded"></div>
								<div class="flex-1 h-3 bg-white/5 rounded mx-4"></div>
								<div class="w-16 h-3 bg-white/5 rounded"></div>
							</div>
						{/each}
					</div>
				</div>
				
				<!-- Overlay Gradient to blend into bottom -->
				<div class="absolute bottom-0 left-0 right-0 h-64 bg-gradient-to-t from-[#050505] via-[#050505]/80 to-transparent pointer-events-none"></div>
			</div>
			
			<!-- Floating label -->
			<div class="absolute bottom-20 left-10 flex items-center gap-2 text-xs text-white/30">
				<div class="w-3 h-3 bg-white/30 rounded-[1px]"></div>
				tatem
			</div>
		</div>
	</header>

	<!-- Scroll Indicator -->
	<div class="flex justify-center py-16">
		<div class="flex flex-col items-center gap-3 text-[11px] font-medium tracking-wide text-white/30 cursor-pointer hover:text-white/60 transition-colors">
			<svg width="10" height="10" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="animate-bounce">
				<path d="M7 13l5 5 5-5M7 6l5 5 5-5"/>
			</svg>
			See what makes Tatem different.
		</div>
	</div>

	<!-- Features Section -->
	<div class="max-w-5xl mx-auto px-6 py-20 space-y-40">
		{#each features as feature, i}
			<div class="space-y-8">
				<div class="space-y-3">
					<h3 class="text-[11px] font-bold tracking-[0.2em] text-white/40 uppercase pl-1">{feature.label}</h3>
					<h2 class="text-2xl md:text-[28px] leading-snug text-white/40 font-normal max-w-2xl">
						<span class="text-white font-medium">{feature.title}</span> {feature.description}
					</h2>
				</div>

				<!-- Feature Visual Container -->
				<div class="w-full aspect-[16/10] md:aspect-[2.2/1] bg-[#0a0a0a] rounded-xl border border-white/5 overflow-hidden relative flex items-center justify-center group shadow-2xl">
					
					<!-- Specific Visuals based on type -->
					{#if feature.type === 'split-inbox'}
						<div class="flex gap-10 items-center justify-center text-sm font-medium text-white/40">
							<div class="text-white border-b border-white pb-1 flex items-center gap-2">
								Important <span class="bg-white/10 text-white px-1.5 py-0.5 rounded text-[10px]">32</span>
							</div>
							<div class="hover:text-white/60 cursor-pointer flex items-center gap-2 transition-colors">
								Team <span class="text-white/20 px-1.5 py-0.5 rounded text-[10px]">15</span>
							</div>
							<div class="hover:text-white/60 cursor-pointer flex items-center gap-2 transition-colors">
								Calendar <span class="text-white/20 px-1.5 py-0.5 rounded text-[10px]">7</span>
							</div>
							<div class="hover:text-white/60 cursor-pointer flex items-center gap-2 transition-colors">
								Receipts <span class="text-white/20 px-1.5 py-0.5 rounded text-[10px]">3</span>
							</div>
						</div>
					
					{:else if feature.type === 'editor-simple'}
						<div class="text-white font-medium text-lg tracking-wide">Once</div>

					{:else if feature.type === 'editor-toolbar'}
						<div class="relative flex flex-col items-center">
							<!-- Floating Toolbar -->
							<div class="absolute -top-16 bg-[#111] border border-white/10 rounded-lg flex items-center p-1.5 gap-1 shadow-2xl shadow-black/50 transform transition-transform group-hover:-translate-y-1 duration-500">
								{#each ['B', 'I', 'U', 'S'] as icon}
									<div class="w-8 h-8 flex items-center justify-center hover:bg-white/10 rounded cursor-pointer text-white/60 text-xs font-serif">
										{icon}
									</div>
								{/each}
								<div class="w-[1px] h-4 bg-white/10 mx-1"></div>
								<div class="w-8 h-8 flex items-center justify-center hover:bg-white/10 rounded cursor-pointer text-white/60">
									<svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg>
								</div>
								<div class="w-8 h-8 flex items-center justify-center hover:bg-white/10 rounded cursor-pointer text-white/60">
									<svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><line x1="8" y1="6" x2="21" y2="6"></line><line x1="8" y1="12" x2="21" y2="12"></line><line x1="8" y1="18" x2="21" y2="18"></line><line x1="3" y1="6" x2="3.01" y2="6"></line><line x1="3" y1="12" x2="3.01" y2="12"></line><line x1="3" y1="18" x2="3.01" y2="18"></line></svg>
								</div>
							</div>
							
							<!-- Text Content -->
							<div class="text-white/80 text-lg leading-relaxed font-light">
								<span class="bg-[#3b82f6]/30 text-[#93c5fd] px-1 rounded selection:bg-transparent">Once upon a time</span>, humans were drowning in emails and<br>calendar invites.
							</div>
						</div>

					{:else if feature.type === 'speed'}
						<div class="flex gap-3 opacity-40">
							{#each Array(14) as _}
								<div class="w-3 md:w-5 h-20 md:h-32 bg-white/20 -skew-x-[20deg] rounded-[1px]"></div>
							{/each}
						</div>

					{:else if feature.type === 'design'}
						<div class="flex gap-6">
							{#each Array(7) as _, i}
								<div class="w-3 h-3 md:w-4 md:h-4 rounded-full bg-white transition-all duration-500" style="opacity: {(i+1)/7}; transform: scale({0.8 + (i/20)})"></div>
							{/each}
						</div>

					{:else if feature.type === 'shortcuts'}
						<div class="relative w-full max-w-lg">
							<!-- Keyboard Grid -->
							<div class="grid grid-cols-10 gap-1.5 opacity-60 px-10">
								{#each Array(40) as _, i}
									<div class="aspect-square border border-white/20 rounded-[4px] flex items-center justify-center text-[10px] text-white/40 {i === 25 ? 'bg-white/10 border-white/40 text-white' : ''}">
										{i === 25 ? 'C' : ''}
									</div>
								{/each}
							</div>
							
							<!-- Tooltip -->
							<div class="absolute top-[65%] left-[58%] transform -translate-x-1/2 mt-4 opacity-0 group-hover:opacity-100 transition-opacity duration-300">
								<div class="bg-[#222] text-white text-[10px] font-medium px-2 py-1 rounded border border-white/10 shadow-lg whitespace-nowrap">
									Compose
								</div>
							</div>
						</div>

					{:else if feature.type === 'security'}
						<div class="grid grid-cols-6 gap-3 opacity-80">
							{#each Array(24) as _, i}
								<div class="w-6 h-6 md:w-8 md:h-8 bg-white/10 rounded-[4px] {i % 5 === 0 || i % 7 === 0 ? 'bg-white/30' : ''} flex items-center justify-center">
									{#if i % 5 === 0 || i % 7 === 0}
										<div class="w-1.5 h-1.5 bg-white/60 rounded-full"></div>
									{/if}
								</div>
							{/each}
						</div>
					{/if}
				</div>
			</div>
		{/each}
	</div>

	<!-- Footer -->
	<footer class="mt-40 border-t border-white/5 pt-32 pb-10 px-6 bg-[#050505]">
		<div class="max-w-5xl mx-auto">
			<div class="flex flex-col items-center text-center mb-32">
				<h2 class="text-4xl md:text-5xl font-semibold mb-6 tracking-tight">Sign up today.</h2>
				<p class="text-white/40 max-w-md mb-10 text-lg">Get through your work faster and save hours each week with Tatem.</p>
				<button class="bg-white/5 backdrop-blur-md border border-white/20 text-white px-8 py-3 rounded-full font-medium hover:bg-white/10 transition-all">
					Get started
				</button>
			</div>

			<div class="grid grid-cols-2 md:grid-cols-4 gap-12 mb-24 text-sm">
				<div class="space-y-6">
					<h4 class="font-medium text-white">Company</h4>
					<ul class="space-y-3 text-white/40">
						<li><a href="#" class="hover:text-white transition-colors">About</a></li>
						<li><a href="#" class="hover:text-white transition-colors">Principles</a></li>
						<li><a href="#" class="hover:text-white transition-colors">Careers</a></li>
						<li><a href="#" class="hover:text-white transition-colors">Writing</a></li>
						<li><a href="#" class="hover:text-white transition-colors">Brand</a></li>
						<li><a href="#" class="hover:text-white transition-colors">Credits</a></li>
					</ul>
				</div>
				<div class="space-y-6">
					<h4 class="font-medium text-white">Product</h4>
					<ul class="space-y-3 text-white/40">
						<li><a href="#" class="hover:text-white transition-colors">Changelog</a></li>
						<li><a href="#" class="hover:text-white transition-colors">Pricing</a></li>
					</ul>
				</div>
				<div class="space-y-6">
					<h4 class="font-medium text-white">Resources</h4>
					<ul class="space-y-3 text-white/40">
						<li><a href="#" class="hover:text-white transition-colors">Affiliate</a></li>
						<li><a href="#" class="hover:text-white transition-colors">Contact</a></li>
					</ul>
				</div>
				<div class="space-y-6">
					<h4 class="font-medium text-white">Connect</h4>
					<ul class="space-y-3 text-white/40">
						<li><a href="#" class="hover:text-white transition-colors">X (Twitter) ↗</a></li>
						<li><a href="#" class="hover:text-white transition-colors">LinkedIn ↗</a></li>
					</ul>
				</div>
			</div>

			<div class="flex flex-col md:flex-row justify-between items-center pt-8 border-t border-white/5 text-xs text-white/30">
				<div class="flex gap-6 mb-4 md:mb-0">
					<span>Designed and built by Tatem in California</span>
				</div>
				<div class="flex gap-6">
					<a href="#" class="hover:text-white/60">Terms</a>
					<a href="#" class="hover:text-white/60">Privacy</a>
					<a href="#" class="hover:text-white/60">Sitemap</a>
					<span>©2024 Tatem Inc.</span>
				</div>
			</div>
			
			<div class="flex justify-end mt-12">
				<button on:click={() => window.scrollTo({top: 0, behavior: 'smooth'})} class="text-xs text-white/30 hover:text-white transition-colors">
					Scroll to top
				</button>
			</div>
		</div>
	</footer>
</div>

<style>
	/* Custom scrollbar to match dark theme */
	::-webkit-scrollbar {
		width: 8px;
	}
	::-webkit-scrollbar-track {
		background: #050505;
	}
	::-webkit-scrollbar-thumb {
		background: #333;
		border-radius: 4px;
	}
	::-webkit-scrollbar-thumb:hover {
		background: #444;
	}
	
	.perspective-1000 {
		perspective: 1000px;
	}
	
	.rotate-x-20 {
		transform: rotateX(20deg);
	}
</style>

