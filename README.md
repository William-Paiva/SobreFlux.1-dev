# FLUX.1 [dev] - Modelo de Texto para Imagem


Todos os modelos públicos FLUX.1 são construídos em uma arquitetura híbrida que combina blocos de transformadores de difusão multimodais e paralelos, dimensionados para impressionantes 12 bilhões de parâmetros. Isso representa um salto significativo no tamanho e na complexidade do modelo em comparação com muitos modelos de texto para imagem existentes.

Os modelos Flux melhoram os modelos de difusão de última geração ao incorporar a correspondência de fluxo, um método geral e conceitualmente simples para treinar modelos generativos. A correspondência de fluxo fornece uma estrutura mais flexível para modelagem generativa, sendo os modelos de difusão um caso especial dentro desta abordagem mais ampla.

Para melhorar o desempenho do modelo e a eficiência do hardware, o Black Forest Labs integrou incorporações posicionais rotativas e camadas de atenção paralelas. Essas técnicas permitem um melhor manuseio das relações espaciais nas imagens e um processamento mais eficiente de dados em grande escala.

O FLUX.1 [dev] é um modelo de IA de ponta capaz de gerar imagens realistas a partir de descrições textuais. Com 12 bilhões de parâmetros, ele oferece resultados impressionantes e versáteis.

## Características Principais
* **Qualidade de imagem superior:** Gerador de imagens de alta resolução e detalhadas.
* **Compreensão precisa de prompts:** Siga instruções complexas e nuances em suas descrições.
* **Treinamento eficiente:** Alcançe de resultados excepcionais com maior eficiência computacional.
* **Código aberto:** Incentivador de pesquisas e desenvolvimento de novas aplicações.
* **Licença flexível:** Utilização das imagens geradas para diversos fins.
* https://huggingface.co/black-forest-labs/FLUX.1-dev/blob/main/LICENSE.md

## Como Usar
* **Implementação de referência:** O código base esá no repositório oficial.
* **APIs:** Utilização das APIs fornecidas por bfl.ml, replicate.com, fal.ai e mystic.ai.
* **ComfyUI:** Interface visual intuitiva para gerar imagens.
* **Diffusers:** Integração do modelo em seus projetos Python com a biblioteca diffusers.

```
pip install -U diffusers

import torch
from diffusers import FluxPipeline

pipe = FluxPipeline.from_pretrained("black-forest-labs/FLUX.1-dev", torch_dtype=torch.bfloat16)
pipe.enable_model_cpu_offload() #save some VRAM by offloading the model to CPU. Remove this if you have enough GPU power

prompt = "A cat holding a sign that says hello world"
image = pipe(
    prompt,
    height=1024,
    width=1024,
    guidance_scale=3.5,
    num_inference_steps=50,
    max_sequence_length=512,
    generator=torch.Generator("cpu").manual_seed(0)
).images[0]
image.save("flux-dev.png")
```


## Limitações e Uso Adequado
* **Informações factuais:** O modelo não é uma fonte de informações confiáveis.
* **Viés:** Pode refletir os vieses presentes nos dados de treinamento.
* **Dependência do prompt:** A qualidade da imagem depende da qualidade da descrição.

**Uso proibido:**
* Violação de leis.
* Conteúdo prejudicial a menores.
* Desinformação e notícias falsas.
* Violação de privacidade.
* Assédio e ameaças.
* Conteúdo pornográfico não consensual.
* Decisões automatizadas que violem direitos.
* Campanhas de desinformação em larga escala.

# FLUX.1 [dev]

## Resultados Impressionantes

![Uma imagem incrível gerada pelo FLUX.1 [dev]](https://github.com/William-Paiva/SobreFlux.1-dev/blob/main/images/dev_grid.jpg)

## Imagem abstrata criada por texto

![Cena de ação dinâmica com integração de texto: “Um super-herói irrompendo em uma página de quadrinhos. As linhas de ação e os efeitos sonoros devem formar o nome do herói ‘FLUX FORCE’ em tipografia ousada e dinâmica.”](https://github.com/William-Paiva/SobreFlux.1-dev/blob/main/Captura%20de%20Tela%20(5).png)


Conheça mais sobre: https://huggingface.co/black-forest-labs/FLUX.1-dev



