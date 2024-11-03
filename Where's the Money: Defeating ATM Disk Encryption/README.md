## Abstract
Holding upwards of $400,000, ATMs continue to be a target of opportunity and have seen over a 600% increase in crime in just the last few years. During this time, I led security research with another colleague into the enterprise ATM industry resulting in the discovery of 6 zero-day vulnerabilities affecting Diebold Nixdorf’s Vynamic Security Suite (VSS), the most prolific ATM security solution in the market. 10 minutes or less is all that a malicious actor would need to gain full control of any system running VSS via offline code injection and decryption of the primary Windows OS. Diebold Nixdorf is one of three major North American enterprise class ATM manufacturers with a global presence in the financial, casino/gaming, and point-of-sale markets. Similar attack surfaces are currently being used in the wild and impact millions of systems across the globe. Furthermore, VSS is known to be present throughout the US gaming industry, including most of the ATM/cash-out systems across Vegas.

In this session, I will publicly disclose this research, review the discovery process, and dive into the technical intricacies of each vulnerability. The Full Disk Encryption module of VSS conducts a complex integrity validation process to ensure a trusted system state, performed as a layered approach during system initialization. Examination of the workflow will highlight various deficiencies that I will demonstrate through PoC exploitation.

Each vulnerability presented in this session has been observed to have a recursive impact across all major versions of VSS and represents a systemic ongoing risk. We will explore the root-cause, vendor remediation steps, and short-comings thereof – perpetuating the attack narrative. In conclusion, proper mitigation techniques and procedures will be covered, providing valuable insights into defending against potential compromise.

## References
* Vynamic Security Suite - Vynamic Security Hard Disk Encryption Secure Sensitive Consumer Data: [link](https://www.dieboldnixdorf.com/-/media/diebold/files/banking/software/dn_product-card_vynamic-security-hard-disk-encryption.pdf)
* SEC Consult - Manipulation of pre-boot authentication in CryptWare CryptoPro Secure Disk for Bitlocker: [link](https://sec-consult.com/vulnerability-lab/advisory/manipulation-of-pre-boot-authentication/)
* Diebold Nixdorf - EULA for Vynamic Security Suite 3.0: [link](https://dnlegalterms.com/wp-content/uploads/2020/03/2020026_Diebold_Nixdorf_EULA_for_VYNAMIC_SECURITY_3_0_December_19_2018_022249.pdf)
* Diebold Nixdorf - Product Legal Terms Website: [link](https://dnlegalterms.com/products/)
* CryptWare Website: [link](https://cryptware-it-security.de/)
* Secure Disk for BitLocker Website: [link](https://secure-disk-for-bitlocker.com/about/)
* CPSD Website: [link](https://www.cpsd.at/)
* O'Reilly - Essential System Administration, 3rd Edition by Æleen Frisch: [link](https://www.oreilly.com/library/view/essential-system-administration/0596003439/ch04s02.html)
* Flowblok's Blog - Shell Startup Scripts: [link](https://blog.flowblok.id.au/2013-02/shell-startup-scripts.html)
* Red Hat Customer Portal - Enhancing Security with the Kernel Integrity Subsystem: [link](https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/8/html/managing_monitoring_and_updating_the_kernel/enhancing-security-with-the-kernel-integrity-subsystem_managing-monitoring-and-updating-the-kernel?extIdCarryOver=true&sc_cid=701f2000001OH7EAAW)
* OpenSUSE Wiki - SDB:Ima evm: [link](https://en.opensuse.org/SDB:Ima_evm)
* ATMIA - ATM Operator Training: [link](https://www.atmia.com/training/atm-operators/)
* 3SI Systems - Stop Criminals from Cashing in at the ATM: [link](https://www.atmia.com/files/whitepapers/2024-atm-crime-trends.pdf)
* Diebold Nixdorf - Vynamic Security Intrusion Protection Product Card: [link](https://www.dieboldnixdorf.com/-/media/diebold/files/banking/software/vynamic-security-intrusion-protectionproduct-card.pdf)
* Diebold Nixdorf - DN Product Card - Vynamic Security Hard Disk Encryption: [link](https://www.dieboldnixdorf.com/-/media/diebold/files/banking/software/dn_product-card_vynamic-security-harddisk-encryption.pdf)
* Everi - Everi to Showcase "Digital Neighborhood" Connecting Guest Loyalty, Cash Access Experiences, and Casino Solutions Made Possible by Industry-Leading Financial Technology Portfolio at 2019 Global Gaming Expo: [link](https://s1.q4cdn.com/401000259/files/doc_news/Everi-to-Showcase-Digital-Neighborhood-Connecting-Guest-Loyalty-Cash-Access-Experiences-and-Casino-Solutions-Made-Possible-by-Industr-SW9PO.pdf)
* GlobeNewswire - NRT Accelerates Growth through Acquisition of Casino ATM Portfolio: [link](https://finance.yahoo.com/news/nrt-accelerates-growth-acquisition-casino-160700070.html)
* Northox - How does the TPM perform integrity measurements on a system?: [link](https://security.stackexchange.com/questions/39329/how-does-the-tpm-perform-integrity-measurementson-a-system)