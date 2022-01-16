# BA_roofline

CPU name:	Intel(R) Xeon(R) CPU E5-2699 v3 @ 2.30GHz
CPU type:	Intel Xeon Haswell EN/EP/EX processor
CPU clock:	2.29 GHz

* Control Group

Result of likwid under roof_latency group and sleep 1s
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
Run Stream benchmark 3 times and calculate the average

* Problem size is big enough for DRAM


+----------------------------------------+---------------+--------------+---------------+--------------+
|                 Metric                 |      Sum      |      Min     |      Max      |      Avg     |
+----------------------------------------+---------------+--------------+---------------+--------------+
|     Time: Runtime (RDTSC) [s] STAT     |      395.9622 |      21.9979 |       21.9979 |      21.9979 |
|     Time: Runtime unhalted [s] STAT    |      390.2989 |      21.6753 |       21.7376 |      21.6833 |
|            inverseClock STAT           |  7.844166e-09 | 4.357870e-10 |  4.357870e-10 | 4.357870e-10 |
|            Clock [MHz] STAT            |    50211.9528 |    2785.7172 |     2794.8715 |    2789.5529 |
|         Uncore Clock [MHz] STAT        |     2987.8220 |            0 |     2987.8220 |     165.9901 |
|       Time: Core total stall STAT      |      284.7393 |      15.7854 |       15.8642 |      15.8189 |
|        Time: Core l2 stall STAT        |      124.5348 |       6.8686 |        6.9578 |       6.9186 |
|        Time: Core ldm stall STAT       |      151.4953 |       8.3399 |        8.4838 |       8.4164 |
|                CPI STAT                |       34.5104 |       1.8997 |        1.9227 |       1.9172 |
|           Power PKG [W] STAT           |      126.4698 |            0 |      126.4698 |       7.0261 |
|           Power DRAM [W] STAT          |       18.3375 |            0 |       18.3375 |       1.0187 |
|           Energy PKG [J] STAT          |     2782.0743 |            0 |     2782.0743 |     154.5597 |
|          Energy DRAM [J] STAT          |      403.3861 |            0 |      403.3861 |      22.4103 |
|           L2M Pending[%] STAT          |      574.3358 |      31.6780 |       32.0861 |      31.9075 |
|           LD Pending[%] STAT           |      698.6750 |      38.3664 |       39.1292 |      38.8153 |
|    LLC Any bandwidth [Bytes/s] STAT    |   74006830000 |            0 |   74006830000 | 4.111491e+09 |
| LLC data read bandwidth [Bytes/s] STAT |   22156010000 |            0 |   22156010000 | 1.230889e+09 |
|    LLC read bandwidth [Bytes/s] STAT   |   36956520000 |            0 |   36956520000 |   2053140000 |
|   LLC write bandwidth [Bytes/s] STAT   |   14623900000 |            0 |   14623900000 | 8.124389e+08 |
|       LLC Any volume [Bytes] STAT      | 1627997408256 |            0 | 1627997408256 | 9.044430e+10 |
|    LLC data read volume [Bytes] STAT   |  487386450112 |            0 |  487386450112 | 2.707703e+10 |
|      LLC read volume [Bytes] STAT      |  812967068032 |            0 |  812967068032 | 4.516484e+10 |
|      LLC write volume [Bytes] STAT     |  321695705792 |            0 |  321695705792 | 1.787198e+10 |
|   DRAM read bandwidth [Bytes/s] STAT   |   36643140000 |            0 |   36643140000 |   2035730000 |
|   DRAM write bandwidth [Bytes/s] STAT  |   14608160000 |            0 |   14608160000 | 8.115644e+08 |
|      DRAM read volume [Bytes] STAT     |  806073487040 |            0 |  806073487040 | 4.478186e+10 |
|     DRAM write volume [Bytes] STAT     |  321349310656 |            0 |  321349310656 | 1.785274e+10 |
|           Time: MEM busy STAT          |       24.2979 |            0 |       24.2979 |       1.3499 |
|           Time: L3 busy STAT           |        2.9319 |            0 |        2.9319 |       0.1629 |
|               Ins [] STAT              |  567881256791 |  31460617356 |   31980817926 | 3.154896e+10 |
|              Cycle [] STAT             | 1088759940804 |  60391086711 |   60753835479 |  60486663378 |
|            Stall_l2M [] STAT           |  347396609123 |  19159558227 |   19446268129 | 1.929981e+10 |
|            Stall_mem [] STAT           |  422604145778 |  23309052164 |   23667538647 | 2.347801e+10 |
|           L3_Latency [] STAT           |       13.6569 |       0.7532 |        0.7645 |       0.7587 |
|          DRAM_latency [] STAT          |       23.9900 |       1.3232 |        1.3435 |       1.3328 |
+----------------------------------------+---------------+--------------+---------------+--------------+



* The problem size is reduced for cache testing


+----------------------------------------+---------------+--------------+---------------+--------------+
|                 Metric                 |      Sum      |      Min     |      Max      |      Avg     |
+----------------------------------------+---------------+--------------+---------------+--------------+
|     Time: Runtime (RDTSC) [s] STAT     |      210.3750 |      11.6875 |       11.6875 |      11.6875 |
|     Time: Runtime unhalted [s] STAT    |      207.8772 |      11.4983 |       11.5539 |      11.5487 |
|            inverseClock STAT           |  7.844175e-09 | 4.357875e-10 |  4.357875e-10 | 4.357875e-10 |
|            Clock [MHz] STAT            |    50111.8036 |    2778.7485 |     2789.3769 |    2783.9891 |
|         Uncore Clock [MHz] STAT        |     2932.2592 |            0 |     2932.2592 |     162.9033 |
|       Time: Core total stall STAT      |       29.5208 |       1.6159 |        1.6487 |       1.6400 |
|        Time: Core l2 stall STAT        |        2.3900 |       0.1034 |        0.2131 |       0.1328 |
|        Time: Core ldm stall STAT       |       26.5063 |       1.4565 |        1.4802 |       1.4726 |
|                CPI STAT                |       10.2467 |       0.5676 |        0.5702 |       0.5693 |
|           Power PKG [W] STAT           |      142.6615 |            0 |      142.6615 |       7.9256 |
|           Power DRAM [W] STAT          |        6.0096 |            0 |        6.0096 |       0.3339 |
|           Energy PKG [J] STAT          |     1667.3534 |            0 |     1667.3534 |      92.6307 |
|          Energy DRAM [J] STAT          |       70.2375 |            0 |       70.2375 |       3.9021 |
|           L2M Pending[%] STAT          |       20.6948 |       0.8952 |        1.8448 |       1.1497 |
|           LD Pending[%] STAT           |      229.5167 |      12.6484 |       12.8170 |      12.7509 |
|    LLC Any bandwidth [Bytes/s] STAT    |  221684800000 |            0 |  221684800000 | 1.231582e+10 |
| LLC data read bandwidth [Bytes/s] STAT |   74693050000 |            0 |   74693050000 | 4.149614e+09 |
|    LLC read bandwidth [Bytes/s] STAT   |  124478300000 |            0 |  124478300000 | 6.915461e+09 |
|   LLC write bandwidth [Bytes/s] STAT   |   49390430000 |            0 |   49390430000 | 2.743913e+09 |
|       LLC Any volume [Bytes] STAT      | 2590936419648 |            0 | 2590936419648 | 1.439409e+11 |
|    LLC data read volume [Bytes] STAT   |  872973565568 |            0 |  872973565568 | 4.849853e+10 |
|      LLC read volume [Bytes] STAT      | 1454838212096 |            0 | 1454838212096 | 8.082435e+10 |
|      LLC write volume [Bytes] STAT     |  577249690688 |            0 |  577249690688 | 3.206943e+10 |
|   DRAM read bandwidth [Bytes/s] STAT   |     116102100 |            0 |     116102100 | 6.450117e+06 |
|   DRAM write bandwidth [Bytes/s] STAT  |      65372070 |            0 |      65372070 | 3.631782e+06 |
|      DRAM read volume [Bytes] STAT     |    1356941248 |            0 |    1356941248 | 7.538562e+07 |
|     DRAM write volume [Bytes] STAT     |     764034880 |            0 |     764034880 | 4.244638e+07 |
|           Time: MEM busy STAT          |        0.0457 |            0 |        0.0457 |       0.0025 |
|           Time: L3 busy STAT           |        5.2509 |            0 |        5.2509 |       0.2917 |
|               Ins [] STAT              | 1016628789998 |  56452247400 |   56522779049 | 5.647938e+10 |
|              Cycle [] STAT             |  578727263967 |  32073186950 |   32200832481 | 3.215151e+10 |
|            Stall_l2M [] STAT           |    6653803438 |    287899126 |     593306081 | 3.696557e+08 |
|            Stall_LDM [] STAT           |   73793263947 |   4062847041 |    4122559801 | 4.099626e+09 |
|           L3_Latency [] STAT           |        0.1643 |       0.0071 |        0.0147 |       0.0091 |
|          DRAM_latency [] STAT          |     2226.6957 |     122.5955 |      124.3974 |     123.7053 |
+----------------------------------------+---------------+--------------+---------------+--------------+


* NAS Parallel bencnmark - CG 
Result of likwid under roof_latency group using CG benchmark
CG = Conjugate Gradient, irregular memory access and communication
Number of cores used: 18
Run CG 5 times and get the average

* The first take

+----------------------------------------+---------------+--------------+---------------+--------------+
|                 Metric                 |      Sum      |      Min     |      Max      |      Avg     |
+----------------------------------------+---------------+--------------+---------------+--------------+
|     Time: Runtime (RDTSC) [s] STAT     |      610.0542 |      33.8919 |       33.8919 |      33.8919 |
|     Time: Runtime unhalted [s] STAT    |      574.4137 |      28.8855 |       33.0064 |      31.9119 |
|            inverseClock STAT           |  7.844224e-09 | 4.357902e-10 |  4.357902e-10 | 4.357902e-10 |
|            Clock [MHz] STAT            |    50201.3997 |    2785.7354 |     2791.4130 |    2788.9667 |
|         Uncore Clock [MHz] STAT        |     2984.6391 |            0 |     2984.6391 |     165.8133 |
|       Time: Core total stall STAT      |      437.4518 |      20.9046 |       25.5386 |      24.3029 |
|        Time: Core l2 stall STAT        |      424.4545 |      19.7572 |       25.0345 |      23.5808 |
|        Time: Core ldm stall STAT       |      426.1188 |      19.8401 |       25.1006 |      23.6733 |
|                CPI STAT                |       45.1421 |       2.1837 |        2.6279 |       2.5079 |
|           Power PKG [W] STAT           |      123.5617 |            0 |      123.5617 |       6.8645 |
|           Power DRAM [W] STAT          |       12.9083 |            0 |       12.9083 |       0.7171 |
|           Energy PKG [J] STAT          |     4187.7411 |            0 |     4187.7411 |     232.6523 |
|          Energy DRAM [J] STAT          |      437.4854 |            0 |      437.4854 |      24.3047 |
|           L2M Pending[%] STAT          |     1328.9526 |      68.3981 |       75.9121 |      73.8307 |
|           LD Pending[%] STAT           |     1334.1855 |      68.6852 |       76.0751 |      74.1214 |
|    LLC Any bandwidth [Bytes/s] STAT    |  141624100000 |            0 |  141624100000 | 7.868006e+09 |
| LLC data read bandwidth [Bytes/s] STAT |  136573900000 |            0 |  136573900000 | 7.587439e+09 |
|    LLC read bandwidth [Bytes/s] STAT   |  137012700000 |            0 |  137012700000 | 7.611817e+09 |
|   LLC write bandwidth [Bytes/s] STAT   |     481571400 |            0 |     481571400 | 2.675397e+07 |
|       LLC Any volume [Bytes] STAT      | 4799910385472 |            0 | 4799910385472 | 2.666617e+11 |
|    LLC data read volume [Bytes] STAT   | 4628750277760 |            0 | 4628750277760 | 2.571528e+11 |
|      LLC read volume [Bytes] STAT      | 4643623314816 |            0 | 4643623314816 | 2.579791e+11 |
|      LLC write volume [Bytes] STAT     |   16321374144 |            0 |   16321374144 |    906743008 |
|   DRAM read bandwidth [Bytes/s] STAT   |   26020330000 |            0 |   26020330000 | 1.445574e+09 |
|   DRAM write bandwidth [Bytes/s] STAT  |     390919500 |            0 |     390919500 |     21717750 |
|      DRAM read volume [Bytes] STAT     |  881878746240 |            0 |  881878746240 |  48993263680 |
|     DRAM write volume [Bytes] STAT     |   13249007488 |            0 |   13249007488 | 7.360560e+08 |
|           Time: MEM busy STAT          |       19.2915 |            0 |       19.2915 |       1.0717 |
|           Time: L3 busy STAT           |       12.0412 |            0 |       12.0412 |       0.6690 |
|               Ins [] STAT              |  639228121806 |  34954122889 |   36849025076 | 3.551267e+10 |
|              Cycle [] STAT             | 1602038610086 |  80467498169 |   92122606007 | 8.900215e+10 |
|            Stall_l2M [] STAT           | 1183812604891 |  55038205932 |   69872472051 | 6.576737e+10 |
|            Stall_mem [] STAT           | 1188454396523 |  55269224819 |   70057075518 | 6.602524e+10 |
|           L3_Latency [] STAT           |       15.7844 |       0.7339 |        0.9317 |       0.8769 |
|          DRAM_latency [] STAT          |       84.9725 |       3.9516 |        5.0090 |       4.7207 |
+----------------------------------------+---------------+--------------+---------------+--------------+

* The second take

+----------------------------------------+---------------+--------------+---------------+--------------+
|                 Metric                 |      Sum      |      Min     |      Max      |      Avg     |
+----------------------------------------+---------------+--------------+---------------+--------------+
|     Time: Runtime (RDTSC) [s] STAT     |      583.3926 |      32.4107 |       32.4107 |      32.4107 |
|     Time: Runtime unhalted [s] STAT    |      551.0382 |      28.8156 |       31.5088 |      30.6132 |
|            inverseClock STAT           |  7.844184e-09 | 4.357880e-10 |  4.357880e-10 | 4.357880e-10 |
|            Clock [MHz] STAT            |    50185.3697 |    2786.8237 |     2789.4947 |    2788.0761 |
|         Uncore Clock [MHz] STAT        |     2984.0062 |            0 |     2984.0062 |     165.7781 |
|       Time: Core total stall STAT      |      415.2960 |      21.0063 |       24.1427 |      23.0720 |
|        Time: Core l2 stall STAT        |      403.0983 |      20.0007 |       23.7065 |      22.3943 |
|        Time: Core ldm stall STAT       |      404.5326 |      20.0933 |       23.7545 |      22.4740 |
|                CPI STAT                |       43.4495 |       2.2097 |        2.5270 |       2.4139 |
|           Power PKG [W] STAT           |      124.8526 |            0 |      124.8526 |       6.9363 |
|           Power DRAM [W] STAT          |       13.2651 |            0 |       13.2651 |       0.7369 |
|           Energy PKG [J] STAT          |     4046.5657 |            0 |     4046.5657 |     224.8092 |
|          Energy DRAM [J] STAT          |      429.9307 |            0 |      429.9307 |      23.8850 |
|           L2M Pending[%] STAT          |     1316.1184 |      69.4093 |       75.2375 |      73.1177 |
|           LD Pending[%] STAT           |     1320.8092 |      69.7305 |       75.3899 |      73.3783 |
|    LLC Any bandwidth [Bytes/s] STAT    |  147419900000 |            0 |  147419900000 | 8.189994e+09 |
| LLC data read bandwidth [Bytes/s] STAT |  142519300000 |            0 |  142519300000 | 7.917739e+09 |
|    LLC read bandwidth [Bytes/s] STAT   |  142967400000 |            0 |  142967400000 | 7.942633e+09 |
|   LLC write bandwidth [Bytes/s] STAT   |     491840900 |            0 |     491840900 | 2.732449e+07 |
|       LLC Any volume [Bytes] STAT      | 4777988864704 |            0 | 4777988864704 | 2.654438e+11 |
|    LLC data read volume [Bytes] STAT   | 4619155278144 |            0 | 4619155278144 | 2.566197e+11 |
|      LLC read volume [Bytes] STAT      | 4633679597568 |            0 | 4633679597568 | 2.574266e+11 |
|      LLC write volume [Bytes] STAT     |   15940927168 |            0 |   15940927168 | 8.856071e+08 |
|   DRAM read bandwidth [Bytes/s] STAT   |   27205720000 |            0 |   27205720000 | 1.511429e+09 |
|   DRAM write bandwidth [Bytes/s] STAT  |     407446300 |            0 |     407446300 | 2.263591e+07 |
|      DRAM read volume [Bytes] STAT     |  881757659584 |            0 |  881757659584 | 4.898654e+10 |
|     DRAM write volume [Bytes] STAT     |   13205636800 |            0 |   13205636800 | 7.336465e+08 |
|           Time: MEM busy STAT          |       19.2880 |            0 |       19.2880 |       1.0716 |
|           Time: L3 busy STAT           |       12.0145 |            0 |       12.0145 |       0.6675 |
|               Ins [] STAT              |  636659722690 |  34570372093 |   36341546572 | 3.536998e+10 |
|              Cycle [] STAT             | 1536341239777 |  80304134443 |   87861231976 | 8.535229e+10 |
|            Stall_l2M [] STAT           | 1123874410744 |  55738504233 |   66104614147 | 6.243747e+10 |
|            Stall_mem [] STAT           | 1127872349857 |  55996464441 |   66238497915 | 6.265957e+10 |
|           L3_Latency [] STAT           |       15.0541 |       0.7466 |        0.8855 |       0.8363 |
|          DRAM_latency [] STAT          |       80.6558 |       4.0044 |        4.7368 |       4.4809 |
+----------------------------------------+---------------+--------------+---------------+--------------+

