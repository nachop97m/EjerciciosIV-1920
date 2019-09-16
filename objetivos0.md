Amortización Servidor
=====================

Tomamos como ejemplo el Lenovo ThinkSystem ST250, uno de los más vendidos según Amazon. El fabricante lo presenta de la siguiente manera:

 	Servidor de torre con calidad empresarial para oficinas remotas y sucursales el más reciente procesador Intel® Xeon® E-2100 y tecnología de memoria, hasta 4x módulos UDIMM TruDDR4 a 2666 MHz.
 	
 	- Soporta opciones de almacenamiento de clase empresarial versátiles y comunes a toda la plataforma ThinkSystem

	- Fiabilidad y capacidad de servicio para la empresa

	- Fuente de alimentación fija de 250 W o doble fuentes de alimentación 550W AC para redundancia

	- 2x puertos de 1 GbE integrados y 1x puerto de 1 GbE dedicado para administración

	- Eficiencia energética certificada de hasta 80 PLUS Platinum y Energy Star 2.1

	- Despliegue y gestione fácilmente aplicaciones de TI mediante el Lenovo XClarity Controller integrado
	
	- Bajo nivel acústico, adecuado para la oficina

	- Tamaño compacto para colocar al lado o debajo del escritorio
	
Analizamos la amortización, que se define como el valor del bien / tiempo que dura:

- Para 4 años: 975 € / 4 años = 243 € / año

- Para 7 años: 975 € / 7 años = 139 € / año

Debemos por tanto ingresar las cantidades anuales calculadas para amortizar el servidor, y aumentar dicha cantidad para haber hecho una inversión rentable. Hay que tener en cuenta además que sería necesario adquirir un servidor de almacenamiento para los datos, y que si se compra a mitad de año, la amortización para ese año sera menor.


Comparación Servidor / Nube
=====================


Comparamos ahora el Dell PowerEdge T340 Intel Xeon E-2124/8GB/1TB, con el coste de una suscripción a MVPS.net de características similares:
CPU de 4 cores, 8GB de RAM y 100GB de almacenamiento SSD (que, más o menos, iguala en costo un disco de 1TB HDD, quizás algo más barato).

En este caso, depende del número de años que usemos el servidor. Por ejemplo, 5 años de suscripción nos saldría por unos 1140 €, frente a los 899€ que costaría el servidor comprándolo en PCComponentes. Sin embargo, si el uso que se le da es menor, el ahorro que se obtiene empleando la nube puede ser mucho mayor. Plataformas como ARSYS ofrecen contratos flexibles, por lo que solo pagarías mensualmente por lo que utilices. Si tan solo usamos un 1% o un 10%, pagaríamos mucho menos, y el coste podría reducirse. Si pagamos el 10% del total, nos costaría aproximadamente 120€ en lugar de 1140€. El ahorro es considerable.


Virtualización a Nivel Hardware
=====================


En mi caso, un portátil gama media-alta MSI del año 2016, obtengo la siguiente salida (8 veces, por los 8 núcleos de la CPU: i7-7700HQ)

	flags		: fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush dts acpi mmx fxsr sse sse2 ss ht tm pbe syscall nx pdpe1gb rdtscp lm constant_tsc art arch_perfmon pebs bts rep_good nopl xtopology nonstop_tsc cpuid aperfmperf tsc_known_freq pni pclmulqdq dtes64 monitor ds_cpl vmx est tm2 ssse3 sdbg fma cx16 xtpr pdcm pcid sse4_1 sse4_2 x2apic movbe popcnt tsc_deadline_timer aes xsave avx f16c rdrand lahf_lm abm 3dnowprefetch cpuid_fault epb invpcid_single pti ssbd ibrs ibpb stibp tpr_shadow vnmi flexpriority ept vpid fsgsbase tsc_adjust bmi1 avx2 smep bmi2 erms invpcid mpx rdseed adx smap clflushopt intel_pt xsaveopt xsavec xgetbv1 xsaves dtherm ida arat pln pts hwp hwp_notify hwp_act_window hwp_epp md_clear flush_l1d
	
	Podemos ver el flag correspondiente a la virtualización en la mitad de la lista: 
	
		 ... monitor ds_cpl VMX est tm2 ssse3...
		 
Comprobamos también que KVM está instalado y disponible:

	nacho@nacho-GE62-7RD:~/IV/EjerciciosIV-1920$ kvm-ok
	INFO: /dev/kvm exists
	KVM acceleration can be used


Justificación del uso de la virtualización:
=====================

	- Ahorro en adquisición y mantenimiento de hardware. Según VMWare, las empresas de IT dedican hasta un 70% de del presupuesto a éstos propósitos.
	
	- Escalabilidad y facilidad para aumentar los recursos.
	
	- Adaptación del 'hardware' (por medio de la virtualización) según las necesidades de la aplicación.
	
	- Facilidad para desplegar una aplicación con unos requerimientos determinados en cualquier sistema.
	

Para más información, consultar los apuntes o la web: [searchdatacenter.techtarget.com](https://searchdatacenter.techtarget.com/es/cronica/Beneficios-de-la-virtualizacion-y-consejos-para-su-implementacion)