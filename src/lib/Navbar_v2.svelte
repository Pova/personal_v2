<script>
	export let title = 'Roman Kitsela';

	// Social links (customize as needed)
	const socials = [
		{
			name: 'Instagram',
			icon: 'instagram-icon.svg',
			url: 'https://twitter.com/yourprofile'
		},
		{ name: 'LinkedIn', icon: 'linkedin.svg', url: 'https://linkedin.com/in/yourprofile' },
		{ name: 'GitHub', icon: 'github-icon.svg', url: 'https://github.com/yourprofile' }
	];
</script>

<nav class="flex justify-between items-center p-4">
	<!-- Icon on the top left -->
	<div class="flex items-center space-x-4">
		<img src="/src/assets/home.svg" alt="Home page" class="h-8 w-8 hover:stroke-blue" />
		<a href="/">
			<h1 class="text-3xl text-gray-600">{title}</h1>
		</a>
	</div>

	<!-- Links to Bio and Projects -->
	<div class="flex items-center space-x-10">
		<a href="/about" class="text-lg text-gray-700 hover:text-blue-600">About Me</a>
		<a href="/projects" class="text-lg text-gray-700 hover:text-blue-600">Projects</a>
		<a href="/blog" class="text-lg text-gray-700 hover:text-blue-600">Data Stories</a>

		<!-- Social media icons -->
		{#each socials as { name, icon, url }}
			<a href={url} target="_blank" rel="noopener noreferrer">
				<div class="h-8 w-8 hover:opacity-80">
					<img src={`/src/assets/${icon}`} alt={name} />
				</div></a
			>
		{/each}
	</div>
</nav>
