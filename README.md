# binary-addition


``` C
#include <stdio.h>
#include <stdbool.h>

#define BITS 8

int main() {
	bool a[BITS] = { 1, 1, 1, 1, 1, 0, 0, 0 };
	bool b[BITS] = { 1, 1, 1, 1, 1, 1, 1, 1 };
	bool s[BITS];
	bool c = 0;

	for(int i = 0; i < BITS; i++) {
		s[i] = (a[i] != b[i]) != c;
		c = ((a[i] != b[i]) && c) || (a[i] && b[i]);
	}

	for(int i = 0; i < BITS; i++) {
		printf("%d", s[i]);
	}

	printf("\n");
}
```
