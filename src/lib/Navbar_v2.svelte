<script>
    export let title = "R.K.";
  
    // Social links (customize as needed)
    const socials = [
      { name: 'Twitter', icon: 'x-social-media-logo-icon.svg', url: 'https://twitter.com/yourprofile' },
      { name: 'LinkedIn', icon: 'instagram-reels-icon.svg', url: 'https://linkedin.com/in/yourprofile' },
      { name: 'GitHub', icon: 'github-icon.svg', url: 'https://github.com/yourprofile' }
    ];
  </script>
  
  <nav class="flex justify-between items-center p-4">
    <!-- Icon on the top left -->
    <div class="flex items-center">
      <img src="/path/to/icon.png" alt="Site Icon" class="h-10 w-10 mr-2" />
      <a href="/">
        <h1 class="text-6xl text-blue-600">{title}</h1>
      </a>
    </div>
  
    <!-- Links to Bio and Projects -->
    <div class="flex items-center space-x-10">
      <a href="/bio" class="text-lg text-gray-700 hover:text-blue-600">Bio</a>
      <a href="/projects" class="text-lg text-gray-700 hover:text-blue-600">Projects</a>
      <a href="/projects" class="text-lg text-gray-700 hover:text-blue-600">Blog</a>
  
      <!-- Social media icons -->
      {#each socials as { name, icon, url }}
        <a href={url} target="_blank" rel="noopener noreferrer">
          <img src={`/src/assets/${icon}`} alt={name} class="h-8 w-8 hover:opacity-80" />
        </a>
      {/each}
    </div>
  </nav>
  