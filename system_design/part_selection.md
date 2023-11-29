# Part Selection

Given the reference design of the course, parts will only be different if there is a special reason to it, as part out of stock or additional functionality.

## Effect controls

- **Bistable buttons with LED:** LP4EE1PBCTR. It's a relatively cheap latched button with illumination. 2.2V illumination voltage and 0.1A current rating for 200mcd, so its consumption will be 1.5mA. 
- **Knobs for filter parameters:** PTV09A-4020F-B103. A cheap 10k linear single-gang potentiometer from Bourns.
- **Bistable footswitch:** (searching)
- **LED indicator:** T1341MND-20P000312U1930. The cheapest 1206 white LED I could find.
  
## USB

- **Receptacle:** 10164359-00011LF, the cheapest USB-C connector available in Digikey that is in stock.
- **ESD protection:** USBLC6-2SC6, from reference design.

## Processor

The suggested processor, STM32F103CBT6TR, is more expensive than STM32F401RBT6, while the F4 model has a Arm Core M4
and more RAM. The increased number of pins (from LQFP48 to LQFP64) is not an issue since this design is not constrained by space.

The main difference between our application and the one from the reference design is that we want to support a continuous and low-latency calculation of effects, and these are not yet specified. Thus, the trade-off of performance for space is advantageous. 

**Chosen part:** STM32F401RBT6

## Power supplies

Since requirements have no differences from the reference design, the parts will be the same. Reason to look for another pair of converters could if we had wanted to allow for the negotiable 500mA power consumption and consume more current (even so, this part would also be sufficient). At the time of the project, HT7533-1 was out of stock, so we chose a similar part: LDLN025M33R.

**Chosen parts:** TLV62569PDRLR (Buck) and LDLN025M33R (LDO).


## Converters

Since requirements have no differences from the reference design, the parts should be the same. Reason to look for another pair of converters could be to have a single-ended ADC or to invest in higher-performance parts, but these are not yet important enough to look for different parts. At the time of the project, both parts are active and in stock in Digikey.

**Chosen parts:** ADC141S616CIMM/NOPB (14-bit, 50-250kSPS, differential) and DAC7563SDGSR (12-bit, single-ended).

## Analogue sections

OPAmp part is the same as the reference design.

**Chosen part:** MCP6001
