## Lite version of Magisk Delta

- MagiskHide in whitelist mode, called SuList
- SuList is forcefully enabled and cannot be disabled
- Magisk is hidden from all app processes by default except processes you added to sulist.
- SuList CLI: `magisk --sulist`

## Changelog

### 2e44b93e-delta-lite

- Switch back to ptrace for now
- No longer automatically add SystemUI

### 3e1b2387-delta-lite

- Fix the problem that SuList is being detected

### ac67cd10-delta-lite

- Refactor magisk.rc

### 5f3a89e9-delta-lite

- Fix SuList mount nosuid issue
- Make magic mount read-only

### 977a4546-delta-lite

- Enable SuList unconditionally

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