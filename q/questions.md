# List of q interview questions & topics
- [List of q interview questions & topics](#list-of-q-interview-questions--topics)
  - [Joins](#joins)
  - [Data on disk](#data-on-disk)
  - [IPC](#ipc)
  - [Tickerplants](#tickerplants)
    - [Vanilla](#vanilla)
    - [Intraday](#intraday)
    - [RTE/Subscribers](#rtesubscribers)
    - [Replay / Disaster recovery](#replay--disaster-recovery)
  - [Adverbs (aka Iterators)](#adverbs-aka-iterators)
  - [Misc](#misc)
    - [Rapid Fire Scenario](#rapid-fire-scenario)
  - [Linux / System debugging](#linux--system-debugging)


## Joins

| Question                                                                                  | Answer              | Further Reading/Material                     |
| ----------------------------------------------------------------------------------------- | ------------------- | -------------------------------------------- |
| What is aj/ej/ij/pj/uj?; What are args?                                                   | Give examples       | [Joins](https://code.kx.com/q/basics/joins/) |
| When would you use each         aj is the big one                                         | See above^          |                                              |
| Have you looked at the underlying code of aj? How does it work?                           | Disgusting question |                                              |
| Why do you first group by sym and then sort by time within sym? What exactly is happening |
| here?                                                                                     |                     |                                              |
| If I added another column, exchange, to my aj, what would happen here:                    |
|                                                                                           |                     |
|                                                                                           |                     |                                              |
|                                                                                           |                     |                                              |
|                                                                                           |                     |                                              |





## Data on disk

| Question                                                | Answer                                                                 | Further Reading/Material                                                                                                                |
| ------------------------------------------------------- | ---------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- |
| Describe types of data on disk                          | flat file, splayed, partitioned, segmented <br /> Talk about structure |                                                                                                                                         |
| When would you use each?                                | give rough size estimates                                              |                                                                                                                                         |
| Attributes - what are they?                             | p,u,g,s    <br /> Talk about when you'd use each                       |                                                                                                                                         |
| bloated sym file - how is it caused? how would you fix? |                                                                        | [compacting;](https://code.kx.com/q/kb/compacting-hdb-sym/)         <br /> [working with sym files](https://code.kx.com/q/wp/symfiles/) |


## IPC

| Question                                                    | Answer | Further Reading/Material |
| ----------------------------------------------------------- | ------ | ------------------------ |
| What is a slow consumer                                     |        |                          |
| How do you detect slow consumers                            |        |                          |
| If I have a slow subscriber, how do I identify it's handle? |        |                          |
| dangers of slow consumers                                   |        |                          |
| async vs sync                                               |        |                          |
| deferred syncronous                                         |        |                          |


## Tickerplants

| Question              | Answer | Further Reading/Material |
| --------------------- | ------ | ------------------------ |
| Again, slow consumers |        |                          |
| chained tickerplants  |        |                          |
|                       |        |                          |

### Vanilla

| Question                         | Answer | Further Reading/Material |
| -------------------------------- | ------ | ------------------------ |
| describe vanilla tp setup        |        |                          |
| EOD - what happens?              |        |                          |
| the .u variables - what they is? |        |                          |
|                                  |        |                          |

### Intraday

| Question | Answer | Further Reading/Material |
| -------- | ------ | ------------------------ |
|          |        |                          |
|          |        |                          |
|          |        |                          |

### RTE/Subscribers

| Question | Answer | Further Reading/Material |
| -------- | ------ | ------------------------ |
|          |        |                          |
|          |        |                          |
|          |        |                          |

### Replay / Disaster recovery

| Question | Answer | Further Reading/Material |
| -------- | ------ | ------------------------ |
|          |        |                          |
|          |        |                          |
|          |        |                          |

## Adverbs (aka Iterators)

| Question | Answer | Further Reading/Material |
| -------- | ------ | ------------------------ |
|          |        |                          |
|          |        |                          |
|          |        |                          |

## Misc

| Question                                                                                     | Answer                                                                                                                                                                                      | Further Reading/Material |
| -------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------ |
| parallel execution- if master is started with -s enabled do you need to explicitly use peach | not since version 3.something                                                                                                                                                               |                          |
| Talk about GW setup                                                                          |                                                                                                                                                                                             |                          |
| how would you improve query times on HDBs?                                                   | monthly/yearly partitions?; <br />parted sym column, grouped on symbol columns frequently used for lookups (eg secondary id);<br /> ensure date=xxxx.xx.xx,time within(x;y),sym in symList; |                          |
| Favourite kdb+ reserved word?                                                                | Leave the interview immediately                                                                                                                                                             |                          |
| How to use peach                                                                             |                                                                                                                                                                                             |                          |
| Some of the .Q functions                                                                     |                                                                                                                                                                                             |                          |
| What is garbage collection                                                                   | .Q.gc[]                                                                                                                                                                                     |                          |
| fby - what/when/why?                                                                         |                                                                                                                                                                                             |                          |
|                                                                                              |
| Excluding –u, how can you manage a connecting process’ permissioning to connect to server?   |                                                                                                                                                                                             |                          |
| Differences between symbols and strings (when to save column as symbol and strings)          |                                                                                                                                                                                             |                          |
| Protected execution                                                                          |                                                                                                                                                                                             |                          |
| apply/index                                                                                  |                                                                                                                                                                                             |                          |
| What is a list?                                                                              |
|                                                                                              |                                                                                                                                                                                             |
| What is a dictionary                                                                         |                                                                                                                                                                                             |                          |
|                                                                                              |                                                                                                                                                                                             |                          |
|                                                                                              |                                                                                                                                                                                             |                          |
|                                                                                              |                                                                                                                                                                                             |                          |



### Rapid Fire Scenario

| Question                                                                 | Answer            | Further Reading/Material |
| ------------------------------------------------------------------------ | ----------------- | ------------------------ |
| Your prod server crashed                                                 | Cry...            |                          |
| RDB went down                                                            | TP recovery       |                          |
| TP went down                                                             | also cry          |                          |
| Loading massive CSV, too big for memory                                  | .Q.fsn            |                          |
| Want to change                                                           | functional select |                          |
| Args to functional select/update/delete                                  | t;c;b;a           |                          |
| Common error codes <br />s-fail; unmappable; badtail; cores; wsfull;     |                   |                          |
| How to set memory limit on a process (- w). What arguments does it take? |                   |                          |
| Gateways? Why would you use gateways?                                    |                   |                          |
| Backups? Why do you need back ups?                                       |                   |                          |
| What to do if TP is using 90% of memory on server                        |
|                                                                          |                   |
| How do you identify the user on a particular port?                       |
|                                                                          |                   |
|                                                                          |                   |                          |
|                                                                          |                   |                          |



## Linux / System debugging

| Question | Answer | Further Reading/Material |
| -------- | ------ | ------------------------ |
|          |        |                          |
|          |        |                          |
|          |        |                          |
