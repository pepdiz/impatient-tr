# $Id: Makefile,v 1.2 2020/01/03 22:17:40 karl Exp $
# public domain

leng = es

all: $(leng)book.dvi $(leng)book.pdf #$(leng)book.html

$(leng)book.dvi: *.tex
	texfot tex '\nonstopmode\input book'
$(leng)book.pdf: *.tex
	texfot pdftex '\nonstopmode\input book'
$(leng)book.html:
	httex book.tex

files = Makefile README *.tex *.pdf 

dist = impatient-$(leng)
dist: all
	rm -f x.tex
	tar -czf $(dist).tar.gz
	tar tf $(dist).tar.gz | head -4
