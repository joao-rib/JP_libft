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
ft_atoi | `int	ft_atoi(const char *str)` | Converts written number from a string str into int format | The desired number | OK
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

typedef struct s_list
{
	void		*content;
	struct s_list	*next;
}			t_list;

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
