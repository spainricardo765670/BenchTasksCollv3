# Final Pool

All tasks marked **implemented** in the Notion **Task Tracker** page, collected under `tasks/finalpool/`.

- Source repository: `toolathlon/BenchTasksCollv3`
- Selection: every tracker entry whose `Task Status` is `implemented` after auditing the newest task-adding commit on each developer branch.
- Total: **63 tasks** (54 previously marked implemented + 9 newly verified).
- Each task directory is copied verbatim from its developer branch; the developer sub-directory is flattened, so a task lives at `tasks/finalpool/<task-name>/`.

## Audit rule

A task is `implemented` when it contains every file/folder present in `tasks/examples/example-task` (existence check only, per `tasks/examples/example-task/readme.txt`):

```
docs/agent_system_prompt.md
docs/task.md
docs/user_system_prompt.md
evaluation/main.py
groundtruth_workspace/
initial_workspace/
preprocess/main.py
```

Otherwise it is `implementing` and is not included in this pool.

## Newly verified tasks

| Task | Branch | Commit |
| --- | --- | --- |
| `audit-logger` | `yuzhen-dev` | `c68265dafe0a` |
| `client-portal` | `lueyang-dev` | `bf8b9a1d25ed` |
| `currency-converter` | `junxian_dev` | `96bbc11b6fc7` |
| `insights-engine` | `lv` | `0be3288e0fd4` |
| `media-organizer` | `haoze` | `e0072cf97954` |
| `resource-monitor` | `yuzhen-dev` | `c68265dafe0a` |
| `robots-handler` | `gyy` | `9612ffff3707` |
| `social-connector` | `junxian_dev` | `96bbc11b6fc7` |
| `tag-manager` | `gyy` | `9612ffff3707` |

## Full pool

| Task | Source branch |
| --- | --- |
| `activity-logger` | `lueyang-dev` |
| `alert-system` | `yuzhen-dev` |
| `asset-optimizer` | `yuxuan-dev` |
| `audit-logger` | `yuzhen-dev` |
| `backup-utility` | `xiaochen_dev` |
| `blog-engine` | `gyy` |
| `booking-system` | `junteng_dev` |
| `calendar-sync` | `junteng_dev` |
| `canvas-automation` | `ruige` |
| `canvas-grade-automation` | `jl_dev` |
| `chat-bot` | `lv` |
| `client-portal` | `lueyang-dev` |
| `cms-builder` | `gyy` |
| `content-manager` | `yuxuan-dev` |
| `content-scheduler` | `gyy` |
| `coupon-manager` | `fan-dev` |
| `crm-system` | `lueyang-dev` |
| `currency-converter` | `junxian_dev` |
| `data-analytics` | `ruige` |
| `data-validator` | `yuzhen-dev` |
| `deal-manager` | `lueyang-dev` |
| `deployment-tool` | `xiaochen_dev` |
| `email-campaign` | `lueyang-dev` |
| `email-classification-system` | `jl_dev` |
| `error-tracker` | `xiaochen_dev` |
| `expense-tracker` | `ruige` |
| `feedback-collector` | `lv` |
| `file-manager` | `ruige` |
| `follow-up-reminder` | `lueyang-dev` |
| `form-builder` | `yuzhen-dev` |
| `image-processor` | `wenshuo-dev` |
| `insights-engine` | `lv` |
| `invoice-generator` | `yuzhen-dev` |
| `lead-tracker` | `lueyang-dev` |
| `load-balancer` | `zhaochen` |
| `media-organizer` | `haoze` |
| `monitoring-agent` | `xiaochen_dev` |
| `network-analyzer` | `yuxuan-dev` |
| `order-processor` | `junteng_dev` |
| `payment-processor` | `yuzhen-dev` |
| `pdf-report-generator` | `jl_dev` |
| `permission-manager` | `yuzhen-dev` |
| `personalization-service` | `lv` |
| `price-tracker` | `fan-dev` |
| `product-catalog` | `junteng_dev` |
| `qr-generator` | `junxian_dev` |
| `reminder-service` | `junteng_dev` |
| `resource-monitor` | `yuzhen-dev` |
| `robots-handler` | `gyy` |
| `sales-pipeline` | `lueyang-dev` |
| `search-engine` | `wenshuo-dev` |
| `security-scanner` | `xiaochen_dev` |
| `sentiment-analyzer` | `lv` |
| `shipment-tracker` | `junteng_dev` |
| `social-connector` | `junxian_dev` |
| `social-publisher` | `gyy` |
| `subtitle-generator` | `haoze` |
| `tag-manager` | `gyy` |
| `task-scheduler` | `yuxuan-dev` |
| `template-engine` | `zhaochen` |
| `translation-api` | `junxian_dev` |
| `video-trimmer` | `haoze` |
| `voice-processor` | `lv` |

## Notes

- `lueyang-dev`: the tip commit refines `territory-manager` / `client-portal`; `client-portal` is complete, while `territory-manager` lost `preprocess/main.py` and has no `initial_workspace/`, so it stays `implementing`.
- `yuxuan-dev`: the tip commit also dropped a second, unnamed task's files directly at `tasks/yuxuan/` (`docs/`, `evaluation/`, `groundtruth_workspace/`). That is not a valid task directory, so only `sync-service` was tracked; it is `implementing`.
- No `task_config.json` exists in any task on any developer branch, nor in the example template itself; the structural file/folder check above is therefore the applied criterion.

This branch lives on the fork `spainricardo765670/BenchTasksCollv3` because the upstream repository is read-only for the working account, and is submitted to upstream via pull request.