* The third take 

+----------------------------------------+---------------+--------------+---------------+--------------+
|                 Metric                 |      Sum      |      Min     |      Max      |      Avg     |
+----------------------------------------+---------------+--------------+---------------+--------------+
|     Time: Runtime (RDTSC) [s] STAT     |      613.5588 |      34.0866 |       34.0866 |      34.0866 |
|     Time: Runtime unhalted [s] STAT    |      575.1707 |      29.3295 |       33.3309 |      31.9539 |
|            inverseClock STAT           |  7.844747e-09 | 4.358193e-10 |  4.358193e-10 | 4.358193e-10 |
|            Clock [MHz] STAT            |    50185.5292 |    2783.9938 |     2790.4758 |    2788.0850 |
|         Uncore Clock [MHz] STAT        |     2984.1110 |            0 |     2984.1110 |     165.7839 |
|       Time: Core total stall STAT      |      438.0784 |      21.3934 |       25.9512 |      24.3377 |
|        Time: Core l2 stall STAT        |      424.8398 |      20.3498 |       25.5549 |      23.6022 |
|        Time: Core ldm stall STAT       |      426.5843 |      20.4146 |       25.6034 |      23.6991 |
|                CPI STAT                |       45.1752 |       2.2282 |        2.6772 |       2.5097 |
|           Power PKG [W] STAT           |      125.4219 |            0 |      125.4219 |       6.9679 |
|           Power DRAM [W] STAT          |       12.9557 |            0 |       12.9557 |       0.7198 |
|           Energy PKG [J] STAT          |     4275.1997 |            0 |     4275.1997 |     237.5111 |
|          Energy DRAM [J] STAT          |      441.6142 |            0 |      441.6142 |      24.5341 |
|           L2M Pending[%] STAT          |     1328.4375 |      69.3833 |       76.6704 |      73.8021 |
|           LD Pending[%] STAT           |     1333.9162 |      69.6044 |       76.8159 |      74.1065 |
|    LLC Any bandwidth [Bytes/s] STAT    |  140641400000 |            0 |  140641400000 | 7.813411e+09 |
| LLC data read bandwidth [Bytes/s] STAT |  135578900000 |            0 |  135578900000 | 7.532161e+09 |
|    LLC read bandwidth [Bytes/s] STAT   |  136012000000 |            0 |  136012000000 | 7.556222e+09 |
|   LLC write bandwidth [Bytes/s] STAT   |     476005700 |            0 |     476005700 | 2.644476e+07 |
|       LLC Any volume [Bytes] STAT      | 4793979902208 |            0 | 4793979902208 | 2.663322e+11 |
|    LLC data read volume [Bytes] STAT   | 4621416348160 |            0 | 4621416348160 | 2.567454e+11 |
|      LLC read volume [Bytes] STAT      | 4636179968576 |            0 | 4636179968576 | 2.575656e+11 |
|      LLC write volume [Bytes] STAT     |   16225393408 |            0 |   16225393408 | 9.014107e+08 |
|   DRAM read bandwidth [Bytes/s] STAT   |   25852800000 |            0 |   25852800000 | 1.436267e+09 |
|   DRAM write bandwidth [Bytes/s] STAT  |     387813800 |            0 |     387813800 | 2.154521e+07 |
|      DRAM read volume [Bytes] STAT     |  881232884736 |            0 |  881232884736 | 4.895738e+10 |
|     DRAM write volume [Bytes] STAT     |   13219234816 |            0 |   13219234816 | 7.344019e+08 |
|           Time: MEM busy STAT          |       19.2770 |            0 |       19.2770 |       1.0709 |
|           Time: L3 busy STAT           |       12.0217 |            0 |       12.0217 |       0.6679 |
|               Ins [] STAT              |  639373036345 |  34740296973 |   36645514472 | 3.552072e+10 |
|              Cycle [] STAT             | 1603647835817 |  81653036871 |   93005074558 | 8.909155e+10 |
|            Stall_l2M [] STAT           | 1184521818630 |  56653581472 |   71307376115 | 6.580677e+10 |
|            Stall_mem [] STAT           | 1189385191769 |  56834083822 |   71442669687 | 6.607696e+10 |
|           L3_Latency [] STAT           |       15.8136 |       0.7563 |        0.9520 |       0.8785 |
|          DRAM_latency [] STAT          |       85.1031 |       4.0666 |        5.1119 |       4.7279 |
+----------------------------------------+---------------+--------------+---------------+--------------+




* Class is B problem size is set to 20000: (in this case data is mostly in cache not DRAM)

+----------------------------------------+--------------+--------------+--------------+--------------+
|                 Metric                 |      Sum     |      Min     |      Max     |      Avg     |
+----------------------------------------+--------------+--------------+--------------+--------------+
|     Time: Runtime (RDTSC) [s] STAT     |      16.9740 |       0.9430 |       0.9430 |       0.9430 |
|     Time: Runtime unhalted [s] STAT    |      14.7399 |       0.8094 |       0.8324 |       0.8189 |
|            inverseClock STAT           | 7.844321e-09 | 4.357956e-10 | 4.357956e-10 | 4.357956e-10 |
|            Clock [MHz] STAT            |   47918.3114 |    2555.1656 |    2699.8191 |    2662.1284 |
|         Uncore Clock [MHz] STAT        |    2765.5592 |            0 |    2765.5592 |     153.6422 |
|       Time: Core total stall STAT      |       4.1852 |       0.2175 |       0.2414 |       0.2325 |
|        Time: Core l2 stall STAT        |       2.3010 |       0.1104 |       0.1565 |       0.1278 |
|        Time: Core ldm stall STAT       |       3.1524 |       0.1584 |       0.2034 |       0.1751 |
|                CPI STAT                |      11.2409 |       0.6014 |       0.6421 |       0.6245 |
|           Power PKG [W] STAT           |     127.3681 |            0 |     127.3681 |       7.0760 |
|           Power DRAM [W] STAT          |       8.8885 |            0 |       8.8885 |       0.4938 |
|           Energy PKG [J] STAT          |     120.1035 |            0 |     120.1035 |       6.6724 |
|          Energy DRAM [J] STAT          |       8.3815 |            0 |       8.3815 |       0.4656 |
|           L2M Pending[%] STAT          |     280.9769 |      13.5251 |      19.0576 |      15.6098 |
|           LD Pending[%] STAT           |     384.9329 |      19.4017 |      24.7683 |      21.3852 |
|    LLC Any bandwidth [Bytes/s] STAT    | 209791800000 |            0 | 209791800000 |  11655100000 |
| LLC data read bandwidth [Bytes/s] STAT | 161550400000 |            0 | 161550400000 | 8.975022e+09 |
|    LLC read bandwidth [Bytes/s] STAT   | 163642800000 |            0 | 163642800000 | 9.091267e+09 |
|   LLC write bandwidth [Bytes/s] STAT   |   1693107000 |            0 |   1693107000 |     94061500 |
|       LLC Any volume [Bytes] STAT      | 197825969024 |            0 | 197825969024 | 1.099033e+10 |
|    LLC data read volume [Bytes] STAT   | 152336124032 |            0 | 152336124032 | 8.463118e+09 |
|      LLC read volume [Bytes] STAT      | 154309137472 |            0 | 154309137472 | 8.572730e+09 |
|      LLC write volume [Bytes] STAT     |   1596537664 |            0 |   1596537664 | 8.869654e+07 |
|   DRAM read bandwidth [Bytes/s] STAT   |  11956440000 |            0 |  11956440000 | 6.642467e+08 |
|   DRAM write bandwidth [Bytes/s] STAT  |    202196800 |            0 |    202196800 | 1.123316e+07 |
|      DRAM read volume [Bytes] STAT     |  11274480512 |            0 |  11274480512 | 6.263600e+08 |
|     DRAM write volume [Bytes] STAT     |    190664128 |            0 |    190664128 | 1.059245e+07 |
|           Time: MEM busy STAT          |       0.2471 |            0 |       0.2471 |       0.0137 |
|           Time: L3 busy STAT           |       0.4029 |            0 |       0.4029 |       0.0224 |
|               Ins [] STAT              |  62839166751 |   3417670621 |   3555966104 | 3.491065e+09 |
|              Cycle [] STAT             |  39241008656 |   2068045476 |   2218019834 | 2.180056e+09 |
|            Stall_l2M [] STAT           |   6126985741 |    287108008 |    418245834 | 3.403881e+08 |
|            Stall_LDM [] STAT           |   8393670245 |    411855653 |    543576290 | 4.663150e+08 |
|           L3_Latency [] STAT           |       1.9822 |       0.0929 |       0.1353 |       0.1101 |
|          DRAM_latency [] STAT          |      46.8546 |       2.2990 |       3.0343 |       2.6030 |
+----------------------------------------+--------------+--------------+--------------+--------------+
* Run sampling doing nothing 

init freeze 700 80000000
init unfreeze 700 20000000
Node object is created
registed sampling event
overflow 0.456825
Socket : 1
socket 1 1206932466 359190
Uncorefreq: 2.6412e+09
18 1120499840.000000 1215273600.000000 1046257920.000000
19 2207371776.000000 2391887360.000000 2085359360.000000
20 3300416512.000000 3577006336.000000 3133085696.000000
21 4377470976.000000 4742683136.000000 4180729600.000000
22 5454765056.000000 5911332864.000000 5228430336.000000
23 6536303616.000000 7085095936.000000 6276311040.000000
24 7618963456.000000 8259426304.000000 7322400256.000000
25 8702027776.000000 9433816064.000000 8369659904.000000
26 9788922880.000000 10612282368.000000 9416792064.000000
27 10873216000.000000 11788219392.000000 10463815680.000000
28 11958189056.000000 12964647936.000000 11510726656.000000
29 13047425024.000000 14145566720.000000 12556689408.000000
30 14135267328.000000 15325296640.000000 13603433472.000000
31 15218341888.000000 16499978240.000000 14650078208.000000
32 16306813952.000000 17680670720.000000 15696628736.000000
33 17404833792.000000 18872272896.000000 16743104512.000000
34 18526425088.000000 20088692736.000000 17789579264.000000
35 19634333696.000000 21271805952.000000 18820263936.000000
coreFreq : 2.4866e+09
clockTime : 4.7526e-01
wallTime : 4.5682e-01
insPerSec : 4.1313e+10
cycles : 21271805952.000000
L2 stalld : 1952944512.000000
 L2 stall rate : 0.091809
 Ldm stalld : 4733447168.000000
LDM stall rate : 0.222522
PKG Energy: 0.000000
 PKG Power : 0.000000
DRAM Energy: 0.000000
 Power : 0.000000
stallL2Rate : 0.0918
stallLDMRate : 0.2225
stallL2Cycles : 1952944512.0000
stallLDMCycles : 4733447168.0000
idealInsPerSecL2 : 4.5489e+10
idealInsPerSecLDM : 5.3137e+10
L3 volum: 5.6021e+07
RAM volum: 1.2676e+07
lowerBound : 14
 upperBound : 15
full L3 BW : 3.8230e+11
 fullRAMBW: 5.9089e+10
Latency L3 : 34.8607
 DRAM : 373.4152
Bandwidth Usage L3 : 0.0003
, Bandwidth usage DRAM : 0.0005
realIntensityL3 : 350.4789
 roofIntensityL3 : 0.1190
realIntensityRAM : 1548.9259
 roofIntensityRAM : 0.8993
conclusion: compute bound 1 l3boundness 1 ramboundness 1

-----------------------
--------------0
overflow 0.359078
Socket : 1
socket 1 2292619700 1206932466
Uncorefreq: 3.0235e+09
18 938878016.000000 1013429504.000000 832460096.000000
19 1877902848.000000 2026856576.000000 1664918016.000000
20 2817007616.000000 3040281088.000000 2497373952.000000
21 3755520000.000000 4053704704.000000 3329829120.000000
22 4694150144.000000 5067129344.000000 4162285056.000000
23 5632905216.000000 6080552448.000000 4994739712.000000
24 6571808768.000000 7093974016.000000 5827193344.000000
25 7510900736.000000 8107395584.000000 6659646464.000000
26 8450067968.000000 9120813056.000000 7492097024.000000
27 9388662784.000000 10134231040.000000 8324547584.000000
28 10327730176.000000 11147648000.000000 9156997120.000000
29 11266587648.000000 12161064960.000000 9989446656.000000
30 12205687808.000000 13174479872.000000 10821894144.000000
31 13144529920.000000 14187892736.000000 11654340608.000000
32 14083381248.000000 15201305600.000000 12486787072.000000
33 15022371840.000000 16214718464.000000 13319233536.000000
34 15961266176.000000 17228132352.000000 14151680000.000000
35 16900695040.000000 18241546240.000000 14984126464.000000
coreFreq : 2.6783e+09
clockTime : 3.7839e-01
wallTime : 3.5908e-01
insPerSec : 4.4665e+10
cycles : 18241546240.000000
L2 stalld : 1538145280.000000
 L2 stall rate : 0.084321
 Ldm stalld : 4057480704.000000
LDM stall rate : 0.222431
PKG Energy: 0.000000
 PKG Power : 0.000000
DRAM Energy: 0.000000
 Power : 0.000000
stallL2Rate : 0.0843
stallLDMRate : 0.2224
stallL2Cycles : 1538145280.0000
stallLDMCycles : 4057480704.0000
idealInsPerSecL2 : 4.8778e+10
idealInsPerSecLDM : 5.7442e+10
L3 volum: 2.5909e+07
RAM volum: 6.0962e+06
lowerBound : 18
 upperBound : 15
full L3 BW : 1.2665e+11
 fullRAMBW: 1.4005e+10
Latency L3 : 59.3668
 DRAM : 665.5763
Bandwidth Usage L3 : 0.0006
, Bandwidth usage DRAM : 0.0012
realIntensityL3 : 652.3052
 roofIntensityL3 : 0.3852
realIntensityRAM : 2772.3364
 roofIntensityRAM : 4.1016
conclusion: compute bound 1 l3boundness 1 ramboundness 1

-----------------------
--------------1
overflow 0.359949
Socket : 1
socket 1 3380002710 2292619700
Uncorefreq: 3.0209e+09
18 939963840.000000 1014922944.000000 833686720.000000
19 1879850240.000000 2029845248.000000 1667372928.000000
20 2819922432.000000 3044767232.000000 2501058816.000000
21 3759595264.000000 4059688192.000000 3334744064.000000
22 4699498496.000000 5074607104.000000 4168427264.000000
23 5639383040.000000 6089524736.000000 5002109952.000000
24 6579368448.000000 7104442880.000000 5835792896.000000
25 7519593472.000000 8119360000.000000 6669474816.000000
26 8459678720.000000 9134277632.000000 7503157248.000000
27 9399775232.000000 10149193728.000000 8336838144.000000
28 10339902464.000000 11164109824.000000 9170519040.000000
29 11280059392.000000 12179022848.000000 10004197376.000000
30 12220178432.000000 13193936896.000000 10837876736.000000
31 13160320000.000000 14208849920.000000 11671555072.000000
32 14100438016.000000 15223760896.000000 12505231360.000000
33 15040487424.000000 16238670848.000000 13338907648.000000
34 15980654592.000000 17253578752.000000 14172581888.000000
35 16921125888.000000 18268485632.000000 15006256128.000000
coreFreq : 2.6783e+09
clockTime : 3.7894e-01
wallTime : 3.5995e-01
insPerSec : 4.4653e+10
cycles : 18268485632.000000
L2 stalld : 1750702336.000000
 L2 stall rate : 0.095832
 Ldm stalld : 4064355072.000000
LDM stall rate : 0.222479
PKG Energy: 0.000000
 PKG Power : 0.000000
DRAM Energy: 0.000000
 Power : 0.000000
