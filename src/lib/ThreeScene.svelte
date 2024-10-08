<script>
	import { onMount } from 'svelte';
	import * as THREE from 'three';

	let container;

	onMount(() => {
		const scene = new THREE.Scene();
		const camera = new THREE.PerspectiveCamera(
			75,
			window.innerWidth / window.innerHeight,
			0.1,
			1000
		);
		const renderer = new THREE.WebGLRenderer({
			
		});

		renderer.setSize(window.innerWidth, window.innerHeight);
		container.appendChild(renderer.domElement);

		const animate = () => {
			requestAnimationFrame(animate);
			renderer.render(scene, camera);
		};
		animate();
	});
</script>

<div bind:this={container} id="bg"></div>
