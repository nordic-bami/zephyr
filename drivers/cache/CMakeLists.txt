# SPDX-License-Identifier: Apache-2.0

zephyr_syscall_header(${ZEPHYR_BASE}/include/zephyr/cache.h)

zephyr_library()
zephyr_library_property(ALLOW_EMPTY TRUE)

zephyr_library_sources_ifdef(CONFIG_CACHE_ASPEED	cache_aspeed.c)
zephyr_library_sources_ifdef(CONFIG_CACHE_ANDES 	cache_andes.c)
zephyr_library_sources_ifdef(CONFIG_USERSPACE		cache_handlers.c)
zephyr_library_sources_ifdef(CONFIG_CACHE_NRF_CACHE	cache_nrf.c)
zephyr_library_sources_ifdef(CONFIG_CACHE_NXP_XCACHE	cache_nxp_xcache.c)
zephyr_library_sources_ifdef(CONFIG_CACHE_STM32	cache_stm32.c)
