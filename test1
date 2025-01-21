# Wazuh: Open-Source EDR for Real-Time Threat Detection

## Introduction
Wazuh is an open-source, scalable, and flexible security monitoring platform that provides real-time visibility into your IT infrastructure. It is designed to help organizations detect, monitor, and respond to security threats. Originally developed as a host-based Intrusion Detection System (HIDS), Wazuh has evolved into a full-featured EDR (Endpoint Detection and Response) solution with capabilities that include log analysis, file integrity monitoring, and vulnerability detection.

Whether you're protecting a small home network or scaling up for enterprise security, Wazuh offers powerful tools to detect anomalies, track incidents, and ensure compliance with security regulations.

---

## Key Features
- **Real-Time Monitoring:** Get live alerts and notifications for suspicious activities.
- **Log Data Analysis:** Aggregate and analyze logs from your servers, applications, and network devices.
- **File Integrity Monitoring:** Detect unauthorized changes to files or system configurations.
- **Vulnerability Detection:** Identify unpatched software vulnerabilities.
- **Scalability:** Easily scale from a single server to hundreds of devices across your network.
- **Open-Source and Free:** Full functionality with no licensing fees.

---

## Installing Wazuh on Ubuntu Server

Follow these steps to install Wazuh on an Ubuntu server. We’ll set up Wazuh Manager, which will be responsible for managing and collecting data from your agents.

### Step 1: Update Your System
Before starting, make sure your system is up-to-date. Run the following commands:
```bash
sudo apt update
sudo apt upgrade -y
```

### Step 2: Install Dependencies
Wazuh requires several dependencies for its installation. Install them using:
```bash
sudo apt install curl apt-transport-https lsb-release -y
```

### Step 3: Add the Wazuh Repository
Next, add the Wazuh repository to your system:
```bash
curl -s https://packages.wazuh.com/4.x/debian/wazuh.repo | sudo tee /etc/apt/sources.list.d/wazuh.list
```

### Step 4: Install Wazuh Manager
Now, install the Wazuh Manager:
```bash
sudo apt update
sudo apt install wazuh-manager -y
```

### Step 5: Start and Enable Wazuh Manager
After installation, start the Wazuh Manager and ensure it starts on boot:
```bash
sudo systemctl start wazuh-manager
sudo systemctl enable wazuh-manager
```

### Step 6: Install the Wazuh API (Optional)
The Wazuh API allows for easier management and integration. To install it, run:
```bash
sudo apt install wazuh-api -y
```

### Step 7: Install Wazuh Agent on Your Devices
To monitor other devices, install the Wazuh agent on them. For Ubuntu, you can do this with:
```bash
sudo apt install wazuh-agent -y
```

### Step 8: Configure the Agent
After installation, configure the agent by editing the configuration file to point it to the Wazuh Manager:
```bash
sudo nano /var/ossec/etc/ossec.conf
```
In the `<server>` section, replace the `address` with the IP address of your Wazuh Manager:
```xml
<address>your_wazuh_manager_ip</address>
```

Save and close the file.

### Step 9: Start and Enable the Wazuh Agent
Start the agent and enable it to run on boot:
```bash
sudo systemctl start wazuh-agent
sudo systemctl enable wazuh-agent
```

### Step 10: Verify Installation
To ensure that everything is running correctly, you can check the status of the Wazuh Manager and Agent:
```bash
sudo systemctl status wazuh-manager
sudo systemctl status wazuh-agent
```

---

## Conclusion

Now you’ve successfully installed Wazuh on your Ubuntu server and are ready to start monitoring your environment. Whether you're an individual securing your home network or part of a larger team managing enterprise infrastructure, Wazuh offers a powerful, flexible, and cost-effective way to enhance your security posture.

For more details, troubleshooting, and additional configurations, visit the [Wazuh Documentation](https://documentation.wazuh.com).

Feel free to contribute or raise any issues directly on this page.
