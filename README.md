# Bienvenido al repositorio oficial de ReinierTutoriales
[![X570 AORUS ELITE](https://static.gigabyte.com/StaticFile/Image/Global/907eecfe94da125eb443dc223715d8cd/Product/22419/webp/1000 "X570 AORUS ELITE")](https://static.gigabyte.com/StaticFile/Image/Global/907eecfe94da125eb443dc223715d8cd/Product/22419/webp/1000 "X570 AORUS ELITE")
## **Qu茅 contiene este repositorio  馃憞**
Este repositorio contiene el directorio EFI para el combo Ryzen 5 3600 y MotherBoard Gigabyte X570 Aorus Elite.
## Especificaci贸n de mi PC
- **MotherBoard**: [Gigabyte X570 Aorus Elite](https://amzn.to/30KCO2k "Gigabyte X570 Aorus Elite")
- **Procesador**: [Ryzen 5 3600](https://amzn.to/3JdS2yj "Ryzen 5 3600")
- **RAM**: [32GB Corsair Vengeance RGB Pro (2 x 16 GB)DDR4 3600(PC4-28800)memoria optimizada AMD](https://amzn.to/3mgZY7O "32GB Corsair Vengeance RGB Pro (2 x 16 GB)DDR4 3600(PC4-28800)memoria optimizada AMD")
- **BT / WIFI**: [Fenvi T919 (BCM94360CD)](https://amzn.to/3p89Mmw "Fenvi T919 (BCM94360CD)")
## Estructura EFI
### Recomendaci贸n
- Te recomiendo que uses esto solo como un recurso de referencia.
- Este EFI contiene kexts adicionales en config.plist en lugar de solo las cosas esenciales para la CPU X570 + Zen2. Debe eliminarlos antes de usar esto en su PC.

### Verifique esto antes de usar
En el archivo config.plist , genere c贸digos de serie nuevos ya que este carece de ellos, pues son personales y cada Mac necesita los de ella propios. Para generar la clave de serie, consulte la Gu铆a OpenCore de Dortania . Cuando genere uno, debe seleccionar MacPro7,1 para un correcto funcionamiento.

### Otro apartado a verificar es
En los nuevos parches de CPU de AMD, ahora tenemos que especificar los recuentos de n煤cleos de CPU en los algrey - Force cpuid_cores_per_packagenodos. Actualmente, mi configuraci贸n de EFI establece para el modelo de CPU de 6 n煤cleos porque estoy usando Ryzen 5 3600.
[Consulte la descripci贸n del autor para obtener m谩s informaci贸n.](https://github.com/AMD-OSX/AMD_Vanilla#instructions "Consulte la descripci贸n del autor para obtener m谩s informaci贸n.")
## OpenCore
**Versi贸n**: 0.7.6
## ACPI
- SSDT-HPET.aml: soluciona conflictos de IRQ
- SSDT-NVME.aml: hace que las unidades NVMe se muestren como almacenamiento interno
- SSDT-PLUG.aml - Corrige la administraci贸n de energ铆a de la CPU
- SSDT-SBRG.aml - Corrige conflictos EC, RTC, IRQ
- SSDT-SBUS-MCHC.aml - Corrige la compatibilidad con SMBus
- SSDT-EC-USBX-DESKTOP.aml: corrige el controlador integrado y las propiedades de alimentaci贸n USB
- SSDT-XHC.aml: corrige la asignaci贸n de puertos USB
## Drivers
- OpenCanopy.efi
- OpenHfsPlus.efi
- OpenRuntime.efi
## Kexts
- AGPMInjector.kext
- AMDRyzenCPUPowerManagement.kext
- AppleALC.kext
- AppleMCEReporterDisabler.kext
- CtlnaAHCIPort.kext
- Lilu.kext
- LucyRTL8125Ethernet.kext
- NVMeFix.kext
- RadeonSensor.kext
- RestrictEvents.kext
- SmallTreeIntel82576.kext
- SMCAMDProcessor.kext
- SMCRadeonSensor.kext
- VirtualSMC.kext
- WhateverGreen.kext
## Tools
- OpenShell.efi
- ResetSystem.efi
## Que funciona y que no funciona
### Finciona
- Casi todo, incluida las actualizaciones de Apple (Handoff, iMessage, Airdrop, Facetime, ...)
### Funciona parcialmente
- Tomas de audio de 3,5 mm
- La salida de altavoz en el panel frontal / posterior funciona.
- La entrada de micr贸fono en el panel frontal / posterior no funciona.
- No he probado la entrada / salida de l铆nea y la salida digital.
- Los problemas habituales de Ryzentosh. Consulte la parte de soporte de CPU de la Gu铆a OpenCore de Dortania
- Es posible que sea necesario parchear aplicaciones profesionales espec铆ficas para procesadores AMD, como aplicaciones de Adobe, Davinci Resolve, etc.
- La virtualizaci贸n (Apple Hypervisor y las aplicaciones que usan esto como AVD en Android Studio, Parallels) no funciona, pero VirtualBox s铆.
### No funciona
- Sidecar
## Referencias
- [OpenCore Install Guide](https://dortania.github.io/OpenCore-Install-Guide/ "Dortania's OpenCore Install Guide")
- [forum ReinierTutoriales](https://forum.softgameplus.com/ "forum ReinierTutoriales")
馃槑
