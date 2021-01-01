EXTRA_DIST = gui icons

install-data-local: uninstall-local
	mkdir -p "$(DESTDIR)$(pkgdatadir)"; \
	find $(EXTRA_DIST) | while read dir; do \
		test -d "$$dir" && install -d "$(DESTDIR)$(pkgdatadir)/$$dir"; \
		test -f "$$dir" && install -m644 "$$dir" "$(DESTDIR)$(pkgdatadir)/$$dir"; \
	done

uninstall-local:
	-test -d "$(DESTDIR)$(pkgdatadir)" && rm -rf "$(DESTDIR)$(pkgdatadir)"
