# Desarrollo
# Builder 1.0

SOURCE = main.tex $(wildcard src/*.tex)
MAINSR = main.tex
OUTPUT = main.pdf
APP    = pdf/Desarrollo.pdf

# tools:
CC      = pdflatex
VISOR   = xdg-open
VISORER = 2> /dev/null

all: $(APP)

$(APP): $(SOURCE)
	@echo "Compilando Documento:"
	@$(CC) $(MAINSR) 1> /dev/null
	@$(CC) $(MAINSR) 1> /dev/null
	@echo "Compilacion Exitosa."
	@echo "Limpiando temporales"
	@rm *.log *.aux *.out 2> /dev/null
	@echo "Generando Documento"
	@mv main.pdf pdf/Desarrollo.pdf
	@echo "Trabajo finalizado."

.PHONY: clean run

clean:
	@echo "Eliminando pdf..."
	@rm pdf/Desarrollo.pdf 2> /dev/null
	@echo "Finalizado."

run:
	@echo "Mostrando Documento."
	@$(VISOR) $(APP) $(VISORER)
	@echo "Fin ejecucion."