stallL2Rate : 0.0958
stallLDMRate : 0.2225
stallL2Cycles : 1750702336.0000
stallLDMCycles : 4064355072.0000
idealInsPerSecL2 : 4.9386e+10
idealInsPerSecLDM : 5.7430e+10
L3 volum: 2.4508e+07
RAM volum: 5.7945e+06
lowerBound : 18
 upperBound : 15
full L3 BW : 1.1778e+11
 fullRAMBW: 1.2456e+10
Latency L3 : 71.4336
 DRAM : 701.4165
Bandwidth Usage L3 : 0.0006
, Bandwidth usage DRAM : 0.0013
realIntensityL3 : 690.4301
 roofIntensityL3 : 0.4193
realIntensityRAM : 2920.2068
 roofIntensityRAM : 4.6107
conclusion: compute bound 1 l3boundness 1 ramboundness 1

-----------------------
--------------2
overflow 0.359227
Socket : 1
socket 1 4464848626 3380002710
Uncorefreq: 3.0199e+09
18 937946752.000000 1012527424.000000 831718848.000000
19 1876163840.000000 2025055744.000000 1663438592.000000
20 2814524928.000000 3037584896.000000 2495159296.000000
21 3752352768.000000 4050113280.000000 3326878976.000000
22 4690348544.000000 5062642688.000000 4158599424.000000
23 5628205056.000000 6075171840.000000 4990320128.000000
24 6566194176.000000 7087700480.000000 5822040064.000000
25 7504347136.000000 8100228096.000000 6653759488.000000
26 8442464256.000000 9112754176.000000 7485477888.000000
27 9380544512.000000 10125282304.000000 8317197312.000000
28 10318640128.000000 11137809408.000000 9148915712.000000
29 11256810496.000000 12150335488.000000 9980634112.000000
30 12194977792.000000 13162862592.000000 10812352512.000000
31 13132553216.000000 14175389696.000000 11644070912.000000
32 14070702080.000000 15187915776.000000 12475789312.000000
33 15008841728.000000 16200441856.000000 13307506688.000000
34 15946700800.000000 17212968960.000000 14139225088.000000
35 16885334016.000000 18225494016.000000 14970941440.000000
coreFreq : 2.6783e+09
clockTime : 3.7805e-01
wallTime : 3.5923e-01
insPerSec : 4.4664e+10
cycles : 18225494016.000000
L2 stalld : 1527777792.000000
 L2 stall rate : 0.083826
 Ldm stalld : 4054459392.000000
LDM stall rate : 0.222461
PKG Energy: 0.000000
 PKG Power : 0.000000
DRAM Energy: 0.000000
 Power : 0.000000
stallL2Rate : 0.0838
stallLDMRate : 0.2225
stallL2Cycles : 1527777792.0000
stallLDMCycles : 4054459392.0000
idealInsPerSecL2 : 4.8750e+10
idealInsPerSecLDM : 5.7443e+10
L3 volum: 2.2787e+07
RAM volum: 5.3354e+06
lowerBound : 18
 upperBound : 15
full L3 BW : 1.1443e+11
 fullRAMBW: 1.1870e+10
Latency L3 : 67.0456
 DRAM : 759.9133
Bandwidth Usage L3 : 0.0006
, Bandwidth usage DRAM : 0.0013
realIntensityL3 : 741.0029
 roofIntensityL3 : 0.4260
realIntensityRAM : 3164.7595
 roofIntensityRAM : 4.8395
conclusion: compute bound 1 l3boundness 1 ramboundness 1

-----------------------
--------------3
overflow 0.359289
Socket : 1
socket 1 5549757698 4464848626
Uncorefreq: 3.0196e+09
18 937969408.000000 1012601664.000000 831779776.000000
19 1875984640.000000 2025202176.000000 1663558784.000000
20 2814284032.000000 3037801472.000000 2495336704.000000
21 3753397504.000000 4050401280.000000 3327115264.000000
22 4691237888.000000 5063001088.000000 4158893824.000000
23 5629149184.000000 6075601408.000000 4990672384.000000
24 6567012864.000000 7088201216.000000 5822450688.000000
25 7505252352.000000 8100802560.000000 6654230016.000000
26 8443440128.000000 9113403392.000000 7486009856.000000
27 9381317632.000000 10126004224.000000 8317789184.000000
28 10319537152.000000 11138605056.000000 9149568000.000000
29 11257739264.000000 12151205888.000000 9981346816.000000
30 12195954688.000000 13163806720.000000 10813125632.000000
31 13134191616.000000 14176405504.000000 11644903424.000000
32 14072432640.000000 15189007360.000000 12476683264.000000
33 15010592768.000000 16201609216.000000 13308463104.000000
34 15948854272.000000 17214208000.000000 14140240896.000000
35 16887533568.000000 18226808832.000000 14972019712.000000
coreFreq : 2.6783e+09
clockTime : 3.7808e-01
wallTime : 3.5929e-01
insPerSec : 4.4667e+10
cycles : 18226808832.000000
L2 stalld : 1657099008.000000
 L2 stall rate : 0.090915
 Ldm stalld : 4054774272.000000
LDM stall rate : 0.222462
PKG Energy: 0.000000
 PKG Power : 0.000000
DRAM Energy: 0.000000
 Power : 0.000000
stallL2Rate : 0.0909
stallLDMRate : 0.2225
stallL2Cycles : 1657099008.0000
stallLDMCycles : 4054774272.0000
idealInsPerSecL2 : 4.9134e+10
idealInsPerSecLDM : 5.7446e+10
L3 volum: 3.0818e+07
RAM volum: 7.0103e+06
lowerBound : 18
 upperBound : 15
full L3 BW : 1.1323e+11
 fullRAMBW: 1.1660e+10
Latency L3 : 53.7704
 DRAM : 578.4020
Bandwidth Usage L3 : 0.0008
, Bandwidth usage DRAM : 0.0017
realIntensityL3 : 547.9755
 roofIntensityL3 : 0.4339
realIntensityRAM : 2408.9587
 roofIntensityRAM : 4.9269
conclusion: compute bound 1 l3boundness 1 ramboundness 1

-----------------------
--------------4
overflow 0.359476
Socket : 1
socket 1 6635274694 5549757698
Uncorefreq: 3.0197e+09
18 938378944.000000 1013133440.000000 832216704.000000
19 1877875712.000000 2026268544.000000 1664434816.000000
20 2816574720.000000 3039404032.000000 2496653312.000000
21 3755030016.000000 4052540672.000000 3328872704.000000
22 4693457408.000000 5065675776.000000 4161090816.000000
23 5631686144.000000 6078812160.000000 4993310208.000000
24 6570076672.000000 7091949056.000000 5825529856.000000
25 7508642304.000000 8105086464.000000 6657750016.000000
26 8447223808.000000 9118224384.000000 7489970176.000000
27 9385234432.000000 10131361792.000000 8322190336.000000
28 10323805184.000000 11144500224.000000 9154411520.000000
29 11262233600.000000 12157638656.000000 9986632704.000000
30 12200797184.000000 13170777088.000000 10818852864.000000
31 13139292160.000000 14183915520.000000 11651074048.000000
32 14077921280.000000 15197051904.000000 12483293184.000000
33 15016441856.000000 16210190336.000000 13315514368.000000
34 15955035136.000000 17223329792.000000 14147735552.000000
35 16893974528.000000 18236471296.000000 14979958784.000000
coreFreq : 2.6783e+09
clockTime : 3.7828e-01
wallTime : 3.5948e-01
insPerSec : 4.4660e+10
cycles : 18236471296.000000
L2 stalld : 1664077696.000000
 L2 stall rate : 0.091250
 Ldm stalld : 4057335040.000000
LDM stall rate : 0.222485
PKG Energy: 0.000000
 PKG Power : 0.000000
DRAM Energy: 0.000000
 Power : 0.000000
stallL2Rate : 0.0912
stallLDMRate : 0.2225
stallL2Cycles : 1664077696.0000
stallLDMCycles : 4057335040.0000
idealInsPerSecL2 : 4.9144e+10
idealInsPerSecLDM : 5.7439e+10
L3 volum: 3.1115e+07
RAM volum: 7.7284e+06
lowerBound : 18
 upperBound : 15
full L3 BW : 1.1365e+11
 fullRAMBW: 1.1733e+10
Latency L3 : 53.4815
 DRAM : 524.9871
Bandwidth Usage L3 : 0.0008
, Bandwidth usage DRAM : 0.0018
realIntensityL3 : 542.9526
 roofIntensityL3 : 0.4324
realIntensityRAM : 2185.9465
 roofIntensityRAM : 4.8954
conclusion: compute bound 1 l3boundness 1 ramboundness 1

-----------------------
--------------5
overflow 0.359383
Socket : 1
socket 1 7720090458 6635274694
Uncorefreq: 3.0185e+09
18 937987392.000000 1012513024.000000 831707392.000000
19 1876166016.000000 2025024256.000000 1663412992.000000
20 2814451200.000000 3037534208.000000 2495117568.000000
21 3752642048.000000 4050043392.000000 3326821632.000000
22 4690555392.000000 5062553088.000000 4158525952.000000
23 5628361216.000000 6075060736.000000 4990228480.000000
24 6566309376.000000 7087568384.000000 5821931008.000000
25 7504532992.000000 8100074496.000000 6653632512.000000
26 8442746368.000000 9112581120.000000 7485334528.000000
27 9380829184.000000 10125086720.000000 8317036032.000000
28 10318976000.000000 11137593344.000000 9148738560.000000
29 11257116672.000000 12150099968.000000 9980439552.000000
30 12195315712.000000 13162606592.000000 10812141568.000000
31 13133218816.000000 14175114240.000000 11643843584.000000
32 14071392256.000000 15187620864.000000 12475545600.000000
33 15009510400.000000 16200125440.000000 13307245568.000000
34 15947614208.000000 17212628992.000000 14138945536.000000
35 16886184960.000000 18225131520.000000 14970644480.000000
coreFreq : 2.6783e+09
clockTime : 3.7805e-01
wallTime : 3.5938e-01
insPerSec : 4.4667e+10
cycles : 18225131520.000000
L2 stalld : 1646577664.000000
 L2 stall rate : 0.090347
 Ldm stalld : 4054213120.000000
LDM stall rate : 0.222452
PKG Energy: 0.000000
 PKG Power : 0.000000
DRAM Energy: 0.000000
 Power : 0.000000
stallL2Rate : 0.0903
stallLDMRate : 0.2225
stallL2Cycles : 1646577664.0000
stallLDMCycles : 4054213120.0000
idealInsPerSecL2 : 4.9103e+10
idealInsPerSecLDM : 5.7446e+10
L3 volum: 2.0893e+07
RAM volum: 4.7539e+06
lowerBound : 18
 upperBound : 15
full L3 BW : 1.0966e+11
 fullRAMBW: 1.1037e+10
Latency L3 : 78.8086
 DRAM : 852.8148
Bandwidth Usage L3 : 0.0005
, Bandwidth usage DRAM : 0.0012
realIntensityL3 : 808.2076
 roofIntensityL3 : 0.4478
realIntensityRAM : 3552.0549
 roofIntensityRAM : 5.2048
conclusion: compute bound 1 l3boundness 1 ramboundness 1

-----------------------
--------------6
overflow 0.359303
Socket : 1
socket 1 8804932676 7720090458
Uncorefreq: 3.0193e+09
18 937951552.000000 1012511936.000000 831705984.000000
19 1876049152.000000 2025024000.000000 1663412224.000000
20 2814275328.000000 3037536512.000000 2495118848.000000
21 3752247808.000000 4050049024.000000 3326825472.000000
22 4689602560.000000 5062563328.000000 4158533632.000000
23 5627376128.000000 6075077632.000000 4990241792.000000
24 6565374976.000000 7087592448.000000 5821950464.000000
25 7503587328.000000 8100106240.000000 6653658112.000000
26 8441636864.000000 9112620032.000000 7485365760.000000
27 9379441664.000000 10125135872.000000 8317075456.000000
28 10317540352.000000 11137650688.000000 9148784640.000000
29 11255734272.000000 12150166528.000000 9980493824.000000
30 12193895424.000000 13162683392.000000 10812204032.000000
31 13132038144.000000 14175199232.000000 11643913216.000000
32 14070192128.000000 15187718144.000000 12475624448.000000
33 15008336896.000000 16200236032.000000 13307335680.000000
34 15946577920.000000 17212755968.000000 14139048960.000000
35 16885193728.000000 18225276928.000000 14970762240.000000
coreFreq : 2.6783e+09
clockTime : 3.7805e-01
wallTime : 3.5930e-01
insPerSec : 4.4664e+10
cycles : 18225276928.000000
L2 stalld : 1830650240.000000
 L2 stall rate : 0.100446
 Ldm stalld : 4054491392.000000
LDM stall rate : 0.222465
PKG Energy: 0.000000
 PKG Power : 0.000000
DRAM Energy: 0.000000
 Power : 0.000000
stallL2Rate : 0.1004
stallLDMRate : 0.2225
stallL2Cycles : 1830650240.0000
stallLDMCycles : 4054491392.0000
idealInsPerSecL2 : 4.9651e+10
idealInsPerSecLDM : 5.7443e+10
L3 volum: 2.3727e+07
RAM volum: 5.3703e+06
lowerBound : 18
 upperBound : 15
full L3 BW : 1.1220e+11
 fullRAMBW: 1.1481e+10
Latency L3 : 77.1550
 DRAM : 754.9836
Bandwidth Usage L3 : 0.0006
, Bandwidth usage DRAM : 0.0013
realIntensityL3 : 711.6473
 roofIntensityL3 : 0.4425
realIntensityRAM : 3144.1785
 roofIntensityRAM : 5.0035
conclusion: compute bound 1 l3boundness 1 ramboundness 1

-----------------------
--------------7
overflow 0.359451
Socket : 1
socket 1 9890791586 8804932676
Uncorefreq: 3.0209e+09
18 938755968.000000 1013437184.000000 832466560.000000
19 1877465600.000000 2026926848.000000 1664975872.000000
20 2816456704.000000 3040415488.000000 2497484288.000000
21 3756130048.000000 4053902336.000000 3329991168.000000
22 4694882304.000000 5067386368.000000 4162495744.000000
23 5633516544.000000 6080869376.000000 4994999808.000000
24 6572370432.000000 7094350848.000000 5827502080.000000
25 7511312384.000000 8107831296.000000 6660003840.000000
26 8450078208.000000 9121310720.000000 7492505088.000000
27 9389047808.000000 10134787072.000000 8325003264.000000
28 10327992320.000000 11148261376.000000 9157500928.000000
29 11333477376.000000 12161703936.000000 9989971968.000000
30 12272394240.000000 13175170048.000000 10822462464.000000
31 13211260928.000000 14188635136.000000 11654951936.000000
32 14150224896.000000 15202097152.000000 12487438336.000000
33 15089117184.000000 16215557120.000000 13319922688.000000
34 16028090368.000000 17229012992.000000 14152404992.000000
35 16967519232.000000 18242467840.000000 14984885248.000000
coreFreq : 2.6783e+09
clockTime : 3.7841e-01
wallTime : 3.5945e-01
insPerSec : 4.4840e+10
cycles : 18242467840.000000
L2 stalld : 2325691904.000000
 L2 stall rate : 0.127488
 Ldm stalld : 4027630080.000000
LDM stall rate : 0.220783
PKG Energy: 0.000000
 PKG Power : 0.000000
DRAM Energy: 0.000000
 Power : 0.000000
stallL2Rate : 0.1275
stallLDMRate : 0.2208
stallL2Cycles : 2325691904.0000
stallLDMCycles : 4027630080.0000
idealInsPerSecL2 : 5.1391e+10
idealInsPerSecLDM : 5.7544e+10
L3 volum: 3.0737e+07
RAM volum: 7.7402e+06
lowerBound : 18
 upperBound : 15
full L3 BW : 1.1759e+11
 fullRAMBW: 1.2423e+10
Latency L3 : 75.6650
 DRAM : 520.3549
Bandwidth Usage L3 : 0.0007
, Bandwidth usage DRAM : 0.0017
realIntensityL3 : 552.0280
 roofIntensityL3 : 0.4370
realIntensityRAM : 2192.1406
 roofIntensityRAM : 4.6321
conclusion: compute bound 1 l3boundness 1 ramboundness 1

