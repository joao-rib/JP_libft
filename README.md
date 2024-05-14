# libft

First library for school 42. Always updating.

## PART 1

### Replicas of <ctype.h>

Function | Format | Description | Return | Status
--- | --- | --- | --- | ---
ft_isalpha | `int	ft_isalpha(int c)` | Check if character c (int format) is alphabetic | 0 or 1 | OK
ft_isdigit | `int	ft_isdigit(int c)` | Check if character c (int format) is numeric | 0 or 1 | OK
ft_isalnum | `int	ft_isalnum(int c)` | Check if character c (int format) is alphanumeric | 0 or 1 | OK
ft_isascii | `int	ft_isascii(int c)` | Check if character c (int format) is ASCII | 0 or 1 | OK
ft_isprint | `int	ft_isprint(int c)` | Check if character c (int format) is printable | 0 or 1 | OK
ft_toupper | `int	ft_toupper(int c)` | If c is a lowercase letter, returns its uppercase equivalent | c | OK
ft_tolower | `int	ft_tolower(int c)` | If c is an uppercase letter, returns its lowercase equivalent | c | OK

### Replicas of <string.h>

Function | Format | Description | Return | Status
--- | --- | --- | --- | ---
ft_strlen | `size_t	ft_strlen(const char *str)` | Checks number of characters in string str | Size of str | OK
ft_memset | `void	*ft_memset(void *s, int c, size_t n)` | Fills the first n bytes of the memory area pointed to by s with the constant byte c | Pointer to s | OK
ft_bzero | `void	ft_bzero(void *s, size_t n)` | Erases the first n bytes of memory in memory area pointed to by s | - | OK
ft_strlcpy | `size_t	ft_strlcpy(char *dest, const char *src, size_t size)` | Copy "size" bytes from src to dst | Size of src | OK
ft_memcpy | `void	*ft_memcpy(void *dest, const void *src, size_t n)` | Copy n bytes of memory from src to dest. There is risk of memory overlap | (void *)dest | OK
ft_memmove | `void	*ft_memmove(void *dest, const void *src, size_t n)` | Copy n bytes of memory from src to dest. Avoids memory overlap | (void *)dest | OK
ft_strlcat | `size_t	ft_strlcat(char *dest, const char *src, size_t size)` | Concatenate src into dest. Final string will have "size" bytes | Whichever size is smaller between [dest+src] OR ["size"+src] | OK
ft_strchr | `char	*ft_strchr(const char *str, int c)` | Returns pointer to first instance of char c in str | Pointer to location in str | OK
ft_strrchr | `char	*ft_strrchr(const char *str, int c)` | Returns pointer to last instance of char c in str | Pointer to location in str | OK
ft_memchr | `void	*ft_memchr(const void *str, int c, size_t n)` | Returns pointer to first instance of char c in str. Only checks the first n bytes | Pointer to location in str | OK
ft_strncmp | `int	ft_strncmp(const char *s1, const char *s2, size_t n)` | Compare the first n bytes of strings s1 and s2 | 1, 0, or -1 | OK
ft_memcmp | `int	ft_memcmp(const void *s1, const void *s2, size_t n)` | Compare the first n bytes of variables s1 and s2 | 1, 0, or -1 | OK
ft_strnstr | `char	*ft_strnstr(const char *big, const char *little, size_t len)` | Checks if string little exists in string big, within len characters | Pointer to location in big | OK
ft_strdup | `char	*ft_strdup(const char *src)` | Creates new string as a duplicate of src [requires malloc] | New string | OK

### Replicas of <stdlib.h>

Function | Format | Description | Return | Status
--- | --- | --- | --- | ---
ft_atoi | `int	ft_atoi(const char *str)` | Converts written number from a string str into int format | The desired number, or 0 if there is none | OK
ft_calloc | `void	*ft_calloc(size_t nmemb, size_t size)` | Allocates memory to an array of nmemb elements of "size" bytes each. [requires malloc] | Pointer to memory block | OK

## PART 2

Function | Format | Description | Return | Status
--- | --- | --- | --- | ---
ft_substr | `char	*ft_substr(const char *str, unsigned int start, size_t len)` | Creates new string, equivalent to a pointer to str at the "start" location. len is maximum size. [requires malloc] | New sub-string | OK
ft_strjoin | `char	*ft_strjoin(const char *s1, const char *s2)` | Concatenates s1 and s2 into a new string. [requires malloc] | New joined string | OK
ft_strtrim | `char	*ft_strtrim(const char *s1, const char *set)` | Trims beginning and end of string s1 out of all "set" characters. [requires malloc] | New trimmed string | OK
ft_split | `char	**ft_split(const char *s, char c)` | Divides string s into words (delimited by c), and turns each word into a string. [requires malloc & free] | Array of strings | OK
ft_itoa | `char	*ft_itoa(int n)` | Converts a number into a string. [requires malloc] | String with a written number | OK
ft_strmapi | `char	*ft_strmapi(const char *str, char (*f)(unsigned int, char))` | Applies function f to each character of str, returning a string with the results. [requires malloc] | New string | OK
ft_striteri | `void	ft_striteri(char *str, void (*f)(unsigned int, char))` | Applies function f to each character of str, altering str in the process | - | OK
ft_putchar_fd | `void	ft_putchar_fd(char c, int fd)` | Prints c to the file descriptor fd. [requires write] | - | OK
ft_putstr_fd | `void	ft_putstr_fd(char *str, int fd)` | Prints str to the file descriptor fd. [requires write] | - | OK
ft_putendl_fd | `void	ft_putendl_fd(char *str, int fd)` | Prints str to the file descriptor fd, followed by a newline. [requires write] | - | OK
ft_putnbr_fd | `void	ft_putnbr_fd(int n, int fd)` | Prints n to the file descriptor fd. [requires write] | - | OK

