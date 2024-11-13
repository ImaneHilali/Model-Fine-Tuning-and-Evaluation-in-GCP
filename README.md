## Fine-Tuning and Evaluation of NLLB-200 for Multilingual Machine Translation on GCP
In this project, I fine-tuned the NLLB-200 model, a powerful multilingual transformer model, using a translation dataset stored in Google Cloud Storage (GCS). The dataset consists of train, validation, and test sets in JSONL format, representing parallel text in different languages. The model is fine-tuned using the Hugging Face transformers library, with specific preprocessing steps to tokenize the source and target texts according to the language pairs defined in the dataset.

The training process is executed on Google Cloud, using custom training arguments that allow for efficient management of model checkpoints and evaluation steps. After every few steps, the model's progress is saved and uploaded to a GCS bucket, ensuring that the training can resume seamlessly. The fine-tuned model is evaluated using standard metrics like BLEU and ROUGE scores, and the results help gauge the effectiveness of the translation.

This project leverages various GCP services such as Google Cloud Storage for data storage, cloud-based model training, and seamless upload of model checkpoints and evaluation results. The use of a custom UploadCheckpointToGCS callback ensures that model checkpoints are consistently backed up to GCS, while the integration of early stopping helps prevent overfitting. The final output is a robust multilingual translation model deployed on GCP that can be used for various translation tasks.

Additionally, the trained model can be pushed to platforms like Hugging Face Hub for broader use, offering a high-quality multilingual translation service.






