# Atomic Blue Team

A compendium of rules and events, created to detect and smite evil.

## Philosophy

Atomic Blue Team is a knowledgebase of SIEM rules and their associated prerequisites (Baselines, Windows Event IDs, Linux log files, etc.), designed to provide 1 to 1 coverage against tests in Atomic Red Team. These rules provide coverage to a wide portion of MITRE's ATT&CK Matrix. 

It currently supports the Splunk Search Processing Language (SPL).

Atomic Blue Team was built on the foundation of these principles:

- **Fundamentals: Blue Teams should be able to detect and respond to commodity attacks before their security programs can become more mature.**
  Our security teams do not want to operate with a “hopes and prayers” attitude toward detection. We need to know
  what our controls and program can detect, and what it cannot. We don’t have to detect every adversary, but we
  do believe in knowing our blind spots.

- **Baseline _Everything_: The mantra of "know normal, find evil" above all.**
Accurate detection of anomalous security events is next to impossible if you cannot establish a proper baseline of what is currently running in your environment.

- **Repeatability: Testing your controls should be repeatable.**
You should be able to use Atomic Blue Team in conjunction with Atomic Red Team to perform quickly repeatable tests to ensure that your SIEM is detecting and alerting on anomalous events.

- **Practice: We talkin' 'bout practice!**
Send your data to a test environment. 


## Getting Started

* [The ABT Matrix](atomics/matrix.md)
* [List of Atomic Rules by ATT&CK Tactic & Technique](atomics/index.md)
* Event Code Library
* Techniques

## Acknowledgements

* Atomic Red Team
* MITRE ATT&CK

## Code of Conduct
TBD

## License
TBD