-----------------------
--------------8
overflow 0.359331
Socket : 1
socket 1 10974305790 9890791586
Uncorefreq: 3.0154e+09
18 937091200.000000 1011514304.000000 830886464.000000
19 1874307584.000000 2022972928.000000 1661727616.000000
20 2811568384.000000 3034429184.000000 2492566528.000000
21 3748805888.000000 4045882368.000000 3323403008.000000
22 4685746688.000000 5057333248.000000 4154237696.000000
23 5622460416.000000 6068782080.000000 4985070592.000000
24 6559467520.000000 7080228352.000000 5815901696.000000
25 7496591872.000000 8091672064.000000 6646730240.000000
26 8433809408.000000 9103111168.000000 7477555200.000000
27 9370985472.000000 10114548736.000000 8308378624.000000
28 10308052992.000000 11125983232.000000 9139200000.000000
29 11313527808.000000 12137259008.000000 9969891328.000000
30 12250630144.000000 13148689408.000000 10800708608.000000
31 13187616768.000000 14160116736.000000 11631523840.000000
32 14124817408.000000 15171542016.000000 12462337024.000000
33 15061921792.000000 16182964224.000000 13293148160.000000
34 15999112192.000000 17194385408.000000 14123958272.000000
35 16937505792.000000 18205804544.000000 14954767360.000000
coreFreq : 2.6783e+09
clockTime : 3.7764e-01
wallTime : 3.5933e-01
insPerSec : 4.4850e+10
cycles : 18205804544.000000
L2 stalld : 2137187968.000000
 L2 stall rate : 0.117390
 Ldm stalld : 4018631168.000000
LDM stall rate : 0.220734
PKG Energy: 0.000000
 PKG Power : 0.000000
DRAM Energy: 0.000000
 Power : 0.000000
stallL2Rate : 0.1174
stallLDMRate : 0.2207
stallL2Cycles : 2137187968.0000
stallLDMCycles : 4018631168.0000
idealInsPerSecL2 : 5.0816e+10
idealInsPerSecLDM : 5.7555e+10
L3 volum: 3.9000e+07
RAM volum: 8.1688e+06
lowerBound : 18
 upperBound : 15
full L3 BW : 9.8822e+10
 fullRAMBW: 9.1429e+09
Latency L3 : 54.7992
 DRAM : 491.9468
Bandwidth Usage L3 : 0.0011
, Bandwidth usage DRAM : 0.0025
realIntensityL3 : 434.2907
 roofIntensityL3 : 0.5142
realIntensityRAM : 2073.4307
 roofIntensityRAM : 6.2950
conclusion: compute bound 1 l3boundness 1 ramboundness 1

-----------------------
--------------9
overflow 0.359404
Socket : 1
socket 1 12058927544 10974305790
Uncorefreq: 3.0178e+09
18 937883072.000000 1012319040.000000 831547776.000000
19 1875956736.000000 2024637440.000000 1663095040.000000
20 2814010368.000000 3036955648.000000 2494642176.000000
21 3752128512.000000 4049273088.000000 3326188800.000000
22 4689758720.000000 5061590528.000000 4157735168.000000
23 5627472384.000000 6073907200.000000 4989281280.000000
24 6565303808.000000 7086224384.000000 5820827136.000000
25 7503398400.000000 8098540544.000000 6652372992.000000
26 8441445888.000000 9110856704.000000 7483918336.000000
27 9379300352.000000 10123172864.000000 8315464192.000000
28 10317330432.000000 11135489024.000000 9147010048.000000
29 11323555840.000000 12147615744.000000 9978400768.000000
30 12261627904.000000 13159931904.000000 10809946112.000000
31 13199480832.000000 14172248064.000000 11641491456.000000
32 14137503744.000000 15184563200.000000 12473036800.000000
33 15075442688.000000 16196879360.000000 13304582144.000000
34 16013471744.000000 17209194496.000000 14136126464.000000
35 16952445952.000000 18221508608.000000 14967670784.000000
coreFreq : 2.6783e+09
clockTime : 3.7797e-01
wallTime : 3.5940e-01
insPerSec : 4.4851e+10
cycles : 18221508608.000000
L2 stalld : 2300731392.000000
 L2 stall rate : 0.126265
 Ldm stalld : 4021766400.000000
LDM stall rate : 0.220715
PKG Energy: 0.000000
 PKG Power : 0.000000
DRAM Energy: 0.000000
 Power : 0.000000
stallL2Rate : 0.1263
stallLDMRate : 0.2207
stallL2Cycles : 2300731392.0000
stallLDMCycles : 4021766400.0000
idealInsPerSecL2 : 5.1333e+10
idealInsPerSecLDM : 5.7554e+10
L3 volum: 3.5952e+07
RAM volum: 6.7503e+06
lowerBound : 18
 upperBound : 15
full L3 BW : 1.0721e+11
 fullRAMBW: 1.0609e+10
Latency L3 : 63.9951
 DRAM : 595.7932
Bandwidth Usage L3 : 0.0009
, Bandwidth usage DRAM : 0.0018
realIntensityL3 : 471.5342
 roofIntensityL3 : 0.4788
realIntensityRAM : 2511.3723
 roofIntensityRAM : 5.4250
conclusion: compute bound 1 l3boundness 1 ramboundness 1

-----------------------
--------------10
overflow 0.359522
Socket : 1
socket 1 13143929982 12058927544
Uncorefreq: 3.0179e+09
18 938113984.000000 1012662720.000000 831830080.000000
19 1876410880.000000 2025326336.000000 1663660800.000000
20 2814725888.000000 3037989888.000000 2495491584.000000
21 3752945920.000000 4050654464.000000 3327323136.000000
22 4690956800.000000 5063319040.000000 4159154688.000000
23 5628866048.000000 6075983360.000000 4990986240.000000
24 6566927872.000000 7088648192.000000 5822818304.000000
25 7505195520.000000 8101313536.000000 6654650880.000000
26 8443435520.000000 9113979904.000000 7486483968.000000
27 9381695488.000000 10126646272.000000 8318316544.000000
28 10319912960.000000 11139312640.000000 9150149632.000000
29 11326162944.000000 12151793664.000000 9981831168.000000
30 12264411136.000000 13164460032.000000 10813664256.000000
31 13202617344.000000 14177126400.000000 11645497344.000000
32 14140896256.000000 15189792768.000000 12477330432.000000
33 15079047168.000000 16202459136.000000 13309163520.000000
34 16017334272.000000 17215125504.000000 14140996608.000000
35 16955866112.000000 18227789824.000000 14972828672.000000
coreFreq : 2.6783e+09
clockTime : 3.7810e-01
wallTime : 3.5952e-01
insPerSec : 4.4845e+10
cycles : 18227789824.000000
L2 stalld : 1928754048.000000
 L2 stall rate : 0.105814
 Ldm stalld : 4024926464.000000
LDM stall rate : 0.220813
PKG Energy: 0.000000
 PKG Power : 0.000000
DRAM Energy: 0.000000
 Power : 0.000000
stallL2Rate : 0.1058
stallLDMRate : 0.2208
stallL2Cycles : 1928754048.0000
stallLDMCycles : 4024926464.0000
idealInsPerSecL2 : 5.0152e+10
idealInsPerSecLDM : 5.7553e+10
L3 volum: 3.0825e+07
RAM volum: 5.6391e+06
lowerBound : 18
 upperBound : 15
full L3 BW : 1.0747e+11
 fullRAMBW: 1.0654e+10
Latency L3 : 62.5716
 DRAM : 713.7528
Bandwidth Usage L3 : 0.0008
, Bandwidth usage DRAM : 0.0015
realIntensityL3 : 550.0728
 roofIntensityL3 : 0.4667
realIntensityRAM : 3006.8369
 roofIntensityRAM : 5.4020
conclusion: compute bound 1 l3boundness 1 ramboundness 1

-----------------------
--------------11
overflow 0.359380
Socket : 1
socket 1 14228575164 13143929982
Uncorefreq: 3.0181e+09
18 937952256.000000 1012336640.000000 831562240.000000
19 1876038144.000000 2024672512.000000 1663123968.000000
20 2814147072.000000 3037008640.000000 2494685696.000000
21 3752231936.000000 4049344768.000000 3326247424.000000
22 4689883136.000000 5061681152.000000 4157809408.000000
23 5627484160.000000 6074017792.000000 4989371392.000000
24 6565334016.000000 7086353920.000000 5820933120.000000
25 7503406080.000000 8098690048.000000 6652494848.000000
26 8441511936.000000 9111026688.000000 7484056576.000000
27 9379620864.000000 10123362304.000000 8315618304.000000
28 10317652992.000000 11135697920.000000 9147180032.000000
29 11323942912.000000 12147844096.000000 9978585088.000000
30 12261962752.000000 13160179712.000000 10810146816.000000
31 13199844352.000000 14172515328.000000 11641708544.000000
32 14137850880.000000 15184851968.000000 12473270272.000000
33 15075818496.000000 16197188608.000000 13304833024.000000
34 16013840384.000000 17209526272.000000 14136395776.000000
35 16952259584.000000 18221864960.000000 14967959552.000000
coreFreq : 2.6783e+09
clockTime : 3.7798e-01
wallTime : 3.5938e-01
insPerSec : 4.4850e+10
cycles : 18221864960.000000
L2 stalld : 1923795200.000000
 L2 stall rate : 0.105576
 Ldm stalld : 4021813248.000000
LDM stall rate : 0.220714
PKG Energy: 0.000000
 PKG Power : 0.000000
DRAM Energy: 0.000000
 Power : 0.000000
stallL2Rate : 0.1056
stallLDMRate : 0.2207
stallL2Cycles : 1923795200.0000
stallLDMCycles : 4021813248.0000
idealInsPerSecL2 : 5.0144e+10
idealInsPerSecLDM : 5.7552e+10
L3 volum: 3.0251e+07
RAM volum: 4.9530e+06
lowerBound : 18
 upperBound : 15
full L3 BW : 1.0812e+11
 fullRAMBW: 1.0768e+10
Latency L3 : 63.5946
 DRAM : 811.9915
Bandwidth Usage L3 : 0.0008
, Bandwidth usage DRAM : 0.0013
realIntensityL3 : 560.3878
 roofIntensityL3 : 0.4638
realIntensityRAM : 3422.6079
 roofIntensityRAM : 5.3447
conclusion: compute bound 1 l3boundness 1 ramboundness 1

-----------------------
--------------12

pi is approximately = 662.51701500969465996604
Error               = 659.37542240969469276024
Energy of socket 1 : PKG: 0.000000 DRAM 0.000000

------------------------------------------------------------------------------------------------------------

* Run stream and run sampling

init freeze 700 80000000
init unfreeze 700 20000000
Node object is created
registed sampling event
overflow 0.411982
Socket : 1
socket 1 1064646636 362446
Uncorefreq: 2.5833e+09
18 967922880.000000 1050256512.000000 944892544.000000
19 1938344960.000000 2103086464.000000 1889699328.000000
20 2906357760.000000 3153253120.000000 2834394624.000000
21 3869777920.000000 4198586880.000000 3779105536.000000
22 4839990272.000000 5249119232.000000 4715609088.000000
23 5881013760.000000 6301851648.000000 5660178432.000000
24 6843840512.000000 7346643456.000000 6603807232.000000
25 7807650304.000000 8391823872.000000 7548179456.000000
26 8772841472.000000 9438437376.000000 8492425216.000000
27 9776381952.000000 10527353856.000000 9436036096.000000
28 10747983872.000000 11581377536.000000 10380203008.000000
29 11718199296.000000 12632558592.000000 11324567552.000000
30 12692153344.000000 13689478144.000000 12268617728.000000
31 13659225088.000000 14738557952.000000 13211802624.000000
32 14626827264.000000 15788311552.000000 14155555840.000000
33 15595493376.000000 16839176192.000000 15099261952.000000
34 16560523264.000000 17885978624.000000 16042577920.000000
35 17537447936.000000 18944274432.000000 16979020800.000000
coreFreq : 2.4546e+09
clockTime : 4.2876e-01
wallTime : 4.1198e-01
insPerSec : 4.0903e+10
cycles : 18944274432.000000
L2 stalld : 1699803008.000000
 L2 stall rate : 0.089726
 Ldm stalld : 4185313792.000000
LDM stall rate : 0.220928
PKG Energy: 0.000000
 PKG Power : 0.000000
DRAM Energy: 0.000000
 Power : 0.000000
stallL2Rate : 0.0897
stallLDMRate : 0.2209
stallL2Cycles : 1699803008.0000
stallLDMCycles : 4185313792.0000
idealInsPerSecL2 : 4.4934e+10
idealInsPerSecLDM : 5.2502e+10
L3 volum: 5.5596e+07
RAM volum: 1.2283e+07
lowerBound : 13
 upperBound : 14
full L3 BW : 3.7750e+11
 fullRAMBW: 5.8783e+10
Latency L3 : 30.5744
 DRAM : 340.7401
Bandwidth Usage L3 : 0.0004
, Bandwidth usage DRAM : 0.0005
realIntensityL3 : 315.4464
 roofIntensityL3 : 0.1190
realIntensityRAM : 1427.7812
 roofIntensityRAM : 0.8931
conclusion: compute bound 1 l3boundness 1 ramboundness 1

-----------------------
--------------0
overflow 0.360304
Socket : 1
socket 1 2153621918 1064646636
Uncorefreq: 3.0224e+09
18 941714688.000000 1016513280.000000 834992960.000000
19 1883650176.000000 2033024128.000000 1669984000.000000
20 2825589760.000000 3049533440.000000 2504973824.000000
21 3767282944.000000 4066041856.000000 3339962880.000000
22 4708824064.000000 5082549760.000000 4174951680.000000
23 5720809984.000000 6099057664.000000 5009939968.000000
24 6662507008.000000 7115564544.000000 5844927488.000000
25 7604361216.000000 8132070400.000000 6679913984.000000
26 8546290688.000000 9148574720.000000 7514899968.000000
27 9488207872.000000 10165079040.000000 8349885440.000000
28 10430170112.000000 11181581312.000000 9184869376.000000
29 11372116992.000000 12198081536.000000 10019852288.000000
30 12313827328.000000 13214580736.000000 10854834176.000000
31 13255716864.000000 14231078912.000000 11689815040.000000
32 14197682176.000000 15247575040.000000 12524793856.000000
33 15139584000.000000 16264069120.000000 13359771648.000000
34 16080916480.000000 17280563200.000000 14194748416.000000
35 17024630784.000000 18297057280.000000 15029725184.000000
coreFreq : 2.6783e+09
clockTime : 3.7954e-01
wallTime : 3.6030e-01
insPerSec : 4.4856e+10
cycles : 18297057280.000000
L2 stalld : 2279505408.000000
 L2 stall rate : 0.124583
 Ldm stalld : 4039034624.000000
LDM stall rate : 0.220748
PKG Energy: 0.000000
 PKG Power : 0.000000
DRAM Energy: 0.000000
 Power : 0.000000
stallL2Rate : 0.1246
stallLDMRate : 0.2207
stallL2Cycles : 2279505408.0000
stallLDMCycles : 4039034624.0000
idealInsPerSecL2 : 5.1240e+10
idealInsPerSecLDM : 5.7563e+10
L3 volum: 3.8064e+07
RAM volum: 7.0941e+06
lowerBound : 18
 upperBound : 15
full L3 BW : 1.2269e+11
 fullRAMBW: 1.3314e+10
Latency L3 : 59.8862
 DRAM : 569.3528
Bandwidth Usage L3 : 0.0009
, Bandwidth usage DRAM : 0.0015
realIntensityL3 : 447.2641
 roofIntensityL3 : 0.4176
realIntensityRAM : 2399.8364
 roofIntensityRAM : 4.3236
conclusion: compute bound 1 l3boundness 1 ramboundness 1

-----------------------
--------------1
overflow 0.361246
Socket : 1
socket 1 3244461142 2153621918
Uncorefreq: 3.0197e+09
18 942968960.000000 1018110272.000000 836304896.000000
19 1886110848.000000 2036221056.000000 1672610304.000000
20 2829245440.000000 3054332672.000000 2508916224.000000
21 3772345856.000000 4072444416.000000 3345222144.000000
22 4715447296.000000 5090554880.000000 4181527296.000000
23 5728770560.000000 6108665856.000000 5017832448.000000
24 6671674880.000000 7126776832.000000 5854137856.000000
25 7614816768.000000 8144888320.000000 6690443776.000000
26 8558011904.000000 9162999808.000000 7526749184.000000
27 9501103104.000000 10181110784.000000 8363055104.000000
28 10444253184.000000 11199222784.000000 9199361024.000000
29 11387454464.000000 12217334784.000000 10035666944.000000
30 12330443776.000000 13235446784.000000 10871972864.000000
31 13273567232.000000 14253558784.000000 11708278784.000000
32 14216711168.000000 15271671808.000000 12544585728.000000
33 15159856128.000000 16289784832.000000 13380892672.000000
34 16102377472.000000 17307897856.000000 14217199616.000000
35 17045734400.000000 18326009856.000000 15053505536.000000
coreFreq : 2.6783e+09
clockTime : 3.8014e-01
wallTime : 3.6125e-01
insPerSec : 4.4841e+10
cycles : 18326009856.000000
L2 stalld : 2326879744.000000
 L2 stall rate : 0.126971
 Ldm stalld : 4046722048.000000
LDM stall rate : 0.220819
PKG Energy: 0.000000
 PKG Power : 0.000000
DRAM Energy: 0.000000
 Power : 0.000000
