# Update translations when the english master changes

NAME=remove-old-kernels

update-pot:
	xgettext -i ../$(NAME) -L Shell -o $(NAME).pot \
		--no-wrap \
		--package-name=$(NAME)

update-po:
	for i in *.po; do \
		msgmerge -v --no-wrap --previous --backup=none --update $$i $(NAME).pot; \
		done
