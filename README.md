# Projetos de aprendizagem de máquina — entrega parcial

Este repositório reúne três atividades em notebooks, organizadas como uma entrega parcial para acompanhamento e continuidade. Elas exploram reconhecimento de imagens e aprendizagem de máquina de maneira prática. Os números abaixo são **resultados registrados no material recebido**, não uma nova execução neste repositório.

## Integrantes do grupo e autoria

Os projetos e conteúdos deste repositório foram produzidos em conjunto pelos integrantes do grupo:

- **[Igor](https://github.com/igorhellmanmelo)**
- **[Raul Milan](https://github.com/Raul-Milan)**

Igor e Raul Milan são coautores dos conteúdos apresentados. O trabalho reúne a contribuição de ambos no desenvolvimento das atividades e na produção dos materiais do grupo.

## Objetivo das atividades extensionistas

A extensão universitária aproxima o conhecimento produzido na faculdade das necessidades e experiências de pessoas fora dela. A proposta destas atividades é transformar exercícios técnicos em oportunidades de diálogo, demonstração e aprendizagem com a comunidade. Em vez de apresentar a inteligência artificial como uma solução pronta, os projetos podem servir para explicar, com exemplos simples, como um sistema aprende a partir de dados, por que comete erros e quais cuidados são necessários antes de usá-lo em situações reais.

O reconhecimento de números permite conversar sobre aplicações como leitura automática de formulários e digitalização de informações. O Jokenpô com webcam oferece uma demonstração interativa: quem participa pode observar como mudanças de iluminação, posição da mão e diversidade das imagens afetam o resultado. Essas atividades podem apoiar oficinas introdutórias, apresentações abertas e conversas sobre tecnologia, estimulando a curiosidade e o pensamento crítico de públicos com diferentes níveis de familiaridade com programação.

O objetivo social é contribuir para que mais pessoas compreendam e discutam tecnologias que já aparecem no cotidiano. Ao levar protótipos e explicações para além do ambiente acadêmico, a equipe também pode ouvir dúvidas, dificuldades e sugestões da comunidade. Essa troca ajuda a tornar o trabalho mais acessível e orienta melhorias nos projetos. Uma ação extensionista completa precisa registrar com quem essa troca ocorreu, o que foi realizado e qual retorno foi recebido; os experimentos publicados aqui representam a preparação técnica para essa etapa.

| Projeto | Conteúdo | Estado da reprodução |
| --- | --- | --- |
| [Atividade 2: KNN e dígitos](projetos/atividade-2-knn/) | Classificação de imagens 8×8 e relatório no notebook | Código disponível; o conjunto de 1.000 imagens usado no resultado original não veio no ZIP. |
| [Jokenpô com CNN](projetos/jokenpo-cnn/) | Coleta pela webcam, treino TensorFlow, comparação com augmentation e notebook alternativo em PyTorch | Código e resultados de teste disponíveis; capturas brutas de mãos e modelos treinados ficaram fora desta edição pública. Requer webcam e coleta de dados para executar integralmente. |
| [Números e redes neurais](projetos/numeros-redes-neurais/) | Comparação MLP × KNN em `digits` e 100 imagens adicionais | Notebook e ZIP das 100 imagens disponíveis; exige as dependências Python. |

## Evidências e continuidade

- [Índice de evidências](evidencias/README.md): arquivos e o que comprovam.
- [Handoff técnico](HANDOFF.md): ambiente, execução, limitações e próximas tarefas.
- [Dependências](requirements.txt): bibliotecas usadas nos notebooks.

As evidências técnicas registram experimentos acadêmicos. O material fornecido não contém comprovação de atividade com comunidade externa, público atendido, consentimento ou avaliação de impacto; esses elementos devem ser reunidos separadamente para uma prestação de contas extensionista.

## Execução rápida

```bash
python -m venv .venv
# Linux/macOS: source .venv/bin/activate
# Windows: .venv\Scripts\activate
python -m pip install -r requirements.txt
jupyter lab
```

Abra o notebook desejado e execute as células em ordem a partir da pasta do projeto correspondente. A etapa de webcam exige um computador com câmera e interface gráfica. Consulte o [handoff](HANDOFF.md) antes de treinar novamente.

Não há licença de redistribuição definida no material recebido. Solicite ao responsável a definição da licença e a confirmação da origem/permissão de publicação das 100 imagens de dígitos antes de reutilizá-las fora do projeto.
