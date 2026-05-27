cmake_minimum_required(VERSION 3.20)

project(PetukhPlusPlus)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_executable(GovorPlusPlus
        src/main.cpp

        src/lexer/Token.h

        src/lexer/Lexer.h
        src/lexer/Lexer.cpp

        src/lexer/Trie.h
        src/lexer/Trie.cpp

        src/parser/AST.h

        src/parser/Parser.h
        src/parser/Parser.cpp

        src/parser/ASTPrinter.h
        src/parser/ASTPrinter.cpp
        src/semantics/SemanticAnalyzer.h
        src/semantics/SemanticAnalyzer.cpp

        src/rpn/RPNGenerator.h
        src/rpn/RPNGenerator.cpp
        src/rpn/RPNInstruction.h
        src/rpn/LabelManager.h

        src/vm/Value.h
        src/vm/VM.h
        src/vm/VM.cpp
)

if(APPLE)
    target_link_libraries(GovorPlusPlus PRIVATE c++)
endif()
