# BA_roofline

CPU name:	Intel(R) Xeon(R) CPU E5-2699 v3 @ 2.30GHz
CPU type:	Intel Xeon Haswell EN/EP/EX processor
CPU clock:	2.29 GHz

* Control Group

Result of likwid under roof_latency group for 1s sleep
Number of cores used: 18
Run 5 times and calculate the average

* The first take
![](pictures/cft1.png)
![](pictures/cft2.png)
![](pictures/cft3.png)

* The second take
+----------------------------------------+----------+-----------+-----+-----------+--------------+
|                  Event                 |  Counter |    Sum    | Min |    Max    |      Avg     |
+----------------------------------------+----------+-----------+-----+-----------+--------------+
|         INSTR_RETIRED_ANY STAT         |   FIXC0  |  43198827 |   0 |   9953040 | 2.399935e+06 |
|       CPU_CLK_UNHALTED_CORE STAT       |   FIXC1  |  83577218 |   0 |  12394536 | 4.643179e+06 |
|        CPU_CLK_UNHALTED_REF STAT       |   FIXC2  | 154661752 |   0 |  23089102 | 8.592320e+06 |
|  CYCLE_ACTIVITY_STALLS_L2_PENDING STAT |   PMC0   |  33547907 |   0 |   4591096 | 1.863773e+06 |
| CYCLE_ACTIVITY_STALLS_LDM_PENDING STAT |   PMC1   |  58800639 |   0 |   7782826 | 3.266702e+06 |
|    CYCLE_ACTIVITY_STALLS_TOTAL STAT    |   PMC2   |  62950766 |   0 |   8242624 | 3.497265e+06 |
|           LLC_LOOKUP_ANY STAT          |  CBOX0C0 |    244239 |   0 |    244239 |   13568.8333 |
|           LLC_LOOKUP_ANY STAT          |  CBOX1C0 |    232412 |   0 |    232412 |   12911.7778 |
|           LLC_LOOKUP_ANY STAT          |  CBOX2C0 |    282597 |   0 |    282597 |   15699.8333 |
|           LLC_LOOKUP_ANY STAT          |  CBOX3C0 |    247894 |   0 |    247894 |   13771.8889 |
|           LLC_LOOKUP_ANY STAT          |  CBOX4C0 |    245431 |   0 |    245431 |   13635.0556 |
|           LLC_LOOKUP_ANY STAT          |  CBOX5C0 |    221222 |   0 |    221222 |   12290.1111 |
|           LLC_LOOKUP_ANY STAT          |  CBOX6C0 |    342116 |   0 |    342116 |   19006.4444 |
|           LLC_LOOKUP_ANY STAT          |  CBOX7C0 |    261060 |   0 |    261060 |   14503.3333 |
|           LLC_LOOKUP_ANY STAT          |  CBOX8C0 |    262228 |   0 |    262228 |   14568.2222 |
|           LLC_LOOKUP_ANY STAT          |  CBOX9C0 |    273570 |   0 |    273570 |   15198.3333 |
|           LLC_LOOKUP_ANY STAT          | CBOX10C0 |    231627 |   0 |    231627 |   12868.1667 |
|           LLC_LOOKUP_ANY STAT          | CBOX11C0 |    236416 |   0 |    236416 |   13134.2222 |
|           LLC_LOOKUP_ANY STAT          | CBOX12C0 |    234998 |   0 |    234998 |   13055.4444 |
|           LLC_LOOKUP_ANY STAT          | CBOX13C0 |    233971 |   0 |    233971 |   12998.3889 |
|           LLC_LOOKUP_ANY STAT          | CBOX14C0 |    253244 |   0 |    253244 |   14069.1111 |
|           LLC_LOOKUP_ANY STAT          | CBOX15C0 |    310193 |   0 |    310193 |   17232.9444 |
|           LLC_LOOKUP_ANY STAT          | CBOX16C0 |    230307 |   0 |    230307 |   12794.8333 |
|           LLC_LOOKUP_ANY STAT          | CBOX17C0 |    267147 |   0 |    267147 |   14841.5000 |
|        LLC_LOOKUP_DATA_READ STAT       |  CBOX0C1 |     71928 |   0 |     71928 |         3996 |
|        LLC_LOOKUP_DATA_READ STAT       |  CBOX1C1 |     65754 |   0 |     65754 |         3653 |
|        LLC_LOOKUP_DATA_READ STAT       |  CBOX2C1 |     86831 |   0 |     86831 |    4823.9444 |
|        LLC_LOOKUP_DATA_READ STAT       |  CBOX3C1 |     69743 |   0 |     69743 |    3874.6111 |
|        LLC_LOOKUP_DATA_READ STAT       |  CBOX4C1 |     75019 |   0 |     75019 |    4167.7222 |
|        LLC_LOOKUP_DATA_READ STAT       |  CBOX5C1 |     65044 |   0 |     65044 |    3613.5556 |
|        LLC_LOOKUP_DATA_READ STAT       |  CBOX6C1 |    115825 |   0 |    115825 |    6434.7222 |
|        LLC_LOOKUP_DATA_READ STAT       |  CBOX7C1 |     73764 |   0 |     73764 |         4098 |
|        LLC_LOOKUP_DATA_READ STAT       |  CBOX8C1 |     78664 |   0 |     78664 |    4370.2222 |
|        LLC_LOOKUP_DATA_READ STAT       |  CBOX9C1 |     86718 |   0 |     86718 |    4817.6667 |
|        LLC_LOOKUP_DATA_READ STAT       | CBOX10C1 |     66712 |   0 |     66712 |    3706.2222 |
|        LLC_LOOKUP_DATA_READ STAT       | CBOX11C1 |     67275 |   0 |     67275 |    3737.5000 |
|        LLC_LOOKUP_DATA_READ STAT       | CBOX12C1 |     69522 |   0 |     69522 |    3862.3333 |
|        LLC_LOOKUP_DATA_READ STAT       | CBOX13C1 |     67040 |   0 |     67040 |    3724.4444 |
|        LLC_LOOKUP_DATA_READ STAT       | CBOX14C1 |     71203 |   0 |     71203 |    3955.7222 |
|        LLC_LOOKUP_DATA_READ STAT       | CBOX15C1 |    102792 |   0 |    102792 |    5710.6667 |
|        LLC_LOOKUP_DATA_READ STAT       | CBOX16C1 |     58793 |   0 |     58793 |    3266.2778 |
|        LLC_LOOKUP_DATA_READ STAT       | CBOX17C1 |     77953 |   0 |     77953 |    4330.7222 |
|          LLC_LOOKUP_READ STAT          |  CBOX0C2 |    185440 |   0 |    185440 |   10302.2222 |
|          LLC_LOOKUP_READ STAT          |  CBOX1C2 |    167828 |   0 |    167828 |    9323.7778 |
|          LLC_LOOKUP_READ STAT          |  CBOX2C2 |    208123 |   0 |    208123 |   11562.3889 |
|          LLC_LOOKUP_READ STAT          |  CBOX3C2 |    182111 |   0 |    182111 |   10117.2778 |
|          LLC_LOOKUP_READ STAT          |  CBOX4C2 |    182080 |   0 |    182080 |   10115.5556 |
|          LLC_LOOKUP_READ STAT          |  CBOX5C2 |    165442 |   0 |    165442 |    9191.2222 |
|          LLC_LOOKUP_READ STAT          |  CBOX6C2 |    255587 |   0 |    255587 |   14199.2778 |
|          LLC_LOOKUP_READ STAT          |  CBOX7C2 |    196173 |   0 |    196173 |   10898.5000 |
|          LLC_LOOKUP_READ STAT          |  CBOX8C2 |    189999 |   0 |    189999 |   10555.5000 |
|          LLC_LOOKUP_READ STAT          |  CBOX9C2 |    204681 |   0 |    204681 |   11371.1667 |
|          LLC_LOOKUP_READ STAT          | CBOX10C2 |    168587 |   0 |    168587 |    9365.9444 |
|          LLC_LOOKUP_READ STAT          | CBOX11C2 |    175654 |   0 |    175654 |    9758.5556 |
|          LLC_LOOKUP_READ STAT          | CBOX12C2 |    173090 |   0 |    173090 |    9616.1111 |
|          LLC_LOOKUP_READ STAT          | CBOX13C2 |    170558 |   0 |    170558 |    9475.4444 |
|          LLC_LOOKUP_READ STAT          | CBOX14C2 |    190344 |   0 |    190344 |   10574.6667 |
|          LLC_LOOKUP_READ STAT          | CBOX15C2 |    238551 |   0 |    238551 |   13252.8333 |
|          LLC_LOOKUP_READ STAT          | CBOX16C2 |    160782 |   0 |    160782 |    8932.3333 |
|          LLC_LOOKUP_READ STAT          | CBOX17C2 |    189014 |   0 |    189014 |   10500.7778 |
|          LLC_LOOKUP_WRITE STAT         |  CBOX0C3 |     16212 |   0 |     16212 |     900.6667 |
|          LLC_LOOKUP_WRITE STAT         |  CBOX1C3 |     17785 |   0 |     17785 |     988.0556 |
|          LLC_LOOKUP_WRITE STAT         |  CBOX2C3 |     31182 |   0 |     31182 |    1732.3333 |
|          LLC_LOOKUP_WRITE STAT         |  CBOX3C3 |     23395 |   0 |     23395 |    1299.7222 |
|          LLC_LOOKUP_WRITE STAT         |  CBOX4C3 |     22618 |   0 |     22618 |    1256.5556 |
|          LLC_LOOKUP_WRITE STAT         |  CBOX5C3 |     18291 |   0 |     18291 |    1016.1667 |
|          LLC_LOOKUP_WRITE STAT         |  CBOX6C3 |     33207 |   0 |     33207 |    1844.8333 |
|          LLC_LOOKUP_WRITE STAT         |  CBOX7C3 |     18609 |   0 |     18609 |    1033.8333 |
|          LLC_LOOKUP_WRITE STAT         |  CBOX8C3 |     24270 |   0 |     24270 |    1348.3333 |
|          LLC_LOOKUP_WRITE STAT         |  CBOX9C3 |     29655 |   0 |     29655 |    1647.5000 |
|          LLC_LOOKUP_WRITE STAT         | CBOX10C3 |     21369 |   0 |     21369 |    1187.1667 |
|          LLC_LOOKUP_WRITE STAT         | CBOX11C3 |     20285 |   0 |     20285 |    1126.9444 |
|          LLC_LOOKUP_WRITE STAT         | CBOX12C3 |     21303 |   0 |     21303 |    1183.5000 |
|          LLC_LOOKUP_WRITE STAT         | CBOX13C3 |     18870 |   0 |     18870 |    1048.3333 |
|          LLC_LOOKUP_WRITE STAT         | CBOX14C3 |     18827 |   0 |     18827 |    1045.9444 |
|          LLC_LOOKUP_WRITE STAT         | CBOX15C3 |     23400 |   0 |     23400 |         1300 |
|          LLC_LOOKUP_WRITE STAT         | CBOX16C3 |     30992 |   0 |     30992 |    1721.7778 |
|          LLC_LOOKUP_WRITE STAT         | CBOX17C3 |     40777 |   0 |     40777 |    2265.3889 |
|            CAS_COUNT_RD STAT           |  MBOX0C0 |    113528 |   0 |    113528 |    6307.1111 |
|            CAS_COUNT_WR STAT           |  MBOX0C1 |     28674 |   0 |     28674 |         1593 |
|            CAS_COUNT_RD STAT           |  MBOX1C0 |    123754 |   0 |    123754 |    6875.2222 |
|            CAS_COUNT_WR STAT           |  MBOX1C1 |     32855 |   0 |     32855 |    1825.2778 |
|            CAS_COUNT_RD STAT           |  MBOX4C0 |     93528 |   0 |     93528 |         5196 |
|            CAS_COUNT_WR STAT           |  MBOX4C1 |     19811 |   0 |     19811 |    1100.6111 |
|            CAS_COUNT_RD STAT           |  MBOX5C0 |    123357 |   0 |    123357 |    6853.1667 |
|            CAS_COUNT_WR STAT           |  MBOX5C1 |     36053 |   0 |     36053 |    2002.9444 |
|            UNCORE_CLOCK STAT           |  UBOXFIX | 697323148 |   0 | 697323148 | 3.874017e+07 |
|           PWR_PKG_ENERGY STAT          |   PWR0   |   16.0503 |   0 |   16.0503 |       0.8917 |
|          PWR_DRAM_ENERGY STAT          |   PWR3   |    2.3318 |   0 |    2.3318 |       0.1295 |
+----------------------------------------+----------+-----------+-----+-----------+--------------+

