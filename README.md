# SECU74000

These are the files for SECU-74000.

Update 2025-08-05
- new versions of containers
- new options for compose files:
- for owncloud:  EXTRA_IP is an IP address that will be accepted that is neither localhost nor the primary IP (useful for containers behind firewall with published NAT port)
- for code-server, jupyter:
  - option USE_OWNCLOUD=YES must be used if 'backend'ed to owncloud.  If owncloud container is linked to this container, no need specify address.  Otherwise, OC_URL should be used to specify the entire URL of the owncloud server
  - option OC_USER=username is the username to be used for remote owncloud
  - option OC_PASS=password is the password to be used for remote owncloud
- if you wish to use an external volume:
  - for codeserver use:
```
    volumes:
      - ./data:/shared
```
  - for jupyter use: 
```
    volumes:
      - ./data:/home/jupyter/work
```
as always, if something isn't quite right, please contact Professor SteveH via your school email account.

Minor update 2024-12-23
- with Kali 2024.3, the sudo apt install docker-compose is no longer fully supported
- follow instruction on downloading docker compose plugin
- the bash script updated to allow for this new version of docker compose
- update the commented lines for codeserver container

Updated on 2024-12-21
- pushed into 'yearless' repo
- updated versions
- embraced dockers stacks architecture
- due to advancements in Jupyter text editor, code-server not in use

Minor update 2024-04-6
- jupyter container adds 32bit compiler libraries

Updated on 2024-04-04
- version bump from v2.0 to v3.0 of docker images.  If poblems, revert to :2.0 on all 3 images and email Professor Steve.

Any question/concerns, contact Professor SteveH via your school email account.
