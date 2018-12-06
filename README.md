# CSR_ASA_HA_CSR
 Commands and Day0 files to build Service chain using Cisco CSR, ASAv VNFs by the SAE (Secure Agile Exchange) Solution guide
There are 3 phases in launching a service chain using SAE on a CSP(Cloud Services Platform) NFV appliance.

Design phase: 
In this example a enterprise is connected to Internet and  that they need a router followed by a firewall. They chose Cisco CSR and Cisco ASAv. They had ASAv in a HA mode.  
The sample chain has CSRc-ASAv-HA-CSRp, where CSRc is a Consumer side router and CSRp is provider side router

VNF Definitions: 

Below is CSR VNF definition 
V_CSR.txt: VNF definition for CSR containing Interfaces, vCPU, Memory, Storage

Below is the CSR definition specific to this enterprise and 
VD_CSR_PC.txt: VNF with Day0 file name/credentials, NTP, DNS server info for the Consumer side 
VD_CSR_C_day0.txt: Day0 details for Consumer side CSR- commands executed on CSR as part of bringup

VD_CSR_PP.txt: VNF with Day0/credentials for the Provider
VD_CSR_P_day0.txt:  Day0 for Provider side CSR

V_ASA.txt: VNF definition for ASAv containing Interfaces, vCPU,memory

VD_ASA_PM.txt : ASA deployment for primary listing Day0 and Credentials
VD_ASA_PM_day0.txt: Day0 for ASA primary

VD_ASA_SM.txt: ASA deployment for Secondary listing Day0 and Credentials
VD_ASA_SM_day0.txt: Day0 for ASA secondary

Service Chain definition 
N_CSR_ASA_CSR_E2E.txt : NSD for the service chain
ND_CSR_ASA_CSR_E2E.txt : VNFD deployment

Deploy/Instantiate 
external.txt : Endpoints definition - VLAN etc.

SC_E2E_CSR_ASA_CSR.txt: Service chain deployment and connect to endpoints
