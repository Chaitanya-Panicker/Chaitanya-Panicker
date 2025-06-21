<div align="center">
  
![MasterHead](https://media.licdn.com/dms/image/v2/D4D16AQFtQm1V5xx7_w/profile-displaybackgroundimage-shrink_200_800/profile-displaybackgroundimage-shrink_200_800/0/1710870009359?e=2147483647&v=beta&t=cIZvlOB6_rB053_id6XabKgAprryKmT20PYaSfkCl_A)

</div>

<h1 align="center">Hi 👋, I'm Chaitanya Panicker</h1>
<h3 align="center">A Passionate Data Analyst from India</h3>

- 🌱 I’m currently learning **PowerBI, MS Excel, SQL, Python & Tableau**
  
- 💬 Ask me about **Data Analytics**

- ⚡ Fun fact **I think I am curious about Data & Visualization**

<h3 align="center">Skills:</h3>
import { useEffect, useRef } from 'react';

export default function Skills() { 
	const skills = [
		{ name: "Excel", percentage: 90 },
		{ name: "SQL", percentage: 85 },
		{ name: "Python", percentage: 80 },
		{ name: "Power BI", percentage: 75 },
		{ name: "Tableau", percentage: 75 }
	];

	const sectionRef = useRef(null);

	useEffect(() => {
		const observer = new IntersectionObserver(
			(entries) => {
				entries.forEach((entry) => {
					if (entry.isIntersecting) {
						entry.target.classList.add('animate-progress');
					} else {
						entry.target.classList.remove('animate-progress');
					}
				});
			},
			{ threshold: 0.2 }
		);

		const progressBars = document.querySelectorAll('.progress-bar');
		progressBars.forEach((bar) => observer.observe(bar));

		return () => {
			progressBars.forEach((bar) => observer.unobserve(bar));
		};
	}, []);

	return ( 
		<section id="skills" ref={sectionRef}
			className="px-20 w-full my-40 max-w-5xl mx-auto gap-10"> 
			<h2 style={{fontFamily: "Bahnschrift"}} className="gap-50 text-black-100 text-5xl font-bold mb-5 border-b-[5px] w-[125px] mx-auto border-indigo-600 pb-2">
				Skills
			</h2> 
			<div className="mt-10 flex gap-10 justify-center flex-wrap mx-auto max-w-4xl">
				{skills.map((skill, index) => (
					<div key={index} className="flex flex-col items-center group">
						<div className="relative w-32 h-32 transform transition-transform duration-300 hover:scale-110">
							<svg className="w-full h-full -rotate-90" viewBox="0 0 36 36">
								<path
									d="M18 2.0845
										a 15.9155 15.9155 0 0 1 0 31.831
										a 15.9155 15.9155 0 0 1 0 -31.831"
									fill="none"
									stroke="#2D3748"
									strokeWidth="3"
								/>
								<path
									d="M18 2.0845
										a 15.9155 15.9155 0 0 1 0 31.831
										a 15.9155 15.9155 0 0 1 0 -31.831"
									fill="none"
									stroke="#6366F1"
									strokeWidth="3"
									strokeDasharray="0 100"
									className="progress-bar transition-all duration-1000 ease-in-out"
									style={{
										"--percentage": `${skill.percentage}, 100`,
										"--initial-dash": "0 100",
										"--final-dash": `${skill.percentage}, 100`
									}}
								/>
							</svg>
							<div className="absolute inset-0 flex items-center justify-center">
								<span className="font-bold text-black-100 transition-colors duration-300 group-hover:text-indigo-600 font-['Bahnschrift'] text-xl">{skill.percentage}%</span>
							</div>
						</div>
						<span className="mt-4 text-black-100 font-medium transition-colors duration-300 group-hover:text-indigo-600 font-['Bahnschrift'] text-xl">{skill.name}</span>
					</div>
				))}
			</div>

			<style jsx>{`
				.progress-bar {
					stroke-dasharray: var(--initial-dash);
				}
				.progress-bar.animate-progress {
					stroke-dasharray: var(--final-dash);
				}
			`}</style>
		</section> 
	) 
}


<div align="center">
<h3 align="center">Connect with me:</h3>
<p align="center">
<a href="mailto:chaitanya.panicker98@gmail.com" target="_blank">
  <img src="https://img.shields.io/static/v1?message=Gmail&logo=gmail&label=&color=D14836&logoColor=white&labelColor=&style=for-the-badge" height="35" alt="gmail logo" />
</a>


<a href="https://www.linkedin.com/in/chaitanyapanicker98/" target="_blank">
  <img src="https://img.shields.io/static/v1?message=LinkedIn&logo=linkedin&label=&color=0077B5&logoColor=white&labelColor=&style=for-the-badge" height="35" alt="linkedin logo" />
</a>
</p>

<div align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=chaitanya-panicker&hide_title=false&hide_rank=true&show_icons=true&include_all_commits=true&count_private=true&disable_animations=false&theme=dracula&locale=en&hide_border=false" height="150" alt="stats graph"  />
  <img src="https://github-readme-streak-stats.herokuapp.com/?user=chaitanya-panicker&" alt="chaitanya-panicker" height="150"/>
</div>
