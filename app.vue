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

const participants = [
	{ name: 'Agripino Segundo de Sousa Neto', affiliation: 'Observtório Nacional - ON' },
	{ name: 'Álvaro Luis Martins de Almeida Nogueira', affiliation: 'CEFET/RJ' },
	{ name: 'Álvaro Santos de Jesus', affiliation: 'UFRN/IIP' },
	{ name: 'Amanda Evelyn de Araujo Carvalho', affiliation: 'Observatório Valongo-UFRJ' },
	{ name: 'Ana Caroline Chagas de Almeida', affiliation: 'Instituto Oswaldo Cruz - Fiocruz/RJ' },
	{ name: 'Ana Clara Magalhães Barcelos', affiliation: 'Ufmg' },
	{ name: 'Ana Kelly Alves de Oliveira', affiliation: 'Ainda não pertenço' },
	{ name: 'Andre Nepomuceno', affiliation: 'Universidade Federal Fluminense' },
	{ name: 'Anibal Varela', affiliation: 'ICAS-instituto Sabato-UNSAM' },
	{ name: 'Antonio Paulo Fada Maia', affiliation: 'UERJ.' },
	{ name: 'Arianna Cortesi', affiliation: 'Observatório do Valongo' },
	{ name: 'Arman Esmaili Taklimi', affiliation: 'PUC-Rio' },
	{ name: 'Arthur Câmara Mesquita', affiliation: 'CBPF' },
	{ name: 'Arthur Ferreira Vieira', affiliation: 'Universidade Federal Fluminense/University of Southern Denmark' },
	{ name: 'Artur de Santiago Camoleze', affiliation: 'Instituto de Física - Universidade de São Paulo' },
	{ name: 'Barbara Nicole Rosa', affiliation: 'Universidade Estadual de Londrina' },
	{ name: 'Beatriz Sayuri Duval Hashimoto', affiliation: 'IFUSP, São Paulo' },
	{ name: 'Bernardo Fraga', affiliation: 'CBPF' },
	{ name: 'Bernhard Meirose', affiliation: 'Lund University + Stockholm University' },
	{ name: 'Binha Ferraz Dauma', affiliation: 'Universidade Estadual Norte Fluminense | Centro Universitário Internacional' },
	{ name: 'Bruno Carvalho da Silva', affiliation: 'Universidade Federal de Catalao - UFCAT' },
	{ name: 'Bruno Henrique da Silva', affiliation: 'USP' },
	{ name: 'Carlos R. Argüelles', affiliation: 'IALP-UNLP&CONICET' },
	{ name: 'Carlos Roberto de Melo Carneiro', affiliation: 'UFRGS' },
	{ name: 'Cássia da Silva Nascimento', affiliation: 'UFRJ' },
	{ name: 'Clarissa Martins Siqueira', affiliation: 'IFSC/USP' },
	{ name: 'Cristina Furlanetto', affiliation: 'Universidade Federal do Rio Grande do Sul' },
	{ name: 'Cristine Nunes Ferreira', affiliation: 'Instituto Federal Fluminense' },
	{ name: 'Danillo Valentino de Oliveira', affiliation: 'UFRJ' },
	{ name: 'Davi Cabral Rodrigues', affiliation: 'UFES' },
	{ name: 'David Rosa Junior', affiliation: 'Universidade Federal Fluminense' },
	{ name: 'Debora Nascimento Mateus', affiliation: 'UERJ-ZO' },
	{ name: 'Diana López Nacir', affiliation: 'DF-UBA' },
	{ name: 'Dinorah Barbosa da Fonseca Teixeira', affiliation: 'Observatório Nacional' },
	{ name: 'Eddy Ariel Ramirez Trino', affiliation: 'Universidade Federal Fluminense' },
	{ name: 'Eduardo Cypriano', affiliation: 'IAG/USP' },
	{ name: 'Eduardo da Costa Valadão', affiliation: 'CBPF' },
	{ name: 'Elvis Brito Rodrigues', affiliation: 'UFRJ' },
	{ name: 'Fabrício Ladislau Santana', affiliation: 'Estudante' },
	{ name: 'Farinaldo da Silva Queiroz', affiliation: 'International Institute of Physics, UFRN' },
	{ name: 'Felipe Augusto da Silva Barbosa', affiliation: 'UFES' },
	{ name: 'Felipe Bezerra Damasceno', affiliation: 'Universidade Federal da Bahia' },
	{ name: 'Felipe Pereira de Castro', affiliation: 'Universidade Federal do Rio Grande do Sul' },
	{ name: 'Felipe Sobrero Sorage Marques', affiliation: 'CBPF' },
	{ name: 'Fernanda Clara Monteiro Hermes', affiliation: 'Universidade Federal Fluminense' },
	{ name: 'Fernanda Lima Matos', affiliation: 'IFUSP' },
	{ name: 'Fernando Marroquim', affiliation: 'Universidade Federal de Sao Joao del Rei' },
	{ name: 'Gabriel da Silva Moreira Teixeira', affiliation: 'CBPF' },
	{ name: 'Gabriel da Silva Rodrigues', affiliation: 'Observatório Nacional' },
	{ name: 'Gabriel Lopes Garcia', affiliation: 'UFJF' },
	{ name: 'Gabriela Rufino Travassos', affiliation: 'UFRJ - OV' },
	{ name: 'Giulya Souza dos Santos', affiliation: 'Universidade de São Paulo' },
	{ name: 'Graziele Baltar Ferreira Antonio', affiliation: 'ITA' },
	{ name: 'Grecia Alejandra Gomez Iriarte', affiliation: 'cbpf' },
	{ name: 'Greique Ademir Valk', affiliation: 'Federal University of Santa Maria' },
	{ name: 'Guilherme Vieira Donato Teixeira', affiliation: 'UFRJ' },
	{ name: 'Gustavo Adolfo Melgarejo Cedeño', affiliation: 'Universidade do Estado do Rio de Janeiro' },
	{ name: 'Gustavo Gil da Silveira', affiliation: 'UFRGS & UERJ' },
	{ name: 'Gustavo Henrique da Silva', affiliation: 'Ufmg' },
	{ name: 'Gustavo Lourenço Lopes Weiterschan Levy', affiliation: 'CBPF' },
	{ name: 'Gustavo Souza de Castro', affiliation: 'UFRJ' },
	{ name: 'Herman Pessoa Lima Júnior', affiliation: 'CBPF' },
	{ name: 'Ícaro Roberto Gonçalves Pinto', affiliation: 'Usama' },
	{ name: 'Idaiane Leandra Machado', affiliation: 'Ufes' },
	{ name: 'Igor de Oliveira Cardoso Pedreira', affiliation: 'Universidade Federal Fluminense - UFF' },
	{ name: 'Isabel Bonomo Pederneiras Barbosa', affiliation: 'IAG/USP' },
	{ name: 'Isabel Yokoyama Amaral de Faria', affiliation: 'Universidade Federal de Lavras' },
	{ name: 'Isabella Lima Leite de Freitas', affiliation: 'Minerva University' },
	{ name: 'Jaiane da Silva Santos', affiliation: 'Observatório Nacional' },
	{ name: 'João Carlos Adriano Batista', affiliation: 'IFSP' },
	{ name: 'João Delvaux Magalhães', affiliation: 'Universidade Federal Fluminense' },
	{ name: 'João Paulo Correia de França', affiliation: 'CBPF' },
	{ name: 'João Pedro da Cruz Bravo Ferreira', affiliation: 'UFRJ' },
	{ name: 'João Vitor Motta Muniz', affiliation: 'UERJ' },
	{ name: 'Jônathas Samuel Tavares de Souza', affiliation: 'Universidade Federal Fluminense' },
	{ name: 'José Nilson da Silva', affiliation: 'Unifap' },
	{ name: 'José Pereira da Silva Neto', affiliation: 'UFPE' },
	{ name: 'Juan Dennis Tejeira Huacani', affiliation: 'Universidad Mayor de San Andrés' },
	{ name: 'Juliene Vargens Ferreira', affiliation: 'UFRJ' },
	{ name: 'Karín Menéndez-Delmestre', affiliation: 'Observatório do Valongo, UFRJ' },
	{ name: 'Késia de Oliveira Barbosa', affiliation: 'UFRJ' },
	{ name: 'Larayane de Oliveira Moreira Santos', affiliation: 'Universidade Federal Fluminense - UFF' },
	{ name: 'Lauziene Nazareth Barboza', affiliation: 'UFF' },
	{ name: 'Lavínia de Oliveira Pereira Barbosa', affiliation: 'Universidade Federal Fluminense' },
	{ name: 'Laylson Alves Vieira', affiliation: 'Secretaria de Educação do Estado do Ceará-SEDUC' },
	{ name: 'Leonardo da Silva Peres', affiliation: 'UFRJ' },
	{ name: 'Lia Doubrawa', affiliation: 'IAG/USP' },
	{ name: 'Lisandra Souza da Costa dos Santos', affiliation: 'Universidade Federal Do Rio De Janeiro' },
	{ name: 'Lucas Antonio Xavier', affiliation: 'Universidade estadual do Norte Fluminense Darcy Ribeiro' },
	{ name: 'Lucas Corrêa de Souza', affiliation: 'Universidade Federal Fluminense' },
	{ name: 'Lucas Haiashi Lima', affiliation: 'CBPF' },
	{ name: 'Lucas Ribeiro da Silva', affiliation: 'Observatório do Valongo' },
	{ name: 'Lucas Ribeiro da Silva', affiliation: 'IFF' },
	{ name: 'Luiz Carlos Cyrico', affiliation: 'Cbpf' },
	{ name: 'Luiz Filipe Guimarães', affiliation: 'UFES' },
	{ name: 'Luiza Mayara Santos Miranda', affiliation: 'CBPF' },
	{ name: 'Manoel Vicente de Souza Filho', affiliation: 'UFF - Universidade Federal Fluminense' },
	{ name: 'Marcelo Granzotto Campo', affiliation: 'affiliationless' },
	{ name: 'Marcio de Sousa Mateus Junior', affiliation: 'Universidade Federal do Rio Grande do Sul (UFRGS)' },
	{ name: 'Marco Grossi', affiliation: 'Observatório do Valongo, UFRJ' },
	{ name: 'Marcos Henrique Novaes Pereira', affiliation: 'UFES' },
	{ name: 'Maria Aline Barros do Vale', affiliation: 'Universidade Federal de São João del Rei' },
	{ name: 'Maria Clemencia Rosario Mora Herrera', affiliation: 'UERJ / DFNAE' },
	{ name: 'Maria Gabriela Ferreira Siqueira Amaral Gomes', affiliation: 'Universidade Estadual da Paraíba' },
	{ name: 'Mário de Oliveira Ferreira', affiliation: 'CBPF' },
	{ name: 'Martim Lourenço de Oliveira Vieira', affiliation: 'UFF' },
	{ name: 'Mateus Felipe Araújo Medeiros', affiliation: 'UERN' },
	{ name: 'Matheus Filipe Santos Alves', affiliation: 'UFES' },
	{ name: 'Matheus Gomes Pacheco', affiliation: 'UFF' },
	{ name: 'Matheus Rodrigues Xavier', affiliation: 'Universidade Federal do Sergipe' },
	{ name: 'Matheus Weber Cyrico', affiliation: 'UFRJ' },
	{ name: 'Maurício Marques Soares Filho', affiliation: 'CBPF' },
	{ name: 'Mayara Hilgert Pacheco', affiliation: 'Instituto Nacional de Pesquisas Espaciais' },
	{ name: 'Michelly Silva Andrade', affiliation: 'UFJF' },
	{ name: 'Miguel Quartin', affiliation: 'UFRJ' },
	{ name: 'Mikael Jakson Silva Gomes', affiliation: 'Estudante de pós-graduação' },
	{ name: 'Mirian Reetz da Silva', affiliation: 'UFES' },
	{ name: 'Mônica Gonçalves Rocha Ricardo', affiliation: 'Estudante' },
	{ name: 'Murilo Santana Rangel', affiliation: 'Universidade Federal do Rio de Janeiro' },
	{ name: 'Natanael Gomes de Oliveira', affiliation: 'Valongo Observatory, UFRJ' },
	{ name: 'Nelson Padilla', affiliation: 'Instituto de Astronomia Teórica y Experimental (IATE - CONICET/UNC)' },
	{ name: 'Ozgen Tunc Turker', affiliation: 'UFES' },
	{ name: 'Pablo Augusto Ferreira da Luz', affiliation: 'IFF' },
	{ name: 'Patricia Rebello Teles', affiliation: 'CBPF' },
	{ name: 'Patricio Colazo', affiliation: 'Iate' },
	{ name: 'Patrick Belmont Oliveira de Menezes', affiliation: 'UERJ/ON' },
	{ name: 'Pedro Alípio Barreto Batista', affiliation: 'UFRJ - Federal University of Rio de Janeiro' },
	{ name: 'Pedro Cataldi', affiliation: 'IAFE CONICET-UBA' },
	{ name: 'Pedro Feitoza de Araújo Caldas', affiliation: 'UFF' },
	{ name: 'Pedro Zilves Maio Ventura', affiliation: 'IF-UFRJ' },
	{ name: 'Phelipe antonie darc de matos', affiliation: 'CBPF' },
	{ name: 'Prajwal Hassan Puttasiddappa', affiliation: 'UFES' },
	{ name: 'Rafael Antunes Nóbrega', affiliation: 'UFJF' },
	{ name: 'Raimundo José Ferreira FIlho', affiliation: 'Observatório do Valongo' },
	{ name: 'Ramon de Sá Pereira', affiliation: 'UFF' },
	{ name: 'Raphael Gomes de Souza', affiliation: 'UERJ/CERN' },
	{ name: 'Raquel Carvalho Pimentel', affiliation: 'Camtuc – UFPA' },
	{ name: 'Rayff Aby Faraj de Souza', affiliation: 'Observatório Nacional' },
	{ name: 'Rian Ferreira Cavalcante', affiliation: 'Universidade do Estado do Rio Grande do Norte - UERN' },
	{ name: 'Rodrigo von Marttens', affiliation: 'Universidade Federal da Bahia' },
	{ name: 'Rogerio Ferreira Emygdio', affiliation: 'ECEME' },
	{ name: 'Samara Cristina Santos de Oliveira', affiliation: 'Universidade do Estado do Rio de Janeiro' },
	{ name: 'Sergio Lucas Torres Mesquita', affiliation: 'UFRJ' },
	{ name: 'Susana Pedrosa', affiliation: 'IAFE - Conicet/UBA' },
	{ name: 'Thaís da Silva Guerini', affiliation: 'UERJ' },
	{ name: 'Thais Lemos Porciuncula Alves', affiliation: 'Observatorio Nacional' },
	{ name: 'Thales da Silva Domingos', affiliation: 'Federal Fluminense University' },
	{ name: 'Thiago do Carmo Ramos', affiliation: 'IFRJ' },
	{ name: 'Thiago S Goncalves', affiliation: 'Observatório do Valongo, Universidade Federal do Rio de Janeiro' },
	{ name: 'Thiago Souza do Nascimento', affiliation: 'IFRJ - Campus Nilópolis' },
	{ name: 'Tiago Henrique Barbosa Alves', affiliation: 'UFMG - Universidade Federal de Minas Gerais' },
	{ name: 'Ulisses Barres de Almeida', affiliation: 'Centro Brasileiro de Pesquisas Físicas (CBPF)' },
	{ name: 'Vanessa do Nascimento Xavier', affiliation: 'CBPF' },
	{ name: 'Vicente Vecce Lessa Navega Dias', affiliation: 'Instituto Federal Fluminense' },
	{ name: 'Vitor Souza Ramos', affiliation: 'CBPF' },
	{ name: 'Vitória Gabriela Souza Torres', affiliation: 'IFAM - INSTITUTO FEDERAL DO AMAZONAS' },
	{ name: 'Vitória Maria Martins Pitanga', affiliation: 'UFF' },
	{ name: 'Vitória Maria Martins Pitanga', affiliation: 'UFF' },
	{ name: 'Viviane Angélico Pereira Alfradique', affiliation: 'CBPF' },
	{ name: 'Widervan Morais', affiliation: 'CBPF' },
	{ name: 'Widervan Morais', affiliation: 'CBPF' },
	{ name: 'Yasmin Cristina Motta Fernandes', affiliation: 'IFRJ -  UNICSUL' },
]

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
					<span @click="ScrollToDiv(`${item.name}`)">{{ item.name }}</span>
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
			<h2 class="md:text-5xl text-2xl pl-10 pt-12 text-center tracking-wider font-bold underline">
				Rationale
			</h2>
			<div class="flex flex-col md:flex-row items-center">
				<div class="w-full md:w-[800px]  p-10 pr-28 space-y-12 text-lg">
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
					<p class="w-full md:w-[400px] pl-2 text-base">
						Participation is open to students and researchers
						worldwide, which can also propose contributed talks.
						Registration is required to receive the zoom link and to
						attend in person.
					</p>
					<p class="w-full md:w-[400px] pl-2 text-base text-blue-600 cursor-pointer" @click="ScrollToDiv('Program')">
						The recorded talks are available on CBPF’s YouTube channel see the
						programa here
					</p>
				</div>
			</div>
		</div>

		<div id="Topics" class="bg-[#F1F1F1]">
			<h3 class="text-center text-2xl p-10 md:text-5xl font-semibold underline">
				Topics
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
		<div id="Venue" class="bg-[#F1F1F1]">
			<h2 class="md:text-5xl md:pl-10 md:pt-12 tracking-wider font-bold underline text-center pl-5 text-2xl pt-6">
				Venue
			</h2>
			<div class="flex flex-col md:flex-row justify-center items-center pb-6">
				<iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3673.8969020311956!2d-43.1762694248101!3d-22.954023739560753!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x99801d6a53c8cb%3A0xd60303dd37504016!2sR.%20Dr.%20Xavier%20Sigaud%2C%20150%20-%20Urca%2C%20Rio%20de%20Janeiro%20-%20RJ%2C%2022290-180!5e0!3m2!1spt-BR!2sbr!4v1700586194816!5m2!1spt-BR!2sbr" style="border:0;" allowfullscreen loading="lazy" referrerpolicy="no-referrer-when-downgrade" class="rounded-xl md:w-[600px] md:h-[500px] w-[300px] h-[300px] m-4" />
				<div class="space-y-6 md:w-1/2 md:pl-6">
					<p class="w-full font-semibold text-xl pl-6 md:text-lg">
						Brazilian Center for Physics Research - <a
							href="https://www.gov.br/cbpf/pt-br/o-cbpf/como-chegar" class="text-slate-600" external target="_blank"
						> CBPF</a>
						<br>
						<span class="block">Rua Dr. Xavier Sigaud, 150 - Urca</span>
						<span class="block">Rio de Janeiro - RJ - Brasil</span>
						<span class="block">CEP: 22290-180</span>
					</p>
					<p class="w-full font-semibold text-xl pl-6 md:text-lg">
						<a
							href="https://
