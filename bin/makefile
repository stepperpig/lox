JFLAGS = -g
JC = javac
.SUFFIXES: .java .class
.java.class: 
	$(JC) $(JFLAGS) $*.java

# This uses the line continuation character (\) for readability
# You can list these all on a single line, separated by a space instead.
# If your version of make can't handle the leading tabs on each
# line, just remove them (these are also just added for readability).
CLASSES = \
		TokenType.java \
		Token.java \
        Scanner.java \
        Lox.java 

default: classes

classes: $(CLASSES:.java=.class)

clean: 
	rm *.class