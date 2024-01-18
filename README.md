# Divisor de Áudio Aleatório

Este script Python utiliza a biblioteca Pydub para dividir arquivos de áudio em segmentos aleatórios, salvando-os em uma pasta específica.

## Instalação

1. Instale as bibliotecas necessárias usando o seguinte comando:
   ```bash
   pip install pydub numpy
   ```

## Uso

1. Configure as pastas de entrada/saída, duração mínima/máxima no código.
2. Execute o script.

## Função Principal

### `dividir_audio_aleatorio(audio_path, duracao_min, duracao_max)`

- **Descrição**: Divide um arquivo de áudio em segmentos aleatórios.
- **Parâmetros**:
  - `audio_path`: Caminho do arquivo de áudio.
  - `duracao_min`: Duração mínima do segmento (em milissegundos).
  - `duracao_max`: Duração máxima do segmento (em milissegundos).

## Configuração

- `pasta_audio`: Diretório dos áudios originais.
- `pasta_audios_divididos`: Diretório para salvar os áudios.

## Execução

Itera sobre os arquivos, divide aleatoriamente e salva os segmentos.

```python
for nome_arquivo in os.listdir(pasta_audio):
    if nome_arquivo.lower().endswith((".mp3", ".wav")):
        audios_divididos = dividir_audio_aleatorio(caminho_audio, duracao_min, duracao_max)
        for i, audio_dividido in enumerate(audios_divididos):
            # Salvar áudio dividido
```

Útil para pré-processamento de dados de áudio antes da classificação ou análise.
