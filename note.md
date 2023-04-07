## 90f5dec2-delta-lite

- Better logcat detection, check if log system is working normally before doing unmount Magisk from zygote processes.

### Lite version of Magisk Delta'

- Sulist - MagiskHide in whitelist mode (also called Dynamic mount)
- Use system logcat to detect start up app processes instead of ptrace. Please test `su -c logcat -b events -s am_proc_start` before installing. **If logcat is not working normally, SuList will be disabled itself.**
- SuList is forcefully enabled and cannot be disabled. Magisk is hidden from all app processes by default.
- SuList CLI: `magisk --sulist`
- Support remounting system as read-write without breaking mount.
- Support SuList only. Zygisk function is cut off to reduce magisk code and binary size.
- Support partial modules, only apps that are on sulist will have all modules mounted. System Server, SystemUI and Settings are whitelist-ed by default.
- In most case, only main process is needed to be added to SuList, not all processes.
- Open source and internal version. It is only released in discussion group.
