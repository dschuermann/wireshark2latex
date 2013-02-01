
bindir = "../../Script"
pcaplist != ls *.pcap
texlist!= echo ${list} | sed -e s/\.pcap/.tex/

all:
.ifdef pdf
	@echo "Doing PDF from : " ${pdf}
.if !exists(${pdf}.tex)
	@${bindir}/pcap2tex ${pdf}
.endif
	@${bindir}/mkdraft ${pdf} > draft-${pdf}.tex
	@${bindir}/mkpdf draft-${pdf}
	kpdf draft-${pdf}.pdf &
.endif
#
.ifdef tex
	@echo "Doing TeX from : " ${tex}
	@${bindir}/pcap2tex ${tex}
.endif

help:
	@echo "Usage example: 			make pdf=call"
	@echo "Usage example:			make clean"
	@echo "Usage example:			make tex=call"

clean:
.for name in ${texlist}
	@rm -f ${name}
	@rm -f *.log
	@rm -f *.aux
.endfor
	@rm -f draft-*

