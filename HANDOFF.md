# Handoff técnico para o próximo módulo

## Ponto de partida

- Os notebooks foram copiados do ZIP recebido. No notebook TensorFlow do Jokenpô, somente saídas de execução foram removidas porque uma delas continha caminho local de usuário; o código foi preservado. As tabelas e gráficos de avaliação foram separados em `evidencias/`.
- A versão pública parcial não contém as 150 fotos de mãos nem os dois modelos `.keras` (cerca de 13 MB cada). A coleta e o treinamento podem ser repetidos com o notebook e dados autorizados.
- A atividade KNN inicial espera arquivos `dataset/0_*.png` a `dataset/9_*.png` (também aceita JPG/JPEG). Essa pasta não constava do ZIP, embora o notebook mostre saída de uma execução com 1.000 imagens. Não inferir que 87,20% seja reproduzível sem os dados originais.
- O projeto de números tem `dataset_mnist_100.zip` com 100 PNGs distribuídos igualmente entre os dígitos de 0 a 9; o notebook extrai as imagens para `imagens_usuario/` na primeira execução.

## Ambiente e execução

1. Criar ambiente virtual Python, instalar `requirements.txt` e iniciar `jupyter lab` na raiz do repositório.
2. Em cada projeto, abrir o terminal na própria pasta e executar o respectivo notebook em ordem. Todos usam caminhos relativos ao diretório de execução.
3. Em `numeros-redes-neurais`, abrir `numeros_redes_neurais.ipynb`; o notebook compara MLP e KNN com semente 42 e separação estratificada de 25% para teste. Confirmar a origem e licença das imagens antes de reutilizar em outro contexto.
4. Em `atividade-2-knn`, providenciar o dataset original ou adaptar o notebook para imagens com nomes `0_*` a `9_*` em `dataset/`; verificar pelo menos duas amostras por classe para a divisão estratificada. O notebook recebido não contém uma verificação explícita dessa condição.
5. Em `jokenpo-cnn`, usar `jokenpo_deep_learning_tempo_real.ipynb` como fluxo TensorFlow principal. Capturar no mínimo 45 imagens por classe (`PEDRA`, `PAPEL`, `TESOURA`), conferir rótulos/duplicatas, preservar a separação teste e avaliar baseline e augmentation. O notebook `aula05_extra_jokenpo_cnn.ipynb` é um roteiro alternativo PyTorch e espera **outra pasta**, `jokenpo_dataset/`.
6. Para testes com webcam, executar localmente com câmera disponível; registrar cada rodada com gesto real, previsto, condição, confiança e data. Não tratar CSVs vazios como testes concluídos.

## Resultados existentes e limites

| Experimento | Registro no material | Próxima validação |
| --- | --- | --- |
| Atividade 2, KNN | 87,20% em 250 amostras de teste, saída do notebook e captura | Recuperar as 1.000 imagens ou repetir com um conjunto documentado. |
| Jokenpô, teste fixo | Baseline 66,67%; augmentation 46,67% em 30 amostras | Confirmar separação por sessão/pessoa para reduzir vazamento entre quadros semelhantes; repetir com novas pessoas e iluminação. |
| Jokenpô, iluminação fraca | Campos de acurácia e confiança vazios | Fazer teste antes/depois sob condição definida, registrar dez rodadas e revisar a conclusão. |
| Números, 100 imagens | KNN 68% e MLP 60% no teste de 25 imagens quando treinados nelas; treinados em `digits`, 32% e 28% no mesmo teste | Repetir divisões e avaliar incerteza; registrar procedência das imagens. |

## Próximas entregas

1. Documentar autorização de publicação, procedência/licença dos dados e licença do código.
2. Registrar e organizar evidências da ação extensionista real: público, parceiro, cronograma, intervenções, feedback e impacto, sem expor dados pessoais.
3. Definir protocolo de validação de generalização por pessoa/sessão e condições de iluminação, com CSVs preenchidos e conclusões revisadas.
4. Fixar versões das dependências após executar os três projetos em ambiente limpo; adicionar comandos reprodutíveis de coleta e avaliação.
5. Disponibilizar modelos e dados somente se houver autorização adequada, com instruções de obtenção quando não puderem ser públicos.

## Publicar no GitHub

Criar um repositório **público vazio** na conta de destino. A partir da pasta `publicacao-git`:

```bash
git init -b main
git add .
git commit -m "Organiza entrega parcial dos tres projetos"
git remote add origin https://github.com/USUARIO/NOME-DO-REPOSITORIO.git
git push -u origin main
```

Antes do `git push`, conferir `git status` e `git diff --cached --stat`. Para enviar arquivos pela interface web do GitHub, extraia o ZIP e arraste o **conteúdo da pasta** `publicacao-git`, incluindo as três pastas em `projetos/`; a interface pode limitar quantidade e tamanho de arquivos, então Git local é mais confiável.
