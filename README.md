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


