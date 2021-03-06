| Shell Command |Docker Environment Variable |Description | Default Value |
| :------------ | :------------  | :------------ | :------------ |
| `-r` or`--run` | QBT_RUN |Run without the scheduler. Script will exit after completion. | False |
| `-sch` or `--schedule` | QBT_SCHEDULE  | Schedule to run every x minutes. (Default set to 1440 (1 day))  | 1440 |
| `-sd` or `--startup-delay` | QBT_STARTUP_DELAY  | Set delay in seconds on the first run of a schedule (Default set to 0)  | 0 |
| `-c CONFIG` or `--config-file CONFIG` | QBT_CONFIG  | This is used if you want to use a different name for your config.yml. `Example: tv.yml`  | config.yml |
| `-lf LOGFILE,` or `--log-file LOGFILE,` | QBT_LOGFILE | This is used if you want to use a different name for your log file. `Example: tv.log` | activity.log |
| `-cs` or `--cross-seed` | QBT_CROSS_SEED | Use this after running [cross-seed script](https://github.com/mmgoodnow/cross-seed) to add torrents from the cross-seed output folder to qBittorrent  | False |
| `-re` or `--recheck` | QBT_RECHECK | Recheck paused torrents sorted by lowest size. Resume if Completed.  | False |
| `-cu` or `--cat-update` | QBT_CAT_UPDATE |  Use this if you would like to update your categories.  | False |
| `-tu` or `--tag-update` | QBT_TAG_UPDATE |  Use this if you would like to update your tags and/or set seed goals/limit upload speed by tag. (Only adds tags to untagged torrents) | False |
| `-ru` or `--rem-unregistered` | QBT_REM_UNREGISTERED |  Use this if you would like to remove unregistered torrents. (It will the delete data & torrent if it is not being cross-seeded, otherwise it will just remove the torrent without deleting data). Trackers that have an error and not covered by the remove unregistered logic will also be tagged as `issue` for manual review.| False |
| `-tte` or `--tag-tracker-error` | QBT_TAG_TRACKER_ERROR |  Use this if you would like to tag torrents that do not have a working tracker. | False |
| `-ro` or `--rem-orphaned` | QBT_REM_ORPHANED | Use this if you would like to remove orphaned files from your `root_dir` directory that are not referenced by any torrents. It will scan your `root_dir` directory and compare it with what is in qBittorrent. Any data not referenced in qBittorrent will be moved into `/data/torrents/orphaned_data` folder for you to review/delete. | False |
| `-tnhl` or `--tag-nohardlinks` | QBT_TAG_NOHARDLINKS | Use this to tag any torrents that do not have any hard links associated with any of the files. This is useful for those that use Sonarr/Radarr that hard links your media files with the torrents for seeding. When files get upgraded they no longer become linked with your media therefore will be tagged with a new tag noHL. You can then safely delete/remove these torrents to free up any extra space that is not being used by your media folder. | False |
| `-sr` or `--skip-recycle` | QBT_SKIP_RECYCLE | Use this to skip emptying the Reycle Bin folder (`/root_dir/.RecycleBin`). | False |
| `-dr` or `--dry-run` | QBT_DRY_RUN |   If you would like to see what is gonna happen but not actually move/delete or tag/categorize anything. | False |
| `-ll` or `--log-level LOGLEVEL` | QBT_LOG_LEVEL |   Change the ouput log level. | INFO |
| `-d` or `--divider` | QBT_DIVIDER |   Character that divides the sections (Default: '=') | = |
| `-w` or `--width` | QBT_WIDTH |   Screen Width (Default: 100) | 100 |