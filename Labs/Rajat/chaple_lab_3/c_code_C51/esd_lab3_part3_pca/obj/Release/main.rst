                                      1 ;--------------------------------------------------------
                                      2 ; File Created by SDCC : free open source ANSI-C Compiler
                                      3 ; Version 3.9.0 #11195 (MINGW64)
                                      4 ;--------------------------------------------------------
                                      5 	.module main
                                      6 	.optsdcc -mmcs51 --model-large
                                      7 	
                                      8 ;--------------------------------------------------------
                                      9 ; Public variables in this module
                                     10 ;--------------------------------------------------------
                                     11 	.globl _pwm_init
                                     12 	.globl _dataout
                                     13 	.globl _getchar
                                     14 	.globl _command
                                     15 	.globl _putstr
                                     16 	.globl _echo
                                     17 	.globl _uart_init
                                     18 	.globl _P5_7
                                     19 	.globl _P5_6
                                     20 	.globl _P5_5
                                     21 	.globl _P5_4
                                     22 	.globl _P5_3
                                     23 	.globl _P5_2
                                     24 	.globl _P5_1
                                     25 	.globl _P5_0
                                     26 	.globl _P4_7
                                     27 	.globl _P4_6
                                     28 	.globl _P4_5
                                     29 	.globl _P4_4
                                     30 	.globl _P4_3
                                     31 	.globl _P4_2
                                     32 	.globl _P4_1
                                     33 	.globl _P4_0
                                     34 	.globl _PX0L
                                     35 	.globl _PT0L
                                     36 	.globl _PX1L
                                     37 	.globl _PT1L
                                     38 	.globl _PSL
                                     39 	.globl _PT2L
                                     40 	.globl _PPCL
                                     41 	.globl _EC
                                     42 	.globl _CCF0
                                     43 	.globl _CCF1
                                     44 	.globl _CCF2
                                     45 	.globl _CCF3
                                     46 	.globl _CCF4
                                     47 	.globl _CR
                                     48 	.globl _CF
                                     49 	.globl _TF2
                                     50 	.globl _EXF2
                                     51 	.globl _RCLK
                                     52 	.globl _TCLK
                                     53 	.globl _EXEN2
                                     54 	.globl _TR2
                                     55 	.globl _C_T2
                                     56 	.globl _CP_RL2
                                     57 	.globl _T2CON_7
                                     58 	.globl _T2CON_6
                                     59 	.globl _T2CON_5
                                     60 	.globl _T2CON_4
                                     61 	.globl _T2CON_3
                                     62 	.globl _T2CON_2
                                     63 	.globl _T2CON_1
                                     64 	.globl _T2CON_0
                                     65 	.globl _PT2
                                     66 	.globl _ET2
                                     67 	.globl _CY
                                     68 	.globl _AC
                                     69 	.globl _F0
                                     70 	.globl _RS1
                                     71 	.globl _RS0
                                     72 	.globl _OV
                                     73 	.globl _F1
                                     74 	.globl _P
                                     75 	.globl _PS
                                     76 	.globl _PT1
                                     77 	.globl _PX1
                                     78 	.globl _PT0
                                     79 	.globl _PX0
                                     80 	.globl _RD
                                     81 	.globl _WR
                                     82 	.globl _T1
                                     83 	.globl _T0
                                     84 	.globl _INT1
                                     85 	.globl _INT0
                                     86 	.globl _TXD
                                     87 	.globl _RXD
                                     88 	.globl _P3_7
                                     89 	.globl _P3_6
                                     90 	.globl _P3_5
                                     91 	.globl _P3_4
                                     92 	.globl _P3_3
                                     93 	.globl _P3_2
                                     94 	.globl _P3_1
                                     95 	.globl _P3_0
                                     96 	.globl _EA
                                     97 	.globl _ES
                                     98 	.globl _ET1
                                     99 	.globl _EX1
                                    100 	.globl _ET0
                                    101 	.globl _EX0
                                    102 	.globl _P2_7
                                    103 	.globl _P2_6
                                    104 	.globl _P2_5
                                    105 	.globl _P2_4
                                    106 	.globl _P2_3
                                    107 	.globl _P2_2
                                    108 	.globl _P2_1
                                    109 	.globl _P2_0
                                    110 	.globl _SM0
                                    111 	.globl _SM1
                                    112 	.globl _SM2
                                    113 	.globl _REN
                                    114 	.globl _TB8
                                    115 	.globl _RB8
                                    116 	.globl _TI
                                    117 	.globl _RI
                                    118 	.globl _P1_7
                                    119 	.globl _P1_6
                                    120 	.globl _P1_5
                                    121 	.globl _P1_4
                                    122 	.globl _P1_3
                                    123 	.globl _P1_2
                                    124 	.globl _P1_1
                                    125 	.globl _P1_0
                                    126 	.globl _TF1
                                    127 	.globl _TR1
                                    128 	.globl _TF0
                                    129 	.globl _TR0
                                    130 	.globl _IE1
                                    131 	.globl _IT1
                                    132 	.globl _IE0
                                    133 	.globl _IT0
                                    134 	.globl _P0_7
                                    135 	.globl _P0_6
                                    136 	.globl _P0_5
                                    137 	.globl _P0_4
                                    138 	.globl _P0_3
                                    139 	.globl _P0_2
                                    140 	.globl _P0_1
                                    141 	.globl _P0_0
                                    142 	.globl _EECON
                                    143 	.globl _KBF
                                    144 	.globl _KBE
                                    145 	.globl _KBLS
                                    146 	.globl _BRL
                                    147 	.globl _BDRCON
                                    148 	.globl _T2MOD
                                    149 	.globl _SPDAT
                                    150 	.globl _SPSTA
                                    151 	.globl _SPCON
                                    152 	.globl _SADEN
                                    153 	.globl _SADDR
                                    154 	.globl _WDTPRG
                                    155 	.globl _WDTRST
                                    156 	.globl _P5
                                    157 	.globl _P4
                                    158 	.globl _IPH1
                                    159 	.globl _IPL1
                                    160 	.globl _IPH0
                                    161 	.globl _IPL0
                                    162 	.globl _IEN1
                                    163 	.globl _IEN0
                                    164 	.globl _CMOD
                                    165 	.globl _CL
                                    166 	.globl _CH
                                    167 	.globl _CCON
                                    168 	.globl _CCAPM4
                                    169 	.globl _CCAPM3
                                    170 	.globl _CCAPM2
                                    171 	.globl _CCAPM1
                                    172 	.globl _CCAPM0
                                    173 	.globl _CCAP4L
                                    174 	.globl _CCAP3L
                                    175 	.globl _CCAP2L
                                    176 	.globl _CCAP1L
                                    177 	.globl _CCAP0L
                                    178 	.globl _CCAP4H
                                    179 	.globl _CCAP3H
                                    180 	.globl _CCAP2H
                                    181 	.globl _CCAP1H
                                    182 	.globl _CCAP0H
                                    183 	.globl _CKCON1
                                    184 	.globl _CKCON0
                                    185 	.globl _CKRL
                                    186 	.globl _AUXR1
                                    187 	.globl _AUXR
                                    188 	.globl _TH2
                                    189 	.globl _TL2
                                    190 	.globl _RCAP2H
                                    191 	.globl _RCAP2L
                                    192 	.globl _T2CON
                                    193 	.globl _B
                                    194 	.globl _ACC
                                    195 	.globl _PSW
                                    196 	.globl _IP
                                    197 	.globl _P3
                                    198 	.globl _IE
                                    199 	.globl _P2
                                    200 	.globl _SBUF
                                    201 	.globl _SCON
                                    202 	.globl _P1
                                    203 	.globl _TH1
                                    204 	.globl _TH0
                                    205 	.globl _TL1
                                    206 	.globl _TL0
                                    207 	.globl _TMOD
                                    208 	.globl _TCON
                                    209 	.globl _PCON
                                    210 	.globl _DPH
                                    211 	.globl _DPL
                                    212 	.globl _SP
                                    213 	.globl _P0
                                    214 	.globl _main
                                    215 ;--------------------------------------------------------
                                    216 ; special function registers
                                    217 ;--------------------------------------------------------
                                    218 	.area RSEG    (ABS,DATA)
      000000                        219 	.org 0x0000
                           000080   220 _P0	=	0x0080
                           000081   221 _SP	=	0x0081
                           000082   222 _DPL	=	0x0082
                           000083   223 _DPH	=	0x0083
                           000087   224 _PCON	=	0x0087
                           000088   225 _TCON	=	0x0088
                           000089   226 _TMOD	=	0x0089
                           00008A   227 _TL0	=	0x008a
                           00008B   228 _TL1	=	0x008b
                           00008C   229 _TH0	=	0x008c
                           00008D   230 _TH1	=	0x008d
                           000090   231 _P1	=	0x0090
                           000098   232 _SCON	=	0x0098
                           000099   233 _SBUF	=	0x0099
                           0000A0   234 _P2	=	0x00a0
                           0000A8   235 _IE	=	0x00a8
                           0000B0   236 _P3	=	0x00b0
                           0000B8   237 _IP	=	0x00b8
                           0000D0   238 _PSW	=	0x00d0
                           0000E0   239 _ACC	=	0x00e0
                           0000F0   240 _B	=	0x00f0
                           0000C8   241 _T2CON	=	0x00c8
                           0000CA   242 _RCAP2L	=	0x00ca
                           0000CB   243 _RCAP2H	=	0x00cb
                           0000CC   244 _TL2	=	0x00cc
                           0000CD   245 _TH2	=	0x00cd
                           00008E   246 _AUXR	=	0x008e
                           0000A2   247 _AUXR1	=	0x00a2
                           000097   248 _CKRL	=	0x0097
                           00008F   249 _CKCON0	=	0x008f
                           0000AF   250 _CKCON1	=	0x00af
                           0000FA   251 _CCAP0H	=	0x00fa
                           0000FB   252 _CCAP1H	=	0x00fb
                           0000FC   253 _CCAP2H	=	0x00fc
                           0000FD   254 _CCAP3H	=	0x00fd
                           0000FE   255 _CCAP4H	=	0x00fe
                           0000EA   256 _CCAP0L	=	0x00ea
                           0000EB   257 _CCAP1L	=	0x00eb
                           0000EC   258 _CCAP2L	=	0x00ec
                           0000ED   259 _CCAP3L	=	0x00ed
                           0000EE   260 _CCAP4L	=	0x00ee
                           0000DA   261 _CCAPM0	=	0x00da
                           0000DB   262 _CCAPM1	=	0x00db
                           0000DC   263 _CCAPM2	=	0x00dc
                           0000DD   264 _CCAPM3	=	0x00dd
                           0000DE   265 _CCAPM4	=	0x00de
                           0000D8   266 _CCON	=	0x00d8
                           0000F9   267 _CH	=	0x00f9
                           0000E9   268 _CL	=	0x00e9
                           0000D9   269 _CMOD	=	0x00d9
                           0000A8   270 _IEN0	=	0x00a8
                           0000B1   271 _IEN1	=	0x00b1
                           0000B8   272 _IPL0	=	0x00b8
                           0000B7   273 _IPH0	=	0x00b7
                           0000B2   274 _IPL1	=	0x00b2
                           0000B3   275 _IPH1	=	0x00b3
                           0000C0   276 _P4	=	0x00c0
                           0000E8   277 _P5	=	0x00e8
                           0000A6   278 _WDTRST	=	0x00a6
                           0000A7   279 _WDTPRG	=	0x00a7
                           0000A9   280 _SADDR	=	0x00a9
                           0000B9   281 _SADEN	=	0x00b9
                           0000C3   282 _SPCON	=	0x00c3
                           0000C4   283 _SPSTA	=	0x00c4
                           0000C5   284 _SPDAT	=	0x00c5
                           0000C9   285 _T2MOD	=	0x00c9
                           00009B   286 _BDRCON	=	0x009b
                           00009A   287 _BRL	=	0x009a
                           00009C   288 _KBLS	=	0x009c
                           00009D   289 _KBE	=	0x009d
                           00009E   290 _KBF	=	0x009e
                           0000D2   291 _EECON	=	0x00d2
                                    292 ;--------------------------------------------------------
                                    293 ; special function bits
                                    294 ;--------------------------------------------------------
                                    295 	.area RSEG    (ABS,DATA)
      000000                        296 	.org 0x0000
                           000080   297 _P0_0	=	0x0080
                           000081   298 _P0_1	=	0x0081
                           000082   299 _P0_2	=	0x0082
                           000083   300 _P0_3	=	0x0083
                           000084   301 _P0_4	=	0x0084
                           000085   302 _P0_5	=	0x0085
                           000086   303 _P0_6	=	0x0086
                           000087   304 _P0_7	=	0x0087
                           000088   305 _IT0	=	0x0088
                           000089   306 _IE0	=	0x0089
                           00008A   307 _IT1	=	0x008a
                           00008B   308 _IE1	=	0x008b
                           00008C   309 _TR0	=	0x008c
                           00008D   310 _TF0	=	0x008d
                           00008E   311 _TR1	=	0x008e
                           00008F   312 _TF1	=	0x008f
                           000090   313 _P1_0	=	0x0090
                           000091   314 _P1_1	=	0x0091
                           000092   315 _P1_2	=	0x0092
                           000093   316 _P1_3	=	0x0093
                           000094   317 _P1_4	=	0x0094
                           000095   318 _P1_5	=	0x0095
                           000096   319 _P1_6	=	0x0096
                           000097   320 _P1_7	=	0x0097
                           000098   321 _RI	=	0x0098
                           000099   322 _TI	=	0x0099
                           00009A   323 _RB8	=	0x009a
                           00009B   324 _TB8	=	0x009b
                           00009C   325 _REN	=	0x009c
                           00009D   326 _SM2	=	0x009d
                           00009E   327 _SM1	=	0x009e
                           00009F   328 _SM0	=	0x009f
                           0000A0   329 _P2_0	=	0x00a0
                           0000A1   330 _P2_1	=	0x00a1
                           0000A2   331 _P2_2	=	0x00a2
                           0000A3   332 _P2_3	=	0x00a3
                           0000A4   333 _P2_4	=	0x00a4
                           0000A5   334 _P2_5	=	0x00a5
                           0000A6   335 _P2_6	=	0x00a6
                           0000A7   336 _P2_7	=	0x00a7
                           0000A8   337 _EX0	=	0x00a8
                           0000A9   338 _ET0	=	0x00a9
                           0000AA   339 _EX1	=	0x00aa
                           0000AB   340 _ET1	=	0x00ab
                           0000AC   341 _ES	=	0x00ac
                           0000AF   342 _EA	=	0x00af
                           0000B0   343 _P3_0	=	0x00b0
                           0000B1   344 _P3_1	=	0x00b1
                           0000B2   345 _P3_2	=	0x00b2
                           0000B3   346 _P3_3	=	0x00b3
                           0000B4   347 _P3_4	=	0x00b4
                           0000B5   348 _P3_5	=	0x00b5
                           0000B6   349 _P3_6	=	0x00b6
                           0000B7   350 _P3_7	=	0x00b7
                           0000B0   351 _RXD	=	0x00b0
                           0000B1   352 _TXD	=	0x00b1
                           0000B2   353 _INT0	=	0x00b2
                           0000B3   354 _INT1	=	0x00b3
                           0000B4   355 _T0	=	0x00b4
                           0000B5   356 _T1	=	0x00b5
                           0000B6   357 _WR	=	0x00b6
                           0000B7   358 _RD	=	0x00b7
                           0000B8   359 _PX0	=	0x00b8
                           0000B9   360 _PT0	=	0x00b9
                           0000BA   361 _PX1	=	0x00ba
                           0000BB   362 _PT1	=	0x00bb
                           0000BC   363 _PS	=	0x00bc
                           0000D0   364 _P	=	0x00d0
                           0000D1   365 _F1	=	0x00d1
                           0000D2   366 _OV	=	0x00d2
                           0000D3   367 _RS0	=	0x00d3
                           0000D4   368 _RS1	=	0x00d4
                           0000D5   369 _F0	=	0x00d5
                           0000D6   370 _AC	=	0x00d6
                           0000D7   371 _CY	=	0x00d7
                           0000AD   372 _ET2	=	0x00ad
                           0000BD   373 _PT2	=	0x00bd
                           0000C8   374 _T2CON_0	=	0x00c8
                           0000C9   375 _T2CON_1	=	0x00c9
                           0000CA   376 _T2CON_2	=	0x00ca
                           0000CB   377 _T2CON_3	=	0x00cb
                           0000CC   378 _T2CON_4	=	0x00cc
                           0000CD   379 _T2CON_5	=	0x00cd
                           0000CE   380 _T2CON_6	=	0x00ce
                           0000CF   381 _T2CON_7	=	0x00cf
                           0000C8   382 _CP_RL2	=	0x00c8
                           0000C9   383 _C_T2	=	0x00c9
                           0000CA   384 _TR2	=	0x00ca
                           0000CB   385 _EXEN2	=	0x00cb
                           0000CC   386 _TCLK	=	0x00cc
                           0000CD   387 _RCLK	=	0x00cd
                           0000CE   388 _EXF2	=	0x00ce
                           0000CF   389 _TF2	=	0x00cf
                           0000DF   390 _CF	=	0x00df
                           0000DE   391 _CR	=	0x00de
                           0000DC   392 _CCF4	=	0x00dc
                           0000DB   393 _CCF3	=	0x00db
                           0000DA   394 _CCF2	=	0x00da
                           0000D9   395 _CCF1	=	0x00d9
                           0000D8   396 _CCF0	=	0x00d8
                           0000AE   397 _EC	=	0x00ae
                           0000BE   398 _PPCL	=	0x00be
                           0000BD   399 _PT2L	=	0x00bd
                           0000BC   400 _PSL	=	0x00bc
                           0000BB   401 _PT1L	=	0x00bb
                           0000BA   402 _PX1L	=	0x00ba
                           0000B9   403 _PT0L	=	0x00b9
                           0000B8   404 _PX0L	=	0x00b8
                           0000C0   405 _P4_0	=	0x00c0
                           0000C1   406 _P4_1	=	0x00c1
                           0000C2   407 _P4_2	=	0x00c2
                           0000C3   408 _P4_3	=	0x00c3
                           0000C4   409 _P4_4	=	0x00c4
                           0000C5   410 _P4_5	=	0x00c5
                           0000C6   411 _P4_6	=	0x00c6
                           0000C7   412 _P4_7	=	0x00c7
                           0000E8   413 _P5_0	=	0x00e8
                           0000E9   414 _P5_1	=	0x00e9
                           0000EA   415 _P5_2	=	0x00ea
                           0000EB   416 _P5_3	=	0x00eb
                           0000EC   417 _P5_4	=	0x00ec
                           0000ED   418 _P5_5	=	0x00ed
                           0000EE   419 _P5_6	=	0x00ee
                           0000EF   420 _P5_7	=	0x00ef
                                    421 ;--------------------------------------------------------
                                    422 ; overlayable register banks
                                    423 ;--------------------------------------------------------
                                    424 	.area REG_BANK_0	(REL,OVR,DATA)
      000000                        425 	.ds 8
                                    426 ;--------------------------------------------------------
                                    427 ; internal ram data
                                    428 ;--------------------------------------------------------
                                    429 	.area DSEG    (DATA)
                                    430 ;--------------------------------------------------------
                                    431 ; overlayable items in internal ram 
                                    432 ;--------------------------------------------------------
                                    433 ;--------------------------------------------------------
                                    434 ; Stack segment in internal ram 
                                    435 ;--------------------------------------------------------
                                    436 	.area	SSEG
      000028                        437 __start__stack:
      000028                        438 	.ds	1
                                    439 
                                    440 ;--------------------------------------------------------
                                    441 ; indirectly addressable internal ram data
                                    442 ;--------------------------------------------------------
                                    443 	.area ISEG    (DATA)
                                    444 ;--------------------------------------------------------
                                    445 ; absolute internal ram data
                                    446 ;--------------------------------------------------------
                                    447 	.area IABS    (ABS,DATA)
                                    448 	.area IABS    (ABS,DATA)
                                    449 ;--------------------------------------------------------
                                    450 ; bit data
                                    451 ;--------------------------------------------------------
                                    452 	.area BSEG    (BIT)
                                    453 ;--------------------------------------------------------
                                    454 ; paged external ram data
                                    455 ;--------------------------------------------------------
                                    456 	.area PSEG    (PAG,XDATA)
                                    457 ;--------------------------------------------------------
                                    458 ; external ram data
                                    459 ;--------------------------------------------------------
                                    460 	.area XSEG    (XDATA)
      00138D                        461 _main_i_65536_77:
      00138D                        462 	.ds 2
                                    463 ;--------------------------------------------------------
                                    464 ; absolute external ram data
                                    465 ;--------------------------------------------------------
                                    466 	.area XABS    (ABS,XDATA)
                                    467 ;--------------------------------------------------------
                                    468 ; external initialized ram data
                                    469 ;--------------------------------------------------------
                                    470 	.area XISEG   (XDATA)
                                    471 	.area HOME    (CODE)
                                    472 	.area GSINIT0 (CODE)
                                    473 	.area GSINIT1 (CODE)
                                    474 	.area GSINIT2 (CODE)
                                    475 	.area GSINIT3 (CODE)
                                    476 	.area GSINIT4 (CODE)
                                    477 	.area GSINIT5 (CODE)
                                    478 	.area GSINIT  (CODE)
                                    479 	.area GSFINAL (CODE)
                                    480 	.area CSEG    (CODE)
                                    481 ;--------------------------------------------------------
                                    482 ; interrupt vector 
                                    483 ;--------------------------------------------------------
                                    484 	.area HOME    (CODE)
      002000                        485 __interrupt_vect:
      002000 02 20 06         [24]  486 	ljmp	__sdcc_gsinit_startup
                                    487 ;--------------------------------------------------------
                                    488 ; global & static initialisations
                                    489 ;--------------------------------------------------------
                                    490 	.area HOME    (CODE)
                                    491 	.area GSINIT  (CODE)
                                    492 	.area GSFINAL (CODE)
                                    493 	.area GSINIT  (CODE)
                                    494 	.globl __sdcc_gsinit_startup
                                    495 	.globl __sdcc_program_startup
                                    496 	.globl __start__stack
                                    497 	.globl __mcs51_genXINIT
                                    498 	.globl __mcs51_genXRAMCLEAR
                                    499 	.globl __mcs51_genRAMCLEAR
                                    500 	.area GSFINAL (CODE)
      00205F 02 20 03         [24]  501 	ljmp	__sdcc_program_startup
                                    502 ;--------------------------------------------------------
                                    503 ; Home
                                    504 ;--------------------------------------------------------
                                    505 	.area HOME    (CODE)
                                    506 	.area HOME    (CODE)
      002003                        507 __sdcc_program_startup:
      002003 02 20 97         [24]  508 	ljmp	_main
                                    509 ;	return from main will return to caller
                                    510 ;--------------------------------------------------------
                                    511 ; code
                                    512 ;--------------------------------------------------------
                                    513 	.area CSEG    (CODE)
                                    514 ;------------------------------------------------------------
                                    515 ;Allocation info for local variables in function 'main'
                                    516 ;------------------------------------------------------------
                                    517 ;received_char             Allocated with name '_main_received_char_65536_77'
                                    518 ;i                         Allocated with name '_main_i_65536_77'
                                    519 ;cmd                       Allocated with name '_main_cmd_65536_77'
                                    520 ;command_processed_status  Allocated with name '_main_command_processed_status_65536_77'
                                    521 ;------------------------------------------------------------
                                    522 ;	main.c:35: void main(void)
                                    523 ;	-----------------------------------------
                                    524 ;	 function main
                                    525 ;	-----------------------------------------
      002097                        526 _main:
                           000007   527 	ar7 = 0x07
                           000006   528 	ar6 = 0x06
                           000005   529 	ar5 = 0x05
                           000004   530 	ar4 = 0x04
                           000003   531 	ar3 = 0x03
                           000002   532 	ar2 = 0x02
                           000001   533 	ar1 = 0x01
                           000000   534 	ar0 = 0x00
                                    535 ;	main.c:38: volatile int i = 0;
      002097 90 13 8D         [24]  536 	mov	dptr,#_main_i_65536_77
      00209A E4               [12]  537 	clr	a
      00209B F0               [24]  538 	movx	@dptr,a
      00209C A3               [24]  539 	inc	dptr
      00209D F0               [24]  540 	movx	@dptr,a
                                    541 ;	main.c:48: uart_init();
      00209E 12 21 08         [24]  542 	lcall	_uart_init
                                    543 ;	main.c:49: pwm_init();
      0020A1 12 20 F5         [24]  544 	lcall	_pwm_init
                                    545 ;	main.c:52: IT0 = 1;
                                    546 ;	assignBit
      0020A4 D2 88            [12]  547 	setb	_IT0
                                    548 ;	main.c:53: EX0 = 1;
                                    549 ;	assignBit
      0020A6 D2 A8            [12]  550 	setb	_EX0
                                    551 ;	main.c:54: EA = 1;
                                    552 ;	assignBit
      0020A8 D2 AF            [12]  553 	setb	_EA
                                    554 ;	main.c:58: putstr("\r\n----------------------------------------------------------------------\r\n\r\n");
      0020AA 90 3B 09         [24]  555 	mov	dptr,#___str_0
      0020AD 75 F0 80         [24]  556 	mov	b,#0x80
      0020B0 12 22 2A         [24]  557 	lcall	_putstr
                                    558 ;	main.c:59: putstr("1. Run PWM\r\n2. Stop PWM\r\n3. Set FCLK PERIPH at the minimum frequency\r\n4. Set FCLK PERIPH at the maximum frequency\r\n5. Enter Idle mode \r\n6. Enter Power Down mode ");
      0020B3 90 3B 56         [24]  559 	mov	dptr,#___str_1
      0020B6 75 F0 80         [24]  560 	mov	b,#0x80
      0020B9 12 22 2A         [24]  561 	lcall	_putstr
                                    562 ;	main.c:60: putstr("\r\n----------------------------------------------------------------------\r\n\r\n");
      0020BC 90 3B 09         [24]  563 	mov	dptr,#___str_0
      0020BF 75 F0 80         [24]  564 	mov	b,#0x80
      0020C2 12 22 2A         [24]  565 	lcall	_putstr
                                    566 ;	main.c:61: putstr("Enter command: ");
      0020C5 90 3B F8         [24]  567 	mov	dptr,#___str_2
      0020C8 75 F0 80         [24]  568 	mov	b,#0x80
      0020CB 12 22 2A         [24]  569 	lcall	_putstr
                                    570 ;	main.c:63: while (1)
      0020CE                        571 00102$:
                                    572 ;	main.c:66: received_char = getchar();
      0020CE 12 22 18         [24]  573 	lcall	_getchar
      0020D1 AE 82            [24]  574 	mov	r6,dpl
                                    575 ;	main.c:67: DEBUGPORT(received_char);
      0020D3 90 13 89         [24]  576 	mov	dptr,#_dataout_PARM_2
      0020D6 EE               [12]  577 	mov	a,r6
      0020D7 F0               [24]  578 	movx	@dptr,a
      0020D8 90 FF FF         [24]  579 	mov	dptr,#0xffff
      0020DB 75 F0 00         [24]  580 	mov	b,#0x00
      0020DE C0 06            [24]  581 	push	ar6
      0020E0 12 20 62         [24]  582 	lcall	_dataout
      0020E3 D0 06            [24]  583 	pop	ar6
                                    584 ;	main.c:69: echo(received_char); // echoing characters back
      0020E5 8E 82            [24]  585 	mov	dpl,r6
      0020E7 C0 06            [24]  586 	push	ar6
      0020E9 12 21 13         [24]  587 	lcall	_echo
      0020EC D0 06            [24]  588 	pop	ar6
                                    589 ;	main.c:71: command(received_char);
      0020EE 8E 82            [24]  590 	mov	dpl,r6
      0020F0 12 21 51         [24]  591 	lcall	_command
                                    592 ;	main.c:73: }
      0020F3 80 D9            [24]  593 	sjmp	00102$
                                    594 	.area CSEG    (CODE)
                                    595 	.area CONST   (CODE)
                                    596 	.area CONST   (CODE)
      003B09                        597 ___str_0:
      003B09 0D                     598 	.db 0x0d
      003B0A 0A                     599 	.db 0x0a
      003B0B 2D 2D 2D 2D 2D 2D 2D   600 	.ascii "------------------------------------------------------------"
             2D 2D 2D 2D 2D 2D 2D
             2D 2D 2D 2D 2D 2D 2D
             2D 2D 2D 2D 2D 2D 2D
             2D 2D 2D 2D 2D 2D 2D
             2D 2D 2D 2D 2D 2D 2D
             2D 2D 2D 2D 2D 2D 2D
             2D 2D 2D 2D 2D 2D 2D
             2D 2D 2D 2D
      003B47 2D 2D 2D 2D 2D 2D 2D   601 	.ascii "----------"
             2D 2D 2D
      003B51 0D                     602 	.db 0x0d
      003B52 0A                     603 	.db 0x0a
      003B53 0D                     604 	.db 0x0d
      003B54 0A                     605 	.db 0x0a
      003B55 00                     606 	.db 0x00
                                    607 	.area CSEG    (CODE)
                                    608 	.area CONST   (CODE)
      003B56                        609 ___str_1:
      003B56 31 2E 20 52 75 6E 20   610 	.ascii "1. Run PWM"
             50 57 4D
      003B60 0D                     611 	.db 0x0d
      003B61 0A                     612 	.db 0x0a
      003B62 32 2E 20 53 74 6F 70   613 	.ascii "2. Stop PWM"
             20 50 57 4D
      003B6D 0D                     614 	.db 0x0d
      003B6E 0A                     615 	.db 0x0a
      003B6F 33 2E 20 53 65 74 20   616 	.ascii "3. Set FCLK PERIPH at the minimum frequency"
             46 43 4C 4B 20 50 45
             52 49 50 48 20 61 74
             20 74 68 65 20 6D 69
             6E 69 6D 75 6D 20 66
             72 65 71 75 65 6E 63
             79
      003B9A 0D                     617 	.db 0x0d
      003B9B 0A                     618 	.db 0x0a
      003B9C 34 2E 20 53 65 74 20   619 	.ascii "4. Set FCLK PERIPH at the maximum frequency"
             46 43 4C 4B 20 50 45
             52 49 50 48 20 61 74
             20 74 68 65 20 6D 61
             78 69 6D 75 6D 20 66
             72 65 71 75 65 6E 63
             79
      003BC7 0D                     620 	.db 0x0d
      003BC8 0A                     621 	.db 0x0a
      003BC9 35 2E 20 45 6E 74 65   622 	.ascii "5. Enter Idle mode "
             72 20 49 64 6C 65 20
             6D 6F 64 65 20
      003BDC 0D                     623 	.db 0x0d
      003BDD 0A                     624 	.db 0x0a
      003BDE 36 2E 20 45 6E 74 65   625 	.ascii "6. Enter Power Down mode "
             72 20 50 6F 77 65 72
             20 44 6F 77 6E 20 6D
             6F 64 65 20
      003BF7 00                     626 	.db 0x00
                                    627 	.area CSEG    (CODE)
                                    628 	.area CONST   (CODE)
      003BF8                        629 ___str_2:
      003BF8 45 6E 74 65 72 20 63   630 	.ascii "Enter command: "
             6F 6D 6D 61 6E 64 3A
             20
      003C07 00                     631 	.db 0x00
                                    632 	.area CSEG    (CODE)
                                    633 	.area XINIT   (CODE)
                                    634 	.area CABS    (ABS,CODE)
