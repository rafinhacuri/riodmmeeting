<script setup lang="ts">
const menuItems = ref([
	{ name: 'Rationale' },
	{ name: 'Topics' },
	{ name: 'Venue' },
	{ name: 'Registration' },
	{ name: 'Program' },
	{ name: 'Participants' },
	{ name: 'Organizing Committee' },
	{ name: 'Organization and support' },
])
const pessoas = [
	{ nome: 'Álvaro Santos de Jesus', instituicao: 'UFRN/IIP' },
	{ nome: 'Amanda Evelyn de Araujo Carvalho', instituicao: 'OV-UFRJ' },
	{ nome: 'Anibal Varela', instituicao: 'UNSAM' },
	{ nome: 'Arianna Cortesi', instituicao: 'OV-UFRJ' },
	{ nome: 'Arman Esmaili Taklimi', instituicao: 'PUC-Rio' },
	{ nome: 'Bernhard Meirose', instituicao: 'Lund University + Stockholm University' },
	{ nome: 'Carlos R. Argüelles', instituicao: 'IALP-CONICET/UNLP' },
	{ nome: 'Clarissa Martins Siqueira', instituicao: 'IFSC/USP' },
	{ nome: 'Davi Cabral Rodrigues', instituicao: 'UFES' },
	{ nome: 'Eduardo Cypriano', instituicao: 'IAG-USP' },
	{ nome: 'Farinaldo da Silva Queiroz', instituicao: 'IIP/UFRN' },
	{ nome: 'Gabriel da Silva Moreira Teixeira', instituicao: 'CBPF' },
	{ nome: 'Hérman Lima Jr.', instituicao: 'CBPF' },
	{ nome: 'João Paulo Correia de França', instituicao: 'CBPF' },
	{ nome: 'Marco Grossi', instituicao: 'OV-UFRJ' },
	{ nome: 'Miguel Quartin', instituicao: 'IF-UFRJ' },
	{ nome: 'Murilo Santana Rangel', instituicao: 'IF-UFRJ' },
	{ nome: 'Natanael Gomes de Oliveira', instituicao: 'OV-UFRJ' },
	{ nome: 'Nelson Padilla', instituicao: 'IATE-CONICET/UNC' },
	{ nome: 'Pedro Cataldi', instituicao: 'IAFE-CONICET/UBA' },
	{ nome: 'Rafael Antunes Nóbrega', instituicao: 'UFJF' },
	{ nome: 'Ramon de Sá Pereira', instituicao: 'UFF' },
	{ nome: 'Ulisses Barres de Almeida', instituicao: 'CBPF' },
	{ nome: 'Vitor Souza Ramos', instituicao: 'CBPF' },
]

const open = ref(false)

function ScrollToDiv(targetId: string) {
	const targetDiv = document.getElementById(`${targetId}`)
	if (targetDiv)
		scrollTo({ top: targetDiv.offsetTop - 65, behavior: 'smooth' })
}
</script>

