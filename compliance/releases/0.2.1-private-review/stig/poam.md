# POA&M — ubuntu24_stig / stig

StigForge docker verify (OpenSCAP). Policy-exempt rules are excluded from the score denominator.
Failure buckets follow stigready `poam-from-arf.py` classification (N/A / risk-accepted / gap).

**Score:** 55.81% (floor 90.0%) — below floor

## OpenSCAP failures — classified (19)

### Gap - deterministic config (fixable in role) (6)

- `accounts_password_pam_unix_rounds_password_auth`
- `accounts_passwords_pam_faillock_audit`
- `accounts_passwords_pam_faillock_deny`
- `accounts_passwords_pam_faillock_interval`
- `accounts_passwords_pam_faillock_silent`
- `accounts_passwords_pam_faillock_unlock_time`

### Gap - role vs SSG (scheduled remediation) (13)

- `account_disable_post_pw_expiration`
- `accounts_max_concurrent_login_sessions`
- `accounts_maximum_age_login_defs`
- `accounts_minimum_age_login_defs`
- `accounts_passwords_pam_faildelay_delay`
- `accounts_umask_etc_login_defs`
- `banner_etc_profiled_ssh_confirm`
- `clean_components_post_updating`
- `display_login_attempts`
- `file_groupowner_var_log`
- `file_permissions_var_log_stig`
- `package_pam_pwquality_installed`
- `set_password_hashing_algorithm_auth_stig`

## Policy exempt — not scored (34)

- `accounts_password_pam_enforce_root`
- `auditd_audispd_configure_remote_server`
- `auditd_offload_logs`
- `configure_opensc_card_drivers`
- `dconf_gnome_screensaver_idle_delay`
- `dconf_gnome_session_idle_user_locks`
- `ensure_root_password_configured`
- `force_opensc_card_drivers`
- `grub2_admin_username`
- `grub2_password`
- `grub2_set_password`
- `grub2_uefi_password`
- `grub2_unique_name`
- `install_smartcard_packages`
- `installed_OS_is_vendor_supported`
- `package_nss_sss_installed`
- `package_opensc_installed`
- `package_pam_sss_installed`
- `package_pcsc-lite_installed`
- `package_subscription-manager_installed`
- `rsyslog_encrypt_offload_defaultnetstreamdriver`
- `rsyslog_remote_access_monitoring`
- `rsyslog_remote_loghost`
- `service_pcscd_enabled`
- `smartcard_configure_ca`
- `smartcard_configure_cert_checking`
- `smartcard_configure_crl`
- `smartcard_pam_enabled`
- `sssd_certificate_verification`
- `sssd_enable_certmap`
- `sssd_enable_smartcards`
- `sudo_remove_nopasswd`
- `sudo_require_authentication`
- `sudo_require_reauthentication`