stallL2Rate : 0.1270
stallLDMRate : 0.2208
stallL2Cycles : 2326879744.0000
stallLDMCycles : 4046722048.0000
idealInsPerSecL2 : 5.1362e+10
idealInsPerSecLDM : 5.7549e+10
L3 volum: 3.4953e+07
RAM volum: 6.5496e+06
lowerBound : 18
 upperBound : 15
full L3 BW : 1.1343e+11
 fullRAMBW: 1.1696e+10
Latency L3 : 66.5713
 DRAM : 617.8549
Bandwidth Usage L3 : 0.0009
, Bandwidth usage DRAM : 0.0016
realIntensityL3 : 487.6729
 roofIntensityL3 : 0.4528
realIntensityRAM : 2602.5483
 roofIntensityRAM : 4.9204
conclusion: compute bound 1 l3boundness 1 ramboundness 1

-----------------------
--------------2
overflow 0.360600
Socket : 1
socket 1 4333207582 3244461142
Uncorefreq: 3.0193e+09
18 941475520.000000 1016173952.000000 834714304.000000
19 1883122688.000000 2032347520.000000 1669428224.000000
20 2824803840.000000 3048519936.000000 2504141312.000000
21 3766433280.000000 4064691968.000000 3338853888.000000
22 4708047360.000000 5080863232.000000 4173565952.000000
23 5720133632.000000 6097034240.000000 5008278016.000000
24 6661588992.000000 7113204736.000000 5842989568.000000
25 7603089408.000000 8129374720.000000 6677700608.000000
26 8544751616.000000 9145544704.000000 7512411648.000000
27 9486325760.000000 10161714176.000000 8347121664.000000
28 10427994112.000000 11177882624.000000 9181831168.000000
29 11369383936.000000 12194051072.000000 10016540672.000000
30 12310825984.000000 13210219520.000000 10851250176.000000
31 13252442112.000000 14226386944.000000 11685959680.000000
32 14194038784.000000 15242555392.000000 12520669184.000000
33 15135669248.000000 16258721792.000000 13355377664.000000
34 16076851200.000000 17274888192.000000 14190086144.000000
35 17018882048.000000 18291056640.000000 15024795648.000000
coreFreq : 2.6783e+09
clockTime : 3.7941e-01
wallTime : 3.6060e-01
insPerSec : 4.4856e+10
cycles : 18291056640.000000
L2 stalld : 2155913728.000000
 L2 stall rate : 0.117867
 Ldm stalld : 4037798912.000000
LDM stall rate : 0.220753
PKG Energy: 0.000000
 PKG Power : 0.000000
DRAM Energy: 0.000000
 Power : 0.000000
stallL2Rate : 0.1179
stallLDMRate : 0.2208
stallL2Cycles : 2155913728.0000
stallLDMCycles : 4037798912.0000
idealInsPerSecL2 : 5.0849e+10
idealInsPerSecLDM : 5.7563e+10
L3 volum: 2.9767e+07
RAM volum: 5.5249e+06
lowerBound : 18
 upperBound : 15
full L3 BW : 1.1209e+11
 fullRAMBW: 1.1462e+10
Latency L3 : 72.4273
 DRAM : 730.8413
Bandwidth Usage L3 : 0.0007
, Bandwidth usage DRAM : 0.0013
realIntensityL3 : 571.7444
 roofIntensityL3 : 0.4536
realIntensityRAM : 3080.4165
 roofIntensityRAM : 5.0220
conclusion: compute bound 1 l3boundness 1 ramboundness 1

-----------------------
--------------3
overflow 0.361232
Socket : 1
socket 1 5424170926 4333207582
Uncorefreq: 3.0201e+09
18 943074688.000000 1018098688.000000 836295488.000000
19 1812025600.000000 2036204800.000000 1672597248.000000
20 2755444480.000000 3054316800.000000 2508903680.000000
21 3698548224.000000 4072433664.000000 3345213952.000000
22 4641487872.000000 5090555392.000000 4181528576.000000
23 5655238656.000000 6108681728.000000 5017846784.000000
24 6598555136.000000 7126812160.000000 5854168064.000000
25 7541864960.000000 8144946688.000000 6690492928.000000
26 8484932096.000000 9163087872.000000 7526822912.000000
27 9428260864.000000 10181232640.000000 8363156480.000000
28 10371526656.000000 11199383552.000000 9199494144.000000
29 11314226176.000000 12217538560.000000 10035835904.000000
30 12257466368.000000 13235697664.000000 10872181760.000000
31 13200817152.000000 14253860864.000000 11708530688.000000
32 14144220160.000000 15272028160.000000 12544882688.000000
33 15087571968.000000 16290200576.000000 13381238784.000000
34 16030527488.000000 17308377088.000000 14217597952.000000
35 16974319616.000000 18326558720.000000 15053961216.000000
coreFreq : 2.6783e+09
clockTime : 3.8015e-01
wallTime : 3.6123e-01
insPerSec : 4.4652e+10
cycles : 18326558720.000000
L2 stalld : 1784112768.000000
 L2 stall rate : 0.097351
 Ldm stalld : 4008678144.000000
LDM stall rate : 0.218736
PKG Energy: 0.000000
 PKG Power : 0.000000
DRAM Energy: 0.000000
 Power : 0.000000
stallL2Rate : 0.0974
stallLDMRate : 0.2187
stallL2Cycles : 1784112768.0000
stallLDMCycles : 4008678144.0000
idealInsPerSecL2 : 4.9467e+10
idealInsPerSecLDM : 5.7153e+10
L3 volum: 3.2264e+08
RAM volum: 8.7162e+07
lowerBound : 18
 upperBound : 15
full L3 BW : 1.1499e+11
 fullRAMBW: 1.1969e+10
Latency L3 : 5.5297
 DRAM : 45.9910
Bandwidth Usage L3 : 0.0078
, Bandwidth usage DRAM : 0.0202
realIntensityL3 : 52.6107
 roofIntensityL3 : 0.4302
realIntensityRAM : 194.7441
 roofIntensityRAM : 4.7751
conclusion: compute bound 1 l3boundness 1 ramboundness 1

-----------------------
--------------4
overflow 0.362927
Socket : 1
socket 1 6520371406 5424170926
Uncorefreq: 3.0204e+09
18 947553664.000000 1023118592.000000 840418880.000000
19 1986835712.000000 2046236416.000000 1680837120.000000
20 2934633472.000000 3069354240.000000 2521255424.000000
21 3882524672.000000 4092471808.000000 3361673472.000000
22 4830293504.000000 5115589120.000000 4202091264.000000
23 5847349760.000000 6138705920.000000 5042508800.000000
24 6795021312.000000 7161823232.000000 5882926592.000000
25 7742742016.000000 8184941568.000000 6723344896.000000
26 8690240512.000000 9208058880.000000 7563762688.000000
27 9638051840.000000 10231177216.000000 8404180992.000000
28 10585869312.000000 11254295552.000000 9244599296.000000
29 11533016064.000000 12277413888.000000 10085018624.000000
30 12480702464.000000 13300534272.000000 10925438976.000000
31 13431835648.000000 14323654656.000000 11765859328.000000
32 14379695104.000000 15346776064.000000 12606279680.000000
33 15327663104.000000 16369898496.000000 13446701056.000000
34 16275002368.000000 17393020928.000000 14287123456.000000
35 17223012352.000000 18416144384.000000 15127545856.000000
coreFreq : 2.6783e+09
clockTime : 3.8201e-01
wallTime : 3.6293e-01
insPerSec : 4.5085e+10
cycles : 18416144384.000000
L2 stalld : 975567936.000000
 L2 stall rate : 0.052974
 Ldm stalld : 3977848320.000000
LDM stall rate : 0.215998
PKG Energy: 0.000000
 PKG Power : 0.000000
DRAM Energy: 0.000000
 Power : 0.000000
stallL2Rate : 0.0530
stallLDMRate : 0.2160
stallL2Cycles : 975567936.0000
stallLDMCycles : 3977848320.0000
idealInsPerSecL2 : 4.7607e+10
idealInsPerSecLDM : 5.7507e+10
L3 volum: 1.3253e+09
RAM volum: 8.5448e+08
lowerBound : 18
 upperBound : 15
full L3 BW : 1.1612e+11
 fullRAMBW: 1.2165e+10
Latency L3 : 0.7361
 DRAM : 4.6553
Bandwidth Usage L3 : 0.0314
, Bandwidth usage DRAM : 0.1935
realIntensityL3 : 12.9958
 roofIntensityL3 : 0.4100
realIntensityRAM : 20.1561
 roofIntensityRAM : 4.7272
conclusion: compute bound 1 l3boundness 1 ramboundness 1

-----------------------
--------------5
overflow 0.362080
Socket : 1
socket 1 7613859964 6520371406
Uncorefreq: 3.0200e+09
18 944616192.000000 1020579392.000000 838333056.000000
19 1916440576.000000 2041158400.000000 1676665728.000000
20 2866184960.000000 3061739008.000000 2514999808.000000
21 3811631104.000000 4082320128.000000 3353334272.000000
22 4755247616.000000 5102902272.000000 4191669504.000000
23 5768078848.000000 6123485184.000000 5030005248.000000
24 6713314816.000000 7144068096.000000 5868341248.000000
25 7658954240.000000 8164651008.000000 6706677248.000000
26 8604564480.000000 9185234944.000000 7545013760.000000
27 9550033920.000000 10205817856.000000 8383349760.000000
28 10495780864.000000 11226399744.000000 9221685248.000000
29 11595324416.000000 12246983680.000000 10060021760.000000
30 12540750848.000000 13267567616.000000 10898358272.000000
31 13486373888.000000 14288151552.000000 11736694784.000000
32 14433549312.000000 15308736512.000000 12575032320.000000
33 15379223552.000000 16329320448.000000 13413369856.000000
34 16324973568.000000 17349904384.000000 14251706368.000000
35 17270566912.000000 18370488320.000000 15090042880.000000
coreFreq : 2.6783e+09
clockTime : 3.8106e-01
wallTime : 3.6208e-01
insPerSec : 4.5322e+10
cycles : 18370488320.000000
L2 stalld : 1495533056.000000
 L2 stall rate : 0.081410
 Ldm stalld : 3992033792.000000
LDM stall rate : 0.217307
PKG Energy: 0.000000
 PKG Power : 0.000000
DRAM Energy: 0.000000
 Power : 0.000000
stallL2Rate : 0.0814
stallLDMRate : 0.2173
stallL2Cycles : 1495533056.0000
stallLDMCycles : 3992033792.0000
idealInsPerSecL2 : 4.9339e+10
idealInsPerSecLDM : 5.7906e+10
L3 volum: 1.3467e+09
RAM volum: 9.5655e+08
lowerBound : 18
 upperBound : 15
full L3 BW : 1.1465e+11
 fullRAMBW: 1.1909e+10
Latency L3 : 1.1105
 DRAM : 4.1733
Bandwidth Usage L3 : 0.0324
, Bandwidth usage DRAM : 0.2218
realIntensityL3 : 12.8239
 roofIntensityL3 : 0.4303
realIntensityRAM : 18.0550
 roofIntensityRAM : 4.8622
conclusion: compute bound 1 l3boundness 1 ramboundness 1

-----------------------
--------------6
overflow 0.362625
Socket : 1
socket 1 8708895690 7613859964
Uncorefreq: 3.0198e+09
18 946417600.000000 1022026176.000000 839521536.000000
19 1893223424.000000 2044052480.000000 1679043072.000000
20 2840009984.000000 3066078208.000000 2518564352.000000
21 3786765312.000000 4088103936.000000 3358085376.000000
22 4733029376.000000 5110129664.000000 4197606400.000000
23 5746742784.000000 6132155392.000000 5037127680.000000
24 6693151232.000000 7154181120.000000 5876648960.000000
25 7639850496.000000 8176206848.000000 6716170240.000000
26 8586689024.000000 9198231552.000000 7555690496.000000
27 9532965888.000000 10220257280.000000 8395211264.000000
28 10479816704.000000 11242284032.000000 9234733056.000000
29 11741779968.000000 12264311808.000000 10074256384.000000
30 12688437248.000000 13286338560.000000 10913778688.000000
31 13635147776.000000 14308365312.000000 11753300992.000000
32 14582389760.000000 15330393088.000000 12592823296.000000
33 15529175040.000000 16352421888.000000 13432346624.000000
34 16475321344.000000 17374451712.000000 14271870976.000000
35 17421991936.000000 18396481536.000000 15111395328.000000
coreFreq : 2.6783e+09
clockTime : 3.8160e-01
wallTime : 3.6262e-01
insPerSec : 4.5655e+10
cycles : 18396481536.000000
L2 stalld : 1206748416.000000
 L2 stall rate : 0.065597
 Ldm stalld : 3959198208.000000
LDM stall rate : 0.215215
PKG Energy: 0.000000
 PKG Power : 0.000000
DRAM Energy: 0.000000
 Power : 0.000000
stallL2Rate : 0.0656
stallLDMRate : 0.2152
stallL2Cycles : 1206748416.0000
stallLDMCycles : 3959198208.0000
idealInsPerSecL2 : 4.8860e+10
idealInsPerSecLDM : 5.8175e+10
L3 volum: 1.9988e+09
RAM volum: 1.4745e+09
lowerBound : 18
 upperBound : 15
full L3 BW : 1.1375e+11
 fullRAMBW: 1.1751e+10
Latency L3 : 0.6037
 DRAM : 2.6851
Bandwidth Usage L3 : 0.0485
, Bandwidth usage DRAM : 0.3460
realIntensityL3 : 8.7164
 roofIntensityL3 : 0.4295
realIntensityRAM : 11.8156
 roofIntensityRAM : 4.9505
conclusion: compute bound 1 l3boundness 1 ramboundness 1

-----------------------
--------------7
overflow 0.363801
Socket : 1
socket 1 9807751568 8708895690
Uncorefreq: 3.0205e+09
18 949477888.000000 1025590336.000000 842449216.000000
19 1899197952.000000 2051185664.000000 1684902656.000000
20 2849194752.000000 3076780800.000000 2527355904.000000
21 3799232512.000000 4102376960.000000 3369809920.000000
22 4748933632.000000 5127971840.000000 4212262912.000000
23 5766458368.000000 6153566720.000000 5054715904.000000
24 6716136960.000000 7179163136.000000 5897169920.000000
25 7666028544.000000 8204760064.000000 6739624960.000000
26 8616089600.000000 9230358528.000000 7582080512.000000
27 9566141440.000000 10255956992.000000 8424536576.000000
28 10516140032.000000 11281555456.000000 9266992128.000000
29 11784474624.000000 12307153920.000000 10109448192.000000
30 12734242816.000000 13332752384.000000 10951904256.000000
31 13684288512.000000 14358350848.000000 11794360320.000000
32 14634268672.000000 15383949312.000000 12636816384.000000
33 15584413696.000000 16409547776.000000 13479272448.000000
34 16533970944.000000 17435146240.000000 14321727488.000000
35 17483915264.000000 18460743680.000000 15164182528.000000
coreFreq : 2.6783e+09
clockTime : 3.8293e-01
wallTime : 3.6380e-01
insPerSec : 4.5658e+10
cycles : 18460743680.000000
L2 stalld : 1045256384.000000
 L2 stall rate : 0.056620
 Ldm stalld : 3974684416.000000
LDM stall rate : 0.215305
PKG Energy: 0.000000
 PKG Power : 0.000000
DRAM Energy: 0.000000
 Power : 0.000000
stallL2Rate : 0.0566
stallLDMRate : 0.2153
stallL2Cycles : 1045256384.0000
stallLDMCycles : 3974684416.0000
idealInsPerSecL2 : 4.8398e+10
idealInsPerSecLDM : 5.8186e+10
L3 volum: 2.0126e+09
RAM volum: 1.4783e+09
lowerBound : 18
 upperBound : 15
full L3 BW : 1.1625e+11
 fullRAMBW: 1.2188e+10
Latency L3 : 0.5194
 DRAM : 2.6886
Bandwidth Usage L3 : 0.0476
, Bandwidth usage DRAM : 0.3334
realIntensityL3 : 8.6872
 roofIntensityL3 : 0.4163
realIntensityRAM : 11.8267
 roofIntensityRAM : 4.7738
conclusion: compute bound 1 l3boundness 1 ramboundness 1

