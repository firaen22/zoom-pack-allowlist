# Zoom Starter Pack Allowlist

Device allowlist for the `zoom-starter-pack` Claude plugin.

This file is read by the plugin to determine which devices are authorized to run the District morning Zoom routine.

## Schema

```json
{
  "updated_at": "ISO timestamp",
  "approved":  [ { "deviceId", "deviceName", "userName", "approvedAt" } ],
  "rejected":  [ { "deviceId", "deviceName", "userName", "rejectedAt" } ],
  "pending":   [ { "deviceId", "deviceName", "userName", "requestedAt" } ]
}
```

## How approvals happen

The admin approves devices via Telegram commands (`/approve_pack`, `/reject_pack`, `/revoke_pack`) which commit changes to this file via the Telegram bot.

## Raw URL (used by plugin)

```
https://raw.githubusercontent.com/firaen22/zoom-pack-allowlist/main/approved-devices.json
```
