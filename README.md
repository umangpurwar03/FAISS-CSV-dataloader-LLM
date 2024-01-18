# FAISS CSV DataLoader for LangChain

This repository contains a Python script (`csv_data_loader.py`) that demonstrates how to use LangChain for processing CSV files, splitting text documents, and creating a FAISS (Facebook AI Similarity Search) vector store. This script leverages the LangChain library for embeddings and vector stores and utilizes multithreading for parallel processing.

## Requirements

- [LangChain](https://github.com/langchain-ai): LangChain is a library for natural language processing tasks, including document loading, text splitting, and vector stores.
- [FAISS](https://github.com/facebookresearch/faiss): FAISS is a library for efficient similarity search and clustering of dense vectors.

## Installation

1. Install LangChain, FAISS and all other requirementsusing the following commands:

   ```bash
   pip install langchain
   pip install faiss
   pip install -r requirements.txt
   ```

2. Clone this repository:

   ```bash
   git clone https://github.com/umangpurwar03/FAISS-CSV-dataloader-LLM
   ```

3. Navigate to the repository directory:

   ```bash
   cd FAISS-CSV-dataloader-LLM
   ```

## Usage

1. Modify the `data_dir` variable in `csv_dataloader.py` to point to the directory containing your CSV files.

2. Run the script:

   ```bash
   python csv_dataloader.py
   ```

This script will process each CSV file in parallel using multithreading, loading the data, splitting the text into chunks, creating embeddings using Hugging Face models, and finally, storing the vectors in a FAISS vector store.

## Customization

- You can customize the model used for embeddings by modifying the `model_name` parameter in the `HuggingFaceEmbeddings` initialization.

- Adjust the chunk size and overlap in the `RecursiveCharacterTextSplitter` initialization according to your requirements.

- Feel free to customize other parameters and configurations based on your specific use case.

## Multithreading

The script uses multithreading to process multiple CSV files concurrently. The `process_csv_files_in_parallel` function initializes a separate thread for each CSV file, allowing for efficient parallel processing. Adjust the number of threads based on your system's capabilities and requirements.

## License

This code is released under the [MIT License](LICENSE). Feel free to use and modify it according to your needs.

## Acknowledgments

- [LangChain](https://github.com/langchain-ai)
- [FAISS](https://github.com/facebookresearch/faiss)

If you find this code helpful or have suggestions for improvement, please feel free to contribute or open an issue.
