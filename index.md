# erol
## erol
### erol
#### erol
##### erol
###### erol
changed stuff
![picture of terracottocat](https://octodex.github.com/images/Terracottocat_Single.png)
``` c
#include <cs50.h>
#include <stdio.h>

int get_height(void);
void print_spaces(int spaces);
void print_blocks(int blocks);
void print_pyramid(int height);

int main(void)
{
    int height = get_height();
    print_pyramid(height);
}
// ask user for pyramid height
int get_height(void)
{
    int height;
    do
    {
        height = get_int("Enter pyramid height between 1 and 8:");
    }
    while (height < 1 || height > 8);
    return height;
}
// print individual spaces function

void print_spaces(int spaces)
{
    for (int i = 0; i < spaces; i++)
    {
        printf(" ");
    }
}
// print individual blocks function

void print_blocks(int blocks)
{
    for (int j = 0; j < blocks; j++)
    {
        printf("#");
    }
}
// print pyramid
void print_pyramid(int height)
{
    int spaces = height - 1;

    int blocks = 1;

    for (int h = 0; h < height; h++)
    {
        print_spaces(spaces);
        print_blocks(blocks);
        printf("  ");
        print_blocks(blocks);
        printf("\n");
        blocks++;
        spaces--;
    }
}
```

- [ ] Turn on GitHub Pages
- [x] Outline my portfolio
- [ ] Introduce myself to the world