-----------------------
--------------8
overflow 0.362455
Socket : 1
socket 1 10902393308 9807751568
Uncorefreq: 3.0201e+09
18 946258240.000000 1021669952.000000 839228928.000000
19 1892718848.000000 2043336448.000000 1678455040.000000
20 2839147008.000000 3065002496.000000 2517680896.000000
21 3785113088.000000 4086668288.000000 3356906240.000000
22 4731213824.000000 5108336128.000000 4196133376.000000
23 5744876544.000000 6130003968.000000 5035360768.000000
24 6690938368.000000 7151671296.000000 5874587648.000000
25 7637266944.000000 8173338624.000000 6713814528.000000
26 8583690752.000000 9195005952.000000 7553041408.000000
27 9530013696.000000 10216673280.000000 8392267776.000000
28 10476435456.000000 11238340608.000000 9231494144.000000
29 11730206720.000000 12260007936.000000 10070720512.000000
30 12676398080.000000 13281676288.000000 10909947904.000000
31 13622887424.000000 14303345664.000000 11749176320.000000
32 14569305088.000000 15325012992.000000 12588403712.000000
33 15515816960.000000 16346681344.000000 13427631104.000000
34 16461840384.000000 17368348672.000000 14266858496.000000
35 17408210944.000000 18390016000.000000 15106084864.000000
coreFreq : 2.6783e+09
clockTime : 3.8147e-01
wallTime : 3.6245e-01
insPerSec : 4.5635e+10
cycles : 18390016000.000000
L2 stalld : 1249763328.000000
 L2 stall rate : 0.067959
 Ldm stalld : 3960219904.000000
LDM stall rate : 0.215346
PKG Energy: 0.000000
 PKG Power : 0.000000
DRAM Energy: 0.000000
 Power : 0.000000
stallL2Rate : 0.0680
stallLDMRate : 0.2153
stallL2Cycles : 1249763328.0000
stallLDMCycles : 3960219904.0000
idealInsPerSecL2 : 4.8962e+10
idealInsPerSecLDM : 5.8159e+10
L3 volum: 1.9780e+09
RAM volum: 1.4502e+09
lowerBound : 18
 upperBound : 15
full L3 BW : 1.1487e+11
 fullRAMBW: 1.1947e+10
Latency L3 : 0.6318
 DRAM : 2.7308
Bandwidth Usage L3 : 0.0475
, Bandwidth usage DRAM : 0.3349
realIntensityL3 : 8.8008
 roofIntensityL3 : 0.4263
realIntensityRAM : 12.0040
 roofIntensityRAM : 4.8683
conclusion: compute bound 1 l3boundness 1 ramboundness 1

-----------------------
--------------9
overflow 0.362195
Socket : 1
socket 1 11996245776 10902393308
Uncorefreq: 3.0201e+09
18 945447744.000000 1020954112.000000 838640832.000000
19 1891099136.000000 2041905664.000000 1677279744.000000
20 2836812800.000000 3062857472.000000 2515918848.000000
21 3782464000.000000 4083807744.000000 3354556672.000000
22 4727895040.000000 5104756224.000000 4193192960.000000
23 5742430208.000000 6125703168.000000 5031827968.000000
24 6687666176.000000 7146649600.000000 5870462464.000000
25 7633010688.000000 8167595520.000000 6709096448.000000
26 8578586624.000000 9188541440.000000 7547730432.000000
27 9524205568.000000 10209486848.000000 8386363904.000000
28 10469936128.000000 11230431232.000000 9224996864.000000
29 11789795328.000000 12251035648.000000 10063350784.000000
30 12735247360.000000 13271975936.000000 10901980160.000000
31 13680805888.000000 14292914176.000000 11740608512.000000
32 14626533376.000000 15313853440.000000 12579236864.000000
33 15572154368.000000 16334790656.000000 13417863168.000000
34 16517180416.000000 17355726848.000000 14256489472.000000
35 17462925312.000000 18376665088.000000 15095116800.000000
coreFreq : 2.6783e+09
clockTime : 3.8119e-01
wallTime : 3.6220e-01
insPerSec : 4.5812e+10
cycles : 18376665088.000000
L2 stalld : 1277001600.000000
 L2 stall rate : 0.069490
 Ldm stalld : 3973335040.000000
LDM stall rate : 0.216216
PKG Energy: 0.000000
 PKG Power : 0.000000
DRAM Energy: 0.000000
 Power : 0.000000
stallL2Rate : 0.0695
stallLDMRate : 0.2162
stallL2Cycles : 1277001600.0000
stallLDMCycles : 3973335040.0000
idealInsPerSecL2 : 4.9233e+10
idealInsPerSecLDM : 5.8449e+10
L3 volum: 1.0843e+09
RAM volum: 7.5455e+08
lowerBound : 18
 upperBound : 15
full L3 BW : 1.1482e+11
 fullRAMBW: 1.1938e+10
Latency L3 : 1.1777
 DRAM : 5.2659
Bandwidth Usage L3 : 0.0261
, Bandwidth usage DRAM : 0.1745
realIntensityL3 : 16.1056
 roofIntensityL3 : 0.4288
realIntensityRAM : 23.1436
 roofIntensityRAM : 4.8961
conclusion: compute bound 1 l3boundness 1 ramboundness 1

-----------------------
--------------10
overflow 0.361563
Socket : 1
socket 1 13087744130 11996245776
Uncorefreq: 3.0188e+09
18 943925632.000000 1018863104.000000 836923072.000000
19 1888055424.000000 2037720832.000000 1673841664.000000
20 2832092160.000000 3056572160.000000 2510755072.000000
21 3776151552.000000 4075419904.000000 3347665664.000000
22 4720120832.000000 5094263296.000000 4184572416.000000
23 5734819840.000000 6113103360.000000 5021476352.000000
24 6678754816.000000 7131938816.000000 5858376704.000000
25 7622787584.000000 8150768128.000000 6695271936.000000
26 8566832640.000000 9169591296.000000 7532162560.000000
27 9510884352.000000 10188409856.000000 8369049088.000000
28 10454961152.000000 11207223296.000000 9205932032.000000
29 11398910976.000000 12226031616.000000 10042810368.000000
30 12342835200.000000 13244834816.000000 10879684608.000000
31 13286842368.000000 14263633920.000000 11716555776.000000
32 14230878208.000000 15282428928.000000 12553422848.000000
33 15175042048.000000 16301219840.000000 13390286848.000000
34 16118233088.000000 17320007680.000000 14227148800.000000
35 17062660096.000000 18338791424.000000 15064006656.000000
coreFreq : 2.6783e+09
clockTime : 3.8040e-01
wallTime : 3.6156e-01
insPerSec : 4.4854e+10
cycles : 18338791424.000000
L2 stalld : 2356969984.000000
 L2 stall rate : 0.128524
 Ldm stalld : 4047917056.000000
LDM stall rate : 0.220730
PKG Energy: 0.000000
 PKG Power : 0.000000
DRAM Energy: 0.000000
 Power : 0.000000
stallL2Rate : 0.1285
stallLDMRate : 0.2207
stallL2Cycles : 2356969984.0000
stallLDMCycles : 4047917056.0000
idealInsPerSecL2 : 5.1469e+10
idealInsPerSecLDM : 5.7559e+10
L3 volum: 3.5889e+07
RAM volum: 7.5297e+06
lowerBound : 18
 upperBound : 15
full L3 BW : 1.1063e+11
 fullRAMBW: 1.1207e+10
Latency L3 : 65.6748
 DRAM : 537.5914
Bandwidth Usage L3 : 0.0009
, Bandwidth usage DRAM : 0.0019
realIntensityL3 : 475.4352
 roofIntensityL3 : 0.4652
realIntensityRAM : 2266.0393
 roofIntensityRAM : 5.1361
conclusion: compute bound 1 l3boundness 1 ramboundness 1

-----------------------
--------------11
overflow 0.360432
Socket : 1
socket 1 14175966406 13087744130
Uncorefreq: 3.0192e+09
18 940780160.000000 1015671296.000000 834301440.000000
19 1882758016.000000 2031343616.000000 1668603904.000000
20 2823880192.000000 3047016448.000000 2502906368.000000
21 3764374016.000000 4062689792.000000 3337209344.000000
22 4705172480.000000 5078363136.000000 4171512576.000000
23 5716396544.000000 6094036480.000000 5005815808.000000
24 6657316864.000000 7109710336.000000 5840119296.000000
25 7598265856.000000 8125384704.000000 6674423296.000000
26 8539303936.000000 9141059584.000000 7508727808.000000
27 9480355840.000000 10156735488.000000 8343032832.000000
28 10421451776.000000 11172411392.000000 9177337856.000000
29 11362550784.000000 12188086272.000000 10011642880.000000
30 12303501312.000000 13203762176.000000 10845947904.000000
31 13244565504.000000 14219438080.000000 11680252928.000000
32 14185703424.000000 15235112960.000000 12514557952.000000
33 15126800384.000000 16250787840.000000 13348861952.000000
34 16066747392.000000 17266462720.000000 14183165952.000000
35 17008175104.000000 18282135552.000000 15017468928.000000
coreFreq : 2.6783e+09
clockTime : 3.7923e-01
wallTime : 3.6043e-01
insPerSec : 4.4849e+10
cycles : 18282135552.000000
L2 stalld : 2312541440.000000
 L2 stall rate : 0.126492
 Ldm stalld : 4036280832.000000
LDM stall rate : 0.220777
PKG Energy: 0.000000
 PKG Power : 0.000000
DRAM Energy: 0.000000
 Power : 0.000000
stallL2Rate : 0.1265
stallLDMRate : 0.2208
stallL2Cycles : 2312541440.0000
stallLDMCycles : 4036280832.0000
idealInsPerSecL2 : 5.1344e+10
idealInsPerSecLDM : 5.7557e+10
L3 volum: 4.4252e+07
RAM volum: 1.0759e+07
lowerBound : 18
 upperBound : 15
full L3 BW : 1.1193e+11
 fullRAMBW: 1.1433e+10
Latency L3 : 52.2590
 DRAM : 375.1570
Bandwidth Usage L3 : 0.0011
, Bandwidth usage DRAM : 0.0026
realIntensityL3 : 384.3523
 roofIntensityL3 : 0.4587
realIntensityRAM : 1580.8452
 roofIntensityRAM : 5.0341
conclusion: compute bound 1 l3boundness 1 ramboundness 1

-----------------------
--------------12

pi is approximately = 662.51701500969465996604
Error               = 659.37542240969469276024
Energy of socket 1 : PKG: 0.000000 DRAM 0.000000


* Run CG and Sampling

init freeze 700 80000000
init unfreeze 700 20000000
Node object is created
registed sampling event
overflow 0.427531
Socket : 1
socket 1 1457169624 526202
Uncorefreq: 3.4071e+09
18 660634752.000000 1345200896.000000 1078374528.000000
19 1670101632.000000 2438103040.000000 2059625984.000000
20 2676316672.000000 3529387264.000000 3040587776.000000
21 3685545472.000000 4619376640.000000 4004641280.000000
22 4711781888.000000 5732038656.000000 4985256448.000000
23 5717576192.000000 6822460928.000000 5965847552.000000
24 6743488000.000000 7935158272.000000 6946485248.000000
25 7791449088.000000 9071851520.000000 7926789120.000000
26 8812073984.000000 10179332096.000000 8907379712.000000
27 9821946880.000000 11272715264.000000 9880803328.000000
28 10835031040.000000 12371563520.000000 10861112320.000000
29 11848884224.000000 13470629888.000000 11839591424.000000
30 12863011840.000000 14570380288.000000 12819357696.000000
31 13915624448.000000 15711669248.000000 13798851584.000000
32 14925005824.000000 16806650880.000000 14778771456.000000
33 15935399936.000000 17902018560.000000 15758649344.000000
34 16966190080.000000 19020267520.000000 16738657280.000000
35 17991424000.000000 20124669952.000000 17711904768.000000
coreFreq : 2.4997e+09
clockTime : 4.4727e-01
wallTime : 4.2753e-01
insPerSec : 4.0225e+10
cycles : 20124669952.000000
L2 stalld : 1910394880.000000
 L2 stall rate : 0.094928
 Ldm stalld : 4858889216.000000
LDM stall rate : 0.241439
PKG Energy: 0.000000
 PKG Power : 0.000000
DRAM Energy: 0.000000
 Power : 0.000000
stallL2Rate : 0.0949
stallLDMRate : 0.2414
stallL2Cycles : 1910394880.0000
stallLDMCycles : 4858889216.0000
idealInsPerSecL2 : 4.4444e+10
idealInsPerSecLDM : 5.3028e+10
L3 volum: 3.9565e+09
RAM volum: 8.2576e+08
lowerBound : 22
 upperBound : 15
full L3 BW : 7.6645e+10
 fullRAMBW: 4.2287e+09
Latency L3 : 0.4829
 DRAM : 5.8841
Bandwidth Usage L3 : 0.1207
, Bandwidth usage DRAM : 0.4568
realIntensityL3 : 4.5474
 roofIntensityL3 : 0.5799
realIntensityRAM : 21.7876
 roofIntensityRAM : 12.5400
conclusion: compute bound 1 l3boundness 1 ramboundness 1

-----------------------
--------------0
overflow 0.455198
Socket : 1
socket 1 2870397026 1457169624
Uncorefreq: 3.1046e+09
18 652751808.000000 1363840128.000000 1120297216.000000
19 1917805824.000000 2727676416.000000 2240591360.000000
20 3181638656.000000 4091506688.000000 3360880640.000000
21 4444673024.000000 5455332352.000000 4481166336.000000
22 5708408832.000000 6819154944.000000 5601449472.000000
23 6972600320.000000 8182972928.000000 6721728512.000000
24 8236643328.000000 9546784768.000000 7842002944.000000
25 9500565504.000000 10910593024.000000 8962273280.000000
26 10764239872.000000 12274396160.000000 10082540544.000000
27 12028240896.000000 13638195200.000000 11202803712.000000
28 13292065792.000000 15001991168.000000 12323064832.000000
29 14555904000.000000 16365783040.000000 13443321856.000000
30 15819905024.000000 17729572864.000000 14563576832.000000
31 17083094016.000000 19093356544.000000 15683827712.000000
32 18346991616.000000 20457136128.000000 16804075520.000000
33 19610994688.000000 21820909568.000000 17924317184.000000
34 20874657792.000000 23184676864.000000 19044554752.000000
35 22138556416.000000 24548438016.000000 20164788224.000000
coreFreq : 2.6783e+09
clockTime : 5.0921e-01
wallTime : 4.5520e-01
insPerSec : 4.3476e+10
cycles : 24548438016.000000
L2 stalld : 1963738880.000000
 L2 stall rate : 0.079994
 Ldm stalld : 5812492800.000000
LDM stall rate : 0.236776
PKG Energy: 0.000000
 PKG Power : 0.000000
DRAM Energy: 0.000000
 Power : 0.000000
stallL2Rate : 0.0800
stallLDMRate : 0.2368
stallL2Cycles : 1963738880.0000
stallLDMCycles : 5812492800.0000
idealInsPerSecL2 : 4.7256e+10
idealInsPerSecLDM : 5.6964e+10
L3 volum: 4.2976e+09
RAM volum: 9.4324e+08
lowerBound : 19
 upperBound : 15
full L3 BW : 6.4405e+10
 fullRAMBW: 2.7622e+09
Latency L3 : 0.4569
 DRAM : 6.1623
Bandwidth Usage L3 : 0.1466
, Bandwidth usage DRAM : 0.7502
realIntensityL3 : 5.1514
 roofIntensityL3 : 0.7337
realIntensityRAM : 23.4709
 roofIntensityRAM : 20.6229
conclusion: balanced 0 l3boundness 1 ramboundness 0

-----------------------
--------------1
overflow 0.439542
Socket : 1
socket 1 4234676932 2870397026
Uncorefreq: 3.1039e+09
18 595092352.000000 1232708736.000000 1012582208.000000
19 1737284864.000000 2465415424.000000 2025162752.000000
20 2879382016.000000 3698123776.000000 3037744640.000000
21 4021007104.000000 4930833408.000000 4050327552.000000
22 5164951552.000000 6163544064.000000 5062910976.000000
23 6307314176.000000 7396255232.000000 6075494912.000000
24 7448836608.000000 8628969472.000000 7088081408.000000
25 8590976000.000000 9861683200.000000 8100667904.000000
26 9733139456.000000 11094397952.000000 9113254912.000000
27 10875037696.000000 12327112704.000000 10125842432.000000
28 12017360896.000000 13559826432.000000 11138428928.000000
29 13159286784.000000 14792542208.000000 12151016448.000000
30 14301159424.000000 16025257984.000000 13163603968.000000
31 15443310592.000000 17257973760.000000 14176191488.000000
32 16585522176.000000 18490689536.000000 15188780032.000000
33 17727817728.000000 19723407360.000000 16201369600.000000
34 18869665792.000000 20956127232.000000 17213960192.000000
35 20011831296.000000 22188847104.000000 18226550784.000000
coreFreq : 2.6783e+09
clockTime : 4.6027e-01
wallTime : 4.3954e-01
insPerSec : 4.3479e+10
cycles : 22188847104.000000
L2 stalld : 1815748864.000000
 L2 stall rate : 0.081832
 Ldm stalld : 5254386688.000000
LDM stall rate : 0.236803
PKG Energy: 0.000000
 PKG Power : 0.000000
DRAM Energy: 0.000000
 Power : 0.000000
