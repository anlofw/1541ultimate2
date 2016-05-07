
CROSS	     = nios2-elf-
ELFTYPE      = elf32-littlenios2
ARCHITECTURE = nios2

include ../common/environment.mk

PRJ      =  ultimate
FINAL    =  $(RESULT)/$(PRJ).bin $(RESULT)/$(PRJ).elf $(OUTPUT)/$(PRJ).sim

SRCS_C   =	itu.c \
			dump_hex.c \
			assert.c \
			profiler.c \
			croutine.c \
            event_groups.c \
            list.c \
            queue.c \
            tasks.c \
            timers.c \
            port.c \
            heap_3.c \
            ff2.c \
            ccsbcs.c \
            ffsyscall.c \
            time.c \
            i2c.c \
            mdio.c \
            nios_main.c
            
SRCS_CC	 =  small_printf.cc \
            stream.cc \
			stream_uart.cc \
			memory_rtos.cc \
			init_function.cc \
			flash.cc \
			at45_flash.cc \
			w25q_flash.cc \
			s25fl_flash.cc \
			config.cc \
			filemanager.cc \
			file_device.cc \
			file_partition.cc \
			embedded_d64.cc \
			embedded_t64.cc \
			embedded_iso.cc \
			embedded_fat.cc \
			rtc.cc \
			c64.cc \
			c64_subsys.cc \
			screen.cc \
			keyboard_c64.cc \
			disk_image.cc \
			c1541.cc \
			bam_header.cc \
			mystring.cc \
			path.cc \
			pattern.cc \
			blockdev.cc \
			blockdev_file.cc \
			blockdev_ram.cc \
			disk.cc \
			partition.cc \
			file_system.cc \
			diskio.cc \
			directory.cc \
			file.cc \
			filesystem_iso9660.cc \
            filesystem_root.cc \
			filesystem_d64.cc \
			filesystem_t64.cc \
			filesystem_fat.cc \
			sd_card.cc \
			sdio.cc \
			sdcard_manager.cc \
			size_str.cc \
			userinterface.cc \
			ui_elements.cc \
            user_file_interaction.cc \
			editor.cc \
			ui_stream.cc \
			tree_browser.cc \
			tree_browser_state.cc \
			stream_menu.cc \
			config_menu.cc \
			context_menu.cc \
			task_menu.cc \
			audio_select.cc \
			filetype_d64.cc \
			filetype_g64.cc \
			filetype_prg.cc \
			filetype_u2u.cc \
			filetype_reu.cc \
			filetype_crt.cc \
			filetype_sid.cc \
            host_stream.cc \
            keyboard_vt100.cc \
            screen_vt100.cc \
			usb_base.cc \
			usb2.cc \
			usb_device.cc \
			usb_scsi.cc \
			usb_hub.cc \
			usb_ax88772.cc \
			usb_em1010.cc \
			network_interface.cc \
			network_lwip.cc \
			vfs.cc \
			ftpd.cc \
			tape_controller.cc \
			tape_recorder.cc \
			command_intf.cc \
			dos.cc \
			network_target.cc \
			iec.cc \
			filetype_tap.cc \
            socket_stream.cc \
            socket_gui.cc \
			socket_test.cc \
			$(PRJ).cc

VPATH +=	$(PATH_SW)/FreeRTOS/Source/portable/nios_sigma
VPATH +=	$(PATH_SW)/niosbsp
VPATH +=	$(PATH_SW)/niosbsp/HAL/inc
VPATH +=	$(PATH_SW)/niosbsp/drivers/inc

#            sock_echo.c \
#			sys_calls.cc \
####			sampler.cc \
####			copper.cc \


SRCS_ASM =

SRCS_ASMS = port_asm.S

SRCS_6502 = sidcrt.tas bootcrt.tas cmd_test_rom.tas ulticopy.tas

SRCS_BIN =  chars.bin 1541.bin 1541c.bin 1541-ii.bin sounds.bin module.bin

SRCS_IEC = iec_code.iec

SRCS_NANO = nano_minimal.nan

PATH_INC =  $(addprefix -I, $(VPATH))
OPTIONS  = -g -ffunction-sections -O0 -DOS  -Wno-write-strings -mno-hw-div -mno-hw-mul -mno-hw-mulx
COPTIONS = $(OPTIONS) -std=gnu99
CPPOPT   = $(OPTIONS) -fno-exceptions -fno-rtti -fno-threadsafe-statics -fpermissive
LINK 	 = ./mb_app.lds
LLIB     =  -L $(PATH_SW)/niosbsp \
			-L ../nios2_elf_lwip/result \
            -L $(NIOS_TOOLCHAIN)/nios2-elf/lib \
            -L $(NIOS_TOOLCHAIN)/lib/gcc/nios2-elf/4.8.3
LIBS     =  -lc -lhal_bsp -llwip -lc -lgcc 
LFLAGS   = --gc-sections 

include ../common/rules.mk