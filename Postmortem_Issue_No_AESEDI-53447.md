#AES CIS Postmortem (Jira Issue No. AESEDI-53447)
##Date
2019-03-26

##Authors
ASLAN
##Status
Resolved

##Summary
Missing records due to customer data not sent from AES EDI.

##Impact
486,000 records were affected.

##Root Causes
Issue with the AES CIS service (Jira Issue No: AESCIS-38263)

##Trigger
Customer data being sent.

##Resolution
Resend file.

##Detection
A Jira issue (AESEDI-53447) was logged that the customer data was not sent from AES EDI.

##Action Item
Improve monitoring so that it detects issues with AES CIS

##Action Item	Type	Owner	Bug

| Action Item	| Type	| Owner	| Bug |
| --- | --- | --- | --- |
| Update playbook with instructions for responding to AES CIS failure | mitigate | ASLAN |	n/a DONE |
|Improve monitoring so that it detects issues with AES CIS | prevent | ASLAN |	n/a DONE |

##Lessons Learned

###What went well
File was resent and the issue got resolved.
###What went wrong
Issue affected monitoring service and therefore missing records were not discovered automatically.

##Timeline
2019-3-26 (all times UTC+3)

|Time	| Description|
| --- | --- |
|11:56|	Missing records discovered|
|13:00|	Records processed|