www.youtube.com/c/CBPFMCTI" class="text-slate-600" external target="_blank"
						>The meeting will also be broadcasted though CBPF’s YouTube channel: </a>
					</p>
				</div>
			</div>
		</div>
		<div id="Registration">
			<div class="text-black text flex flex-col items-center justify-center font-semibold p-7 space-y-4 shadow-xl">
				<p class="text-6xl text-center tracking-wide md:text-4xl">
					Registration deadline
				</p>
				<p class="text-4xl md:text-2xl">
					March 13, 2023
				</p>
			</div>
			<div>
				<h2 class="md:text-5xl md:pl-10 md:pt-12 tracking-wider text-center font-bold underline text-2xl pl-5 pt-6">
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
							Please fill the registration form<a href="https://tinyurl.com/1sRioDMmeeting" external target="_blank" class="text-blue-600">
								here
							</a> by March 15
						</p>
					</div>
				</div>
			</div>
		</div>

		<div>
			<div id="Program" class="bg-[#F1F1F1]">
				<p class="text-center md:pt-10 md:pb-4 md:text-5xl font-bold underline text-2xl pt-5 pb-2">
					Program
				</p>
				<div class="flex flex-col space-y-10 p-7 justify-center items-center">
					<div>
						<p class="text-center text-lg font-bold pb-3">
							<a href="https://www.youtube.com/watch?v=_F6Yqnrk1Q8"> The recorded talks of the rst day of the meeting are available at:
							</a>
						</p>

						<img src="/program/monday.png" alt="program of monday">
					</div>
					<div>
						<p class="text-center text-lg font-bold pb-3">
							<a href="https://www.youtube.com/watch?v=8yB1D_AYOBU"> The recorded talks of the second day of the meeting are available at:
							</a>
						</p>

						<img src="/program/tuesday.png" alt="program of tuesday">
					</div>
					<div>
						<p class="text-center text-lg font-bold pb-3">
							<a href="https://www.youtube.com/watch?v=uMkMT5-IC28">The recorded talks of the third day of the meeting are available at:
							</a>
						</p>

						<img src="/program/wednesday.png" alt="program of wednesday">
					</div>
				</div>
			</div>
		</div>

		<div id="Participants" class="flex flex-col justify-center items-center">
			<h3 class="pt-16 pb-7 md:text-5xl text-2xl text-center font-bold tracking-wider underline">
				Participants
			</h3>
			<div class="container mx-auto">
				<table class="min-w-full mb-12 bg-white border border-gray-300">
					<thead>
						<tr>
							<th class="py-2 px-4 border-b">
								Participantes
							</th>
							<th class="py-2 px-4 border-b">
								Afiliação
							</th>
						</tr>
					</thead>
					<tbody>
						<tr v-for="(participant, index) in participants" :key="index">
							<td class="py-2 px-4 border-b">
								{{ participant.name }}
							</td>
							<td class="py-2 px-4 border-b">
								{{ participant.affiliation }}
							</td>
						</tr>
					</tbody>
				</table>
			</div>
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

		<div id="Organization and support">
			<p class="text-center pt-10 pb-4 md:text-5xl font-bold underline text-2xl md:pt-5 md:pb-2">
				Organization and support
			</p>
			<div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-4 p-6">
				<NuxtLink to="https://www.gov.br/cbpf/pt-br" external target="_blank">
					<img class="md:w-80 md:h-80  w-32 h-32" src="/logo/cbpf.png" alt=" organization and suport">
				</NuxtLink>
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
