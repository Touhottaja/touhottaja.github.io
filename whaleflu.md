# Whaleflu: Exploring Network Malware in a Sandbox Environment

Malware development is often motivated by malicious intent, but I wanted to use it as a tool for understanding cybersecurity threats. I didn't have any previous experience with malware development, so I wanted to start simple. Something that simply scans the host and tries to copy itself over the network. This could be thought of a start for a ransomware, for example.

To dip my toes into the dark-ish gray area of cybersecurity, I created **whaleflu**. I came up with the name as I wanted to run it inside a Docker sandbox environment and Docker's mascot is a whale, and flu is caused by a virus. Very clever, I know.

## Starting Scenario & Goal
![Whaleflu chart](https://raw.githubusercontent.com/Touhottaja/whaleflu/main/img/whaleflu_chart.png?token=GHSAT0AAAAAACSCNYX35CYEBNQ5LAHTDMS2ZS6APGA)
In the environment, whaleflu has already infected a single machine within a network, marked in red. This infected machine communicates with a command-and-control server (not really a C2C server, but simulates one), marked in blue.

The primary objective of whaleflu is to gather information about the infected host and send it back to the C2C server. Additionally, it periodically pings the server to maintain communication. Once the initial data transmission is complete, whaleflu attempts to propagate itself across the network using SSH and common insecure credentials. If the propagation is successful, the newly infected machines repeat the process, continuing until no further spread is possible.

Right now, whaleflu doesn't do anything else besides eating up some resources. It could be easily extended to do other malicious activities, such as encrypt files, but this code is not something I'd feel comfortable publishing.

## Lessons Learned
Appraching cybersecurity from the attacker's point of view via malware development really drove the point of not using unsecure/default credentials. It also made me a bit more sceptical of using lesser known packages without reading through the source code first.

Whaleflu is available on my [GitHub](https://github.com/Touhottaja/whaleflu) with instructions on how to setup and run it yourself in a Docker sandbox environment.
