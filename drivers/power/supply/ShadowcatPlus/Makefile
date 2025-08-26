#+chk2828, fangduozhu, add, 20210908, for ato charging capacity control
ifeq ($(WT_COMPILE_FACTORY_VERSION),yes)
    ccflags-y += -DWT_COMPILE_FACTORY_VERSION
endif
#-chk2828, fangduozhu, add, 20210908, for ato charging capacity control
#zhiqing.liu add, SCP-3679, RDX version charging capacity control, 20220105 begin
ifeq ($(HMD_DEMO_SUPPORT),true)
    ccflags-y += -DHMD_DEMO_SUPPORT
endif
#zhiqing.liu add, SCP-3679, RDX version charging capacity control, 20220105 end

power_supply-y := power_supply_core.o
power_supply-$(CONFIG_SYSFS) += power_supply_sysfs.o
power_supply-$(CONFIG_LEDS_TRIGGERS)	+= power_supply_leds.o
obj-$(CONFIG_POWER_SUPPLY)	+= power_supply.o

obj-$(CONFIG_FUEL_GAUGE_SC27XX) += sc27xx_fuel_gauge.o sprd_battery_info.o
obj-$(CONFIG_CHARGER_MANAGER) += charger-manager.o sprd_vote.o
obj-$(CONFIG_FAST_CHARGER_SC2730) += sc2730_fast_charger.o
obj-$(CONFIG_CHARGER_BQ25890)	+= bq25890_charger.o

