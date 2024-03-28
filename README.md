# Text2ImageDescription
The project has 2 main parts:
1. Image Retrieval: Given a text query, retrieve images from a dataset that are relevant to the query.
2. Image Description Generation: Given a text query, generate a description for the image that is most relevant to the query.

## Image Retrieval
The image retrieval part of the project uses a pre-trained openai CLIP model(https://github.com/openai/clip) to retrieve images from a dataset that are relevant to a given text query. The dataset used for this project is the [Pascal VOC 2012 dataset](https://huggingface.co/datasets/nateraw/pascal-voc-2012). The dataset contains around 3500 images (train + validation). The CLIP model is used to encode the text query and the images in the dataset. The similarity between the text query and the images is calculated using cosine similarity. The images are then ranked based on the similarity score and the top k images are returned.

## Image Description Generation
The image description generation part of the project uses a pre-trained Mistral-7b (https://huggingface.co/TheBloke/Mistral-7B-Instruct-v0.1-GGUF) model to generate descriptions for the give input query. 

## Usage
To run the project, follow the steps below:
1. Clone the repository
2. Run the notebook `code.ipynb`

## Performane
Resource: 12 GB GPU (nvidia T4)
Image search: ~ 50 milliseconds.
Description generation: Streaming starts within approximately 2.5 seconds, achieving a rate of 40 tokens per second.

## Results
Check out the demo video to see Text2ImageDescription in action:

https://github.com/mahadev0811/Text2ImageDescription/assets/124283478/cd2a16a5-4e52-49f0-bfec-192ef7e73fd5

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

