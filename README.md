no :1

#include <stdio.h>

int main() { int num; printf("Enter a number: "); scanf("%d", &num);

if(num % 5 == 0 && num % 11 == 0) { printf("Number is divisible by 5 and 11\n"); } else { printf("Number is not divisible by 5 and 11\n"); }

return 0; }

no:2 #include <stdio.h>

int main() { int num;

printf("Enter a number: "); scanf("%d", &num);

if (num > 0) { printf("%d is positive", num); } else if (num < 0) { printf("%d is negative", num); } else { printf("The number is zero"); }

return 0; }

no:3 #include <stdio.h>

int main() { char ch; printf("Enter a character: "); scanf("%c", &ch);

if((ch >= 'a' && ch <= 'z') || (ch >= 'A' && ch <= 'Z')) { printf("'%c' is alphabet\n", ch); } else { printf("'%c' is not alphabet\n", ch); }

return 0; }

no:4

#include <stdio.h> #include <string.h>

int main() { char str[100]; int vowels = 0; printf("Enter a string: "); fgets(str, sizeof(str), stdin);

for(int i = 0; i < strlen(str); i++) { if(str[i] == 'a' || str[i] == 'e' || str[i] == 'i' || str[i] == 'o' || str[i] == 'u' || str[i] == 'A' || str[i] == 'E' || str[i] == 'I' || str[i] == 'O' || str[i] == 'U') { vowels++; } }

printf("Number of vowels in the string: %d\n", vowels);

return 0; }

no:5

#include <stdio.h>

int main() { char ch; printf("Enter a character: "); scanf("%c", &ch);

if(ch >= 'a' && ch <= 'z') { printf("'%c' is lowercase alphabet\n", ch); } else if(ch >= 'A' && ch <= 'Z') { printf("'%c' is uppercase alphabet\n", ch); } else { printf("'%c' is not an alphabet\n", ch); }

return 0; }

no:6

#include <stdio.h>

int main() { int amount, notes; int denominations[] = {500, 100, 50, 20, 10, 5, 2, 1}; int notes_count[sizeof(denominations) / sizeof(denominations[0])];

printf("Enter the amount: "); scanf("%d", &amount);

// Initialize notes count for each denomination to 0 for(int i = 0; i < sizeof(denominations) / sizeof(denominations[0]); i++) { notes_count[i] = 0; }

// Calculate minimum number of notes for each denomination for(int i = 0; i < sizeof(denominations) / sizeof(denominations[0]); i++) { notes = amount / denominations[i]; amount = amount % denominations[i]; notes_count[i] = notes; }

// Print minimum number of notes for each denomination printf("Total number of notes:\n"); for(int i = 0; i < sizeof(denominations) / sizeof(denominations[0]); i++) { printf("%d: %d\n", denominations[i], notes_count[i]); }

return 0; }

no:7

#include <stdio.h>

int main() { int num, count = 0;

printf("Enter a number: "); scanf("%d", &num);

// Count number of digits using loop while(num != 0) { num /= 10; count++; }

printf("Number of digits: %d\n", count);

return 0; }

no:8

#include <stdio.h>

int main() { int num, sum = 0, digit;

printf("Enter a number: "); scanf("%d", &num);

// Calculate sum of digits using for loop for(int temp = num; temp > 0; temp /= 10) { digit = temp % 10; sum += digit; }

printf("Sum of digits: %d\n", sum);

return 0; }

no:9

#include <stdio.h>

int main() { int num, reverse = 0, digit;

printf("Enter a number: "); scanf("%d", &num);

// Find reverse of number using for loop for(int temp = num; temp > 0; temp /= 10) { digit = temp % 10; reverse = reverse * 10 + digit; }

printf("Reverse of %d = %d\n", num, reverse);

return 0;

no:10

#include <stdio.h> int main() { int num, binary = 0, place = 1;

printf("Enter a decimal number: "); scanf("%d", &num);

// Convert decimal to binary while(num > 0) { binary += (num % 2) * place; num /= 2; place *= 10; }

printf("Binary number: %07d\n", binary); // Print binary number with leading zeroes

return 0; }
