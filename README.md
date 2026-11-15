
*This project has been created as part of the 42 curriculum by mmaatouk.*

# Libft

## Description

Libft is the first project of the 42 curriculum. Its goal is to create a personal C library by reimplementing a collection of standard C library functions and developing additional utility functions.

The purpose of this project is to understand how fundamental C functions work internally and strengthen programming skills, particularly in memory management, pointers, strings, and data structures.

The library is compiled into a static library named `libft.a`, which can be reused in future 42 projects.

## Instructions

### Requirements

- GCC or another C compiler.
- Make.
- Unix-based operating system (Linux or macOS).

### Compilation

Clone the repository:

```bash
git clone "repo"
cd libft
```

Compile the library:

```bash
make
```

This generates the static library `libft.a`.

### Makefile Commands

| Command | Description |
|---|---|
| `make` | Compiles the library. |
| `make all` | Compiles the library. |
| `make clean` | Removes object files. |
| `make fclean` | Removes object files and `libft.a`. |
| `make re` | Recompiles everything from scratch. |

### Using the Library

Include the header file in your C program:

```c
#include "libft.h"
```

Compile your program by linking the library:

```bash
cc main.c -L. -lft -I. -o program
```

Run it:

```bash
./program
```

## Library Contents

### 1. Libc Functions

Reimplementations of standard C library functions.

**Character checking and conversion:**

- `ft_isalpha` – Checks whether a character is alphabetic.
- `ft_isdigit` – Checks whether a character is a digit.
- `ft_isalnum` – Checks whether a character is alphanumeric.
- `ft_isascii` – Checks whether a character belongs to the ASCII character set.
- `ft_isprint` – Checks whether a character is printable.
- `ft_toupper` – Converts a lowercase character to uppercase.
- `ft_tolower` – Converts an uppercase character to lowercase.

**String manipulation:**

- `ft_strlen` – Calculates the length of a string.
- `ft_strchr` – Searches for a character in a string.
- `ft_strrchr` – Searches for the last occurrence of a character.
- `ft_strncmp` – Compares two strings.
- `ft_strlcpy` – Copies a string into a destination buffer.
- `ft_strlcat` – Appends a string to another.
- `ft_strnstr` – Searches for a substring within a limited length.
- `ft_strdup` – Duplicates a string using dynamic memory allocation.

**Memory manipulation:**

- `ft_memset` – Fills a memory area with a specified byte.
- `ft_bzero` – Sets a memory area to zero.
- `ft_memcpy` – Copies memory from one location to another.
- `ft_memmove` – Copies memory while handling overlapping regions.
- `ft_memchr` – Searches for a byte in a memory area.
- `ft_memcmp` – Compares two memory areas.
- `ft_calloc` – Allocates memory and initializes it to zero.

**Conversion:**

- `ft_atoi` – Converts a string into an integer.

### 2. Additional Functions

- `ft_substr` – Extracts a substring from a string.
- `ft_strjoin` – Concatenates two strings.
- `ft_strtrim` – Removes specified characters from the beginning and end of a string.
- `ft_split` – Splits a string into an array of strings using a delimiter.
- `ft_itoa` – Converts an integer into a string.
- `ft_strmapi` – Applies a function to each character of a string and creates a new string.
- `ft_striteri` – Applies a function to each character of a string.
- `ft_putchar_fd` – Writes a character to a file descriptor.
- `ft_putstr_fd` – Writes a string to a file descriptor.
- `ft_putendl_fd` – Writes a string followed by a newline.
- `ft_putnbr_fd` – Writes an integer to a file descriptor.

### 3. Linked List Functions (Bonus)

Libft also introduces singly linked lists through the following structure:

```c
typedef struct s_list
{
    void            *content;
    struct s_list   *next;
}   t_list;
```

The linked list functions include:

- `ft_lstnew` – Creates a new list node.
- `ft_lstadd_front` – Adds a node to the beginning of a list.
- `ft_lstsize` – Counts the number of nodes.
- `ft_lstlast` – Returns the last node.
- `ft_lstadd_back` – Adds a node to the end of a list.
- `ft_lstdelone` – Deletes a single node and frees its content.
- `ft_lstclear` – Deletes and frees an entire list.
- `ft_lstiter` – Applies a function to each node's content.
- `ft_lstmap` – Creates a new list by applying a function to each node's content.

## Technical Choices

- **C language:** Used to understand low-level programming concepts.
- **Static library:** The project produces `libft.a`, allowing functions to be reused.
- **Makefile:** Automates compilation and project cleanup.
- **Header file:** `libft.h` contains function prototypes and the linked list structure.
- **Dynamic memory allocation:** Used when creating strings and linked list nodes.

## Resources

The following resources were useful during the development of this project:

- [C Library Reference - cppreference](https://en.cppreference.com/w/c/header)
- [Linux Manual Pages](https://man7.org/linux/man-pages/)
- [GNU C Library Documentation](https://www.gnu.org/software/libc/manual/)
- [Learn-C.org](https://www.learn-c.org/)

### AI Usage

AI tools were used as a learning and support resource during this project.

They were used for:

- Understanding the behavior and purpose of standard C library functions.
- Clarifying concepts related to pointers, memory allocation, and linked lists.
- Understanding compiler errors and debugging potential issues.
- Improving the documentation and structure of this README file.

All implementations were reviewed and tested by the student to ensure understanding of the code and compliance with the project requirements.

## Project Structure

```text
├── libft.h
├── ft_isalpha.c
├── ft_strlen.c
├── ft_memset.c
├── ft_strdup.c
├── ...
├── Makefile
├── README.md
└── libft.a
```
## Conclusion

Libft is a foundational project that provides a deeper understanding of the C language and its standard library. It develops essential programming skills, particularly in memory management, string manipulation, and data structures.

The resulting library serves as a personal collection of reusable functions for future projects throughout the 42 curriculum.