## BONUS

Function | Format | Description | Return | Status
--- | --- | --- | --- | ---
ft_lstnew | `t_list	*ft_lstnew(void *content)` | Creates new node with "content". "next" node becomes NULL. [requires malloc] | The new node | OK
ft_lstadd_front | `void	 ft_lstadd_front(t_list **lst, t_list *new)` | Adds node "new" to the front of the lst | - | OK
ft_lstsize | `int	 ft_lstsize(t_list *lst)` | Checks number of nodes in lst | Number of nodes | OK
ft_lstlast | `t_list	 *ft_lstlast(t_list *lst)` | Checks last node in lst | Last node | OK
ft_lstadd_back | `void	 ft_lstadd_back(t_list **lst, t_list *new)` | Adds node "new" to the back of the lst | - | OK
ft_lstdelone | `void	 ft_lstdelone(t_list *lst, void (*del)(void *))` | Frees memory from current node's content in lst, using the del function. [requires free] | - | OK
ft_lstclear | `void	 ft_lstclear(t_list **lst, void (*del)(void *))` | Frees memory from current node's content in lst, as well as all following nodes, using the del function. List then points to NULL. [requires free] | - | OK
ft_lstiter | `void	 ft_lstiter(t_list *lst, void (*f)(void *))` | Applies function f to each node in lst | - | OK
ft_lstmap | `t_list	 *ft_lstmap(t_list *lst, void *(*f)(void *), void (*del)(void *))` | Applies function f to each node in lst, returning a new list with the results. Node content is freed with del wherever necessary. [requires malloc & free] | New list | OK

## Later Additions

### Altered/Improved Functions

Reason | Function | Format | Modified
--- | --- | --- | ---
ft_printf | ft_putchar_fd | `int	ft_putchar_fd(char c, int fd);` | Function now returns int with value 1
ft_printf | ft_putstr_fd | `int	ft_putstr_fd(char *str, int fd);` | Function now returns printed length. If str is NULL, function prints (null)
ft_printf | ft_putnbr_fd | `int	ft_putnbr_fd(long n, int fd);` | Function now accepts numbers in "long" format, and returns printed length
get_next_line | ft_strchr | `char	*ft_strchr(const char *str, int c)` | Function now returns 0 on error
push_swap | ft_isdigit | `bool	ft_isdigit(int c)` | Function now returns a boolean value
push_swap | ft_lstadd_back | `void	ft_lstadd_back(t_stack **lst, t_stack *new)` | Function now considers a 'prev' pointer
revision | ft_isalpha | `bool	ft_isalpha(int c)` | Function now returns a boolean value
revision | ft_isalnum | `bool	ft_isalnum(int c)` | Function now returns a boolean value
revision | ft_isascii | `bool	ft_isascii(int c)` | Function now returns a boolean value
revision | ft_isprint | `bool	ft_isprint(int c)` | Function now returns a boolean value
revision | ft_lstnew | `t_list	*ft_lstnew(void *content)` | Function now considers a 'prev' pointer
revision | ft_lstadd_front | `void	ft_lstadd_front(t_list **lst, t_list *new)` | Function now considers a 'prev' pointer

### New Functions

Function | Format | Description | Return | Status
--- | --- | --- | --- | ---
ft_printf | `int	ft_printf(const char *string, ...)` | Prints a string, converting a series of variables according to a specific cipher [requires va_ functions] | Printed length | OK, but lacks flag implementation
ft_putnbr_ubase_fd | `int	ft_putnbr_ubase_fd(unsigned int nbr, char *base, int fd)` | Prints nbr to the file descriptor fd, in numerical "base" [requires write] | Printed length | OK
ft_putnbr_lbase_fd | `int	ft_putnbr_lbase_fd(unsigned long nbr, char *base, int fd)` | Prints nbr to the file descriptor fd, in numerical "base" [requires write] | Printed length | OK
ft_strbuild | `char	*ft_strbuild(char *s1, const char *s2)` | Based on strjoin. Concatenates s1 and s2 into a new string. Allows s1 to be modified. [requires malloc] | New joined string | OK
ft_atol | `long	ft_atol(const char *str)`  | Converts written number from a string str into long format | The desired number, or 0 if there is none | OK
ft_str_cmp | `bool	ft_str_cmp(const char *s1, const char *s2)` | Checks if strings s1 and s2 are identical | Boolean | OK
ft_rptcheck_str | `bool	ft_rptcheck_str(char **str)` | Checks if an array of strings str has any repeated strings | Boolean | OK
ft_smaller_int | `int	ft_smaller_int(int n1, int n2)` | Determines which value is lowest between n1 and n2 | The smaller value | OK
ft_print_error | `int	ft_print_error(char *str)` | Prints str as an error message, without exiting the program. [requires ft_printf] | 1
