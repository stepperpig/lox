JFLAGS = -g
JC = javac
JAVA = java
LOX_SUBDIR = com/craftinginterpreters/lox/
TOOL_SUBDIR = com/craftinginterpreters/tool/
.SUFFIXES: .java .class
.java.class: 
	$(JC) $(JFLAGS) $*.java

# This uses the line continuation character (\) for readability
# You can list these all on a single line, separated by a space instead.
# If your version of make can't handle the leading tabs on each
# line, just remove them (these are also just added for readability).
CLASSES = \
		  $(LOX_SUBDIR)Environment.java \
		  $(LOX_SUBDIR)Expr.java \
		  $(LOX_SUBDIR)Interpreter.java \
          $(LOX_SUBDIR)Lox.java \
		  $(LOX_SUBDIR)LoxCallable.java \
		  $(LOX_SUBDIR)LoxFunction.java \
		  $(LOX_SUBDIR)Parser.java \
		  $(LOX_SUBDIR)Return.java \
		  $(LOX_SUBDIR)RuntimeError.java \
		  $(LOX_SUBDIR)Scanner.java \
		  $(LOX_SUBDIR)Stmt.java \
		  $(LOX_SUBDIR)Token.java \
		  $(LOX_SUBDIR)TokenType.java \

default: classes

classes: $(CLASSES:.java=.class)

clean_lox: 
	rm $(LOX_SUBDIR)*.class

clean_tool:
	rm $(TOOL_SUBDIR)*.class

run:
	$(JAVA) $(LOX_SUBDIR)Lox

clean: clean_lox clean_tool