<template>
	<div>
		<div class="bg-[#CDEBFE] flex flex-wrap justify-between pb-4 top-0">
			<div class="flex items-center mt-4 ml-3 space-x-3">
				<NuxtLink
					to="https://cbpf.br"
					external
					target="_blank"
					class="flex items-center"
				>
					<img
						src="/cbpf.svg"
						class="h-12 mr-3 ml-10"
						alt="Logo do Centro Brasileiro de Pesquisas Físicas"
					>
					<span class="self-center text-5xl font-bold whitespace-nowrap text-[#394B63] pb-1">CBPF</span>
				</NuxtLink>
			</div>
			<ol class="md:flex items-center justify-center p-3 md:space-x-9 md:pr-20 md:pt-5 font-medium grid grid-cols-4 grid-rows-2">
				<li v-for="item in menuItems" :key="item.name" class="link link-underline link-underline-black  text-black font-mono cursor-pointer relative">
					<span @click="item.name === 'Program' ? open = !open : ScrollToDiv(`${item.name}`)">{{ item.name }}</span>
					<div v-if="item.name === 'Program'" v-show="open" class="absolute left-0 mt-2 w-48 rounded-md shadow-lg bg-white ring-1 ring-black ring-opacity-5 overflow-hidden">
						<div class="py-1" role="menu" aria-orientation="vertical" aria-labelledby="options-menu">
							<a href="/program/Monday.pdf" download class="block px-4 py-2 text-sm text-gray-700 hover:bg-gray-100 hover:text-gray-900" role="menuitem">Monday</a>
							<a href="/program/Tuesday.pdf" download class="block px-4 py-2 text-sm text-gray-700 hover:bg-gray-100 hover:text-gray-900" role="menuitem">Tuesday</a>
							<a href="/program/Wednesday.pdf" download class="block px-4 py-2 text-sm text-gray-700 hover:bg-gray-100 hover:text-gray-900" role="menuitem">Wednesday</a>
						</div>
					</div>
				</li>
			</ol>
		</div>

		<div class="bg-[#343434] text-white h-80 flex items-center justify-center flex-col space-y-6">
			<p class="text-5xl text-center tracking-wider font-semibold">
				First Rio Dark Matter Meeting
			</p>
			<p class="text-2xl text-center">
				March 20-22, 2023
			</p>
		</div>
		<div id="Rationale">
			<h2 class="text-4xl pl-10 pt-12 tracking-wider font-bold underline">
				Rationale
			</h2>
			<div class="flex flex-col md:flex-row items-center">
				<div class="w-full md:w-[800px] p-10 pr-28 space-y-12 text-sm font-bold">
					<p>
						The nature of Dark Matter has been one of the major scientific issues for decades. Although
						a vast amount of astrophysical evidence points at its existence, so far a hypothetical Dark
						Matter particle has eluded its detection. In recent years the field of Dark Matter research
						has dramatically broadened its scope from the cosmological and astrophysical realms to
						encompass a myriad of dedicated experiments, also connecting to particle astrophysics,
						accelerator physics and the development of new detection techniques. The many
						possibilites of Dark Matter physics, including alternatives to its existence, have fueled an
						intense activity in theoretical models and phenomenology. Perhaps the only certainty we
						have until now about Dark Matter is that is has become an imminently interdisciplinary field,
						involving large sectors of theoretical and experimental physics, astronomy and cosmology,
						and instrumentation and data analysis.
					</p>
					<p class="pb-6">
						The Rio de Janeiro state hosts a significant number of universities and research institutions,
						which carry out research potentially connected to Dark Matter, and indeed, this field of
						research has been emerging in the region. However, due to the interdisciplinary nature of
						the field and the diversity of the institutions, that has been very little interaction among the
						scientists interested in this field. This has motivated the organization of a workshop where
						students and researchers in the region interested in Dark Matter could have an overview of
						the research currently being carried out in this field, discuss potential collaborations, and
						plan new avenues for research. To that end, we have invited researchers from Rio de Janeiro
						and abroad to deliver short talks on their field and talk about their current research.
					</p>
					<p>
						The meeting was initially planned as a small workshop with in person attendance, thus
						naturally restricted to participants from the Rio de Janeiro area and a few invited
						participants from other regions. However, the first edition was abruptly canceled due to the
						onset of the COVID-19 pandemic. One of the lessons learned during that period is how to
						hold hybrid meetings, which enables a broader participation. Therefore, we are holding the
						First Rio Dark Matter Meeting with in person and remote participation.
					</p>
				</div>
				<div class="flex flex-col justify-center items-center space-y-52">
					<div>
						<img src="/foto1.png" alt="foto de ciencia" class="h-[350px]">
						<img src="/PBH_Rio.png" alt="foto de ciencia" class="h-[180px] pt-4">
					</div>
					<p class="w-full md:w-[400px] pl-2 text-base font-extrabold">
						Participation is open to students and researchers
						worldwide, which can also propose contributed talks.
						Registration is required to receive the zoom link and to
						attend in person.
					</p>
				</div>
			</div>
		</div>

		<div id="Topics" class="bg-[#F1F1F1]">
			<h3 class="text-center p-10 text-5xl font-semibold underline">
				Topic
			</h3>
			<div class="flex space-x-20 justify-center pl-3 pb-16">
				<div>
					<ul class="md:list-disc list-none space-y-3 text-2xl font-semibold">
						<li>Astrophysical probes of Dark Matter</li>
						<li>Dark Matter experiments</li>
						<li>Indirect Dark Matter detection</li>
						<li>Accelerator experiments</li>
					</ul>
				</div>
				<div>
					<ul class="md:list-disc list-none space-y-3 text-2xl font-semibold">
						<li>Detection techniques</li>
						<li>Dark Matter models</li>
						<li>Alternatives to Dark Matter</li>
						<li>Beyond Standard Model Physics</li>
					</ul>
				</div>
			</div>
		</div>
		<div id="Registration">
			<div class="bg-[#0D0D0D] text-white flex flex-col items-center justify-center font-semibold p-7 space-y-4 shadow-xl">
				<p class="text-6xl text-center tracking-wide md:text-4xl">
					Registration deadline
				</p>
				<p class="text-4xl md:text-2xl">
					March 13, 2023
				</p>
			</div>
			<div>
				<h2 class="text-4xl pl-10 pt-12 tracking-wider font-bold underline text-end md:text-2xl md:pl-5 md:pt-6">
					Registration
				</h2>
				<div class="flex flex-col md:flex-row">
					<div class="flex flex-col justify-center items-center space-y-16">
						<img src="/foto2.png" alt="foto de ciencia" class=" m-5 ">
					</div>
					<div class="w-full p-10 space-y-7 text-base font-medium md:w-auto">
						<p>
							The registration is free and open to participants worldwide, limited by our zoom
							availability. If needed be, priority will be given to participants from Latin America.
						</p>
						<p>
							Applications for contributed talks from all participants are welcome. However, given
							the motivation to foster the collaboration and awareness of research conducted in the
							Rio de Janeiro state, priority of presentations will be given to in-person participants
							and presentations from scientists connected to Rio de Janeiro.
						</p>
						<p>
							Applications for contributed talks from all participants are welcome. However, given
							the motivation to foster the collaboration and awareness of research conducted in the
							Rio de Janeiro state, priority of presentations will be given to in person participants
							and presentations from scientists connected to Rio de Janeiro
						</p>
						<p>
							Also, to promote a more direct connection among the participants, we request those
							from the city of Rio de Janeiro and surroundings to attend at least one of the
							sessions in person (exceptions will be considered).
						</p>
						<p>
							Please fill the registration form here <a href="https://tinyurl.com/1sRioDMmeeting" external target="_blank">
								https://tinyurl.com/1sRioDMmeeting
							</a> by March 15
						</p>
					</div>
				</div>
			</div>
		</div>

		<div>
			<div class="bg-[#F1F1F1]">
				<p class="text-center pt-10 pb-4 text-4xl font-bold underline md:text-2xl md:pt-5 md:pb-2">
					Program
				</p>
				<p class="text-center text-xl font-medium pb-14 md:text-lg md:pb-7">
					The program will be available on March 16
				</p>
				<p class="pl-32 pb-12 text-3xl font-semibold md:text-xl md:pl-16 md:pb-6">
					Confirmed speakers
				</p>
				<ol class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-4">
					<li v-for="(pessoa, index) in pessoas" :key="index">
						<div class="bg-white rounded-xl shadow-md overflow-hidden w-full m-3 mb-10 md:m-1.5 md:mb-5">
							<div class="flex flex-col">
								<div class="p-8 md:p-4">
									<div class="uppercase tracking-wide text-sm text-black font-semibold md:text-xs">
										{{ pessoa.nome }}
									</div>
									<p class="mt-2 text-gray-700 md:text-xs">
										{{ pessoa.instituicao }}
									</p>
								</div>
							</div>
						</div>
					</li>
				</ol>
			</div>
		</div>

		<div id="Participants" class="flex flex-col justify-center items-center">
			<h3 class="pt-16 pb-7 text-4xl font-semibold tracking-wider underline">
				Participants
			</h3>
			<a href="/1stRioDMform(Responses)_FINAL.xlsx" download class="bg-slate-700 p-4 rounded-xl shadow-lg text-xl font-semibold text-white hover:bg-slate-600 mb-2" role="particpants">Participants List</a>
			<p class="text-xl font-medium pb-16">
				The list will be available on March 14
			</p>
		</div>
		<div
			id="Organizing Committee" class="bg-[#0D0D0D] text-white flex items-center justify-center font-semibold p-7 space-y-4 shadow-xl"
		>
			<p class="text-4xl pr-20 tracking-wide">
				Organizing Committee
			</p>
			<p class="text-xl font-normal w-[500px]">
				Local Organizing Committee: Martín Makler (UNSAM/
				CBPF - chair), Clécio De Bom (CBPF), Arthur Câmara
				Mesquita (CBPF), João Paulo França (CBPF)
			</p>
		</div>
		<div id="Venue" class="bg-[#F1F1F1]">
			<h2 class="text-4xl pl-10 pt-12 tracking-wider font-bold underline text-end md:text-2xl md:pl-5 md:pt-6">
				Venue
			</h2>
			<div class="flex flex-col md:flex-row justify-center pb-6">
				<iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3673.8969020311956!2d-43.1762694248101!3d-22.954023739560753!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x99801d6a53c8cb%3A0xd60303dd37504016!2sR.%20Dr.%20Xavier%20Sigaud%2C%20150%20-%20Urca%2C%20Rio%20de%20Janeiro%20-%20RJ%2C%2022290-180!5e0!3m2!1spt-BR!2sbr!4v1700586194816!5m2!1spt-BR!2sbr" style="border:0;" allowfullscreen loading="lazy" referrerpolicy="no-referrer-when-downgrade" class="rounded-xl md:w-[600px] md:h-[500px] w-[300px] h-[300px] m-4" />
				<div class="space-y-6 md:w-1/2 md:pl-6">
					<p class="w-full font-semibold text-xl pl-6 md:text-lg">
						Brazilian Center for Physics Research - <a
							href="https://www.gov.br/
				cbpf/pt-br/o-cbpf/como-chegar" class="text-slate-600" external target="_blank"
						> CBPF</a>
						Rua Dr. Xavier Sigaud, 150 - Urca
						Rio de Janeiro - RJ - Brasil
						CEP: 22290-180
					</p>
					<p class="w-full font-semibold text-xl pl-6 md:text-lg">
						The meeting will also be broadcasted though CBPF’s YouTube channel:<a
							href="https://
				www.youtube.com/c/CBPFMCTI" class="text-slate-600" external target="_blank"
						> https://
							www.youtube.com/c/CBPFMCTI</a>
					</p>
				</div>
			</div>
		</div>

		<div id="Organization and support">
			<p class="text-center pt-10 pb-4 text-4xl font-bold underline md:text-2xl md:pt-5 md:pb-2">
				Organization and support
			</p>
			<div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-4 p-6">
				<NuxtLink to="" external target="_blank">
					<img class="md:w-80 md:h-80 object-cover w-40 h-40" src="/logo/DMnuLogo.png" alt=" organization and suport">
				</NuxtLink>
				<NuxtLink to="https://icas-brasil.com/" external target="_blank">
					<img class="md:w-80 md:h-70 object-cover w-40 h-35" src="/logo/ICAS_logo.png" alt=" organization and suport">
				</NuxtLink>
				<NuxtLink to="https://www.icifi.unsam.edu.ar/" external target="_blank">
					<img class="md:w-80 md:h-70 object-cover w-40 h-35" src="/logo/ICIFI_logo.png" alt=" organization and suport">
				</NuxtLink>
				<NuxtLink to="https://www.faperj.br/" external target="_blank">
					<img class="md:w-80 md:h-70 object-cover w-40 h-35" src="/logo/index.png" alt=" organization and suport">
				</NuxtLink>
				<NuxtLink to="https://unsam.edu.ar/" external target="_blank">
					<img class="md:w-80 md:h-70 object-cover w-40 h-35" src="/logo/Logo_UNSAM.png" alt=" organization and suport">
				</NuxtLink>
			</div>
		</div>

		<footer class="bg-gray-800 text-white p-6">
			<p class="text-center text-sm">
				Figure credits: CONNIE; Kamiokande; HST; SNO; Zenon; G. Bertone & T. Tait (arXiv:1810.01668);
				meeting logo adapted from Villanueva-Domingo, Mena & Palomares-Ruiz, 2021.
			</p>
		</footer>
	</div>
</template>
