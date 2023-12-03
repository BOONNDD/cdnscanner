
### CDN Scanner

![MrBOOND](https://github.com/BOONNDD/cdnscanner/blob/main/Screenshot_%D9%A2%D9%A0%D9%A2%D9%A3-%D9%A1%D9%A2-%D9%A0%D9%A4-%D9%A0%D9%A2-%D9%A5%D9%A3-%D9%A4%D9%A3-%D9%A4%D9%A1%D9%A1_com.termux.jpg) <!-- Replace with an image link or remove this line -->

CDN Scanner is a Python tool designed to scan IP addresses or ranges for CDN (Content Delivery Network) services. It checks if a given IP is served by popular CDN providers such as Cloudflare or Cloudfront.

#### Features

- Single IP and IP range scanning
- Multi-threaded scanning for faster results
- Support for proxy usage
- Save results to files

#### Usage

1. Clone the repository:

   ```bash
   git clone https://github.com/BOONNDD/cdnscanner.git
   cd cdn-scanner
   ```

2. Install the required dependencies:

   ```bash
   pip install -r requirements.txt
   ```

3. Run the tool:

   ```bash
   python cdnscanner.py [IP_INPUT] [OPTIONS]
   ```

   Replace `[IP_INPUT]` with the target IP address or range. Additional options can be specified:

   - `-t, --threads`: Number of threads to use (default is 10)
   - `-p, --port`: Port to scan (default is 80)
   - `-P, --proxy`: Proxy IP and port (e.g., 12.34.56.6:80)
   - `-o, --output`: Save output to a file
   - `-f, --file`: Read IP addresses from a file

#### Examples

- Scan a single IP:

  ```bash
  python cdnscanner.py 192.168.1.1
  ```

- Scan an IP range:

  ```bash
  python cdnscanner.py 192.168.1.0/24
  ```

- Scan using a proxy:

  ```bash
  python cdnscanner.py 192.168.1.1 -P 12.34.56.6:80
  ```

- Scan from a file:

  ```bash
  python cdnscanner.py -f ip_addresses.txt
  ```

#### Output

The tool generates two output files:

- `cloudflare_cloudfront_results.txt`: Contains results for Cloudflare and Cloudfront.
- `successful_results.txt`: Contains successful scan results.
