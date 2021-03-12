![Rain Seattle Annual - 19481979](https://user-images.githubusercontent.com/73729810/110890103-3fb4e800-82a4-11eb-80f6-771265968337.png)
# hello-world
Ken's first branch via tutorial step-by-step @ https://guides.github.com/activities/hello-world/
# hello-world inside comment
#             inside comment 2
#         2-5-21  comment
#         2-5-21  comment 2
#         3-11-21 comment added
#         3-11-21 comment 2 added to main
#         pasted from clipboard
import java.util.Scanner;

import java.text.NumberFormat;

public class Arith6

{

public static void main(String[] args)

{

System.out.println("----------------Arith6");     

double A =  5;  

int B    =  6;  

double C = A + B;

System.out.println( C  );

System.out.println( A + B);

System.out.println( 5 + 6 );

System.out.println( 5   ==  6);

System.out.println( 5 + 6   ==  6 + 5);
      }
}

       IDENTIFICATION DIVISION.
       PROGRAM-ID.       COBSHEL.
       DATE-COMPILED.   01/01/2015.
       ENVIRONMENT DIVISION.
       INPUT-OUTPUT SECTION.
       FILE-CONTROL.
      **********************************************************
      **  THE DD NAME FOR THE DEPARTMENT FILE IS DEPTFILE   ****
      **  LOOK FOR //DEPTFILE  DD  DSN= . . .  IN THE JCL   ****
      **********************************************************
           SELECT DEPT-FILE  ASSIGN TO DEPTFILE.
       DATA DIVISION.
       FILE SECTION.

       FD  DEPT-FILE
           RECORD CONTAINS 80 CHARACTERS
           BLOCK  CONTAINS  0 RECORDS
           RECORDING  MODE IS F.
        01  DEPT-RECORD          PIC X(80).

       WORKING-STORAGE SECTION.
       01  WS-DEPT-EOF     PIC X(03)     VALUE SPACES.
       01  WS-DEPT-RECORD  PIC X(80).
       LINKAGE SECTION.

       PROCEDURE DIVISION.
       0000-MAIN.
           DISPLAY '0000-MAIN'

           PERFORM 1000-PROCESS-DEPT-FILE

           GOBACK
            .


       1000-PROCESS-DEPT-FILE.
      **********************************************************
      ***  OPEN THE DEPARTMENT FILE TO ALLOW FOR PROCESSING   **
      ***  PROCESS THE DEPARTMENT FILE IN THE 1000- PARAGRAPH **
      ***  CLOSE THE DEPARTMENT FILE WHEN THE PROCESSING IN   **
      ***      PARAGRAPH 1100- IS FINISHED                    **
      **********************************************************
           DISPLAY '1000-PROCESS-DEPT-FILE'

           OPEN INPUT DEPT-FILE

           PERFORM 1100-PROCESS-DEPT-RECORD

           CLOSE DEPT-FILE
            .

       1100-PROCESS-DEPT-RECORD.
      **********************************************************
      ********  READ ONE RECORD FROM THE DEPARTMENT FILE  ******
      **********************************************************
           DISPLAY '1100-PROCESS-DEPT-RECORD'

           READ DEPT-FILE INTO  WS-DEPT-RECORD
               AT END      MOVE 'END' TO WS-DEPT-EOF
               NOT AT END  DISPLAY WS-DEPT-RECORD
           END-READ
           .
      ********  END OF PROGRAM    COBSHEL ***********************   
