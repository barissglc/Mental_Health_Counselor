# zihinsel_Saglik_Danismani_llama3.28b - Zihinsel Sağlık Danışmanı Modeli

Bu proje, **zihinsel sağlık danışmanlığı** yapmak amacıyla fine-tune edilmiş bir dil modelidir.  
`unsloth/Meta-Llama-3.1-8B-Instruct-bnb-4bit` modeline dayanmaktadır ve zihinsel sağlık danışmanlığı konusundaki verilerle eğitilmiştir.

## Eğitim Detayları:

- **Model İsmi:** zihinsel_Saglik_Danismani_llama3.28b
- **Kullanılan Temel Model:** Meta-Llama-3.1-8B-Instruct-bnb-4bit
- **Maksimum Sekans Uzunluğu:** 2048
- **Kullanılan Eğitim Verisi:** Amod/mental_health_counseling_conversations
- **Optimizasyon Algoritması:** AdamW 8-bit
- **Batch Size:** 2
- **Gradient Accumulation Steps:** 4
- **Learning Rate:** 0.0002
- **Num Train Epochs:** 60
- **FP16 Kullandı mı:** Evet
- **BF16 Kullandı mı:** Hayır

## Performans:

- **Son Eğitim Kaybı (Final Training Loss):** 2.2762949109077453
- **Eğitim Süresi:** 642.8567 saniye (10.71 dakika)
- **Model Perplexity:** 9.740523960379797

## Kullanım

Fine-tune edilmiş modeli şu şekilde kullanabilirsiniz:

```python
from unsloth import FastLanguageModel
model, tokenizer = FastLanguageModel.from_pretrained("zihinsel_Saglik_Danismani_llama3.28b")