+----------------------------------------+--------------+--------------+--------------+--------------+
|                 Metric                 |      Sum     |      Min     |      Max     |      Avg     |
+----------------------------------------+--------------+--------------+--------------+--------------+
|     Time: Runtime (RDTSC) [s] STAT     |      17.8308 |       0.9906 |       0.9906 |       0.9906 |
|     Time: Runtime unhalted [s] STAT    |       0.0675 |            0 |       0.0101 |       0.0038 |
|            inverseClock STAT           | 7.844234e-09 | 4.357908e-10 | 4.357908e-10 | 4.357908e-10 |
|            Clock [MHz] STAT            |   20864.3966 |    1196.9087 |    1571.8162 |    1159.1331 |
|         Uncore Clock [MHz] STAT        |     703.9413 |            0 |     703.9413 |      39.1078 |
|       Time: Core total stall STAT      |       0.0509 | 2.491276e-05 |       0.0067 |       0.0028 |
|        Time: Core l2 stall STAT        |       0.0269 | 1.656730e-05 |       0.0037 |       0.0015 |
|        Time: Core ldm stall STAT       |       0.0474 | 1.873907e-05 |       0.0063 |       0.0026 |
|                CPI STAT                |      34.2575 |       1.0331 |       3.7368 |       1.9032 |
|           Power PKG [W] STAT           |      16.2026 |            0 |      16.2026 |       0.9001 |
|           Power DRAM [W] STAT          |       2.3539 |            0 |       2.3539 |       0.1308 |
|           Energy PKG [J] STAT          |      16.0503 |            0 |      16.0503 |       0.8917 |
|          Energy DRAM [J] STAT          |       2.3318 |            0 |       2.3318 |       0.1295 |
|           L2M Pending[%] STAT          |     653.7438 |      28.6600 |      50.2432 |      36.3191 |
|           LD Pending[%] STAT           |    1025.0537 |      32.3121 |      80.7195 |      56.9474 |
|    LLC Any bandwidth [Bytes/s] STAT    |    297883600 |            0 |    297883600 | 1.654909e+07 |
| LLC data read bandwidth [Bytes/s] STAT |     88549620 |            0 |     88549620 | 4.919423e+06 |
|    LLC read bandwidth [Bytes/s] STAT   |    219926500 |            0 |    219926500 | 1.221814e+07 |
|   LLC write bandwidth [Bytes/s] STAT   |     27848830 |            0 |     27848830 | 1.547157e+06 |
|       LLC Any volume [Bytes] STAT      |    295083008 |            0 |    295083008 | 1.639350e+07 |
|    LLC data read volume [Bytes] STAT   |     87717120 |            0 |     87717120 | 4.873173e+06 |
|      LLC read volume [Bytes] STAT      |    217858816 |            0 |    217858816 | 1.210327e+07 |
|      LLC write volume [Bytes] STAT     |     27587008 |            0 |     27587008 | 1.532612e+06 |
|   DRAM read bandwidth [Bytes/s] STAT   |     29342550 |            0 |     29342550 | 1.630142e+06 |
|   DRAM write bandwidth [Bytes/s] STAT  |      7584458 |            0 |      7584458 |  421358.7778 |
|      DRAM read volume [Bytes] STAT     |     29066688 |            0 |     29066688 |      1614816 |
|     DRAM write volume [Bytes] STAT     |      7513152 |            0 |      7513152 |  417397.3333 |
|           Time: MEM busy STAT          |       0.0006 |            0 |       0.0006 | 3.333333e-05 |
|           Time: L3 busy STAT           |       0.0006 |            0 |       0.0006 | 3.333333e-05 |
|               Ins [] STAT              |     43198827 |            0 |      9953040 | 2.399935e+06 |
|              Cycle [] STAT             |     83577218 |            0 |     12394536 | 4.643179e+06 |
|            Stall_l2M [] STAT           |     33547907 |            0 |      4591096 | 1.863773e+06 |
|            Stall_mem [] STAT           |     58800639 |            0 |      7782826 | 3.266702e+06 |
|           L3_Latency [] STAT           |       7.2763 |            0 |       0.9958 |       0.4042 |
|          DRAM_latency [] STAT          |     102.8774 |            0 |      13.6168 |       5.7154 |
+----------------------------------------+--------------+--------------+--------------+--------------+

