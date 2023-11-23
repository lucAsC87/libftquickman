**General Notes**
- follow the Norm!
- No global variables
- helper functions must be defined as `static`, so their scope is limited to the appropriate file
- necessary external libraries: `stdlib.h` (to use `size_t`, `malloc` and `free`) and `unistd.h` (to use `write`)
- compile using `cc` and use the command `ar` to create your library (no libtool)
- use the flags `-Wall -Wextra -Werror`
- Makefile mandatory rules: **$(name)**, **all**, **clean**, **fclean**, **re**. In case of bonus, add the rule **bonus**

## **MANDATORY FUNCTIONS**
## ft_isalpha.c
*Prototype*: `int ft_isalpha(int c)`
*Description*: checks  for an alphabetic character.
*Return value*: the  values  returned  are  nonzero  if  the character c falls into the tested class, and zero if not.

## ft_isdigit.c
*Prototype*: `int ft_isdigit(int c)`
*Description*: checks for a digit (0 through 9).
*Return value*: the  values  returned  are  nonzero  if  the character c falls into the tested class, and zero if not.

## ft_isalnum.c
*Prototype*: `int ft_isalnum(int c)`
*Description*: checks for an alphanumeric character.
*Return value*: the  values  returned  are  nonzero  if  the character c falls into the tested class, and zero if not.

## ft_isascii.c
*Prototype*: `int ft_isascii(int c)`
*Description*: checks whether c fits into the ASCII character set.
*Return value*: the  values  returned  are  nonzero  if  the character c falls into the tested class, and zero if not.
## ft_isprint.c
*Prototype*: `int ft_isprint(int c)`
*Description*: checks for any printable character including space.
*Return value*: the  values  returned  are  nonzero  if  the character c falls into the tested class, and zero if not.

## ft_strlen.c
*Prototype*: `size_t ft_strlen(const char *s)`
*Description*: calculates the length of the string pointed to by `s`, excluding the terminating null byte (`'\0'`)
*Return value*: the number of bytes in the string pointed to by `s`.

## ft_memset.c
*Prototype*: `void *ft_memset(void *s, int c, size_t n)`
*Description*: fills the first `n` bytes of the memory area pointed to by `s` with the constant byte `c`.
*Return value*: a pointer to the memory area `s`.

## ft_bzero.c
*Prototype*: `void ft_bzero(void *s, size_t n)`
*Description*: erases the data in the `n` bytes of the memory startint at the location pointed to by `s`, by writing zeros (bytes containing `'\0'`) to that area.
*Return value*: none.

## ft_memcpy.c
*Prototype*: `void *ft_memcpy(void *dest, const void *src, size_t n)`
*Description*: copies `n` bytes from memory area `src` to memory area `dest`. The memory area must not overlap.
*Return value*: a pointer to `dest`.

## ft_memmove.c
*Prototype*: `void *ft_memmove(void *dest, const void *src, size_t n)`
*Description*: copies `n` bytes from memory area `src` to memory area `dest`. The memory areas may overlap: copying takes place as though the bytes in `src` are first copied into a temporary array that does non overlap `src` or `dest`, and the bytes are then copied from the temporary array to `dest`.
*Return value*: a pointer to `dest`.

## ft_strlcpy.c
*Prototype*: `size_t ft_strlcpy(char *dst, const char *src, size_t size)`
*Description*: copies up to `size - 1` characters from the NUL-terminated string `src` to `dst`, NUL-terminating the result (as long as `size` is larger than 0), taking the full size of the buffer. Note that a byte for the NUL should be included in `size`.
*Return value*: the total length of `src`.

## ft_strlcat.c
*Prototype*: `size_t ft_strlcat(char *dest, const char *src, size_t size)`
*Description*: appends the NUl_terminated string `src` to the end of `dst`. It will append at most `size - ft_strlen(dst) - 1` bytes, NUL_terminating the result (as long as there is at least one byte free in `dst`), taking the full size of the buffer. Note that a byte for the NUL should be included in `size`.
*Return value*: the initial length of `dst` plus the length of `src`. If traverses `size` characters without finding a NUL, the length if the string is considered to be `size` and the destination string will not be NUL-terminated.

