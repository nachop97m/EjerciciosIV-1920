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