* The third take
+----------------------------------------+----------+-----------+-----+-----------+--------------+
|                  Event                 |  Counter |    Sum    | Min |    Max    |      Avg     |
+----------------------------------------+----------+-----------+-----+-----------+--------------+
|         INSTR_RETIRED_ANY STAT         |   FIXC0  |  43648388 |   0 |   6978084 | 2.424910e+06 |
|       CPU_CLK_UNHALTED_CORE STAT       |   FIXC1  |  76757120 |   0 |  10312223 | 4.264284e+06 |
|        CPU_CLK_UNHALTED_REF STAT       |   FIXC2  | 143396812 |   0 |  19645105 | 7.966490e+06 |
|  CYCLE_ACTIVITY_STALLS_L2_PENDING STAT |   PMC0   |  32084348 |   0 |   4030231 | 1.782464e+06 |
| CYCLE_ACTIVITY_STALLS_LDM_PENDING STAT |   PMC1   |  53607427 |   0 |   7184540 | 2.978190e+06 |
|    CYCLE_ACTIVITY_STALLS_TOTAL STAT    |   PMC2   |  56899724 |   0 |   7501065 | 3.161096e+06 |
|           LLC_LOOKUP_ANY STAT          |  CBOX0C0 |    276035 |   0 |    276035 |   15335.2778 |
|           LLC_LOOKUP_ANY STAT          |  CBOX1C0 |    221422 |   0 |    221422 |   12301.2222 |
|           LLC_LOOKUP_ANY STAT          |  CBOX2C0 |    243674 |   0 |    243674 |   13537.4444 |
|           LLC_LOOKUP_ANY STAT          |  CBOX3C0 |    222554 |   0 |    222554 |   12364.1111 |
|           LLC_LOOKUP_ANY STAT          |  CBOX4C0 |    218774 |   0 |    218774 |   12154.1111 |
|           LLC_LOOKUP_ANY STAT          |  CBOX5C0 |    200611 |   0 |    200611 |   11145.0556 |
|           LLC_LOOKUP_ANY STAT          |  CBOX6C0 |    275076 |   0 |    275076 |        15282 |
|           LLC_LOOKUP_ANY STAT          |  CBOX7C0 |    229594 |   0 |    229594 |   12755.2222 |
|           LLC_LOOKUP_ANY STAT          |  CBOX8C0 |    231131 |   0 |    231131 |   12840.6111 |
|           LLC_LOOKUP_ANY STAT          |  CBOX9C0 |    251435 |   0 |    251435 |   13968.6111 |
|           LLC_LOOKUP_ANY STAT          | CBOX10C0 |    223788 |   0 |    223788 |   12432.6667 |
|           LLC_LOOKUP_ANY STAT          | CBOX11C0 |    218411 |   0 |    218411 |   12133.9444 |
|           LLC_LOOKUP_ANY STAT          | CBOX12C0 |    220398 |   0 |    220398 |   12244.3333 |
|           LLC_LOOKUP_ANY STAT          | CBOX13C0 |    224018 |   0 |    224018 |   12445.4444 |
|           LLC_LOOKUP_ANY STAT          | CBOX14C0 |    223246 |   0 |    223246 |   12402.5556 |
|           LLC_LOOKUP_ANY STAT          | CBOX15C0 |    304828 |   0 |    304828 |   16934.8889 |
|           LLC_LOOKUP_ANY STAT          | CBOX16C0 |    257918 |   0 |    257918 |   14328.7778 |
|           LLC_LOOKUP_ANY STAT          | CBOX17C0 |    224346 |   0 |    224346 |   12463.6667 |
|        LLC_LOOKUP_DATA_READ STAT       |  CBOX0C1 |     93227 |   0 |     93227 |    5179.2778 |
|        LLC_LOOKUP_DATA_READ STAT       |  CBOX1C1 |     64677 |   0 |     64677 |    3593.1667 |
|        LLC_LOOKUP_DATA_READ STAT       |  CBOX2C1 |     73264 |   0 |     73264 |    4070.2222 |
|        LLC_LOOKUP_DATA_READ STAT       |  CBOX3C1 |     62583 |   0 |     62583 |    3476.8333 |
|        LLC_LOOKUP_DATA_READ STAT       |  CBOX4C1 |     66478 |   0 |     66478 |    3693.2222 |
|        LLC_LOOKUP_DATA_READ STAT       |  CBOX5C1 |     60081 |   0 |     60081 |    3337.8333 |
|        LLC_LOOKUP_DATA_READ STAT       |  CBOX6C1 |     91186 |   0 |     91186 |    5065.8889 |
|        LLC_LOOKUP_DATA_READ STAT       |  CBOX7C1 |     66464 |   0 |     66464 |    3692.4444 |
|        LLC_LOOKUP_DATA_READ STAT       |  CBOX8C1 |     66959 |   0 |     66959 |    3719.9444 |
|        LLC_LOOKUP_DATA_READ STAT       |  CBOX9C1 |     80739 |   0 |     80739 |    4485.5000 |
|        LLC_LOOKUP_DATA_READ STAT       | CBOX10C1 |     66411 |   0 |     66411 |    3689.5000 |
|        LLC_LOOKUP_DATA_READ STAT       | CBOX11C1 |     62038 |   0 |     62038 |    3446.5556 |
|        LLC_LOOKUP_DATA_READ STAT       | CBOX12C1 |     66869 |   0 |     66869 |    3714.9444 |
|        LLC_LOOKUP_DATA_READ STAT       | CBOX13C1 |     65354 |   0 |     65354 |    3630.7778 |
|        LLC_LOOKUP_DATA_READ STAT       | CBOX14C1 |     64347 |   0 |     64347 |    3574.8333 |
|        LLC_LOOKUP_DATA_READ STAT       | CBOX15C1 |    108019 |   0 |    108019 |    6001.0556 |
|        LLC_LOOKUP_DATA_READ STAT       | CBOX16C1 |     75156 |   0 |     75156 |    4175.3333 |
|        LLC_LOOKUP_DATA_READ STAT       | CBOX17C1 |     58858 |   0 |     58858 |    3269.8889 |
|          LLC_LOOKUP_READ STAT          |  CBOX0C2 |    206564 |   0 |    206564 |   11475.7778 |
|          LLC_LOOKUP_READ STAT          |  CBOX1C2 |    158979 |   0 |    158979 |    8832.1667 |
|          LLC_LOOKUP_READ STAT          |  CBOX2C2 |    178684 |   0 |    178684 |    9926.8889 |
|          LLC_LOOKUP_READ STAT          |  CBOX3C2 |    161984 |   0 |    161984 |    8999.1111 |
|          LLC_LOOKUP_READ STAT          |  CBOX4C2 |    159648 |   0 |    159648 |    8869.3333 |
|          LLC_LOOKUP_READ STAT          |  CBOX5C2 |    146819 |   0 |    146819 |    8156.6111 |
|          LLC_LOOKUP_READ STAT          |  CBOX6C2 |    202521 |   0 |    202521 |   11251.1667 |
|          LLC_LOOKUP_READ STAT          |  CBOX7C2 |    168836 |   0 |    168836 |    9379.7778 |
|          LLC_LOOKUP_READ STAT          |  CBOX8C2 |    165609 |   0 |    165609 |    9200.5000 |
|          LLC_LOOKUP_READ STAT          |  CBOX9C2 |    183455 |   0 |    183455 |   10191.9444 |
|          LLC_LOOKUP_READ STAT          | CBOX10C2 |    161769 |   0 |    161769 |    8987.1667 |
|          LLC_LOOKUP_READ STAT          | CBOX11C2 |    160478 |   0 |    160478 |    8915.4444 |
|          LLC_LOOKUP_READ STAT          | CBOX12C2 |    161484 |   0 |    161484 |    8971.3333 |
|          LLC_LOOKUP_READ STAT          | CBOX13C2 |    159973 |   0 |    159973 |    8887.3889 |
|          LLC_LOOKUP_READ STAT          | CBOX14C2 |    164810 |   0 |    164810 |    9156.1111 |
|          LLC_LOOKUP_READ STAT          | CBOX15C2 |    230806 |   0 |    230806 |   12822.5556 |
|          LLC_LOOKUP_READ STAT          | CBOX16C2 |    182651 |   0 |    182651 |   10147.2778 |
|          LLC_LOOKUP_READ STAT          | CBOX17C2 |    157861 |   0 |    157861 |    8770.0556 |
|          LLC_LOOKUP_WRITE STAT         |  CBOX0C3 |     27177 |   0 |     27177 |    1509.8333 |
|          LLC_LOOKUP_WRITE STAT         |  CBOX1C3 |     17673 |   0 |     17673 |     981.8333 |
|          LLC_LOOKUP_WRITE STAT         |  CBOX2C3 |     25191 |   0 |     25191 |    1399.5000 |
|          LLC_LOOKUP_WRITE STAT         |  CBOX3C3 |     18582 |   0 |     18582 |    1032.3333 |
|          LLC_LOOKUP_WRITE STAT         |  CBOX4C3 |     19161 |   0 |     19161 |    1064.5000 |
|          LLC_LOOKUP_WRITE STAT         |  CBOX5C3 |     16701 |   0 |     16701 |     927.8333 |
|          LLC_LOOKUP_WRITE STAT         |  CBOX6C3 |     23512 |   0 |     23512 |    1306.2222 |
|          LLC_LOOKUP_WRITE STAT         |  CBOX7C3 |     17897 |   0 |     17897 |     994.2778 |
|          LLC_LOOKUP_WRITE STAT         |  CBOX8C3 |     19110 |   0 |     19110 |    1061.6667 |
|          LLC_LOOKUP_WRITE STAT         |  CBOX9C3 |     28282 |   0 |     28282 |    1571.2222 |
|          LLC_LOOKUP_WRITE STAT         | CBOX10C3 |     19281 |   0 |     19281 |    1071.1667 |
|          LLC_LOOKUP_WRITE STAT         | CBOX11C3 |     17284 |   0 |     17284 |     960.2222 |
|          LLC_LOOKUP_WRITE STAT         | CBOX12C3 |     19523 |   0 |     19523 |    1084.6111 |
|          LLC_LOOKUP_WRITE STAT         | CBOX13C3 |     17859 |   0 |     17859 |     992.1667 |
|          LLC_LOOKUP_WRITE STAT         | CBOX14C3 |     17552 |   0 |     17552 |     975.1111 |
|          LLC_LOOKUP_WRITE STAT         | CBOX15C3 |     27854 |   0 |     27854 |    1547.4444 |
|          LLC_LOOKUP_WRITE STAT         | CBOX16C3 |     34629 |   0 |     34629 |    1923.8333 |
|          LLC_LOOKUP_WRITE STAT         | CBOX17C3 |     26581 |   0 |     26581 |    1476.7222 |
|            CAS_COUNT_RD STAT           |  MBOX0C0 |    113159 |   0 |    113159 |    6286.6111 |
|            CAS_COUNT_WR STAT           |  MBOX0C1 |     22051 |   0 |     22051 |    1225.0556 |
|            CAS_COUNT_RD STAT           |  MBOX1C0 |    121807 |   0 |    121807 |    6767.0556 |
|            CAS_COUNT_WR STAT           |  MBOX1C1 |     24275 |   0 |     24275 |    1348.6111 |
|            CAS_COUNT_RD STAT           |  MBOX4C0 |     91726 |   0 |     91726 |    5095.8889 |
|            CAS_COUNT_WR STAT           |  MBOX4C1 |     12425 |   0 |     12425 |     690.2778 |
|            CAS_COUNT_RD STAT           |  MBOX5C0 |    119804 |   0 |    119804 |    6655.7778 |
|            CAS_COUNT_WR STAT           |  MBOX5C1 |     28371 |   0 |     28371 |    1576.1667 |
|            UNCORE_CLOCK STAT           |  UBOXFIX | 640514924 |   0 | 640514924 | 3.558416e+07 |
|           PWR_PKG_ENERGY STAT          |   PWR0   |   15.2393 |   0 |   15.2393 |       0.8466 |
|          PWR_DRAM_ENERGY STAT          |   PWR3   |    2.2231 |   0 |    2.2231 |       0.1235 |
+----------------------------------------+----------+-----------+-----+-----------+--------------+

