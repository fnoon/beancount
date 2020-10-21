PYTHON ?= python3

.PHONY:
clean:
	rm -rf input archive


.PHONY:
test-local: clean
	cp -a masters input
	mkdir archive
	../bin/bean-file -o archive bean.cfg input
	find archive -name '*.ofx' -o -name '*.qbo'

.PHONY:
pytest:
	cd .. && $(PYTHON) -m pytest -v -s beancount/ingest/importers
