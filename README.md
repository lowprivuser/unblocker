# unblocker
Burp Suite extension for encoding/decoding EVM calldata


## 0x00_prerequisites
1. Burp Suite
2. Java 8+
3. Python 2.7

## 0x01_installation
1. clone this repository
2. in Burp, go to Extender->Options
    1. in the Java Environment section add "<install_dir>/unblocker/" as "Folder for loading library JAR files"
    2. in the Python Environment section:
    3. add "<install_dir>/unblocker/jython-standalone-2.7.2.jar" as "Location of Jython standalone JAR file"
    4. add "<install_dir>/unblocker/src/lib" as "Folder for loading modules"
3. in Burp, go to Extender->Extensions
    1. click "Add" in the Burp Extensions section and select "<install_dir>/unblocker/unblocker.py" as "Extension file (.jar)"--Burp will detect the filetype automatically
    2. confirm the installation by approving all subsequent modal windows

## 0x02_usage
Unblocker features ABI-less EVM calldata decoding but you can also provide the ABI yourself if you know it.
Encoding does require ABI to be provided.

Input data strings have to be provided like so: `"s'hello, world'"`
Input data bytes have to be provided like so: `"b'deadbeef'"`
Input data structs have to be provided with square brackets instead of parenthesis, like so: `("s'some string'", true, 123)`