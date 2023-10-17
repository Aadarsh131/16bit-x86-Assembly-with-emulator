## Binary and decimal

#### What is the binary number 10100101b (b is for binary) in decimal number?

The decimal numbers have a power of 10 for each digit (eg. 754 = 7 x 10^2 + 5 x 10^1 + 4 x 10^0). Likewise, a binary number can be raised to the power of two for each digit. The rightmost is 0 of 2, the left of 1 is 2, and so on.

`10100101b = 1*2^0 + 1*2^2 + 1*2^5 + 1*2^7 = 1 + 4 + 32 + 128 = 5 + 160 = 165`

Conversely, how do you express 165 as a binary number? As you learned in school, there are ways to list the rest after dividing by 2. Rather, I like the way calculating the power of 2 which is the closest to 165. I find 165 = 128 + 37 first because 128 is 2 ^ 7. As I studied assembly language, I was able to memorize several numbers which are the square of 2. After 165 next is 37 = 32 + 5. 32 is 2 ^ 5. So 5 is 4 + 1, so it is 2 ^ 2 + 1. The conclusion is 165 = 2 ^ 7 + 2 ^ 5 + 2 ^ 2 + 2 ^ 0. The way to convert this to binary is to add zero to the power of the square. 2 ^ 7 is 10000000b since there are seven zeros. 2 ^ 5 is 100000 and 2 ^ 2 is 100 because there are five zeros. Add everything to 10100101b.

> 4 bits are one nibble and 8 bits are one byte. 2 bytes are one word and 2 words are called as a double word.
>
> Byte, Word, Dword and Qword are 8-bit, 16-bit, 32bit and 64-bit mode respectively

> The rightmost bit is called as the Least Significant Bit (LSB), and the leftmost bit is called as the Most Significant Bit (MSB).

## Hexadecimal number

Ts relatively simple because you can think of hexadecimal by breaking four binary digits. If you cut four digits from 10100101b, it is 1010 and 0101. 1010b is 10 in decimal and 0101 is 5, which in Hexadecimal is A5

- No matter how long the binary number is, we can only think of it as four. Splitting long 32-bit binary numbers into four can be represented as an 8-digit hexadecimal number. In other words, `one nibble is a single hexadecimal digit`. However, to write a decimal number, you have to calculate the number of digits of each digit of the binary number. It must be multiplied, it must be added, and it is too difficult

- If the first digit is an alphabet, 0 is sometimes added as prefix. So A5 is displayed as 0A5h (h for hexadecimal). In addition, C language code prefer 0xA5. `"0x" means a hexadecimal number`


>hexadecimal value 1234h to decimal
>      
>``1234h = 4 * 16 ^ 0 + 3 * 16 ^ 1 + 2 * 16 ^ 2 + 1 * 16 ^ 3 = 4660``

## NOTE: Skipped Signed binary numbers for now