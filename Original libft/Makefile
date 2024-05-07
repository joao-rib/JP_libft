NAME = libft.a
CC = cc
FLAGS = -Wall -Wextra -Werror
SRC = $(filter-out $(wildcard *_bonus.c), $(wildcard ft*.c))
OBJ = $(SRC:.c=.o)
BONUS_SRC = $(wildcard ft*_bonus.c)
BONUS_OBJ = $(BONUS_SRC:.c=.o)

all: $(NAME)

%.o: %.c
	$(CC) $(FLAGS) -c $(SRC)

%bonus.o: %bonus.c
	$(CC) $(FLAGS) -c $(BONUS_SRC)

$(NAME): $(OBJ)
	ar -rcs $(NAME) $(OBJ)

clean:
	rm -fr $(OBJ) $(BONUS_OBJ)

fclean:
	rm -fr $(OBJ) $(BONUS_OBJ) $(NAME)

re: fclean all

bonus: $(OBJ) $(BONUS_OBJ)
	ar -rcs $(NAME) $(OBJ) $(BONUS_OBJ)
