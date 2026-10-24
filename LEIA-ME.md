# Ritmo — controle pessoal de estudos

Aplicativo gratuito, sem cadastro, sem dependências externas e sem compilação. Arquivos HTML, CSS e JavaScript prontos para hospedar. O plano contém as 72 sessões enviadas pela usuária: 26/10/2026 a 16/01/2027, seis sessões semanais. A cobertura dos editais oficiais de TRT SP/RJ/MG e TCE-SP não foi verificada; o aplicativo não substitui os editais.

## Começar no computador

Para uma consulta rápida, abra index.html. O modo instalado e o funcionamento offline exigem HTTPS ou servidor local; não funcionam abrindo apenas o arquivo. Para usar o servidor local opcional, instale Node.js, dê dois cliques em INICIAR.cmd e abra http://localhost:8080. Mantenha a janela aberta durante o uso; Ctrl+C encerra. Não é preciso instalar pacotes. Use sempre o mesmo endereço: dados de file://, localhost e GitHub Pages são separados.

## Publicar gratuitamente no GitHub Pages

1. Entre em https://github.com e crie um repositório **público**, por exemplo ritmo-estudos. GitHub Free oferece Pages para repositórios públicos.
2. Extraia o ZIP. No repositório, escolha Add file → Upload files e envie **o conteúdo** da pasta ritmo-estudos, não a pasta inteira. index.html deve ficar na raiz. Não envie seus backups pessoais.
3. Salve em Commit changes. Abra Settings → Pages.
4. Em Build and deployment, escolha Deploy from a branch. Selecione main e /(root), depois Save.
5. Aguarde a publicação e abra o endereço mostrado pelo GitHub, normalmente https://SEU-USUARIO.github.io/ritmo-estudos/.
6. Abra uma vez com internet e aguarde alguns segundos para preparar o uso offline. Se necessário, recarregue uma vez.

Referência oficial: https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site

## Instalar no celular ou computador

- Android: abra o endereço publicado no Chrome → menu ⋮ → Instalar aplicativo ou Adicionar à tela inicial.
- iPhone/iPad: abra no Safari → Compartilhar → Adicionar à Tela de Início.
- Computador: abra no Chrome ou Edge e use o ícone de instalação na barra de endereço ou a opção Instalar aplicativo no menu. O botão Instalar também aparece no aplicativo quando o navegador oferece essa possibilidade.
- Não há loja, assinatura ou conta no aplicativo. As opções de instalação variam conforme o navegador.

Referência: https://developer.mozilla.org/en-US/docs/Web/Progressive_web_apps/Guides/Making_PWAs_installable

## Como estudar

- O painel abre a primeira sessão pendente. Use Meu ciclo para abrir qualquer outra; filtros permitem buscar semana, disciplina e situação.
- As datas são referências. Pular um dia não apaga nem pula matérias. Domingo fica livre para descanso ou recuperação.
- Iniciar/retomar conta o tempo até Pausar. O contador continua com a tela fechada e é recuperado ao reabrir. Pause em intervalos para não contar tempo extra. Abrir outra sessão pausa o contador anterior.
- Salvar registro **adiciona** as novas questões, acertos e minutos manuais ao acumulado; as anotações são atualizadas. Os campos numéricos voltam a zero para evitar somar duas vezes.
- Concluir sessão cria revisões em 1, 7 e 30 dias, contadas da data real de conclusão, e sugere a próxima pendente.
- Revisões ficam na aba Revisões, inclusive as atrasadas. Marque cada uma como revisada. Não há notificações com o aplicativo fechado.
- Reabrir uma sessão remove suas revisões, mantendo tempo, questões e anotações. Você pode desfazer uma revisão marcada.
- Editar assunto permite alterar disciplina e conteúdo de qualquer sessão. A estrutura continua com 72 sessões.

## Backup e dispositivos — importante

**O armazenamento é local e NÃO sincroniza automaticamente entre dispositivos.** Cada navegador e endereço tem seus próprios dados. Exporte regularmente em Meus dados → Exportar backup JSON. No outro dispositivo, abra o aplicativo → Meus dados → Importar backup JSON. A importação substitui tudo após confirmação; não combina registros. Exporte antes de importar se quiser guardar a versão atual.

Limpar os dados do site, usar navegação anônima ou trocar de endereço/navegador pode remover ou tornar inacessível o progresso. O aplicativo avisa quando não consegue salvar. Não use simultaneamente em várias abas, pois uma pode sobrescrever a outra. Os arquivos de backup contêm suas anotações: mantenha-os privados.

## Atualizações

Exporte um backup antes de atualizar os arquivos. Para alterar o aplicativo, envie os novos arquivos ao mesmo repositório/endereço. Em atualizações do conteúdo offline, altere CACHE em sw.js (por exemplo, ritmo-shell-v2). Feche as abas e reabra com internet para concluir a troca de versão. Os dados locais são separados do cache do aplicativo.

## Arquivos

index.html, style.css, app.js e plan.js: aplicativo e plano; manifest.webmanifest, sw.js e ícones: instalação/offline; server.cjs e INICIAR.cmd: execução local opcional; .nojekyll: publicação estática. Nenhum serviço externo é chamado para registrar seus estudos.

## Apostilas em PDF (versão 2)

Na aba **Apostilas**, escolha um PDF de até 50 MB e indique onde ele deve aparecer: em todas as sessões de uma disciplina ou somente em uma sessão específica. Clique em **Salvar apostila**. Você também pode fazer isso diretamente no painel, em **Apostilas desta sessão**.

Exemplo: vincule sua apostila à disciplina Português. Ela aparecerá na sessão 1 e nas outras sessões de Português. Para uma apostila exclusiva de interpretação de textos, escolha somente a sessão 1.

Use **Abrir PDF** para ler dentro do aplicativo. Alguns navegadores de celular não mostram PDFs dentro da tela: nesse caso, use **Abrir em nova aba** ou **Baixar PDF**. Não há extração automática de capítulos nem marcação de páginas nesta versão.

Os arquivos ficam no armazenamento local de PDFs do navegador (IndexedDB), sem envio ao GitHub ou a servidores. Podem ser acessados offline após adicionados, desde que o aplicativo já esteja disponível offline. O espaço depende do navegador. **O backup JSON de progresso não inclui PDFs.** Guarde os originais, baixe cópias pela biblioteca e adicione novamente no outro aparelho. Limpar os dados do site também apaga a biblioteca. Editar o nome de uma disciplina exige vincular novamente os PDFs associados àquele nome; os PDFs associados pelo número da sessão continuam vinculados.
