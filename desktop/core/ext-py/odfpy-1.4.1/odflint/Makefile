all: odf odflint.1


%.1: %.docbook 
	xmlto man $<

%.txt: %.docbook 
	xmlto txt $<

clean:
	rm -f *.1 *~ *.txt odf
odf:
	ln -s ../odf

test: clean odf
	@echo ================== output by Python2 ======================
	@python2 odflint ../tests/examples/simplestyles.odt
	@echo ================== output by Python3 ======================
	@python3 odflint ../tests/examples/simplestyles.odt
