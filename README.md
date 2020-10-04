# Fuzzy-Keyword-Search-Over-Encrypted-Data-Using-Cloud-Computing

As Cloud Computing becomes prevalent, more and more sensitive information are being centralized into the cloud. 
 However, the data owners and cloud server are not in the same trusted domain,  this make our data at risk. 
data usually should be encrypted prior to outsourcing.
 One of the most popular ways is to selectively retrieve files through keyword-based search. 
But this is impractical in cloud computing scenario.
In this project, we focus on enabling effective yet privacy preserving fuzzy keyword search in cloud computing.


Existing system was to selectively retrieve files through simple keyword-based search.
It  is through simple spell check mechanisms. 
They cannot tolerate both minor types and format inconsistencies.

The fuzzy keyword search scheme returns the search results according to the following rules: 
If the user’s searching input exactly matches the pre-defined set of keywords, the server will return the files containing the keyword.
If there exist some error in spelling or some format inconsistencies in the searching input, the server will return the closest possible results based on pre-specified similarity semantics. 

approximate string matching
	Ex. Languaje will be corrected to language
 Fuzzy keyword search greatly enhances system usability by returning the matching files when user’s searching inputs exactly match. 

User want search keyword language
User misspelled it as languaje and clicked on search button
Data in the database is in encrypted form.
Now we will try to search the encrypted data for inputted keyword languaje. Which will convert it  to language and display result.
This is the technique which will help us to match the keyword languaje with encrypted keywords in the database.
We can implement this project by three methods
 Wildcard – Based Technique 
 Gram - Based Technique 
 Symbol – Based Trie – traverse Search Scheme 
Here we use a wild-card Technique to solve this project. For this we first need to find the Edit distance. 
Edit distance method is used for finding string similarity.
The edit distance ed(w1, w2) between two words w1, w2 is the number of operation required to transform one of them to other.
Edit distance operation can be performed in 3 ways,
    a. Substitution (changing one character to another)
    b. Deletion (deleting one character)
    c. Insertion (inserting a single character)
To build an index for wi with edit distance d, the data owner first constructs a fuzzy keyword set Swi,d using the wildcard based technique.
That is for a keyword CASTLE: {AASTLE, BASTLE, DASTLE, · · · , YASTLE, ZASTLE}.
Then we keep a secret key sk shared between data owner and authorized users.
The index table with the secret key is stored in the cloud.
For searching authorized user sends request to the server.
Upon receiving the search request the server compares them with the index table and returns all the possible encrypted file identifiers.

