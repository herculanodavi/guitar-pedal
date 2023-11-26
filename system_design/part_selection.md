# Part Selection

## Effect controls

## USB

## Processor
The suggested processor, STM32F103CBT6TR, is more expensive than STM32F401RBT6, while the F4 model has a Arm Core M4
and more RAM. The increased number of pins (from LQFP48 to LQFP64) is not an issue since this design is not constrained by space.

The main difference between our application and the one from the course is that we want to support a continuous and low-latency calculation of effects, and these are not yet specified. Thus, the trade-off of performance for space is advantageous. 

**Chosen part:** STM32F401RBT6

## Power supplies
Since requirements have no differences from the course, the parts will be the same. Reason to look for another pair of converters could if we had wanted to allow for the negotiable 500mA power consumption and consume more current (even so, this part would also be sufficient). At the time of the project, HT7533-1 was out of stock, so we chose a similar part: LDLN025M33R.

**Chosen parts:** TLV62569PDRLR (Buck) and LDLN025M33R (LDO).


## Converters
Since requirements have no differences from the course, the parts will be the same. Reason to look for another pair of converters could be to have a single-ended ADC or to invest in higher-performance parts, but these are not yet important enough to look for different parts. At the time of the project, both parts are active and in stock in Digikey.

**Chosen parts:** ADC141S616CIMM/NOPB (14-bit, 50-250kSPS, differential) and DAC7563SDGSR (12-bit, single-ended).

## Analogue sections


## Miscellaneous
