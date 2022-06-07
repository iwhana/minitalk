# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Makefile                                           :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: iwhana <iwhana@student.21-school.ru>       +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2021/10/16 19:19:48 by iwhana            #+#    #+#              #
#    Updated: 2021/11/02 19:11:46 by amalia           ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

SERVER_SRCS = server.c
SERVER_OBJS = $(SERVER_SRCS:.c=.o)
SERVER_NAME = server

CLIENT_SRCS = client.c
CLIENT_OBJS = $(CLIENT_SRCS:.c=.o)
CLIENT_NAME = client

NAME = minitalk
RM = rm -f
CC = gcc
CFLAGS = -Wall -Wextra -Werror

$(NAME) : $(SERVER_NAME) $(CLIENT_NAME)

$(SERVER_NAME) : $(SERVER_OBJS)
		$(CC) $(CFLAGS) $^ -o $@

$(CLIENT_NAME) : $(CLIENT_OBJS)
		$(CC) $(CFLAGS) $^ -o $@

all : $(NAME)

clean :
	$(RM) $(SERVER_OBJS) $(CLIENT_OBJS)

fclean : clean
	$(RM) $(SERVER_NAME) $(CLIENT_NAME)

re : fclean all

.PHONY: all clean fclean re
