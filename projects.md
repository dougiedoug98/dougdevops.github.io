---
layout: default
title: Projects
description: Portfolio of DevOps, cybersecurity, and infrastructure projects by Douglas Collins
---

# Projects

<div style="background: rgba(0, 255, 0, 0.05); padding: 1rem; border-left: 3px solid #00ff00; margin-bottom: 2rem;">
Here's a curated showcase of projects I've architected and implemented. These range from enterprise infrastructure deployments to personal lab experiments that push the boundaries of what's possible with modern DevOps tools.
</div>

---

<div style="display: grid; gap: 2rem; margin: 2rem 0;">

  <!-- Project 1 -->
  <article style="border: 1px solid #00ff00; padding: 1.5rem; border-radius: 5px; background: rgba(0, 255, 0, 0.02);">
    <h3 style="margin-top: 0; color: #00ff00;">🔧 Network Segmentation + VLAN Rollout</h3>

    <div style="display: grid; gap: 0.5rem; margin: 1rem 0;">
      <div><strong>Objective:</strong> Restructure flat Layer 2 network into segmented VLANs for enhanced security and performance</div>
      <div><strong>Environment:</strong> Manufacturing plant with 200+ devices</div>
      <div><strong>Technologies:</strong> Cisco Catalyst, Meraki, Palo Alto Firewalls, DHCP, VLAN tagging, Cisco DNA Center</div>
    </div>

    <p style="margin: 1rem 0;"><strong>Implementation Highlights:</strong></p>
    <ul style="margin: 0.5rem 0;">
      <li>Designed and deployed 8 VLANs separating IT/OT networks, guest access, and management traffic</li>
      <li>Configured inter-VLAN routing with Palo Alto firewall policies</li>
      <li>Reduced broadcast domains by 75%, improving network performance</li>
      <li>Implemented zero-trust segmentation following NIST guidelines</li>
    </ul>

    <div style="margin-top: 1rem; padding: 0.75rem; background: rgba(0, 255, 0, 0.05); border-left: 2px solid #00ff00;">
      <strong>Impact:</strong> Improved security posture, reduced attack surface, enabled granular traffic monitoring
    </div>
  </article>

  <!-- Project 2 -->
  <article style="border: 1px solid #00ff00; padding: 1.5rem; border-radius: 5px; background: rgba(0, 255, 0, 0.02);">
    <h3 style="margin-top: 0; color: #00ff00;">🖥️ Automated Patch Management (WSUS + PowerShell)</h3>

    <div style="display: grid; gap: 0.5rem; margin: 1rem 0;">
      <div><strong>Objective:</strong> Automate monthly Windows patching across 150+ servers with minimal downtime</div>
      <div><strong>Environment:</strong> Enterprise Windows Server infrastructure</div>
      <div><strong>Technologies:</strong> WSUS, PowerShell, Group Policy Objects (GPO), Task Scheduler</div>
    </div>

    <p style="margin: 1rem 0;"><strong>Implementation Highlights:</strong></p>
    <ul style="margin: 0.5rem 0;">
      <li>Developed PowerShell scripts for automated patch approval and deployment scheduling</li>
      <li>Created maintenance windows with automated pre/post-reboot checks</li>
      <li>Built compliance dashboard tracking patch status across server fleet</li>
      <li>Implemented rollback procedures for failed updates</li>
    </ul>

    <div style="margin-top: 1rem; padding: 0.75rem; background: rgba(0, 255, 0, 0.05); border-left: 2px solid #00ff00;">
      <strong>Impact:</strong> Reduced manual patching time by 80%, achieved 95%+ patch compliance rate
    </div>
  </article>

  <!-- Project 3 -->
  <article style="border: 1px solid #00ff00; padding: 1.5rem; border-radius: 5px; background: rgba(0, 255, 0, 0.02);">
    <h3 style="margin-top: 0; color: #00ff00;">☁️ Personal Homelab (Virtualization + Monitoring)</h3>

    <div style="display: grid; gap: 0.5rem; margin: 1rem 0;">
      <div><strong>Objective:</strong> Build a production-grade home lab for learning and testing enterprise tools</div>
      <div><strong>Environment:</strong> Self-hosted infrastructure with 24/7 uptime</div>
      <div><strong>Technologies:</strong> Proxmox, pfSense, Zabbix, Docker, Ansible, Grafana, Pi-hole</div>
    </div>

    <p style="margin: 1rem 0;"><strong>Architecture Components:</strong></p>
    <ul style="margin: 0.5rem 0;">
      <li>Proxmox hypervisor hosting 15+ VMs (Linux/Windows mix)</li>
      <li>pfSense firewall with VPN (WireGuard), DNS filtering, and traffic shaping</li>
      <li>Zabbix + Grafana for infrastructure monitoring and alerting</li>
      <li>Docker swarm running containerized services (Nextcloud, Git server, media server)</li>
      <li>Automated provisioning with Ansible playbooks</li>
      <li>Internal CA for SSL/TLS certificates</li>
    </ul>

    <div style="margin-top: 1rem; padding: 0.75rem; background: rgba(0, 255, 0, 0.05); border-left: 2px solid #00ff00;">
      <strong>Impact:</strong> Hands-on learning environment for DevOps tools, serves as proof-of-concept for enterprise solutions
    </div>
  </article>

  <!-- Project 4 -->
  <article style="border: 1px solid #00ff00; padding: 1.5rem; border-radius: 5px; background: rgba(0, 255, 0, 0.02);">
    <h3 style="margin-top: 0; color: #00ff00;">🔐 Security Event Monitoring PoC</h3>

    <div style="display: grid; gap: 0.5rem; margin: 1rem 0;">
      <div><strong>Objective:</strong> Detect lateral movement and suspicious activity in Windows networks</div>
      <div><strong>Environment:</strong> Lab simulation with attack scenarios</div>
      <div><strong>Technologies:</strong> Wazuh SIEM, ELK Stack (Elasticsearch, Logstash, Kibana), Sysmon, Windows Event Forwarding</div>
    </div>

    <p style="margin: 1rem 0;"><strong>Implementation Highlights:</strong></p>
    <ul style="margin: 0.5rem 0;">
      <li>Deployed Wazuh agents across lab environment for centralized log collection</li>
      <li>Configured Sysmon for detailed process, network, and file activity logging</li>
      <li>Built custom detection rules for SMB enumeration, privilege escalation, and credential theft</li>
      <li>Created Kibana dashboards for real-time security monitoring</li>
      <li>Simulated MITRE ATT&CK techniques to validate detection capabilities</li>
    </ul>

    <div style="margin-top: 1rem; padding: 0.75rem; background: rgba(0, 255, 0, 0.05); border-left: 2px solid #00ff00;">
      <strong>Impact:</strong> Successfully detected 90%+ of simulated attacks, validated SIEM effectiveness for production use
    </div>
  </article>

</div>

---

<div style="text-align: center; margin-top: 3rem; padding: 2rem; background: rgba(0, 255, 0, 0.05); border-radius: 5px;">
  <h3>Interested in discussing these projects?</h3>
  <p>I'd love to share more details about the technical challenges and solutions.</p>
  <a href="/contact" class="tech-button" style="margin-top: 1rem;">Get in Touch</a>
</div>
