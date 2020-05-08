# Popt
Source code for the 680x0 Peephole OPTimizer (http://aminet.net/package/dev/asm/popt)

```
Short:        A powerfull assembly source optimizer - v1.0b
Author:       devulder@info.unicaen.fr      (Samuel DEVULDER)
Uploader:     devulder info unicaen fr      (Samuel DEVULDER)
Date:         1996-03-08
Type:         dev/asm
Architecture: m68k-amigaos

                                   Popt
                                   ----
Architecture: m68k-amigaos

        Popt is an  optimizer  of  assembly  sourcefile.  It  does  various
    standard peephole optimizations by pattern-matching. It ranges  from  1
    intruction lookahead to 3 and many more ! It makes more job than  usual
    bluid-in assembler optimizer and uses data-flow analysis to find  which
    register are used or not. With those  informations  it  is  capable  of
    deleting intructions that are of no use and re-assigning  registers  to
    produce a code of better quality/looking. It is specialy  powerfull  on
    code produced by C-compilers (even those that optimize their code !).

	See popt.doc for further explanations.

	If you're a fan of benchmarks,  here is what Popt is  able to do to
    the  well-known   "DHRYSTONE" Benchmark Program   (Reinhold P. Weicker,  
    CACM Vol 27,  No 10, 10/84  pg. 1013) compiled with the  non-registered 
    dcc version of DICE, by Matt DILLON:

    +=====================================================================+
    |                      GVP A530 (68EC030@40Mhz)                       |
    +=====================================================================+
    |                                   | Dhrystones/sec | speed increase |
    +-----------------------------------+----------------+----------------+
    | no opt.             (dhr.a)       |      6846      |      ---       |
    | opt. for 68000      (dhr000.a)    |      7899      |     +15.4%     |
    | opt. for 68020/30   (dhr020.a)    |      8015      |     +17.1%     |
    | opt. for 68020/30   (dhr020i.a) * |      8062      |     +17.8%     |
    | opt. for 68040      (dhr040.a)    |      7830      |     +14.4%     |
    | opt. for 68040      (dhr040i.a) * |      7837      |     +14.5%     |
    +=====================================================================+
    |                      Stock A500 (68000@7Mhz)                        |
    +=====================================================================+
    |                                   | Dhrystones/sec | speed increase |
    +-----------------------------------+----------------+----------------+
    | no opt.             (dhr.a)       |      775       |      ---       |
    | opt. for 68000      (dhr000.a)    |      912       |     +17.7%     |
    | opt. for 68020/30   (dhr020.a)    |      912       |     +17.7%     |
    | opt. for 68040      (dhr040.a)    |      883       |     +13.9%     |
    +-----------------------------------+----------------+----------------+
 
	You can find the source code of those programs  (dhr.a, dh0?0.a) to
    have a look to the quality of the optimisation. The source is dhr.a and
    the destinations are dhr0?0.a.

	This version is a beta version. Little testing has been done. It is
    rather experimantal.  Use it at your own risks.  Please  feel  free  to 
    report any bugs or comments to me.

        Happy optimizations !
 
                Sam.

_________________
* The star indicates that the code uses special 68020+ instructions or
  addressing modes.
```