# Lessons learned and future direction

AHP v1 demonstrates a practical approach to coordinating coding agents through explicit state and human authority. Its limitations are also useful architecture evidence.

| Observation | Design implication |
| --- | --- |
| Markdown is readable but vulnerable to omissions and parsing drift | Consider typed canonical state with generated human-readable views |
| Git supports audit and portability but synchronization can interrupt lifecycle transitions | Consider transactional state transitions, durable intent records and explicit recovery |
| Different coding clients expose different execution capabilities | Define adapter contracts and capability tests rather than assuming interchangeable agents |
| Approval gates add necessary control but can introduce overhead | Keep risk-adaptive policy and measure friction before simplifying |
| Historical timing and usage data are incomplete | Capture structured timestamps, attempt outcomes and provider-measured usage prospectively |

The owner is considering a second-generation design. These are proposed directions, not implemented v2 features. The existing tool remains an alpha-stage, primarily owner-operated system; independent security assessment, external adoption and comparative productivity evidence have not been established.
