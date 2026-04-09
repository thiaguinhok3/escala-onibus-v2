# TODO — EscalaOnibus

## Setup e Configuração
- [x] Gerar logo do app
- [x] Configurar branding (nome, cores, ícones)
- [x] Configurar tema de cores personalizado
- [x] Configurar estrutura de navegação (Auth + Admin + Motorista)

## Banco de Dados Local (AsyncStorage)
- [x] Schema: usuários (admin + motoristas)
- [x] Schema: escalas diárias
- [x] Schema: ocorrências/relatórios
- [x] Schema: confirmações de visualização
- [x] Seed inicial: admin (admin/admin123)

## Autenticação
- [x] Tela de login
- [x] Contexto de autenticação (AuthContext)
- [x] Detecção de perfil (admin/motorista)
- [x] Persistência de sessão (AsyncStorage)
- [x] Logout

## App Admin — Tab Escalas
- [x] Listagem de escalas do dia com filtro por data
- [x] Cards de resumo (total, aprovadas, pendentes, negadas)
- [x] Criar nova escala (modal com formulário completo)
- [x] Editar escala existente
- [x] Excluir escala
- [x] Aprovar escala
- [x] Negar escala
- [x] Histórico de todas as escalas

## App Admin — Tab Motoristas
- [x] Listagem de motoristas
- [x] Criar motorista (nome, WhatsApp, ID, usuário, senha)
- [x] Editar motorista
- [x] Excluir motorista

## App Admin — Tab Relatórios
- [x] Listagem de ocorrências enviadas pelos motoristas
- [x] Visualizar detalhes da ocorrência
- [x] Marcar como visualizado

## App Admin — Tab Perfil
- [x] Exibir dados do admin
- [x] Alterar senha
- [x] Logout

## App Motorista — Tab Minha Escala
- [x] Card da escala de hoje
- [x] Status visual (aprovada/pendente/negada)
- [x] Confirmar visualização da escala
- [x] Lista de escalas dos próximos 7 dias

## App Motorista — Tab Histórico
- [x] Lista de escalas passadas
- [x] Filtro por período

## App Motorista — Tab Ocorrências
- [x] Formulário para reportar ocorrência
- [x] Lista de ocorrências enviadas

## App Motorista — Tab Perfil
- [x] Exibir dados do motorista
- [x] Alterar senha
- [x] Logout

## Finalização
- [x] Testes unitários (11 testes passando)
- [x] Checkpoint final
- [x] APK disponível para download (via botão Publish)

## Melhorias v1.1
- [x] Notificações push locais ao aprovar/negar escala
- [x] Solicitar permissão de notificação no primeiro acesso
- [x] Exportar relatório de escalas em PDF (Admin)
- [x] Compartilhar PDF via WhatsApp/e-mail
- [x] Filtro por motorista nas escalas do Admin

## Melhorias v1.2
- [x] Escala recorrente — copiar escala para toda a semana ou mês
- [x] Motivo ao negar escala — admin escreve motivo, motorista vê no app
- [x] Dashboard com gráficos — resumo mensal de escalas por motorista

## Melhorias v1.3
- [x] Busca rápida de escalas por motorista, linha ou prefixo
- [x] Escala de folga/férias com cor diferente no calendário
- [x] Comparativo entre meses no Dashboard (mês atual vs anterior)
- [x] Ponto eletrônico — bater ponto de início de serviço
- [x] Ponto eletrônico — bater ponto de pausa (almoço/janta)
- [x] Ponto eletrônico — bater ponto de retorno da pausa
- [x] Ponto eletrônico — bater ponto de término de trabalho
- [x] Admin visualiza registros de ponto dos motoristas
- [ ] Admin pode exportar relatório de ponto em PDF (próxima versão)

## Melhorias v1.4
- [x] CNH fictícia — número, categoria, validade, pontos (máx 40) por motorista
- [x] Admin pode registrar multa (tipo, pontos, valor) na CNH do motorista
- [x] Bloqueio automático quando motorista perde todos os pontos (CNH suspensa)
- [x] Motorista bloqueado vê tela de suspensão com instruções de treinamento
- [x] Admin pode criar treinamento e aprovar conclusão para liberar motorista
- [x] Crachá virtual para cada motorista (nome, foto, ID, linha, status CNH)
- [x] Foto obrigatória ao bater ponto (início, pausa, retorno, término)
- [x] Admin visualiza foto de cada registro de ponto
- [x] Exportar relatório de ponto em PDF (Admin)
- [x] Alerta de jornada excedida (>8h sem registrar término)
- [x] Assinatura por PIN pessoal ao bater ponto

## Melhorias v1.5
- [x] Corrigido: Foto no ponto agora usa compartilhamento nativo (WhatsApp, Email, etc)
- [x] Notificação push ao motorista quando CNH é pontuada (multa registrada)
- [ ] Relatório de CNH em PDF com histórico completo de multas
- [ ] Admin visualiza foto de cada registro de ponto com zoom e data/hora