## ft_toupper.c
*Prototype*: `int ft_toupper(int c)`
*Description*: if it's a lowercase letter, converts `c` to its uppercase equivalent.
*Return value*: the letter converted or `c` if the conversion was not possible.

## ft_tolower.c
*Prototype*: `int ft_tolower(int c)`
*Description*: if it's an uppercase letter, converts `c` to its lowercase equivalent.
*Return value*: the letter converted or `c` if the conversion was not possible.

## ft_strchr.c
*Prototype*: `char *ft_strchr(const char *s, int c)`
*Description*: finds the first occurrence of the character `c` in the string `s`.
*Return value*: a pointer to the matched character of NULL if the character is not found. The terminating null byte is considered part of the string, so that if `c` is specified as `'\0'` return a pointer to the terminator.

## ft_strrchr.c
*Prototype*: `char *strrchr(const char *s, int c)`
*Description*: finds the last occurrence of the character `c` in the string `s`.
*Return value*: a pointer to the matched character of NULL if the character is not found. The terminating null byte is considered part of the string, so that if `c` is specified as `'\0'` return a pointer to the terminator.

## ft_strncmp.c
*Prototype*: `int strncmp(const char *s1, const char *s2, size_t n)`
*Description*: compares the first (at most) `n` bytes of the two strings `s1` and `s2`.
*Return value*: an integer less than, equal to, or greater than zero if the first `n` bytes of `s1` is found, respectively, to be less than, to match or be greater than `s2`.

## ft_memchr.c
*Prototype*: `void *ft_memchr(const void *s, int c, size_t n)`
*Description*: scans the initial `n` bytes of the memory area pointed to by `s` for the first instance of `c`.
*Return value*: a pointer to the matching byte or NULL if the character does not occur in the given memory area.

## ft_memcmp.c
*Prototype*: `int ft_memcmp(const void *s1, const void *s2, size_t n)`
*Description*: compares the first `n` bytes of the memory areas `s1` and `s2`.
*Return value*: an integer less than, equal to, or greater than zero if the first `n` bytes of `s1` is found, respectively, to be less than, to match, or be greater than the first `n` bytes of `s2`. If `n` is zero, the return value is zero.

## ft_strnstr.c
*Prototype*: `char *ft_strnstr(const char *big, const char *little, size_t len)`
*Description*: locates the fist occurrence of the null-terminated string `little` in the string `big`, where not more than `len` characters are searched.
*Return value*: if `little` is an empty string, `big` is returned; if `little` occurs nowhere in `big`, NULL is returned; otherwise a pointer to the first character of the first occurrence of `little` is returned.

## ft_atoi.c
*Prototype*: `int ft_atoi(const char *nptr)`
*Description*: converts the initial portion of the string pointed to by `nptr` to `int`.
*Return value*: the converted value or 0 on error.

## ft_calloc.c
*Prototype*: `void *ft_calloc(size_t nmemb, size_t size)`
*Description*: allocates memory for an array of `nmemb` elements of `size` bytes each. The memory is set to zero.
*Return value*: a pointer to the allocated memory or NULL in case of error or in case one of the two parameters is equal to zero.

## ft_strdup.c
*Prototype*: `char *ft_strdup(const char *s)`
*Description*: duplicate the string `s`. The memory for the new string is obtained with `malloc`.
*Return value*: a pointer to the duplicated string.

## ft_substr.c
*Prototype*: `char *ft_substr(char const *s, unsigned int start, size_t len)`
*Description*: allocates with `malloc` and returns a substring from `s`, that begins at index `start` and of maximum size `len`.
*Return value*: the substring or NULL if the allocation fails.

## ft_strjoin.c
*Prototype*: `char *ft_strjoin(char const *s1, char const *s2)`
*Description*: allocates with `malloc` and returns a new string resulting from the concatenation of `s1` and `s2`
*Return value*: the new string or NULL if the allocation fails.

## ft_strtrim.c
*Prototype*: `char *ft_strtrim(char const *s1, char const *set)`
*Description*: allocates with `malloc` and returns a copy of `s1` with the characters specified in set removed from the beginning and the end of the string.
*Return value*: the trimmed string of NULL if the allocation fails.

