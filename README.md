# Game-crashed
I don't understand how to fix it
---- Minecraft Crash Report ----
// Daisy, daisy...

Time: 3/15/22, 10:24 PM
Description: Initializing game

java.lang.RuntimeException: Could not execute entrypoint stage 'main' due to errors, provided by 'dynamicfps'!
	at net.fabricmc.loader.impl.entrypoint.EntrypointUtils.lambda$invoke0$0(EntrypointUtils.java:51)
	at net.fabricmc.loader.impl.util.ExceptionUtil.gatherExceptions(ExceptionUtil.java:33)
	at net.fabricmc.loader.impl.entrypoint.EntrypointUtils.invoke0(EntrypointUtils.java:49)
	at net.fabricmc.loader.impl.entrypoint.EntrypointUtils.invoke(EntrypointUtils.java:35)
	at net.fabricmc.loader.impl.game.minecraft.Hooks.startClient(Hooks.java:52)
	at net.minecraft.class_310.<init>(class_310.java:452)
	at net.minecraft.client.main.Main.main(Main.java:199)
	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:77)
	at java.base/jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
	at java.base/java.lang.reflect.Method.invoke(Method.java:568)
	at net.fabricmc.loader.impl.game.minecraft.MinecraftGameProvider.launch(MinecraftGameProvider.java:416)
	at net.fabricmc.loader.impl.launch.knot.Knot.launch(Knot.java:77)
	at net.fabricmc.loader.impl.launch.knot.KnotClient.main(KnotClient.java:23)
	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:77)
	at java.base/jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
	at java.base/java.lang.reflect.Method.invoke(Method.java:568)
	at org.multimc.onesix.OneSixLauncher.launchWithMainClass(OneSixLauncher.java:210)
	at org.multimc.onesix.OneSixLauncher.launch(OneSixLauncher.java:245)
	at org.multimc.EntryPoint.listen(EntryPoint.java:143)
	at org.multimc.EntryPoint.main(EntryPoint.java:34)
	Suppressed: java.lang.RuntimeException: Failed to initialize REI entry point: me.shedaniel.rei.RoughlyEnoughItemsCore
		at me.shedaniel.rei.RoughlyEnoughItemsInitializer.initializeEntryPoint(RoughlyEnoughItemsInitializer.java:86)
		at me.shedaniel.rei.RoughlyEnoughItemsInitializer.onInitialize(RoughlyEnoughItemsInitializer.java:46)
		at java.base/java.lang.invoke.MethodHandleProxies$1.invoke(MethodHandleProxies.java:198)
		at jdk.proxy2/com.sun.proxy.jdk.proxy2.$Proxy31.onInitialize(Unknown Source)
		at net.fabricmc.loader.impl.entrypoint.EntrypointUtils.invoke0(EntrypointUtils.java:47)
		... 19 more
	Caused by: java.lang.ExceptionInInitializerError
		at java.base/java.lang.Class.forName0(Native Method)
		at java.base/java.lang.Class.forName(Class.java:375)
		at me.shedaniel.rei.RoughlyEnoughItemsInitializer.initializeEntryPoint(RoughlyEnoughItemsInitializer.java:63)
		... 23 more
	Caused by: java.lang.NullPointerException: Cannot invoke "me.shedaniel.autoconfig.ConfigData.validatePostLoad()" because "this.config" is null
		at me.shedaniel.autoconfig.ConfigManager.load(ConfigManager.java:106)
		at me.shedaniel.autoconfig.ConfigManager.<init>(ConfigManager.java:53)
		at me.shedaniel.autoconfig.AutoConfig.register(AutoConfig.java:66)
		at me.shedaniel.rei.impl.client.config.ConfigManagerImpl.<init>(ConfigManagerImpl.java:100)
		at me.shedaniel.rei.RoughlyEnoughItemsCoreClient.attachClientInternals(RoughlyEnoughItemsCoreClient.java:202)
		at dev.architectury.utils.EnvExecutor.runInEnv(EnvExecutor.java:35)
		at me.shedaniel.rei.RoughlyEnoughItemsCore.<clinit>(RoughlyEnoughItemsCore.java:86)
		... 26 more
	Suppressed: java.lang.NoClassDefFoundError: Could not initialize class net.minecraft.class_3675
		at com.misterpemodder.shulkerboxtooltip.impl.util.Key.<clinit>(Key.java:12)
		at com.misterpemodder.shulkerboxtooltip.impl.config.Configuration$ControlsCategory.<init>(Configuration.java:219)
		at com.misterpemodder.shulkerboxtooltip.impl.config.Configuration.<init>(Configuration.java:40)
		at com.misterpemodder.shulkerboxtooltip.impl.config.ShulkerBoxTooltipConfigSerializer.fromJson(ShulkerBoxTooltipConfigSerializer.java:74)
		at me.shedaniel.cloth.clothconfig.shadowed.blue.endless.jankson.api.DeserializerFunction.deserialize(DeserializerFunction.java:38)
		at me.shedaniel.cloth.clothconfig.shadowed.blue.endless.jankson.impl.serializer.DeserializerFunctionPool.apply(DeserializerFunctionPool.java:72)
		at me.shedaniel.cloth.clothconfig.shadowed.blue.endless.jankson.impl.MarshallerImpl.marshall(MarshallerImpl.java:201)
		at me.shedaniel.cloth.clothconfig.shadowed.blue.endless.jankson.impl.MarshallerImpl.marshallCarefully(MarshallerImpl.java:187)
		at me.shedaniel.cloth.clothconfig.shadowed.blue.endless.jankson.Jankson.fromJsonCarefully(Jankson.java:287)
		at com.misterpemodder.shulkerboxtooltip.impl.config.ShulkerBoxTooltipConfigSerializer.deserialize(ShulkerBoxTooltipConfigSerializer.java:163)
		at com.misterpemodder.shulkerboxtooltip.impl.config.ShulkerBoxTooltipConfigSerializer.deserialize(ShulkerBoxTooltipConfigSerializer.java:29)
		at me.shedaniel.autoconfig.ConfigManager.load(ConfigManager.java:92)
		at me.shedaniel.autoconfig.ConfigManager.<init>(ConfigManager.java:53)
		at me.shedaniel.autoconfig.AutoConfig.register(AutoConfig.java:66)
		at com.misterpemodder.shulkerboxtooltip.impl.config.ConfigurationHandler.register(ConfigurationHandler.java:59)
		at com.misterpemodder.shulkerboxtooltip.impl.ShulkerBoxTooltip.onInitialize(ShulkerBoxTooltip.java:53)
		at net.fabricmc.loader.impl.entrypoint.EntrypointUtils.invoke0(EntrypointUtils.java:47)
		... 19 more
