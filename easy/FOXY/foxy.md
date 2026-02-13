# Foxy Lab Report

<img width="940" height="517" alt="image" src="https://github.com/user-attachments/assets/13c2d509-df16-47fa-b048-b619d4c2c498" />

- Q1) The SOC recently observed network connections from 3 internal hosts towards hxxp://45.63.126[.]199/dot.gif (URL has been sanitized). What is this activity likely related to?
  - Using ctrl+f to find the url in the sheet, it matches to the activity it is likely related to

<img width="940" height="510" alt="image" src="https://github.com/user-attachments/assets/16a891e6-0364-40a0-a563-67426584687a" />

- Q2) How many URLs are using the same endpoint 'dot.gif', across all export files? (include duplicates)
  - Running the grep command reveals how many urls are using the same endpoint "dot.gif" across all export files

<img width="940" height="480" alt="image" src="https://github.com/user-attachments/assets/79e9812b-aca6-4308-ac58-233eadc85e6c" />

- Q3) The SHA256 hash of a file was detected and quarantined on one of the Executives old android phones. We are trying to work out what this file does so we can take next steps. The hash value is 6461851c092d0074150e4e56a146108ae82130c22580fb444c1444e7d936e0b5. Is this file associated with malware? If so, what is the malware name? (as stated by Malware Bazaar)
  - Searching the sha256 hash on malware bazar will reveal the answer

<img width="940" height="946" alt="image" src="https://github.com/user-attachments/assets/d13532e5-3a07-4610-9e3b-187865554b1c" />

- Q4) Investigate the reference link for this SHA256 hash value. Submit the threat name (acronym only), the C2 domain, IP, and the domain registrar.
  - Clicking on the twitter link will reveal all answers to this question

<img width="940" height="469" alt="image" src="https://github.com/user-attachments/assets/c056b37f-0e13-49b7-b03b-cde5e9662189" />

- Q5) Visit https://www.joesandbox.com/analysis/1319345/1/html. Investigate the MITRE ATT&CK Matrix to understand the Collection activities this file can take, and what the potential impact is to the Executives work mobile phone. Submit the 5 Technique names in alphabetical order.
  - Under the MITRE ATT&CK matrix in the link, the collection column reveals the five activites which can potentially impact the executives work mobile phone

<img width="940" height="354" alt="image" src="https://github.com/user-attachments/assets/d44fe2c1-83d2-4f74-a6f2-b0d99904dc82" />

- Q6) A junior analyst was handling an event that involved outbound connections to a private address and didn't perform any further analysis on the IP. What are the two ports used by the IP 192.236.198.236?
  - Using grep with the IP address given and applying the file name where this is to be searched in will reveal the ports used by the IP

<img width="940" height="668" alt="image" src="https://github.com/user-attachments/assets/79b783f1-63e6-4727-8787-4a6faa2853f2" />

- Q7) Use the reference to help you further research the IP. What is the C2 domain?
  - Clicking on the link attached will direct to a Twitter page revealing the C2 domain

<img width="940" height="463" alt="image" src="https://github.com/user-attachments/assets/d66c9181-f809-4c59-b151-9a346dbead2a" />

- Q8) What is the likely delivery method into our organization? Provide the Technique name and Technique ID from ATT&CK.
  - Performing OSINT using MITRE ATT&CK framework shows the technique used as the likely delivery method

<img width="940" height="297" alt="image" src="https://github.com/user-attachments/assets/a9a7ad01-bda5-443b-afd9-e9ee340ff82d" />

- Q9) Investigate further and try to find the name of the weaponized Word document, so we can use our EDR to check if it is present anywhere else within the organization.
  - Using the xml url and putting the ctrl+f command will show the word document name

<img width="940" height="242" alt="image" src="https://github.com/user-attachments/assets/6ede5a40-47a6-4b79-b529-e60b046b4373" />

- Q10) What is the name of the .JAR file dropped by the Word document?
  - Using the same concept as previous question, the .jar file can also be found within the webpage

<img width="940" height="633" alt="image" src="https://github.com/user-attachments/assets/25dca86c-9b23-474b-9dad-8e7802962b70" />

- Q11) Executives have expressed concern about allowing employees to visit Discord on the corporate network because of online reports that it can be used for malware delivery and data exfiltration. Investigate how Discord can be abused for malicious file storage/distribution! What is the URL of the Discord CDN, ending with /attachments/?
  - Using grep command can help find the Discord CDN ending wity /attachments/

<img width="940" height="386" alt="image" src="https://github.com/user-attachments/assets/04e6fa03-8ce1-4f0b-8239-31fba5fdb07d" />

- Q12) Looking at all export files, how many rows reference this URL? (include duplicates)
  - Same concept can be applied as previous question

<img width="940" height="498" alt="image" src="https://github.com/user-attachments/assets/b2c1cbef-2596-4d55-86ef-643b97045acf" />

- Q13) Based on this information, what is the name of the malware family that is being widely distributed via Discord?
  - Using ctrl+f on the full_urls.csv file will help see the answer to this question

<img width="940" height="499" alt="image" src="https://github.com/user-attachments/assets/bac1c2c0-c966-4c17-879b-ee94fd9d2715" />

- Q14) We can proactively use indicators from threat feeds for detection, or for prevention via blocking. When it comes to blocking indicators, it is crucial that they are from a reputable source and have a high level of confidence to prevent blocking legitimate entities. How many rows in the full_urls.csv have a confidence rating of 100, and would likely be safe to block on the web proxy?
  - Using the countif command of excel, we can use the entire J column which is for confidence and filter it out for "100" only

<img width="940" height="499" alt="image" src="https://github.com/user-attachments/assets/2e7bc2fd-d082-41b8-9532-5aa00834b67a" />

- Q15) An analyst has reported activity coming from an IP address using source port 8001, but they don't understand what this IP is trying to achieve. Looking at full_ip-port.csv in Gnumeric, filter on malware_printable = Unknown malware, and find an IP that is using port 8001. What is the IP address value?
  - Using ctrl+f on the full_urls.csv file will help see the answer to this question

<img width="940" height="689" alt="image" src="https://github.com/user-attachments/assets/50098e40-6174-41ad-9be8-eecb199fa3e0" />

- Q16) Investigating the reference material, what is the CVE ID of the vulnerability that this IP has been trying to exploit? And what is the industry nickname for this vulnerability?
  - Looking at the Twitter link, the CVE is given. Searching the CVE on Google will reveal the industry nickname
