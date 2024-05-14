# 5G-Service-Architecture-Model
Rolling Drawio diagram of a 5G Service Oriented Architectural Model. 

This work aims at depicting an E2E model being fully compliant with 3GPP Release 17 standardization framework and able to integrate novel directives provided by main standardization organizations and industry alliances, to flexibly adapt to future "Beyond 5G" network instances.

## Architecture description

The model consists of three interacting layers whose constituting elements are here indicated.

### Management & Orchestration Layer
This layer describes all the management functions needed for converting service requirements posed by the OSS/BSS, along with vertical operators, into a set of slices and manage both their deployment and evolution.
- **OSS/BSS**: Operation Support System / Business Support System functions have full end-to-end visibility of the 5G infrastructure and the services provided toward this former. They coordinate other management and orchestration functionalities.

- **Network Slice Management**: NSM represents the set of functions responsible for the management (including lifecycle) of Network Slices, Slice Subnets and Network Functions (See XXX)
    - *CSMF*: Communication Service Management Function;
    - *NSMF*: Network Slice Management Function;
    - *NSSMF*: Network Slice Subnet management Function;
    - *EGMF*: Exposure Governance Management Function;
    - *MDAF*: Management Data Analytics Function;
    - *NFMF*: Network Function Management Function;
    - *NFV Security Management*: logical functional block for overall security management;
    - *Non RT RIC*: non Real-Time RAN Intelligent Controller.

- **NFV-MANO**: Network Functions Virtualization, Management and Orchestration is an architectural framework for deploying and orchestrating virtualized network functions (VNFs) and other software components proposed by ETSI (See \cite{ETSI-NFV-006}, \cite{ETSI-GR-NFV-IFA-039}).
    - *NFVO*: Network Function Virtualization Orchestrator;
    - *VNFM* Virtual Network Function Manager;
    - *CISM*: Container Infrastructure Service Manager;
    - *CCM*: CIS Cluster Management;
    - *CIR*: Container Image Registry;
    - *VIM*: Virtualised Infrastructure Manager;
    - *WIM*: Wide area network Infrastructure Manager.

- **SBMA**: Service Based Management Architecture is an architectural model that defines basic Management Services (MnS) and a  model-driven approach for consumer/producer interaction between them in order to create Management Functions (MnF) (See \cite{3GPP-TS28-533}).

### Network Service Layer
The slices put into operation and the network functions deployed to implement them are characterized here, highlighting the interfaces and the nature of exchanged data.

- **UE**: User Equipment

- **RAN**: Radio Access Network, with GNodeB and its possible decomposition, in particular O-RAN solution 

- **Regional/Edge Cloud**: they are resource infrastructures placed relatively close to the RAN (Regional) or even at the boundaries with it (Edge).

- **near-RT RIC**: near Real-Time RAN Intelligent Controller \cite{polese2023ORAN}.

- **DN**: Data Network

- **Network Slice**: a logical network that provides specific network capabilities and
network characteristics \cite{marinos2020enisa}

- **Network Slice Subnetwork**: a group of network functions (including their
corresponding resources) that form part or complete constituents of a network slice \cite{marinos2020enisa}

- **xNFs**: (x) Network Functions according to 3GPP Release 17 (See \cite{3GPP-TS23-501});

### Physical Infrastructure Layer
The last layer characterizes the physical resources available in any segment of the E2E network and the virtualization facilities used to create the necessary network functions.

- **NFVI** : Network Function Virtualization Infrastructure (See \cite{ETSI-NFV-006}).

    - *Physical Resource*: any resource provided as physical appliance;
    - *Containerized Resource*: any resource provided as a container;
    - *Virtual Resource*: any resource provided as a Virtual Machine;
    - *Virtualization Layer*:  A layer providing VM virtualization functionalities;
    - *CIS Cluster*: Container Infrastructure Service Cluster, providing container-based virtualization functionalities.

- **WAN**: Wide Area Network


# Acknowledgements

This work is partially supported by project SERICS (PE00000014) under the NRRP MUR program funded by the EU - NGEU.
