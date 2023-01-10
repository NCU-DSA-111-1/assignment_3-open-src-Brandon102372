#Huffman coding and Arithmetic coding
##Usage
###Huffman coding:
Make sure you directory is at /huffman
Enter the following command to build
```bash
make
```
To encode the file enter the following command
```bash
./huffcode -i input_file -o output_file -c
```
After encoding, the program will show how long the encoding process takes

To decode the file enter the following command
```bash
./huffcode -i input_file -o output_file -d
```
After decoding, the program will show how long the decoding process takes
Note: Replace input_file as the file you wnat to encode and replace output_file as the file name you want to output.(If the file does not  exist, the program will create one by itself)
For example:
```bash
./huffcode -i long -o encode -c
./huffcode -i encode -o decode -d
```
###Arithmetic coding:
Make sure your directory is at /arithmetic
Enter the following command to build
```bash
gcc -o arithmetic arcd_stream.c arcd.c arcd.h adaptive_model.h adaptive_model.c
```
To encode the file enter the following command
```bash
./arithmetic -e <input_file | tee output_file
```
After encoding, the program will show how long the encoding process takes and the encoding result.

To decode the file enter the following command
```bash
./arithmetic -d  <input_file | tee output_file
```
After decoding, the program will show how long the decoding process takes and the decoding result.
Note: Replace input_file as the file you wnat to encode and replace output_file as the file name you want to output.(If the file does not  exist, the program will create one by itself)
For example:
```bash
./arithmetic -e <long | tee encode
./arithmetic -d  <encode | tee decode
```
