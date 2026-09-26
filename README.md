# Projetos de aprendizagem de máquina — entrega parcial

Três atividades em notebooks, organizadas para acompanhamento e continuidade. Os números abaixo são **resultados registrados no material recebido**, não uma nova execução neste repositório.

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