+----------------------------------------+--------------+--------------+--------------+--------------+
|                 Metric                 |      Sum     |      Min     |      Max     |      Avg     |
+----------------------------------------+--------------+--------------+--------------+--------------+
|     Time: Runtime (RDTSC) [s] STAT     |      17.8578 |       0.9921 |       0.9921 |       0.9921 |
|     Time: Runtime unhalted [s] STAT    |       0.0627 |            0 |       0.0086 |       0.0035 |
|            inverseClock STAT           | 7.844238e-09 | 4.357910e-10 | 4.357910e-10 | 4.357910e-10 |
|            Clock [MHz] STAT            |   21691.1543 |    1197.0720 |    1943.0443 |    1205.0641 |
|         Uncore Clock [MHz] STAT        |     645.6443 |            0 |     645.6443 |      35.8691 |
|       Time: Core total stall STAT      |       0.0464 | 1.651947e-05 |       0.0063 |       0.0026 |
|        Time: Core l2 stall STAT        |       0.0263 | 9.333608e-06 |       0.0034 |       0.0015 |
|        Time: Core ldm stall STAT       |       0.0438 | 8.927617e-06 |       0.0060 |       0.0024 |
|                CPI STAT                |      39.7990 |       1.1907 |      10.4039 |       2.2111 |
|           Power PKG [W] STAT           |      15.3613 |            0 |      15.3613 |       0.8534 |
|           Power DRAM [W] STAT          |       2.2409 |            0 |       2.2409 |       0.1245 |
|           Energy PKG [J] STAT          |      15.2393 |            0 |      15.2393 |       0.8466 |
|          Energy DRAM [J] STAT          |       2.2231 |            0 |       2.2231 |       0.1235 |
|           L2M Pending[%] STAT          |     660.3110 |      19.4737 |      53.7049 |      36.6839 |
|           LD Pending[%] STAT           |    1033.7805 |      27.7101 |      78.6166 |      57.4323 |
|    LLC Any bandwidth [Bytes/s] STAT    |    275291600 |            0 |    275291600 | 1.529398e+07 |
| LLC data read bandwidth [Bytes/s] STAT |     83395980 |            0 |     83395980 |      4633110 |
|    LLC read bandwidth [Bytes/s] STAT   |    200823000 |            0 |    200823000 | 1.115683e+07 |
|   LLC write bandwidth [Bytes/s] STAT   |     25408190 |            0 |     25408190 | 1.411566e+06 |
|       LLC Any volume [Bytes] STAT      |    273104576 |            0 |    273104576 | 1.517248e+07 |
|    LLC data read volume [Bytes] STAT   |     82733440 |            0 |     82733440 | 4.596302e+06 |
|      LLC read volume [Bytes] STAT      |    199227584 |            0 |    199227584 | 1.106820e+07 |
|      LLC write volume [Bytes] STAT     |     25206336 |            0 |     25206336 |      1400352 |
|   DRAM read bandwidth [Bytes/s] STAT   |     28804580 |            0 |     28804580 | 1.600254e+06 |
|   DRAM write bandwidth [Bytes/s] STAT  |      5620460 |            0 |      5620460 |  312247.7778 |
|      DRAM read volume [Bytes] STAT     |     28575744 |            0 |     28575744 | 1.587541e+06 |
|     DRAM write volume [Bytes] STAT     |      5575808 |            0 |      5575808 |  309767.1111 |
|           Time: MEM busy STAT          |       0.0006 |            0 |       0.0006 | 3.333333e-05 |
|           Time: L3 busy STAT           |       0.0006 |            0 |       0.0006 | 3.333333e-05 |
|               Ins [] STAT              |     43648388 |            0 |      6978084 | 2.424910e+06 |
|              Cycle [] STAT             |     76757120 |            0 |     10312223 | 4.264284e+06 |
|            Stall_l2M [] STAT           |     32084348 |            0 |      4030231 | 1.782464e+06 |
|            Stall_mem [] STAT           |     53607427 |            0 |      7184540 | 2.978190e+06 |
|           L3_Latency [] STAT           |       7.5189 |            0 |       0.9445 |       0.4177 |
|          DRAM_latency [] STAT          |     100.4605 |            0 |      13.4638 |       5.5811 |
+----------------------------------------+--------------+--------------+--------------+--------------+


