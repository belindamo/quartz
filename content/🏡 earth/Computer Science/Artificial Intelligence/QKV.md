#concept
#todo : don't fully grasp this intuitively yet....

`QKV` stands for [[SR/memory/zms7JIl1.md|>>]] query, key, value


`Query` in QKV [[SR/memory/pC9vWy9q.md|>>]] vectors that represent input elements


`Key` in QKV [[SR/memory/S9LOE67m.md|>>]] vectors that represent input elements, but for the future prediction


`Value` in QKV [[SR/memory/eEOS4i5b.md|>>]] actual content from input that is aggregated into the output


### References
1. Karpathy GPT vid? 
2. https://stats.stackexchange.com/questions/421935/what-exactly-are-keys-queries-and-values-in-attention-mechanisms#:~:text=For%20unsupervised%20language,profile%20and%20history.

### Notes

For unsupervised language model training like [GPT](https://s3-us-west-2.amazonaws.com/openai-assets/research-covers/language-unsupervised/language_understanding_paper.pdf), 𝑄,𝐾,𝑉  are usually from the same source, so such operation is also called self-attention.

For the machine translation task in the second paper, it first ≠ self-attention separately to source and target sequences, then on top of that it applies another attention where 𝑄Q is from the target sequence and 𝐾,𝑉K,V are from the source sequence.

For recommendation systems, 𝑄Q can be from the target items, 𝐾,𝑉K,V can be from the user profile and history.


