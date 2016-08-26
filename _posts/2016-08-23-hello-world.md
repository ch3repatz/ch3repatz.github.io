---
layout: post
title: Hello, world!
date: 2016-08-23 2:36
math: yes
---

This is just a test :) Math: $e = mc^2$. Code inline: `mov x0, x1`, code block:

```
def __init__(self):
  """
  The constructor
  """
  pass
```

Lorem ipsum dolor sit amet, sea et nostro molestiae constituto, mea te tale virtute detraxit. Saperet probatus at cum. Pro ei populo atomorum elaboraret. Cum adhuc integre ad, nostrum consequuntur duo ad. Suscipit sapientem prodesset usu an, ex eam modo dolorem, bonorum eruditi laboramus eum cu.

<!-- more -->

Ad ridens facilisi sea, decore luptatum sed ex, te fuisset euripidis mei. Sed ea alii soluta doctus, legimus electram erroribus no duo, duo dictas suscipiantur et. Mei in justo neglegentur, ei quo tota everti nostrum. Admodum probatus deserunt his eu, iudico splendide disputando ei eam. His semper salutatus ut, soluta accusamus similique duo at, utroque ocurreret pri an. Ut nusquam postulant vel, et etiam propriae signiferumque his.

Sea ei antiopam recteque. Et putent luptatum vis, sed scribentur efficiantur ea. Quod eripuit qui no, vero fuisset duo ex, vix vero interpretaris no. Odio phaedrum quo ut, sea quaeque definitionem ne, te mea dicunt veritus offendit. Ea cum scaevola pertinax suavitate, est partem tibique concludaturque te. Mutat tollit alterum nec ad, choro everti persequeris ut qui.