stallL2Rate : 0.0818
stallLDMRate : 0.2368
stallL2Cycles : 1815748864.0000
stallLDMCycles : 5254386688.0000
idealInsPerSecL2 : 4.7354e+10
idealInsPerSecLDM : 5.6969e+10
L3 volum: 4.0396e+09
RAM volum: 8.4983e+08
lowerBound : 19
 upperBound : 15
full L3 BW : 6.1785e+10
 fullRAMBW: 2.3014e+09
Latency L3 : 0.4495
 DRAM : 6.1829
Bandwidth Usage L3 : 0.1488
, Bandwidth usage DRAM : 0.8401
realIntensityL3 : 4.9539
 roofIntensityL3 : 0.7664
realIntensityRAM : 23.5480
 roofIntensityRAM : 24.7542
conclusion: balanced 0 l3boundness 1 ramboundness 0

-----------------------
--------------2
overflow 0.582386
Socket : 1
socket 1 6018557832 4234676932
Uncorefreq: 3.0631e+09
18 802066112.000000 1672173184.000000 1373570816.000000
19 2351940096.000000 3344347648.000000 2747142656.000000
20 3901587968.000000 5016521728.000000 4120714240.000000
21 5451138560.000000 6688695296.000000 5494285312.000000
22 7000784896.000000 8360868864.000000 6867856384.000000
23 8550764544.000000 10033043456.000000 8241428480.000000
24 10098691072.000000 11705217024.000000 9615000576.000000
25 11648319488.000000 13377392640.000000 10988572672.000000
26 13198168064.000000 15049567232.000000 12362144768.000000
27 14747976704.000000 16721741824.000000 13735716864.000000
28 16297868288.000000 18393915392.000000 15109287936.000000
29 17847408640.000000 20066088960.000000 16482859008.000000
30 19397236736.000000 21738262528.000000 17856430080.000000
31 20946677760.000000 23410436096.000000 19230001152.000000
32 22496419840.000000 25082609664.000000 20603572224.000000
33 24044836864.000000 26754783232.000000 21977143296.000000
34 25594023936.000000 28426954752.000000 23350714368.000000
35 27143753728.000000 30099128320.000000 24724285440.000000
coreFreq : 2.6783e+09
clockTime : 6.2435e-01
wallTime : 5.8239e-01
insPerSec : 4.3475e+10
cycles : 30099128320.000000
L2 stalld : 2355489792.000000
 L2 stall rate : 0.078258
 Ldm stalld : 7128340992.000000
LDM stall rate : 0.236829
PKG Energy: 0.000000
 PKG Power : 0.000000
DRAM Energy: 0.000000
 Power : 0.000000
stallL2Rate : 0.0783
stallLDMRate : 0.2368
stallL2Cycles : 2355489792.0000
stallLDMCycles : 7128340992.0000
idealInsPerSecL2 : 4.7166e+10
idealInsPerSecLDM : 5.6967e+10
L3 volum: 5.4053e+09
RAM volum: 1.1581e+09
lowerBound : 18
 upperBound : 15
full L3 BW : 2.6121e+11
 fullRAMBW: 3.7520e+10
Latency L3 : 0.4358
 DRAM : 6.1554
Bandwidth Usage L3 : 0.0355
, Bandwidth usage DRAM : 0.0530
realIntensityL3 : 5.0217
 roofIntensityL3 : 0.1806
realIntensityRAM : 23.4390
 roofIntensityRAM : 1.5183
conclusion: compute bound 1 l3boundness 1 ramboundness 1

-----------------------
--------------3
overflow 0.383884
Socket : 1
socket 1 7215785452 6018557832
Uncorefreq: 3.1187e+09
18 534090560.000000 1108046848.000000 910181376.000000
19 1623261696.000000 2216000000.000000 1820285440.000000
20 2649979392.000000 3324044800.000000 2730465024.000000
21 3676257024.000000 4432087040.000000 3640642816.000000
22 4702920704.000000 5540128256.000000 4550819328.000000
23 5729840128.000000 6648167936.000000 5460995072.000000
24 6756745216.000000 7756206080.000000 6371168768.000000
25 7783406080.000000 8864242688.000000 7281341440.000000
26 8810456064.000000 9972279296.000000 8191514112.000000
27 9837440000.000000 11080314880.000000 9101685760.000000
28 10864163840.000000 12188349440.000000 10011856896.000000
29 11890757632.000000 13296382976.000000 10922027008.000000
30 12917571584.000000 14404415488.000000 11832197120.000000
31 13944246272.000000 15512448000.000000 12742366208.000000
32 14971032576.000000 16620479488.000000 13652535296.000000
33 15997904896.000000 17728509952.000000 14562703360.000000
34 17024260096.000000 18836541440.000000 15472871424.000000
35 18051049472.000000 19944570880.000000 16383038464.000000
coreFreq : 2.6783e+09
clockTime : 4.1371e-01
wallTime : 3.8388e-01
insPerSec : 4.3632e+10
cycles : 19944570880.000000
L2 stalld : 1538726784.000000
 L2 stall rate : 0.077150
 Ldm stalld : 4697342976.000000
LDM stall rate : 0.235520
PKG Energy: 0.000000
 PKG Power : 0.000000
DRAM Energy: 0.000000
 Power : 0.000000
stallL2Rate : 0.0772
stallLDMRate : 0.2355
stallL2Cycles : 1538726784.0000
stallLDMCycles : 4697342976.0000
idealInsPerSecL2 : 4.7280e+10
idealInsPerSecLDM : 5.7074e+10
L3 volum: 3.5329e+09
RAM volum: 7.5661e+08
lowerBound : 19
 upperBound : 15
full L3 BW : 1.1204e+11
 fullRAMBW: 1.1140e+10
Latency L3 : 0.4355
 DRAM : 6.2084
Bandwidth Usage L3 : 0.0821
, Bandwidth usage DRAM : 0.1769
realIntensityL3 : 5.1095
 roofIntensityL3 : 0.4220
realIntensityRAM : 23.8579
 roofIntensityRAM : 5.1232
conclusion: compute bound 1 l3boundness 1 ramboundness 1

-----------------------
--------------4
overflow 0.423949
Socket : 1
socket 1 8520760300 7215785452
Uncorefreq: 3.0781e+09
18 590384320.000000 1232655872.000000 1012538688.000000
19 1799648768.000000 2465046528.000000 2024859776.000000
20 2938637312.000000 3697699584.000000 3037396224.000000
21 4081602048.000000 4930352128.000000 4049932032.000000
22 5224051712.000000 6163004416.000000 5062467584.000000
23 6366571008.000000 7395655680.000000 6075002368.000000
24 7508890112.000000 8628304896.000000 7087535616.000000
25 8651238400.000000 9860954112.000000 8100069376.000000
26 9793680384.000000 11093604352.000000 9112603648.000000
27 10936076288.000000 12326254592.000000 10125137920.000000
28 12078449664.000000 13558903808.000000 11137671168.000000
29 13220682752.000000 14791552000.000000 12150203392.000000
30 14363061248.000000 16024200192.000000 13162735616.000000
31 15504822272.000000 17256847360.000000 14175266816.000000
32 16647181312.000000 18489495552.000000 15187799040.000000
33 17789612032.000000 19722141696.000000 16200329216.000000
34 18931439616.000000 20954785792.000000 17212858368.000000
35 20073811968.000000 22187429888.000000 18225387520.000000
coreFreq : 2.6783e+09
clockTime : 4.6024e-01
wallTime : 4.2395e-01
insPerSec : 4.3616e+10
cycles : 22187429888.000000
L2 stalld : 1653773184.000000
 L2 stall rate : 0.074536
 Ldm stalld : 5226487808.000000
LDM stall rate : 0.235561
PKG Energy: 0.000000
 PKG Power : 0.000000
DRAM Energy: 0.000000
 Power : 0.000000
stallL2Rate : 0.0745
stallLDMRate : 0.2356
stallL2Cycles : 1653773184.0000
stallLDMCycles : 5226487808.0000
idealInsPerSecL2 : 4.7129e+10
idealInsPerSecLDM : 5.7057e+10
L3 volum: 3.9803e+09
RAM volum: 8.5789e+08
lowerBound : 18
 upperBound : 15
full L3 BW : 3.1258e+11
 fullRAMBW: 4.6495e+10
Latency L3 : 0.4155
 DRAM : 6.0923
Bandwidth Usage L3 : 0.0300
, Bandwidth usage DRAM : 0.0435
realIntensityL3 : 5.0433
 roofIntensityL3 : 0.1508
realIntensityRAM : 23.3990
 roofIntensityRAM : 1.2272
conclusion: compute bound 1 l3boundness 1 ramboundness 1

-----------------------
--------------5
overflow 0.391560
Socket : 1
socket 1 9715000970 8520760300
Uncorefreq: 3.0500e+09
18 597036928.000000 1142656640.000000 938610880.000000
19 1702892160.000000 2285102592.000000 1877048576.000000
20 2761863168.000000 3427799552.000000 2815692800.000000
21 3820358400.000000 4570496000.000000 3754336512.000000
22 4879442944.000000 5713193472.000000 4692980736.000000
23 5938606080.000000 6855889920.000000 5631624704.000000
24 6997565440.000000 7998587392.000000 6570269184.000000
25 8056431616.000000 9141284864.000000 7508913152.000000
26 9115096064.000000 10283982848.000000 8447557632.000000
27 10174075904.000000 11426680832.000000 9386202112.000000
28 11233922048.000000 12569378816.000000 10324847616.000000
29 12292238336.000000 13712077824.000000 11263493120.000000
30 13351330816.000000 14854776832.000000 12202138624.000000
31 14410146816.000000 15997476864.000000 13140785152.000000
32 15469086720.000000 17140175872.000000 14079430656.000000
33 16528153600.000000 18282874880.000000 15018077184.000000
34 17586819072.000000 19425574912.000000 15956724736.000000
35 18645936128.000000 20568276992.000000 16895373312.000000
coreFreq : 2.6783e+09
clockTime : 4.2665e-01
wallTime : 3.9156e-01
insPerSec : 4.3703e+10
cycles : 20568276992.000000
L2 stalld : 1612131840.000000
 L2 stall rate : 0.078380
 Ldm stalld : 4813774336.000000
LDM stall rate : 0.234039
PKG Energy: 0.000000
 PKG Power : 0.000000
DRAM Energy: 0.000000
 Power : 0.000000
stallL2Rate : 0.0784
stallLDMRate : 0.2340
stallL2Cycles : 1612131840.0000
stallLDMCycles : 4813774336.0000
idealInsPerSecL2 : 4.7420e+10
idealInsPerSecLDM : 5.7057e+10
L3 volum: 3.2562e+09
RAM volum: 7.2874e+08
lowerBound : 18
 upperBound : 15
full L3 BW : 2.1660e+11
 fullRAMBW: 2.9723e+10
Latency L3 : 0.4951
 DRAM : 6.6057
Bandwidth Usage L3 : 0.0384
, Bandwidth usage DRAM : 0.0626
realIntensityL3 : 5.7262
 roofIntensityL3 : 0.2189
realIntensityRAM : 25.5867
 roofIntensityRAM : 1.9196
conclusion: compute bound 1 l3boundness 1 ramboundness 1

-----------------------
--------------6
overflow 0.548295
Socket : 1
socket 1 11430029198 9715000970
Uncorefreq: 3.1279e+09
18 747937920.000000 1563565312.000000 1284357248.000000
19 2193789440.000000 3126931968.000000 2568551424.000000
20 3642685184.000000 4690502656.000000 3852913152.000000
21 5091672576.000000 6254074880.000000 5137275904.000000
22 6589130752.000000 7817464832.000000 6421488640.000000
23 8038271488.000000 9381033984.000000 7705848832.000000
24 9487229952.000000 10944603136.000000 8990210048.000000
25 10936067072.000000 12508172288.000000 10274570240.000000
26 12385244160.000000 14071740416.000000 11558930432.000000
27 13834414080.000000 15635307520.000000 12843289600.000000
28 15283473408.000000 17198874624.000000 14127648768.000000
29 16732286976.000000 18762442752.000000 15412007936.000000
30 18181318656.000000 20326010880.000000 16696367104.000000
31 19630071808.000000 21889576960.000000 17980725248.000000
32 21078992896.000000 23453145088.000000 19265083392.000000
33 22528141312.000000 25016711168.000000 20549441536.000000
34 23976388608.000000 26580277248.000000 21833799680.000000
35 25425461248.000000 28143843328.000000 23118157824.000000
coreFreq : 2.6783e+09
clockTime : 5.8379e-01
wallTime : 5.4830e-01
insPerSec : 4.3552e+10
cycles : 28143843328.000000
L2 stalld : 2060400384.000000
 L2 stall rate : 0.073210
 Ldm stalld : 6629535744.000000
LDM stall rate : 0.235559
PKG Energy: 0.000000
 PKG Power : 0.000000
DRAM Energy: 0.000000
 Power : 0.000000
stallL2Rate : 0.0732
stallLDMRate : 0.2356
stallL2Cycles : 2060400384.0000
stallLDMCycles : 6629535744.0000
idealInsPerSecL2 : 4.6993e+10
idealInsPerSecLDM : 5.6973e+10
L3 volum: 5.1763e+09
RAM volum: 1.0757e+09
lowerBound : 19
 upperBound : 15
full L3 BW : 1.4318e+11
 fullRAMBW: 1.6617e+10
Latency L3 : 0.3980
 DRAM : 6.1630
Bandwidth Usage L3 : 0.0659
, Bandwidth usage DRAM : 0.1181
realIntensityL3 : 4.9119
 roofIntensityL3 : 0.3282
realIntensityRAM : 23.6364
 roofIntensityRAM : 3.4286
conclusion: compute bound 1 l3boundness 1 ramboundness 1

-----------------------
--------------7
overflow 0.403876
Socket : 1
socket 1 12661715914 11430029198
Uncorefreq: 3.0497e+09
18 751586112.000000 1167197952.000000 958769792.000000
19 1832186112.000000 2334393856.000000 1917537920.000000
20 2913487104.000000 3501593600.000000 2876308992.000000
21 3993174272.000000 4668789760.000000 3835077376.000000
22 5143663616.000000 5835894784.000000 4793771008.000000
23 6225232896.000000 7003092480.000000 5752540672.000000
24 7309157376.000000 8170295296.000000 6711314432.000000
25 8390468608.000000 9337493504.000000 7670084608.000000
26 9471937536.000000 10504699904.000000 8628860928.000000
27 10553141248.000000 11671904256.000000 9587636224.000000
28 11634534400.000000 12839109632.000000 10546411520.000000
29 12715518976.000000 14006321152.000000 11505192960.000000
30 13796508672.000000 15173525504.000000 12463968256.000000
31 14877875200.000000 16340729856.000000 13422743552.000000
32 15959160832.000000 17507934208.000000 14381518848.000000
33 17040379904.000000 18675148800.000000 15340301312.000000
34 18121547776.000000 19842361344.000000 16299083776.000000
35 19202932736.000000 21009569792.000000 17257861120.000000
coreFreq : 2.6783e+09
clockTime : 4.3580e-01
wallTime : 4.0388e-01
insPerSec : 4.4063e+10
cycles : 21009569792.000000
L2 stalld : 1868807424.000000
 L2 stall rate : 0.088950
 Ldm stalld : 4835949568.000000
LDM stall rate : 0.230178
PKG Energy: 0.000000
 PKG Power : 0.000000
DRAM Energy: 0.000000
 Power : 0.000000
stallL2Rate : 0.0890
stallLDMRate : 0.2302
stallL2Cycles : 1868807424.0000
stallLDMCycles : 4835949568.0000
idealInsPerSecL2 : 4.8365e+10
idealInsPerSecLDM : 5.7238e+10
L3 volum: 2.1911e+09
RAM volum: 6.8533e+08
lowerBound : 18
 upperBound : 15
full L3 BW : 2.1560e+11
 fullRAMBW: 2.9549e+10
Latency L3 : 0.8529
 DRAM : 7.0564
Bandwidth Usage L3 : 0.0252
, Bandwidth usage DRAM : 0.0574
realIntensityL3 : 8.7642
 roofIntensityL3 : 0.2243
realIntensityRAM : 28.0200
 roofIntensityRAM : 1.9370
conclusion: compute bound 1 l3boundness 1 ramboundness 1

