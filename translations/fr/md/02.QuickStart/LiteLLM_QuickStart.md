Utiliser [LiteLLM](https://docs.litellm.ai/) pour le modèle Phi-3 peut être un excellent choix, surtout si vous cherchez à l'intégrer dans diverses applications. LiteLLM agit comme un middleware qui traduit les appels API en requêtes compatibles avec différents modèles, y compris Phi-3.

Phi-3 est un petit modèle de langage (SLM) développé par Microsoft, conçu pour être efficace et capable de fonctionner sur des machines aux ressources limitées. Il peut fonctionner sur des CPU avec support AVX et seulement 4 Go de RAM, ce qui en fait une bonne option pour l'inférence locale sans avoir besoin de GPU.

Voici quelques étapes pour commencer avec LiteLLM pour Phi-3 :

1. **Installer LiteLLM** : Vous pouvez installer LiteLLM en utilisant pip :
   ```bash
   pip install litellm
   ```

2. **Configurer les variables d'environnement** : Configurez vos clés API et autres variables d'environnement nécessaires.
   ```python
   import os
   os.environ["OPENAI_API_KEY"] = "your-api-key"
   ```

3. **Faire des appels API** : Utilisez LiteLLM pour faire des appels API au modèle Phi-3.
   ```python
   from litellm import completion

   response = completion(
       model="phi-3",
       messages=[{"role": "user", "content": "Hello, how are you?"}]
   )
   print(response)
   ```

4. **Intégration** : Vous pouvez intégrer LiteLLM avec diverses plateformes comme Nextcloud Assistant, vous permettant d'utiliser Phi-3 pour la génération de texte et d'autres tâches.

**Exemple de code complet pour LLMLite**
[Sample Code Notebook for LLMLite](https://github.com/Azure/azureml-examples/blob/main/sdk/python/foundation-models/phi-3/litellm.ipynb)

**Avertissement**:
Ce document a été traduit en utilisant des services de traduction automatisée par IA. Bien que nous nous efforcions d'assurer l'exactitude, veuillez noter que les traductions automatiques peuvent contenir des erreurs ou des inexactitudes. Le document original dans sa langue d'origine doit être considéré comme la source faisant autorité. Pour des informations critiques, une traduction humaine professionnelle est recommandée. Nous ne sommes pas responsables des malentendus ou des interprétations erronées résultant de l'utilisation de cette traduction.