<script lang="ts">
	const socialMediaLinks = [
		{
			name: 'LinkedIn',
			iconClass: 'fab fa-linkedin',
			link: 'https://www.linkedin.com/in/marius-margowski/'
		},
		{
			name: 'Instagram',
			iconClass: 'fab fa-instagram',
			link: 'https://www.instagram.com/marius.margowski/'
		},
		{
			name: 'GitHub',
			iconClass: 'fab fa-github',
			link: 'https://github.com/mmargowski'
		},
		{
			name: 'Twitter',
			iconClass: 'fab fa-x-twitter',
			link: 'https://x.com/mariusmargowski'
		}
	];

	let items = [
		{
			date: 'since 08.2021',
			role: 'Director Software Engineering',
			company: 'Dealcode GmbH'
		},
		{
			date: '08.2019-07.2021',
			role: 'Chief Technology Officer',
			company: '20 Scoops Venture Capital GmbH & Co. KG'
		},
		{
			date: '06.2018-07.2019',
			role: 'IT Project Manager',
			company: '20 Scoops Venture Capital GmbH & Co. KG'
		},
		{
			date: '04.2017-05.2018',
			role: 'Salesforce Consultant',
			company: 'mindquare GmbH'
		},
		{
			date: '10.2013-01.2017',
			role: 'M.Sc. Informatik',
			company: 'Universität Zu Lübeck'
		},
		{
			date: '10.2010-09.2013',
			role: 'B.Sc. Informatik',
			company: 'Universität Zu Lübeck'
		}
	];
</script>

<main class="flex flex-col flex-1 p-4">
	<section id="introPage" class="grid grid-cols-1 lg:grid-cols-2 gap-10 py-8 sm:py-14">
		<div class="flex flex-col lg:justify-center text-center lg:text-left gap-6 md:gap-8 lg:gap-10">
			<h2 class="font-semibold text-4xl sm:text-5xl md:text-6xl">
				Hi! I'm <span class="poppins text-violet-400">Marius</span> Margowski
				<br />
				<div class="pt-8">
					Software
					<span class="poppins text-violet-400">Engineer</span>
				</div>
			</h2>
			<p class="text-base sm:text-lg md:text-xl">
				My <span class="text-violet-400"> favorite tech</span> includes Sveltekit, Nest.js, TailwindCSS
				& PostgreSQL or Firebase/Firestore!
			</p>
			<a
				href="#contact"
				class="blueShadow mx-auto lg:mr-auto lg:ml-0 text-base sm:text-lg md:text-xl poppins relative overflow-hidden px-6 py-3 group rounded-full bg-white text-slate-950"
			>
				<div
					class="absolute top-0 right-full w-full h-full bg-violet-400 opacity-20 group-hover:translate-x-full z-0 duration-200"
				/>
				<h4 class="relative z-9">Get in touch &rarr;</h4>
			</a>
		</div>
		<div class="relative shadow-2xl grid place-items-center">
			<img
				src={'images/profile.jpeg'}
				alt="Marius Margowski"
				class="object-cover z-[2] max-h-[70vh]"
			/>
		</div>
	</section>

	<section class="py-20 lg:py-32 flex flex-col gap-24" id="contact">
		<div class="flex flex-col gap-2 text-center">
			<h6 class="text-large sm:text-xl md:text-2xl">Want to connect?</h6>
			<h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
				See my <span class="poppins text-violet-400">channels</span> below!
			</h3>
		</div>
		<div class="social-links text-center">
			{#each socialMediaLinks as link (link.name)}
				<a
					href={link.link}
					target="_blank"
					rel="noopener noreferrer"
					class="text-white hover:text-violet-400 social-link px-4"
				>
					<span class="text-3xl sm:text-4xl md:text-5xl">
						<i class={link.iconClass} />
					</span>
					<span class="sr-only">{link.name}</span>
				</a>
			{/each}
		</div>
	</section>
	<section
		id="about"
		class="py-20 pt-10 lg:pt-16 lg:py-32 flex flex-col gap-16 sm:gap-20 md:gap-24 relative"
	>
		<div
			class="flex flex-col gap-2 text-center relative before:absolute before:top-0 before:left-0 before:w-2/3 before:h-1.5 before:bg-violet-700 after:absolute after:bottom-0 after:right-0 after:w-2/3 after:h-1.5 after:bg-violet-700 py-4"
		>
			<h6 class="text-large sm:text-xl md:text-2xl">Want to know more?</h6>
			<h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
				A bit <span class="poppins text-violet-400">about</span> me.
			</h3>
		</div>
		<p class="mx-auto poppins font-semibold text-lg sm:text-xl md:text-2xl">My CV . . .</p>
		<div class="flex flex-col gap-20 w-full mx-auto max-w-[800px]">
			{#each items as benefit, index}
				<div class="flex gap-6 sm:gap-8">
					<p class="poppins text-4xl sm:text-5xl md:text-1xl text-slate-500 font-semibold">
						{benefit.date}
					</p>
					<div class="flex flex-col gap-6 sm:gap-8 py-4 text-center">
						<h3 class="text-2xl sm:text-3xl md:text-2xl">
							<span class="poppins text-violet-400">{benefit.role}</span> @ {benefit.company}
						</h3>
					</div>
				</div>
			{/each}
		</div>
	</section>
</main>