```hopper-arm
0x000000018350dfcc F44FBEA9                        stp        x20, x19, [sp, #-0x20]! ; XREF=<redacted>_18350cb0c+360, <redacted>_18350cb0c+440, <redacted>_18350d2cc+1460, <redacted>_18350d2cc+1684, <redacted>_18350d2cc+1764, <redacted>_18350d2cc+1844, <redacted>_18350d2cc+1924, <redacted>_18350dee4+28, <redacted>_18350dee4+72
0x000000018350dfd0 FD7B01A9                        stp        x29, x30, [sp, #0x10]
0x000000018350dfd4 FD430091                        add        x29, sp, #0x10
0x000000018350dfd8 F30302AA                        mov        x19, x2
0x000000018350dfdc F40300AA                        mov        x20, x0
0x000000018350dfe0 000080D2                        movz       x0, #0x0
0x000000018350dfe4 F30200B4                        cbz        x19, 0x18350e040

                                       ; Basic Block Registers Used: r20 - Defined: r8 - Killed: <nothing> - LiveIn: r1 r19 r20 r31 - LiveOut: r1 r8 r19 r20 r31 - AvailIn: r0 r19 r20 r29 - AvailOut: r0 r8 r19 r20 r29
0x000000018350dfe8 880240F9                        ldr        x8, [x20]
0x000000018350dfec A80200B4                        cbz        x8, 0x18350e040

                                       ; Basic Block Registers Used: r19 r20 - Defined: r0 r9 r10 - Killed: <nothing> - LiveIn: r1 r8 r19 r20 r31 - LiveOut: r1 r8 r9 r19 r20 r31 - AvailIn: r0 r8 r19 r20 r29 - AvailOut: r0 r8 r9 r10 r19 r20 r29
0x000000018350dff0 000080D2                        movz       x0, #0x0
0x000000018350dff4 890A40F9                        ldr        x9, [x20, #0x10]
0x000000018350dff8 2A0113AB                        adds       x10, x9, x19
0x000000018350dffc 22020054                        b.hs       0x18350e040

                                       ; Basic Block Registers Used: r9 - Defined: r10 - Killed: <nothing> - LiveIn: r1 r8 r9 r19 r20 r31 - LiveOut: r1 r8 r9 r10 r19 r20 r31 - AvailIn: r0 r8 r9 r10 r19 r20 r29 - AvailOut: r0 r8 r9 r10 r19 r20 r29
0x000000018350e000 5F0109EB                        cmp        x10, x9           ; XREF=<redacted>_18350e22c+176, <redacted>_18350e320+96, <redacted>_18350e714+92, <redacted>_18350ebc8+56, <redacted>_18350ee28+28
0x000000018350e004 E3010054                        b.lo       0x18350e040

                                       ; Basic Block Registers Used: r10 r20 - Defined: r11 - Killed: <nothing> - LiveIn: r1 r8 r9 r10 r19 r20 r31 - LiveOut: r1 r8 r9 r19 r20 r31 - AvailIn: r0 r8 r9 r10 r19 r20 r29 - AvailOut: r0 r8 r9 r10 r11 r19 r20 r29
0x000000018350e008 8B0640F9                        ldr        x11, [x20, #0x8]
0x000000018350e00c 7F010AEB                        cmp        x11, x10
0x000000018350e010 62000054                        b.hs       0x18350e01c

                                       ; Basic Block Registers Used: <nothing> - Defined: r0 - Killed: <nothing> - LiveIn: r31 - LiveOut: r31 - AvailIn: r0 r8 r9 r10 r11 r19 r20 r29 - AvailOut: r0 r8 r9 r10 r11 r19 r20 r29
0x000000018350e014 000080D2                        movz       x0, #0x0
0x000000018350e018 0A000014                        b          0x18350e040

                                       ; Basic Block Registers Used: r1 r8 r9 r19 r20 - Defined: r0 r1 r2 r8 - Killed: r0 r1 r2 r3 r9 r12 r14 r15 s0 s1 s2 s3 s4 s5 s6 s7 s8 s9 s10 s11 s12 s13 s14 s15 d0 d1 d2 d3 d4 d5 d6 d7 d8 d9 d10 d11 d12 d13 d14 d15 q0 q1 q2 q3 q4 q5 q6 q7 q8 q9 q10 q11 q12 q13 q14 q15 - LiveIn: r1 r8 r9 r19 r20 r31 - LiveOut: r31 - AvailIn: r0 r8 r9 r10 r11 r19 r20 r29 - AvailOut: r0 r1 r2 r8 r9 r10 r11 r19 r20 r29
0x000000018350e01c 0801098B                        add        x8, x8, x9        ; XREF=<redacted>_18350dfcc+68
0x000000018350e020 E00301AA                        mov        x0, x1
0x000000018350e024 E10308AA                        mov        x1, x8
0x000000018350e028 E20313AA                        mov        x2, x19
0x000000018350e02c B0D40594                        bl         imp___stubs__memcpy
0x000000018350e030 880A40F9                        ldr        x8, [x20, #0x10]
0x000000018350e034 0801138B                        add        x8, x8, x19
0x000000018350e038 880A00F9                        str        x8, [x20, #0x10]
0x000000018350e03c E00313AA                        mov        x0, x19

                                       ; Basic Block Registers Used: r31 - Defined: r19 r20 r29 r30 - Killed: <nothing> - LiveIn: r31 - LiveOut: <nothing> - AvailIn: r0 r19 r20 r29 - AvailOut: r0 r19 r20 r29 r30
0x000000018350e040 FD7B41A9                        ldp        x29, x30, [sp, #0x10] ; XREF=<redacted>_18350dfcc+24, <redacted>_18350dfcc+32, <redacted>_18350dfcc+48, <redacted>_18350dfcc+56, <redacted>_18350dfcc+76
0x000000018350e044 F44FC2A8                        ldp        x20, x19, [sp], #0x20
0x000000018350e048 C0035FD6                        ret        
                        ; endp
```

Ridens gloriatur pro no, in commodo probatus quo. No usu falli aeterno. Hendrerit constituto definiebas ex mei, ut vix mazim ubique aperiri. Te fugit epicurei verterem qui, in dicta aliquando cum. Ceteros definiebas signiferumque nam ex, assum everti evertitur ut mea, usu persius praesent et. Nam an menandri imperdiet prodesset, te pri harum choro ponderum, eros debitis per ut. Nec nulla meliore suscipit in, omnium nusquam suscipit cu nec, aliquam consequat mnesarchum ad cum.

Cu noluisse repudiare cotidieque vel, ad has tale assueverit referrentur. Ex mei prompta adolescens reformidans. Eum utinam quaestio cu, populo quaestio voluptaria vix id. Ius ad paulo iriure, te eius perpetua mea. At per affert facilisis voluptatibus, ius in purto cibo dolor.

Here we go :)
