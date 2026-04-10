# Prompt Engineering Playground

Premier projet de la série LLM — avant de toucher au RAG,
j'ai voulu comprendre ce qu'un LLM peut faire avec juste un prompt, sans rien d'autre.

## Ce que j'ai testé

- Prompts simples et vagues
- Role-based prompts ("Tu es un expert en...")
- Instructions de format strict (bullet points, JSON)
- Contraintes de refus ("réponds je ne sais pas si tu n'es pas sûr")

## Ce que j'ai compris

Le prompt seul ne suffit pas. Le modèle suit les instructions de façon probabiliste,
pas logique — il peut ignorer une contrainte explicite juste parce que
statistiquement il a rarement vu ce pattern dans son entraînement.

C'est ce projet qui m'a poussé vers le RAG : pas parce que c'est à la mode,
mais parce que j'ai vu concrètement pourquoi le prompt seul a des limites.

## Stack

Python · HuggingFace Transformers · FLAN-T5 · Google Colab
