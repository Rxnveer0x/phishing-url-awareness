
# Test Results

Python version used: Python 3.14.5  
Operating system: Windows 11  
Date: 30 October 2026

| # | Sample Input | Expected Result | Actual Result | Status |
|---|---|---|---|---|
| 1 | https://www.example.com/login | No listed warning signs | No listed warning signs found. This does NOT prove safety. | PASS |
| 2 | http://192.0.2.10/account | IP address and HTTP warnings | Uses an IP address instead of a familiar domain. Uses HTTP. HTTPS alone does not prove trust. | PASS |
| 3 | http://example.com@sample.invalid/login | @ symbol and HTTP warnings | Contains an @ symbol; inspect carefully. Uses HTTP. HTTPS alone does not prove trust. | PASS |
| 4 | https://a.b.c.d.e.example.invalid/path | Many hostname segments warning | Contains many hostname segments/subdomains. | PASS |
| 5 | https://xn--example.invalid/ | Punycode warning | Contains a punycode-style hostname. | PASS |

## Testing Summary

Total tests: 5  
Passed: 5  
Failed: 0

## Additional Improvement Tests

| Test | Input | Expected Result |
|---|---|---|
| Multiple URL testing | Multiple URLs followed by q | All URLs are checked and q exits the program. |
| Malformed URL handling | http://[bad | Displays an invalid URL format message without crashing. |
