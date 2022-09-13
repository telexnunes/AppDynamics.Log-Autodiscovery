# AppDynamics.Log-Autodiscovery
Extension no Machine Agent:
 
	1 Será executada a cada 5 minutos.
	2 Critério para identificar o arquivo de log e seu caminho automaticamente:
		a	Verificar os processos abertos no SO, deve tiver na linha de comando o agente do AppDynamics e for um Servidor de Aplicação (Tomcat, JBoss, etc).
		b	Identificar os arquivos de logs do Servidor de Aplicação encontrado, seja verificando se existem arquivos abertos pelo processo do SO, identificando o arquivo através de propriedades do processo ou qualquer outra forma.
		c Chamar as API's para criar uma Source Rule (simulando a navegação do usuário). Navegar na UI com F12 do Browser apertado para verificar quais APIs são chamadas, elas não são documentadas.
		d Configurar na Source Rule o template do arquivo conforme o Servidor de Aplicação identificado (Tomcat, etc.).
	3 Antes de criar a regra é necessário verificar se ela já existe, para não criar regra duplicada.
	4 A extensão será responsável apenas para encontrar os arquivos e configurar a Source Rule, ainda será necessário instalar o agente de Log Analytics.
 
