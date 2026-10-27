# Test Results

Python version used: Fill in after running `python --version`
Operating system: Fill in on your computer
Date tested: Fill in after running the tests

| # | Input | Expected result | Actual result (reference; verify locally) | Pass/Fail |
|---|---|---|---|---|
| 1 | `https://www.example.com/login` | No listed warning signs | No listed warning signs found. This does NOT prove safety. | pass |
| 2 | `http://192.0.2.10/account` | IP address + HTTP | Uses an IP address instead of a familiar domain; Uses HTTP. HTTPS alone does not prove trust. | Pass |
| 3 | `http://example.com@sample.invalid/login` | `@` symbol + HTTP | Contains an @ symbol; inspect carefully; Uses HTTP. HTTPS alone does not prove trust. | Pass|
| 4 | `https://a.b.c.d.e.example.invalid/path` | Many hostname segments | Contains many hostname segments/subdomains. | Pass |
| 5 | `https://xn--example.invalid/` | Punycode-style hostname | Contains a punycode-style hostname. | Pass |


