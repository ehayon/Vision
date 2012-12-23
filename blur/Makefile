DIR = ./
SRC = demo1.c
OBJ = $(SRC:.c=.o)
NAME = 
TMS = demo1.c
TMO = $(TMS:.c=.o)
TMN = main
LIBS =
OPENCV_FLAGS = `pkg-config opencv --cflags --libs`
LIBPATH = .
RM = rm -f

all: $(OBJ)

test: $(NAME) $(TMO)
	cc $(OPENCV_FLAGS) -L$(LIBPATH) $(LIBS) $(TMO) -o $(TMN)

clean:
	-$(RM) $(OBJ)
	-$(RM) *~
	-$(RM) \#*
	-$(RM) *.core

fclean: clean
	-$(RM) $(NAME)
	-$(RM) $(TMN)

re: fclean all

$(NAME): all

ftest: fclean test
