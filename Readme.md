# 🎓 Plataforma de Gestão de Eventos Escolares & Controlo de Acessos
---

## 📌 Funcionalidades Principais

 1. Gestão e Inscrição (Painel Web)
* **Criação de Eventos (Administração / Associação / Professores):**
  * Suporte para palestras, torneios ou exibições.
  * Configuração de data, janela horária (início/fim), local e lotação máxima opcional.
  * Ativação ou desativação parametrizável da emissão de certificados.
* **Modalidades de Inscrição:**
  * **Por Turma:** O professor inscreve a turma inteira no bloco de aulas correspondente.

---

### 2. Geração e Distribuição de Credenciais
* **QR Code Dinâmico:** Geração automática de um QR Code único enviado por e-mail e disponibilizado na área pessoal do aluno.
* **Integração com Cartão Escolar:** Compatibilidade com o cartão físico da escola , associado ao número do aluno.

---

### 3. Check-in e Validação na Entrada (Ponto de Acesso)
Validação instantânea no terminal de leitura com feedback audiovisual e atualização de estado na base de dados:

* 🟢 **Sinal Verde + Apito Suave (Entrada Autorizada):**
  * **Mensagem no Ecrã:** `Entrada Autorizada - [Nome do Aluno] ([Turma])`
  * Registo do *timestamp* de entrada e alteração do bilhete para o estado `Utilizado`.
* 🔴 **Sinal Vermelho + Apito de Erro (Entrada Recusada):**
  * **Credencial Reutilizada:** `Acesso Negado: Bilhete já validado às [Hora]`
  * **Ausência de Inscrição:** `Acesso Negado: Aluno não inscrito neste evento`
  * **Fora de Horário:** `Acesso Negado: Evento fora do horário de acesso ou encerrado`

---

### 4. Painel do Professor em Tempo Real
Acompanhamento contínuo da assiduidade da turma via WebSockets/Socket.io durante o período letivo:

* **Métricas em Tempo Real:**
  * 🟩 **Presentes (Verdes):** Alunos que efetuaram check-in no ponto de acesso.
  * 🟥 **Ausentes (Vermelhos):** Alunos inscritos que ainda não passaram no leitor.
* **Ações de Controlo:**
  * **Registo Manual:** Permite ao professor assinalar manualmente a presença em situações excecionais (ex.: esquecimento do cartão/telemóvel).
  * **Exportação de Dados:** Exportação das presenças e faltas em PDF ou Excel para sincronização com a caderneta escolar.

---

### 5. Módulo Final: Emissão de Certificados
* **Geração Automática:** Disponibilização automática do certificado em PDF para download aos alunos com estado de presença confirmado (`Utilizado`).
  
---