* The fourth take
+----------------------------------------+----------+-----------+-------+-----------+--------------+
|                  Event                 |  Counter |    Sum    |  Min  |    Max    |      Avg     |
+----------------------------------------+----------+-----------+-------+-----------+--------------+
|         INSTR_RETIRED_ANY STAT         |   FIXC0  |  55891389 |   272 |   7502343 | 3.105077e+06 |
|       CPU_CLK_UNHALTED_CORE STAT       |   FIXC1  |  93791522 |  8356 |   9632741 | 5.210640e+06 |
|        CPU_CLK_UNHALTED_REF STAT       |   FIXC2  | 179362119 | 16031 |  18462721 | 9.964562e+06 |
|  CYCLE_ACTIVITY_STALLS_L2_PENDING STAT |   PMC0   |  40066161 |  3427 |   3988391 | 2.225898e+06 |
| CYCLE_ACTIVITY_STALLS_LDM_PENDING STAT |   PMC1   |  64410123 |  3173 |   6736900 | 3.578340e+06 |
|    CYCLE_ACTIVITY_STALLS_TOTAL STAT    |   PMC2   |  68461258 |  7240 |   7069600 | 3.803403e+06 |
|           LLC_LOOKUP_ANY STAT          |  CBOX0C0 |    239885 |     0 |    239885 |   13326.9444 |
|           LLC_LOOKUP_ANY STAT          |  CBOX1C0 |    250338 |     0 |    250338 |   13907.6667 |
|           LLC_LOOKUP_ANY STAT          |  CBOX2C0 |    288603 |     0 |    288603 |   16033.5000 |
|           LLC_LOOKUP_ANY STAT          |  CBOX3C0 |    284729 |     0 |    284729 |   15818.2778 |
|           LLC_LOOKUP_ANY STAT          |  CBOX4C0 |    234432 |     0 |    234432 |        13024 |
|           LLC_LOOKUP_ANY STAT          |  CBOX5C0 |    233498 |     0 |    233498 |   12972.1111 |
|           LLC_LOOKUP_ANY STAT          |  CBOX6C0 |    296270 |     0 |    296270 |   16459.4444 |
|           LLC_LOOKUP_ANY STAT          |  CBOX7C0 |    287340 |     0 |    287340 |   15963.3333 |
|           LLC_LOOKUP_ANY STAT          |  CBOX8C0 |    256020 |     0 |    256020 |   14223.3333 |
|           LLC_LOOKUP_ANY STAT          |  CBOX9C0 |    253044 |     0 |    253044 |        14058 |
|           LLC_LOOKUP_ANY STAT          | CBOX10C0 |    244390 |     0 |    244390 |   13577.2222 |
|           LLC_LOOKUP_ANY STAT          | CBOX11C0 |    235979 |     0 |    235979 |   13109.9444 |
|           LLC_LOOKUP_ANY STAT          | CBOX12C0 |    284690 |     0 |    284690 |   15816.1111 |
|           LLC_LOOKUP_ANY STAT          | CBOX13C0 |    244437 |     0 |    244437 |   13579.8333 |
|           LLC_LOOKUP_ANY STAT          | CBOX14C0 |    318920 |     0 |    318920 |   17717.7778 |
|           LLC_LOOKUP_ANY STAT          | CBOX15C0 |    282303 |     0 |    282303 |   15683.5000 |
|           LLC_LOOKUP_ANY STAT          | CBOX16C0 |    249230 |     0 |    249230 |   13846.1111 |
|           LLC_LOOKUP_ANY STAT          | CBOX17C0 |    240598 |     0 |    240598 |   13366.5556 |
|        LLC_LOOKUP_DATA_READ STAT       |  CBOX0C1 |     67855 |     0 |     67855 |    3769.7222 |
|        LLC_LOOKUP_DATA_READ STAT       |  CBOX1C1 |     73194 |     0 |     73194 |    4066.3333 |
|        LLC_LOOKUP_DATA_READ STAT       |  CBOX2C1 |     90391 |     0 |     90391 |    5021.7222 |
|        LLC_LOOKUP_DATA_READ STAT       |  CBOX3C1 |     87265 |     0 |     87265 |    4848.0556 |
|        LLC_LOOKUP_DATA_READ STAT       |  CBOX4C1 |     68218 |     0 |     68218 |    3789.8889 |
|        LLC_LOOKUP_DATA_READ STAT       |  CBOX5C1 |     70883 |     0 |     70883 |    3937.9444 |
|        LLC_LOOKUP_DATA_READ STAT       |  CBOX6C1 |     94241 |     0 |     94241 |    5235.6111 |
|        LLC_LOOKUP_DATA_READ STAT       |  CBOX7C1 |     86511 |     0 |     86511 |    4806.1667 |
|        LLC_LOOKUP_DATA_READ STAT       |  CBOX8C1 |     73557 |     0 |     73557 |    4086.5000 |
|        LLC_LOOKUP_DATA_READ STAT       |  CBOX9C1 |     73803 |     0 |     73803 |    4100.1667 |
|        LLC_LOOKUP_DATA_READ STAT       | CBOX10C1 |     71345 |     0 |     71345 |    3963.6111 |
|        LLC_LOOKUP_DATA_READ STAT       | CBOX11C1 |     65755 |     0 |     65755 |    3653.0556 |
|        LLC_LOOKUP_DATA_READ STAT       | CBOX12C1 |     91951 |     0 |     91951 |    5108.3889 |
|        LLC_LOOKUP_DATA_READ STAT       | CBOX13C1 |     70039 |     0 |     70039 |    3891.0556 |
|        LLC_LOOKUP_DATA_READ STAT       | CBOX14C1 |    103592 |     0 |    103592 |    5755.1111 |
|        LLC_LOOKUP_DATA_READ STAT       | CBOX15C1 |     88332 |     0 |     88332 |    4907.3333 |
|        LLC_LOOKUP_DATA_READ STAT       | CBOX16C1 |     65192 |     0 |     65192 |    3621.7778 |
|        LLC_LOOKUP_DATA_READ STAT       | CBOX17C1 |     61246 |     0 |     61246 |    3402.5556 |
|          LLC_LOOKUP_READ STAT          |  CBOX0C2 |    179888 |     0 |    179888 |    9993.7778 |
|          LLC_LOOKUP_READ STAT          |  CBOX1C2 |    182584 |     0 |    182584 |   10143.5556 |
|          LLC_LOOKUP_READ STAT          |  CBOX2C2 |    213113 |     0 |    213113 |   11839.6111 |
|          LLC_LOOKUP_READ STAT          |  CBOX3C2 |    207840 |     0 |    207840 |   11546.6667 |
|          LLC_LOOKUP_READ STAT          |  CBOX4C2 |    172055 |     0 |    172055 |    9558.6111 |
|          LLC_LOOKUP_READ STAT          |  CBOX5C2 |    173440 |     0 |    173440 |    9635.5556 |
|          LLC_LOOKUP_READ STAT          |  CBOX6C2 |    218361 |     0 |    218361 |   12131.1667 |
|          LLC_LOOKUP_READ STAT          |  CBOX7C2 |    214707 |     0 |    214707 |   11928.1667 |
|          LLC_LOOKUP_READ STAT          |  CBOX8C2 |    185155 |     0 |    185155 |   10286.3889 |
|          LLC_LOOKUP_READ STAT          |  CBOX9C2 |    187446 |     0 |    187446 |   10413.6667 |
|          LLC_LOOKUP_READ STAT          | CBOX10C2 |    178917 |     0 |    178917 |    9939.8333 |
|          LLC_LOOKUP_READ STAT          | CBOX11C2 |    176423 |     0 |    176423 |    9801.2778 |
|          LLC_LOOKUP_READ STAT          | CBOX12C2 |    210679 |     0 |    210679 |   11704.3889 |
|          LLC_LOOKUP_READ STAT          | CBOX13C2 |    177422 |     0 |    177422 |    9856.7778 |
|          LLC_LOOKUP_READ STAT          | CBOX14C2 |    238370 |     0 |    238370 |   13242.7778 |
|          LLC_LOOKUP_READ STAT          | CBOX15C2 |    213438 |     0 |    213438 |   11857.6667 |
|          LLC_LOOKUP_READ STAT          | CBOX16C2 |    172070 |     0 |    172070 |    9559.4444 |
|          LLC_LOOKUP_READ STAT          | CBOX17C2 |    166658 |     0 |    166658 |    9258.7778 |
|          LLC_LOOKUP_WRITE STAT         |  CBOX0C3 |     13034 |     0 |     13034 |     724.1111 |
|          LLC_LOOKUP_WRITE STAT         |  CBOX1C3 |     19632 |     0 |     19632 |    1090.6667 |
|          LLC_LOOKUP_WRITE STAT         |  CBOX2C3 |     31483 |     0 |     31483 |    1749.0556 |
|          LLC_LOOKUP_WRITE STAT         |  CBOX3C3 |     30940 |     0 |     30940 |    1718.8889 |
|          LLC_LOOKUP_WRITE STAT         |  CBOX4C3 |     20431 |     0 |     20431 |    1135.0556 |
|          LLC_LOOKUP_WRITE STAT         |  CBOX5C3 |     19304 |     0 |     19304 |    1072.4444 |
|          LLC_LOOKUP_WRITE STAT         |  CBOX6C3 |     23581 |     0 |     23581 |    1310.0556 |
|          LLC_LOOKUP_WRITE STAT         |  CBOX7C3 |     23069 |     0 |     23069 |    1281.6111 |
|          LLC_LOOKUP_WRITE STAT         |  CBOX8C3 |     19644 |     0 |     19644 |    1091.3333 |
|          LLC_LOOKUP_WRITE STAT         |  CBOX9C3 |     21773 |     0 |     21773 |    1209.6111 |
|          LLC_LOOKUP_WRITE STAT         | CBOX10C3 |     20726 |     0 |     20726 |    1151.4444 |
|          LLC_LOOKUP_WRITE STAT         | CBOX11C3 |     17962 |     0 |     17962 |     997.8889 |
|          LLC_LOOKUP_WRITE STAT         | CBOX12C3 |     29234 |     0 |     29234 |    1624.1111 |
|          LLC_LOOKUP_WRITE STAT         | CBOX13C3 |     18789 |     0 |     18789 |    1043.8333 |
|          LLC_LOOKUP_WRITE STAT         | CBOX14C3 |     35891 |     0 |     35891 |    1993.9444 |
|          LLC_LOOKUP_WRITE STAT         | CBOX15C3 |     17509 |     0 |     17509 |     972.7222 |
|          LLC_LOOKUP_WRITE STAT         | CBOX16C3 |     34308 |     0 |     34308 |         1906 |
|          LLC_LOOKUP_WRITE STAT         | CBOX17C3 |     31081 |     0 |     31081 |    1726.7222 |
|            CAS_COUNT_RD STAT           |  MBOX0C0 |    126514 |     0 |    126514 |    7028.5556 |
|            CAS_COUNT_WR STAT           |  MBOX0C1 |     35229 |     0 |     35229 |    1957.1667 |
|            CAS_COUNT_RD STAT           |  MBOX1C0 |    115397 |     0 |    115397 |    6410.9444 |
|            CAS_COUNT_WR STAT           |  MBOX1C1 |     21239 |     0 |     21239 |    1179.9444 |
|            CAS_COUNT_RD STAT           |  MBOX4C0 |    107364 |     0 |    107364 |    5964.6667 |
|            CAS_COUNT_WR STAT           |  MBOX4C1 |     26512 |     0 |     26512 |    1472.8889 |
|            CAS_COUNT_RD STAT           |  MBOX5C0 |    120834 |     0 |    120834 |         6713 |
|            CAS_COUNT_WR STAT           |  MBOX5C1 |     26747 |     0 |     26747 |    1485.9444 |
|            UNCORE_CLOCK STAT           |  UBOXFIX | 542755642 |     0 | 542755642 | 3.015309e+07 |
|           PWR_PKG_ENERGY STAT          |   PWR0   |   13.9830 |     0 |   13.9830 |       0.7768 |
|          PWR_DRAM_ENERGY STAT          |   PWR3   |    1.8250 |     0 |    1.8250 |       0.1014 |
+----------------------------------------+----------+-----------+-------+-----------+--------------+
+----------------------------------------+--------------+--------------+--------------+--------------+
|                 Metric                 |      Sum     |      Min     |      Max     |      Avg     |
+----------------------------------------+--------------+--------------+--------------+--------------+
|     Time: Runtime (RDTSC) [s] STAT     |      17.8848 |       0.9936 |       0.9936 |       0.9936 |
|     Time: Runtime unhalted [s] STAT    |       0.0782 | 6.986219e-06 |       0.0080 |       0.0043 |
|            inverseClock STAT           | 7.844297e-09 | 4.357943e-10 | 4.357943e-10 | 4.357943e-10 |
|            Clock [MHz] STAT            |   22009.7926 |    1196.0691 |    1637.7926 |    1222.7663 |
|         Uncore Clock [MHz] STAT        |     546.2578 |            0 |     546.2578 |      30.3477 |
|       Time: Core total stall STAT      |       0.0571 | 6.053162e-06 |       0.0059 |       0.0032 |
|        Time: Core l2 stall STAT        |       0.0334 | 2.865219e-06 |       0.0033 |       0.0019 |
|        Time: Core ldm stall STAT       |       0.0537 | 2.652857e-06 |       0.0056 |       0.0030 |
|                CPI STAT                |      66.3575 |       1.2381 |      30.7206 |       3.6865 |
|           Power PKG [W] STAT           |      14.0733 |            0 |      14.0733 |       0.7818 |
|           Power DRAM [W] STAT          |       1.8368 |            0 |       1.8368 |       0.1020 |
|           Energy PKG [J] STAT          |      13.9830 |            0 |      13.9830 |       0.7768 |
|          Energy DRAM [J] STAT          |       1.8250 |            0 |       1.8250 |       0.1014 |
|           L2M Pending[%] STAT          |     711.1608 |      10.8882 |      48.1544 |      39.5089 |
|           LD Pending[%] STAT           |    1121.1086 |      28.3927 |      75.6539 |      62.2838 |
|    LLC Any bandwidth [Bytes/s] STAT    |    304332300 |            0 |    304332300 |     16907350 |
| LLC data read bandwidth [Bytes/s] STAT |     90395220 |            0 |     90395220 | 5.021957e+06 |
|    LLC read bandwidth [Bytes/s] STAT   |    223420600 |            0 |    223420600 | 1.241226e+07 |
|   LLC write bandwidth [Bytes/s] STAT   |     27593930 |            0 |     27593930 | 1.532996e+06 |
|       LLC Any volume [Bytes] STAT      |    302381184 |            0 |    302381184 | 1.679895e+07 |
|    LLC data read volume [Bytes] STAT   |     89815680 |            0 |     89815680 |      4989760 |
|      LLC read volume [Bytes] STAT      |    221988224 |            0 |    221988224 | 1.233268e+07 |
|      LLC write volume [Bytes] STAT     |     27417024 |            0 |     27417024 |      1523168 |
|   DRAM read bandwidth [Bytes/s] STAT   |     30281110 |            0 |     30281110 | 1.682284e+06 |
|   DRAM write bandwidth [Bytes/s] STAT  |      7067842 |            0 |      7067842 |  392657.8889 |
|      DRAM read volume [Bytes] STAT     |     30086976 |            0 |     30086976 | 1.671499e+06 |
|     DRAM write volume [Bytes] STAT     |      7022528 |            0 |      7022528 |  390140.4444 |
|           Time: MEM busy STAT          |       0.0006 |            0 |       0.0006 | 3.333333e-05 |
|           Time: L3 busy STAT           |       0.0006 |            0 |       0.0006 | 3.333333e-05 |
|               Ins [] STAT              |     55891389 |          272 |      7502343 | 3.105077e+06 |
|              Cycle [] STAT             |     93791522 |         8356 |      9632741 | 5.210640e+06 |
|            Stall_l2M [] STAT           |     40066161 |         3427 |      3988391 | 2.225898e+06 |
|            Stall_mem [] STAT           |     64410123 |         3173 |      6736900 | 3.578340e+06 |
|           L3_Latency [] STAT           |       8.4801 |       0.0007 |       0.8442 |       0.4711 |
|          DRAM_latency [] STAT          |     111.0832 |       0.0055 |      11.6186 |       6.1713 |
+----------------------------------------+--------------+--------------+--------------+--------------+