Caused by: java.lang.ExceptionInInitializerError
	at dynamicfps.util.KeyBindingHandler.<init>(KeyBindingHandler.java:15)
	at dynamicfps.DynamicFPSMod.<clinit>(DynamicFPSMod.java:29)
	at java.base/java.lang.Class.forName0(Native Method)
	at java.base/java.lang.Class.forName(Class.java:467)
	at net.fabricmc.loader.impl.util.DefaultLanguageAdapter.create(DefaultLanguageAdapter.java:50)
	at net.fabricmc.loader.impl.entrypoint.EntrypointStorage$NewEntry.getOrCreate(EntrypointStorage.java:117)
	at net.fabricmc.loader.impl.entrypoint.EntrypointContainerImpl.getEntrypoint(EntrypointContainerImpl.java:53)
	at net.fabricmc.loader.impl.entrypoint.EntrypointUtils.invoke0(EntrypointUtils.java:47)
	... 19 more
Caused by: java.lang.RuntimeException: java.lang.UnsatisfiedLinkError: Failed to locate library: glfw.dll
	at net.minecraft.class_3675.<clinit>(class_3675.java:46)
	... 27 more
Caused by: java.lang.UnsatisfiedLinkError: Failed to locate library: glfw.dll
	at org.lwjgl.system.Library.loadNative(Library.java:299)
	at org.lwjgl.system.Library.loadNative(Library.java:205)
	at org.lwjgl.glfw.GLFW.<clinit>(GLFW.java:674)
	at java.base/jdk.internal.misc.Unsafe.ensureClassInitialized0(Native Method)
	at java.base/jdk.internal.misc.Unsafe.ensureClassInitialized(Unsafe.java:1155)
	at java.base/java.lang.invoke.DirectMethodHandle$EnsureInitialized.computeValue(DirectMethodHandle.java:377)
	at java.base/java.lang.invoke.DirectMethodHandle$EnsureInitialized.computeValue(DirectMethodHandle.java:374)
	at java.base/java.lang.ClassValue.getFromHashMap(ClassValue.java:228)
	at java.base/java.lang.ClassValue.getFromBackup(ClassValue.java:210)
	at java.base/java.lang.ClassValue.get(ClassValue.java:116)
	at java.base/java.lang.invoke.DirectMethodHandle.checkInitialized(DirectMethodHandle.java:400)
	at java.base/java.lang.invoke.DirectMethodHandle.ensureInitialized(DirectMethodHandle.java:388)
	at java.base/java.lang.invoke.DirectMethodHandle.ensureInitialized(DirectMethodHandle.java:422)
	at net.minecraft.class_3675.<clinit>(class_3675.java:43)
	... 27 more


