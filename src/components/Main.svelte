<script>
	import Step from './Step.svelte';
	let steps = [
		{
			name: 'TechPeople Astro Blog',
			icon: 'fa-solid fa-book',
			href: 'https://github.com/Epiq122/astro-blog'
		},
		{
			name: 'React Essentials',
			icon: 'fa-solid fa-x',
			href: 'https://github.com/Epiq122/react-essentials-v2',
			link: 'https://react-essentials-max-ts.vercel.app'
		},
		{
			name: 'Todo Mangement',
			icon: 'fa-solid fa-list',
			href: 'https://github.com/Epiq122/todo-mangement-system'
		}
	];

	let benifits = [
		{
			name: 'java bootcamp graduate ',
			description:
				'I completed a Full Stack Java bootcamp where I learned all about Java and Springboot, we also learned how to work with MySql DB'
		},
		{
			name: 'frontend self taught developer ',
			description:
				'I taught myself to code using various resources I found online, I fell in love with the creativity and problem solving thats involded in developing web applications. I quickly found that I really enjoy working with the frontend as well'
		},
		{
			name: 'willingness to learn ',
			description:
				'I am willing to learn just about anything when it comes to web development or software development in general, I have a mind ready to be molded'
		}
	];
</script>

<main class="flex flex-col flex-1 p-4">
	<section id="introPage" class="grid grid-cols-1 lg:grid-cols-2 gap-10 py-8 sm:py-14">
		<div class="flex flex-col lg:justify-center text-center lg:text-left gap-6 md:gap-8 lg:gap-10">
			<h2 class="font-semibold text-4xl sm:text-5xl md:text-6xl">
				Hi! I'm <span class="poppins text-violet-400">Rob</span> Gleason<br /> Full Stack
				<span class="poppins text-violet-400">Developer</span>
			</h2>
			<p class="text-base sm:text-lg md:text-xl">
				My <span class="text-violet-400">favorite tech</span>
				includes Javascript (NextJs,React), TailwindCSS, Java. SpringBoot!
			</p>
			<!-- socials -->
			<a
				href="#socials"
				class="blueShadow mx-auto lg:mr-auto lg:ml-0 text-base sm:text-lg md:text-xl poppins relative overflow-hidden px-6 py-3
        group rounded-full bg-white text-slate-950 cursor-pointer"
			>
				<div
					class="absolute top-0 right-full w-full h-full bg-violet-500 opacity-20 group-hover:translate-x-full duration-200"
				/>
				<h4 class="relative z-[10]">Get in touch &rarr;</h4>
			</a>
		</div>
		<div class="relative shadow-2xl grid place-items-center">
			<img src={'images/profile.png'} alt="Profile" class="object-cover z-[2] max-h-[50vh]" />
		</div>
	</section>
	<section id="projects" class="py-20 lg:py-32 flex flex-col gap-24">
		<div class="flex flex-col gap-2 text-center">
			<h6 class="text-lge sm:text-xl md:text-2xl">A few of my creations</h6>
			<h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
				Curious to <span class="poppins text-violet-400">see</span> my work?
			</h3>
		</div>
		<!-- <a
			href="#"
			target="_blank"
			class="mx-auto px-4 py-2 rounded-md border border-solid border-white flex items-center gap-2 mb-4 sm:mb-0
    -mt-10 hover:border-violent-700 duration-200
    "
		>
			<i class="fa-regular fa-circle-play" />
			<p>Watch the video</p>
		</a> -->

		<div class="grid grid-cols-1 lg:grid-cols-3 gap-12 lg:gap-10">
			<Step step={steps[0]}
				>TechPeople is a small bolg site with pagination and search functionality created with<strong
					class="text-violet-400"
				>
					Astro, Typescript,TailwindCSS</strong
				>
				<h5>Github Repo</h5>
				<a
					href="https://astro-blog-azure-eight.vercel.app/"
					class="hover:text-blue-500 transition duration-200">Live Demo</a
				>
			</Step>
			<Step step={steps[1]}>
				A React landing type page that shows some information about react essentials<strong
					class="text-violet-400"
				>
					React, Typescript,Styled Components</strong
				>
				<h5 class="hover:text-blue-500 transition duration-200">GitHub Repo</h5>
				<a
					href="https://react-essentials-max-ts.vercel.app"
					class="hover:text-blue-500 transition duration-200">Live Demo</a
				>
			</Step>
			<Step step={steps[2]}>
				This to-do management app offers login/register functionality, full CRUD operations, admin
				roles for adding, updating, and deleting tasks, basic user roles for task completion, and
				utilizes JWT authentication with user data stored in a database.<strong
					class="text-violet-400"
				>
					Spring Boot 3 Spring Security 6 JWT Spring Data MySQL React Bootstrap JPA</strong
				>
				<h5>Currently only GitHub Repo</h5>
			</Step>
		</div>
	</section>
	<section
		id="about"
		class="py-20 pt-10 lg:pt-16 lg:py-32 flex flex-col gap-16 sm:gap-20 md:gap-24 relative"
	>
		<div
			class="flex flex-col gap-2 text-center relative before:absolute before:top-0 before:left-0 before:w-2/3 before:h-1.5 before:bg-violet-700
      after:absolute after:bottom-0 after:right-0 after:w-2/3 after:h-1.5 after:bg-violet-700 py-4
 "
		>
			<h6 class="text-lg sm:text-xl md:text-2xl">Want to know more?</h6>
			<h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
				A bit <span class="poppins text-violet-400">about</span> me
			</h3>
		</div>
		<p class="mx-auto poppins font-semibold text-lg sm:text-xl md:text-2xl">I am . . .</p>
		<div class="flex flex-col gap-20 w-full mx-auto max-w-[800px]">
			{#each benifits as benifit, index}
				<div class="flex gap-6 sm:gap-8">
					<p class="poppins text-4xl sm:text-5xl md:text-6xl text-slate-500 font-semibold">
						0{index + 1}
					</p>
					<div class="flex flex-col gap-6 sm:gap-8">
						<h3 class="text-2xl sm:text-3xl md:text-5xl">
							{benifit.name}
						</h3>
						<p>
							{benifit.description}
						</p>
					</div>
				</div>
			{/each}
		</div>
		<h5 class="text-2xl sm:text-3xl font-semibold text-center poppins">
			The <span class="text-violet-400 poppins">Complete</span> Package
		</h5>
		<div class="flex flex-col overflow-x-scroll gap-10 max-w-[800px] mx-auto w-full">
			<table class="bg-white text-slate-700 rounded text-center">
				<thead class="border-b border-solid border-slate-200">
					<tr class="">
						<th class="" />
						<th class="whitespace-nowrap p-2 px-4">Candidate #1</th>
						<th class="whitespace-nowrap p-2 px-4">Candidate #2</th>
						<th class="whitespace-nowrap p-2 px-4">Candidate #3</th>
						<th class="whitespace-nowrap bg-violet-700 text-white p-4 px-8">Me</th>
					</tr>
				</thead>
				<tbody>
					<tr class="border-b border-solid border-slate-200">
						<td
							class="border-right border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm whitespace-nowrap"
							>Dedication</td
						>
						<td><i class="fa-solid fa-xmark text-slate-500" /></td>
						<td><i class="fa-solid fa-check text-green-500" /></td>
						<td><i class="fa-solid fa-xmark text-slate-500" /></td>
						<td><i class="fa-solid fa-check text-green-500" /></td>
					</tr>
					<tr class="border-b border-solid border-slate-200">
						<td
							class="border-right border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm whitespace-nowrap"
							>Critical Thinker</td
						>
						<td><i class="fa-solid fa-check text-green-500" /></td>
						<td><i class="fa-solid fa-xmark text-slate-500" /></td>
						<td><i class="fa-solid fa-check text-green-500" /></td>
						<td><i class="fa-solid fa-check text-green-500" /></td>
					</tr>
					<tr class="border-b border-solid border-slate-200">
						<td
							class="border-right border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm whitespace-nowrap"
							>Interpersonal Skills</td
						>
						<td><i class="fa-solid fa-xmark text-slate-500" /></td>
						<td><i class="fa-solid fa-check text-green-500" /></td>
						<td><i class="fa-solid fa-xmark text-slate-500" /></td>
						<td><i class="fa-solid fa-check text-green-500" /></td>
					</tr>
					<tr class="border-b border-solid border-slate-200">
						<td
							class="border-right border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm whitespace-nowrap"
							>Programming Ability</td
						>
						<td><i class="fa-solid fa-check text-green-500" /></td>
						<td><i class="fa-solid fa-xmark text-slate-500" /></td>
						<td><i class="fa-solid fa-xmark text-slate-500" /></td>
						<td><i class="fa-solid fa-check text-green-500" /></td>
					</tr>
				</tbody>
			</table>
			<div class="mx-auto -mt-12 itealic sm:hidden opacity-50">
				<p>Scroll to see more &rarr;</p>
			</div>
		</div>
		<p class="mx-auto">So why not invest?</p>
	</section>
</main>
