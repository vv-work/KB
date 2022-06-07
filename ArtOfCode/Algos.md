# Algorithms

## Navigation

- A*
- ORCA

## A*

## ORCA
Optimal Reciprocal Collision Avoidance

[RVO2](https://gamma.cs.unc.edu/RVO2/downloads/) - is popular implementation with C# version


## Deflate

Supported in gzip.

`.gz` - file stands for **GZIP** file
`.tar` - stands for multiple files


### Links

- [Deflate White Paper](http://www.infinitepartitions.com/art001.html)
- [Youtube Lecture](https://youtu.be/oi2lMBBjQ8s)

### Questions

- Basic explanation on LZ77 and Huffman coding
- Test gzip in windows ? 
- Gzip vs 7zip? 
- What is hex dump?
- What the diffrence between LZ77 vs LZ78 vs LZSS

## Huffman coding

- Huffman tree nodes.

## LZ Family

`5:3`

**Backrefrecne** -
**Sliding Window** -

### Family lines


DEFLATE->LZSS->LZ77 
Length Distance pairs

Gif->LZW->LZ78->LZ77
Symbol table

LZMA->LZ77
### LZ77
Achives compression by replacing repeated occurences of data with references.

As well known as **LZSS**

**LZ77** - also known as **LZ1** 
**LZ78** - also knows as **LZ2**
**LZSS** - is the same as LZ77 but add the additional bit to identify what data infront. 

**LZSS** - **L**empel- **Z**iv- **S**torer-Szymanski

![LZSS](res\LZSS_example.png)

### History 

Abraham Lempel - Is from lviv
Presented LZ77 (Lempel-Ziv in 1977)

Jacom Ziv - presented improved version
in 1978

**RLE** **R**un- **L**enght **E**ncoding


> from

`00000000 00000000 01111111 11111111 10000011 11111111`

> into

 data compresses into values of `17 15 5 10`. 

`00010001 00001111 00000101 00001010`