A detailed walkthrough of the error, its code path and all known details is as follows:
---------------------------------------------------------------------------------------

-- Head --
Thread: Render thread
Stacktrace:
	at net.fabricmc.loader.impl.entrypoint.EntrypointUtils.lambda$invoke0$0(EntrypointUtils.java:51)
	at net.fabricmc.loader.impl.util.ExceptionUtil.gatherExceptions(ExceptionUtil.java:33)
	at net.fabricmc.loader.impl.entrypoint.EntrypointUtils.invoke0(EntrypointUtils.java:49)
	at net.fabricmc.loader.impl.entrypoint.EntrypointUtils.invoke(EntrypointUtils.java:35)
	at net.fabricmc.loader.impl.game.minecraft.Hooks.startClient(Hooks.java:52)
	at net.minecraft.class_310.<init>(class_310.java:452)

-- Initialization --
Details:
	Modules: 
		ADVAPI32.dll:Расширенная библиотека API Windows 32:10.0.19041.1586 (WinBuild.160101.0800):Microsoft Corporation
		COMCTL32.dll:Библиотека элементов управления взаимодействия с пользователем:6.10 (WinBuild.160101.0800):Microsoft Corporation
		CRYPT32.dll:API32 криптографии:10.0.19041.1586 (WinBuild.160101.0800):Microsoft Corporation
		CRYPTBASE.dll:Base cryptographic API DLL:10.0.19041.546 (WinBuild.160101.0800):Microsoft Corporation
		CRYPTSP.dll:Cryptographic Service Provider API:10.0.19041.546 (WinBuild.160101.0800):Microsoft Corporation
		DBGHELP.DLL:Windows Image Helper:10.0.19041.867 (WinBuild.160101.0800):Microsoft Corporation
		DNSAPI.dll:Динамическая библиотека API DNS-клиента:10.0.19041.1586 (WinBuild.160101.0800):Microsoft Corporation
		GDI32.dll:GDI Client DLL:10.0.19041.1202 (WinBuild.160101.0800):Microsoft Corporation
		IMM32.DLL:Multi-User Windows IMM32 API Client DLL:10.0.19041.546 (WinBuild.160101.0800):Microsoft Corporation
		IPHLPAPI.DLL:API вспомогательного приложения IP:10.0.19041.1586 (WinBuild.160101.0800):Microsoft Corporation
		KERNEL32.DLL:Библиотека клиента Windows NT BASE API:10.0.19041.1503 (WinBuild.160101.0800):Microsoft Corporation
		KERNELBASE.dll:Библиотека клиента Windows NT BASE API:10.0.19041.1503 (WinBuild.160101.0800):Microsoft Corporation
		MpOav.dll:IOfficeAntiVirus Module:4.18.2202.4 (WinBuild.160101.0800):Microsoft Corporation
		NLAapi.dll:Network Location Awareness 2:10.0.19041.1151 (WinBuild.160101.0800):Microsoft Corporation
		NSI.dll:NSI User-mode interface DLL:10.0.19041.610 (WinBuild.160101.0800):Microsoft Corporation
		NTASN1.dll:Microsoft ASN.1 API:10.0.19041.320 (WinBuild.160101.0800):Microsoft Corporation
		Ole32.dll:Microsoft OLE для Windows:10.0.19041.1586 (WinBuild.160101.0800):Microsoft Corporation
		OleAut32.dll:OLEAUT32.DLL:10.0.19041.985 (WinBuild.160101.0800):Microsoft Corporation
		PSAPI.DLL:Process Status Helper:10.0.19041.546 (WinBuild.160101.0800):Microsoft Corporation
		Pdh.dll:Модуль поддержки данных производительности Windows:10.0.19041.1586 (WinBuild.160101.0800):Microsoft Corporation
		RPCRT4.dll:Библиотека удаленного вызова процедур:10.0.19041.1586 (WinBuild.160101.0800):Microsoft Corporation
		SHCORE.dll:SHCORE:10.0.19041.1586 (WinBuild.160101.0800):Microsoft Corporation
		SHELL32.dll:Общая библиотека оболочки Windows:10.0.19041.1586 (WinBuild.160101.0800):Microsoft Corporation
		USER32.dll:Многопользовательская библиотека клиента USER API Windows:10.0.19041.1586 (WinBuild.160101.0800):Microsoft Corporation
		USERENV.dll:Userenv:10.0.19041.1586 (WinBuild.160101.0800):Microsoft Corporation
		VCRUNTIME140.dll:Microsoft® C Runtime Library:14.28.29913.0 built by: vcwrkspc:Microsoft Corporation
		VERSION.dll:Version Checking and File Installation Libraries:10.0.19041.546 (WinBuild.160101.0800):Microsoft Corporation
		WINHTTP.dll:Службы HTTP Windows:10.0.19041.1586 (WinBuild.160101.0800):Microsoft Corporation
		WINMM.dll:MCI API DLL:10.0.19041.1586 (WinBuild.160101.0800):Microsoft Corporation
		WS2_32.dll:32-разрядная библиотека Windows Socket 2.0:10.0.19041.1081 (WinBuild.160101.0800):Microsoft Corporation
		WSOCK32.dll:Windows Socket 32-Bit DLL:10.0.19041.1586 (WinBuild.160101.0800):Microsoft Corporation
		Wldp.dll:Политика блокировки Windows:10.0.19041.1586 (WinBuild.160101.0800):Microsoft Corporation
		amsi.dll:Anti-Malware Scan Interface:10.0.19041.746 (WinBuild.160101.0800):Microsoft Corporation
		bcrypt.dll:Библиотека криптографических примитивов Windows:10.0.19041.1586 (WinBuild.160101.0800):Microsoft Corporation
		bcryptPrimitives.dll:Windows Cryptographic Primitives Library:10.0.19041.1415 (WinBuild.160101.0800):Microsoft Corporation
		clbcatq.dll:COM+ Configuration Catalog:2001.12.10941.16384 (WinBuild.160101.0800):Microsoft Corporation
		combase.dll:Microsoft COM для Windows:10.0.19041.1586 (WinBuild.160101.0800):Microsoft Corporation
		dbgcore.DLL:Windows Core Debugging Helpers:10.0.19041.789 (WinBuild.160101.0800):Microsoft Corporation
		dhcpcsvc.DLL:Служба DHCP-клиента:10.0.19041.1586 (WinBuild.160101.0800):Microsoft Corporation
		dhcpcsvc6.DLL:Клиент DHCPv6:10.0.19041.1586 (WinBuild.160101.0800):Microsoft Corporation
		fwpuclnt.dll:API пользовательского режима FWP/IPsec:10.0.19041.1586 (WinBuild.160101.0800):Microsoft Corporation
		gdi32full.dll:GDI Client DLL:10.0.19041.1466 (WinBuild.160101.0800):Microsoft Corporation
		java.dll:Java(TM) Platform SE binary:17.0.2.0:Oracle Corporation
		javaw.exe:Java(TM) Platform SE binary:17.0.2.0:Oracle Corporation
		jimage.dll:Java(TM) Platform SE binary:17.0.2.0:Oracle Corporation
		jli.dll:Java(TM) Platform SE binary:17.0.2.0:Oracle Corporation
		jna15954815765539870871.dll:JNA native library:6.1.1:Java(TM) Native Access (JNA)
		jsvml.dll:Java(TM) Platform SE binary:17.0.2.0:Oracle Corporation
		jvm.dll:Java HotSpot(TM) 64-Bit server VM:17.0.2.0:Oracle Corporation
		kernel.appcore.dll:AppModel API Host:10.0.19041.546 (WinBuild.160101.0800):Microsoft Corporation
		lwjgl.dll
		management.dll:Java(TM) Platform SE binary:17.0.2.0:Oracle Corporation
		management_ext.dll:Java(TM) Platform SE binary:17.0.2.0:Oracle Corporation
		msvcp140.dll:Microsoft® C Runtime Library:14.28.29913.0 built by: vcwrkspc:Microsoft Corporation
		msvcp_win.dll:Microsoft® C Runtime Library:10.0.19041.789 (WinBuild.160101.0800):Microsoft Corporation
		msvcrt.dll:Windows NT CRT DLL:7.0.19041.546 (WinBuild.160101.0800):Microsoft Corporation
		mswsock.dll:Расширение поставщика службы API Microsoft Windows Sockets 2.0:10.0.19041.1586 (WinBuild.160101.0800):Microsoft Corporation
		napinsp.dll:Поставщик оболочки совместимости для имен электронной почты:10.0.19041.1586 (WinBuild.160101.0800):Microsoft Corporation
		ncrypt.dll:Маршрутизатор Windows NCrypt:10.0.19041.1586 (WinBuild.160101.0800):Microsoft Corporation
		net.dll:Java(TM) Platform SE binary:17.0.2.0:Oracle Corporation
		nio.dll:Java(TM) Platform SE binary:17.0.2.0:Oracle Corporation
		ntdll.dll:Системная библиотека NT:10.0.19041.1466 (WinBuild.160101.0800):Microsoft Corporation
		perfos.dll:Библиотека объектов производительности системы Windows:10.0.19041.1586 (WinBuild.160101.0800):Microsoft Corporation
		pnrpnsp.dll:Поставщик пространства имен PNRP:10.0.19041.1586 (WinBuild.160101.0800):Microsoft Corporation
		profapi.dll:User Profile Basic API:10.0.19041.844 (WinBuild.160101.0800):Microsoft Corporation
		rasadhlp.dll:Remote Access AutoDial Helper:10.0.19041.546 (WinBuild.160101.0800):Microsoft Corporation
		rsaenh.dll:Microsoft Enhanced Cryptographic Provider:10.0.19041.320 (WinBuild.160101.0800):Microsoft Corporation
		sechost.dll:Host for SCM/SDDL/LSA Lookup APIs:10.0.19041.320 (WinBuild.160101.0800):Microsoft Corporation
		shlwapi.dll:Библиотека небольших программ оболочки:10.0.19041.1586 (WinBuild.160101.0800):Microsoft Corporation
		sunmscapi.dll:Java(TM) Platform SE binary:17.0.2.0:Oracle Corporation
		ucrtbase.dll:Microsoft® C Runtime Library:10.0.19041.789 (WinBuild.160101.0800):Microsoft Corporation
		vcruntime140_1.dll:Microsoft® C Runtime Library:14.28.29913.0 built by: vcwrkspc:Microsoft Corporation
		verify.dll:Java(TM) Platform SE binary:17.0.2.0:Oracle Corporation
		win32u.dll:Win32u:10.0.19041.1526 (WinBuild.160101.0800):Microsoft Corporation
		windows.storage.dll:API хранения Microsoft WinRT:10.0.19041.1586 (WinBuild.160101.0800):Microsoft Corporation
		winrnr.dll:LDAP RnR Provider DLL:10.0.19041.546 (WinBuild.160101.0800):Microsoft Corporation
		wshbth.dll:Windows Sockets Helper DLL:10.0.19041.546 (WinBuild.160101.0800):Microsoft Corporation
		zip.dll:Java(TM) Platform SE binary:17.0.2.0:Oracle Corporation
