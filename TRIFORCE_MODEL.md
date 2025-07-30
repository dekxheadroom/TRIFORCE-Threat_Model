# TRIFORCE: Intelligence-Driven Detection and Defence Against Probable Threats

<img width="800" height="653" alt="TRIFORCE_git" src="https://github.com/user-attachments/assets/42371d7d-4989-47c7-b1b6-47d23eeadafa" />
 
## Introduction
This cyber threat model was inspired by DragonForce's song "Power of the Triforce" (from the album Warp Speed Warriors) which in turn was inspired by the Nintendo game "Legend of Zelda". The threat assessment and modelling methodology is built upon my experience in combat intelligence and counter-terrorism intelligence. My role as an intelligence analyst was to provide operation planners with probable scenarios on how the adversary is likely to behave and react to our operations, so that we can make our operations more robust and resilient. 

## TRIFORCE: **T**hreat-**R**eady **I**nsights, **F**ocusing **O**n **R**elevant **C**apabilities & **E**ntities

## Purpose & Target Audience
* **<ins>Purpose</ins>:** A heuristic model for Threat-Informed Defence to enable security operators to formulate probable threat courses of action for simulation of attack and defence, so as to validate and fine-tune current security posture.
* **<ins>Target Audience</ins>:** Purple Teams defending systems already in production. 

## Impetus: Why TRIFORCE?
* We need something quick, dirty yet substantial like a good bowl of Jiro Ramen - no frills, high-impact approach that hits you in the palette and gut.
* Lack of action-oriented model for developing simulation exercises to validate security posture.
* Existing threat models primarily for strategic risk management and biased towards technical vulnerabilities: 
    * <ins>STRIDE-DREAD</ins> meant for system development phase; purely technical and devoid of human behavioural interaction with technology.
    * <ins>PASTA</ins> is pre-requisite for designing fundamental security posture through strategic risk identification and mitigation, but does not consider user behaviours (susceptibility to social engineering) and is a costly process in terms of time and resources for continuous validation and review of posture. 
    * <ins>OCTAVE</ins> is primarily focused on threat possibilities (threat trees) on own assets, absent of threat actors with specific intentions.
    * <ins>VAST</ins> is tied to a commercial tool.
    * <ins>TRIKE</ins> is geared towards design phase and for risk management, threats are simplified and employ attack trees not contextualised to threats with specific intention.
    * <ins>LINDDUN</ins> is focused primarily on the privacy or confidentiality aspect of the CIA triad.
      
## Core Concept
1.  Uses the axiom: `Threat = (Intent x Capability x Opportunity) / Security Posture`
2.  Assume the Attacker's Perspective to find a path to and through Defender's infrastructure to Final Objective, leveraging on technical and non-technical assets of organisation; 
3.  Develop Threat Courses of Action expressed in format of Cyber Kill Chain;
4.  Develop Own Courses of Action to detect and defeat Attack;
5.  Exercise simulation of Attack and Defence so as to Validate and Fine-Tune defence posture including counter-reconnaissance measures.

## Desired Outcomes
* Defence team able to know if security posture is sufficient to deter, delay or disrupt attacks from identified threat actors.
* Defence team able to reduce attack surface area.
* Defence team able to pro-actively observe detect and decisively respond to threat activities.

## Limitations
* The approach is best suited for threat actors that follow known playbooks, and may not be applicable to top-tier threat teams that innovate playbooks.
* This method is not meant to simulate all possible attacks against  every discovered vulnerability of its own system.

## Resource Requirements
* <ins>Team</ins>:
  * Minimum: One committed analyst;
  * Recommended: Three analysts with expertise in stakeholder communications (seek information from stakeholders), threat intelligence, OSINT, defence & attack competencies;
