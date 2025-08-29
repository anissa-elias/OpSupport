# OpSupport
An Agentic Small Language Model Operator Support System for Mission Critical SCADA Operational Decisions in Power Grids
# Purpose:

We are proposing a method that would design and evaluate a natural language data analytics support system for mission critical decisions for power system operators who are continuously monitoring and interpreting SCADA data streams. Modern power systems generate massive amounts of real-time data from substations, transmission lines, renewable assets, etc., yet during mission-critical events such as cascading outages or frequency instabilities, operators lack the time and software support to manually interpret the abnormal data. 

To address this, we propose a Small Language Model(SLM) architecture that contextualizes incoming system data across multiple streams, relates each signal to the overall grid state, and provides operators with concise, continuous fact-based natural language summaries, where every summary links back to the data sources.

This is achieved by embedding domain-specific knowledge within the SLM agents, enabling each agent to be a 'representative' to the different devices sending in the data, with a final SLM agent that would be trained on the overall system. This solution could be a stress reliever to operators during high-stress conditions, could lead to preventive solutions. 

Novelty: Most decision-support systems today are visualization heavy, not language based. Proposing the framing of real-time sate evolution in NLP could improve operator situational awareness. 

Agentic system with shared memory and expertise specialization enable more accurate, interpretable and scalable understanding of complex multi-source data streams

# Challenges

**Latency & Real-Time Constraint:**
    -SCADA data is 2-4 seconds
    - PMU data arrives at 30-120Hz
    - Analytics system must operate at near-real time speed <1s delay

**Model Generalization:**
    - Power grids are all different, and utility companies might want different embedded information 
    - Will we generalize or would it be specific to the control room? 

# Agentic System Architecture:

Our proposed agentic approach would map agents to devices/subsystems aligning with modular SCADA/EMS architecture deployed in the field today. This offers a smaller, auditable, domain-specific model that is feasible for real-time and mission critical environment. 

This is a decision-making support tool ONLY, it is not intended to make suggestions to the operators based on system conditions. Output will be in Restricted Natural Language, making it a point to avoid extraneous language. 

**Simulation Test-Bed**
    - Commonly used devices in power grids: PMU, RTU, IED, Modbus, Breakers, Renewable systems, etc. 
    - Choose three devices that send different types of data
    - We chose: PMU, IED, PV Modbus

**Agentic System:**
    1. PMU Agent
    2. IED Agent
    3. RTU Agent
    4. System Agent