# Synology app mover

<a href="https://github.com/007revad/Synology_app_mover/releases"><img src="https://img.shields.io/github/release/007revad/Synology_app_mover.svg"></a>
<a href="https://hits.seeyoufarm.com"><img src="https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=https%3A%2F%2Fgithub.com%2F007revad%2FSynology_app_mover&count_bg=%2379C83D&title_bg=%23555555&icon=&icon_color=%23E7E7E7&title=views&edge_flat=false"/></a>
[![](https://img.shields.io/static/v1?label=Sponsor&message=%E2%9D%A4&logo=GitHub&color=%23fe8e86)](https://github.com/sponsors/007revad)
[![committers.top badge](https://user-badge.committers.top/australia/007revad.svg)](https://user-badge.committers.top/australia/007revad)

### Description

Easily move Synology packages from one volume to another volume

You just select the package and the destination volume and the script will stop the app, move it, update the symlinks then start the app.

Handy for moving packages to an SSD volume.

  - Supports DSM 7. Not tested with DSM 6.


### Packages confirmed working (or being tested)

<details>
  <summary>Click here to see list</summary>

| Package Center Name | System Name | Result |
|---------------------|-------------|--------|
| Active Backup for Business | ActiveBackup | Still Testing... |
| Active Backup for Google Workspace | ActiveBackup-GSuite | Still Testing... |
| Active Backup for Microsoft Office 365 | ActiveBackup-Office365 | Still Testing... |
| Advanced Media Extensions | CodecPack | OK |
| AntiVirus Essential |  | OK |
| AntiVirus by McAfee |  | OK |
| Apache 2.4 |  | OK |
| Audio Station | AudioStation | OK |	
| Bitdefender for MailPlus |  |  |
| C2 Identity LDAP Server | C2IdentityLDAPAgent | OK but I don't have a C2 account to fully test |
| Cloud Sync | CloudSync | OK |
| Central Management System | CMS | OK |
| Container Manager | ContainerManager | OK |
| Directory Server For Windows Domain | DirectoryServerForWindowsDomain | OK |
| DNS Server | DNSServer | OK |
| DHCP Server |  |  |
| Document Viewer |  |  |
| Download Station | DownloadStation | OK |
| Emby Server | Emby | OK |
| exFAT Access | exFAT-Free | OK |
| git | git | OK |
| Git | Git | OK |
| Glacier Backup |  |  |
| Hyper Backup | HyperBackup | OK |
| Hyper Backup Vault | HyperBackupVault | OK |
| LDAP Server |  |  |
| LogAnalysis | LogAnalysis | OK |
| Log Center |  | OK |
| Mail Station |  | OK |
| MariaDB 10 |  | OK |
| Media Server |  | OK |
| MediaInfo |  | OK |
| Migration Asssitant |  |  |
| MinimServer |  | OK |
| Node.js v14 | Node.js_v14 | OK |
| Node.js v16 | Node.js_v16 | OK |
| Node.js v18 | Node.js_v18 | OK |
| Node.js v20 | Node.js_v20 | OK |
| Note Station | NoteStation | OK |
| PDF Viewer |  | OK |
| Perl | Perl | OK |
| PHP 7.3 | PHP7.3 | OK |
| PHP 7.4 | PHP7.4 | OK |
| PHP 8.0 | PHP8.0 | OK |
| PHP 8.1 | PHP8.1 | OK |
| PHP 8.2 | PHP8.2 | OK |
| Plex Media Server | PlexMediaServer | OK |
| Presto File Server | PrestoServer | OK |
| Proxy Server |  | OK |
| Python 3.9 | Python3.9 | OK |
| Radius Server |  | OK |
| SMI-S Provider |  |  |
| Snapshot Replication | SnapshotReplication | OK |
| SSO Server |  | OK |
| Storage Analyzer | StorageAnalyzer | OK |
| Surveillance Station | SurveillanceStation | OK |
| SynoCli Tools | synocli-"toolname" | OK |
| Synology Application Service | SynologyApplicationService | OK |
| Synology Calendar | Calendar | OK |
| Synology Chat Server | Chat | OK |
| Synology Contacts | Contacts | OK |
| Synology Directory Server |  | OK |
| Synology Drive Server | SynologyDrive | OK |
| Synology High Availability |  |  |
| Synology MailPlus | MailPlus | OK |
| Synology MailPlus Server | MailPlus-Server | OK |
| Synology Mail Server |  | OK |
| Synology Office | Spreadsheet | OK |
| Synology Photos | SynologyPhotos | OK |
| Syno Smis Provider |  | OK |
| Tailscale | Tailscale | OK |
| Text Editor |  | OK |
| Universal Viewer | UniversalViewer | OK |
| Video Station | VideoStation | OK |
| Virtual Machine Manager | Virtualization | OK |
| VPN Server |  | OK |
| Web Station | WebStation | OK |
| WebDAV Server |  | OK |

</details>

#### Packages not tested

<details>
  <summary>Click here to see list</summary>

| Package | Result |
|---------|--------|
| Archiware P5 |  |
| BRAVIA Signage |  |
| Data Deposit Box |  |
| Domotz Network Monitoring |  |
| ElephantDrive |  |
| GoodSync |  |
| IDrive |  |
| KodiExplorer |  |
| MEGAcmd |  |
| NAKIVO Backup and Replication |  |
| NAKIVO Transporter |  |
| Ragic Cloud DB |  |
| Resilo Sync |  |
| TeamViewer |  |
| VirtualHere |  |

</details>

#### Packages that won't be tested

<details>
  <summary>Click here to see list</summary>

These need MarioDB and they either fail to install or don't run properly!?!?

**Note:** I will not test any package that needs MariaDB.

| Package | Result |
|---------|--------|
| Joomla | Doesn't install |
| MediaWiki | Doesn't install |
| PACS |  Won't test |
| phpMyAdmin | Won't test |
| Wordpress | Won't test |
| vtigerCRM | Installs but doesn't run |

</details>


### Download the script

1. Download the latest version _Source code (zip)_ from https://github.com/007revad/Synology_app_mover/releases
2. Save the download zip file to a folder on the Synology.
3. Unzip the zip file.

### To run the script

[How to enable SSH and login to DSM via SSH](https://kb.synology.com/en-global/DSM/tutorial/How_to_login_to_DSM_with_root_permission_via_SSH_Telnet)

```YAML
sudo -i /volume1/scripts/syno_app_mover.sh
```

**Note:** Replace /volume1/scripts/ with the path to where the script is located.

### Troubleshooting

If the script won't run check the following:

1. Make sure you download the zip file and unzipped it to a folder on your Synology (not on your computer).
2. If the path to the script contains any spaces you need to enclose the path/scriptname in double quotes:
   ```YAML
   sudo -i "/volume1/my scripts/syno_app_mover.sh"
   ```
3. Make sure you unpacked the zip or rar file that you downloaded and are trying to run the syno_app_mover.sh file.
4. Set the script file as executable:
   ```YAML
   sudo chmod +x "/volume1/scripts/syno_app_mover.sh"
   ```

### DSM 7 screenshots

<p align="center">Moving a package (with dependencies)</p>
<p align="center"><img src="/images/app2.png"></p>

<br>

<p align="center">Moving packages with shared folders</p>
<p align="center"><img src="/images/app3.png"></p>
<p align="center"><img src="/images/app4.png"></p>

<br>

<p align="center">Moving a package that has a volume location setting</p>
<p align="center"><img src="/images/app5.png"></p>