* The fifth take
+----------------------------------------+----------+-----------+-------+-----------+--------------+
|                  Event                 |  Counter |    Sum    |  Min  |    Max    |      Avg     |
+----------------------------------------+----------+-----------+-------+-----------+--------------+
|         INSTR_RETIRED_ANY STAT         |   FIXC0  |  43076772 |  1743 |   5737867 |      2393154 |
|       CPU_CLK_UNHALTED_CORE STAT       |   FIXC1  |  94613446 | 13020 |  11385668 | 5.256303e+06 |
|        CPU_CLK_UNHALTED_REF STAT       |   FIXC2  | 178842641 | 24955 |  21822400 | 9.935702e+06 |
|  CYCLE_ACTIVITY_STALLS_L2_PENDING STAT |   PMC0   |  41478628 |  4211 |   4871467 | 2.304368e+06 |
| CYCLE_ACTIVITY_STALLS_LDM_PENDING STAT |   PMC1   |  70652065 |  4375 |   7778690 | 3.925115e+06 |
|    CYCLE_ACTIVITY_STALLS_TOTAL STAT    |   PMC2   |  74397608 | 10977 |   8371765 | 4.133200e+06 |
|           LLC_LOOKUP_ANY STAT          |  CBOX0C0 |    246147 |     0 |    246147 |   13674.8333 |
|           LLC_LOOKUP_ANY STAT          |  CBOX1C0 |    204480 |     0 |    204480 |        11360 |
|           LLC_LOOKUP_ANY STAT          |  CBOX2C0 |    228753 |     0 |    228753 |   12708.5000 |
|           LLC_LOOKUP_ANY STAT          |  CBOX3C0 |    205346 |     0 |    205346 |   11408.1111 |
|           LLC_LOOKUP_ANY STAT          |  CBOX4C0 |    200751 |     0 |    200751 |   11152.8333 |
|           LLC_LOOKUP_ANY STAT          |  CBOX5C0 |    190093 |     0 |    190093 |   10560.7222 |
|           LLC_LOOKUP_ANY STAT          |  CBOX6C0 |    260877 |     0 |    260877 |   14493.1667 |
|           LLC_LOOKUP_ANY STAT          |  CBOX7C0 |    230964 |     0 |    230964 |   12831.3333 |
|           LLC_LOOKUP_ANY STAT          |  CBOX8C0 |    219590 |     0 |    219590 |   12199.4444 |
|           LLC_LOOKUP_ANY STAT          |  CBOX9C0 |    207938 |     0 |    207938 |   11552.1111 |
|           LLC_LOOKUP_ANY STAT          | CBOX10C0 |    206983 |     0 |    206983 |   11499.0556 |
|           LLC_LOOKUP_ANY STAT          | CBOX11C0 |    196417 |     0 |    196417 |   10912.0556 |
|           LLC_LOOKUP_ANY STAT          | CBOX12C0 |    198675 |     0 |    198675 |   11037.5000 |
|           LLC_LOOKUP_ANY STAT          | CBOX13C0 |    204747 |     0 |    204747 |   11374.8333 |
|           LLC_LOOKUP_ANY STAT          | CBOX14C0 |    215021 |     0 |    215021 |   11945.6111 |
|           LLC_LOOKUP_ANY STAT          | CBOX15C0 |    286019 |     0 |    286019 |   15889.9444 |
|           LLC_LOOKUP_ANY STAT          | CBOX16C0 |    217092 |     0 |    217092 |   12060.6667 |
|           LLC_LOOKUP_ANY STAT          | CBOX17C0 |    211637 |     0 |    211637 |   11757.6111 |
|        LLC_LOOKUP_DATA_READ STAT       |  CBOX0C1 |     78490 |     0 |     78490 |    4360.5556 |
|        LLC_LOOKUP_DATA_READ STAT       |  CBOX1C1 |     57711 |     0 |     57711 |    3206.1667 |
|        LLC_LOOKUP_DATA_READ STAT       |  CBOX2C1 |     66072 |     0 |     66072 |    3670.6667 |
|        LLC_LOOKUP_DATA_READ STAT       |  CBOX3C1 |     54262 |     0 |     54262 |    3014.5556 |
|        LLC_LOOKUP_DATA_READ STAT       |  CBOX4C1 |     57955 |     0 |     57955 |    3219.7222 |
|        LLC_LOOKUP_DATA_READ STAT       |  CBOX5C1 |     55122 |     0 |     55122 |    3062.3333 |
|        LLC_LOOKUP_DATA_READ STAT       |  CBOX6C1 |     83138 |     0 |     83138 |    4618.7778 |
|        LLC_LOOKUP_DATA_READ STAT       |  CBOX7C1 |     68078 |     0 |     68078 |    3782.1111 |
|        LLC_LOOKUP_DATA_READ STAT       |  CBOX8C1 |     62408 |     0 |     62408 |    3467.1111 |
|        LLC_LOOKUP_DATA_READ STAT       |  CBOX9C1 |     61941 |     0 |     61941 |    3441.1667 |
|        LLC_LOOKUP_DATA_READ STAT       | CBOX10C1 |     60039 |     0 |     60039 |    3335.5000 |
|        LLC_LOOKUP_DATA_READ STAT       | CBOX11C1 |     52373 |     0 |     52373 |    2909.6111 |
|        LLC_LOOKUP_DATA_READ STAT       | CBOX12C1 |     56520 |     0 |     56520 |         3140 |
|        LLC_LOOKUP_DATA_READ STAT       | CBOX13C1 |     57814 |     0 |     57814 |    3211.8889 |
|        LLC_LOOKUP_DATA_READ STAT       | CBOX14C1 |     60531 |     0 |     60531 |    3362.8333 |
|        LLC_LOOKUP_DATA_READ STAT       | CBOX15C1 |     97981 |     0 |     97981 |    5443.3889 |
|        LLC_LOOKUP_DATA_READ STAT       | CBOX16C1 |     56272 |     0 |     56272 |    3126.2222 |
|        LLC_LOOKUP_DATA_READ STAT       | CBOX17C1 |     55527 |     0 |     55527 |    3084.8333 |
|          LLC_LOOKUP_READ STAT          |  CBOX0C2 |    179184 |     0 |    179184 |    9954.6667 |
|          LLC_LOOKUP_READ STAT          |  CBOX1C2 |    143597 |     0 |    143597 |    7977.6111 |
|          LLC_LOOKUP_READ STAT          |  CBOX2C2 |    161585 |     0 |    161585 |    8976.9444 |
|          LLC_LOOKUP_READ STAT          |  CBOX3C2 |    142557 |     0 |    142557 |    7919.8333 |
|          LLC_LOOKUP_READ STAT          |  CBOX4C2 |    143313 |     0 |    143313 |    7961.8333 |
|          LLC_LOOKUP_READ STAT          |  CBOX5C2 |    136555 |     0 |    136555 |    7586.3889 |
|          LLC_LOOKUP_READ STAT          |  CBOX6C2 |    188299 |     0 |    188299 |   10461.0556 |
|          LLC_LOOKUP_READ STAT          |  CBOX7C2 |    167516 |     0 |    167516 |    9306.4444 |
|          LLC_LOOKUP_READ STAT          |  CBOX8C2 |    152624 |     0 |    152624 |    8479.1111 |
|          LLC_LOOKUP_READ STAT          |  CBOX9C2 |    150028 |     0 |    150028 |    8334.8889 |
|          LLC_LOOKUP_READ STAT          | CBOX10C2 |    146273 |     0 |    146273 |    8126.2778 |
|          LLC_LOOKUP_READ STAT          | CBOX11C2 |    139764 |     0 |    139764 |    7764.6667 |
|          LLC_LOOKUP_READ STAT          | CBOX12C2 |    140581 |     0 |    140581 |    7810.0556 |
|          LLC_LOOKUP_READ STAT          | CBOX13C2 |    143550 |     0 |    143550 |         7975 |
|          LLC_LOOKUP_READ STAT          | CBOX14C2 |    154446 |     0 |    154446 |    8580.3333 |
|          LLC_LOOKUP_READ STAT          | CBOX15C2 |    212237 |     0 |    212237 |   11790.9444 |
|          LLC_LOOKUP_READ STAT          | CBOX16C2 |    144880 |     0 |    144880 |    8048.8889 |
|          LLC_LOOKUP_READ STAT          | CBOX17C2 |    145636 |     0 |    145636 |    8090.8889 |
|          LLC_LOOKUP_WRITE STAT         |  CBOX0C3 |     21787 |     0 |     21787 |    1210.3889 |
|          LLC_LOOKUP_WRITE STAT         |  CBOX1C3 |     15086 |     0 |     15086 |     838.1111 |
|          LLC_LOOKUP_WRITE STAT         |  CBOX2C3 |     24123 |     0 |     24123 |    1340.1667 |
|          LLC_LOOKUP_WRITE STAT         |  CBOX3C3 |     16762 |     0 |     16762 |     931.2222 |
|          LLC_LOOKUP_WRITE STAT         |  CBOX4C3 |     15877 |     0 |     15877 |     882.0556 |
|          LLC_LOOKUP_WRITE STAT         |  CBOX5C3 |     14590 |     0 |     14590 |     810.5556 |
|          LLC_LOOKUP_WRITE STAT         |  CBOX6C3 |     21405 |     0 |     21405 |    1189.1667 |
|          LLC_LOOKUP_WRITE STAT         |  CBOX7C3 |     18502 |     0 |     18502 |    1027.8889 |
|          LLC_LOOKUP_WRITE STAT         |  CBOX8C3 |     17231 |     0 |     17231 |     957.2778 |
|          LLC_LOOKUP_WRITE STAT         |  CBOX9C3 |     18470 |     0 |     18470 |    1026.1111 |
|          LLC_LOOKUP_WRITE STAT         | CBOX10C3 |     18325 |     0 |     18325 |    1018.0556 |
|          LLC_LOOKUP_WRITE STAT         | CBOX11C3 |     15264 |     0 |     15264 |          848 |
|          LLC_LOOKUP_WRITE STAT         | CBOX12C3 |     16091 |     0 |     16091 |     893.9444 |
|          LLC_LOOKUP_WRITE STAT         | CBOX13C3 |     15338 |     0 |     15338 |     852.1111 |
|          LLC_LOOKUP_WRITE STAT         | CBOX14C3 |     16081 |     0 |     16081 |     893.3889 |
|          LLC_LOOKUP_WRITE STAT         | CBOX15C3 |     25069 |     0 |     25069 |    1392.7222 |
|          LLC_LOOKUP_WRITE STAT         | CBOX16C3 |     26859 |     0 |     26859 |    1492.1667 |
|          LLC_LOOKUP_WRITE STAT         | CBOX17C3 |     25411 |     0 |     25411 |    1411.7222 |
|            CAS_COUNT_RD STAT           |  MBOX0C0 |    133144 |     0 |    133144 |    7396.8889 |
|            CAS_COUNT_WR STAT           |  MBOX0C1 |     38335 |     0 |     38335 |    2129.7222 |
|            CAS_COUNT_RD STAT           |  MBOX1C0 |    112443 |     0 |    112443 |    6246.8333 |
|            CAS_COUNT_WR STAT           |  MBOX1C1 |     20142 |     0 |     20142 |         1119 |
|            CAS_COUNT_RD STAT           |  MBOX4C0 |    104434 |     0 |    104434 |    5801.8889 |
|            CAS_COUNT_WR STAT           |  MBOX4C1 |     25545 |     0 |     25545 |    1419.1667 |
|            CAS_COUNT_RD STAT           |  MBOX5C0 |    120247 |     0 |    120247 |    6680.3889 |
|            CAS_COUNT_WR STAT           |  MBOX5C1 |     26763 |     0 |     26763 |    1486.8333 |
|            UNCORE_CLOCK STAT           |  UBOXFIX | 525148648 |     0 | 525148648 | 2.917492e+07 |
|           PWR_PKG_ENERGY STAT          |   PWR0   |   13.6923 |     0 |   13.6923 |       0.7607 |
|          PWR_DRAM_ENERGY STAT          |   PWR3   |    1.7842 |     0 |    1.7842 |       0.0991 |
+----------------------------------------+----------+-----------+-------+-----------+--------------+

