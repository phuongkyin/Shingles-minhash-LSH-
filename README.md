# Shingles-minhash-LSH-Method (References: various sources)
LSH is is an algorithmic technique that hashes similar input items into the same “buckets” with high .
probability. New document -> Set representation -> Minhashing ->LSH -> Potential duplicate pairs.

num_perm is the number of permutations we want for the MinHash algorithm (discussed before). The higher the permutations the longer the runtime.
The minHash has a property that the probability for two minimum elements are the same is equal to the Jaccard distance between two arrays. replace large sets by much smaller representations. We call it as signatures, compare the signatures of two sets and estimate the Jaccard similaritysignatures alone. 

The primary idea of minHash is to have a hash function that is sensitive to distances (Locality Sensitive Hashing - LSH). In other words, if two points are close to each other, the probability that this function hashes them to the same bucket is high. On the contrary, if the points are far apart, the probability that they get hashed to the same bucket is low. 

Shingles
For text, they could be characters, unigrams or bigrams, a set of categories as shingles. Shingles simply reduce our documents to sets of elements that so can calculate similarity betweens sets.
In the standard literature there is a concept of shingle size, k, where the number of shingles is equal to 20k.
LSH is a type of Neighborhood Based method like k-nearest neighbors (KNN).
Many applications of near duplicate document detection today are very large scale search problems. Two such popular optimizations are minhash and Locality Sensitive Hashing (LSH).
Minhash maps shingles (sets of strings/characters) to integers by hashing each shingle with n number of hashing functions and the minimum hash value for each shingle is kept. Using n hashing functions and choosing the minimum hash value acts as "random" shingle sampling. By hashing strings we can compare and store them more efficiently, as integers are programmatically "cheaper" to work with than strings.
