# **Update DuckDNS**

> I created this repo to overcome an issue that I was having with Metronet and DuckDNS.
> Metronet uses a sort of NAT which doesn't map directly back to my router. So, with this playbook, I can update DuckDNS with the WAN IP on my router, instead of the one it auto-discovers (Metronet's NAT'd IP address).  

### **Variables:**
  - **DOMAINS**: Comma separated list of the domains to update  
  - **IP_ADDRESS**: IP to use in the update  
  - **TOKEN**: DuckDNS token  
  - **BASE_URL**: Base URL of the update address  

I've moved most of the variable into **Secrets** since I plan to run this with GitHub Actions. 
IF you intend to run this locally, then you would simply "un-comment" and re-implement.

