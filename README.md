PROJECT NAME : Lyric Search Engine

project description:
	Users will have pieces of song lyrics in mind. When they want to get the lyrics of the song. They should search.
	We are solving the problem using our retrieval model.
	User will give query having broken lyrics , we will recommend them list of lyrics similar to that lyrics using Vector Space Model (VSM).

Group members:
	1. NUKA SUDHEER                     --> S20200010152
	2.VANDRAPU YESHWANTH SAI SRINIVAS   --> S20200010218
	
Dataset Link:

https://drive.google.com/file/d/1ukgtj3po1jnpnKCk0NBbk1AltxBooMLb/view
    
Project Drive Link:

https://drive.google.com/drive/folders/1Pqe_iXtXbLUzGpEtStgGQp_12m2MnpWO?usp=share_link
    
How to run:
  1.unzip the file
  2.go to the current folder (PROJECT)
  3.type on console : python code_1.py
  
Dirve link contains:
  codes files
  Already calculated idf, tfidf binary files

Components:

1. Indexing:
   We take the all documents and create a dictionary ,keys are the all unique words and posting list is document ID and frequency of that word in that document.
2. Searching:
   We calculate the tf and idf values and assign the weights to the each document by creating vector.Similarly find vector to query,now find the similarity between query and each document by using cosine similarity ,based on that we rank the document and return the top 10 document.
3. Refining searches based on specific filters:
   a. Search based on genre
      We search the documents based on the genre of each document , in our data set we have only 7 genres ,if user enter the genre we return the top 10 documents based on the entered genre and similarity of that document
   b. Search based on artist name 
      We search the documents based on artist name,if user enter any artist we return the documents related to the artist name
4. Capturing Feedback:
   By taking the relevance feedback from user,we find the new query using rocchio algorthim
   (Qnew = alpha(q) + beta(u(R))-gama(u(NR))) a = 1 ,B = 0.75 ,r = 0.25
   after geting new query we find cosine similarity between the new query and each document and return the top 10 documents
5. Assessment Components:
   We calculate the Precison , Recall and avgP and plot graph of Precison and Recall

Contribution:
	
     1. NUKA SUDHEER                     --> Indexing,Refining Search based on artist name,
                                            Capturing Feedback (using Rocchio Algorithm)
     2.VANDRAPU YESHWANTH SAI SRINIVAS   --> Searching,Refining Search based on genre,Assessment
                                            component

#
