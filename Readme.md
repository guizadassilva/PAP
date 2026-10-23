1. Gestão e Inscrição (Painel Web)
Criação de Eventos (Administração / Associação / Professores):

Criação de palestras, torneios, workshops ou exibições.

Definição de data, horário de início/fim, local e lotação máxima (opcional).

Ativação/desativação da opção de Emissão de Certificado de Presença.

Modalidades de Inscrição:

Por Turma: Um professor pode inscrever a sua turma inteira num evento que decorra durante o seu bloco de aulas. O sistema valida automaticamente se algum aluno já está inscrito para evitar duplicados.

Individual: O próprio aluno pode inscrever-se diretamente através da web/app.

2. Geração e Distribuição de Credenciais (Web / App / Cartão)
QR Code Dinâmico: Assim que a inscrição é confirmada, é gerado um QR Code único e encriptado (hash com timestamp) enviado por e-mail e disponibilizado na área pessoal/app do aluno.

Integração com Cartão da Escola (NFC / RFID / Barcode): O aluno pode optar por usar o seu cartão físico da escola, associado ao seu número de aluno na base de dados.

3. Check-in e Validação na Entrada (Ponto de Acesso / Leitor)
À entrada do auditório/espaço, o leitor (QR Code ou Cartão da Escola) faz a validação instantânea no ecrã com feedback visual e sonoro:

Sinal Verde + Apito Suave (Entrada Autorizada):

Ecrã: "Entrada Autorizada - [Nome do Aluno] ([Turma])"

O sistema regista a hora exata de entrada e altera o estado do bilhete para "Utilizado".

Sinal Vermelho + Apito de Erro (Entrada Recusada):

QR Code ou Cartão já Utilizado: "Acesso Negado: Bilhete já validado às [Hora de Entrada]"

Aluno Não Inscrito: "Acesso Negado: Aluno não inscrito neste evento"

Fora de Horário: "Acesso Negado: Evento fora do horário de acesso ou já encerrado"

4. Painel do Professor em Tempo Real (Web / App)
O professor acompanha em tempo real a comparência da sua turma durante o seu bloco de aulas:

Métricas em Tempo Real (WebSockets / Socket.io):

Verdes (Presentes): Alunos que já passaram no leitor e estão na sala.

Vermelhos / Alertas (Ausentes): Alunos da turma inscritos que ainda não fizeram check-in.

Ações de Controlo:

Marcador Manual: O professor pode marcar presença manualmente caso o aluno tenha esquecido o cartão/telemóvel.

Exportação de Faltas: Geração de ficheiro (PDF/Excel) com o registo de presenças/faltas para integração com a caderneta escolar.

5. Módulo Final: Emissão de Certificados
Geração Automática: Se o evento tiver a opção de certificado ativa, o sistema disponibiliza o PDF para download aos alunos cujo bilhete esteja marcado como "Utilizado".

