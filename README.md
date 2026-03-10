#include <stdio.h>
#include <string.h>

int main() {
    char text[] = "ABC ABCDAB ABCDABCDABDE";
    char pattern[] = "ABCDABD";
    int i, j;

    int n = strlen(text);
    int m = strlen(pattern);

    for (i = 0; i <= n - m; i++) {
        for (j = 0; j < m; j++) {
            if (text[i + j] != pattern[j])
                break;
        }
        if (j == m)
            printf("Pattern found at index %d\n", i);
    }
    return 0;
}