+----------------------------------------+--------------+--------------+--------------+--------------+
|                 Metric                 |      Sum     |      Min     |      Max     |      Avg     |
+----------------------------------------+--------------+--------------+--------------+--------------+
|     Time: Runtime (RDTSC) [s] STAT     |      17.8884 |       0.9938 |       0.9938 |       0.9938 |
|     Time: Runtime unhalted [s] STAT    |       0.0779 | 1.087507e-05 |       0.0095 |       0.0043 |
|            inverseClock STAT           | 7.844171e-09 | 4.357873e-10 | 4.357873e-10 | 4.357873e-10 |
|            Clock [MHz] STAT            |   21740.0646 |    1197.2028 |    1354.1053 |    1207.7814 |
|         Uncore Clock [MHz] STAT        |     528.4099 |            0 |     528.4099 |      29.3561 |
|       Time: Core total stall STAT      |       0.0612 | 9.168639e-06 |       0.0070 |       0.0034 |
|        Time: Core l2 stall STAT        |       0.0342 | 3.517276e-06 |       0.0039 |       0.0019 |
|        Time: Core ldm stall STAT       |       0.0581 | 3.654259e-06 |       0.0063 |       0.0032 |
|                CPI STAT                |      45.7314 |       0.9163 |       7.4699 |       2.5406 |
|           Power PKG [W] STAT           |      13.7774 |            0 |      13.7774 |       0.7654 |
|           Power DRAM [W] STAT          |       1.7953 |            0 |       1.7953 |       0.0997 |
|           Energy PKG [J] STAT          |      13.6923 |            0 |      13.6923 |       0.7607 |
|          Energy DRAM [J] STAT          |       1.7842 |            0 |       1.7842 |       0.0991 |
|           L2M Pending[%] STAT          |     743.4477 |      29.9070 |      52.4016 |      41.3026 |
|           LD Pending[%] STAT           |    1194.5547 |      33.6022 |      83.5322 |      66.3642 |
|    LLC Any bandwidth [Bytes/s] STAT    |    253180500 |            0 |    253180500 | 1.406558e+07 |
| LLC data read bandwidth [Bytes/s] STAT |     73556950 |            0 |     73556950 | 4.086497e+06 |
|    LLC read bandwidth [Bytes/s] STAT   |    179837900 |            0 |    179837900 | 9.990994e+06 |
|   LLC write bandwidth [Bytes/s] STAT   |     22041380 |            0 |     22041380 | 1.224521e+06 |
|       LLC Any volume [Bytes] STAT      |    251617920 |            0 |    251617920 | 1.397877e+07 |
|    LLC data read volume [Bytes] STAT   |     73102976 |            0 |     73102976 | 4.061276e+06 |
|      LLC read volume [Bytes] STAT      |    178728000 |            0 |    178728000 | 9.929333e+06 |
|      LLC write volume [Bytes] STAT     |     21905344 |            0 |     21905344 | 1.216964e+06 |
|   DRAM read bandwidth [Bytes/s] STAT   |     30284060 |            0 |     30284060 | 1.682448e+06 |
|   DRAM write bandwidth [Bytes/s] STAT  |      7134271 |            0 |      7134271 |  396348.3889 |
|      DRAM read volume [Bytes] STAT     |     30097152 |            0 |     30097152 |      1672064 |
|     DRAM write volume [Bytes] STAT     |      7090240 |            0 |      7090240 |  393902.2222 |
|           Time: MEM busy STAT          |       0.0006 |            0 |       0.0006 | 3.333333e-05 |
|           Time: L3 busy STAT           |       0.0005 |            0 |       0.0005 | 2.777778e-05 |
|               Ins [] STAT              |     43076772 |         1743 |      5737867 |      2393154 |
|              Cycle [] STAT             |     94613446 |        13020 |     11385668 | 5.256303e+06 |
|            Stall_l2M [] STAT           |     41478628 |         4211 |      4871467 | 2.304368e+06 |
|            Stall_mem [] STAT           |     70652065 |         4375 |      7778690 | 3.925115e+06 |
|           L3_Latency [] STAT           |      10.5502 |       0.0011 |       1.2391 |       0.5861 |
|          DRAM_latency [] STAT          |     121.5929 |       0.0075 |      13.3872 |       6.7552 |
+----------------------------------------+--------------+--------------+--------------+--------------+



* Stream benchmark
Result of likwid under roof_latency group using Stream benchmark
Number of cores used: 18
Run Stream benchmark 5 times and calculate the average

* The first take
![](pictures/firsttake1.png)
![](pictures/firsttake2.png)
![](pictures/firsttake3.png)

* The second take
![](pictures/secondtake1.png)
![](pictures/secondtake2.png)
![](pictures/secondtake3.png)

* The third take
![](pictures/thirdtake1.png)
![](pictures/thirdtake2.png)
![](pictures/thirdtake3.png)

* The fourth take
![](pictures/fourthtake1.png)
![](pictures/fourthtake2.png)
![](pictures/fourthtake3.png)

* The fifth take
![](pictures/fifthtake1.png)
![](pictures/fifthtake2.png)
![](pictures/fifthtake3.png)

