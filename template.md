COBOL

- History of the language: who/when invented it, which languages influenced it, etc.

COBOL(common business-oriented language) is an English-like programming language designed for business usage. Cobol is a legacy language, which means the language is not relevant to up-to-date systems. Cobol created around 1959, developed by Conference on Data Systems Languages (CODASYL). It is developed on previous programming language design by Grace Hopper. Cobol was one of the first high level programming language created.

Around 1980’s, some small businesses moved a part of their mainframe Cobol programs to PC. In the 1990’s, Cobol considered an old and non relevant programming language of the past because of rise of object-oriented programming. Cobol was not completely thrown away, some of banks and corporations that want reliable and stable programs kept using Cobol. In 1997, the Gartner Group (a global research company) reported that %80 of world’s business ran on Cobol.

While object orienting is rising, Cobol’s transformation was inevitable. Project of object-oriented Cobol started from early 90’s. Object-oriented features were added from C++ and Smalltalk. Fınal form of ISO standart approved in 2002. This version of Cobol was named Cobol 2002.

Cobol 2002 was not supported enough to fully functional, no compilers completely supported the standart. Researchs found out that it was due to lack of user demand for the new features and abortion of testing platform for compiler compatibility. 
Today, Cobol is not dead at all. During 2020 Coronavirus pandemic, a part of US states reported a shortage of skilled Cobol programmers to support the legacy systems, which means Cobol programs still running around the world at substantial degrees.

- Why was it invented

In late 1950s, not long ago from creation of Cobol, programming costs was rising at huge amounts. Back in the days, in any data processing installation, programming cost 800,000 $ average and translating programs to new hardware would cost 600,000 $. To decrease thsese costs, the survey that found out the costs, suggested that a new language design would decrease the cost and time.

- When/why shall we use it

“The problem to solve should determine the language to use.”. Cobol’s strenght lies in processing financial-style data and number crunching.
Cobol survived and transformed since 1959, language is very adaptive. It has been changed to the ways that shaped by user’s demands for 50 years.
It integrates with the next-gen languages like C#, Java.
It easy to learn since language’s structure is like English.

- How to setup an environment to use it in different platforms

Firstly, there are many online compilers, one of them can be used with any browser available.
In Windows, Cobol can be used via IDEs, Visual Studio.

But it is possible to emulate mainframe and use Cobol in emulator.
In Windows, Hercules mainframe emulator can be used. Hercules is a software implementation of IBM System/370 and ESA/390 mainframe hardware which runs under Linux on a PC. Before start only Cobol compiler from MVT addon is needed.

In Linux or Unix, cobol compiler needed. To add cobol compiler to system;


$ sudo apt-get install open-cobol


To be display if compiler is installed;


$ whereis cobc
cobc: /usr/bin/cobc /usr/share/man/man1/cobc.1.gz

$ which cobc
/usr/bin/cobc


Cobol program can be written by using Vim editor.

- Example codes

Cobol structed with 4 divisions. Divisions are set of codes.

Identification Division: contains program name, programmer name, other items to identify the program.

Environment Division: This division is optional, contains data to specify computer and other devices used to compile and execute the program.

Data Division: Optional division, contains data items which are names, lenghts, storage formats etc.

Procedure Division: Simply contains operations of program.

A Hello World program:

   IDENTIFICATION DIVISION.

   PROGRAM-ID. HELLO-WORLD.  *> setting program id

   PROCEDURE DIVISION.      
      DISPLAY 'Hello world!'.  *>printing Hello World! string
      STOP RUN. *> end program
      
      
 Program to display declared variables:
 
           IDENTIFICATION DIVISION.
            PROGRAM-ID. VARS.
            DATA DIVISION.
                                
              WORKING-STORAGE SECTION. *> working storage defines variables
   

              01 FIRST-VAR PIC S9(3)V9(2). *> a number with S-->sign, 9(3)-->3 numbers, V-->decimal, 9(2)-->2 numbers
              *> It will be filled with 0 by default.
              
              01 SECOND-VAR PIC S9(3)V9(2) VALUE -111.22. *>same as FIRST-VAR variable but not filled with 0s, it will be -123.45

              
              01 THIRD-VAR PIC A(6) VALUE 'AKDNZU'. *> A string, 'AKDNZU'
              
              01 FOURTH-VAR PIC X(5) VALUE 'AKDNZ$'. *> alphanumeric string, 'AKDNZ$'
              
              01 GROUP-VAR. *> a grouped variable
                05 SUBVAR-1 PIC 9(4) VALUE 1982.
                05 SUBVAR-2 PIC X(15) VALUE 'AKDENIZ'.
                05 SUBVAR-3 PIC X(15) VALUE 'UNIVERSITY'.
                05 SUBVAR-4 PIC X(15) VALUE 'CSE'. *> 3 alphanumeriz string variables but all of the space didn't used
      
            *> printing
            PROCEDURE DIVISION.
              DISPLAY "1ST VAR :"FIRST-VAR.
              DISPLAY "2ND VAR :"SECOND-VAR.
              DISPLAY "3RD VAR :"THIRD-VAR.
              DISPLAY "4TH VAR :"FOURTH-VAR.
              DISPLAY "GROUP VAR :"GROUP-VAR.
              STOP RUN.
            
Output:
1ST VAR :+000.00
2ND VAR :-123.45
3RD VAR :AKDNZU
4TH VAR :AKDNZ
GROUP VAR :1982AKDENIZ        UNIVERSITY     CSE 

- Things that are specific to this language?

Divisions are specific to COBOL.

Syntax is like speaking language more than mathematical basis, normally situation where x equals y specified like x = y, in cobol it is shown by MOVE x TO y.

In cobol, columns are divided to specific identifiers(like first 6 columns of character specifies line number, column 7 reserved for special characters etc.).