* <ins>Time</ins>: Roughly three business days (eight hours per day not inclusive of breaks - assuming team starts with knowledge of 60% of own environment)
* <ins>Tools</ins>: Open Source Threat Intelligence Tools
* <ins>Infrastructure</ins>: Digital proxy of defended environment or consider employing [Kali Purple](https://gitlab.com/kalilinux/kali-purple/documentation/-/wikis/home);

## Methodology: Seven Phases of Threat-Informed Defence

Five-Phased if only conducting structured threat analysis; Seven-Phased if include simulation exercise and defence fine-tuning.

### PHASE 1. THREAT INTENT: Who's Going to Hit You and Why You're A Target
>"Know Thyself, Know Thy Enemy" (Planning Attacks - Sun Zi, Chapter III)

>" 知彼知己者，百战不殆。" - 孙子【谋攻篇】

1.  **<ins>Identify Probable Threat Actor</ins>:**
    * Which threat actor is likely eyeing our organisation and why?
2.  **<ins>Examine context of own organisation</ins>:**
    * **<ins>Nature</ins>.** What is the nature of our organisation and which sector does it fall under (e.g. Non-Government Organisation/Narrow Interest non-profit organisation, government, private enterprise, critical infrastructure etc), and which sphere of geopolitical dependencies does it come under (e.g European, American, Chinese or Diversified);
    * **<ins>Victim</ins>.** Which identified threat actors had targeted organisations of the same nature or sector;
    * **<ins>Primary or Secondary Target</ins>.** Is own organisation a primary target (asset custodian) or a pivot point to actual target (on-path in supply chain);
3.  **<ins>Value to Attacker</ins>.** What does a threat actor specifically want from your organisation? List and enumerate.
4.  **<ins>Valued Target</ins>.** Who or which group of users in the organisation has access to the asset?
5.  **<ins>Sources of Knowledge</ins>:**
    * <ins>Threat intelligence Dossiers</ins>: CTI vendors, [MITRE ATT&CK Groups](https://attack.mitre.org/groups/);
    * <ins>Own info</ins>: 
        * Business Strategy (ends, ways, means);
        * Asset list that enables business strategy, connected business partners (clients and vendors);
        * Human Resource: Key Appointment Holders, Intellectual Property Developers, Staff with direct access to Critical Personnel or Sensitive Information; 
6.  **<ins>Output from THREAT INTENT phase</ins>:**
    * Identified Likely Threat Actor(s);
    * Identified Own Assets Likely to Be Targeted;
    * Identified People Likely to Be Targeted;
    * **_Identified own knowledge gaps to drive intelligence collection on threat intent and review of own situation_**;

### PHASE 2. THREAT CAPABILITIES: Attacker's Modus Operandi & Resources 
>"There are not more than two methods of attack--the direct and the indirect" - (Force - Sun Zi, Chapter V)

>"战势不过奇正。"  - 孙子【兵势篇】

1.  **<ins>Modus Operandi</ins>.** Enumerate Known Tactics, Techniques & Procedures (TTP) of likely Threat Actor(s);
2.  **<ins>Resources</ins>.** Enumerate Known infrastructure and tools utilised by Threat Actor(s);
3.  **<ins>Competence</ins>.** Assess adjacent skill sets of Threat Actor(s) - what are the other implied or assessed skill sets (known unknowns) in order for threat actors to be effective
4.  **<ins>Resilience</ins>.** Assess alternate providers of infrastructure (known unknowns);
5.  **<ins>Sources of Knowledge</ins>:**
    * Threat Intelligence Dossiers: CTI vendors, [MITRE ATT&CK GROUPS](https://attack.mitre.org/groups/), [ShadowServer](https://dashboard.shadowserver.org/);
    * OSINT Collection & Analysis;
6.  **<ins>Output from THREAT CAPABILITIES phase</ins>:**
    * Preliminary Threat Course of Action of Likely Threat Actor:
       * Indirect: How will they social engineer targets in order to gain initial foothold;
       * Direct: How will they come in through the front doors and windows;
       * What are they likely to do after establishing initial foothold;
       * How will they evade detection;
       * How will they install malware;
       * How will they elevate privileges and move laterally;
       * Where will they next move;
       * What is their action on objective and how will they do it;
       * What will they do if they know they’ve been detected;

    * **_Identified own knowledge gaps to drive intelligence collection on threat capabilities_**

### PHASE 3. OWN SECURITY POSTURE: Understanding the Lay of Own's Land
>"Adaptations to the nine grounds, the advantages in defensive and offensive maneuvers, and the patterns of human emotions must be examined." (Nine Ground - Sun Zi, Chapter XI)

>"九地之变，屈伸之利，人情之理，不可不察。" -  孙子 【九地篇】

1.  **<ins>Review Existing Security Posture</ins>**
    * What is our organisation's security policies and defence architecture?
2.  **<ins>Visibility</ins>**
    * Asset register (End Points, Software)
    * Architectural diagrams (network, connectivity)
    * Data Flow - Map current data flows to, through and from own organisation;
3.  **<ins>Defensive Architecture</ins>**
    * Access Controls, Trust boundaries, Identity Management, Detection and Response Measures
4.  **<ins>Organisational Pattern of Life</ins>**
    * Standard operating hours and non-operating hours activity: human traffic and network activity
5.  **<ins>Cyber Hygiene Assessment</ins>**
    * Enumerate personnel of privileged users, owners of targeted assets, nodes in chain-of-trust
    * Identify Internal Persons-of-Interest with poor cyber hygiene practices;
6.  **<ins>Sources of Knowledge</ins>:**
    * IT Engineering/Operations department;
    * System Administrators;
    * Critical Process Owners;
    * Business Partners;
    * Security Department (if any);
7.  **<ins>Output from OWN SECURITY POSTURE phase</ins>: (Ideal World Version)**
    * Comprehensive understanding of own assets (System Architecture, Data Flow, Business Rhythm, Security Culture);
    * Identified defensive strengths;
    * Identified defensive weaknesses;
    * **_Identified <ins>knowledge gaps</ins> to level-up self-awareness_**;

### ⚠️ REALITY CHECK ⚠️ ###
* **_A complete and comprehensive ledger of assets may never have existed in your organisation;_**
* **_This is a heroic opportunity to be brutally honest and acknowledge lapses in accounting and accountability;_**
* **_Seek leadership's consent for period of amnesty to exhume the skeletons in the closet: take stock of all assets - anything that runs a service and has a IP address,  and map the entire networked environment - including supposed air-gapped pockets;_**
* **_Get this step right before proceeding further._**

8.  **<ins>Output from OWN SECURITY POSTURE phase</ins>:(Real World Version)**
    * Best-effort understanding of own assets and enviroment (System Architecture, Data Flow, Business Rhythm, Security Culture);
    * Enumerate Assumptions of Defence Architecture (Known Unknowns)
    * Assumed defensive strengths;
    * Assessed defensive weaknesses;
    * **_Identified <ins>knowledge gaps</ins> to level-up self-awareness_**;

### PHASE 4. ATTACK OPPORTUNITIES: When and Where to Attacker Will Hit 
>"Those skilled in warfare made themselves invincible, and then waited for the enemy to become vulnerable" (Formation - Sun Zi, Chapter IV)

> "昔之善战者，先为不可胜，以待敌之可胜。" - 孙子【军形篇】

1.  **<ins>What to Attack (Technical Vulnerabilities)</ins>:**
    * Enumerate Unpatched or Unpatchable Services/Appliances
    * Defence Architecture assumptions (in situation when there's incomplete visibility of own environment)
2.  **<ins>When to Attack (Temporal Factors)</ins>:**
    * Identify Vulnerable Moments from Organisation's Pattern of Life:
	* Time in between scheduled maintenance;
	* Patch management cycle;
	* System or Data Migration schedule;
	* System Upgrade schedule (when and where system will need to be un-hardened);
	* SOC Manning Patterns (shift changes, low manning period, leave schedule of managers);
	* Periods of High Staff Turnover (Voluntary or Involuntary);
3.  **<ins>Who to Attack (Human/Social Engineering Vulnerabilities)</ins>:**
    * Identify Privileged Persons with Poor Cyber Hygiene;
    * Assess candidate's public exposure of personal information, social relations, habits, preferences and pattern of life;
    * Assess candidate's susceptibility to enticement or coercion;
4.  **<ins>Where to Ingress (Attack Surface Analysis)</ins>:**
    * Assess Observability of Own Organisation's Vulnerabilities through non-intrusive or intrusive reconnaissance;
    * Map vulnerable points;
5.  **<ins>Sources of Knowledge</ins>:**
    * IT Operations department
    * System Administrators
    * Help Desk Staff
    * Internal Security Audit
    * OSINT
6.  **<ins>Output from ATTACK OPPORTUNITIES phase</ins>:**
    * Target List - List of Who, What to Attack
    * Target Pattern of Life - When is Organisation Likely to Relax or Drop Security Posture?
    * Map of Bypasses - Any?
    * Map of Obstacles - Defences that can't be circumvented or bypassed
    * Map of Potential Traps - Relatively Easy access But Does it Lead to a Sinkhole or Honeypot?

### PHASE 5. THREAT COURSES OF ACTION: Contextualised Cyber Kill Chain
> "Attack where(when) the Target Cannot Defend" (Weakness and Strength - Sun Zi, Chapter VI)

> "攻而必取者，攻其所不守也。"  - 孙子【虚实篇】 

1.  **<ins>Construct Threat Courses of Action (TCoAs)<ins>:**
    * Synthesise outputs from Phase 4 to 1, build contextualised cyber kill chain in reverse order
    * **💡Pro Tip 💡** 
        * **_For those prefering a more comprehensive and granular template for TCoA formulation, please refer to [Unified Killchain](https://www.unifiedkillchain.com/)_**
    * **<ins>Inputs</ins>:**
        * Adversary Playbook from Identified by THREAT INTENT and THREAT CAPABILITIES
        * Vulnerability, Target List, Vectors and Forcasted Business Events as Identified in ATTACK OPPORTUNITIES
        * Security Control Inventory and Policies as identified in OWN SECURITY POSTURE
    
    * **Format for TCoA (Cyber Kill Chain Example):**
        | Phase | Target (Asset/Person/System) | Technique & Resource (TTP, Tool, Infrastructure) | Outcomes (Adversary's Goal at this stage) |
        |---|---|---|---|
        | Actions on Objective | Which Information Asset |  | * Pre-positioning for further operations? * Exfiltration of Data? (Confidentiality) * Tampering of Data to Dislocate Business Operations? (Integrity) * Deny Access to Data to Disrupt Business Operations? (Availability)|
        | Command and Control | * When to phone home * Where to phone home|  | * Freedom of Action * Deliver more payloads * Build Hive |
        | Installation | Where to embed and hide in target infrastructure |  | * Establish sanctuary * Blend in * Gain Persistence  |
        | Exploitation | * Who to exploit * What to exploit * When to exploit |  | * Establish toe-hold * Expand foothold * Establish line-of-communication |
        | Delivery | * Who to social engineer * Which door or window to break * When to deliver |  | * Access via Cooperative Insider * Direct Ingress through weak or open Access Points|
        | Weaponisation | * What's already available in known arsenal * What needs to be adapted * What needs to be engineered to lure victim |  | * tool that delivers intended effect |
        | Reconnaissance | * What can be learned from non-intrusive information gathering * What can be learned through intrusive information gathering |  | * Mapped target architecture *  Schedule for Pattern of Life * Identified persons-of-interest and susceptibility to social engineering|

2.  **Identify Indicators of Attack (IoAs) & Compromise (IoCs)**
    * **<ins>IoA Focus</ins>:** Behavioral indicators
    * **<ins>IoC Focus</ins>:** Atomic indicators
3.  **<ins>Output from TCoA phase</ins>:**
    * Prioritised Probabilistic Threat Courses of Action (TCoAs);
    * Specific IoAs and IoCs for each TCoA;

### PHASE 6. ATTACK AND DEFENCE SIMULATION: Where the Rubber Meets the Road
>"Many calculations mean victory; few calculations mean no victory;" (Calculations - Sun Zi, Chapter I)

>"多算胜，少算不胜，而况于无算乎？"  - 孙子【始计篇】
1.  **<ins>Exercise Umpire</ins>:**
    * Designate an umpire
    * Umpire to Inject Simulated Events that Cannot be Automated or Quantified such as judgement on success of social engineering;
    * Arbitrate Conflict that Cannot be Resolved through objective means;
2.  **<ins>Red Team (Attacker) Actions</ins>:**
    * Emulate the highest priority TCoAs;
    * Execute Counter-Defence Actions;
3.  **<ins>Blue Team (Defender) Actions</ins>:**
    * Actively monitor for IoA;
    * Check for IoC;
    * Execute Counter-Attack Actions;
4.  **<ins>Data Collection</ins>:**
    * Meticulously document actions taken;
    * Log Events;
    * Record detections and observations;
5.  **<ins>Output from Simulation Phase</ins>:**
    * Simulation Exercise Report;
    * Identified Gaps;

### PHASE 7. CONTINUOUS LEARNING & IMPROVEMENT: Sustainable Security Posture
>"Do not depend on the enemy not coming, but depend on our readiness against him. Do not depend on the enemy not attacking, but depend on our position that cannot be attacked."  (Nine Changes - Sun Zi, Chapter VIII)

> "故用兵之法，无恃其不来，恃吾有以待之；无恃其不攻，恃吾有所不可攻也。"  - 孙子【九变篇】

1.  **<ins>Purple Team Debrief</ins>:**
    * **<ins>Discussion Points</ins>:**
        * **<ins>Plausible Attack Paths</ins>:** Was the TCoA realistic?
        * **<ins>Known Unknowns</ins>:** Did Red Team uncover previously unknown attack paths?
        * **<ins>Defence Worked or Were Irrelevant</ins>:** Which detection rules worked and which didn't?
        * **<ins>Fine-Tune Defence Posture</ins>:** What actions need to be taken to recalibrate existing policies and rules?
2.  **<ins>Re-visit key battles through turn-based simulation</ins>:**
    * Replay events and step through each sequence to understand perspectives of Attacker and Defender
3.  **<ins>Update Security Posture</ins>:**
    * Create new detection rules;
    * Tune existing rules;
    * Prioritise remediation;
    * Re-education Programmes;
4.  **<ins>Output from Continuous Learning Phase</ins>:**
    * Updated Threat Actor Playbooks;
    * Refined TCoAs;
    * Prioritised Remediation Roadmap;
    * Re-calibrated Privileges;
    * Security Training;
    * New Intelligence Collection Requirements;