-----------------------
--------------8
overflow 0.475753
Socket : 1
socket 1 14071321806 12661715914
Uncorefreq: 2.9629e+09
18 1274574592.000000 1375593344.000000 1129951488.000000
19 2549253120.000000 2751164928.000000 2259885312.000000
20 3823893248.000000 4126749952.000000 3389830144.000000
21 5098503680.000000 5502306816.000000 4519751680.000000
22 6443148288.000000 6877793792.000000 5649615872.000000
23 7718346752.000000 8253332992.000000 6779523072.000000
24 8994167808.000000 9628876800.000000 7909434368.000000
25 10268798976.000000 11004409856.000000 9039336448.000000
26 11543498752.000000 12379949056.000000 10169243648.000000
27 12818185216.000000 13755472896.000000 11299137536.000000
28 14092818432.000000 15131004928.000000 12429038592.000000
29 15367322624.000000 16506545152.000000 13558945792.000000
30 16641846272.000000 17882056704.000000 14688831488.000000
31 17915887616.000000 19257567232.000000 15818715136.000000
32 19190458368.000000 20633071616.000000 16948592640.000000
33 20464846848.000000 22008590336.000000 18078482432.000000
34 21739008000.000000 23384104960.000000 19208368128.000000
35 23013627904.000000 24759595008.000000 20338235392.000000
coreFreq : 2.6783e+09
clockTime : 5.1359e-01
wallTime : 4.7575e-01
insPerSec : 4.4809e+10
cycles : 24759595008.000000
L2 stalld : 2290386688.000000
 L2 stall rate : 0.092505
 Ldm stalld : 5473818624.000000
LDM stall rate : 0.221079
PKG Energy: 0.000000
 PKG Power : 0.000000
DRAM Energy: 0.000000
 Power : 0.000000
stallL2Rate : 0.0925
stallLDMRate : 0.2211
stallL2Cycles : 2290386688.0000
stallLDMCycles : 5473818624.0000
idealInsPerSecL2 : 4.9377e+10
idealInsPerSecLDM : 5.7527e+10
L3 volum: 4.8648e+07
RAM volum: 4.4568e+08
lowerBound : 17
 upperBound : 15
full L3 BW : 2.5983e+11
 fullRAMBW: 3.7421e+10
Latency L3 : 47.0812
 DRAM : 12.2821
Bandwidth Usage L3 : 0.0004
, Bandwidth usage DRAM : 0.0250
realIntensityL3 : 473.0686
 roofIntensityL3 : 0.1900
realIntensityRAM : 51.6376
 roofIntensityRAM : 1.5373
conclusion: compute bound 1 l3boundness 1 ramboundness 1

-----------------------
--------------9
overflow 0.423640
Socket : 1
socket 1 15280250860 14071321806
Uncorefreq: 2.8537e+09
18 1134730752.000000 1224618496.000000 1005936576.000000
19 2269070848.000000 2449228032.000000 2011865856.000000
20 3403877888.000000 3673845760.000000 3017801984.000000
21 4538502656.000000 4898450944.000000 4023727616.000000
22 5743263744.000000 6122983424.000000 5029593600.000000
23 6878255616.000000 7347584000.000000 6035515904.000000
24 8012777472.000000 8572197888.000000 7041448960.000000
25 9147516928.000000 9796803584.000000 8047374848.000000
26 10282417152.000000 11021423616.000000 9053313024.000000
27 11417868288.000000 12246031360.000000 10059241472.000000
28 12552677376.000000 13470642176.000000 11065171968.000000
29 13687020544.000000 14695267328.000000 12071114752.000000
30 14821756928.000000 15919877120.000000 13077044224.000000
31 15956428800.000000 17144485888.000000 14082972672.000000
32 17091179520.000000 18369089536.000000 15088898048.000000
33 18225940480.000000 19593715712.000000 16094840832.000000
34 19361273856.000000 20818339840.000000 17100781568.000000
35 20495988736.000000 22042947584.000000 18106710016.000000
coreFreq : 2.6783e+09
clockTime : 4.5724e-01
wallTime : 4.2364e-01
insPerSec : 4.4826e+10
cycles : 22042947584.000000
L2 stalld : 2539278336.000000
 L2 stall rate : 0.115197
 Ldm stalld : 4868485120.000000
LDM stall rate : 0.220864
PKG Energy: 0.000000
 PKG Power : 0.000000
DRAM Energy: 0.000000
 Power : 0.000000
stallL2Rate : 0.1152
stallLDMRate : 0.2209
stallL2Cycles : 2539278336.0000
stallLDMCycles : 4868485120.0000
idealInsPerSecL2 : 5.0662e+10
idealInsPerSecLDM : 5.7532e+10
L3 volum: 3.7527e+07
RAM volum: 3.5634e+08
lowerBound : 16
 upperBound : 15
full L3 BW : 2.2701e+11
 fullRAMBW: 3.1932e+10
Latency L3 : 67.6651
 DRAM : 13.6626
Bandwidth Usage L3 : 0.0004
, Bandwidth usage DRAM : 0.0263
realIntensityL3 : 546.1640
 roofIntensityL3 : 0.2232
realIntensityRAM : 57.5186
 roofIntensityRAM : 1.8017
conclusion: compute bound 1 l3boundness 1 ramboundness 1

-----------------------
--------------10
overflow 0.368504
Socket : 1
socket 1 16361391478 15280250860
Uncorefreq: 2.9339e+09
18 737565120.000000 799201088.000000 649334016.000000
19 1749173504.000000 1849536768.000000 1487910528.000000
20 2367997440.000000 2513451264.000000 2032918272.000000
21 2899178752.000000 3090160384.000000 2506643712.000000
22 3824936448.000000 4025293824.000000 3257414912.000000
23 4403651584.000000 4653561344.000000 3773517824.000000
24 5447600128.000000 5719889920.000000 4623645696.000000
25 6418412032.000000 6722913280.000000 5426846208.000000
26 7028459520.000000 7371411968.000000 5959540736.000000
27 7625971712.000000 8018135040.000000 6490825728.000000
28 8188179456.000000 8628871168.000000 6992499200.000000
29 8867743744.000000 9352233984.000000 7588240896.000000
30 9431258112.000000 9965409280.000000 8092051456.000000
31 9958293504.000000 10536581120.000000 8561223168.000000
32 10993496064.000000 11603168256.000000 9411563520.000000
33 11562781696.000000 12218278912.000000 9916832768.000000
34 12128360448.000000 12832507904.000000 10421494784.000000
35 12717068288.000000 13466863616.000000 10942586880.000000
coreFreq : 2.7075e+09
clockTime : 2.7633e-01
wallTime : 3.6850e-01
insPerSec : 4.6022e+10
cycles : 13466863616.000000
L2 stalld : 1671288064.000000
 L2 stall rate : 0.124104
 Ldm stalld : 3716267520.000000
LDM stall rate : 0.275956
PKG Energy: 0.000000
 PKG Power : 0.000000
DRAM Energy: 0.000000
 Power : 0.000000
stallL2Rate : 0.1241
stallLDMRate : 0.2760
stallL2Cycles : 1671288064.0000
stallLDMCycles : 3716267520.0000
idealInsPerSecL2 : 5.2542e+10
idealInsPerSecLDM : 6.3562e+10
L3 volum: 6.7268e+07
RAM volum: 3.4750e+08
lowerBound : 17
 upperBound : 15
full L3 BW : 1.6036e+11
 fullRAMBW: 2.0151e+10
Latency L3 : 24.8453
 DRAM : 10.6942
Bandwidth Usage L3 : 0.0011
, Bandwidth usage DRAM : 0.0468
realIntensityL3 : 189.0516
 roofIntensityL3 : 0.3276
realIntensityRAM : 36.5956
 roofIntensityRAM : 3.1543
conclusion: compute bound 1 l3boundness 1 ramboundness 1

-----------------------
--------------11
overflow 0.284358
Socket : 1
socket 1 17214987870 16361391478
Uncorefreq: 3.0018e+09
18 116463.000000 745801.000000 565685.000000
19 633409.000000 2446607.000000 2008199.000000
20 903743.000000 3573093.000000 3032228.000000
21 1121202.000000 4637758.000000 4059339.000000
22 1650194.000000 5944222.000000 5141788.000000
23 1738476.000000 6722400.000000 6146980.000000
24 442872288.000000 438611776.000000 306759104.000000
25 442975488.000000 439150336.000000 307299296.000000
26 442988320.000000 439451008.000000 307543296.000000
27 443051808.000000 440661920.000000 308853504.000000
28 443183584.000000 441192800.000000 309460544.000000
29 1444693504.000000 1416675328.000000 958589376.000000
30 1444809984.000000 1418185472.000000 960849792.000000
31 1445400960.000000 1420572032.000000 964303936.000000
32 1549382400.000000 1524966784.000000 1040090240.000000
33 1549395712.000000 1525143424.000000 1040245056.000000
34 1549604224.000000 1526032128.000000 1041546432.000000
35 1549878400.000000 1527208704.000000 1042565312.000000
coreFreq : 3.2227e+09
clockTime : 2.6327e-02
wallTime : 2.8436e-01
insPerSec : 5.8870e+10
--------------12

pi is approximately = 662.51701500969477365288
Error               = 659.37542240969480644708
Energy of socket 1 : PKG: 0.000000 DRAM 0.000000

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------


export OMP_NUM_THREADS=18
export OMP_PROC_BIND=close
export OMP_PLACES="{18:18:1}"

### Sampling interval is 2s

Start_core 18 End_core 36  num_core_events 6
init freeze 700 80000000
init unfreeze 700 20000000
Socket : 1
WallTime : 2.000000
Uncorefreq: 2.9939e+09
CoreFreq : 1.9913e+09
Core unhlated time : 1.999017
Core halted time : 0.000983
--------
ins cumulative: 50256310272.000000
cycles cumulative: 71651500032.000000
L2 stalld : 19535601664.000000
 Ldm stalld : 25178054656.000000
total stalld : 45873991680.000000
cycles : 71651500032.000000
--------
Time: Core : running 0.719171, total stall: 1.279846, stall+halted: 1.280829
Time: Core : running 1.453990, l2 stall: 0.545027, stall+halted: 0.546010
Time: Core : running 1.296570, ldm stall: 0.702447, stall+halted: 0.703430
Rate: Core : running 35.958557%, total stall: 63.992290%, stall+halted: 64.041443%
Rate: Core : running 72.699509%, l2 stall: 27.251345%, stall+halted: 27.300495%
Rate: Core : running 64.828506%, ldm stall: 35.122334%, stall+halted: 35.171490%
Time: Mem Busy: 1.944384 idle 0.055616
Time: L3 busy: 0.417789 idle 1.582211
Rate: Mem Busy: 97.219215 0dle 2.780783%
Rate: L3 busy: 20.889429 0dle 79.110573%
L3 volum: 9.3585e+10
RAM volum: 9.9140e+10
lowerBound : 17
 upperBound : 18
full L3 BW : 2.2400e+11
 fullRAMBW: 5.0988e+10
PKG Energy: 186.111633
 PKG Power : 93.055817
DRAM Energy: 36.356689
 Power : 18.178345
***** Roofline L3 ******
ins 50256310272.000000, datavolume 93584637952.000000, timeinterval 2.000000, timeCoreStall 0.546010, timeMemIdle 1.582211, fullBW 224000000000.000000, coreFreq 1991298432.000000, uncoreFreq 2993936384.000000
timeRoof 1.453990 timeLatency 0.546010
coreFreq 20 uncoreFreq 30
compute bound time atMaxFreq 2.000000 latency 0.546010 coreBusy 1.453990 factor 1.000000
timeInterval 2.000000  timeCoreBusy 1.453990 timeMemBusy 0.417789 1.05*timeAtMaxFreq 2.100000 new timeInterval 2.018828 noBottlenecktime 0.432195
timeInterval 2.000000  timeCoreBusy 1.453990 timeMemBusy 0.417789 1.05*timeAtMaxFreq 2.100000 new timeInterval 2.039001 noBottlenecktime 0.447631
timeInterval 2.000000  timeCoreBusy 1.453990 timeMemBusy 0.417789 1.05*timeAtMaxFreq 2.100000 new timeInterval 2.060668 noBottlenecktime 0.464209
timeInterval 2.000000  timeCoreBusy 1.453990 timeMemBusy 0.417789 1.05*timeAtMaxFreq 2.100000 new timeInterval 2.084002 noBottlenecktime 0.482064
timeInterval 2.000000  timeCoreBusy 1.453990 timeMemBusy 0.417789 1.05*timeAtMaxFreq 2.100000 new timeInterval 2.109202 noBottlenecktime 0.501346
core bound new Freq core 28 uncore 26

***** Roofline DRAM ******
ins 50256310272.000000, datavolume 99140018176.000000, timeinterval 2.000000, timeCoreStall 0.703430, timeMemIdle 0.055616, fullBW 50987872256.000000, coreFreq 1991298432.000000, uncoreFreq 2993936384.000000
timeRoof 1.944384 timeLatency 0.055616
coreFreq 20 uncoreFreq 30
memory bound time atMaxFreq 1.984110 latency 0.055616 coreBusy 1.296570 factor 0.714286
timeInterval 2.000000  timeCoreBusy 1.296570 timeMemBusy 1.944384 1.05*timeAtMaxFreq 2.083315 new time latency 0.058543 , new timeInterval 2.002927 noBottlenecktime 1.364811
 latency procent 2.922863
core 19  uncore 30
memory bound new Freq core 19 uncore 30

***** Conclusion ******
l3BOundness 1 dramBoundness -1
new setting : core 19  uncore 30
Socket : 1
WallTime : 2.000000
Uncorefreq: 2.9937e+09
CoreFreq : 1.8917e+09
Core unhlated time : 1.998981
Core halted time : 0.001019
--------
ins cumulative: 50264109056.000000
cycles cumulative: 68067917824.000000
L2 stalld : 18128506880.000000
 Ldm stalld : 23557871616.000000
total stalld : 42420314112.000000
cycles : 68067917824.000000
--------
Time: Core : running 0.753205, total stall: 1.245777, stall+halted: 1.246795
Time: Core : running 1.466593, l2 stall: 0.532388, stall+halted: 0.533407
Time: Core : running 1.307147, ldm stall: 0.691835, stall+halted: 0.692853
Rate: Core : running 37.660240%, total stall: 62.288837%, stall+halted: 62.339760%
Rate: Core : running 73.329666%, l2 stall: 26.619404%, stall+halted: 26.670338%
Rate: Core : running 65.357338%, ldm stall: 34.591736%, stall+halted: 34.642662%
Time: Mem Busy: 1.952636 idle 0.047364
Time: L3 busy: 0.416322 idle 1.583678
Rate: Mem Busy: 97.631790 0dle 2.368212%
Rate: L3 busy: 20.816095 0dle 79.183907%
L3 volum: 9.3256e+10
RAM volum: 9.9560e+10
lowerBound : 17
 upperBound : 18
full L3 BW : 2.2400e+11
 fullRAMBW: 5.0987e+10
PKG Energy: 182.243958
 PKG Power : 91.121979
DRAM Energy: 36.665985
 Power : 18.332993
***** Roofline L3 ******
ins 50264109056.000000, datavolume 93256105984.000000, timeinterval 2.000000, timeCoreStall 0.533407, timeMemIdle 1.583678, fullBW 224000000000.000000, coreFreq 1891738752.000000, uncoreFreq 2993746432.000000
timeRoof 1.466593 timeLatency 0.533407
coreFreq 19 uncoreFreq 30
compute bound time atMaxFreq 2.000000 latency 0.533407 coreBusy 1.466593 factor 1.000000
timeInterval 2.000000  timeCoreBusy 1.466593 timeMemBusy 0.416322 1.05*timeAtMaxFreq 2.100000 new timeInterval 2.018393 noBottlenecktime 0.430678
timeInterval 2.000000  timeCoreBusy 1.466593 timeMemBusy 0.416322 1.05*timeAtMaxFreq 2.100000 new timeInterval 2.038100 noBottlenecktime 0.446059
timeInterval 2.000000  timeCoreBusy 1.466593 timeMemBusy 0.416322 1.05*timeAtMaxFreq 2.100000 new timeInterval 2.059268 noBottlenecktime 0.462580
timeInterval 2.000000  timeCoreBusy 1.466593 timeMemBusy 0.416322 1.05*timeAtMaxFreq 2.100000 new timeInterval 2.082062 noBottlenecktime 0.480371
timeInterval 2.000000  timeCoreBusy 1.466593 timeMemBusy 0.416322 1.05*timeAtMaxFreq 2.100000 new timeInterval 2.106681 noBottlenecktime 0.499586
core bound new Freq core 28 uncore 26

***** Roofline DRAM ******
ins 50264109056.000000, datavolume 99560005632.000000, timeinterval 2.000000, timeCoreStall 0.692853, timeMemIdle 0.047364, fullBW 50987495424.000000, coreFreq 1891738752.000000, uncoreFreq 2993746432.000000
timeRoof 1.952636 timeLatency 0.047364
coreFreq 19 uncoreFreq 30
memory bound time atMaxFreq 1.984776 latency 0.047364 coreBusy 1.307147 factor 0.678571
timeInterval 2.000000  timeCoreBusy 1.307147 timeMemBusy 1.952636 1.05*timeAtMaxFreq 2.084015 new time latency 0.049996 , new timeInterval 2.002631 noBottlenecktime 1.379766
 latency procent 2.496495
core 18  uncore 30
memory bound new Freq core 18 uncore 30

***** Conclusion ******
l3BOundness 1 dramBoundness -1