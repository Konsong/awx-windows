Job Template → Variables
---
win_updates_reset_wu_cache: true
win_updates_revoke_pause_expiry: true
win_updates_uso_scan_mode: deep
win_updates_uso_before_install: true
win_updates_uso_scan_wait_sec: 180
win_updates_verify_debug: true

Inventories → homelab_lcl_inventory → Groups → windows_servers → Edit.

---
ansible_connection: winrm
ansible_port: 5985
ansible_winrm_transport: ntlm
ansible_winrm_server_cert_validation: ignore

# group_vars/windows_servers.yml içeriği:
win_updates_category_names:
  - "*"
win_updates_server_selection: windows_update
win_updates_revoke_pause_expiry: true
win_updates_reset_wu_cache: false
win_updates_uso_scan_mode: deep
win_updates_uso_before_install: true
win_updates_wuauclt_detect_before_install: true
win_updates_pre_install_wait_sec: 20
win_updates_reboot: true
win_updates_reboot_timeout: 3600
win_updates_skip_optional: false
win_updates_log_enabled: true
win_updates_log_dir: 'C:\AnsibleLogs'
win_updates_log_path: 'C:\AnsibleLogs\win_updates.log'
win_updates_max_passes: 3
win_updates_retry_delay_sec: 30
win_updates_post_reboot_delay_sec: 90
win_updates_usoclient_before_verify: true
win_updates_uso_scan_wait_sec: 180
win_updates_verify_debug: false
win_updates_reject_list: []
win_updates_accept_list: []
