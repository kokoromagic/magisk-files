## Lite version of Magisk Delta

- Sulist - MagiskHide in whitelist mode
- Use system logcat to detect start up app processes instead of ptrace. Please test `su -c logcat -b events -s am_proc_start` before installing. **If logcat is not working normally, SuList will be disabled itself.**
- SuList is forcefully enabled and cannot be disabled. Magisk is hidden from all app processes by default.
- SuList CLI: `magisk --sulist`
- Support remounting system as read-write without breaking mount.
- Support SuList only. Zygisk function is cut off to reduce magisk code and binary size.
- Support partial modules, only apps that are on sulist will have all modules mounted. System Server, SystemUI and Settings are whitelist-ed by default.
- In most case, only main process is needed to be added to SuList, not all processes.
- Open source and internal version. It is only released in discussion group.

## Changelog

### cb2f1d74-delta-lite

- Better hiding Magisk
- Refactor mounting mirror again (Prepare for v26)

### 38d98145-delta-lite

- Don't care about Zygisk
- Use `/data/adb/modules` instead of `MAGISKTMP/.magisk/modules`
- Fix clean hidelist option doesn't work

### dae0693c-delta-lite

- Introduce new UI

### 27773b9e-delta-lite

- Show SuList notification correctly

### 90f5dec2-delta-lite

- Better logcat detection, check if log system is working normally before doing unmount Magisk from zygote processes.

### d930b3b1-delta-lite

- Refactor SU mount

### 194d9ea2-delta-lite

- Refactor UI
- Fix Logcat tracing

### 484e04a0-delta-lite

- Clean more code

### e67e4f22-delta-lite

- Since we are tracing app process start by `logcat` and SuList is started on boot, we don't need to kill `usap`
- Fix rescanning zygote process

### 061e3e6e-delta-lite

- Initial release