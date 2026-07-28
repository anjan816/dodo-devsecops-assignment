
<h1 align="center">🔍 Task 4 – Reconnaissance & Penetration Testing</h1>

<p align="center">
This task performs authorized reconnaissance and security testing against the provided vulnerable application.
The assessment follows ethical hacking principles and focuses on identifying common web application security weaknesses.
</p>

<hr>

<h2>📌 Objective</h2>

<p>
The objective is to discover exposed services, identify application technologies,
enumerate attack surfaces, and validate common vulnerabilities using industry-standard security tools.
All testing was performed only against the authorized target environment.
</p>

<hr>

<h2>🔎 Reconnaissance Activities</h2>

<h3>Subdomain Enumeration</h3>

<p>
Subfinder, Amass, and Assetfinder were used to discover publicly accessible subdomains.
Combining multiple tools improves discovery accuracy by using different data sources.
</p>

<h3>Technology Fingerprinting</h3>

<p>
WhatWeb identifies web technologies such as web servers, frameworks,
content management systems, programming languages, and security headers.
</p>

<h3>HTTP Service Validation</h3>

<p>
ProjectDiscovery HTTPX validates discovered hosts, checks HTTP response codes,
identifies active services, and collects metadata for further analysis.
</p>

<hr>

<h2>🧪 Penetration Testing</h2>

<h3>Directory Enumeration</h3>

<p>
FFUF performs directory and endpoint discovery using custom wordlists to identify hidden resources
that may expose administrative interfaces or sensitive files.
</p>

<h3>SQL Injection Testing</h3>

<p>
SQLMap performs automated testing for SQL injection vulnerabilities.
Only low-risk and authorized testing options were used during assessment.
</p>

<h3>Template-based Scanning</h3>

<p>
Nuclei executes security templates to detect known vulnerabilities,
misconfigurations, exposed panels, and insecure services.
</p>

<hr>

<h2>🛠 Security Tools Used</h2>

<ul>

<li>Subfinder</li>

<li>Amass</li>

<li>Assetfinder</li>

<li>HTTPX</li>

<li>WhatWeb</li>

<li>FFUF</li>

<li>SQLMap</li>

<li>Nuclei</li>

</ul>

<hr>

<h2>📸 Evidence</h2>

<ul>

<li>Subdomain Enumeration</li>

<li>Technology Fingerprinting</li>

<li>HTTP Validation</li>

<li>Directory Discovery</li>

<li>SQLMap Results</li>

<li>Nuclei Scan Results</li>

</ul>

<hr>

<h2>⚠ Responsible Disclosure</h2>

<p>
All security testing was performed only against the authorized target provided for this assignment.
No testing was conducted against unauthorized systems, and no attempts were made to exploit or impact production services.
The objective of the assessment was to identify security weaknesses responsibly and recommend appropriate remediation measures.
</p>

<hr>

<h2>🎯 Key Learnings</h2>

<ul>

<li>Reconnaissance methodology</li>

<li>Attack surface discovery</li>

<li>Technology fingerprinting</li>

<li>Web application penetration testing</li>

<li>Responsible security assessment</li>

</ul>

<hr>

<h2>📖 Conclusion</h2>

<p>
The reconnaissance and penetration testing activities successfully identified the exposed attack surface,
validated accessible services, and demonstrated the use of industry-standard security assessment tools.
The exercise reinforced the importance of continuous security testing and proactive vulnerability management throughout the software development lifecycle.
</p>