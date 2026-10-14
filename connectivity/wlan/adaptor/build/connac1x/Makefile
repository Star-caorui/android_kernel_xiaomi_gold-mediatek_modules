# Where this repository is checked out; MediaTek's own build has it at
# vendor/mediatek/kernel_modules next to the output directory.
MTK_KERNEL_MODULES_PATH ?= $(OUT_DIR)/../vendor/mediatek/kernel_modules

include $(wildcard $(KERNEL_SRC)/$(DEVICE_MODULES_REL_DIR)/Makefile.include)

EXTRA_SYMBOLS += $(MTK_KERNEL_MODULES_PATH)/connectivity/common/Module.symvers
# conninfra is not built for CONNAC 1.x chips (MT6833, MT6768 ...)
EXTRA_SYMBOLS += $(wildcard $(MTK_KERNEL_MODULES_PATH)/connectivity/conninfra/Module.symvers)

modules modules_install clean:
	$(MAKE) -C $(KERNEL_SRC) M=$(M) $(KBUILD_OPTIONS) KBUILD_EXTRA_SYMBOLS="$(EXTRA_SYMBOLS)" $(@)