Stacktrace:
	at net.minecraft.client.main.Main.main(Main.java:199)
	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:77)
	at java.base/jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
	at java.base/java.lang.reflect.Method.invoke(Method.java:568)
	at net.fabricmc.loader.impl.game.minecraft.MinecraftGameProvider.launch(MinecraftGameProvider.java:416)
	at net.fabricmc.loader.impl.launch.knot.Knot.launch(Knot.java:77)
	at net.fabricmc.loader.impl.launch.knot.KnotClient.main(KnotClient.java:23)
	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:77)
	at java.base/jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
	at java.base/java.lang.reflect.Method.invoke(Method.java:568)
	at org.multimc.onesix.OneSixLauncher.launchWithMainClass(OneSixLauncher.java:210)
	at org.multimc.onesix.OneSixLauncher.launch(OneSixLauncher.java:245)
	at org.multimc.EntryPoint.listen(EntryPoint.java:143)
	at org.multimc.EntryPoint.main(EntryPoint.java:34)

-- System Details --
Details:
	Minecraft Version: 1.18.1
	Minecraft Version ID: 1.18.1
	Operating System: Windows 10 (amd64) version 10.0
	Java Version: 17.0.2, Oracle Corporation
	Java VM Version: Java HotSpot(TM) 64-Bit Server VM (mixed mode, sharing), Oracle Corporation
	Memory: 347664896 bytes (331 MiB) / 1572864000 bytes (1500 MiB) up to 4026531840 bytes (3840 MiB)
	CPUs: 2
	Processor Vendor: GenuineIntel
	Processor Name: Intel(R) Pentium(R) CPU 3550M @ 2.30GHz
	Identifier: Intel64 Family 6 Model 60 Stepping 3
	Microarchitecture: Haswell (Client)
	Frequency (GHz): 2.30
	Number of physical packages: 1
	Number of physical CPUs: 2
	Number of logical CPUs: 2
	Graphics card #0 name: NVIDIA GeForce GT 820M
	Graphics card #0 vendor: NVIDIA (0x10de)
	Graphics card #0 VRAM (MB): 2048.00
	Graphics card #0 deviceId: 0x1140
	Graphics card #0 versionInfo: DriverVersion=21.21.13.7654
	Graphics card #1 name: Intel(R) HD Graphics
	Graphics card #1 vendor: Intel Corporation (0x8086)
	Graphics card #1 VRAM (MB): 1024.00
	Graphics card #1 deviceId: 0x0406
	Graphics card #1 versionInfo: DriverVersion=20.19.15.4835
	Memory slot #0 capacity (MB): 4096.00
	Memory slot #0 clockSpeed (GHz): 1.60
	Memory slot #0 type: DDR3
	Virtual memory max (MB): 24020.27
	Virtual memory used (MB): 4532.71
	Swap memory total (MB): 20000.00
	Swap memory used (MB): 297.56
	JVM Flags: 3 total; -XX:HeapDumpPath=MojangTricksIntelDriversForPerformance_javaw.exe_minecraft.exe.heapdump -Xms512m -Xmx3840m
	Fabric Mods: 
		architectury: Architectury 3.7.31
		autoreconnect: AutoReconnect 1.3.2
		blue_endless_jankson: jankson 1.2.1
		cloth-basic-math: cloth-basic-math 0.6.0
		cloth-config: Cloth Config v6 6.2.57
		cmdkeybind: Command Macros 1.5.3-1.18
		com_moandjiezana_toml_toml4j: toml4j 0.7.2
		drippyloadingscreen: Drippy Loading Screen 1.5.1
		dynamicfps: Dynamic FPS 2.1.0
		fabric: Fabric API 0.46.6+1.18
		fabric-api-base: Fabric API Base 0.4.2+d7c144a865
		fabric-api-lookup-api-v1: Fabric API Lookup API (v1) 1.5.3+d7c144a865
		fabric-biome-api-v1: Fabric Biome API (v1) 6.0.2+d7c144a865
		fabric-blockrenderlayer-v1: Fabric BlockRenderLayer Registration (v1) 1.1.10+3ac43d9565
		fabric-command-api-v1: Fabric Command API (v1) 1.1.7+d7c144a865
		fabric-commands-v0: Fabric Commands (v0) 0.2.6+b4f4f6cd65
		fabric-containers-v0: Fabric Containers (v0) 0.1.19+d7c144a865
		fabric-content-registries-v0: Fabric Content Registries (v0) 0.4.9+d7c144a865
		fabric-crash-report-info-v1: Fabric Crash Report Info (v1) 0.1.9+3ac43d9565
		fabric-dimensions-v1: Fabric Dimensions API (v1) 2.1.10+a1d9bbf565
		fabric-entity-events-v1: Fabric Entity Events (v1) 1.4.6+d7c144a865
		fabric-events-interaction-v0: Fabric Events Interaction (v0) 0.4.17+d7c144a865
		fabric-events-lifecycle-v0: Fabric Events Lifecycle (v0) 0.2.9+d7c144a865
		fabric-game-rule-api-v1: Fabric Game Rule API (v1) 1.0.11+d7c144a865
		fabric-item-api-v1: Fabric Item API (v1) 1.3.1+691a79b565
		fabric-item-groups-v0: Fabric Item Groups (v0) 0.3.7+3ac43d9565
		fabric-key-binding-api-v1: Fabric Key Binding API (v1) 1.0.9+d7c144a865
		fabric-keybindings-v0: Fabric Key Bindings (v0) 0.2.7+b4f4f6cd65
		fabric-lifecycle-events-v1: Fabric Lifecycle Events (v1) 1.4.13+713c266865
		fabric-loot-tables-v1: Fabric Loot Tables (v1) 1.0.9+d7c144a865
		fabric-mining-level-api-v1: Fabric Mining Level API (v1) 1.0.7+d7c144a865
		fabric-mining-levels-v0: Fabric Mining Levels (v0) 0.1.12+b4f4f6cd65
		fabric-models-v0: Fabric Models (v0) 0.3.4+d7c144a865
		fabric-networking-api-v1: Fabric Networking API (v1) 1.0.19+d7c144a865
		fabric-networking-v0: Fabric Networking (v0) 0.3.6+b4f4f6cd65
		fabric-object-builder-api-v1: Fabric Object Builder API (v1) 1.11.5+737332ce65
		fabric-object-builders-v0: Fabric Object Builders (v0) 0.7.13+d7c144a865
		fabric-particles-v1: Fabric Particles (v1) 0.2.10+526dc1ac65
		fabric-registry-sync-v0: Fabric Registry Sync (v0) 0.9.2+ad01bfbd65
		fabric-renderer-api-v1: Fabric Renderer API (v1) 0.4.11+b0b66fc365
		fabric-renderer-indigo: Fabric Renderer - Indigo 0.4.15+6825030165
		fabric-renderer-registries-v1: Fabric Renderer Registries (v1) 3.2.10+b4f4f6cd65
		fabric-rendering-data-attachment-v1: Fabric Rendering Data Attachment (v1) 0.3.5+d7c144a865
		fabric-rendering-fluids-v1: Fabric Rendering Fluids (v1) 0.1.19+3ac43d9565
		fabric-rendering-v0: Fabric Rendering (v0) 1.1.12+b4f4f6cd65
		fabric-rendering-v1: Fabric Rendering (v1) 1.10.6+713c266865
		fabric-resource-conditions-api-v1: Fabric Resource Conditions API (v1) 1.0.2+d7c144a865
		fabric-resource-loader-v0: Fabric Resource Loader (v0) 0.4.15+8906aafd65
		fabric-screen-api-v1: Fabric Screen API (v1) 1.0.8+d7c144a865
		fabric-screen-handler-api-v1: Fabric Screen Handler API (v1) 1.1.12+d7c144a865
		fabric-structure-api-v1: Fabric Structure API (v1) 2.1.3+d7c144a865
		fabric-tag-extensions-v0: Fabric Tag Extensions (v0) 1.2.9+d7c144a865
		fabric-textures-v0: Fabric Textures (v0) 1.0.10+3ac43d9565
		fabric-tool-attribute-api-v1: Fabric Tool Attribute API (v1) 1.3.9+fb3b57b465
		fabric-transfer-api-v1: Fabric Transfer API (v1) 1.5.10+c329913d65
		fabricloader: Fabric Loader 0.13.3
		fastchest: FastChest 1.2+1.18
		itemscroller: Item Scroller 0.16.0
		java: Java HotSpot(TM) 64-Bit Server VM 17
		konkrete: Konkrete 1.3.3
		kyrptconfig: Kyrpt Config 1.2.6-1.18
		litematica: Litematica 0.10.4
		lithium: Lithium 0.7.8
		malilib: MaLiLib 0.11.8
		minecraft: Minecraft 1.18.1
		minihud: MiniHUD 0.21.5
		mm: Manningham Mills 2.3
		modmenu: Mod Menu 3.0.1
		org_joml_joml: joml 1.10.2
		phosphor: Phosphor 0.8.1
		roughlyenoughitems: Roughly Enough Items 7.3.443
		shulkerboxtooltip: Shulker Box Tooltip 3.0.5+1.18
		sodium: Sodium 0.4.0-alpha6+build.14
		tweakeroo: Tweakeroo 0.12.3
	Launched Version: MultiMC5
	Backend library: LWJGL version 3.2.2 build 10
	Backend API: Unknown
	Window size: <not initialized>
	GL Caps: Using framebuffer using OpenGL 3.2
	GL debug messages: <disabled>
	Using VBOs: Yes
	Is Modded: Definitely; Client brand changed to 'fabric'
	Type: Client (map_client.txt)
	CPU: <unknown>
