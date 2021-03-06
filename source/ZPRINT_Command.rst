==============
ZPRINT Command
==============

Material prepared from `M Programming Book`_ [WALTERS1997]_

Page 208

ZPRINT "routine" prints lines of source code, from starting and ending labels::

    ZPRINT <position1>:[position2]

Position1 is given as a label to start at, possibly with an offset.  Position2 (optional) is where to end.  If position2 is not provided, will only print the line at position1.

Examples::

    GTM>zprint fib^helloworld1
    fib ; fibinachi

    GTM>zprint fib^helloworld1:fib+5
    fib ; fibinachi
     s a=1 w a,!
     s b=2 w b,!
     for i=1:1:100 do
     . s c=a+b w c,!
     . s a=b s b=c

    GTM>zprint fib+-5^helloworld1:fib
     for i=1:1:10 do
     . write i
     . write "--",!
     quit
 
    fib ; fibinachi


.. _M Programming book: http://books.google.com/books?id=jo8_Mtmp30kC&printsec=frontcover&dq=M+Programming&hl=en&sa=X&ei=2mktT--GHajw0gHnkKWUCw&ved=0CDIQ6AEwAA#v=onepage&q=M%20Programming&f=false
