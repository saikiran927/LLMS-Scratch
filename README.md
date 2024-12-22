## Here i Am Building a LLM like chatGPT from scratch for educational purposes using Pytorch I took dataset from notebooks and articles to train LLM

# we will first start with Data Preprocessing and Data Sampling 
 
 # How do you Prepare input Text for Training LLms ?
 * Step1: Splitting Text Into Individual Words (or) Tokens
 * Step2: Convert Tokens into Token IDS
 * Step3: Encode TokenIDS into Vector Representations

 * Implemented Tokenizer class to do all the step as shown in above and also to decode tokenids into text and i also special text tokens like <|UNK|> and <|EndofText|> which helps us to process input text when it is not present in bag of words

 # Create Input - Target Pairs

 * we take token Ids of tokens and create Input and Outpairs for the entire dataset with the help of Dataset and DataLoader in PyTorch.
 * Dataset and DataLoader converts input and output pairs into pytorch tensors returns the Pytorch tensors as output. 

 # Positional Encoding

 * In the embedding layer, the same tokenID gets mapped to the same embedding vector Representation regardless of the tokenId position in input sequence
 * It is helpful to inject additional positional information to the LLM.
 * 2 Types of Positional Encoding
 * 1) Absolute positional Embedding
 * 2) Relative Positional Embedding

 # Absolute Positional Encoding

 * In absolute encoding for each position in input sequence a unique embedding is added to the token embedding to convey its exact location.
 * Positional vectors in absolute encoding have the same dimension as the original token embeddings
 * Suitable when you have fixed order of tokens is crucial.
 * Gpt also Uses absolute positional encoding 

# Relative Positional Encoding

* The emphasis is on the relative position or distance between tokens the model learns the relationships in terms of how far apart rather than at which exact position.
* Model can generalize better to sequence of varying length, even if it has not seen such lengths during training.

* Both types of positional encoding enables the LLMs to understand the order and relationship between tokens ,ensuring more accurate and context aware predictions. 
