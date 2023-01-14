# Update translations when the english master changes

NAME=remove-old-kernels

all:

update-po:
	for i in *.po; do \
		msgmerge -v --no-wrap --previous --backup=none --update $$i $(NAME).pot; \
		done