## ft_split.c
*Prototype*: `char **ft_split(char const *s, char c)`
*Description*: allocates with `malloc` and return an array of strings obtained splitting `s` using the character `c` as a delimiter. The array must end with a NULL pointer.
*Return value*: the array of new strings or NULL if the allocation fails.

## ft_itoa
*Prototype*: `char *ft_itoa(int n)`
*Description*: allocates with `malloc` and returns a string representing the integer `n`.
*Return value*: the string representing the integer or NULL if the allocation fails.

## ft_strmapi
*Prototype*: `char *ft_strmapi(char const *s, char (*f)(unsigned int, char))`
*Description*: applies the function `f` to each character of the string `s` to create a new string (using `malloc`) resulting from successive applications of `f`.
*Return value*: the string created or NULL if the allocation fails.

## ft_striteri
*Prototype*: `void ft_striteri(char *s, void (*f)(unsigned int, char*))`
*Description*: applies the function `f` on each character of the string `s`.
*Return value*: none.

## ft_putchar_fd
*Prototype*: `void ft_putchar_fd(char c, int fd)`
*Description*: outputs the character `c` to the given file descriptor.
*Return value*: none.

## ft_putstr_fd
*Prototype*: `void ft_putstr_fd(char *s, int fd)`
*Description*: Outputs the string `s` to the given file descriptor.
*Return value*: none.

## ft_putendl_fd
*Prototype*: `void ft_putend_fd(char *s, int fd)`
*Description*: Outputs the string `s` to the given file descriptor followed by a newline.
*Return value*: none.

## ft_putnbr_fd
*Prototype*: `void ft_putnbr_fd(int n, int fd)`
*Description*: outputs the integer `n` to the given file descriptor.
*Return value*: none.

## **BONUS FUNCTIONS**
To start, add this structure to your libft.h file:

`typedef struct   s_list
`{                       
` void            *content;`
` struct s_list   *next;`
`}                t_list;`

## ft_lstnew_bonus
*Prototype*: `t_list *ftlstnew(void *content)`
*Description*: allocates with `malloc` and return a new node. The variable `next` is initialized to NULL.
*Return value*: the new node.

## ft_lstadd_front_bonus
*Prototype*: `void ft_lstadd_front(t_list **lst, t_list *new)`
*Description*: adds the node `new` to the beginning of the list.
*Return value*: none.

## ft_lstsize_bonus
*Prototype*: `int ft_lstsize(t_list *lst)`
*Description*: count the number of nodes in a list.
*Return value*: the length of the list.

## ft_lstlast_bonus
*Prototype*: `t_list *ft_lstlast(t_list *lst)`
*Description*: returns the last node of the list.
*Return value*: the last node of the list.

## ft_lstadd_back_bonus
*Prototype*: `void ft_lstadd_back(t_list **lst, t_list *new)`
*Description*: add the node `new` at the end of the list.
*Return value*: none.

## ft_lstdelone_bonus
*Prototype*: `void ft_lstdelone(t_list *lst, void (*del)(void *))`
*Description*: takes as a parameter a node and frees its `content`'s memory using the function `del`.
*Return value*: none.

## ft_lstclear_bonus
*Prototype*: `void ft_lstclear(t_list **lst, void (*del)(void *))`
*Description*: deletes and frees the given node and its every successor using the function `del` and `free`. Finally, the pointer to the list must be set to NULL.
*Return value*: none.

## ft_lstiter_bonus
*Prototype*: `void ft_lstiter(t_list *lst, void (*f)(void *))`
*Description*: iterates `lst` and applies the function `f` on the `content` of each node.
*Return value*: none.

## ft_lstmap_bonus
*Prototype*: `t_list *ft_lstmap(t_list *lst, void *(*f)(void *), void (*del)(void *))`
*Description*: iterates on `lst` and applies the function `f` on the `content` of each node. Creates a new list resulting of the successive applications of `f`. The function `del` is used to delete the `content` of a node if needed.
*Return value*: the new list or NULL if the allocation fails.