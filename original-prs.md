# Pull Requests — Arriven/db1000n

Total: **306** pull requests


## #568 add --source Parameter
**State:** MERGED | **Author:** @OleksandrBlack | **Date:** 2023-12-10 | **Branch:** source_param → main | **+3/-0** | **Files:** 1

> default:
> --source standalone
> possible launch source options:
> --source adss
> --source itarmykit

<details><summary>Files changed (1)</summary>

- `src/job/base.go` (+3/-0)
</details>

## #565 Added flag for periodic GC invocation 
**State:** MERGED | **Author:** @millfreedom | **Date:** 2022-08-13 | **Branch:** main → main | **+29/-0** | **Files:** 2

> # Description
> Added flag for periodic GC invocation  to reduce overall memory consuption in pooling scenarios (db1000nx100)
> 
> ## Type of change
> - [x] New feature (non-breaking change which adds functionality)
> 
> ## How Has This Been Tested?
> manually tested

<details><summary>Comments (1)</summary>

- **@millfreedom** (2022-08-13): @arriven Богдане, пінг. Гляньте, чи можете прийняти PR.
</details>

<details><summary>Files changed (2)</summary>

- `main.go` (+25/-0)
- `src/utils/utils.go` (+4/-0)
</details>

## #564 Update README.md
**State:** MERGED | **Author:** @vanillajonathan | **Date:** 2022-08-08 | **Branch:** patch-1 → main | **+3/-4** | **Files:** 1

> # Description
> 
> Please include a summary of the change and which issue is fixed. Please also include relevant motivation and context. List any dependencies that are required for this change.
> 
> Fixes # (issue)
> 
> ## Type of change
> 
> Please delete options that are not relevant.
> 
> - [ ] Bug fix...

<details><summary>Files changed (1)</summary>

- `README.md` (+3/-4)
</details>

## #562 Update install.sh for armv6
**State:** MERGED | **Author:** @app/ | **Date:** 2022-08-08 | **Branch:** main → main | **+4/-3** | **Files:** 1

> # Description
> 
> Use armv6 binary for architecture for armv7
> 
> Fixes # (issue)
> 
> ## Type of change
> 
> - [x] Bug fix (non-breaking change which fixes an issue)
> 
> 
> ## How Has This Been Tested?
> 
> Please describe the tests that you ran to verify your changes. Provide instructions so we can...

<details><summary>Files changed (1)</summary>

- `install.sh` (+4/-3)
</details>

## #552 Add `-less-stats` cmd param to group targets by protocols
**State:** MERGED | **Author:** @roman-kruglov | **Date:** 2022-06-11 | **Branch:** less-stats → main | **+36/-18** | **Files:** 3

> # Description
> 
> Adds a cmd line parameter `-less-stats` to group all target stats by protocols. Currently the list of stats could be very long and it's not always convenient to observe.
> 
> Maybe "fewer" would be more grammatical, but I guess "less" is kinda more conventional for text and more...

<details><summary>Files changed (3)</summary>

- `main.go` (+5/-4)
- `src/utils/metrics/metrics.go` (+21/-6)
- `src/utils/metrics/reporter.go` (+10/-8)
</details>

## #551 docs: move markdown config in one single place
**State:** MERGED | **Author:** @iamtodor | **Date:** 2022-06-09 | **Branch:** docs_put_markdown_rules_in_one_place → main | **+1/-1** | **Files:** 2

> # Description
> 
> Removed additional config file, and moved the exclude rule to a single place where we hold and configure markdown rules.
> 
> Fixes # (issue)
> 
> ## Type of change
> 
> - [x] Documentation update
> 
> ## How Has This Been Tested?
> 
> Please describe the tests that you ran to verify your...

<details><summary>Files changed (2)</summary>

- `.mdlrc` (+0/-1)
- `db1000n.rb` (+1/-0)
</details>

## #548 perf: add buffering in metrics table reporter
**State:** MERGED | **Author:** @deputinizer | **Date:** 2022-06-02 | **Branch:** feature/statsbuf → main | **+11/-2** | **Files:** 1

> Writing letter-by-letter is very inefficient.
> On kinda slow machines, the whole table was printing in like 10 seconds word by word.
> This commit prevents these write calls
> because now, everything is added to a 4096-byte buffer and flushed in the end.
> Multiple 1-byte write syscalls were made...

<details><summary>Files changed (1)</summary>

- `src/utils/metrics/reporter.go` (+11/-2)
</details>

## #547 Mobile support (android, ios)
**State:** OPEN | **Author:** @roman-kruglov | **Date:** 2022-06-11 | **Branch:** mobile-support → main | **+179/-3** | **Files:** 6

> # Description
> 
> Made with `fyne` - a terminal emulator which supports text selection and copying; for mobile platforms. Also respects dark and light themes. If you remove the theming code - the terminal is only 65 lines long. Note: it doesn't need any manifests - fyne enables networking / internet...

<details><summary>Files changed (6)</summary>

- `Icon.png` (+0/-0)
- `go.mod` (+14/-0)
- `go.sum` (+44/-2)
- `main.go` (+11/-1)
- `src/platform/mobile/terminal.go` (+99/-0)
- `src/platform/mobile/terminal_stub.go` (+11/-0)
</details>

## #544 add hcloud_server output
**State:** MERGED | **Author:** @andruwa13 | **Date:** 2022-05-25 | **Branch:** main → main | **+3/-0** | **Files:** 1

> Add output ip

<details><summary>Files changed (1)</summary>

- `terraform/hetzner_cloud/outputs.tf` (+3/-0)
</details>

## #538 Switch console log time format to RFC3339
**State:** MERGED | **Author:** @roman-kruglov | **Date:** 2022-05-08 | **Branch:** change-console-log-time-format → main | **+5/-0** | **Files:** 1

> instead of default epoch floating time
> 
> # Description
> 
> This format should be more familiar for users. Why not ISO8601 - to my taste RFC3339 is a tad more readable. Although both formats are almost interchangeable.
> 
> ## Type of change
> 
> - [x] Breaking change (fix or feature that would cause...

<details><summary>Files changed (1)</summary>

- `main.go` (+5/-0)
</details>

## #536 Fixed log message for prometheus server
**State:** MERGED | **Author:** @bogdanprodanj | **Date:** 2022-05-08 | **Branch:** log_fix → main | **+7/-3** | **Files:** 1

> # Description
> 
> This PR fixes an incorrect log printed when the service execution is canceled.
> 
> ## Type of change
> 
> - [x] Log fix
> 
> ## How Has This Been Tested?
> 
> When stopping the service execution using Ctrl+C incorrect logs are no longer...

<details><summary>Files changed (1)</summary>

- `src/utils/metrics/serve.go` (+7/-3)
</details>

## #535 Performance + protocol fixes
**State:** CLOSED | **Author:** @deputinizer | **Date:** 2022-06-24 | **Branch:** main → main | **+2463/-168** | **Files:** 28

> # Description
> 
> Performance fixes + HTTP 1.1 protocol fix.
> 
> Fixes 
> - #533 
> - #534
> - #528
> 
> ## Type of change
> 
> 
> - [x] Bug fix: ctrl+C slowly responding even without prometheus metrics
> - [x] New feature: tls.Config cache in metrics
> - [x] Breaking change / fix: SkipBody did unintended...

<details><summary>Comments (8)</summary>

- **@deputinizer** (2022-05-06): Lol why use lint :sob:  Lint disallows `this` and `self`
- **@deputinizer** (2022-05-07): <details>   <summary>[Spoiler] We can make DNS resolver use almost 0% CPU</summary> ...
- **@deputinizer** (2022-05-07): <details>   <summary>[Spoiler] Works.</summary>    ![image](https://user-images.githubusercontent.com/100740281/167231678-a250e5fe-b349-4c80-934f-843cd5cdc228.png)  However, I think this linter...
- **@deputinizer** (2022-05-07): Also, stoppropaganda + db1000n authors should do some collab and on rewriting the whole thing in Rust.
- **@deputinizer** (2022-05-07): These templates are not entirely necessary... <details>   <summary>Spoiler: pprof memory</summary>  ...
- **@deputinizer** (2022-05-07): Probably fixed #528
- **@deputinizer** (2022-05-08): Ok since @Arriven commited changes already, I'm closing due to merge conflicts.
- **@roman-kruglov** (2022-05-08): maybe just rebase, I'm sure there isn't a lot of conflicts
</details>

<details><summary>Files changed (28)</summary>

- `go.mod` (+1/-0)
- `go.sum` (+2/-0)
- `main.go` (+7/-6)
- `src/core/countrychecker/countrychecker.go` (+157/-0)
- `src/core/customresolver/customresolver.go` (+75/-0)
- `src/core/customtcpdial/customtcpdial.go` (+376/-0)
- `src/core/customtcpdial/resolvefix.go` (+27/-0)
- `src/core/http/http.go` (+31/-8)
- `src/core/packetgen/connection.go` (+4/-1)
- `src/core/spdnsclient/addrselect.go` (+391/-0)
- `src/core/spdnsclient/hook.go` (+21/-0)
- `src/core/spdnsclient/ip.go` (+157/-0)
- `src/core/spdnsclient/ipsock.go` (+12/-0)
- `src/core/spdnsclient/lookup.go` (+221/-0)
- `src/core/spdnsclient/net.go` (+57/-0)
- `src/core/spdnsclient/parse.go` (+97/-0)
- `src/core/spdnsclient/singleflight/singleflight.go` (+123/-0)
- `src/core/spdnsclient/unixlike_dnsclient.go` (+570/-0)
- `src/core/spdnsclient/unixlike_dnsconfig.go` (+85/-0)
- `src/job/complex.go` (+2/-0)
- `src/job/http.go` (+4/-1)
- `src/job/packetgen.go` (+1/-0)
- `src/job/rawnet.go` (+2/-0)
- `src/job/utils.go` (+1/-0)
- `src/utils/backoff.go` (+4/-0)
- `src/utils/countrychecker.go` (+0/-141)
- `src/utils/metrics/prometheus.go` (+23/-7)
- `src/utils/proxy.go` (+12/-4)
</details>

## #531 Fix a crash when interface name is empty
**State:** CLOSED | **Author:** @roman-kruglov | **Date:** 2022-05-04 | **Branch:** fix-bind-crash → main | **+6/-1** | **Files:** 1

> # Description
> 
> Main's top crashes with lots of errors about dereferencing nil. Happens in Bind(). Because `getSockaddrByName()` can return `nil` in lots of cases. Not sure if I fixed it entirely correctly, but this is my take on it. Maybe instead of returning nil this route needs to evade...

<details><summary>Files changed (1)</summary>

- `src/utils/utils_unix.go` (+6/-1)
</details>

## #530 Fix double total stats reported in table simple output
**State:** MERGED | **Author:** @roman-kruglov | **Date:** 2022-05-05 | **Branch:** fix-double-totals → main | **+21/-60** | **Files:** 2

> # Description
> 
> When run with simple output format the table reported doubled total stats. There was an additional loop for totals which I didn't notice when copied table's formatter implementation. Also I shrank the table implementation a bit.
> 
> ## Type of change
> 
> - [x] Bug fix (non-breaking...

<details><summary>Files changed (2)</summary>

- `src/utils/metrics/reporter.go` (+21/-25)
- `src/utils/metrics/stats.go` (+0/-35)
</details>

## #519 Simple output improvements (also make simple output format default)
**State:** MERGED | **Author:** @roman-kruglov | **Date:** 2022-04-28 | **Branch:** simple-output-improvement → main | **+294/-208** | **Files:** 7

> # Description
> 
> I want to improve it further to show a pretty summary like before. For this I split `Reporter` into several implementations - for zap and console.
> 
>  Also `simple` output format is made default now.
> 
> It's a work in progress - I intend to split `mectrics.go` into several files....

<details><summary>Comments (1)</summary>

- **@roman-kruglov** (2022-04-27): Guys, could somebody look through the pr with a fresh eye to make sure I didn't fuck up memory somewhere. Pretty exhausted right now, I'll skim over it again in the morning.
</details>

<details><summary>Files changed (7)</summary>

- `main.go` (+21/-5)
- `src/job/http.go` (+7/-2)
- `src/job/runner.go` (+17/-16)
- `src/utils/metrics/accumulator.go` (+55/-0)
- `src/utils/metrics/metrics.go` (+20/-185)
- `src/utils/metrics/reporter.go` (+80/-0)
- `src/utils/metrics/stats.go` (+94/-0)
</details>

## #518 Combine metrics summary into one object
**State:** MERGED | **Author:** @roman-kruglov | **Date:** 2022-04-25 | **Branch:** combine-report → main | **+16/-10** | **Files:** 1

> so the whole report goes as one log entry with a JSON object for each target
> 
> # Description
> 
> This might be helpful for logging and assessing to have the whole summary report as one entry. Though arguably it makes it even less readable in terminal's output, and I tried to improve that with pr...

<details><summary>Comments (3)</summary>

- **@roman-kruglov** (2022-04-25): I have several more ideas regarding this and simple output too, I'll have more improvements
- **@arriven** (2022-04-25): I've added a change that groups up all the targets into an object to simplify parsing (you can safely iterate on all keys in targets json object instead of having to filter root keys), please be aware
- **@roman-kruglov** (2022-04-25): > I've added a change that groups up all the targets into an object to simplify parsing (you can safely iterate on all keys in targets json object instead of having to filter root keys), please be...
</details>

<details><summary>Files changed (1)</summary>

- `src/utils/metrics/metrics.go` (+16/-10)
</details>

## #517 Add a new flag `-log-format` and a `simple` format
**State:** MERGED | **Author:** @roman-kruglov | **Date:** 2022-04-25 | **Branch:** simple-terminal-output → main | **+17/-2** | **Files:** 1

> the most human readable format for those who only look at the output in a terminal
> 
> # Description
> 
> With the recent switch to `zap` as the used logger it became much harder to just look at terminal's output. If you just run it manually and the output is for reading rather than logging, using...

<details><summary>Comments (1)</summary>

- **@roman-kruglov** (2022-04-25): > I would maybe even go ahead and make it the default format in next release  yeah, exactly, I was thinking the same thing, but thought it would be too much to ask for this with my first pr :) I'll...
</details>

<details><summary>Files changed (1)</summary>

- `main.go` (+17/-2)
</details>

## #514 Added aarch64 architecture
**State:** MERGED | **Author:** @impFred | **Date:** 2022-04-23 | **Branch:** patch-1 → main | **+1/-0** | **Files:** 1

> For some devices (like PinePhone), OS_ARCH is aarch64, which is the same as arm64.
> 
> # Description
> 
> Please include a summary of the change and which issue is fixed. Please also include relevant motivation and context. List any dependencies that are required for this change.
> 
> Fixes #...

<details><summary>Files changed (1)</summary>

- `install.sh` (+1/-0)
</details>

## #508 update manual and fix public key for Win instance
**State:** CLOSED | **Author:** @ralfeus | **Date:** 2022-07-21 | **Branch:** main → main | **+58/-3** | **Files:** 3

> # Description
> 
> Update manual and fix public key upload for Windows instance
> 
> Fixes # (issue)
> 
> ## Type of change
> 
> - [x] Bug fix (non-breaking change which fixes an issue)
> - [x] Documentation update
> 
> ## How Has This Been Tested?
> 
> 1. Provision Windows instance
> 2. Log on with private key option
> 3....

<details><summary>Comments (1)</summary>

- **@arriven** (2022-04-15): @ralfeus you have conflicts in the PR, can you resolve them? I could do it in the web editor like I did for your previous PR but it seems like it leads to further conflicts
</details>

<details><summary>Files changed (3)</summary>

- `ansible/aws/AWS.pub` (+1/-0)
- `ansible/aws/README.md` (+51/-2)
- `ansible/aws/aws-provisioning.yaml` (+6/-1)
</details>

## #507 Update StartDB1000N.bat
**State:** MERGED | **Author:** @nicolaspbl | **Date:** 2022-04-15 | **Branch:** patch-2 → main | **+3/-3** | **Files:** 1

> Add -UseBasicParsing in Invoke-WebRequest to avoid this error message :
> 
> "The response content cannot be parsed because the Internet Explorer engine is not available, or Internet Explorer's first-launch configuration is not complete. Specify the UseBasicParsing parameter and try again."
> 
> #...

<details><summary>Files changed (1)</summary>

- `scripts/StartDB1000N.bat` (+3/-3)
</details>

## #505 Update Windows EC2 instance
**State:** MERGED | **Author:** @ralfeus | **Date:** 2022-04-14 | **Branch:** main → main | **+16/-2** | **Files:** 3

> # Description
> 
> - Replaced Windows AMI with OpenSSH server installed 
> - Copy public key to the Windows server
> - Reset password upon new Windows EC2 instance spin up
> 
> ## Type of change
> 
> - [x] New feature (non-breaking change which adds functionality)
> 
> ## How Has This Been Tested?
> 
> On...

<details><summary>Files changed (3)</summary>

- `ansible/aws/AWS.pub` (+1/-0)
- `ansible/aws/README.md` (+11/-1)
- `ansible/aws/aws-provisioning.yaml` (+4/-1)
</details>

## #502 AWS provisioning playbook and account creation manual
**State:** MERGED | **Author:** @ralfeus | **Date:** 2022-04-13 | **Branch:** main → main | **+60/-0** | **Files:** 2

> # Description
> 
> Please include a summary of the change and which issue is fixed. Please also include relevant motivation and context. List any dependencies that are required for this change.
> 
> Fixes # (issue)
> 
> ## Type of change
> 
> Please delete options that are not relevant.
> 
> - [x] New...

<details><summary>Files changed (2)</summary>

- `ansible/aws/README.md` (+5/-0)
- `ansible/aws/aws-provisioning.yaml` (+55/-0)
</details>

## #497 Update StartDB1000N.bat
**State:** MERGED | **Author:** @nicolaspbl | **Date:** 2022-04-08 | **Branch:** patch-1 → main | **+1/-1** | **Files:** 1

> Change "$Asset.name -match" as file name to download for windows is "db1000n_windows_amd64.zip"
> 
> # Description
> 
> Without that change, file is not downloaded as previous regexp doesn't match Asset-name
> 
> Fixes # (issue)
> 
> ## Type of change
> 
> Please delete options that are not relevant.
> 
> - [...

<details><summary>Files changed (1)</summary>

- `scripts/StartDB1000N.bat` (+1/-1)
</details>

## #496 Update link for Hetzner Cloud to the latest release
**State:** MERGED | **Author:** @Amet13 | **Date:** 2022-04-07 | **Branch:** main → main | **+2/-3** | **Files:** 2

> # Description
> 
> Due to the latest changes to release naming structure we can get rid of hardcode for Hetzner Cloud release.
> 
> ## Type of change
> 
> - [x] Breaking change (fix or feature that would cause existing functionality to not work as expected)
> 
> ## How Has This Been Tested?
> 
> - [x] Wget...

<details><summary>Files changed (2)</summary>

- `terraform/heroku/terraform.tfvars` (+1/-1)
- `terraform/hetzner_cloud/user_data.yml` (+1/-2)
</details>

## #488 AWS Lightsail support
**State:** MERGED | **Author:** @Amet13 | **Date:** 2022-04-04 | **Branch:** main → main | **+91/-2** | **Files:** 8

> # Description
> 
> AWS Lightsail support added
> 
> Fixes #224
> 
> ## Type of change
> 
> - [x] New feature (non-breaking change which adds functionality)
> - [x] Documentation update
> 
> ## Test Configuration
> 
> - Release version: latest 
> - Platform: docker
> <img width="983" alt="Screenshot 2022-04-04 at...

<details><summary>Comments (2)</summary>

- **@amaestr0** (2022-04-05): @Arriven , has the multiple containers per service been added in scope of this changes? Should existing containers be redeployed?
- **@Amet13** (2022-04-05): @amaestr0 you can scale containers by changing `scale` parameter in TF vars: https://github.com/Arriven/db1000n/blob/main/terraform/aws_lightsail/terraform.tfvars#L1  >Should existing containers be...
</details>

<details><summary>Files changed (8)</summary>

- `docs/advanced-docs/terraform/aws_lightsail.md` (+6/-0)
- `terraform/aws_lightsail/README.md` (+24/-0)
- `terraform/aws_lightsail/main.tf` (+18/-0)
- `terraform/aws_lightsail/provider.tf` (+13/-0)
- `terraform/aws_lightsail/terraform.tfvars` (+3/-0)
- `terraform/aws_lightsail/variables.tf` (+25/-0)
- `terraform/heroku/terraform.tfvars` (+1/-1)
- `terraform/hetzner_cloud/user_data.yml` (+1/-1)
</details>

## #487 Pass an URL to a proxy list using `proxy-path` flag
**State:** CLOSED | **Author:** @Kashkovsky | **Date:** 2022-04-04 | **Branch:** main → main | **+32/-3** | **Files:** 4

> Fixes #475
> 
> ## Type of change
> - [x] New feature (non-breaking change which adds functionality)
> - [x] Documentation update
> 
> ## How Has This Been Tested?
> 
> ```
> ./db1000n -proxy-path https://raw.githubusercontent.com/porthole-ascend-cinnamon/proxy_scraper/main/proxies.txt
> ```

<details><summary>Comments (1)</summary>

- **@arriven** (2022-04-04): > This particular approach is almost the same as downloading that proxylist, reformatting it with simple commandline and passing it directly into the command. Current approach re-downloads the...
</details>

<details><summary>Files changed (4)</summary>

- `docs/advanced-docs/configuration.md` (+3/-1)
- `main.go` (+2/-0)
- `src/job/base.go` (+25/-0)
- `src/utils/templates/templates.go` (+2/-2)
</details>

## #484 Implement the new metrics Reporter
**State:** MERGED | **Author:** @jdoe7865623 | **Date:** 2022-04-12 | **Branch:** metrics → main | **+626/-824** | **Files:** 19

> This is a work in progress for feedback, migration to the new reporter is not done yet.
> 
> The new console stats will tentatively look as follows:
> 
> ```
>  --- Traffic stats ---
>  |            Target | Requests attempted | Requests sent | Responses received | Data sent | Data received |
>  |...

<details><summary>Comments (5)</summary>

- **@roman-kruglov** (2022-04-06): Hi! I thought about something similar too, to better inform the user about the results and thus efficiency. So I had one more thought - maybe it should somehow specify summarised response codes and...
- **@roman-kruglov** (2022-04-06): Also had an idea to replace those tons of duplicated repetitive messages about starting a thread for a target like ``` 2022/04/06 17:07:48.414177 http.go:147: Attacking **sample** 2022/04/06...
- **@jdoe7865623** (2022-04-07): > Hi! I thought about something similar too, to better inform the user about the results and thus efficiency. So I had one more thought - maybe it should somehow specify summarised response codes and...
- **@jdoe7865623** (2022-04-07): > Also had an idea to replace those tons of duplicated repetitive messages about starting a thread for a target like >  > ``` > 2022/04/06 17:07:48.414177 http.go:147: Attacking...
- **@roman-kruglov** (2022-04-07): ok, yep, I'll try. I have several small ideas to start from.
</details>

<details><summary>Files changed (19)</summary>

- `src/core/dnsblast/dns-blast.go` (+79/-135)
- `src/core/dnsblast/dns-blast_test.go` (+1/-26)
- `src/core/dnsblast/dns-dhh.go` (+0/-94)
- `src/core/dnsblast/dns-dhh_test.go` (+0/-38)
- `src/core/dnsblast/qry/types.go` (+0/-171)
- `src/core/dnsblast/qry/types_test.go` (+0/-91)
- `src/core/packetgen/connection.go` (+27/-12)
- `src/core/slowloris/slowloris.go` (+35/-55)
- `src/job/base.go` (+2/-1)
- `src/job/complex.go` (+8/-9)
- `src/job/dnsblast.go` (+4/-3)
- `src/job/http.go` (+24/-27)
- `src/job/packetgen.go` (+10/-12)
- `src/job/rawnet.go` (+12/-16)
- `src/job/runner.go` (+20/-45)
- `src/job/slowloris.go` (+3/-12)
- `src/job/utils.go` (+13/-12)
- `src/utils/metrics/metrics.go` (+204/-65)
- `src/utils/metrics/metrics_internal_test.go` (+184/-0)
</details>

## #483 Ansible role for AWS instance creation and account creation instruction
**State:** CLOSED | **Author:** @ralfeus | **Date:** 2022-04-07 | **Branch:** main → main | **+116/-0** | **Files:** 2

> # Description
> An Ansible playbook that creates Linux instance on AWS account  and instruction on AWS account creation and playbook execution
> 
> ## Type of change
> 
> Please delete options that are not relevant.
> 
> - [ ] Bug fix (non-breaking change which fixes an issue)
> - [x] New feature (non-breaking...

<details><summary>Files changed (2)</summary>

- `ansible/aws/README.md` (+1/-0)
- `ansible/aws/aws-provisioning.yaml` (+115/-0)
</details>

## #479 only send lastmodified and etag if present
**State:** MERGED | **Author:** @arriven | **Date:** 2022-04-02 | **Branch:** fix-config-fetch → main | **+11/-2** | **Files:** 1

> # Description
> 
> Please include a summary of the change and which issue is fixed. Please also include relevant motivation and context. List any dependencies that are required for this change.
> 
> Fixes # (issue)
> 
> ## Type of change
> 
> Please delete options that are not relevant.
> 
> - [ ] Bug fix...

<details><summary>Files changed (1)</summary>

- `src/job/config/config.go` (+11/-2)
</details>

## #477 Heroku Go 1.18 and fixing small issues
**State:** MERGED | **Author:** @Amet13 | **Date:** 2022-04-01 | **Branch:** main → main | **+3/-7** | **Files:** 4

> # Description
> 
> - Heroku Go 1.18 (https://devcenter.heroku.com/changelog-items/2366)
> - Do not run shellcheck on Windows, it's redundant
> - Fix shellcheck for EKS script
> - Bump release for Hetzner Cloud
> 
> ## Type of change
> 
> - [x] Breaking change (fix or feature that would cause existing...

<details><summary>Files changed (4)</summary>

- `.github/workflows/test-installer.yaml` (+0/-4)
- `terraform/aws_eks/scripts/node-user-data.sh` (+1/-1)
- `terraform/heroku/main.tf` (+1/-1)
- `terraform/hetzner_cloud/user_data.yml` (+1/-1)
</details>

## #476 AWS EKS documentation updated
**State:** MERGED | **Author:** @localdotcom | **Date:** 2022-04-01 | **Branch:** aws-eks → main | **+99/-23** | **Files:** 1

> # Description
> 
> README.md updated
> 
> ## Type of change
> 
> Please delete options that are not relevant.
> 
> - [x] Documentation update
> 
> ## Screenshots
> 
> - [x] No screenshot

<details><summary>Files changed (1)</summary>

- `terraform/aws_eks/README.md` (+99/-23)
</details>

## #474 README.md for AWS EKS cluster added
**State:** CLOSED | **Author:** @localdotcom | **Date:** 2022-04-01 | **Branch:** aws-eks → main | **+1319/-0** | **Files:** 24

> # Description
> README.md for AWS EKS cluster added
> 
> ## Type of change
> 
> - [x] Documentation update
> 
> ## Screenshots
> 
> - [x] No screenshot

<details><summary>Comments (1)</summary>

- **@Amet13** (2022-04-01): I believe it would be easier to create a new PR with changed README only @localdotcom
</details>

<details><summary>Files changed (24)</summary>

- `terraform/aws/eks-cluster/README.md` (+88/-0)
- `terraform/aws/eks-cluster/data.tf` (+1/-0)
- `terraform/aws/eks-cluster/main.tf` (+59/-0)
- `terraform/aws/eks-cluster/modules/eks-cluster/data.tf` (+47/-0)
- `terraform/aws/eks-cluster/modules/eks-cluster/main.tf` (+107/-0)
- `terraform/aws/eks-cluster/modules/eks-cluster/outputs.tf` (+17/-0)
- `terraform/aws/eks-cluster/modules/eks-cluster/variables.tf` (+21/-0)
- `terraform/aws/eks-cluster/modules/eks-nodes/data.tf` (+46/-0)
- `terraform/aws/eks-cluster/modules/eks-nodes/main.tf` (+239/-0)
- `terraform/aws/eks-cluster/modules/eks-nodes/outputs.tf` (+8/-0)
- `terraform/aws/eks-cluster/modules/eks-nodes/variables.tf` (+106/-0)
- `terraform/aws/eks-cluster/modules/kubernetes/data.tf` (+1/-0)
- `terraform/aws/eks-cluster/modules/kubernetes/main.tf` (+272/-0)
- `terraform/aws/eks-cluster/modules/kubernetes/providers.tf` (+11/-0)
- `terraform/aws/eks-cluster/modules/kubernetes/variables.tf` (+27/-0)
- `terraform/aws/eks-cluster/modules/network/data.tf` (+3/-0)
- `terraform/aws/eks-cluster/modules/network/main.tf` (+124/-0)
- `terraform/aws/eks-cluster/modules/network/outputs.tf` (+19/-0)
- `terraform/aws/eks-cluster/modules/network/variables.tf` (+17/-0)
- `terraform/aws/eks-cluster/outputs.tf` (+35/-0)
- `terraform/aws/eks-cluster/providers.tf` (+4/-0)
- `terraform/aws/eks-cluster/scripts/node-user-data.sh` (+4/-0)
- `terraform/aws/eks-cluster/variables.tf` (+52/-0)
- `terraform/aws/eks-cluster/versions.tf` (+11/-0)
</details>

## #473 Docs for AWS
**State:** MERGED | **Author:** @Amet13 | **Date:** 2022-04-01 | **Branch:** main → main | **+43/-9** | **Files:** 34

> # Description
> 
> - split AWS EC2 and EKS configuration by different directories
> - add missed mkdocs for Vultr
> 
> ## Type of change
> 
> - [x] Documentation update

<details><summary>Files changed (34)</summary>

- `docs/advanced-docs/terraform/aws.md` (+0/-6)
- `docs/advanced-docs/terraform/aws_ec2.md` (+6/-0)
- `docs/advanced-docs/terraform/aws_eks.md` (+6/-0)
- `docs/advanced-docs/terraform/vultr.md` (+6/-0)
- `terraform/aws_ec2/README.md` (+1/-1)
- `terraform/aws_ec2/ireland.tfvars` (+0/-0)
- `terraform/aws_ec2/main.tf` (+0/-0)
- `terraform/aws_ec2/tor-proxy/tor-proxy.tf` (+0/-0)
- `terraform/aws_ec2/variables.tf` (+0/-0)
- `terraform/aws_eks/README.md` (+23/-0)
- `terraform/aws_eks/data.tf` (+0/-0)
- `terraform/aws_eks/main.tf` (+0/-0)
- `terraform/aws_eks/modules/eks-cluster/data.tf` (+0/-0)
- `terraform/aws_eks/modules/eks-cluster/main.tf` (+0/-0)
- `terraform/aws_eks/modules/eks-cluster/outputs.tf` (+0/-0)
- `terraform/aws_eks/modules/eks-cluster/variables.tf` (+0/-0)
- `terraform/aws_eks/modules/eks-nodes/data.tf` (+0/-0)
- `terraform/aws_eks/modules/eks-nodes/main.tf` (+0/-0)
- `terraform/aws_eks/modules/eks-nodes/outputs.tf` (+0/-0)
- `terraform/aws_eks/modules/eks-nodes/variables.tf` (+0/-0)
- `terraform/aws_eks/modules/kubernetes/data.tf` (+0/-0)
- `terraform/aws_eks/modules/kubernetes/main.tf` (+0/-0)
- `terraform/aws_eks/modules/kubernetes/providers.tf` (+0/-0)
- `terraform/aws_eks/modules/kubernetes/variables.tf` (+0/-0)
- `terraform/aws_eks/modules/network/data.tf` (+0/-0)
- `terraform/aws_eks/modules/network/main.tf` (+0/-0)
- `terraform/aws_eks/modules/network/outputs.tf` (+0/-0)
- `terraform/aws_eks/modules/network/variables.tf` (+0/-0)
- `terraform/aws_eks/outputs.tf` (+0/-0)
- `terraform/aws_eks/providers.tf` (+0/-0)
- `terraform/aws_eks/scripts/node-user-data.sh` (+0/-1)
- `terraform/aws_eks/variables.tf` (+0/-0)
- `terraform/aws_eks/versions.tf` (+0/-0)
- `terraform/heroku/terraform.tfvars` (+1/-1)
</details>

## #462 Fix azure neutral name readme
**State:** MERGED | **Author:** @slayer | **Date:** 2022-03-30 | **Branch:** neutral-name-readme → main | **+6/-6** | **Files:** 1

> # Description
> 
> Fix README for terraform azure
> 
> ## Type of change
> 
> Please delete options that are not relevant.
> 
> - [x] Bug fix (non-breaking change which fixes an issue)

<details><summary>Files changed (1)</summary>

- `terraform/azure/README.md` (+6/-6)
</details>

## #460 AWS EKS cluster autoscaler implementation
**State:** MERGED | **Author:** @localdotcom | **Date:** 2022-03-30 | **Branch:** aws-eks → main | **+1231/-0** | **Files:** 23

> # Description
> 
> This implementation allows to deploy AWS EKS multi-az cluster and and it's infrastructure including VPC, subnets and cluster autoscaler.
> 
> ## How Has This Been Tested?
> - [x] Cluster deployed
> 
> ## Test Configuration
> 
> - Platform: AWS
> 
> ## Screenshots
> 
> - [x] No screenshot

<details><summary>Comments (1)</summary>

- **@arriven** (2022-03-30): Could you fix the formatting here please?
</details>

<details><summary>Files changed (23)</summary>

- `terraform/aws/eks-cluster/data.tf` (+1/-0)
- `terraform/aws/eks-cluster/main.tf` (+59/-0)
- `terraform/aws/eks-cluster/modules/eks-cluster/data.tf` (+47/-0)
- `terraform/aws/eks-cluster/modules/eks-cluster/main.tf` (+107/-0)
- `terraform/aws/eks-cluster/modules/eks-cluster/outputs.tf` (+17/-0)
- `terraform/aws/eks-cluster/modules/eks-cluster/variables.tf` (+21/-0)
- `terraform/aws/eks-cluster/modules/eks-nodes/data.tf` (+46/-0)
- `terraform/aws/eks-cluster/modules/eks-nodes/main.tf` (+239/-0)
- `terraform/aws/eks-cluster/modules/eks-nodes/outputs.tf` (+8/-0)
- `terraform/aws/eks-cluster/modules/eks-nodes/variables.tf` (+106/-0)
- `terraform/aws/eks-cluster/modules/kubernetes/data.tf` (+1/-0)
- `terraform/aws/eks-cluster/modules/kubernetes/main.tf` (+272/-0)
- `terraform/aws/eks-cluster/modules/kubernetes/providers.tf` (+11/-0)
- `terraform/aws/eks-cluster/modules/kubernetes/variables.tf` (+27/-0)
- `terraform/aws/eks-cluster/modules/network/data.tf` (+3/-0)
- `terraform/aws/eks-cluster/modules/network/main.tf` (+124/-0)
- `terraform/aws/eks-cluster/modules/network/outputs.tf` (+19/-0)
- `terraform/aws/eks-cluster/modules/network/variables.tf` (+17/-0)
- `terraform/aws/eks-cluster/outputs.tf` (+35/-0)
- `terraform/aws/eks-cluster/providers.tf` (+4/-0)
- `terraform/aws/eks-cluster/scripts/node-user-data.sh` (+4/-0)
- `terraform/aws/eks-cluster/variables.tf` (+52/-0)
- `terraform/aws/eks-cluster/versions.tf` (+11/-0)
</details>

## #459 AWS EKS cluster autoscaler
**State:** CLOSED | **Author:** @localdotcom | **Date:** 2022-03-29 | **Branch:** aws-eks → main | **+1260/-0** | **Files:** 23

> # Description
> 
> This implementation allows to deploy AWS EKS multi-az cluster and and it's infrastructure including VPC, subnets and cluster autoscaler.
> 
> ## How Has This Been Tested?
> - [x] Cluster deployed
> 
> ## Test Configuration
> 
> - Platform: AWS
> 
> ## Screenshots
> 
> - [x] No screenshot

<details><summary>Files changed (23)</summary>

- `terraform/aws/eks-cluster-autoscaler/data.tf` (+1/-0)
- `terraform/aws/eks-cluster-autoscaler/main.tf` (+59/-0)
- `terraform/aws/eks-cluster-autoscaler/modules/eks-cluster/data.tf` (+48/-0)
- `terraform/aws/eks-cluster-autoscaler/modules/eks-cluster/main.tf` (+107/-0)
- `terraform/aws/eks-cluster-autoscaler/modules/eks-cluster/outputs.tf` (+17/-0)
- `terraform/aws/eks-cluster-autoscaler/modules/eks-cluster/variables.tf` (+21/-0)
- `terraform/aws/eks-cluster-autoscaler/modules/eks-nodes/data.tf` (+46/-0)
- `terraform/aws/eks-cluster-autoscaler/modules/eks-nodes/main.tf` (+262/-0)
- `terraform/aws/eks-cluster-autoscaler/modules/eks-nodes/outputs.tf` (+8/-0)
- `terraform/aws/eks-cluster-autoscaler/modules/eks-nodes/variables.tf` (+106/-0)
- `terraform/aws/eks-cluster-autoscaler/modules/kubernetes/data.tf` (+1/-0)
- `terraform/aws/eks-cluster-autoscaler/modules/kubernetes/main.tf` (+272/-0)
- `terraform/aws/eks-cluster-autoscaler/modules/kubernetes/providers.tf` (+11/-0)
- `terraform/aws/eks-cluster-autoscaler/modules/kubernetes/variables.tf` (+27/-0)
- `terraform/aws/eks-cluster-autoscaler/modules/network/data.tf` (+3/-0)
- `terraform/aws/eks-cluster-autoscaler/modules/network/main.tf` (+125/-0)
- `terraform/aws/eks-cluster-autoscaler/modules/network/outputs.tf` (+19/-0)
- `terraform/aws/eks-cluster-autoscaler/modules/network/variables.tf` (+17/-0)
- `terraform/aws/eks-cluster-autoscaler/outputs.tf` (+39/-0)
- `terraform/aws/eks-cluster-autoscaler/providers.tf` (+4/-0)
- `terraform/aws/eks-cluster-autoscaler/scripts/node-user-data.sh` (+4/-0)
- `terraform/aws/eks-cluster-autoscaler/variables.tf` (+52/-0)
- `terraform/aws/eks-cluster-autoscaler/versions.tf` (+11/-0)
</details>

## #458 Added terraform for Vultr
**State:** MERGED | **Author:** @aot9 | **Date:** 2022-03-30 | **Branch:** terraform_vultr → main | **+101/-0** | **Files:** 5

> # Description
> 
> Added terraform configuration for Vultr.
> Default config:
> - Docker Ubuntu 20.04
> - Seoul, South Korea
> - 1 cpu 1 gb ram
> - cronjob for periodic container restart
> 
> ## Type of change
> 
> Please delete options that are not relevant.
> 
> - [x] New feature (non-breaking change which...

<details><summary>Files changed (5)</summary>

- `terraform/vultr/README.md` (+33/-0)
- `terraform/vultr/main.tf` (+32/-0)
- `terraform/vultr/outputs.tf` (+3/-0)
- `terraform/vultr/scripts/deploy.sh` (+11/-0)
- `terraform/vultr/variable.tf` (+22/-0)
</details>

## #456 neutral name for terraform azure
**State:** MERGED | **Author:** @slayer | **Date:** 2022-03-29 | **Branch:** neutral-name → main | **+1/-1** | **Files:** 1

> # Description
> 
> Make azure terraform names more neutral to avoid banning
> 
> Fixes # (issue)
> 
> ## Type of change
> 
> Please delete options that are not relevant.
> 
> - [ ] Bug fix (non-breaking change which fixes an issue)
> - [ ] New feature (non-breaking change which adds functionality)
> - [ ]...

<details><summary>Comments (2)</summary>

- **@nonchalant-enthusiast** (2022-03-30): Please update https://github.com/Arriven/db1000n/blob/main/terraform/azure/README.md as it has code examples that rely on the old naming
- **@slayer** (2022-03-30): https://github.com/Arriven/db1000n/pull/462
</details>

<details><summary>Files changed (1)</summary>

- `terraform/azure/variables.tf` (+1/-1)
</details>

## #453 Move runner to job package; runner/config to job/config; GA stats to metrics
**State:** MERGED | **Author:** @jdoe7865623 | **Date:** 2022-03-28 | **Branch:** housekeeping → main | **+111/-108** | **Files:** 20

> This simplifies the packages structure and puts highly coupled components together. I plan to clean this up further.

<details><summary>Files changed (20)</summary>

- `.goreleaser.yaml` (+1/-1)
- `.ko.yaml` (+1/-1)
- `Makefile` (+1/-1)
- `docs/advanced-docs/config-encryption.md` (+2/-2)
- `main.go` (+9/-13)
- `src/job/base.go` (+4/-15)
- `src/job/complex.go` (+6/-5)
- `src/job/config/config.go` (+23/-12)
- `src/job/config/defaultconfig.go` (+0/-0)
- `src/job/config/updater.go` (+2/-2)
- `src/job/dnsblast.go` (+4/-3)
- `src/job/http.go` (+5/-4)
- `src/job/packetgen.go` (+3/-2)
- `src/job/rawnet.go` (+5/-4)
- `src/job/runner.go` (+15/-15)
- `src/job/slowloris.go` (+3/-2)
- `src/job/utils.go` (+13/-8)
- `src/utils/metrics/ga.go` (+1/-1)
- `src/utils/metrics/metrics.go` (+7/-8)
- `src/utils/templates/network.go` (+6/-9)
</details>

## #452 exponential backoff implementation
**State:** MERGED | **Author:** @arriven | **Date:** 2022-03-27 | **Branch:** exponential-backoff → main | **+121/-40** | **Files:** 5

> # Description
> 
> Introduce exponential backoff for http and tcp jobs loop to prevent cpu overload on failures
> 
> Fixes #448 
> 
> ## Type of change
> 
> Please delete options that are not relevant.
> 
> - [ ] New feature (non-breaking change which adds functionality)

<details><summary>Files changed (5)</summary>

- `src/jobs/base.go` (+3/-15)
- `src/jobs/http.go` (+3/-5)
- `src/jobs/rawnet.go` (+9/-4)
- `src/utils/backoff.go` (+89/-0)
- `src/utils/countrychecker.go` (+17/-16)
</details>

## #451 docker compose updater mode fix
**State:** MERGED | **Author:** @andser | **Date:** 2022-03-28 | **Branch:** main → main | **+1/-1** | **Files:** 1

> Fixes #450

<details><summary>Files changed (1)</summary>

- `examples/docker/static-docker-compose.yml` (+1/-1)
</details>

## #449 #448 Backoff sleeper implementation and a use example in country checker
**State:** CLOSED | **Author:** @jdoe7865623 | **Date:** 2022-03-28 | **Branch:** sleeper → main | **+91/-26** | **Files:** 4

> Refer to #448 for background.

<details><summary>Files changed (4)</summary>

- `main.go` (+3/-5)
- `src/jobs/base.go` (+10/-12)
- `src/utils/backoff_sleeper.go` (+62/-0)
- `src/utils/countrychecker.go` (+16/-9)
</details>

## #446 Mention --network host in the docs.
**State:** MERGED | **Author:** @michaelKaefer | **Date:** 2022-03-27 | **Branch:** patch-1 → main | **+12/-0** | **Files:** 2

> -

<details><summary>Comments (2)</summary>

- **@arriven** (2022-03-27): There's a trailing space somewhere in the index.uk.md, can you remove it?
- **@michaelKaefer** (2022-03-27): @Arriven  Sorry, fixed it.
</details>

<details><summary>Files changed (2)</summary>

- `docs/index.md` (+6/-0)
- `docs/index.uk.md` (+6/-0)
</details>

## #445 Make docker-compose not configurable
**State:** MERGED | **Author:** @PerchunPak | **Date:** 2022-03-27 | **Branch:** make-docker-compose-not-configurable → main | **+105/-15** | **Files:** 10

> # Description
> 
> This will make docker-compose.yml not configurable. Only OpenVPN can be configured. Reason of this: I really hate resolve "merge-conflicts" when updating my docker-compose system. I just want use `git pull && docker-compose pull` to update without anything else. This PR make it...

<details><summary>Comments (5)</summary>

- **@arriven** (2022-03-27): Ideally I'd want to have both this static version and old example of having multiple different providers present. Can you move that old version to the examples folder? (Also while you're at it could...
- **@PerchunPak** (2022-03-27): Moving this in example folder will ruin all sense of this PR. I want make updates with just few commands, instead of moving all edited files and after pull, move it back. Also there is only one...
- **@arriven** (2022-03-27): This docker compose doesn't depend on any files in the repo except those provider ones so you can have that immutable use case regardless of the folder it's in (yeah, you'd need to have one initial...
- **@PerchunPak** (2022-03-27): > benefit of having multiple vpn providers - if one goes temporarily down you still have others + it allows to disperse the traffic and make it harder to block attacks based on IP/geo  This will...
- **@arriven** (2022-03-27): As for 1 vpn vs multiple vpns vs proxies - proxylist is the easiest one to setup globally but it only supports some of attacks (I'm not sure if you can send upd or raw ip traffic through it, at least...
</details>

<details><summary>Files changed (10)</summary>

- `.gitignore` (+4/-0)
- `docs/advanced-docs/configuration.md` (+2/-2)
- `docs/advanced-docs/docker-vpn.md` (+14/-5)
- `examples/config/advanced/ddos-guard.yaml` (+0/-0)
- `examples/config/advanced/packetgen-ipv6.yaml` (+0/-0)
- `examples/config/advanced/packetgen.yaml` (+0/-0)
- `examples/config/http-host.yaml` (+0/-0)
- `examples/config/http-login.json` (+0/-0)
- `examples/docker/old-docker-compose.yml` (+8/-8)
- `examples/docker/static-docker-compose.yml` (+77/-0)
</details>

## #442 Updater docker-compose.yaml
**State:** MERGED | **Author:** @bitshape | **Date:** 2022-03-27 | **Branch:** docker-compose-for-ko → main | **+8/-28** | **Files:** 1

> # Description
> 
> * Updating example config path as they changed if the Docker image is built with `ko`
> * Removing healthcheck example commands as they won't work for `ko` images anymore
> 
> Fixes https://github.com/Arriven/db1000n/issues/439
> 
> ## Type of change
> 
> - [x] Bug fix (non-breaking...

<details><summary>Files changed (1)</summary>

- `docker-compose.yml` (+8/-28)
</details>

## #441 Fix updater exiting early
**State:** MERGED | **Author:** @bitshape | **Date:** 2022-03-27 | **Branch:** fix-updater → main | **+2/-2** | **Files:** 1

> # Description
> 
> https://github.com/Arriven/db1000n/commit/750f6bdf27af85a19427cc0bf63d0e23b157a384#diff-010176c2ca9e3ceeacb9d76da1fca2f2df823fd20df0bb68d2a773616e063de5 introduced a bug in updater where it will exit upon successful file download. Previously it would only exit if there's an issue...

<details><summary>Files changed (1)</summary>

- `src/runner/config/updater.go` (+2/-2)
</details>

## #440 Shellcheck and CI for install script
**State:** MERGED | **Author:** @Amet13 | **Date:** 2022-03-26 | **Branch:** main → main | **+26/-8** | **Files:** 3

> # Description
> 
> - Bump release for heroku deployment
> - CI for `install.sh` with shellcheck
> - Fix warnings from shellcheck in `install.sh`
> 
> ## Type of change
> 
> - [x] New feature (non-breaking change which adds functionality)
> - [x] Breaking change (fix or feature that would cause existing...

<details><summary>Files changed (3)</summary>

- `.github/workflows/test-installer.yaml` (+19/-2)
- `install.sh` (+6/-5)
- `terraform/heroku/terraform.tfvars` (+1/-1)
</details>

## #437 Reset metrics on config change
**State:** MERGED | **Author:** @Kashkovsky | **Date:** 2022-03-26 | **Branch:** main → main | **+8/-0** | **Files:** 2

> # Description
> 
> When the config is updated with new targets, metrics remain the same hence meaningless.
> My little proposal is to reset metrics on each config update to get relevant information about current targets.
> Sorry if anything is wrong, I learned Go yesterday.
> 
> Fixes # (issue)
> N/A
> ##...

<details><summary>Comments (2)</summary>

- **@arriven** (2022-03-26): Good idea, but can we make it a separate set of metrics instead? Ideally we'd show users both the general amount of traffic and traffic for latest targets as simple reset would probably be a bit...
- **@arriven** (2022-03-26): Thinking about it more, I'll probably merge it as is since everything else works as if the app was restarted when config changes
</details>

<details><summary>Files changed (2)</summary>

- `src/runner/runner.go` (+2/-0)
- `src/utils/metrics/metrics.go` (+6/-0)
</details>

## #436 Report GA metrics after writing stats to the console
**State:** MERGED | **Author:** @jdoe7865623 | **Date:** 2022-03-26 | **Branch:** metrics → main | **+8/-15** | **Files:** 1

<details><summary>Files changed (1)</summary>

- `src/runner/runner.go` (+8/-15)
</details>

## #431 Update Azure terraform config
**State:** MERGED | **Author:** @neatdecisions | **Date:** 2022-03-26 | **Branch:** fix/terraform-azure → main | **+46/-34** | **Files:** 4

> # Description
> 
> Update the terraform config for Azure:
> - stop overriding container's `commands` (the default config URL was wrong);
> - propagate `environment_variables` and set ``ENABLE_PRIMITIVE: false``.
> 
> Fixes # (issue)
> Now terraform deployment for Azure can be launched right away without...

<details><summary>Files changed (4)</summary>

- `terraform/azure/README.md` (+3/-2)
- `terraform/azure/bomblet/variables.tf` (+1/-1)
- `terraform/azure/main.tf` (+36/-30)
- `terraform/azure/variables.tf` (+6/-1)
</details>

## #430 Руський - це український. Варто про це пам'ятати.
**State:** MERGED | **Author:** @andriibulbuk | **Date:** 2022-03-25 | **Branch:** patch-1 → main | **+1/-1** | **Files:** 1

> Ру́ський (прикметник) (давньоруськ. руськии, пол. ruski) — в українській мові такий, що відноситься до часів Русі або до її населення — русічи їхніх нащадків — українців. Слово руський не слід плутати з рос. русский, тобто росіянин.

<details><summary>Comments (3)</summary>

- **@SLDay** (2022-03-25): Але перекладачі кажуть що правильно **російський корабель**
- **@andriibulbuk** (2022-03-25): > Але перекладачі кажуть що правильно **російський корабель**  Звичайно, проте відомий вислів військових на острові Зміїному був озвучений російською.   Транслітерація українською тут доречна
- **@andser** (2022-03-26): Також треба памʼятати що руська мова не належить росіянам і називати її російською - невірно. Називати мешканців росії - руськими теж невірно, бо вони - росіяни. І останнє: росіяни не винайшли...
</details>

<details><summary>Files changed (1)</summary>

- `src/runner/runner.go` (+1/-1)
</details>

## #429 Update StartDB1000N.bat
**State:** MERGED | **Author:** @SLDay | **Date:** 2022-03-25 | **Branch:** main → main | **+1/-1** | **Files:** 1

> Update script with new release underscore naming
> 
> # Description
> 
> Updated the script with new (underscore) naming of releases.
> 
> Fixes 1 (issue)
> 
> ## Type of change
> 
> Please delete options that are not relevant.
> 
> - Bug fix (non-breaking change which fixes an issue)
> 
> ## How Has This Been...

<details><summary>Files changed (1)</summary>

- `scripts/StartDB1000N.bat` (+1/-1)
</details>

## #428 Get rid of advanced Docker image and change cloud deployments to use ENABLE_PRIMITIVE=false
**State:** MERGED | **Author:** @Amet13 | **Date:** 2022-03-25 | **Branch:** main → main | **+31/-24** | **Files:** 12

> # Description
> 
> - Fix kubeval bug with linting all yamls in repo
> - Cleanup all mentions for advanced image from repo
> - Optimize k8s and terraform deployments to use `ENABLE_PRIMITIVE=false`
> 
> Fixes #421
> 
> ## Type of change
> 
> Please delete options that are not relevant.
> 
> - [x] Bug fix...

<details><summary>Files changed (12)</summary>

- `.github/workflows/kubernetes-lint.yaml` (+2/-0)
- `ansible/linux/setup.yaml` (+4/-4)
- `docker-compose.yml` (+3/-3)
- `docs/advanced-docs/advanced-and-devs.md` (+0/-7)
- `docs/faq.md` (+0/-1)
- `docs/faq.uk.md` (+0/-2)
- `kubernetes/helm-charts/templates/deployment.yaml` (+5/-0)
- `kubernetes/helm-charts/values.yaml` (+5/-1)
- `kubernetes/manifests/daemonset.yaml` (+4/-1)
- `kubernetes/manifests/deployment.yaml` (+4/-1)
- `terraform/aws/main.tf` (+2/-2)
- `terraform/gcp_expressvpn/main.tf` (+2/-2)
</details>

## #426 Merge updater into the config package
**State:** MERGED | **Author:** @jdoe7865623 | **Date:** 2022-03-25 | **Branch:** config → main | **+60/-65** | **Files:** 6

<details><summary>Files changed (6)</summary>

- `go.mod` (+1/-1)
- `go.sum` (+2/-2)
- `main.go` (+3/-3)
- `src/runner/config/config.go` (+2/-1)
- `src/runner/config/updater.go` (+52/-0)
- `src/utils/updater/updater.go` (+0/-58)
</details>

## #425 Docker image build on CI & Issue template
**State:** MERGED | **Author:** @Amet13 | **Date:** 2022-03-25 | **Branch:** main → main | **+19/-0** | **Files:** 2

> # Description
> 
> - Issue template added
> - Docker build command added to pipeline to ensure that image is buildable without manual verification
> 
> ## Type of change
> 
> - [x] New feature (non-breaking change which adds functionality)
> - [x] Documentation update
> 
> ## How Has This Been Tested?
> 
> See...

<details><summary>Files changed (2)</summary>

- `.github/issue_template.md` (+17/-0)
- `.github/workflows/docker-lint.yaml` (+2/-0)
</details>

## #418 Enable gomoddirectives and make it happy
**State:** MERGED | **Author:** @jdoe7865623 | **Date:** 2022-03-25 | **Branch:** gomoddirectives → main | **+3/-5** | **Files:** 3

<details><summary>Files changed (3)</summary>

- `.golangci.yml` (+1/-1)
- `go.mod` (+0/-2)
- `go.sum` (+2/-2)
</details>

## #417 Enable funlen and finally make it happy
**State:** MERGED | **Author:** @jdoe7865623 | **Date:** 2022-03-25 | **Branch:** funlen2 → main | **+72/-68** | **Files:** 6

<details><summary>Files changed (6)</summary>

- `.golangci.yml` (+19/-19)
- `main.go` (+6/-31)
- `src/jobs/base.go` (+0/-3)
- `src/runner/runner.go` (+8/-4)
- `src/utils/metrics/prometheus.go` (+30/-11)
- `src/utils/updater/updater.go` (+9/-0)
</details>

## #414 Dockerfile: linter and optimizations
**State:** MERGED | **Author:** @Amet13 | **Date:** 2022-03-25 | **Branch:** main → main | **+31/-4** | **Files:** 3

> # Description
> 
> - Added missed mkdocs doc for Hetzner Cloud
> - Use hadolint for linting `Dockerfile`
>   - Update alpine basic image to the latest version: https://hub.docker.com/_/alpine
>   - Pin package version for `curl`
>   - Install packages without caching it
>   - Remove deprecated `rm -rf`...

<details><summary>Files changed (3)</summary>

- `.github/workflows/docker-lint.yaml` (+21/-0)
- `Dockerfile` (+4/-4)
- `docs/advanced-docs/terraform/hetzner-cloud.md` (+6/-0)
</details>

## #411 Terraform and k8s linters
**State:** MERGED | **Author:** @Amet13 | **Date:** 2022-03-24 | **Branch:** main → main | **+54/-13** | **Files:** 9

> # Description
> 
> Adding linters for terraform validate/fmt commands and for k8s plain manifests linter checks.
> 
> ## Type of change
> 
> - [x] New feature (non-breaking change which adds functionality)
> 
> ## How Has This Been Tested?
> 
> See results in CI

<details><summary>Files changed (9)</summary>

- `.github/workflows/kubernetes-lint.yaml` (+17/-0)
- `.github/workflows/markdownlint.yaml` (+1/-1)
- `.github/workflows/terraformci.yaml` (+24/-0)
- `terraform/azure/bomblet/main.tf` (+1/-1)
- `terraform/azure/bomblet/variables.tf` (+2/-2)
- `terraform/azure/variables.tf` (+1/-1)
- `terraform/hetzner_cloud/provider.tf` (+1/-1)
- `terraform/hetzner_cloud/terraform.tfvars` (+2/-2)
- `terraform/hetzner_cloud/variables.tf` (+5/-5)
</details>

## #407 Hetzner Cloud support
**State:** MERGED | **Author:** @Amet13 | **Date:** 2022-03-24 | **Branch:** cloud_updates → main | **+128/-9** | **Files:** 11

> # Description
> 
> - Support for Hetzner Cloud added
> - Heroku cloud tested and updated app version
> - Small fixes
> 
> ## Type of change
> 
> - [x] New feature (non-breaking change which adds functionality)
> - [x] Documentation update
> 
> ## How Has This Been Tested?
> 
> Heroku terraform output:
> 
> ```
> $...

<details><summary>Files changed (11)</summary>

- `.github/CODEOWNERS` (+0/-3)
- `.gitignore` (+0/-1)
- `terraform/digital_ocean/README.md` (+2/-2)
- `terraform/heroku/README.md` (+2/-2)
- `terraform/heroku/terraform.tfvars` (+1/-1)
- `terraform/hetzner_cloud/README.md` (+29/-0)
- `terraform/hetzner_cloud/main.tf` (+19/-0)
- `terraform/hetzner_cloud/provider.tf` (+13/-0)
- `terraform/hetzner_cloud/terraform.tfvars` (+3/-0)
- `terraform/hetzner_cloud/user_data.yml` (+29/-0)
- `terraform/hetzner_cloud/variables.tf` (+30/-0)
</details>

## #406 [DRAFT] Add load balanced tor proxy to AWS terraform config
**State:** MERGED | **Author:** @SemiConscious | **Date:** 2022-03-25 | **Branch:** add-aws-tor-proxy → main | **+314/-19** | **Files:** 4

> # Description
> 
> This is more a basis for discussion than a serious proposal to merge. I'm happy to take suggestions, I am not a tor expert so there may be much that can be improved, eg using some other existing tor proxy setup, or not using one at all. 
> 
> The goal is to obfuscate the origin IPs...

<details><summary>Comments (10)</summary>

- **@arriven** (2022-03-24): Looks pretty good to me, someone recently told me that they had issues with tor proxy, can you confirm that it works for you? I was going to start looking into possible causes tomorrow but knowing...
- **@SemiConscious** (2022-03-24): @Arriven thanks for the prompt reply. Tor seems to be working well for me both locally and in AWS. The NLB would only get recreated when something significant changes like changing the number of...
- **@SemiConscious** (2022-03-24): @Arriven - kudos for a bloody amazing tool by the way :-D
- **@arriven** (2022-03-24): I'll try to find where that issue was mentioned  As for disrupting current workflows for people: there's always an option to have both old and new config in two different folders although I'd prefer...
- **@SemiConscious** (2022-03-24): > I'd prefer having some switches to enable/disable tor NLB within a single terraform deployment  I did think about that. Leave it with me
- **@SemiConscious** (2022-03-25): I have checked in a module-ised version of the tor proxy, and I have set the defaults to no-proxy.  Incidentally - I am seeing errors in my tor proxy I didn't see yesterday:   > Mar 25 12:46:05...
- **@jdoe7865623** (2022-03-27): @SemiConscious I've done some testing with tor as well (except I've build the tor service directly into the docker image). Unfortunately, I observe a significant reduction in the number of accepted...
- **@SemiConscious** (2022-03-27): I agree - it's not a complete solution, and it was particularly bad on Friday - I have 5 proxy instances which were running at 100% CPU capacity and a very poor network throughput. *It seems VERY...
- **@SemiConscious** (2022-03-27): By the way - I did consider putting Tor into the db1000n container. It would work great for those not running in the cloud. But for the cloud, I felt that it was likely that the resource needs of the...
- **@SemiConscious** (2022-03-28): @Arriven @jdoe7865623 I have tried a lot of different things today. My main aim was to develop an openvpn solution to replace tor, which I have checked in, though it looks as if I'll need a new pull...
</details>

<details><summary>Files changed (4)</summary>

- `terraform/aws/ireland.tfvars` (+2/-1)
- `terraform/aws/main.tf` (+73/-18)
- `terraform/aws/tor-proxy/tor-proxy.tf` (+202/-0)
- `terraform/aws/variables.tf` (+37/-0)
</details>

## #405 Make funlen even happier
**State:** MERGED | **Author:** @jdoe7865623 | **Date:** 2022-03-24 | **Branch:** funlen → main | **+262/-277** | **Files:** 18

<details><summary>Files changed (18)</summary>

- `main.go` (+16/-129)
- `src/core/dnsblast/dns-blast.go` (+21/-30)
- `src/jobs/base.go` (+26/-11)
- `src/jobs/complex.go` (+2/-2)
- `src/jobs/dnsblast.go` (+1/-1)
- `src/jobs/http.go` (+3/-5)
- `src/jobs/packetgen.go` (+14/-30)
- `src/jobs/rawnet.go` (+2/-2)
- `src/jobs/slowloris.go` (+1/-1)
- `src/jobs/utils.go` (+11/-5)
- `src/runner/runner.go` (+40/-27)
- `src/utils/countrychecker.go` (+28/-1)
- `src/utils/ota/ota.go` (+93/-20)
- `src/utils/ota/restart.go` (+1/-1)
- `src/utils/ota/restart_darwin.go` (+1/-1)
- `src/utils/ota/restart_linux.go` (+1/-1)
- `src/utils/ota/restart_windows.go` (+1/-2)
- `src/utils/ota/version.go` (+0/-8)
</details>

## #404 Make funlen a little happier
**State:** MERGED | **Author:** @jdoe7865623 | **Date:** 2022-03-24 | **Branch:** funlen → main | **+100/-119** | **Files:** 9

<details><summary>Files changed (9)</summary>

- `src/core/dnsblast/qry/types.go` (+1/-1)
- `src/jobs/complex.go` (+0/-3)
- `src/jobs/dnsblast.go` (+41/-48)
- `src/jobs/http.go` (+56/-59)
- `src/jobs/packetgen.go` (+0/-1)
- `src/jobs/rawnet.go` (+0/-4)
- `src/jobs/slowloris.go` (+0/-1)
- `src/jobs/utils.go` (+0/-2)
- `src/runner/runner.go` (+2/-0)
</details>

## #403 terraform: Added arm support for aws
**State:** MERGED | **Author:** @alexdanger | **Date:** 2022-03-24 | **Branch:** main → main | **+9/-2** | **Files:** 2

> # Description
> 
> Added arm instance type and ami for the aws terraform configuration.
> arm instance is more performant and cheaper than regular non graviton instances.
> 
> Fixes # (issue)
> 
> ## Type of change
> 
> Please delete options that are not relevant.
> 
> - [ ] Bug fix (non-breaking change which...

<details><summary>Files changed (2)</summary>

- `terraform/aws/main.tf` (+1/-1)
- `terraform/aws/variables.tf` (+8/-1)
</details>

## #400 allow sending http flood to static host
**State:** MERGED | **Author:** @arriven | **Date:** 2022-03-23 | **Branch:** http-flood-to-static-host → main | **+45/-9** | **Files:** 3

> # Description
> 
> Allow sending http traffic to a predefined host different from a url one to prevent dns re-targeting
> 
> ## Type of change
> 
> Please delete options that are not relevant.
> 
> - [ ] New feature (non-breaking change which adds functionality)
> 
> ## How Has This Been Tested?
> 
> Please...

<details><summary>Files changed (3)</summary>

- `config/examples/http-host.yaml` (+9/-0)
- `src/core/http/http.go` (+35/-8)
- `src/jobs/http.go` (+1/-1)
</details>

## #398 Added few cases for serialization_test
**State:** MERGED | **Author:** @alexdanger | **Date:** 2022-03-22 | **Branch:** main → main | **+99/-40** | **Files:** 1

> # Description
> 
> Added test for `serialiation_test.go`, included check payload for ipv4/ipv6 packets and different payload string and int.
> 
> 
> 
> test cases
> 
> @Arriven just a question, is this ok to use some package for test like assert to avoid linter issues with cyclomatic complexity. I believe...

<details><summary>Comments (1)</summary>

- **@arriven** (2022-03-22): @alexdanger I don't have objections against testing frameworks - feel free to include them as long as they are maintained
</details>

<details><summary>Files changed (1)</summary>

- `src/core/packetgen/serialization_test.go` (+99/-40)
</details>

## #397 Update command line description
**State:** MERGED | **Author:** @bitshape | **Date:** 2022-03-23 | **Branch:** bitshape-primitive-jobs → main | **+4/-0** | **Files:** 1

> # Description
> 
> I think what you want to say is "primitive jobs are less resource intensive" or "more resource-efficient". The latter sounds wrong, so I'm going with the first one.
> 
> ## Type of change
> 
> - [x] Documentation update

<details><summary>Comments (4)</summary>

- **@arriven** (2022-03-22): The wording is correct there - most primitive jobs (layer 3-4 OSI) rely on being able to generate large amounts of traffic in order to be effective as their main goal is to flood the communication...
- **@arriven** (2022-03-22): Something like "primitive jobs rely on generating as much raw traffic as possible and may exhaust your system. They are also easier to detect and unadvisable to be used in clouds"
- **@bitshape** (2022-03-22): @Arriven 97c4f3dcbc17d3d9804661a69866d436bad41837
- **@arriven** (2022-03-22): Markdown linter detected trailing spaces in the file
</details>

<details><summary>Files changed (1)</summary>

- `docs/faq.md` (+4/-0)
</details>

## #395 Improve traffic tracking
**State:** MERGED | **Author:** @arriven | **Date:** 2022-03-22 | **Branch:** improve-traffic-tracking → main | **+31/-7** | **Files:** 4

> # Description
> 
> Track common protocol header sizes in rawnet jobs for better visibility (it's approximate but better than nothing)
> 
> Fix #12 
> 
> ## Type of change
> 
> Please delete options that are not relevant.
> 
> - [ ] Bug fix (non-breaking change which fixes an issue)
> 
> ## How Has This Been...

<details><summary>Files changed (4)</summary>

- `src/core/http/http.go` (+4/-5)
- `src/core/packetgen/packetgen.go` (+7/-0)
- `src/jobs/rawnet.go` (+13/-2)
- `src/utils/metrics/metrics.go` (+7/-0)
</details>

## #393 Enable gocyclo, lll, maintidx, and make them happy
**State:** MERGED | **Author:** @jdoe7865623 | **Date:** 2022-03-22 | **Branch:** linters → main | **+55/-35** | **Files:** 6

<details><summary>Files changed (6)</summary>

- `.golangci.yml` (+12/-15)
- `main.go` (+30/-14)
- `src/core/dnsblast/qry/types.go` (+3/-3)
- `src/core/slowloris/slowloris.go` (+6/-2)
- `src/runner/config/defaultconfig.go` (+1/-0)
- `src/utils/metrics/prometheus.go` (+3/-1)
</details>

## #391 DB1000N | Add support for the restart option after the auto-update for the Windows OS
**State:** MERGED | **Author:** @sivillakonski | **Date:** 2022-03-23 | **Branch:** main → main | **+75/-25** | **Files:** 6

> ## Restart the needle once the auto-update has finished on the Windows OS
> (Codename: `Glory to Those who protect the Land`)
> 
> This patch brings the restart the option for the DB1000N on the OS with non-boring wallpapers.
> 
> Take care and stay safe, folks!
> 
> ### References
> 1....

<details><summary>Comments (1)</summary>

- **@sivillakonski** (2022-03-23): @Arriven, what a sharp eye! I bet it was a last second change ![Screenshot 2022-03-22 at 22 26...
</details>

<details><summary>Files changed (6)</summary>

- `main.go` (+4/-1)
- `src/utils/ota/ota.go` (+0/-17)
- `src/utils/ota/restart.go` (+7/-4)
- `src/utils/ota/restart_windows.go` (+46/-0)
- `src/utils/ota/shared.go` (+18/-0)
- `src/utils/ota/shared_test.go` (+0/-3)
</details>

## #388 Avoid app crash with -prometheus_on=false
**State:** MERGED | **Author:** @neatdecisions | **Date:** 2022-03-21 | **Branch:** fix/prometheus_off → main | **+30/-0** | **Files:** 1

> # Description
> 
> Prometheus counters are created only upon the call to ``InitMetrics`` (e.g. with ``prometheus_on=true``), but are still accessed always. This leads to the app crash with ``prometheus_on=false``.
> 
> Fix: add nil-checks before incrementing the counters.
> 
> ## Type of change
> 
> - [x]...

<details><summary>Files changed (1)</summary>

- `src/utils/metrics/prometheus.go` (+30/-0)
</details>

## #385 added socks5 proxies support to slowloris
**State:** MERGED | **Author:** @arriven | **Date:** 2022-03-21 | **Branch:** socks5-proxy-slowloris → main | **+17/-6** | **Files:** 3

> # Description
> 
> Added socks5 support to slowloris
> 
> WIP #279 
> 
> ## Type of change
> 
> Please delete options that are not relevant.
> 
> - [ ] New feature (non-breaking change which adds functionality)
> 
> ## How Has This Been Tested?
> 
> Please describe the tests that you ran to verify your changes....

<details><summary>Files changed (3)</summary>

- `go.mod` (+0/-1)
- `src/core/slowloris/slowloris.go` (+6/-4)
- `src/jobs/slowloris.go` (+11/-1)
</details>

## #384 allow using socks5 proxy in tcp jobs
**State:** MERGED | **Author:** @arriven | **Date:** 2022-03-21 | **Branch:** socks5-proxy → main | **+94/-61** | **Files:** 5

> # Description
> 
> Allow using socks5 proxy in tcp jobs. Inspired by #381
> 
> WIP #279 
> 
> ## Type of change
> 
> Please delete options that are not relevant.
> 
> - [ ] New feature (non-breaking change which adds functionality)
> 
> ## How Has This Been Tested?
> 
> Please describe the tests that you ran to...

<details><summary>Files changed (5)</summary>

- `src/core/http/http.go` (+11/-38)
- `src/jobs/http.go` (+2/-2)
- `src/jobs/rawnet.go` (+31/-21)
- `src/utils/proxy.go` (+34/-0)
- `src/utils/utils.go` (+16/-0)
</details>

## #383 Template functions
**State:** MERGED | **Author:** @arriven | **Date:** 2022-03-21 | **Branch:** template-functions → main | **+128/-31** | **Files:** 6

> # Description
> 
> copied json and yaml templates from helm. Also changed default config format to yaml as yaml is a superset of json and any valid json is also a valid yaml
> 
> ## Type of change
> 
> Please delete options that are not relevant.
> 
> - [ ] New feature (non-breaking change which adds...

<details><summary>Files changed (6)</summary>

- `main.go` (+1/-1)
- `src/utils/templates/encoding.go` (+107/-0)
- `src/utils/templates/network.go` (+10/-0)
- `src/utils/templates/templates.go` (+8/-23)
- `src/utils/utils.go` (+1/-6)
- `testconfig.yaml` (+1/-1)
</details>

## #381 Added proxy URL validation and socks5 support for rawnet job type (#279)
**State:** CLOSED | **Author:** @lollypot | **Date:** 2022-03-21 | **Branch:** main → main | **+52/-7** | **Files:** 4

> See description of CR here #279
> 
> It's still not work for udp type jobs
> "msg":"error running job","error":"socks connect udp 172.17.0.1:9150->1.2.3.4:53: network not implemented"
> because socks5 library is not support udp for now. But I am decided to leave it as is because when you will run it...

<details><summary>Comments (4)</summary>

- **@arriven** (2022-03-20): Btw, would it be ok to you to add this proxy to slowloris as well? Can be a separate PR
- **@arriven** (2022-03-20): And one more thing - can we also expose proxy settings to the job config so that it's similar to how it's done in http jobs?
- **@arriven** (2022-03-21): @lollypot hope you don't mind me reimplementing this with my comments in #384
- **@lollypot** (2022-03-21): @Arriven Yes. Thank you very much - you will do it better. of course :). Sorry that I not respond in shorter time. But I have one comment:...
</details>

<details><summary>Files changed (4)</summary>

- `main.go` (+7/-0)
- `src/jobs/rawnet.go` (+10/-7)
- `src/jobs/utils.go` (+20/-0)
- `src/utils/utils.go` (+15/-0)
</details>

## #380 Enable cyclop and make it happy
**State:** MERGED | **Author:** @jdoe7865623 | **Date:** 2022-03-21 | **Branch:** cyclop → main | **+222/-124** | **Files:** 10

<details><summary>Files changed (10)</summary>

- `.golangci.yml` (+1/-1)
- `main.go` (+72/-57)
- `src/core/dnsblast/qry/types.go` (+1/-0)
- `src/core/dnsblast/qry/types_test.go` (+91/-0)
- `src/jobs/base.go` (+1/-0)
- `src/jobs/packetgen.go` (+1/-1)
- `src/jobs/rawnet.go` (+1/-1)
- `src/jobs/utils.go` (+3/-3)
- `src/utils/countrychecker.go` (+50/-60)
- `src/utils/utils.go` (+1/-1)
</details>

## #378 Proxylist refactoring
**State:** MERGED | **Author:** @arriven | **Date:** 2022-03-20 | **Branch:** proxylist-refactoring → main | **+50/-93** | **Files:** 5

> # Description
> 
> Some proxylist cleanup
> 
> ## Type of change
> 
> Please delete options that are not relevant.
> 
> - [ ] Bug fix (non-breaking change which fixes an issue)
> 
> ## How Has This Been Tested?
> 
> Please describe the tests that you ran to verify your changes. Provide instructions so we can...

<details><summary>Comments (3)</summary>

- **@arriven** (2022-03-20): This is still WIP
- **@Mancersoft** (2022-03-20): @Arriven One more thing, the app is supporting only SOCK5 now, correct? Is there a reason why not use other types of proxies (HTTP, HTTPS, SOCK4)? Or it just not implemented yet?
- **@arriven** (2022-03-20): @Staskkk My tests seem to indicate that socks5 package supports http/https/socks4 proxies similar to how ipv6 connection supports communication over ipv4 in packetgen
</details>

<details><summary>Files changed (5)</summary>

- `main.go` (+2/-8)
- `src/jobs/base.go` (+1/-1)
- `src/jobs/http.go` (+4/-4)
- `src/utils/templates/templates.go` (+33/-78)
- `testconfig.yaml` (+10/-2)
</details>

## #375 docker pull always added
**State:** MERGED | **Author:** @ichornyi | **Date:** 2022-03-19 | **Branch:** docker-pull → main | **+3/-3** | **Files:** 2

> # Description
> 
> added Docker flag --pull=always in order to automatically fetch new builds
> 
> ## Type of change
> 
> - [x] New feature (non-breaking change which adds functionality)
> 
> ## How Has This Been Tested?
> 
> - [x] Redeploy application
> - [x] Check logs
> 
> ## Test Configuration
> 
> - Release...

<details><summary>Files changed (2)</summary>

- `ansible/linux/setup.yaml` (+2/-2)
- `terraform/gcp_expressvpn/main.tf` (+1/-1)
</details>

## #374 feat: add dns config
**State:** MERGED | **Author:** @alexdanger | **Date:** 2022-03-19 | **Branch:** add-dns-config → main | **+23/-0** | **Files:** 1

> # Description
> 
> Added dns package building 
> Fixes # (issue) https://github.com/Arriven/db1000n/issues/49
> 
> ## Type of change
> 
> Please delete options that are not relevant.
> 
> - [ ] Bug fix (non-breaking change which fixes an issue)
> - [x] New feature (non-breaking change which adds...

<details><summary>Comments (4)</summary>

- **@alexdanger** (2022-03-19): @Arriven could you please check is there right start?
- **@arriven** (2022-03-19): @alexdanger looks good but you need to fix the linter You can also add automatic check for correct serialization/deserialization similar to the one being present in serialize_test.go but that's...
- **@alexdanger** (2022-03-19): > @alexdanger looks good but you need to fix the linter You can also add automatic check for correct serialization/deserialization similar to the one being present in serialize_test.go but that's...
- **@alexdanger** (2022-03-19): sorry, somehow golang-lint didn't catch .golangci.yml, linter is fixed.
</details>

<details><summary>Files changed (1)</summary>

- `src/core/packetgen/payload.go` (+23/-0)
</details>

## #373 Use filters instead of separate advanced config
**State:** MERGED | **Author:** @arriven | **Date:** 2022-03-19 | **Branch:** advanced-techniques-filter → main | **+21/-15** | **Files:** 5

> # Description
> 
> Use job filters instead of separate advanced config
> 
> Fixes #341 
> 
> ## Type of change
> 
> Please delete options that are not relevant.
> 
> - [ ] New feature (non-breaking change which adds functionality)
> 
> ## How Has This Been Tested?
> 
> Please describe the tests that you ran to...

<details><summary>Files changed (5)</summary>

- `Dockerfile` (+1/-1)
- `main.go` (+7/-5)
- `src/jobs/base.go` (+6/-5)
- `src/runner/runner.go` (+4/-3)
- `testconfig.json` (+3/-1)
</details>

## #372 Packetgen ipv6
**State:** MERGED | **Author:** @arriven | **Date:** 2022-03-18 | **Branch:** packetgen-ipv6 → main | **+163/-103** | **Files:** 10

> # Description
> 
> Add ipv6 support to packetgen
> 
> Fixes #371 
> 
> ## Type of change
> 
> Please delete options that are not relevant.
> 
> - [ ] New feature (non-breaking change which adds functionality)
> 
> ## How Has This Been Tested?
> 
> Please describe the tests that you ran to verify your changes....

<details><summary>Files changed (10)</summary>

- `config/examples/advanced/packetgen-ipv6.yaml` (+23/-0)
- `src/core/packetgen/application.go` (+0/-28)
- `src/core/packetgen/connection.go` (+2/-12)
- `src/core/packetgen/network.go` (+37/-7)
- `src/core/packetgen/packetgen.go` (+13/-34)
- `src/core/packetgen/payload.go` (+50/-0)
- `src/core/packetgen/serialization_test.go` (+5/-5)
- `src/jobs/packetgen.go` (+3/-9)
- `src/utils/templates/network.go` (+24/-6)
- `src/utils/templates/templates.go` (+6/-2)
</details>

## #370 Add icmpv4 layer support
**State:** MERGED | **Author:** @arriven | **Date:** 2022-03-18 | **Branch:** packetgen-icmpv4 → main | **+61/-39** | **Files:** 4

> # Description
> 
> Added icmpv4 support to packetgen
> 
> ## Type of change
> 
> Please delete options that are not relevant.
> 
> - [ ] New feature (non-breaking change which adds functionality)
> 
> ## How Has This Been Tested?
> 
> Please describe the tests that you ran to verify your changes. Provide...

<details><summary>Files changed (4)</summary>

- `src/core/packetgen/application.go` (+0/-28)
- `src/core/packetgen/packetgen.go` (+10/-10)
- `src/core/packetgen/payload.go` (+50/-0)
- `src/core/packetgen/serialization_test.go` (+1/-1)
</details>

## #368 Packetgen tests
**State:** MERGED | **Author:** @arriven | **Date:** 2022-03-18 | **Branch:** packetgen-tests → main | **+88/-38** | **Files:** 5

> # Description
> 
> Some automated testing for packetgen
> 
> ## Type of change
> 
> Please delete options that are not relevant.
> 
> - [ ] Bug fix (non-breaking change which fixes an issue)
> 
> ## How Has This Been Tested?
> 
> Please describe the tests that you ran to verify your changes. Provide...

<details><summary>Files changed (5)</summary>

- `config/examples/advanced/packetgen.yaml` (+0/-5)
- `src/core/packetgen/serialization.go` (+4/-0)
- `src/core/packetgen/serialization_test.go` (+76/-0)
- `src/utils/templates/network.go` (+1/-24)
- `src/utils/templates/templates.go` (+7/-9)
</details>

## #367 refactor packetgen (WIP)
**State:** MERGED | **Author:** @arriven | **Date:** 2022-03-18 | **Branch:** packetgen-v2 → main | **+400/-218** | **Files:** 10

> # Description
> 
> Previous packetgen implementation was quite hard to extend with new protocols. This one should be a lot more modular. This refactoring breaks previous packetgen configs but we don't use it in the current default config yet so I'm making a decision to cut not support it
> 
> Useful...

<details><summary>Files changed (10)</summary>

- `config/examples/advanced/packetgen.yaml` (+28/-0)
- `src/core/packetgen/application.go` (+28/-0)
- `src/core/packetgen/connection.go` (+34/-0)
- `src/core/packetgen/link.go` (+44/-0)
- `src/core/packetgen/network.go` (+45/-0)
- `src/core/packetgen/packetgen.go` (+40/-163)
- `src/core/packetgen/serialization.go` (+45/-0)
- `src/core/packetgen/transport.go` (+101/-0)
- `src/jobs/packetgen.go` (+34/-54)
- `src/utils/utils.go` (+1/-1)
</details>

## #366 Return country name from CheckCountry and send to Prometheus
**State:** MERGED | **Author:** @bitshape | **Date:** 2022-03-18 | **Branch:** metrics-change → main | **+97/-74** | **Files:** 8

> # Description
> 
> - Pass ClientID as const label for Prometheus
> - Return country name from CheckCountry function
> - Add country name to Prometheus metrics
> 
> This is useful if you're using Prometheus / Grafana to monitor overall performance.
> 
> ## Type of change
> 
> - [x] New feature (non-breaking...

<details><summary>Files changed (8)</summary>

- `main.go` (+11/-2)
- `src/core/dnsblast/dns-blast.go` (+6/-6)
- `src/core/slowloris/slowloris.go` (+10/-10)
- `src/jobs/http.go` (+5/-5)
- `src/jobs/rawnet.go` (+10/-10)
- `src/runner/runner.go` (+1/-1)
- `src/utils/countrychecker.go` (+6/-6)
- `src/utils/metrics/prometheus.go` (+48/-34)
</details>

## #364 Return country name from CheckCountry and send to Prometheus
**State:** CLOSED | **Author:** @bitshape | **Date:** 2022-03-17 | **Branch:** metrics-change → main | **+83/-65** | **Files:** 8

> # Description
> 
> - Pass ClientID as const label for Prometheus
> - Return country name from CheckCountry function
> - Add country name to Prometheus metrics
> 
> This is useful if you're using Prometheus / Grafana to monitor overall performance.
> 
> ## Type of change
> 
> - [x] New feature (non-breaking...

<details><summary>Files changed (8)</summary>

- `main.go` (+7/-2)
- `src/core/dnsblast/dns-blast.go` (+6/-6)
- `src/core/slowloris/slowloris.go` (+8/-8)
- `src/jobs/http.go` (+2/-2)
- `src/jobs/rawnet.go` (+6/-6)
- `src/runner/runner.go` (+1/-1)
- `src/utils/countrychecker.go` (+6/-6)
- `src/utils/metrics/prometheus.go` (+47/-34)
</details>

## #359 add client id to prom metrics for distincion
**State:** MERGED | **Author:** @arriven | **Date:** 2022-03-16 | **Branch:** prom-metrics-id → main | **+71/-50** | **Files:** 11

> # Description
> 
> Added client id to prom metrics because push gateways seem to not accumulate values from different clients
> 
> ## Type of change
> 
> Please delete options that are not relevant.
> 
> - [ ] Bug fix (non-breaking change which fixes an issue)
> 
> ## How Has This Been Tested?
> 
> Please...

<details><summary>Files changed (11)</summary>

- `main.go` (+8/-1)
- `src/core/dnsblast/dns-blast.go` (+11/-10)
- `src/core/slowloris/slowloris.go` (+11/-10)
- `src/jobs/base.go` (+1/-0)
- `src/jobs/dnsblast.go` (+1/-0)
- `src/jobs/http.go` (+5/-5)
- `src/jobs/packetgen.go` (+4/-2)
- `src/jobs/rawnet.go` (+10/-10)
- `src/jobs/slowloris.go` (+2/-0)
- `src/runner/runner.go` (+1/-1)
- `src/utils/metrics/prometheus.go` (+17/-11)
</details>

## #358 create empty cert pool if system one is unavailabe
**State:** MERGED | **Author:** @arriven | **Date:** 2022-03-16 | **Branch:** cert-pool-windows → main | **+1/-2** | **Files:** 1

> # Description
> 
> use empty cert pool in prom if system one is unavailable (like on windows)
> 
> ## Type of change
> 
> Please delete options that are not relevant.
> 
> - [ ] Bug fix (non-breaking change which fixes an issue)
> 
> ## How Has This Been Tested?
> 
> Please describe the tests that you ran to...

<details><summary>Files changed (1)</summary>

- `src/utils/metrics/prometheus.go` (+1/-2)
</details>

## #357 Improve prom metrics
**State:** MERGED | **Author:** @arriven | **Date:** 2022-03-16 | **Branch:** improve-prom-metrics → main | **+23/-5** | **Files:** 2

> # Description
> 
> Add client count metric and add prefix to app specific metrics for ease of use
> 
> ## Type of change
> 
> Please delete options that are not relevant.
> 
> - [ ] New feature (non-breaking change which adds functionality)
> 
> ## How Has This Been Tested?
> 
> Please describe the tests that...

<details><summary>Files changed (2)</summary>

- `src/runner/runner.go` (+2/-0)
- `src/utils/metrics/prometheus.go` (+21/-5)
</details>

## #356 Zap logging
**State:** MERGED | **Author:** @arriven | **Date:** 2022-03-16 | **Branch:** zap-logging → main | **+200/-205** | **Files:** 18

> # Description
> 
> use zap for non user facing logs to have better context management
> 
> Fixes #353 
> 
> ## Type of change
> 
> Please delete options that are not relevant.
> 
> - [ ] New feature (non-breaking change which adds functionality)
> 
> ## How Has This Been Tested?
> 
> Please describe the tests...

<details><summary>Files changed (18)</summary>

- `go.mod` (+3/-1)
- `go.sum` (+13/-0)
- `main.go` (+15/-1)
- `src/core/dnsblast/dns-blast.go` (+29/-24)
- `src/core/dnsblast/dns-blast_test.go` (+3/-1)
- `src/core/http/http.go` (+6/-8)
- `src/core/slowloris/slowloris.go` (+20/-19)
- `src/jobs/base.go` (+3/-1)
- `src/jobs/complex.go` (+9/-11)
- `src/jobs/dnsblast.go` (+5/-3)
- `src/jobs/http.go` (+20/-37)
- `src/jobs/packetgen.go` (+13/-27)
- `src/jobs/rawnet.go` (+17/-23)
- `src/jobs/slowloris.go` (+6/-7)
- `src/jobs/utils.go` (+13/-19)
- `src/runner/runner.go` (+10/-9)
- `src/utils/templates/templates.go` (+12/-12)
- `src/utils/utils.go` (+3/-2)
</details>

## #355 human-readable client-side network stats logging
**State:** MERGED | **Author:** @dshpet | **Date:** 2022-03-16 | **Branch:** improve_network_client_side_stats_logging → main | **+22/-7** | **Files:** 1

> # Description
> 
> Make network logging more human-readable and understandable.
> 
> - Add tabbed alignment;
> - Use Megabytes and Percent as metric
> - Visually indent stats message.
> 
> ## Type of change
> 
> Minor visual quality-of-life improvement for end-user
> 
> ## How Has This Been Tested?
> 
> Tested...

<details><summary>Comments (2)</summary>

- **@arriven** (2022-03-16): @dshpet lint is failing for your PR
- **@dshpet** (2022-03-16): Fixed linter errors. Improved formatting even further.
</details>

<details><summary>Files changed (1)</summary>

- `src/runner/runner.go` (+22/-7)
</details>

## #354 only allow one thread to decrypt data at a time
**State:** MERGED | **Author:** @arriven | **Date:** 2022-03-15 | **Branch:** avoid-parallel-decryption → main | **+8/-0** | **Files:** 1

> # Description
> 
> decryption takes a bunch of RAM to generate scrypt identity. we don't do decryption in hot paths so it's better to only allow one thread doing decryption at a time to avoid OOM
> 
> Fixes #347 
> 
> ## Type of change
> 
> Please delete options that are not relevant.
> 
> - [ ] Bug fix...

<details><summary>Files changed (1)</summary>

- `src/utils/crypto.go` (+8/-0)
</details>

## #352 disable logging in encrypted jobs
**State:** MERGED | **Author:** @arriven | **Date:** 2022-03-15 | **Branch:** disable-logs-in-encrypted-jobs → main | **+108/-87** | **Files:** 10

> # Description
> 
> disabling logs in encrypted jobs (still need to disable logging in slowloris and dnsblast modules)
> 
> ## Type of change
> 
> Please delete options that are not relevant.
> 
> - [ ] New feature (non-breaking change which adds functionality)
> 
> ## How Has This Been Tested?
> 
> Please...

<details><summary>Files changed (10)</summary>

- `main.go` (+2/-2)
- `src/jobs/base.go` (+12/-1)
- `src/jobs/complex.go` (+7/-5)
- `src/jobs/dnsblast.go` (+1/-1)
- `src/jobs/http.go` (+37/-22)
- `src/jobs/packetgen.go` (+24/-9)
- `src/jobs/rawnet.go` (+7/-31)
- `src/jobs/slowloris.go` (+2/-2)
- `src/jobs/utils.go` (+13/-7)
- `src/runner/runner.go` (+3/-7)
</details>

## #351 prettier and more human-readable network stats logging
**State:** CLOSED | **Author:** @dshpet | **Date:** 2022-03-15 | **Branch:** network_stats_pretty_log → main | **+15/-4** | **Files:** 1

> # Description
> Make network stats more readable and human-friendly
> -  add tabbed align
> -  structure log
> -  add MB and percentage representation
> 
> ## Type of change
> 
> - [ ] New feature (non-breaking change which adds functionality)
> 
> ## How Has This Been Tested?
> 
> Tested locally in console...

<details><summary>Files changed (1)</summary>

- `src/runner/runner.go` (+15/-4)
</details>

## #350 Ansible playbook to setup Linux VM
**State:** MERGED | **Author:** @ichornyi | **Date:** 2022-03-15 | **Branch:** ansible → main | **+220/-0** | **Files:** 5

> # Description
> 
> In case someone have plain Linux VM's - he can quickly setup application using this simple Ansible playbook
> 
> ## Type of change
> - [x] New feature (non-breaking change which adds functionality)
> 
> ## How Has This Been Tested?
> 
> - [x] Install Ansible
> - [x] Start any plain VM with...

<details><summary>Files changed (5)</summary>

- `.gitignore` (+8/-0)
- `ansible/linux/README.md` (+45/-0)
- `ansible/linux/countries.txt` (+58/-0)
- `ansible/linux/inventory.cfg.example` (+7/-0)
- `ansible/linux/setup.yaml` (+102/-0)
</details>

## #346 Encrypt specific jobs
**State:** MERGED | **Author:** @arriven | **Date:** 2022-03-15 | **Branch:** encrypt-specific-jobs → main | **+82/-20** | **Files:** 6

> # Description
> 
> Add functionality to encrypt only specific jobs. Also add a flag to skip encrypted jobs if someone is very concerned about their security
> 
> WIP #343 
> 
> ## Type of change
> 
> Please delete options that are not relevant.
> 
> - [ ] New feature (non-breaking change which adds...

<details><summary>Files changed (6)</summary>

- `main.go` (+2/-1)
- `src/jobs/base.go` (+5/-2)
- `src/jobs/utils.go` (+45/-0)
- `src/runner/config/config.go` (+3/-17)
- `src/utils/utils.go` (+20/-0)
- `testconfig.json` (+7/-0)
</details>

## #345 docs: fix some typos
**State:** MERGED | **Author:** @MetaMmodern | **Date:** 2022-03-15 | **Branch:** main → main | **+4/-4** | **Files:** 2

> # Description
> 
> Hi, I was just reading docs and found some typo issues).
> 
> Fixes # (issue)
> 
> ## Type of change
> 
> Please delete options that are not relevant.
> 
> - [x] Documentation update
> 
> ## How Has This Been Tested?
> 
> - [x] Ran a preview in VSCode😁
> 
> ## Test Configuration
> 
> - Release...

<details><summary>Comments (2)</summary>

- **@MetaMmodern** (2022-03-15): btw, unfortunately in dark themes that checkbox looks weird and dark, maybe you'd like to replace it with on eof these: ✅☑✔. But it does not matter actually)
- **@MetaMmodern** (2022-03-15): @Arriven ummm, I guess something is wrong here...  Where should I dig? ![image](https://user-images.githubusercontent.com/42899786/158442649-48937b2d-1878-4314-b5d7-dcf9633779eb.png)
</details>

<details><summary>Files changed (2)</summary>

- `docs/faq.md` (+1/-1)
- `src/utils/ota/README.md` (+3/-3)
</details>

## #342 DB1000N | Add advanced configuration default dynamic URL based on version & fix panic on missing system cert pool for the Prometheus Metrics
**State:** CLOSED | **Author:** @sivillakonski | **Date:** 2022-03-17 | **Branch:** main → main | **+150/-4** | **Files:** 5

> Hello there, my fellow friends
> 
> Addressing the issue: https://github.com/Arriven/db1000n/issues/339
> 
> Fix the Windows-related issue related to the missing system cert. pool. `SystemCertPool() (*CertPool, error)` method is not available for the Windows machines (`system root pool is not available...

<details><summary>Comments (3)</summary>

- **@sivillakonski** (2022-03-15): Addressing the request: https://github.com/Arriven/db1000n/issues/341  No need to provide the extra flag to automatically follow the major & minor version changes, thanks to...
- **@sivillakonski** (2022-03-17): @Arriven , mind if I closed the PR? Looks like this feature is not relevant here
- **@arriven** (2022-03-17): @sivillakonski sure
</details>

<details><summary>Files changed (5)</summary>

- `main.go` (+1/-1)
- `src/runner/config/defaultconfig.go` (+28/-1)
- `src/runner/config/defaultconfig_test.go` (+79/-0)
- `src/utils/metrics/prometheus.go` (+2/-1)
- `src/utils/ota/version.go` (+40/-1)
</details>

## #338 Refactor NewClient for fasthttp to make linters happier
**State:** MERGED | **Author:** @jdoe7865623 | **Date:** 2022-03-15 | **Branch:** http → main | **+42/-63** | **Files:** 1

<details><summary>Files changed (1)</summary>

- `src/core/http/http.go` (+42/-63)
</details>

## #337 Send multiple tcp messages in one conn
**State:** MERGED | **Author:** @arriven | **Date:** 2022-03-14 | **Branch:** send-multiple-tcp-messages-in-one-conn → main | **+48/-38** | **Files:** 2

> # Description
> 
> We were only sending one message per opened tcp connection
> 
> ## Type of change
> 
> Please delete options that are not relevant.
> 
> - [ ] Bug fix (non-breaking change which fixes an issue)

<details><summary>Files changed (2)</summary>

- `src/jobs/rawnet.go` (+45/-36)
- `testconfig.json` (+3/-2)
</details>

## #336 Add ARM build
**State:** MERGED | **Author:** @app/ | **Date:** 2022-03-14 | **Branch:** feature/arm-support → main | **+9/-3** | **Files:** 2

> # Description
> 
> Add ARM build for old Raspberry Pi
> 
> ## Type of change
> 
> Please delete options that are not relevant.
> 
> - [ ] Bug fix (non-breaking change which fixes an issue)
> - [x] New feature (non-breaking change which adds functionality)
> - [ ] Breaking change (fix or feature that would...

<details><summary>Files changed (2)</summary>

- `.github/workflows/release-binaries.yaml` (+5/-1)
- `install.sh` (+4/-2)
</details>

## #334 Refactor rawnet to make cyclop happier; close TCP and UDP conns
**State:** MERGED | **Author:** @jdoe7865623 | **Date:** 2022-03-14 | **Branch:** rawnet → main | **+91/-77** | **Files:** 1

<details><summary>Files changed (1)</summary>

- `src/jobs/rawnet.go` (+91/-77)
</details>

## #333 Fix nolint directives
**State:** MERGED | **Author:** @jdoe7865623 | **Date:** 2022-03-14 | **Branch:** nonolint → main | **+42/-67** | **Files:** 5

> # Description
> 
> Please do not accept PRs with nolint directives. Some are introduced simply because of lack of knowledge of [common golang wisdom](https://zchee.github.io/golang-wiki/CodeReviewComments/#indent-error-flow).

<details><summary>Comments (1)</summary>

- **@sivillakonski** (2022-03-15): Haha, really? Chaps, the golint directives that are set for this project are sometimes just ridiculous.   Don't blindly follow someone's Go guides, there is a native Go's one -...
</details>

<details><summary>Files changed (5)</summary>

- `main.go` (+18/-19)
- `src/utils/ota/ota.go` (+17/-0)
- `src/utils/ota/restart_darwin.go` (+0/-23)
- `src/utils/ota/restart_linux.go` (+0/-23)
- `src/utils/ota/restart_linux_test.go` (+7/-2)
</details>

## #332 Add "updater mode"
**State:** MERGED | **Author:** @bitshape | **Date:** 2022-03-15 | **Branch:** updater-mode → main | **+138/-61** | **Files:** 6

> # Description
> 
> This is mostly useful if you're running `db1000n` with docker-compose with VPN container. In this case you're likely to receive errors or time-outs while trying to update config file due to the fact that VPN connection is already highly saturated. Typically it looks like...

<details><summary>Files changed (6)</summary>

- `Dockerfile` (+2/-0)
- `docker-compose.yml` (+39/-3)
- `main.go` (+12/-1)
- `src/runner/config/config.go` (+23/-48)
- `src/runner/runner.go` (+19/-9)
- `src/utils/updater/updater.go` (+43/-0)
</details>

## #329 Remove '304 Not Modified' to not cause confusion
**State:** MERGED | **Author:** @bitshape | **Date:** 2022-03-14 | **Branch:** remove-304-logging → main | **+0/-2** | **Files:** 1

> # Description
> 
> Seems like logging `Received HTTP 304 Not Modified` might be confusing. It's also somewhat redundant since app will log `The config has not changed. Keep calm and carry on!` anyway.
> 
> Related to https://github.com/Arriven/db1000n/issues/327
> 
> ## Type of change
> 
> - [x] Bug fix...

<details><summary>Files changed (1)</summary>

- `src/runner/config/config.go` (+0/-2)
</details>

## #328 Add option to apply your own proxy list with command-line args
**State:** CLOSED | **Author:** @Mancersoft | **Date:** 2022-03-20 | **Branch:** fix_proxy_list → main | **+12/-5** | **Files:** 4

> # Description
> The app was not using a proxy list from URL when it was applied via command-line argument "-proxylist-url".
> 
> The fix allows specifying proxy list url via the command-line argument (without using custom config).
> 
> Changes summary:
> Add ProxyListURL to GlobalConfig
> Make...

<details><summary>Comments (8)</summary>

- **@Mancersoft** (2022-03-20): All right, I will extend the existing system-proxy flag (not sure why the existing -proxylist-url flag is never used though, I didn't add it, it was in the code, just never used from the...
- **@arriven** (2022-03-20): @Staskkk the idea with the file seems good but you can kinda already achieve that functionality via the shell. i.e. `db1000n --system-proxy $(cat proxylist.txt | tr '\n' ',')`
- **@Mancersoft** (2022-03-20): All right, I will try to post the changes later today, thanks!
- **@arriven** (2022-03-20): actually, you can already pass a comma-separated list of proxies into the `--proxy` flag (misstyped that flag in previous comment, sorry). This won't work if you want the proxylist to be dynamically...
- **@Mancersoft** (2022-03-20): @Arriven All right, I'll use the --proxy then and make PR for some other issue. BTW, is it always just choosing the random proxy from the list? Maybe it makes sense to use all the proxies in the...
- **@arriven** (2022-03-20): It's always choosing random proxy from the list, yes, and I think it's better than splitting the list between threads as that would actually make it easier for specific targets to defend - they'd...
- **@arriven** (2022-03-20): Also see #378 for a draft of proxylist refactoring, I think I'll finish it today a bit later
- **@Mancersoft** (2022-03-20): All right man, thanks for the explanation!
</details>

<details><summary>Files changed (4)</summary>

- `main.go` (+2/-1)
- `src/jobs/base.go` (+1/-0)
- `src/jobs/http.go` (+7/-2)
- `src/utils/templates/templates.go` (+2/-2)
</details>

## #326 Enable and fix more linters
**State:** MERGED | **Author:** @jdoe7865623 | **Date:** 2022-03-13 | **Branch:** linters → main | **+92/-61** | **Files:** 12

<details><summary>Files changed (12)</summary>

- `.golangci.yml` (+3/-3)
- `main.go` (+27/-19)
- `src/core/dnsblast/dns-blast.go` (+1/-1)
- `src/core/dnsblast/dns-blast_test.go` (+6/-0)
- `src/core/dnsblast/dns-dhh.go` (+1/-1)
- `src/core/dnsblast/dns-dhh_test.go` (+2/-0)
- `src/core/http/http.go` (+2/-2)
- `src/core/packetgen/utils.go` (+4/-3)
- `src/runner/config/config.go` (+9/-4)
- `src/utils/countrychecker.go` (+13/-23)
- `src/utils/metrics/prometheus.go` (+4/-3)
- `src/utils/templates/templates.go` (+20/-2)
</details>

## #325 fix: release script fixed to add correct build flags
**State:** CLOSED | **Author:** @arfgdev | **Date:** 2022-03-13 | **Branch:** release_fix → main | **+2/-1** | **Files:** 2

> # Description
> 
> release binaries github action fixed
> Fixes #322
> 
> ## Type of change
> 
> - [x] Bug fix (non-breaking change which fixes an issue)

<details><summary>Comments (1)</summary>

- **@arriven** (2022-03-13): Already fixed, there was a caveat of making make build output .exe in order to comply with the action (just one more point in my "why I don't like windows" list). Changing the version name to...
</details>

<details><summary>Files changed (2)</summary>

- `.github/workflows/release-binaries.yaml` (+1/-0)
- `src/utils/ota/version.go` (+1/-1)
</details>

## #324 cloudfare response example [DRAFT]
**State:** OPEN | **Author:** @bmirnoff | **Date:** 2022-03-13 | **Branch:** cf_bypass → main | **+158/-0** | **Files:** 2

> This is the initial start of work for Cloudflare bypass.
> 
> IN SCOPE OF  #293

<details><summary>Files changed (2)</summary>

- `src/core/cf/cf.go` (+9/-0)
- `src/core/cf/test_cf_response.txt` (+149/-0)
</details>

## #323 GCP Terraform: code refactoring and improvements `[triage needed]`
**State:** MERGED | **Author:** @ichornyi | **Date:** 2022-03-13 | **Branch:** terraform-gcp-improvements → main | **+152/-54** | **Files:** 5

> # Description
> 
> - Allow to restart process with VPN location change every 10 minutes
> - Instance groups manager added to automatically spawn new instances when old is stopped
> - code format
> - README updated
> - VPN client moved to separated container in order to make logs work
> 
> ## Type of...

<details><summary>Comments (3)</summary>

- **@ichornyi** (2022-03-13): @Arriven is something needs to be fixed here?
- **@arriven** (2022-03-13): @paalomnikdev I don't have physical capacity to confirm if changes to deployment scripts yet so I'm usually asking someone who already uses the setup in question to confirm that the changes are...
- **@ichornyi** (2022-03-13): @Arriven I am using it and spent whole day to improve it let me share some examples how it's working now currently I'm using 2 VM's <img width="1194" alt="Screenshot 2022-03-13 at 20 22 03"...
</details>

<details><summary>Files changed (5)</summary>

- `.gitignore` (+1/-0)
- `terraform/gcp_expressvpn/README.md` (+18/-1)
- `terraform/gcp_expressvpn/main.tf` (+117/-49)
- `terraform/gcp_expressvpn/variables.tf` (+5/-4)
- `terraform/gcp_expressvpn/versions.tf` (+11/-0)
</details>

## #321 fix: terrafrom aws simplified `[triage needed]`
**State:** MERGED | **Author:** @arfgdev | **Date:** 2022-03-13 | **Branch:** fix_aws_terraform → main | **+1/-13** | **Files:** 1

> # Description
> removed section from AWS terrafrom that could make deployment so long
> Fixes #244
> 
> ## Type of change
> 
> - [x] Bug fix (non-breaking change which fixes an issue)
> 
> ## How Has This Been Tested?
> - go to ./terraform/aws directory
> - run `terraform init`
> - run `terraform apply...

<details><summary>Files changed (1)</summary>

- `terraform/aws/main.tf` (+1/-13)
</details>

## #320 feat: added plain text proxy list parsing
**State:** MERGED | **Author:** @arfgdev | **Date:** 2022-03-13 | **Branch:** plain_text_proxies → main | **+11/-1** | **Files:** 1

> # Description
> now proxies urls can be provided not only as json array but as plain text delimited with newline(`\n`)
> Fixes #282
> 
> ## Type of change
> 
> Please delete options that are not relevant.
> 
> - [ ] Bug fix (non-breaking change which fixes an issue)
> - [x] New feature (non-breaking change...

<details><summary>Files changed (1)</summary>

- `src/utils/templates/templates.go` (+11/-1)
</details>

## #319 fix absolute path handling for configs
**State:** MERGED | **Author:** @arriven | **Date:** 2022-03-13 | **Branch:** fix-absolute-path-handling → main | **+3/-1** | **Files:** 1

> # Description
> 
> Check for absolute path in `config.fetchSingle`
> 
> Fixes #318 
> 
> ## Type of change
> 
> Please delete options that are not relevant.
> 
> - [ ] Bug fix (non-breaking change which fixes an issue)

<details><summary>Files changed (1)</summary>

- `src/runner/config/config.go` (+3/-1)
</details>

## #317 DB1000N | Add app. auto-restart upon successful update
**State:** MERGED | **Author:** @sivillakonski | **Date:** 2022-03-13 | **Branch:** main → main | **+367/-85** | **Files:** 9

> # Over-the-air updates
> 
> Lots of maintainers run their needles on a bare metal machines.
> As long as this project is so frequently updated, it might be
> a good idea to let them update it without the hassle.
> 
> - [V] Enabled automatic time-based version check
> - [V] Enabled application self-restart...

<details><summary>Comments (2)</summary>

- **@sivillakonski** (2022-03-13): @Arriven, please, add the version embedding to the binary distributed thru release downloads. The example on how to add the version you can find in the `Makefile`.  Btw, I can't test if the restart...
- **@sivillakonski** (2022-03-13): Checked the build with a cross-compilation in the docker container: ~~~ root@0478a04ad044:/go/src/github.com/Arriven/db1000n# go version go version go1.16.15...
</details>

<details><summary>Files changed (9)</summary>

- `Dockerfile` (+1/-2)
- `main.go` (+67/-6)
- `src/utils/ota/README.md` (+66/-23)
- `src/utils/ota/ota.go` (+17/-53)
- `src/utils/ota/restart.go` (+10/-0)
- `src/utils/ota/restart_darwin.go` (+76/-0)
- `src/utils/ota/restart_linux.go` (+76/-0)
- `src/utils/ota/restart_linux_test.go` (+53/-0)
- `src/utils/ota/version.go` (+1/-1)
</details>

## #316 Refactor how configs are fetched
**State:** MERGED | **Author:** @bitshape | **Date:** 2022-03-13 | **Branch:** refactor-config → main | **+74/-45** | **Files:** 2

> # Description
> 
> This will rely on `Last-Modified / If-Modified-Since` headers to see if remote config has changed. If these headers aren't available, it will try to use `Etag / If-None-Match` as fallback. If those aren't available either it will simply try to fetch whole file. This should result...

<details><summary>Files changed (2)</summary>

- `src/runner/config/config.go` (+70/-38)
- `src/runner/runner.go` (+4/-7)
</details>

## #314 Update docker-compose.yml example
**State:** MERGED | **Author:** @bitshape | **Date:** 2022-03-13 | **Branch:** update-dns-check → main | **+6/-6** | **Files:** 1

> # Description
> 
> Use Google DNS while performing DNS health check
> 
> Fixes https://github.com/Arriven/db1000n/issues/300#issuecomment-1065949528
> 
> ## Type of change
> 
> - [x] New feature (non-breaking change which adds functionality)

<details><summary>Files changed (1)</summary>

- `docker-compose.yml` (+6/-6)
</details>

## #312 Enable and fix more linters
**State:** MERGED | **Author:** @jdoe7865623 | **Date:** 2022-03-12 | **Branch:** linters → main | **+132/-112** | **Files:** 26

<details><summary>Files changed (26)</summary>

- `.golangci.yml` (+5/-5)
- `main.go` (+33/-45)
- `src/core/dnsblast/dns-blast.go` (+5/-2)
- `src/core/dnsblast/dns-blast_test.go` (+4/-2)
- `src/core/dnsblast/dns-dhh.go` (+1/-0)
- `src/core/dnsblast/dns-dhh_test.go` (+1/-0)
- `src/core/dnsblast/qry/types.go` (+1/-3)
- `src/core/http/http.go` (+1/-0)
- `src/core/packetgen/packetgen.go` (+8/-13)
- `src/core/packetgen/utils.go` (+7/-6)
- `src/core/slowloris/slowloris.go` (+7/-2)
- `src/jobs/complex.go` (+5/-2)
- `src/jobs/dnsblast.go` (+1/-3)
- `src/jobs/http.go` (+3/-2)
- `src/jobs/packetgen.go` (+4/-2)
- `src/jobs/rawnet.go` (+7/-3)
- `src/jobs/slowloris.go` (+1/-0)
- `src/runner/config/config.go` (+5/-0)
- `src/runner/config/defaultconfig.go` (+1/-0)
- `src/runner/runner.go` (+6/-2)
- `src/utils/countrychecker.go` (+3/-4)
- `src/utils/crypto.go` (+3/-0)
- `src/utils/metrics/metrics.go` (+3/-1)
- `src/utils/metrics/prometheus.go` (+13/-8)
- `src/utils/statistics.go` (+2/-2)
- `src/utils/templates/templates.go` (+2/-5)
</details>

## #309 Terraform variables update
**State:** MERGED | **Author:** @exsesx | **Date:** 2022-03-12 | **Branch:** terraform-update → main | **+2/-2** | **Files:** 2

> # Description
> 
> This PR updates Terraform variables for Azure and Heroku.
> 
> Fixes #308.
> 
> ## Type of change
> 
> Please delete options that are not relevant.
> 
> - [x] Bug fix (non-breaking change which fixes an issue)
> 
> ## How Has This Been Tested?
> 
> Please describe the tests that you ran to...

<details><summary>Files changed (2)</summary>

- `terraform/azure/variables.tf` (+1/-1)
- `terraform/heroku/terraform.tfvars` (+1/-1)
</details>

## #307 Enable, configure, and fix linters
**State:** MERGED | **Author:** @jdoe7865623 | **Date:** 2022-03-12 | **Branch:** linters → main | **+1201/-1010** | **Files:** 29

<details><summary>Files changed (29)</summary>

- `.golangci.yml` (+903/-908)
- `main.go` (+1/-0)
- `src/core/dnsblast/dns-blast.go` (+19/-6)
- `src/core/dnsblast/dns-blast_test.go` (+4/-1)
- `src/core/dnsblast/dns-dhh.go` (+4/-2)
- `src/core/dnsblast/dns-dhh_test.go` (+9/-8)
- `src/core/dnsblast/qry/types.go` (+1/-0)
- `src/core/http/http.go` (+10/-3)
- `src/core/packetgen/packetgen.go` (+5/-1)
- `src/core/packetgen/utils.go` (+14/-3)
- `src/core/slowloris/slowloris.go` (+28/-7)
- `src/jobs/complex.go` (+9/-3)
- `src/jobs/dnsblast.go` (+3/-1)
- `src/jobs/http.go` (+35/-13)
- `src/jobs/packetgen.go` (+11/-1)
- `src/jobs/rawnet.go` (+3/-2)
- `src/jobs/slowloris.go` (+7/-4)
- `src/jobs/utils.go` (+18/-5)
- `src/runner/config/config.go` (+13/-3)
- `src/runner/config/defaultconfig.go` (+0/-1)
- `src/runner/runner.go` (+9/-6)
- `src/utils/countrychecker.go` (+6/-1)
- `src/utils/crypto.go` (+6/-0)
- `src/utils/metrics/metrics.go` (+5/-4)
- `src/utils/metrics/prometheus.go` (+24/-9)
- `src/utils/ota/ota.go` (+13/-3)
- `src/utils/statistics.go` (+11/-10)
- `src/utils/templates/templates.go` (+15/-2)
- `src/utils/utils.go` (+15/-3)
</details>

## #306 Explicitly enable all non-deprecated, currently passing linters
**State:** MERGED | **Author:** @jdoe7865623 | **Date:** 2022-03-12 | **Branch:** golangci → main | **+1856/-0** | **Files:** 1

> This configuration explicitly enables all golangci-lint linters which are not deprecated and pass the build. All other linters require fixes to be enabled.

<details><summary>Files changed (1)</summary>

- `.golangci.yml` (+1856/-0)
</details>

## #305 use context in runner
**State:** MERGED | **Author:** @arriven | **Date:** 2022-03-12 | **Branch:** cleanup → main | **+62/-75** | **Files:** 5

> # Description
> 
> Cleanup runner to use ctx instead of stop channel. Also some minor code cleanup
> 
> ## Type of change
> 
> Please delete options that are not relevant.
> 
> - [ ] Bug fix (non-breaking change which fixes an issue)
> 
> ## How Has This Been Tested?
> 
> Please describe the tests that you ran...

<details><summary>Files changed (5)</summary>

- `main.go` (+6/-3)
- `src/core/packetgen/utils.go` (+2/-2)
- `src/jobs/http.go` (+1/-2)
- `src/jobs/rawnet.go` (+1/-2)
- `src/runner/runner.go` (+52/-66)
</details>

## #304 12 factor flags
**State:** MERGED | **Author:** @arriven | **Date:** 2022-03-12 | **Branch:** 12-factor-flags → main | **+73/-41** | **Files:** 4

> # Description
> 
> Provide a way to set general app configuration via env variables in addition to flags
> 
> ## Type of change
> 
> Please delete options that are not relevant.
> 
> - [ ] New feature (non-breaking change which adds functionality)
> 
> ## How Has This Been Tested?
> 
> Please describe the...

<details><summary>Files changed (4)</summary>

- `main.go` (+21/-21)
- `src/runner/runner.go` (+7/-15)
- `src/utils/metrics/prometheus.go` (+1/-5)
- `src/utils/utils.go` (+44/-0)
</details>

## #302 Add --strict-country-check and --country-list command line parameters
**State:** MERGED | **Author:** @bitshape | **Date:** 2022-03-14 | **Branch:** test-ip → main | **+105/-33** | **Files:** 4

> # Description
> 
> I'm still trying to figure out how to make Docker VPN setup be more stable, hopefully this is step in right direction.
> 
> IP/Country check will be performed before starting any jobs. This is slight departure from current code but it shouldn't be a breaking change as options are...

<details><summary>Files changed (4)</summary>

- `docker-compose.yml` (+12/-0)
- `main.go` (+10/-2)
- `src/utils/countrychecker.go` (+70/-31)
- `src/utils/utils.go` (+13/-0)
</details>

## #301 Some code restructure
**State:** MERGED | **Author:** @arriven | **Date:** 2022-03-11 | **Branch:** code-restructure → main | **+271/-287** | **Files:** 30

> # Description
> 
> Moving code a bit to improve maintainability
> 
> ## Type of change
> 
> Please delete options that are not relevant.
> 
> - [ ] Bug fix (non-breaking change which fixes an issue)
> 
> ## How Has This Been Tested?
> 
> Please describe the tests that you ran to verify your changes. Provide...

<details><summary>Files changed (30)</summary>

- `Dockerfile` (+1/-1)
- `Makefile` (+1/-1)
- `config/examples/advanced/ddos-guard.yaml` (+48/-44)
- `main.go` (+3/-3)
- `ota/version.go` (+0/-6)
- `src/core/dnsblast/README.md` (+0/-0)
- `src/core/dnsblast/dns-blast.go` (+2/-2)
- `src/core/dnsblast/dns-blast_test.go` (+0/-0)
- `src/core/dnsblast/dns-dhh.go` (+0/-0)
- `src/core/dnsblast/dns-dhh_test.go` (+0/-0)
- `src/core/dnsblast/qry/types.go` (+0/-0)
- `src/core/http/http.go` (+138/-0)
- `src/core/packetgen/packetgen.go` (+0/-0)
- `src/core/packetgen/utils.go` (+0/-0)
- `src/core/slowloris/slowloris.go` (+1/-1)
- `src/jobs/dnsblast.go` (+1/-1)
- `src/jobs/http.go` (+36/-204)
- `src/jobs/packetgen.go` (+2/-2)
- `src/jobs/rawnet.go` (+1/-1)
- `src/jobs/slowloris.go` (+1/-1)
- `src/runner/runner.go` (+1/-1)
- `src/utils/countrychecker.go` (+6/-7)
- `src/utils/metrics/metrics.go` (+0/-0)
- `src/utils/metrics/prometheus.go` (+0/-0)
- `src/utils/ota/README.md` (+0/-0)
- `src/utils/ota/ota.go` (+3/-0)
- `src/utils/ota/version.go` (+8/-0)
- `src/utils/templates/templates.go` (+1/-1)
- `testconfig.json` (+11/-7)
- `testconfig.yaml` (+6/-4)
</details>

## #299 Added loop job
**State:** MERGED | **Author:** @arriven | **Date:** 2022-03-11 | **Branch:** more-utility-jobs → main | **+66/-24** | **Files:** 4

> # Description
> 
> Added a job to simulate loops in scenarios
> 
> ## Type of change
> 
> Please delete options that are not relevant.
> 
> - [ ] New feature (non-breaking change which adds functionality)
> 
> ## How Has This Been Tested?
> 
> Please describe the tests that you ran to verify your changes....

<details><summary>Files changed (4)</summary>

- `src/jobs/base.go` (+31/-18)
- `src/jobs/complex.go` (+4/-4)
- `src/jobs/utils.go` (+29/-0)
- `src/runner/runner.go` (+2/-2)
</details>

## #297 add httpattack client
**State:** CLOSED | **Author:** @bmirnoff | **Date:** 2022-03-11 | **Branch:** refactor_http → main | **+299/-232** | **Files:** 2

> # Description
> 
> This is refactoring of HTTP job that causes problematic enhancement of http attacking logic.
> 
> Main concept: more HTTP attack logic into separate go files. The job only allocates HttpAttackClient and executes required methods.
> 
> This refactoring will help to add new options for...

<details><summary>Files changed (2)</summary>

- `src/httpattack/httpattack.go` (+273/-0)
- `src/jobs/http.go` (+26/-232)
</details>

## #296 Added healthcheck and autoheal labels
**State:** MERGED | **Author:** @mjolnir404 | **Date:** 2022-03-11 | **Branch:** main → main | **+36/-8** | **Files:** 1

> Added healthcheck and autoheal labels to every container
> 
> # Description
> 
> Think for `willfarrell/autoheal` container to work properly the `healthcheck` and `label` should be on every container. Currently If `ovpn_XX` container stops working and is restarted by autoheal, the `db1000n_XX` that...

<details><summary>Files changed (1)</summary>

- `docker-compose.yml` (+36/-8)
</details>

## #295 Use ENTRYPOINT instead of CMD
**State:** MERGED | **Author:** @ivankovnatsky | **Date:** 2022-03-11 | **Branch:** main → main | **+1/-1** | **Files:** 1

> # Description
> 
> To be able to pass only args, instead of both command and args:
> 
> ```
>     spec:
>       containers:
>         - name: db1000n
>           image: ghcr.io/arriven/db1000n:latest
>           args: ["-enable-self-update"]
> ```
> 
> ## Type of change
> 
> Please delete options that are not...

<details><summary>Files changed (1)</summary>

- `Dockerfile` (+1/-1)
</details>

## #291 Add MkDocs
**State:** MERGED | **Author:** @m-v-kalashnikov | **Date:** 2022-03-11 | **Branch:** main → main | **+1375/-262** | **Files:** 56

> # Description
> 
> Add MkDocs setup
> 
> Fixes # ([issue](https://github.com/Arriven/db1000n/issues/194))
> 
> ## Type of change
> 
> Please delete options that are not relevant.
> 
> - [ ] New feature (non-breaking change which adds functionality)
> - [ ] Documentation update
> 
> ## How Has This Been...

<details><summary>Comments (2)</summary>

- **@arriven** (2022-03-11): @m-v-kalashnikov looks really great, but any chance we can split out root README.md from mkdocs index? regular github UI doesn't seem to parse mkdocs directives properly and it would probably be nice...
- **@m-v-kalashnikov** (2022-03-11): >   WIP
</details>

<details><summary>Files changed (56)</summary>

- `.github/workflows/gh-pages.yml` (+12/-10)
- `.github/workflows/markdownlint.yaml` (+2/-1)
- `FAQ.md` (+0/-60)
- `LICENSE` (+21/-0)
- `README-ua.md` (+0/-90)
- `README.md` (+44/-30)
- `db1000n.rb` (+3/-0)
- `docs/_config.yml` (+0/-1)
- `docs/advanced-docs/advanced-and-devs.md` (+20/-8)
- `docs/advanced-docs/config-encryption.md` (+3/-1)
- `docs/advanced-docs/configuration.md` (+0/-0)
- `docs/advanced-docs/docker-vpn.md` (+8/-2)
- `docs/advanced-docs/kubernetes/helm-charts.md` (+6/-0)
- `docs/advanced-docs/kubernetes/manifests.md` (+6/-0)
- `docs/advanced-docs/prometheus.md` (+0/-0)
- `docs/advanced-docs/pull-request-template.md` (+6/-0)
- `docs/advanced-docs/terraform/aws.md` (+6/-0)
- `docs/advanced-docs/terraform/azure.md` (+6/-0)
- `docs/advanced-docs/terraform/digital-ocean.md` (+6/-0)
- `docs/advanced-docs/terraform/gcp.md` (+6/-0)
- `docs/advanced-docs/terraform/heroku.md` (+6/-0)
- `docs/azure.md` (+12/-0)
- `docs/azure.uk.md` (+20/-18)
- `docs/faq.md` (+90/-0)
- `docs/faq.uk.md` (+92/-0)
- `docs/images/azure/tutorial-1.png` (+0/-0)
- `docs/images/azure/tutorial-10.png` (+0/-0)
- `docs/images/azure/tutorial-11.png` (+0/-0)
- `docs/images/azure/tutorial-12.png` (+0/-0)
- `docs/images/azure/tutorial-13.png` (+0/-0)
- `docs/images/azure/tutorial-14.png` (+0/-0)
- `docs/images/azure/tutorial-15.png` (+0/-0)
- `docs/images/azure/tutorial-16.png` (+0/-0)
- `docs/images/azure/tutorial-17.png` (+0/-0)
- `docs/images/azure/tutorial-2.png` (+0/-0)
- `docs/images/azure/tutorial-3.png` (+0/-0)
- `docs/images/azure/tutorial-4.png` (+0/-0)
- `docs/images/azure/tutorial-5.png` (+0/-0)
- `docs/images/azure/tutorial-6.png` (+0/-0)
- `docs/images/azure/tutorial-7.png` (+0/-0)
- `docs/images/azure/tutorial-8.png` (+0/-0)
- `docs/images/azure/tutorial-9.png` (+0/-0)
- `docs/index.md` (+6/-0)
- `docs/index.uk.md` (+106/-0)
- `docs/license.md` (+6/-0)
- `docs/over-the-air.md` (+6/-0)
- `docs/system-pages/vpn.md` (+0/-31)
- `docs/vpn.md` (+14/-0)
- `docs/vpn.uk.md` (+14/-0)
- `kubernetes/helm-charts/README.md` (+2/-2)
- `kubernetes/manifests/README.md` (+4/-4)
- `mkdocs.yml` (+120/-0)
- `poetry.lock` (+685/-0)
- `pyproject.toml` (+21/-0)
- `src/utils/countrychecker.go` (+15/-3)
- `terraform/azure/README.md` (+1/-1)
</details>

## #290 Setup docker publish with ko
**State:** MERGED | **Author:** @arriven | **Date:** 2022-03-11 | **Branch:** ko → main | **+34/-0** | **Files:** 2

> # Description
> 
> Build and push docker images with ko
> 
> ## Type of change
> 
> Please delete options that are not relevant.
> 
> - [ ] New feature (non-breaking change which adds functionality)
> 
> ## How Has This Been Tested?
> 
> Please describe the tests that you ran to verify your changes. Provide...

<details><summary>Files changed (2)</summary>

- `.github/workflows/ko-build.yaml` (+25/-0)
- `.ko.yaml` (+9/-0)
</details>

## #289 fix ota readme markdown
**State:** MERGED | **Author:** @arriven | **Date:** 2022-03-11 | **Branch:** fix-markdown → main | **+21/-15** | **Files:** 1

> # Description
> 
> fix markdown in ota readme
> 
> ## Type of change
> 
> Please delete options that are not relevant.
> 
> - [ ] Documentation update
> 
> ## How Has This Been Tested?
> 
> Please describe the tests that you ran to verify your changes. Provide instructions so we can reproduce. Please also list...

<details><summary>Files changed (1)</summary>

- `ota/README.md` (+21/-15)
</details>

## #288 DB1000N | Add basic Over-The-Air updates support
**State:** MERGED | **Author:** @sivillakonski | **Date:** 2022-03-11 | **Branch:** main → main | **+180/-2** | **Files:** 7

> # Over-the-air updates
> 
> Lots of maintainers run their needles on a bare metal machines.
> As long as this project is so frequently updated, it might be
> a good idea to let them update it without the hassle.
> 
> ### TODO:
> *TO BE CONFIRMED WITH THE CODE OWNER!*
> * [?] Enable automatic time-based...

<details><summary>Comments (3)</summary>

- **@arriven** (2022-03-11): @sivillakonski looks good, thanks for this feature! As further steps I'd focus on time-based version check and self-restart on update if you wish to continue working on it. Other two options seem...
- **@sivillakonski** (2022-03-11): Sure, @Arriven, let me do this. I just wanted to make sure that this is something that project needs
- **@arriven** (2022-03-11): @sivillakonski sure, I wouldn't say it's critical but definitely something users will enjoy
</details>

<details><summary>Files changed (7)</summary>

- `Makefile` (+12/-2)
- `go.mod` (+8/-0)
- `go.sum` (+30/-0)
- `main.go` (+10/-0)
- `ota/README.md` (+46/-0)
- `ota/ota.go` (+68/-0)
- `ota/version.go` (+6/-0)
</details>

## #286 Ddos guard test
**State:** MERGED | **Author:** @arriven | **Date:** 2022-03-10 | **Branch:** ddos-guard-test → main | **+7/-7** | **Files:** 1

> # Description
> 
> tested ddos guard bypass scenario on the test site from example and it works

<details><summary>Files changed (1)</summary>

- `config/examples/advanced/ddos-guard.yaml` (+7/-7)
</details>

## #285 Remove warning about slowloris being unfinished
**State:** MERGED | **Author:** @arriven | **Date:** 2022-03-10 | **Branch:** docs-update → main | **+0/-2** | **Files:** 1

> Slowloris has been fixed couple days ago to support preliminary stop. Forgot to update configuration reference (TODO: update the configuration doc with all new jobs parameters)
> 
> - [ ] Documentation update

<details><summary>Files changed (1)</summary>

- `docs/configuration.md` (+0/-2)
</details>

## #284 Fix metrics value type
**State:** MERGED | **Author:** @arriven | **Date:** 2022-03-10 | **Branch:** fix-metrics-value-type → main | **+18/-18** | **Files:** 4

> # Description
> 
> change metrics storage value type to uint64
> 
> Fixes #280 
> 
> ## Type of change
> 
> Please delete options that are not relevant.
> 
> - [ ] Bug fix (non-breaking change which fixes an issue)

<details><summary>Files changed (4)</summary>

- `src/jobs/http.go` (+4/-4)
- `src/jobs/packetgen.go` (+1/-1)
- `src/jobs/rawnet.go` (+3/-3)
- `src/metrics/metrics.go` (+10/-10)
</details>

## #283 Complex jobs ddos guard test
**State:** MERGED | **Author:** @arriven | **Date:** 2022-03-10 | **Branch:** complex-jobs-ddos-guard-test → main | **+164/-14** | **Files:** 6

> # Description
> 
> A showcase of the tools capabilities by implementing an example of ddos-guard bypass purely via configuration (it is done for educational purposes only and neither this nor original bypasses seem to work anyway)
> 
> ## Type of change
> 
> Please delete options that are not...

<details><summary>Files changed (6)</summary>

- `config/examples/advanced/ddos-guard.yaml` (+99/-0)
- `src/jobs/base.go` (+2/-0)
- `src/jobs/complex.go` (+1/-12)
- `src/jobs/http.go` (+2/-2)
- `src/jobs/utils.go` (+44/-0)
- `src/utils/templates/templates.go` (+16/-0)
</details>

## #277 Add complex job scenarios
**State:** MERGED | **Author:** @arriven | **Date:** 2022-03-10 | **Branch:** complex-jobs → main | **+315/-92** | **Files:** 11

> # Description
> 
> Adding jobs that would allow to create complex attack patterns
> 
> ## Type of change
> 
> Please delete options that are not relevant.
> 
> - [ ] New feature (non-breaking change which adds functionality)
> 
> ## How Has This Been Tested?
> 
> Please describe the tests that you ran to...

<details><summary>Files changed (11)</summary>

- `src/jobs/base.go` (+17/-12)
- `src/jobs/complex.go` (+94/-0)
- `src/jobs/dnsblast.go` (+7/-8)
- `src/jobs/http.go` (+126/-29)
- `src/jobs/packetgen.go` (+9/-9)
- `src/jobs/rawnet.go` (+13/-14)
- `src/jobs/slowloris.go` (+5/-6)
- `src/runner/runner.go` (+7/-1)
- `src/utils/templates/templates.go` (+10/-0)
- `src/utils/utils.go` (+12/-0)
- `testconfig.yaml` (+15/-13)
</details>

## #276 Fix goroutine leaks if job fails
**State:** MERGED | **Author:** @arriven | **Date:** 2022-03-10 | **Branch:** fix-goroutine-leaks-if-job-fails → main | **+66/-49** | **Files:** 8

> # Description
> 
> Use local function context in order to prevent metric writers being running after the job has crashed
> 
> ## Type of change
> 
> Please delete options that are not relevant.
> 
> - [ ] Bug fix (non-breaking change which fixes an issue)

<details><summary>Files changed (8)</summary>

- `src/dnsblast/dns-blast.go` (+7/-1)
- `src/dnsblast/dns-blast_test.go` (+1/-1)
- `src/jobs/base.go` (+8/-8)
- `src/jobs/dnsblast.go` (+8/-1)
- `src/jobs/http.go` (+34/-34)
- `src/jobs/packetgen.go` (+2/-0)
- `src/jobs/rawnet.go` (+4/-4)
- `src/jobs/slowloris.go` (+2/-0)
</details>

## #275 Add willfarrell/autoheal to docker-compose.yaml to restart OpenVPN containers
**State:** MERGED | **Author:** @bitshape | **Date:** 2022-03-10 | **Branch:** vpn-autoheal → main | **+25/-1** | **Files:** 1

> # Description
> 
> This runs a command of your choice (`nslookup google.com`) every X seconds to verify that OpenVPN container still has an active VPN connection. If it doesn't, containers with `autoheal: true` label will be auto-restarted by...

<details><summary>Files changed (1)</summary>

- `docker-compose.yml` (+25/-1)
</details>

## #274 Increase HTTP timeout for fetching config to 20 seconds
**State:** MERGED | **Author:** @bitshape | **Date:** 2022-03-10 | **Branch:** increase-http-timeout → main | **+5/-1** | **Files:** 1

> # Description
> 
> I found config updating process throws less errors when timeout is increased. Which makes sense since `db1000n` saturates your channel if you're using VPN.
> 
> ## Type of change
> 
> Please delete options that are not relevant.
> 
> - [x] Bug fix (non-breaking change which fixes an...

<details><summary>Files changed (1)</summary>

- `src/runner/config/config.go` (+5/-1)
</details>

## #271 User friendly logs
**State:** MERGED | **Author:** @arriven | **Date:** 2022-03-09 | **Branch:** user-friendly-logs → main | **+3/-0** | **Files:** 1

> # Description
> 
> forgot to include one more commit

<details><summary>Files changed (1)</summary>

- `src/jobs/rawnet.go` (+3/-0)
</details>

## #270 More user friendly logs
**State:** MERGED | **Author:** @arriven | **Date:** 2022-03-09 | **Branch:** user-friendly-logs → main | **+22/-8** | **Files:** 5

> ```text
> 2022/03/09 17:55:20.121068 runner.go:162: Атака проводиться успішно! Руський воєнний корабль іди нахуй!
> 2022/03/09 17:55:20.121085 runner.go:163: Attack is successful! Russian warship, go fuck yourself!
> 2022/03/09 17:55:20.121093 runner.go:164: The app has generated approximately 1188...

<details><summary>Files changed (5)</summary>

- `src/jobs/http.go` (+5/-2)
- `src/jobs/packetgen.go` (+1/-1)
- `src/jobs/rawnet.go` (+2/-2)
- `src/metrics/metrics.go` (+8/-1)
- `src/runner/runner.go` (+6/-2)
</details>

## #267 Added an ability to specify app flags in azure terraform `[triage needed]`
**State:** MERGED | **Author:** @predivan2022 | **Date:** 2022-03-10 | **Branch:** extend_terraform_azure → main | **+17/-0** | **Files:** 5

> # Description
> This PR adds an ability to explicitly specify db1000n flags in Azure terraform scripts. It might be very useful in case if custom config is required to be used.
> 
> ## Usage
> Specify `attack_commands` variable in `terraform.tfvars`
> ``
> attack_commands =...

<details><summary>Comments (1)</summary>

- **@arriven** (2022-03-09): To improve stability I would like all changes that are not covered by CI to be vet by someone other than the author who's already using the corresponding guide. This particular change seems less...
</details>

<details><summary>Files changed (5)</summary>

- `terraform/azure/README.md` (+1/-0)
- `terraform/azure/bomblet/main.tf` (+1/-0)
- `terraform/azure/bomblet/variables.tf` (+4/-0)
- `terraform/azure/main.tf` (+6/-0)
- `terraform/azure/variables.tf` (+5/-0)
</details>

## #266 Markdownlint
**State:** MERGED | **Author:** @arriven | **Date:** 2022-03-09 | **Branch:** markdownlint → main | **+135/-103** | **Files:** 13

> # Description
> 
> Add ci job to lint markdown files in the repo. Will update with fixes before merging
> 
> ## Type of change
> 
> Please delete options that are not relevant.
> 
> - [ ] New feature (non-breaking change which adds functionality)
> 
> ## How Has This Been Tested?
> 
> Please describe the tests...

<details><summary>Files changed (13)</summary>

- `.github/workflows/markdownlint.yaml` (+30/-0)
- `.mdlrc` (+1/-0)
- `FAQ.md` (+12/-17)
- `README-ua.md` (+24/-22)
- `README.md` (+24/-22)
- `docs/advanced-users-and-devs.md` (+4/-4)
- `docs/azure-vpn-ua.md` (+4/-4)
- `docs/prometheus.md` (+1/-1)
- `docs/system-pages/vpn.md` (+18/-16)
- `kubernetes/helm-charts/README.md` (+1/-1)
- `kubernetes/manifests/README.md` (+2/-2)
- `src/dnsblast/README.md` (+13/-13)
- `terraform/heroku/README.md` (+1/-1)
</details>

## #263 Digital Ocean Terraform code to create multiple instances in multiple…
**State:** CLOSED | **Author:** @dddbbbsss | **Date:** 2022-03-09 | **Branch:** db1000n-01 → main | **+280/-0** | **Files:** 11

> Add version support

<details><summary>Comments (1)</summary>

- **@arriven** (2022-03-09): This PR is the same as #237  Please update that one instead
</details>

<details><summary>Files changed (11)</summary>

- `terraform/digital_ocean_ext/03-main.tf` (+20/-0)
- `terraform/digital_ocean_ext/img/SCR-20220306-sq0.png` (+0/-0)
- `terraform/digital_ocean_ext/img/SCR-20220306-sqw.png` (+0/-0)
- `terraform/digital_ocean_ext/module/do-512-ams.tf` (+54/-0)
- `terraform/digital_ocean_ext/module/script.sh` (+30/-0)
- `terraform/digital_ocean_ext/module/script.tpl` (+30/-0)
- `terraform/digital_ocean_ext/module/variables.tf` (+55/-0)
- `terraform/digital_ocean_ext/module/versions.tf` (+9/-0)
- `terraform/digital_ocean_ext/provider.tf` (+13/-0)
- `terraform/digital_ocean_ext/readme.md` (+59/-0)
- `terraform/digital_ocean_ext/variables.tf` (+10/-0)
</details>

## #262 Golangci lint
**State:** MERGED | **Author:** @arriven | **Date:** 2022-03-09 | **Branch:** golangci-lint → main | **+70/-8** | **Files:** 6

> # Description
> 
> Add golangci-lint action to automate linting and catch issues early
> 
> ## Type of change
> 
> Please delete options that are not relevant.
> 
> - [ ] New feature (non-breaking change which adds functionality)
> 
> ## How Has This Been Tested?
> 
> Please describe the tests that you ran to...

<details><summary>Files changed (6)</summary>

- `.gitattributes` (+1/-0)
- `.github/workflows/golangci-lint.yaml` (+49/-0)
- `main.go` (+3/-1)
- `src/metrics/prometheus.go` (+4/-1)
- `src/runner/runner.go` (+10/-4)
- `src/utils/crypto.go` (+3/-2)
</details>

## #261 Linter fixes
**State:** MERGED | **Author:** @arriven | **Date:** 2022-03-09 | **Branch:** linter-fixes → main | **+149/-85** | **Files:** 24

> # Description
> 
> Linter suggested fixes
> 
> ## Type of change
> 
> Please delete options that are not relevant.
> 
> - [ ] Bug fix (non-breaking change which fixes an issue)
> 
> ## How Has This Been Tested?
> 
> Please describe the tests that you ran to verify your changes. Provide instructions so we can...

<details><summary>Files changed (24)</summary>

- `main.go` (+1/-1)
- `src/dnsblast/dns-blast.go` (+14/-2)
- `src/dnsblast/dns-blast_test.go` (+10/-9)
- `src/dnsblast/dns-dhh.go` (+6/-2)
- `src/dnsblast/dns-dhh_test.go` (+1/-1)
- `src/dnsblast/qry/types.go` (+3/-0)
- `src/jobs/base.go` (+1/-0)
- `src/jobs/http.go` (+2/-1)
- `src/jobs/packetgen.go` (+4/-1)
- `src/jobs/rawnet.go` (+6/-2)
- `src/jobs/slowloris.go` (+2/-2)
- `src/metrics/metrics.go` (+38/-23)
- `src/metrics/prometheus.go` (+6/-5)
- `src/packetgen/packetgen.go` (+1/-0)
- `src/packetgen/utils.go` (+1/-0)
- `src/runner/config/config.go` (+1/-0)
- `src/runner/config/defaultconfig.go` (+1/-0)
- `src/runner/runner.go` (+1/-0)
- `src/slowloris/slowloris.go` (+13/-8)
- `src/utils/env.go` (+0/-11)
- `src/utils/panichandler.go` (+0/-9)
- `src/utils/statistics.go` (+5/-4)
- `src/utils/templates/templates.go` (+9/-4)
- `src/utils/utils.go` (+23/-0)
</details>

## #260 Add flag to enable pprof
**State:** MERGED | **Author:** @arriven | **Date:** 2022-03-09 | **Branch:** pprof → main | **+18/-0** | **Files:** 1

> # Description
> 
> Add flag to enable pprof if needed
> 
> ## Type of change
> 
> Please delete options that are not relevant.
> 
> - [ ] New feature (non-breaking change which adds functionality)
> 
> ## How Has This Been Tested?
> 
> Please describe the tests that you ran to verify your changes. Provide...

<details><summary>Files changed (1)</summary>

- `main.go` (+18/-0)
</details>

## #259 force resolve host to use ipv4
**State:** MERGED | **Author:** @arriven | **Date:** 2022-03-09 | **Branch:** force-ipv4-in-resolve-host → main | **+8/-7** | **Files:** 2

> # Description
> 
> force usage of ipv4 in `packetgen.ResolveHost`
> 
> ## Type of change
> 
> Please delete options that are not relevant.
> 
> - [ ] Bug fix (non-breaking change which fixes an issue)
> 
> ## How Has This Been Tested?
> 
> Please describe the tests that you ran to verify your changes. Provide...

<details><summary>Files changed (2)</summary>

- `src/packetgen/utils.go` (+6/-5)
- `testconfig.json` (+2/-2)
</details>

## #258 Minor packetgen improvements
**State:** MERGED | **Author:** @arriven | **Date:** 2022-03-09 | **Branch:** minor-packetgen-improvements → main | **+96/-105** | **Files:** 6

> # Description
> 
> Split opening raw connection from sending packets in packetgen. Move metrics out of the package to the job. Minor linter fixes
> 
> ## Type of change
> 
> Please delete options that are not relevant.
> 
> - [ ] Bug fix (non-breaking change which fixes an issue)
> 
> ## How Has This Been...

<details><summary>Files changed (6)</summary>

- `src/jobs/base.go` (+1/-1)
- `src/jobs/http.go` (+1/-2)
- `src/jobs/packetgen.go` (+34/-17)
- `src/packetgen/packetgen.go` (+48/-82)
- `src/packetgen/utils.go` (+10/-1)
- `testconfig.json` (+2/-2)
</details>

## #257 Optimize ResolveHost; remove regexp matching
**State:** MERGED | **Author:** @jdoe7865623 | **Date:** 2022-03-09 | **Branch:** cpu2 → main | **+5/-39** | **Files:** 2

<details><summary>Files changed (2)</summary>

- `src/packetgen/constants.go` (+0/-6)
- `src/packetgen/utils.go` (+5/-33)
</details>

## #256 Remove host regex matching in packetgen; add cpu profiling option
**State:** CLOSED | **Author:** @jdoe7865623 | **Date:** 2022-03-09 | **Branch:** cpu → main | **+19/-40** | **Files:** 3

> This generates about 1.5x more traffic with the current config

<details><summary>Comments (1)</summary>

- **@arriven** (2022-03-09): Can you split this into two separate PRs? host regex matching change seems like a no-brainer to accept but I have some suggestions about the CPU profile option and wouldn't want them to block that...
</details>

<details><summary>Files changed (3)</summary>

- `main.go` (+14/-1)
- `src/packetgen/constants.go` (+0/-6)
- `src/packetgen/utils.go` (+5/-33)
</details>

## #255 Improve docs a bit
**State:** MERGED | **Author:** @arriven | **Date:** 2022-03-09 | **Branch:** docs-polishing → main | **+96/-80** | **Files:** 15

> # Description
> 
> Improve docs a bit (formatting fixes + make it clearer to everyone what we do here)
> 
> ## Type of change
> 
> Please delete options that are not relevant.
> 
> - [x] Documentation update

<details><summary>Files changed (15)</summary>

- `.github/pull_request_template.md` (+3/-3)
- `FAQ.md` (+9/-10)
- `README-ua.md` (+4/-2)
- `README.md` (+4/-2)
- `docs/advanced-users-and-devs.md` (+0/-4)
- `docs/azure-vpn-ua.md` (+6/-4)
- `docs/config_encryption.md` (+27/-22)
- `docs/docker-vpn.md` (+2/-2)
- `docs/prometheus.md` (+19/-10)
- `kubernetes/manifests/README.md` (+1/-1)
- `terraform/aws/README.md` (+3/-3)
- `terraform/azure/README.md` (+11/-10)
- `terraform/digital_ocean/README.md` (+2/-2)
- `terraform/gcp_expressvpn/README.md` (+3/-3)
- `terraform/heroku/README.md` (+2/-2)
</details>

## #254 remove redundant resolve host from packetgen.SendPacket
**State:** MERGED | **Author:** @arriven | **Date:** 2022-03-09 | **Branch:** remove-resolve-host-from-packetgen → main | **+0/-4** | **Files:** 1

> # Description
> 
> With all the latest changes ResolveHost was there for purely cosmetic reasons. Thanks @jdoe7865623 for noticing!
> 
> ## Type of change
> 
> Please delete options that are not relevant.
> 
> - [ ] Bug fix (non-breaking change which fixes an issue)
> 
> # How Has This Been Tested?
> 
> Please...

<details><summary>Files changed (1)</summary>

- `src/packetgen/packetgen.go` (+0/-4)
</details>

## #253 allow setting system proxy override
**State:** MERGED | **Author:** @arriven | **Date:** 2022-03-09 | **Branch:** system-proxy-setting → main | **+37/-21** | **Files:** 9

> # Description
> 
> Allow setting system proxy override
> 
> Alternative to #207 
> 
> ## Type of change
> 
> Please delete options that are not relevant.
> 
> - [ ] New feature (non-breaking change which adds functionality)

<details><summary>Files changed (9)</summary>

- `main.go` (+8/-4)
- `src/jobs/base.go` (+6/-1)
- `src/jobs/dnsblast.go` (+1/-1)
- `src/jobs/http.go` (+9/-4)
- `src/jobs/packetgen.go` (+1/-1)
- `src/jobs/rawnet.go` (+2/-2)
- `src/jobs/slowloris.go` (+1/-1)
- `src/runner/config/config.go` (+2/-1)
- `src/runner/runner.go` (+7/-6)
</details>

## #252 Expose ResolveHost to template engine
**State:** MERGED | **Author:** @arriven | **Date:** 2022-03-09 | **Branch:** more-templates-and-cleanup → main | **+7/-44** | **Files:** 5

> # Description
> 
> Expose packetgen.ResolveHost to the templating engine
> 
> ## Type of change
> 
> Please delete options that are not relevant.
> 
> - [ ] New feature (non-breaking change which adds functionality)
> 
> # How Has This Been Tested?
> 
> Please describe the tests that you ran to verify your...

<details><summary>Files changed (5)</summary>

- `src/jobs/packetgen.go` (+1/-1)
- `src/packetgen/packetgen.go` (+1/-1)
- `src/packetgen/utils.go` (+2/-40)
- `src/utils/templates/templates.go` (+1/-0)
- `testconfig.json` (+2/-2)
</details>

## #251 Fix random ip to not produce invalid IPs
**State:** MERGED | **Author:** @arriven | **Date:** 2022-03-09 | **Branch:** fix-random-ip → main | **+2/-2** | **Files:** 1

> # Description
> 
> It took me couple days to realize that most of the time when packetgen is bitching about and argument in sendmsg it doesn't like the ip containing leading 0. Tweaked random IP generation function to stop producing those value
> 
> Fixes #249 
> 
> ## Type of change
> 
> Please delete...

<details><summary>Files changed (1)</summary>

- `src/packetgen/utils.go` (+2/-2)
</details>

## #250 Expose network settings in packetgen
**State:** MERGED | **Author:** @arriven | **Date:** 2022-03-09 | **Branch:** packetgen-expose-network-settings → main | **+27/-19** | **Files:** 2

> # Description
> 
> Make it possible to set parameters of raw network packetgen should use to send packets
> 
> ## Type of change
> 
> Please delete options that are not relevant.
> 
> - [ ] New feature (non-breaking change which adds functionality)

<details><summary>Files changed (2)</summary>

- `src/jobs/packetgen.go` (+12/-0)
- `src/packetgen/packetgen.go` (+15/-19)
</details>

## #246 Fix proxylist
**State:** MERGED | **Author:** @arriven | **Date:** 2022-03-08 | **Branch:** fix-proxylist → main | **+21/-27** | **Files:** 4

> # Description
> 
> Fixed proxylist parsing
> 
> Fixes #243 
> 
> ## Type of change
> 
> Please delete options that are not relevant.
> 
> - [ ] Bug fix (non-breaking change which fixes an issue)

<details><summary>Files changed (4)</summary>

- `src/jobs/http.go` (+14/-26)
- `src/utils/templates/templates.go` (+4/-0)
- `testconfig.json` (+1/-1)
- `testconfig.yaml` (+2/-0)
</details>

## #245 Add basic auth and tls support for prometheus exporter
**State:** MERGED | **Author:** @Lagovas | **Date:** 2022-03-08 | **Branch:** lagovas/https-and-basic-auth-for-push-gateways → main | **+156/-7** | **Files:** 5

> # Description
> * TLS support for prometheus push exporter
> * embed basic auth credentials and use authentication for prometheus push exporter
> * optionally use embedded CA used to verify TLS connection with push gateways
> * update Makefile with target to encrypt CA and embed to binary
> * document...

<details><summary>Files changed (5)</summary>

- `Makefile` (+18/-3)
- `docs/prometheus.md` (+65/-0)
- `src/metrics/prometheus.go` (+70/-1)
- `src/runner/config/config.go` (+1/-1)
- `src/utils/crypto.go` (+2/-2)
</details>

## #242 Use system http proxy by default
**State:** MERGED | **Author:** @arriven | **Date:** 2022-03-08 | **Branch:** use-system-http-proxy-by-default → main | **+1/-4** | **Files:** 1

> # Description
> 
> Use system proxy settings if no proxylist is provided in the job definition
> 
> Fixes #241 
> 
> ## Type of change
> 
> Please delete options that are not relevant.
> 
> - [ ] New feature (non-breaking change which adds functionality)

<details><summary>Files changed (1)</summary>

- `src/jobs/http.go` (+1/-4)
</details>

## #240 Separate parse and execute mapstruct
**State:** MERGED | **Author:** @arriven | **Date:** 2022-03-08 | **Branch:** separate-parse-and-execute-mapstruct → main | **+46/-4** | **Files:** 2

> # Description
> 
> Split parse and execute of templates in packetgen for performance (again, see switch to yaml as to when it was temporarily removed)
> 
> ## Type of change
> 
> Please delete options that are not relevant.
> 
> - [ ] Bug fix (non-breaking change which fixes an issue)

<details><summary>Files changed (2)</summary>

- `src/jobs/packetgen.go` (+8/-2)
- `src/utils/templates/templates.go` (+38/-2)
</details>

## #239 Allow encrypted configuration files
**State:** MERGED | **Author:** @Lagovas | **Date:** 2022-03-08 | **Branch:** lagovas/encrypt-config → main | **+235/-430** | **Files:** 8

> # Description
> 
> New features:
> * encryption/decryption configuration files with `make`
> * decryption encrypted configuration files with different encryption keys
> * embedding into binary default configuration file in encrypted or decrypted format
> * embedding default encryption keys into binary...

<details><summary>Files changed (8)</summary>

- `Dockerfile` (+2/-1)
- `Makefile` (+24/-1)
- `docs/config_encryption.md` (+108/-0)
- `go.mod` (+2/-1)
- `go.sum` (+10/-0)
- `src/runner/config/config.go` (+10/-2)
- `src/runner/config/defaultconfig.go` (+14/-425)
- `src/utils/crypto.go` (+65/-0)
</details>

## #238 Fix packetgen mapstructure
**State:** MERGED | **Author:** @arriven | **Date:** 2022-03-08 | **Branch:** fix-packetgen-mapstructure → main | **+109/-238** | **Files:** 14

> # Description
> 
> Fix packetgen to use mapstructure format
> 
> Fixes #234 
> 
> ## Type of change
> 
> Please delete options that are not relevant.
> 
> - [ ] Bug fix (non-breaking change which fixes an issue)

<details><summary>Files changed (14)</summary>

- `go.mod` (+1/-0)
- `go.sum` (+2/-0)
- `main.go` (+3/-0)
- `src/jobs/base.go` (+4/-5)
- `src/jobs/dnsblast.go` (+7/-7)
- `src/jobs/http.go` (+22/-195)
- `src/jobs/packetgen.go` (+6/-12)
- `src/jobs/rawnet.go` (+3/-3)
- `src/jobs/slowloris.go` (+2/-2)
- `src/packetgen/packetgen.go` (+8/-8)
- `src/runner/config/config.go` (+18/-5)
- `src/runner/runner.go` (+4/-1)
- `src/utils/templates/templates.go` (+16/-0)
- `testconfig.yaml` (+13/-0)
</details>

## #237 Digital Ocean Terraform code to create multiple instances in multiple… `[triage needed]`
**State:** OPEN | **Author:** @dddbbbsss | **Date:** 2022-03-13 | **Branch:** db1000n → main | **+280/-0** | **Files:** 11

> This module creates a number of servers in each of provided region. If you set `count = 2` and regions = ["nyc1", "nyc2", "nyc3"] this will create six servers total. Two servers in each of regions. See readme.txt for more details.

<details><summary>Comments (4)</summary>

- **@arriven** (2022-03-08): as discussed somewhere previously - can you please get someone (ideally at least 2 people) to validate your instruction and modules before I merge it?
- **@dddbbbsss** (2022-03-09): Unfortunately, I can't ask someone to validate. But it is easy read code without any hidden catch.
- **@arriven** (2022-03-09): I don't mean to indicate your code might be doing something suspicious, just that I'm trying to test every change going in the repo to improve stability but in order to test out changes to cloud...
- **@arfgdev** (2022-03-13): I have tried to run it but got  ``` tag not found: GET https://api.digitalocean.com/v2/tags/stop-sites: 404 (request "xxxxxx-17e5-4dca-bf45-xxxxxxx") The resource you were accessing could not be...
</details>

<details><summary>Files changed (11)</summary>

- `terraform/digital_ocean_ext/03-main.tf` (+20/-0)
- `terraform/digital_ocean_ext/img/SCR-20220306-sq0.png` (+0/-0)
- `terraform/digital_ocean_ext/img/SCR-20220306-sqw.png` (+0/-0)
- `terraform/digital_ocean_ext/module/do-512-ams.tf` (+54/-0)
- `terraform/digital_ocean_ext/module/script.sh` (+30/-0)
- `terraform/digital_ocean_ext/module/script.tpl` (+30/-0)
- `terraform/digital_ocean_ext/module/variables.tf` (+55/-0)
- `terraform/digital_ocean_ext/module/versions.tf` (+9/-0)
- `terraform/digital_ocean_ext/provider.tf` (+13/-0)
- `terraform/digital_ocean_ext/readme.md` (+59/-0)
- `terraform/digital_ocean_ext/variables.tf` (+10/-0)
</details>

## #236 (WIP) Use mapstruct for job args where possible
**State:** MERGED | **Author:** @arriven | **Date:** 2022-03-08 | **Branch:** yaml-config → main | **+89/-227** | **Files:** 13

> # Description
> 
> I want to add support for yaml based config to this app to support better templating. This is a first step. Still need to fix proxylist in http job and packetgen

<details><summary>Files changed (13)</summary>

- `go.mod` (+1/-0)
- `go.sum` (+2/-0)
- `main.go` (+3/-0)
- `src/jobs/base.go` (+4/-5)
- `src/jobs/dnsblast.go` (+7/-7)
- `src/jobs/http.go` (+22/-195)
- `src/jobs/packetgen.go` (+2/-1)
- `src/jobs/rawnet.go` (+3/-3)
- `src/jobs/slowloris.go` (+2/-2)
- `src/packetgen/packetgen.go` (+8/-8)
- `src/runner/config/config.go` (+18/-5)
- `src/runner/runner.go` (+4/-1)
- `testconfig.yaml` (+13/-0)
</details>

## #235 Don't take into account failed to send requests; cleanup some logs
**State:** MERGED | **Author:** @jdoe7865623 | **Date:** 2022-03-08 | **Branch:** cleanup → main | **+64/-68** | **Files:** 8

<details><summary>Files changed (8)</summary>

- `main.go` (+0/-1)
- `src/jobs/base.go` (+2/-2)
- `src/jobs/dnsblast.go` (+0/-1)
- `src/jobs/http.go` (+20/-22)
- `src/jobs/packetgen.go` (+1/-9)
- `src/jobs/rawnet.go` (+5/-3)
- `src/runner/config/config.go` (+30/-29)
- `src/runner/runner.go` (+6/-1)
</details>

## #233 add insta and fb
**State:** MERGED | **Author:** @iamtodor | **Date:** 2022-03-08 | **Branch:** add_contancts → main | **+2/-0** | **Files:** 1

> # Description
> 
> Please include a summary of the change and which issue is fixed. Please also include relevant motivation and context. List any dependencies that are required for this change.
> 
> Fixes # (issue)
> 
> ## Type of change
> add links to FB and insta
> Please delete options that are not...

<details><summary>Files changed (1)</summary>

- `README.md` (+2/-0)
</details>

## #232 support proxying in fast https
**State:** MERGED | **Author:** @arriven | **Date:** 2022-03-08 | **Branch:** fasthttp-proxy → main | **+21/-9** | **Files:** 3

> # Description
> 
> Added http proxies support to fasthttp job

<details><summary>Files changed (3)</summary>

- `go.mod` (+1/-0)
- `go.sum` (+1/-0)
- `src/jobs/http.go` (+19/-9)
</details>

## #230 remove async from http job (ineffective)
**State:** MERGED | **Author:** @arriven | **Date:** 2022-03-08 | **Branch:** remove-async-http → main | **+29/-16** | **Files:** 1

> # Description
> 
> Async mode in http job causes more problems than benefits. Bombardier and other tools use set amount of connections and this was already achievable long ago by setting "count" on a job

<details><summary>Files changed (1)</summary>

- `src/jobs/http.go` (+29/-16)
</details>

## #229 Fasthttp
**State:** MERGED | **Author:** @arriven | **Date:** 2022-03-08 | **Branch:** fasthttp → main | **+284/-6** | **Files:** 7

> # Description
> 
> Add fasthttp job which utilizes resources better

<details><summary>Files changed (7)</summary>

- `benchmarking/benchserver.go` (+46/-0)
- `benchmarking/go.mod` (+17/-0)
- `benchmarking/go.sum` (+40/-0)
- `go.mod` (+6/-2)
- `go.sum` (+13/-4)
- `src/jobs/base.go` (+1/-0)
- `src/jobs/http.go` (+161/-0)
</details>

## #228 Avoid pushing metrics with empty string for push gateways
**State:** CLOSED | **Author:** @Lagovas | **Date:** 2022-03-08 | **Branch:** lagovas/prometheus-metrics → main | **+3/-3** | **Files:** 2

> # Description
> 
> `""` value splitted by delimiter returns `[""]` value and miss `len(var) == 0` check. So added extra check to handle this case.
> 
> ## Type of change
> 
> Please delete options that are not relevant.
> 
> - [+] Bug fix (non-breaking change which fixes an issue)

<details><summary>Comments (1)</summary>

- **@arriven** (2022-03-08): Fixed in https://github.com/Arriven/db1000n/commit/737bf6b891068a799de23b6f8d3d770e61ad3ff5
</details>

<details><summary>Files changed (2)</summary>

- `main.go` (+1/-2)
- `src/metrics/prometheus.go` (+2/-1)
</details>

## #227 Don't use randomed values in packetgen metrics
**State:** MERGED | **Author:** @arriven | **Date:** 2022-03-08 | **Branch:** fix-prometheus-packetgen → main | **+3/-4** | **Files:** 1

> # Description
> 
> One of prometheus metrics was gathering too much randomized attack data
> 
> Fixes #225 
> 
> ## Type of change
> 
> Please delete options that are not relevant.
> 
> - [ ] Bug fix (non-breaking change which fixes an issue)

<details><summary>Files changed (1)</summary>

- `src/packetgen/packetgen.go` (+3/-4)
</details>

## #226 Fix memory leak for the non-closed response body
**State:** CLOSED | **Author:** @sivillakonski | **Date:** 2022-03-08 | **Branch:** main → main | **+4/-2** | **Files:** 1

> Addressing the issue: https://github.com/Arriven/db1000n/issues/225
> References:
> * http://devs.cloudimmunity.com/gotchas-and-common-mistakes-in-go-golang/index.html#close_http_resp_body
> 
> Stay safe, take care, and benchmark only appropriate resources (that you own).

<details><summary>Comments (2)</summary>

- **@arriven** (2022-03-08): While this does seem like a good change I'm not convinced it would fix a memory leak (the only way it would be a leak is if metrics were to panic but that should've been visible on logs. There should...
- **@arriven** (2022-03-08): The original memory issue was completely different but I've also implemented alternative http job that uses fasthttp and is a lot more effective. For now it's possible to use both of them but I plan...
</details>

<details><summary>Files changed (1)</summary>

- `src/jobs/http.go` (+4/-2)
</details>

## #220 Move config out
**State:** MERGED | **Author:** @arriven | **Date:** 2022-03-07 | **Branch:** move-config-out → main | **+126/-167** | **Files:** 5

> # Description
> 
> Move config related functionality from runner into an existing package
> 
> ## Type of change
> 
> Please delete options that are not relevant.
> 
> - [ ] Bug fix (non-breaking change which fixes an issue)

<details><summary>Files changed (5)</summary>

- `main.go` (+3/-2)
- `src/config/config.go` (+0/-63)
- `src/runner/config/config.go` (+95/-0)
- `src/runner/config/defaultconfig.go` (+0/-0)
- `src/runner/runner.go` (+28/-102)
</details>

## #219 Add prometheus metrics support
**State:** MERGED | **Author:** @Lagovas | **Date:** 2022-03-07 | **Branch:** lagovas/prometheus-metrics → main | **+858/-28** | **Files:** 12

> # Description
> 
> Added exporting prometheus metrics that can export as HTTP server to pull metrics on `http://0.0.0.0:9090/metrics` or pushing to specified push gateways.
> New parameters:
> - `prometheus_on` - turn on exporting via HTTP server
> - `prometheus_gateways` - list with comma separated...

<details><summary>Files changed (12)</summary>

- `go.mod` (+9/-1)
- `go.sum` (+433/-0)
- `main.go` (+16/-5)
- `src/dnsblast/dns-blast.go` (+16/-2)
- `src/dnsblast/dns-blast_test.go` (+19/-0)
- `src/jobs/http.go` (+3/-0)
- `src/jobs/rawnet.go` (+22/-13)
- `src/metrics/prometheus.go` (+245/-0)
- `src/packetgen/packetgen.go` (+62/-1)
- `src/runner/runner.go` (+11/-4)
- `src/slowloris/slowloris.go` (+11/-2)
- `src/utils/env.go` (+11/-0)
</details>

## #218 Separate template parsing and execution in packetgen
**State:** MERGED | **Author:** @jdoe7865623 | **Date:** 2022-03-07 | **Branch:** packetgen → main | **+8/-12** | **Files:** 1

> # Description
> 
> Template parsing is an expensive operation; now it happens on packetgen job init.

<details><summary>Files changed (1)</summary>

- `src/jobs/packetgen.go` (+8/-12)
</details>

## #215 [bug] aws terraform state fix
**State:** MERGED | **Author:** @golubovskyi | **Date:** 2022-03-07 | **Branch:** patch-2 → main | **+1/-1** | **Files:** 1

> # Description
> 
> Small fix to prevent terraform state refreshing warning.
> 
> ```
> aws_autoscaling_group.example: Refreshing state... [id=ir_db1000n]
> 
> Note: Objects have changed outside of Terraform
> 
> Terraform detected the following changes made outside of Terraform since the last "terraform...

<details><summary>Comments (1)</summary>

- **@golubovskyi** (2022-03-07): @Arriven actually it is related to inline_policy usage and there are a lot of issues in aws provider about...
</details>

<details><summary>Files changed (1)</summary>

- `terraform/aws/main.tf` (+1/-1)
</details>

## #213 Changed aws ec2 to spot instances
**State:** MERGED | **Author:** @golubovskyi | **Date:** 2022-03-07 | **Branch:** patch-1 → main | **+3/-0** | **Files:** 1

> A Spot Instance is an instance that uses spare EC2 capacity that is available for less than the On-Demand price.
> 
> We can use this type because it's safe and even good to recreate instances in our case (new external IP and latest docker image).

<details><summary>Comments (1)</summary>

- **@arriven** (2022-03-07): It would be nice to apply this to other providers as well (I know gke has similar thing called preemptive pools)
</details>

<details><summary>Files changed (1)</summary>

- `terraform/aws/main.tf` (+3/-0)
</details>

## #212 use source for installation through script
**State:** MERGED | **Author:** @olegykz | **Date:** 2022-03-07 | **Branch:** issue/readme-adjustment → main | **+1/-1** | **Files:** 1

> # Description
> 
> Fixes https://github.com/Arriven/db1000n/issues/211
> 
> ## Type of change
> 
> Please delete options that are not relevant.
> 
> - [ ] Bug fix (non-breaking change which fixes an issue)
> - [ ] New feature (non-breaking change which adds functionality)
> - [ ] Breaking change (fix or...

<details><summary>Files changed (1)</summary>

- `docs/advanced-users-and-devs.md` (+1/-1)
</details>

## #209 Split template parsing and execution in rawnet; tidy up http job a bit
**State:** MERGED | **Author:** @jdoe7865623 | **Date:** 2022-03-07 | **Branch:** rawnet → main | **+87/-71** | **Files:** 2

> # Description
> 
> Template parsing is an expensive operation; now it happens on rawnet job init.
> 
> ## Type of change
> 
> - [ ] Bug fix (non-breaking change which fixes an issue)

<details><summary>Files changed (2)</summary>

- `src/jobs/http.go` (+62/-61)
- `src/jobs/rawnet.go` (+25/-10)
</details>

## #207 Added global http proxy argument for using with tor in k8s or in dock…
**State:** CLOSED | **Author:** @lollypot | **Date:** 2022-03-10 | **Branch:** main → main | **+39/-12** | **Files:** 9

> Now you can set -http-proxy 172.17.0.1:8080 as argument and use tor for http runner

<details><summary>Comments (2)</summary>

- **@arriven** (2022-03-07): I like the idea, but we need to implement this a bit differently to have better maintainability. Can you pass this parameter to the http job directly instead of changing json representation...
- **@lollypot** (2022-03-08): @Arriven reworked in more universal way
</details>

<details><summary>Files changed (9)</summary>

- `main.go` (+3/-0)
- `src/jobs/base.go` (+6/-1)
- `src/jobs/dnsblast.go` (+1/-1)
- `src/jobs/http.go` (+19/-4)
- `src/jobs/packetgen.go` (+1/-1)
- `src/jobs/rawnet.go` (+2/-2)
- `src/jobs/slowloris.go` (+1/-1)
- `src/runner/config/config.go` (+2/-1)
- `src/runner/runner.go` (+4/-1)
</details>

## #205 Added mirrors for config.
**State:** CLOSED | **Author:** @Devaniti | **Date:** 2022-12-27 | **Branch:** ConfigMirror → main | **+1/-1** | **Files:** 1

> # Description
> 
> Added mirrors for config files, in case Russia blocks github, so RU VPN users can still load config
> 
> Related to #204
> Not closing since we may also add non git mirrors
> 
> ## Type of change
> 
> Added additional links to mirrors of config files
> 
> # How Has This Been...

<details><summary>Comments (6)</summary>

- **@exsesx** (2022-03-07): Do these configurations merge into one? I mean, if the same address and method are described in several configs, what will be the behavior?
- **@arriven** (2022-03-07): @exsesx the way this commandline argument works is it allows you to specify mirror configs (i.e. if one is unavailable - try net one and so on) We're discussing the best approach to manage actual...
- **@Devaniti** (2022-03-07): For the record, that 2 mirrors are automatically updated when main config updates
- **@bitshape** (2022-03-07): @Arriven @Devaniti do you have any thoughts on fingerprinting of mirror configs to prevent rogue .conf poisoning?
- **@Devaniti** (2022-03-08): @Arriven https://github.com/Arriven/db1000n/pull/205#issuecomment-1061062692
- **@Devaniti** (2022-12-27): Closing since I no longer maintain those mirrors. If in the future mirrors will be needed, I can start maintaining them again. But before that we need some kind of configuration signing and...
</details>

<details><summary>Files changed (1)</summary>

- `main.go` (+1/-1)
</details>

## #203 Dynamic job filtering
**State:** MERGED | **Author:** @arriven | **Date:** 2022-03-07 | **Branch:** dynamic-job-filtering → main | **+31/-19** | **Files:** 7

> # Description
> 
> Added optional dynamic filter to jobs to be able to disable some jobs to some random clients to have more diverse traffic
> 
> ## Type of change
> 
> Please delete options that are not relevant.
> 
> - [ ] Bug fix (non-breaking change which fixes an issue)
> - [X] New feature...

<details><summary>Files changed (7)</summary>

- `src/jobs/base.go` (+4/-3)
- `src/jobs/http.go` (+3/-3)
- `src/jobs/packetgen.go` (+3/-3)
- `src/jobs/rawnet.go` (+4/-4)
- `src/runner/runner.go` (+7/-2)
- `src/utils/templates/templates.go` (+9/-4)
- `testconfig.json` (+1/-0)
</details>

## #202 Remove synflood (use packetgen instead)
**State:** MERGED | **Author:** @arriven | **Date:** 2022-03-07 | **Branch:** remove-synflood → main | **+1/-337** | **Files:** 8

> # Description
> 
> Removing synflood job and package. I used it as a base to create packetgen which fully covers synflood use-case but is also configurable to do a lot more. Note: neither of current default configs use synflood so this is rather safe to remove.
> 
> ## Type of change
> 
> Please delete...

<details><summary>Files changed (8)</summary>

- `go.mod` (+1/-5)
- `go.sum` (+0/-12)
- `src/jobs/base.go` (+0/-1)
- `src/jobs/synflood.go` (+0/-40)
- `src/synfloodraw/constants.go` (+0/-10)
- `src/synfloodraw/synfloodraw.go` (+0/-171)
- `src/synfloodraw/utils.go` (+0/-89)
- `testconfig.json` (+0/-9)
</details>

## #198 bring back default for attack env variable
**State:** MERGED | **Author:** @arriven | **Date:** 2022-03-07 | **Branch:** fix-azure-terraform → main | **+3/-1** | **Files:** 1

> # Description
> 
> This default was mistakenly removed during docs refactoring.
> 
> Fixes #195 
> 
> ## Type of change
> 
> Please delete options that are not relevant.
> 
> - [x] Bug fix (non-breaking change which fixes an issue)
> - [ ] New feature (non-breaking change which adds functionality)
> - [ ]...

<details><summary>Files changed (1)</summary>

- `terraform/azure/bomblet/variables.tf` (+3/-1)
</details>

## #197 Refactor TCP-TLS connection to bypass filtering based on SSL fingerprinting
**State:** MERGED | **Author:** @sivillakonski | **Date:** 2022-03-07 | **Branch:** main → main | **+208/-81** | **Files:** 8

> # Description
> 
> Refactor TCP over TLS connections to bypass SSL fingerprinting. This update brings a refactoring for two benchmarking jobs:
> * SlowLoris
> * DNSBlast
> 
> Research:
> * https://habr.com/ru/post/596411/
> * https://www.ietf.org/proceedings/91/slides/slides-91-dprive-5.pdf
> *...

<details><summary>Files changed (8)</summary>

- `go.mod` (+1/-0)
- `go.sum` (+2/-0)
- `src/dnsblast/README.md` (+12/-1)
- `src/dnsblast/dns-blast.go` (+106/-47)
- `src/dnsblast/dns-blast_test.go` (+76/-27)
- `src/jobs/dnsblast.go` (+5/-0)
- `src/slowloris/slowloris.go` (+5/-4)
- `testconfig.json` (+1/-2)
</details>

## #196 Q
**State:** CLOSED | **Author:** @mrAlexZT | **Date:** 2022-03-07 | **Branch:** main → main | **+112601/-0** | **Files:** 36

> # Description
> 
> Please include a summary of the change and which issue is fixed. Please also include relevant motivation and context. List any dependencies that are required for this change.
> 
> Fixes # (issue)
> 
> ## Type of change
> 
> Please delete options that are not relevant.
> 
> - [ ] Bug fix...

<details><summary>Files changed (36)</summary>

- `.github/workflows/gh-pages-deploy.yml` (+17/-0)
- `.github/workflows/gh-pages.yml` (+18/-0)
- `.github/workflows/release-binaries.yaml` (+37/-0)
- `.github/workflows/release-docker.yaml` (+36/-0)
- `.github/workflows/test.yaml` (+20/-0)
- `.gitignore` (+4/-0)
- `Dockerfile` (+15/-0)
- `Makefile` (+10/-0)
- `README.md` (+186/-0)
- `defaultconfig.go` (+427/-0)
- `go.mod` (+24/-0)
- `go.sum` (+78/-0)
- `helm/.helmignore` (+23/-0)
- `helm/Chart.yaml` (+12/-0)
- `helm/README.md` (+18/-0)
- `helm/templates/_helpers.tpl` (+62/-0)
- `helm/templates/deployment.yaml` (+46/-0)
- `helm/values.yaml` (+26/-0)
- `install.sh` (+38/-0)
- `k8s-manifest/00_db1000n_namespace.yaml` (+4/-0)
- `k8s-manifest/01_db1000n_deployment.yaml` (+27/-0)
- `logs/logs.go` (+51/-0)
- `main.go` (+644/-0)
- `metrics/metrics.go` (+96/-0)
- `packetgen/constants.go` (+6/-0)
- `packetgen/packetgen.go` (+203/-0)
- `packetgen/utils.go` (+172/-0)
- `proxylist.json` (+109104/-0)
- `site/assets/db1000n.wasm` (+0/-0)
- `site/assets/index.html` (+21/-0)
- `site/assets/wasm_exec.js` (+636/-0)
- `slowloris/slowloris.go` (+170/-0)
- `synfloodraw/constants.go` (+10/-0)
- `synfloodraw/synfloodraw.go` (+171/-0)
- `synfloodraw/utils.go` (+101/-0)
- `testconfig.json` (+88/-0)
</details>

## #193 Add VPN_CONFIG_PATTERN to be able to do random VPN selection
**State:** MERGED | **Author:** @bitshape | **Date:** 2022-03-07 | **Branch:** random-vpn → main | **+9/-9** | **Files:** 1

> # Description
> 
> I've made a couple of changes to `wfg/docker-openvpn-client` docker image that were successfully merged into main branch and got released as `v2.1.0`:
> 
> https://github.com/wfg/docker-openvpn-client/pull/51
> https://github.com/wfg/docker-openvpn-client/pull/52
> 
> This allows...

<details><summary>Files changed (1)</summary>

- `docker-compose.yml` (+9/-9)
</details>

## #192 Accumulate traffic over time in metrics
**State:** MERGED | **Author:** @arriven | **Date:** 2022-03-06 | **Branch:** fix-metrics → main | **+4/-32** | **Files:** 2

> # Description
> 
> Accumulate traffic over time in metrics. Trying to calculate traffic per second without proper tooling was not a best idea
> 
> Fixes #182 
> 
> ## Type of change
> 
> Please delete options that are not relevant.
> 
> - [*] Bug fix (non-breaking change which fixes an issue)
> - [ ] New...

<details><summary>Files changed (2)</summary>

- `src/metrics/metrics.go` (+0/-1)
- `src/runner/runner.go` (+4/-31)
</details>

## #188 Separate template parsing and execution
**State:** MERGED | **Author:** @jdoe7865623 | **Date:** 2022-03-06 | **Branch:** template → main | **+105/-52** | **Files:** 4

<details><summary>Files changed (4)</summary>

- `src/jobs/http.go` (+77/-39)
- `src/jobs/packetgen.go` (+3/-3)
- `src/jobs/rawnet.go` (+4/-4)
- `src/utils/templates/templates.go` (+21/-6)
</details>

## #187 CODEOWNERS, PR template
**State:** MERGED | **Author:** @Amet13 | **Date:** 2022-03-06 | **Branch:** main → main | **+143/-219** | **Files:** 23

> - PR template
> - CODEOWNERS
> - Cleanup

<details><summary>Comments (2)</summary>

- **@iamtodor** (2022-03-06): @Arriven may we ask with @Amet13 to have `Triage` role in the repo? According to...
- **@iamtodor** (2022-03-06): @Arriven relates to https://github.com/Arriven/db1000n/pull/187#pullrequestreview-901101286 as well
</details>

<details><summary>Files changed (23)</summary>

- `.github/CODEOWNERS` (+4/-0)
- `.github/pull_request_template.md` (+36/-0)
- `.github/workflows/test-installer.yaml` (+2/-2)
- `.github/workflows/test.yaml` (+2/-1)
- `FAQ.md` (+1/-1)
- `Makefile` (+0/-8)
- `docs/advanced-users-and-devs.md` (+4/-3)
- `docs/azure-vpn-ua.md` (+55/-61)
- `docs/docker-vpn.md` (+5/-104)
- `kubernetes/helm-charts/README.md` (+3/-3)
- `kubernetes/manifests/README.md` (+1/-1)
- `openvpn/.gitkeep` (+0/-0)
- `terraform/aws/README.md` (+0/-0)
- `terraform/aws/ireland.tfvars` (+0/-0)
- `terraform/aws/main.tf` (+0/-0)
- `terraform/aws/variables.tf` (+0/-0)
- `terraform/azure/README.md` (+21/-19)
- `terraform/azure/bomblet/main.tf` (+0/-1)
- `terraform/azure/bomblet/requirements.tf` (+1/-1)
- `terraform/azure/bomblet/variables.tf` (+5/-11)
- `terraform/azure/main.tf` (+1/-1)
- `terraform/azure/requirements.tf` (+1/-1)
- `terraform/azure/variables.tf` (+1/-1)
</details>

## #186 - Change DNS job to accept domain name instead of NS IP.
**State:** MERGED | **Author:** @AndriiChuzhynov | **Date:** 2022-03-06 | **Branch:** dns_dynamic_ns_resolution → main | **+40/-41** | **Files:** 4

> Job will query NS servers for this domain and send requests to all NS.
> - Removed "port" option, since all target services uses standard ports

<details><summary>Files changed (4)</summary>

- `src/dnsblast/README.md` (+1/-2)
- `src/dnsblast/dns-blast.go` (+28/-9)
- `src/dnsblast/dns-blast_test.go` (+2/-2)
- `src/jobs/dnsblast.go` (+9/-28)
</details>

## #185 Reload targets config each 30 minutes
**State:** CLOSED | **Author:** @synapse-unix | **Date:** 2022-03-06 | **Branch:** patch-1 → main | **+1/-1** | **Files:** 1

<details><summary>Comments (1)</summary>

- **@synapse-unix** (2022-03-06): I see we are wasting a lot of time reloading config each minute  > [INFO]  2022/03/06 16:10:52 [INFO] Attacking https://185.178.208.185:443 [INFO]  2022/03/06 16:11:36 [INFO] Attacking...
</details>

<details><summary>Files changed (1)</summary>

- `Dockerfile` (+1/-1)
</details>

## #184 add few question to faq
**State:** MERGED | **Author:** @iamtodor | **Date:** 2022-03-06 | **Branch:** faq_update → main | **+27/-0** | **Files:** 1

<details><summary>Files changed (1)</summary>

- `FAQ.md` (+27/-0)
</details>

## #181 Setup for github pages with vpn instructions.
**State:** MERGED | **Author:** @Devaniti | **Date:** 2022-03-06 | **Branch:** GithubPagesSetup → main | **+30/-685** | **Files:** 6

> @Arriven you'll need to enable github pages for it to work
> You should be able to do that here https://github.com/Arriven/db1000n/settings/pages
> Please select docs/ as root for pages when enabling
> You can also check how will it look here https://devaniti.github.io/db1000n/system-pages/vpn

<details><summary>Files changed (6)</summary>

- `docs/system-pages/vpn.md` (+29/-0)
- `site/assets/db1000n.wasm` (+0/-0)
- `site/assets/index.html` (+0/-21)
- `site/assets/vpn.html` (+0/-26)
- `site/assets/wasm_exec.js` (+0/-636)
- `src/utils/countrychecker.go` (+1/-2)
</details>

## #180 Use `docker run --rm -it --pull always ghcr.io/arriven/db1000n` command
**State:** MERGED | **Author:** @fetchdedafrombunker | **Date:** 2022-03-06 | **Branch:** patch-1 → main | **+1/-1** | **Files:** 1

<details><summary>Comments (2)</summary>

- **@iamtodor** (2022-03-06): @fetchdedafrombunker please provide the benefits of these flags. procs and cons
- **@fetchdedafrombunker** (2022-03-06): @iamtodor  `--rm` - removes the container after stop, immediately (no need to do the docker prune and other cleanup procedures) `-it` - print the container stdout interactively, allows to trace the...
</details>

<details><summary>Files changed (1)</summary>

- `README.md` (+1/-1)
</details>

## #179 update release links
**State:** MERGED | **Author:** @iamtodor | **Date:** 2022-03-06 | **Branch:** update_releases_to_current_version → main | **+10/-10** | **Files:** 2

<details><summary>Files changed (2)</summary>

- `README-ua.md` (+5/-5)
- `README.md` (+5/-5)
</details>

## #178 Add FAQ
**State:** MERGED | **Author:** @Amet13 | **Date:** 2022-03-06 | **Branch:** main → main | **+56/-226** | **Files:** 6

> Closes #170 
> 
> @Arriven @iamtodor let me know if we can add more info here

<details><summary>Comments (2)</summary>

- **@iamtodor** (2022-03-06): @Amet13 as for now it seems good for me. let's fix the checks
- **@iamtodor** (2022-03-06): @Amet13 altho, I advise leaving the link to FAQ.md in main README.md not just having standalone FAQ
</details>

<details><summary>Files changed (6)</summary>

- `.github/workflows/test-installer.yaml` (+2/-0)
- `FAQ.md` (+39/-0)
- `README-ua.md` (+7/-3)
- `README.md` (+7/-3)
- `docs/README.md` (+0/-219)
- `kubernetes/helm-charts/README.md` (+1/-1)
</details>

## #176 Update cloud defaults to point to advanced image
**State:** MERGED | **Author:** @arriven | **Date:** 2022-03-06 | **Branch:** docs-advanced → main | **+252/-25** | **Files:** 9

> Fix #175

<details><summary>Files changed (9)</summary>

- `docker-compose.yml` (+4/-5)
- `docs/README.md` (+219/-0)
- `docs/advanced-users-and-devs.md` (+6/-1)
- `docs/docker-vpn.md` (+7/-5)
- `kubernetes/helm-charts/values.yaml` (+3/-2)
- `kubernetes/manifests/daemonset.yaml` (+10/-9)
- `kubernetes/manifests/deployment.yaml` (+1/-1)
- `terraform/aws_ec2/main.tf` (+1/-1)
- `terraform/gcp_expressvpn/main.tf` (+1/-1)
</details>

## #173 Slowloris - handle config reload
**State:** MERGED | **Author:** @AndriiChuzhynov | **Date:** 2022-03-06 | **Branch:** slowloris_handle_config_reload → main | **+14/-10** | **Files:** 2

> Use stopChan to stop workers. 
> Send number "stop" signals according to configured workers

<details><summary>Files changed (2)</summary>

- `src/jobs/slowloris.go` (+2/-2)
- `src/slowloris/slowloris.go` (+12/-8)
</details>

## #172 Docker target with advanced config
**State:** MERGED | **Author:** @arriven | **Date:** 2022-03-06 | **Branch:** docker-advanced → main | **+52/-0** | **Files:** 2

<details><summary>Files changed (2)</summary>

- `.github/workflows/release-docker-advanced.yaml` (+43/-0)
- `Dockerfile` (+9/-0)
</details>

## #171 upd readme k8s cluster if namespace doesn't exist
**State:** MERGED | **Author:** @krotoveugene | **Date:** 2022-03-06 | **Branch:** k8s_readme_upd → main | **+2/-1** | **Files:** 1

<details><summary>Files changed (1)</summary>

- `kubernetes/helm-charts/README.md` (+2/-1)
</details>

## #169 Remove gcp-ua doc cause it's not working
**State:** MERGED | **Author:** @Amet13 | **Date:** 2022-03-06 | **Branch:** main → main | **+0/-199** | **Files:** 1

> As we didn't find original author of doc, removing it
> 
> Closes https://github.com/Arriven/db1000n/issues/146

<details><summary>Comments (1)</summary>

- **@Amet13** (2022-03-06): @Arriven @iamtodor as discussed here https://github.com/Arriven/db1000n/issues/146#issuecomment-1059794244 pinging both of you for this type of changes
</details>

<details><summary>Files changed (1)</summary>

- `docs/gcp-installation-ua.md` (+0/-199)
</details>

## #168 Heroku support
**State:** MERGED | **Author:** @Amet13 | **Date:** 2022-03-06 | **Branch:** heroku → main | **+130/-11** | **Files:** 12

> - add heroku support
> - add billing warning
> - fix kubernetes setup

<details><summary>Files changed (12)</summary>

- `Procfile` (+1/-0)
- `README-ua.md` (+2/-0)
- `README.md` (+2/-0)
- `kubernetes/helm-charts/Chart.yaml` (+0/-6)
- `kubernetes/helm-charts/values.yaml` (+3/-3)
- `terraform/digital_ocean/README.md` (+1/-1)
- `terraform/digital_ocean/variables.tf` (+2/-1)
- `terraform/heroku/README.md` (+32/-0)
- `terraform/heroku/main.tf` (+33/-0)
- `terraform/heroku/provider.tf` (+14/-0)
- `terraform/heroku/terraform.tfvars` (+7/-0)
- `terraform/heroku/variables.tf` (+33/-0)
</details>

## #167 Add free vpn source doc
**State:** MERGED | **Author:** @krotoveugene | **Date:** 2022-03-06 | **Branch:** add_free_vpn_source_doc → main | **+4/-0** | **Files:** 3

<details><summary>Files changed (3)</summary>

- `README-ua.md` (+1/-0)
- `README.md` (+1/-0)
- `site/assets/vpn.html` (+2/-0)
</details>

## #166 Add DNS Blast Job for DNS stress testing
**State:** MERGED | **Author:** @sivillakonski | **Date:** 2022-03-06 | **Branch:** main → main | **+678/-1** | **Files:** 12

> # DNS Blast
> 
> An adoption of DNS Stress tool to validate the DNS server throughput.
> Original source codes: [https://github.com/sandeeprenjith/dnsblast](https://github.com/sandeeprenjith/dnsblast).
> 
> Heavily relies on the idea of [Distinct Heavy Hitter...

<details><summary>Comments (3)</summary>

- **@sivillakonski** (2022-03-06): @AndriiChuzhynov , this is different from your approach as there is only one server is being benchmarked per job
- **@AndriiChuzhynov** (2022-03-06): Hi @sivillakonski what do you think about adding dynamic NS resolution?  Because some NS can change IP pretty fast.
- **@AndriiChuzhynov** (2022-03-06): @sivillakonski I can do dynamic resolution if you are not working on it right now
</details>

<details><summary>Files changed (12)</summary>

- `.gitignore` (+1/-1)
- `go.mod` (+4/-0)
- `go.sum` (+18/-0)
- `src/dnsblast/README.md` (+17/-0)
- `src/dnsblast/dns-blast.go` (+180/-0)
- `src/dnsblast/dns-blast_test.go` (+53/-0)
- `src/dnsblast/dns-dhh.go` (+87/-0)
- `src/dnsblast/dns-dhh_test.go` (+34/-0)
- `src/dnsblast/qry/types.go` (+168/-0)
- `src/jobs/base.go` (+1/-0)
- `src/jobs/dnsblast.go` (+102/-0)
- `testconfig.json` (+13/-0)
</details>

## #164 Use last known good config if new config can't be loaded
**State:** MERGED | **Author:** @bitshape | **Date:** 2022-03-06 | **Branch:** keep-config → main | **+7/-1** | **Files:** 1

> Sometimes you get EOF errors while trying to update job definitions:
> 
> ```
> [INFO]  2022/03/06 01:37:50 [INFO] Loading config from "https://raw.githubusercontent.com/db1000n-coordinators/LoadTestConfig/main/config.json"
> [WARN]  2022/03/06 01:37:50 [WARN] Failed to fetch config from...

<details><summary>Files changed (1)</summary>

- `src/runner/runner.go` (+7/-1)
</details>

## #163 Remove built-in VPN tunnel
**State:** MERGED | **Author:** @bitshape | **Date:** 2022-03-06 | **Branch:** main → main | **+201/-186** | **Files:** 11

> I'm removing code I've introduced in https://github.com/Arriven/db1000n/pull/74 as I think that using `docker-compose` is more elegant solution and it's easier to work with.
> 
> @kraftwerk28 suggested to use `dperson/openvpn-client` for OpenVPN container in their PR...

<details><summary>Files changed (11)</summary>

- `Dockerfile` (+2/-20)
- `docker-compose.yml` (+96/-0)
- `docs/advanced-users-and-devs.md` (+1/-27)
- `docs/docker-vpn.md` (+102/-44)
- `run.sh` (+0/-15)
- `run/db1000n.sh` (+0/-13)
- `run/openvpn-up.sh` (+0/-7)
- `run/run-openvpn.sh` (+0/-41)
- `supervisord/supervisord-db1000n.conf` (+0/-7)
- `supervisord/supervisord-openvpn.conf` (+0/-7)
- `supervisord/supervisord.conf` (+0/-5)
</details>

## #161 fixed async
**State:** CLOSED | **Author:** @industral | **Date:** 2022-03-06 | **Branch:** async-fix → main | **+1/-5** | **Files:** 1

> fixed https://github.com/Arriven/db1000n/issues/133

<details><summary>Comments (3)</summary>

- **@jdoe7865623** (2022-03-06): You're basically making async non-configurable. Should this be fixed in configs instead?
- **@synapse-unix** (2022-03-06): @jdoe7865623 is right here. Can you check if we don;t have any leakage in go routine `go sendRequest()` itself. I create MR in config to add async where it was.
- **@arriven** (2022-03-06): I'll close this PR as async is meant to be configurable (see my comment on the linked issue)
</details>

<details><summary>Files changed (1)</summary>

- `src/jobs/http.go` (+1/-5)
</details>

## #160 add pull policy to docker run in order to use the very last container
**State:** MERGED | **Author:** @iamtodor | **Date:** 2022-03-06 | **Branch:** change_docker_command → main | **+1/-1** | **Files:** 1

<details><summary>Comments (1)</summary>

- **@arriven** (2022-03-06): Hmm, I thought I already added that, thanks for catching!
</details>

<details><summary>Files changed (1)</summary>

- `README.md` (+1/-1)
</details>

## #159 added get proxies by url function and proxies url argument
**State:** MERGED | **Author:** @arfgdev | **Date:** 2022-03-06 | **Branch:** proxy_url → main | **+37/-22** | **Files:** 2

> - added templating function `get_proxylist_by_url` to add ability to set separate proxies for each job
> - added `p` flag to set generic list of proxies
> 
> config example
> ```
> {
>       "type": "http",
>       "args": {
>         "method": "GET",
>         "path": "http://riabir.ru:443/",
>        ...

<details><summary>Files changed (2)</summary>

- `main.go` (+7/-0)
- `src/utils/templates/templates.go` (+30/-22)
</details>

## #158 #100 azure terraform with docker
**State:** MERGED | **Author:** @crabulik | **Date:** 2022-03-06 | **Branch:** #100_azure_terrafform_with_docker → main | **+198/-0** | **Files:** 7

> A multi region solution for deploying the db1000n container on Azure Container Group

<details><summary>Comments (1)</summary>

- **@crabulik** (2022-03-05): @Amet13 Done
</details>

<details><summary>Files changed (7)</summary>

- `terraform/azure/README.md` (+64/-0)
- `terraform/azure/bomblet/main.tf` (+19/-0)
- `terraform/azure/bomblet/requirements.tf` (+8/-0)
- `terraform/azure/bomblet/variables.tf` (+27/-0)
- `terraform/azure/main.tf` (+62/-0)
- `terraform/azure/requirements.tf` (+8/-0)
- `terraform/azure/variables.tf` (+10/-0)
</details>

## #156 azure-vpn-ua manual
**State:** MERGED | **Author:** @didgudan | **Date:** 2022-03-06 | **Branch:** main → main | **+114/-0** | **Files:** 18

> added a manual for creating a dedicated server on microsoft azure + vpn with pictures in ukrainian

<details><summary>Files changed (18)</summary>

- `docs/azure-vpn-ua-images/Screenshot_1.png` (+0/-0)
- `docs/azure-vpn-ua-images/Screenshot_10.png` (+0/-0)
- `docs/azure-vpn-ua-images/Screenshot_11.png` (+0/-0)
- `docs/azure-vpn-ua-images/Screenshot_12.png` (+0/-0)
- `docs/azure-vpn-ua-images/Screenshot_13.png` (+0/-0)
- `docs/azure-vpn-ua-images/Screenshot_14.png` (+0/-0)
- `docs/azure-vpn-ua-images/Screenshot_15.png` (+0/-0)
- `docs/azure-vpn-ua-images/Screenshot_16.png` (+0/-0)
- `docs/azure-vpn-ua-images/Screenshot_17.png` (+0/-0)
- `docs/azure-vpn-ua-images/Screenshot_2.png` (+0/-0)
- `docs/azure-vpn-ua-images/Screenshot_3.png` (+0/-0)
- `docs/azure-vpn-ua-images/Screenshot_4.png` (+0/-0)
- `docs/azure-vpn-ua-images/Screenshot_5.png` (+0/-0)
- `docs/azure-vpn-ua-images/Screenshot_6.png` (+0/-0)
- `docs/azure-vpn-ua-images/Screenshot_7.png` (+0/-0)
- `docs/azure-vpn-ua-images/Screenshot_8.png` (+0/-0)
- `docs/azure-vpn-ua-images/Screenshot_9.png` (+0/-0)
- `docs/azure-vpn-ua.md` (+114/-0)
</details>

## #155 Data source for tf aws linux ami
**State:** MERGED | **Author:** @nazariozad | **Date:** 2022-03-06 | **Branch:** main → main | **+10/-7** | **Files:** 3

<details><summary>Files changed (3)</summary>

- `terraform/aws_ec2/ireland.tfvars` (+0/-1)
- `terraform/aws_ec2/main.tf` (+10/-1)
- `terraform/aws_ec2/variables.tf` (+0/-5)
</details>

## #154 Move to default go log package
**State:** MERGED | **Author:** @jdoe7865623 | **Date:** 2022-03-06 | **Branch:** logs → main | **+250/-339** | **Files:** 21

<details><summary>Comments (1)</summary>

- **@arriven** (2022-03-06): There are merge conflicts in this. If I recall correctly your main concern is performance, can we maybe resort to switching the package inside logs implementation in order to minimize changes? I'd...
</details>

<details><summary>Files changed (21)</summary>

- `go.mod` (+0/-2)
- `go.sum` (+0/-12)
- `main.go` (+12/-13)
- `src/dnsblast/dns-blast.go` (+7/-9)
- `src/dnsblast/dns-blast_test.go` (+1/-4)
- `src/jobs/base.go` (+1/-3)
- `src/jobs/dnsblast.go` (+2/-3)
- `src/jobs/http.go` (+55/-35)
- `src/jobs/packetgen.go` (+25/-14)
- `src/jobs/rawnet.go` (+43/-23)
- `src/jobs/slowloris.go` (+9/-8)
- `src/jobs/synflood.go` (+11/-5)
- `src/logs/logs.go` (+0/-51)
- `src/packetgen/utils.go` (+12/-24)
- `src/runner/runner.go` (+35/-32)
- `src/slowloris/slowloris.go` (+13/-16)
- `src/synfloodraw/utils.go` (+7/-19)
- `src/utils/countrychecker.go` (+12/-11)
- `src/utils/dumpmetrics.go` (+0/-50)
- `src/utils/panichandler.go` (+2/-2)
- `src/utils/templates/templates.go` (+3/-3)
</details>

## #152 azure-vpn-ua manual
**State:** CLOSED | **Author:** @didgudan | **Date:** 2022-03-05 | **Branch:** main → main | **+114/-0** | **Files:** 18

> added a manual for creating a dedicated server on microsoft azure + vpn with pictures in ukrainian

<details><summary>Files changed (18)</summary>

- `docs/azure-vpn-ua-images/Screenshot_1.png` (+0/-0)
- `docs/azure-vpn-ua-images/Screenshot_10.png` (+0/-0)
- `docs/azure-vpn-ua-images/Screenshot_11.png` (+0/-0)
- `docs/azure-vpn-ua-images/Screenshot_12.png` (+0/-0)
- `docs/azure-vpn-ua-images/Screenshot_13.png` (+0/-0)
- `docs/azure-vpn-ua-images/Screenshot_14.png` (+0/-0)
- `docs/azure-vpn-ua-images/Screenshot_15.png` (+0/-0)
- `docs/azure-vpn-ua-images/Screenshot_16.png` (+0/-0)
- `docs/azure-vpn-ua-images/Screenshot_17.png` (+0/-0)
- `docs/azure-vpn-ua-images/Screenshot_2.png` (+0/-0)
- `docs/azure-vpn-ua-images/Screenshot_3.png` (+0/-0)
- `docs/azure-vpn-ua-images/Screenshot_4.png` (+0/-0)
- `docs/azure-vpn-ua-images/Screenshot_5.png` (+0/-0)
- `docs/azure-vpn-ua-images/Screenshot_6.png` (+0/-0)
- `docs/azure-vpn-ua-images/Screenshot_7.png` (+0/-0)
- `docs/azure-vpn-ua-images/Screenshot_8.png` (+0/-0)
- `docs/azure-vpn-ua-images/Screenshot_9.png` (+0/-0)
- `docs/azure-vpn-ua.md` (+114/-0)
</details>

## #151 Add DNS flood job
**State:** CLOSED | **Author:** @AndriiChuzhynov | **Date:** 2022-03-06 | **Branch:** main → main | **+215/-0** | **Files:** 8

> This is first iteration of DNS flood job.
> Based on dnsstresss.go but adapted to work with db1000n.
> Each job can be pointed on the resolver with multiple target domains, check testconfig.json
> May close #8

<details><summary>Comments (5)</summary>

- **@AndriiChuzhynov** (2022-03-05): Random subdomain may be a good idea https://github.com/galprz/dns-random-subdomains-ddos-attack
- **@arriven** (2022-03-06): @AndriiChuzhynov I went ahead with #166 instead, although I have a feeling that we can have both jobs even if they're doing similar things. We can always remove one of them later once we test both...
- **@AndriiChuzhynov** (2022-03-06): Hi @Arriven I'm ok with #166 but, I think, we need to add dynamic nameserver resolving.  Because NS servers IPs could change pretty fast this days
- **@arriven** (2022-03-06): Can you make an issue or PR for that?
- **@AndriiChuzhynov** (2022-03-06): closing in favor of #166
</details>

<details><summary>Files changed (8)</summary>

- `docs/configuration.md` (+6/-0)
- `go.mod` (+1/-0)
- `go.sum` (+18/-0)
- `src/dnsflood/dnsflood.go` (+112/-0)
- `src/jobs/base.go` (+1/-0)
- `src/jobs/dnsflood.go` (+27/-0)
- `src/utils/string_utils.go` (+21/-0)
- `testconfig.json` (+29/-0)
</details>

## #150 azure-vpn-ua
**State:** CLOSED | **Author:** @didgudan | **Date:** 2022-03-05 | **Branch:** main → main | **+114/-0** | **Files:** 18

> manual how to set up a dedicated server on microsoft azure + vpn with pictures

<details><summary>Files changed (18)</summary>

- `docs/azure-vpn-ua-images/Screenshot_1.png` (+0/-0)
- `docs/azure-vpn-ua-images/Screenshot_10.png` (+0/-0)
- `docs/azure-vpn-ua-images/Screenshot_11.png` (+0/-0)
- `docs/azure-vpn-ua-images/Screenshot_12.png` (+0/-0)
- `docs/azure-vpn-ua-images/Screenshot_13.png` (+0/-0)
- `docs/azure-vpn-ua-images/Screenshot_14.png` (+0/-0)
- `docs/azure-vpn-ua-images/Screenshot_15.png` (+0/-0)
- `docs/azure-vpn-ua-images/Screenshot_16.png` (+0/-0)
- `docs/azure-vpn-ua-images/Screenshot_17.png` (+0/-0)
- `docs/azure-vpn-ua-images/Screenshot_2.png` (+0/-0)
- `docs/azure-vpn-ua-images/Screenshot_3.png` (+0/-0)
- `docs/azure-vpn-ua-images/Screenshot_4.png` (+0/-0)
- `docs/azure-vpn-ua-images/Screenshot_5.png` (+0/-0)
- `docs/azure-vpn-ua-images/Screenshot_6.png` (+0/-0)
- `docs/azure-vpn-ua-images/Screenshot_7.png` (+0/-0)
- `docs/azure-vpn-ua-images/Screenshot_8.png` (+0/-0)
- `docs/azure-vpn-ua-images/Screenshot_9.png` (+0/-0)
- `docs/azure-vpn-ua.md` (+114/-0)
</details>

## #149 [Install script] Fix md5sum for macOS, test install script on CI, fail script in case of error
**State:** MERGED | **Author:** @Amet13 | **Date:** 2022-03-06 | **Branch:** main → main | **+41/-13** | **Files:** 4

> <img width="1000" alt="Screenshot 2022-03-05 at 18 32 26" src="https://user-images.githubusercontent.com/5184847/156892039-a1343246-1b99-4834-87de-589115f045c5.png">

<details><summary>Files changed (4)</summary>

- `.github/workflows/test.yaml` (+2/-0)
- `.gitignore` (+10/-4)
- `install.sh` (+25/-9)
- `run.sh` (+4/-0)
</details>

## #147 Remove two redundant docker layers
**State:** CLOSED | **Author:** @Amet13 | **Date:** 2022-03-05 | **Branch:** docker_layers → main | **+89/-4** | **Files:** 7

<details><summary>Files changed (7)</summary>

- `.gitignore` (+0/-1)
- `Dockerfile` (+1/-3)
- `terraform/digital_ocean/README.md` (+29/-0)
- `terraform/digital_ocean/main.tf` (+18/-0)
- `terraform/digital_ocean/provider.tf` (+13/-0)
- `terraform/digital_ocean/terraform.tfvars` (+3/-0)
- `terraform/digital_ocean/variables.tf` (+25/-0)
</details>

## #144 Add guide for VPN-in-docker
**State:** MERGED | **Author:** @kraftwerk28 | **Date:** 2022-03-05 | **Branch:** main → main | **+73/-0** | **Files:** 1

<details><summary>Files changed (1)</summary>

- `docs/docker-vpn.md` (+73/-0)
</details>

## #142 Digital Ocean setup + Docker optimization
**State:** MERGED | **Author:** @Amet13 | **Date:** 2022-03-05 | **Branch:** main → main | **+97/-8** | **Files:** 7

> Closes: https://github.com/Arriven/db1000n/issues/101
> Most of the code is from https://github.com/db1000n-coordinators/db1000n-infra, but cleaned up and tested
> 
> <img width="1114" alt="Screenshot 2022-03-05 at 15 33 55"...

<details><summary>Files changed (7)</summary>

- `.gitignore` (+0/-1)
- `Dockerfile` (+9/-7)
- `terraform/digital_ocean/README.md` (+29/-0)
- `terraform/digital_ocean/main.tf` (+18/-0)
- `terraform/digital_ocean/provider.tf` (+13/-0)
- `terraform/digital_ocean/terraform.tfvars` (+3/-0)
- `terraform/digital_ocean/variables.tf` (+25/-0)
</details>

## #141 Added supervisor to start script
**State:** MERGED | **Author:** @Devaniti | **Date:** 2022-03-05 | **Branch:** AddScriptSupervisor → main | **+8/-1** | **Files:** 1

> closes #123

<details><summary>Files changed (1)</summary>

- `scripts/StartDB1000N.bat` (+8/-1)
</details>

## #140 Implement job runner
**State:** MERGED | **Author:** @jdoe7865623 | **Date:** 2022-03-05 | **Branch:** runner → main | **+255/-46** | **Files:** 2

<details><summary>Files changed (2)</summary>

- `main.go` (+24/-46)
- `src/runner/runner.go` (+231/-0)
</details>

## #139 1
**State:** CLOSED | **Author:** @didgudan | **Date:** 2022-03-05 | **Branch:** main → main | **+114/-0** | **Files:** 18

> azure vm + vpn + db1000n manual and img

<details><summary>Comments (3)</summary>

- **@Amet13** (2022-03-05): Hey, @didgudan it looks very nice. Could you please rename file `azure-vpn-db1000n.md` to `azure-vpn-ua.md` to keep all docs in Ukraininan with `-ua` suffix? Could you also rename directory `img`...
- **@arriven** (2022-03-05): > Hey, @didgudan it looks very nice. > Could you please rename file `azure-vpn-db1000n.md` to `azure-vpn-ua.md` to keep all docs in Ukraininan with `-ua` suffix? > Could you also rename directory...
- **@didgudan** (2022-03-05): OK. now I will fork again, make all the edits and send the pull request again
</details>

<details><summary>Files changed (18)</summary>

- `docs/azure-vpn-db1000n.md` (+114/-0)
- `docs/img/Screenshot_1.png` (+0/-0)
- `docs/img/Screenshot_10.png` (+0/-0)
- `docs/img/Screenshot_11.png` (+0/-0)
- `docs/img/Screenshot_12.png` (+0/-0)
- `docs/img/Screenshot_13.png` (+0/-0)
- `docs/img/Screenshot_14.png` (+0/-0)
- `docs/img/Screenshot_15.png` (+0/-0)
- `docs/img/Screenshot_16.png` (+0/-0)
- `docs/img/Screenshot_17.png` (+0/-0)
- `docs/img/Screenshot_2.png` (+0/-0)
- `docs/img/Screenshot_3.png` (+0/-0)
- `docs/img/Screenshot_4.png` (+0/-0)
- `docs/img/Screenshot_5.png` (+0/-0)
- `docs/img/Screenshot_6.png` (+0/-0)
- `docs/img/Screenshot_7.png` (+0/-0)
- `docs/img/Screenshot_8.png` (+0/-0)
- `docs/img/Screenshot_9.png` (+0/-0)
</details>

## #138 Add supervisor for app restart after crash
**State:** CLOSED | **Author:** @5har0varik | **Date:** 2022-03-05 | **Branch:** iss_123 → main | **+5/-1** | **Files:** 1

> closes #123

<details><summary>Comments (4)</summary>

- **@arriven** (2022-03-05): @Devaniti can you take a quick look? it looks ok to me but I'd rather check with you until I get enough time to get fluent in that script
- **@Devaniti** (2022-03-05): On windows ctrl-c seems to generate non 0 exit code You can take a look at go code to make it return 0 in that case, and I'll write supervisor in that script in the meantime
- **@Devaniti** (2022-03-05): Oh wait, Ctrl+C stops whole batch script, so supervisor will not deadlock even if exit code is wrong
- **@Devaniti** (2022-03-05): I made another pull request, same idea, but with comments, without using start command (I guess it's my personal preference), and with graceful exit from script when app does graceful...
</details>

<details><summary>Files changed (1)</summary>

- `scripts/StartDB1000N.bat` (+5/-1)
</details>

## #135 Fix some misspells and misslinks in docs
**State:** MERGED | **Author:** @Amet13 | **Date:** 2022-03-05 | **Branch:** main → main | **+14/-14** | **Files:** 4

> Just went through all docs and fixed misspells and misslinks

<details><summary>Files changed (4)</summary>

- `README-ua.md` (+3/-3)
- `README.md` (+1/-1)
- `docs/advanced-users-and-devs.md` (+6/-6)
- `docs/configuration.md` (+4/-4)
</details>

## #134 Added comments to start script
**State:** MERGED | **Author:** @Devaniti | **Date:** 2022-03-05 | **Branch:** StartScriptsComments → main | **+12/-0** | **Files:** 1

> suggested by @Amet13

<details><summary>Files changed (1)</summary>

- `scripts/StartDB1000N.bat` (+12/-0)
</details>

## #130 Added script for one click start
**State:** MERGED | **Author:** @Devaniti | **Date:** 2022-03-05 | **Branch:** StartScript → main | **+28/-0** | **Files:** 1

<details><summary>Files changed (1)</summary>

- `scripts/StartDB1000N.bat` (+28/-0)
</details>

## #128 #118 PoC for doc structure
**State:** MERGED | **Author:** @Amet13 | **Date:** 2022-03-05 | **Branch:** n118 → main | **+491/-403** | **Files:** 23

> https://github.com/Arriven/db1000n/issues/118
> 
> See how it looks like: https://github.com/Amet13/db1000n-1/tree/n118

<details><summary>Comments (7)</summary>

- **@Amet13** (2022-03-05): Great!
- **@iamtodor** (2022-03-05): @Amet13 @Arriven please take a look on my comment above before merge it
- **@arriven** (2022-03-05): > @Amet13 @Arriven please take a look on my comment above before merge it  You sure you published that comment? I can't seem to find it
- **@Amet13** (2022-03-05): @iamtodor I already saw comments, they were marked as resolved automatically, probably.  Or you mean this one? https://github.com/Arriven/db1000n/issues/118#issuecomment-1059743788
- **@iamtodor** (2022-03-05): @Arriven @Amet13  <img width="616" alt="image" src="https://user-images.githubusercontent.com/12586108/156881380-b2227591-dd2a-4227-a6f3-1b70c60af4ff.png">
- **@Amet13** (2022-03-05): @iamtodor thanks. Fixed. We can't see it, because it's pending. You have to press review button to show the comment for everyone
- **@iamtodor** (2022-03-05): @Amet13 got you, didn't know that :)
</details>

<details><summary>Files changed (23)</summary>

- `README-ua.md` (+71/-0)
- `README.md` (+36/-280)
- `docs/advanced-users-and-devs.md` (+87/-0)
- `docs/configuration.md` (+100/-0)
- `docs/gcp-installation-ua.md` (+56/-76)
- `k8s-manifest/advanced/00_db1000n_namespace.yaml` (+0/-4)
- `k8s-manifest/simple/00_db1000n_namespace.yaml` (+0/-4)
- `kubernetes/helm-charts/.helmignore` (+0/-0)
- `kubernetes/helm-charts/Chart.yaml` (+0/-0)
- `kubernetes/helm-charts/README.md` (+11/-5)
- `kubernetes/helm-charts/templates/_helpers.tpl` (+0/-0)
- `kubernetes/helm-charts/templates/deployment.yaml` (+0/-0)
- `kubernetes/helm-charts/values.yaml` (+0/-0)
- `kubernetes/manifests/README.md` (+62/-0)
- `kubernetes/manifests/daemonset.yaml` (+7/-0)
- `kubernetes/manifests/deployment.yaml` (+7/-0)
- `terraform/aws_ec2/README.md` (+11/-8)
- `terraform/aws_ec2/ireland.tfvars` (+1/-1)
- `terraform/aws_ec2/main.tf` (+9/-8)
- `terraform/aws_ec2/variables.tf` (+3/-3)
- `terraform/gcp_expressvpn/README.md` (+21/-5)
- `terraform/gcp_expressvpn/main.tf` (+7/-7)
- `terraform/gcp_expressvpn/variables.tf` (+2/-2)
</details>

## #127 Update 01_db1000n_deployment.yaml
**State:** CLOSED | **Author:** @oleksdovz | **Date:** 2022-03-05 | **Branch:** patch-1 → main | **+2/-1** | **Files:** 1

> [Default image pull policy](https://kubernetes.io/docs/concepts/containers/images/#imagepullpolicy-defaulting)
> 
> When you (or a controller) submit a new Pod to the API server, your cluster sets the imagePullPolicy field when specific conditions are met:
> 
> if you omit the imagePullPolicy field,...

<details><summary>Comments (2)</summary>

- **@arriven** (2022-03-05): @oleksdovz #128 has changed the directory structure a bit, can you reapply your patch to resolve the conflict?
- **@arriven** (2022-03-05): Applied the patch manually
</details>

<details><summary>Files changed (1)</summary>

- `k8s-manifest/simple/01_db1000n_deployment.yaml` (+2/-1)
</details>

## #122 Add arm/v7 support for Docker images
**State:** MERGED | **Author:** @Amet13 | **Date:** 2022-03-05 | **Branch:** main → main | **+1/-1** | **Files:** 1

> Probably should fix https://github.com/Arriven/db1000n/issues/116
> 
> Available platforms:
> <img width="971" alt="Screenshot 2022-03-05 at 11 49 36" src="https://user-images.githubusercontent.com/5184847/156878047-ca4b3f91-e2df-4836-ad9b-aa00d5678e4f.png">
> 
> arm/v7 used for old raspberry:...

<details><summary>Files changed (1)</summary>

- `.github/workflows/release-docker.yaml` (+1/-1)
</details>

## #120 Code restructure
**State:** MERGED | **Author:** @arriven | **Date:** 2022-03-05 | **Branch:** code-restructure → main | **+243/-202** | **Files:** 23

> Move some code a bit to reduce chance of merge conflicts for contributors
> 
> Fix #119

<details><summary>Files changed (23)</summary>

- `main.go` (+13/-152)
- `src/config/config.go` (+63/-0)
- `src/config/defaultconfig.go` (+1/-1)
- `src/jobs/base.go` (+3/-8)
- `src/jobs/http.go` (+11/-9)
- `src/jobs/packetgen.go` (+11/-9)
- `src/jobs/rawnet.go` (+12/-10)
- `src/jobs/slowloris.go` (+5/-4)
- `src/jobs/synflood.go` (+5/-4)
- `src/logs/logs.go` (+0/-0)
- `src/metrics/metrics.go` (+0/-0)
- `src/packetgen/constants.go` (+0/-0)
- `src/packetgen/packetgen.go` (+0/-0)
- `src/packetgen/utils.go` (+1/-1)
- `src/slowloris/slowloris.go` (+1/-1)
- `src/synfloodraw/constants.go` (+0/-0)
- `src/synfloodraw/synfloodraw.go` (+0/-0)
- `src/synfloodraw/utils.go` (+0/-0)
- `src/utils/countrychecker.go` (+54/-0)
- `src/utils/dumpmetrics.go` (+50/-0)
- `src/utils/panichandler.go` (+9/-0)
- `src/utils/statistics.go` (+0/-0)
- `src/utils/templates/templates.go` (+4/-3)
</details>

## #117 Allow specifying username and password in config itself
**State:** MERGED | **Author:** @bitshape | **Date:** 2022-03-05 | **Branch:** main → main | **+41/-17** | **Files:** 2

> In current implementation we have to replace `auth-user-pass` line with values that are provided `--env "OPENVPN_USERNAME="` and `--env "OPENVPN_PASSWORD="`.
> 
> This works fine if you have a setup where you are using a single VPN provider and multiple `.conf` files, typically representing different...

<details><summary>Files changed (2)</summary>

- `README.md` (+16/-0)
- `run/run-openvpn.sh` (+25/-17)
</details>

## #114 Added country check to make sure users don't launch it with Ukrainian IPs
**State:** MERGED | **Author:** @Devaniti | **Date:** 2022-03-05 | **Branch:** main → main | **+67/-0** | **Files:** 2

> First time coding in go, so code may be horrible
> Need to replace URL to correct one
> closes #110

<details><summary>Files changed (2)</summary>

- `main.go` (+43/-0)
- `site/assets/vpn.html` (+24/-0)
</details>

## #113 couple free vpn added
**State:** MERGED | **Author:** @ctukraine22 | **Date:** 2022-03-05 | **Branch:** main → main | **+2/-0** | **Files:** 1

<details><summary>Files changed (1)</summary>

- `README.md` (+2/-0)
</details>

## #112 add contact section
**State:** CLOSED | **Author:** @iamtodor | **Date:** 2022-03-05 | **Branch:** add_telegram_link → main | **+7/-0** | **Files:** 1

<details><summary>Comments (3)</summary>

- **@arriven** (2022-03-05): Ah, ok, it is only possible to commit suggestions if you are have write permissions to the fork. I thought it's a bit smarter than that
- **@iamtodor** (2022-03-05): @Arriven I updated the contact section, the data was taken from the channel info
- **@arriven** (2022-03-05): There were conflicts due to #128 so I applied the patch manually
</details>

<details><summary>Files changed (1)</summary>

- `README.md` (+7/-0)
</details>

## #108 added DaemonSets
**State:** CLOSED | **Author:** @killabayte | **Date:** 2022-03-05 | **Branch:** main → main | **+66/-3** | **Files:** 5

> - added DaemonSets

<details><summary>Comments (4)</summary>

- **@arriven** (2022-03-04): @killabayte still conflicts
- **@killabayte** (2022-03-04): Guys, I can't see what exactly I need to fix to resolve those conflicts. It would be super great if you can point me to the particular piece that should be fixed.
- **@arriven** (2022-03-05): hmm, ok, github mobile client was showing me that it's possible to merge this. Guess I'll have to cherry-pick it manually. @killabayte the easiest way for you to bring your fork back up to date after...
- **@arriven** (2022-03-05): @killabayte I cherry-picked commits manually, you should be good to go recreate your fork
</details>

<details><summary>Files changed (5)</summary>

- `README.md` (+33/-3)
- `k8s-manifest/advanced/00_db1000n_namespace.yaml` (+0/-0)
- `k8s-manifest/advanced/01_db1000n_daemonset.yaml` (+29/-0)
- `k8s-manifest/simple/00_db1000n_namespace.yaml` (+4/-0)
- `k8s-manifest/simple/01_db1000n_deployment.yaml` (+0/-0)
</details>

## #107 Added advanced k8s manifests
**State:** CLOSED | **Author:** @killabayte | **Date:** 2022-03-04 | **Branch:** main → main | **+66/-3** | **Files:** 5

> - added DaemonSets

<details><summary>Comments (1)</summary>

- **@arriven** (2022-03-04): @killabayte Resolve conflicts in README please
</details>

<details><summary>Files changed (5)</summary>

- `README.md` (+33/-3)
- `k8s-manifest/advanced/00_db1000n_namespace.yaml` (+0/-0)
- `k8s-manifest/advanced/01_db1000n_daemonset.yaml` (+29/-0)
- `k8s-manifest/simple/00_db1000n_namespace.yaml` (+4/-0)
- `k8s-manifest/simple/01_db1000n_deployment.yaml` (+0/-0)
</details>

## #106 Added advanced kubernetes manifests(DaemonSets) for k8s cluster which can scaled horizontally
**State:** CLOSED | **Author:** @killabayte | **Date:** 2022-03-04 | **Branch:** main → main | **+2213/-79** | **Files:** 41

> - Added advanced Kubernetes manifests(DaemonSets) for k8s cluster which can be scaled horizontally
> - Corrected requested DaemonSet resources in a favor of GKE standard clusters

<details><summary>Files changed (41)</summary>

- `.github/workflows/gh-pages-deploy.yml` (+17/-0)
- `.github/workflows/gh-pages.yml` (+18/-0)
- `.github/workflows/release-binaries.yaml` (+14/-2)
- `.github/workflows/release-docker.yaml` (+9/-3)
- `.gitignore` (+11/-1)
- `Dockerfile` (+28/-7)
- `README.md` (+134/-7)
- `docs/README.md` (+233/-0)
- `go.mod` (+5/-1)
- `go.sum` (+20/-1)
- `helm/.helmignore` (+23/-0)
- `helm/Chart.yaml` (+12/-0)
- `helm/README.md` (+18/-0)
- `helm/templates/_helpers.tpl` (+62/-0)
- `helm/templates/deployment.yaml` (+46/-0)
- `helm/values.yaml` (+26/-0)
- `install.sh` (+11/-7)
- `k8s-manifest/advanced/00_db1000n_namespace.yaml` (+4/-0)
- `k8s-manifest/advanced/01_db1000n_daemonset.yaml` (+29/-0)
- `k8s-manifest/simple/00_db1000n_namespace.yaml` (+4/-0)
- `k8s-manifest/simple/01_db1000n_deployment.yaml` (+27/-0)
- `logs/logs.go` (+18/-10)
- `main.go` (+101/-32)
- `openvpn/place-your-ovpn-configuration-here` (+0/-0)
- `packetgen/utils.go` (+8/-7)
- `run.sh` (+15/-0)
- `run/db1000n.sh` (+13/-0)
- `run/openvpn-up.sh` (+7/-0)
- `run/run-openvpn.sh` (+33/-0)
- `site/assets/db1000n.wasm` (+0/-0)
- `site/assets/index.html` (+21/-0)
- `site/assets/wasm_exec.js` (+636/-0)
- `supervisord/supervisord-db1000n.conf` (+7/-0)
- `supervisord/supervisord-openvpn.conf` (+7/-0)
- `supervisord/supervisord.conf` (+5/-0)
- `terraform/gcp_expressvpn/README.md` (+7/-0)
- `terraform/gcp_expressvpn/main.tf` (+101/-0)
- `terraform/gcp_expressvpn/variables.tf` (+21/-0)
- `testconfig.json` (+2/-1)
- `utils/defaultconfig.go` (+427/-0)
- `utils/statistics.go` (+33/-0)
</details>

## #104 add vpn list
**State:** MERGED | **Author:** @iamtodor | **Date:** 2022-03-04 | **Branch:** add_vpn_list → main | **+13/-0** | **Files:** 1

<details><summary>Comments (1)</summary>

- **@iamtodor** (2022-03-04): @Arriven @horodchukanton open new PR with VPN list as the previous one https://github.com/Arriven/db1000n/pull/94 was overwritten
</details>

<details><summary>Files changed (1)</summary>

- `README.md` (+13/-0)
</details>

## #103 feat(doc): add docker commands for server run(for easy copy-paste)
**State:** MERGED | **Author:** @kuzm1ch | **Date:** 2022-03-04 | **Branch:** main → main | **+30/-1** | **Files:** 1

> tune readme to have easy copy-paste command for server run 
> 
> Also there is memory leak and therefore restart=always is required 
> <img width="766" alt="Screenshot 2022-03-04 at 20 49 13" src="https://user-images.githubusercontent.com/32264674/156824090-4d4c63e1-45e5-406f-8980-19dd93dcd6c0.png">

<details><summary>Files changed (1)</summary>

- `README.md` (+30/-1)
</details>

## #102 Move jobs to a separate package
**State:** MERGED | **Author:** @jdoe7865623 | **Date:** 2022-03-04 | **Branch:** jobs → main | **+503/-423** | **Files:** 7

<details><summary>Files changed (7)</summary>

- `job/base.go` (+65/-0)
- `job/http.go` (+170/-0)
- `job/packetgen.go` (+72/-0)
- `job/rawnet.go` (+98/-0)
- `job/slowloris.go` (+55/-0)
- `job/synflood.go` (+33/-0)
- `main.go` (+10/-423)
</details>

## #98 temporary fix for oracle cloud vms
**State:** MERGED | **Author:** @securims | **Date:** 2022-03-04 | **Branch:** main → main | **+5/-1** | **Files:** 1

<details><summary>Files changed (1)</summary>

- `install.sh` (+5/-1)
</details>

## #97 Minor cleanup
**State:** MERGED | **Author:** @jdoe7865623 | **Date:** 2022-03-04 | **Branch:** newmain → main | **+130/-114** | **Files:** 2

<details><summary>Files changed (2)</summary>

- `main.go` (+40/-114)
- `template/template.go` (+90/-0)
</details>

## #95 Fixing small typos in README
**State:** MERGED | **Author:** @horodchukanton | **Date:** 2022-03-04 | **Branch:** patch-1 → main | **+3/-3** | **Files:** 1

<details><summary>Files changed (1)</summary>

- `README.md` (+3/-3)
</details>

## #94 issue #19: add VPN list
**State:** MERGED | **Author:** @iamtodor | **Date:** 2022-03-04 | **Branch:** add_vpn_list → main | **+13/-0** | **Files:** 1

<details><summary>Comments (1)</summary>

- **@iamtodor** (2022-03-04): @Arriven @horodchukanton your recent push overwrites this PR
</details>

<details><summary>Files changed (1)</summary>

- `README.md` (+13/-0)
</details>

## #93 Minor cleanup; move templates to a separate file; prepare for splitti…
**State:** CLOSED | **Author:** @jdoe7865623 | **Date:** 2022-03-08 | **Branch:** cleanup → main | **+2004/-180** | **Files:** 33

> …ng template parsing and execution

<details><summary>Files changed (33)</summary>

- `.github/workflows/gh-pages-deploy.yml` (+17/-0)
- `.github/workflows/gh-pages.yml` (+18/-0)
- `.github/workflows/release-binaries.yaml` (+14/-2)
- `.github/workflows/release-docker.yaml` (+9/-3)
- `.gitignore` (+11/-1)
- `Dockerfile` (+10/-7)
- `README.md` (+89/-5)
- `go.mod` (+5/-1)
- `go.sum` (+20/-1)
- `helm/.helmignore` (+23/-0)
- `helm/Chart.yaml` (+12/-0)
- `helm/README.md` (+18/-0)
- `helm/templates/_helpers.tpl` (+62/-0)
- `helm/templates/deployment.yaml` (+46/-0)
- `helm/values.yaml` (+26/-0)
- `install.sh` (+11/-7)
- `k8s-manifest/00_db1000n_namespace.yaml` (+4/-0)
- `k8s-manifest/01_db1000n_deployment.yaml` (+27/-0)
- `logs/logs.go` (+18/-10)
- `main.go` (+152/-135)
- `metrics/metrics.go` (+22/-0)
- `packetgen/packetgen.go` (+22/-0)
- `packetgen/utils.go` (+30/-7)
- `site/assets/db1000n.wasm` (+0/-0)
- `site/assets/index.html` (+21/-0)
- `site/assets/wasm_exec.js` (+636/-0)
- `template/template.go` (+90/-0)
- `terraform/gcp_expressvpn/README.md` (+7/-0)
- `terraform/gcp_expressvpn/main.tf` (+101/-0)
- `terraform/gcp_expressvpn/variables.tf` (+21/-0)
- `testconfig.json` (+2/-1)
- `utils/defaultconfig.go` (+427/-0)
- `utils/statistics.go` (+33/-0)
</details>

## #92 feat: added tf for aws ec2 deployment
**State:** CLOSED | **Author:** @arfgdev | **Date:** 2022-03-04 | **Branch:** add_aws_tf → 99-infrastructure-as-a-code-aws | **+321/-41** | **Files:** 5

> - added tf example to deploy on aws ec2

<details><summary>Comments (3)</summary>

- **@arriven** (2022-03-04): Hey, I had to do some commit amending to remove references to my work account. Could you rebase your fork on the latest version?
- **@arfgdev** (2022-03-04): @Arriven done
- **@arriven** (2022-03-04): Had to cherry-pick the commits manually, don't like github a bit
</details>

<details><summary>Files changed (5)</summary>

- `docs/README.md` (+55/-41)
- `terraform/aws_ec2/README.md` (+29/-0)
- `terraform/aws_ec2/ireland.tfvars` (+8/-0)
- `terraform/aws_ec2/main.tf` (+190/-0)
- `terraform/aws_ec2/variables.tf` (+39/-0)
</details>

## #91 minor cleanup
**State:** CLOSED | **Author:** @jdoe7865623 | **Date:** 2022-03-04 | **Branch:** cleanup → main | **+112849/-0** | **Files:** 41

<details><summary>Files changed (41)</summary>

- `.github/workflows/gh-pages-deploy.yml` (+17/-0)
- `.github/workflows/gh-pages.yml` (+18/-0)
- `.github/workflows/release-binaries.yaml` (+37/-0)
- `.github/workflows/release-docker.yaml` (+42/-0)
- `.github/workflows/test.yaml` (+20/-0)
- `.gitignore` (+12/-0)
- `Dockerfile` (+15/-0)
- `Makefile` (+10/-0)
- `README.md` (+187/-0)
- `go.mod` (+26/-0)
- `go.sum` (+85/-0)
- `helm/.helmignore` (+23/-0)
- `helm/Chart.yaml` (+12/-0)
- `helm/README.md` (+18/-0)
- `helm/templates/_helpers.tpl` (+62/-0)
- `helm/templates/deployment.yaml` (+46/-0)
- `helm/values.yaml` (+26/-0)
- `install.sh` (+42/-0)
- `k8s-manifest/00_db1000n_namespace.yaml` (+4/-0)
- `k8s-manifest/01_db1000n_deployment.yaml` (+27/-0)
- `logs/logs.go` (+51/-0)
- `main.go` (+611/-0)
- `metrics/metrics.go` (+96/-0)
- `packetgen/constants.go` (+6/-0)
- `packetgen/packetgen.go` (+203/-0)
- `packetgen/utils.go` (+173/-0)
- `proxylist.json` (+109104/-0)
- `site/assets/db1000n.wasm` (+0/-0)
- `site/assets/index.html` (+21/-0)
- `site/assets/wasm_exec.js` (+636/-0)
- `slowloris/slowloris.go` (+170/-0)
- `synfloodraw/constants.go` (+10/-0)
- `synfloodraw/synfloodraw.go` (+171/-0)
- `synfloodraw/utils.go` (+101/-0)
- `template.go` (+90/-0)
- `terraform/gcp_expressvpn/README.md` (+7/-0)
- `terraform/gcp_expressvpn/main.tf` (+101/-0)
- `terraform/gcp_expressvpn/variables.tf` (+21/-0)
- `testconfig.json` (+88/-0)
- `utils/defaultconfig.go` (+427/-0)
- `utils/statistics.go` (+33/-0)
</details>

## #90 docs
**State:** CLOSED | **Author:** @didgudan | **Date:** 2022-03-04 | **Branch:** main → main | **+113065/-0** | **Files:** 41

> create manual google cloud + openvpn + db1000n

<details><summary>Comments (1)</summary>

- **@arriven** (2022-03-04): I had to amend commits in the repo for privacy and legal reasons (mostly precaution but still), could you please recreate your fork or rebase it on the latest history?
</details>

<details><summary>Files changed (41)</summary>

- `.github/workflows/gh-pages-deploy.yml` (+17/-0)
- `.github/workflows/gh-pages.yml` (+18/-0)
- `.github/workflows/release-binaries.yaml` (+37/-0)
- `.github/workflows/release-docker.yaml` (+42/-0)
- `.github/workflows/test.yaml` (+20/-0)
- `.gitignore` (+12/-0)
- `Dockerfile` (+15/-0)
- `Makefile` (+10/-0)
- `README.md` (+187/-0)
- `defaultconfig.go` (+427/-0)
- `docs/README.md` (+233/-0)
- `go.mod` (+26/-0)
- `go.sum` (+85/-0)
- `helm/.helmignore` (+23/-0)
- `helm/Chart.yaml` (+12/-0)
- `helm/README.md` (+18/-0)
- `helm/templates/_helpers.tpl` (+62/-0)
- `helm/templates/deployment.yaml` (+46/-0)
- `helm/values.yaml` (+26/-0)
- `install.sh` (+42/-0)
- `k8s-manifest/00_db1000n_namespace.yaml` (+4/-0)
- `k8s-manifest/01_db1000n_deployment.yaml` (+27/-0)
- `logs/logs.go` (+51/-0)
- `main.go` (+684/-0)
- `metrics/metrics.go` (+96/-0)
- `packetgen/constants.go` (+6/-0)
- `packetgen/packetgen.go` (+203/-0)
- `packetgen/utils.go` (+173/-0)
- `proxylist.json` (+109104/-0)
- `site/assets/db1000n.wasm` (+0/-0)
- `site/assets/index.html` (+21/-0)
- `site/assets/wasm_exec.js` (+636/-0)
- `slowloris/slowloris.go` (+170/-0)
- `statistics.go` (+33/-0)
- `synfloodraw/constants.go` (+10/-0)
- `synfloodraw/synfloodraw.go` (+171/-0)
- `synfloodraw/utils.go` (+101/-0)
- `terraform/gcp_expressvpn/README.md` (+7/-0)
- `terraform/gcp_expressvpn/main.tf` (+101/-0)
- `terraform/gcp_expressvpn/variables.tf` (+21/-0)
- `testconfig.json` (+88/-0)
</details>

## #88 Move instructions from google doc to readme
**State:** MERGED | **Author:** @iamtodor | **Date:** 2022-03-04 | **Branch:** move_instructions_from_gdoc_to_readme → main | **+54/-2** | **Files:** 2

<details><summary>Comments (2)</summary>

- **@iamtodor** (2022-03-04): Also, this PR brings updates for #69
- **@iamtodor** (2022-03-04): @Arriven @securims Please take a look. How does it look to you?
</details>

<details><summary>Files changed (2)</summary>

- `.gitignore` (+2/-0)
- `README.md` (+52/-2)
</details>

## #87 minor files restructuring
**State:** MERGED | **Author:** @securims | **Date:** 2022-03-04 | **Branch:** main → main | **+7/-6** | **Files:** 3

<details><summary>Files changed (3)</summary>

- `main.go` (+3/-2)
- `utils/defaultconfig.go` (+2/-2)
- `utils/statistics.go` (+2/-2)
</details>

## #86 panic handlers to non-critical paths just in case
**State:** MERGED | **Author:** @arriven | **Date:** 2022-03-04 | **Branch:** stability-precautions → main | **+4/-0** | **Files:** 1

<details><summary>Files changed (1)</summary>

- `main.go` (+4/-0)
</details>

## #84 Sending traffic (and basic usage data) to Google analytics
**State:** MERGED | **Author:** @artem-korotenko | **Date:** 2022-03-04 | **Branch:** feature/statistics → main | **+48/-2** | **Files:** 4

<details><summary>Files changed (4)</summary>

- `go.mod` (+3/-1)
- `go.sum` (+8/-1)
- `main.go` (+4/-0)
- `statistics.go` (+33/-0)
</details>

## #83 Trim spaces in udp/tcp address
**State:** MERGED | **Author:** @arriven | **Date:** 2022-03-04 | **Branch:** fix-address-parsing → main | **+2/-2** | **Files:** 1

<details><summary>Files changed (1)</summary>

- `main.go` (+2/-2)
</details>

## #81 fixed install.sh for arm64 and mac
**State:** MERGED | **Author:** @securims | **Date:** 2022-03-04 | **Branch:** main → main | **+48/-16** | **Files:** 2

<details><summary>Files changed (2)</summary>

- `install.sh` (+11/-7)
- `main.go` (+37/-9)
</details>

## #80 Add multiarch build for Docker
**State:** MERGED | **Author:** @Amet13 | **Date:** 2022-03-04 | **Branch:** main → main | **+9/-3** | **Files:** 1

> https://github.com/docker/build-push-action/blob/master/docs/advanced/multi-platform.md
> 
> https://github.com/Arriven/db1000n/issues/67

<details><summary>Files changed (1)</summary>

- `.github/workflows/release-docker.yaml` (+9/-3)
</details>

## #76 added async mode to improve http job throughput
**State:** MERGED | **Author:** @securims | **Date:** 2022-03-04 | **Branch:** main → main | **+37/-9** | **Files:** 1

<details><summary>Files changed (1)</summary>

- `main.go` (+37/-9)
</details>

## #74 Create VPN tunnel from within Docker container
**State:** CLOSED | **Author:** @bitshape | **Date:** 2022-03-04 | **Branch:** main → main | **+112864/-0** | **Files:** 47

> Pros of this approach:
> 
> * You can place as many `*.ovpn` configurations into `openvpn` directory to rotate between them randomly
> * If container's VPN dies for any reason, it will take the whole container with it meaning less chance of IP leakage (further hardening could be achieved with...

<details><summary>Comments (2)</summary>

- **@arriven** (2022-03-04): @bitshape pls tag me here or via other channels if you get a chance to address my comment
- **@arriven** (2022-03-04): Cherry picked it into main branch and applied the fix to change this config to be non-default target
</details>

<details><summary>Files changed (47)</summary>

- `.github/workflows/gh-pages-deploy.yml` (+17/-0)
- `.github/workflows/gh-pages.yml` (+18/-0)
- `.github/workflows/release-binaries.yaml` (+37/-0)
- `.github/workflows/release-docker.yaml` (+36/-0)
- `.github/workflows/test.yaml` (+20/-0)
- `.gitignore` (+12/-0)
- `Dockerfile` (+26/-0)
- `Makefile` (+10/-0)
- `README.md` (+191/-0)
- `defaultconfig.go` (+427/-0)
- `go.mod` (+24/-0)
- `go.sum` (+78/-0)
- `helm/.helmignore` (+23/-0)
- `helm/Chart.yaml` (+12/-0)
- `helm/README.md` (+18/-0)
- `helm/templates/_helpers.tpl` (+62/-0)
- `helm/templates/deployment.yaml` (+46/-0)
- `helm/values.yaml` (+26/-0)
- `install.sh` (+38/-0)
- `k8s-manifest/00_db1000n_namespace.yaml` (+4/-0)
- `k8s-manifest/01_db1000n_deployment.yaml` (+27/-0)
- `logs/logs.go` (+51/-0)
- `main.go` (+666/-0)
- `metrics/metrics.go` (+96/-0)
- `openvpn/place-your-ovpn-configuration-here` (+0/-0)
- `packetgen/constants.go` (+6/-0)
- `packetgen/packetgen.go` (+203/-0)
- `packetgen/utils.go` (+173/-0)
- `proxylist.json` (+109104/-0)
- `run.sh` (+15/-0)
- `run/db1000n.sh` (+13/-0)
- `run/openvpn-up.sh` (+7/-0)
- `run/run-openvpn.sh` (+33/-0)
- `site/assets/db1000n.wasm` (+0/-0)
- `site/assets/index.html` (+21/-0)
- `site/assets/wasm_exec.js` (+636/-0)
- `slowloris/slowloris.go` (+170/-0)
- `supervisord/supervisord-db1000n.conf` (+7/-0)
- `supervisord/supervisord-openvpn.conf` (+7/-0)
- `supervisord/supervisord.conf` (+5/-0)
- `synfloodraw/constants.go` (+10/-0)
- `synfloodraw/synfloodraw.go` (+171/-0)
- `synfloodraw/utils.go` (+101/-0)
- `terraform/gcp_expressvpn/README.md` (+7/-0)
- `terraform/gcp_expressvpn/main.tf` (+101/-0)
- `terraform/gcp_expressvpn/variables.tf` (+21/-0)
- `testconfig.json` (+88/-0)
</details>

## #71 terraform initial
**State:** MERGED | **Author:** @ichornyi | **Date:** 2022-03-03 | **Branch:** terraform-initial → main | **+138/-1** | **Files:** 4

> For advanced users: Simple Terraform manifest for fast deploy VM into GCP using ExpressVPN

<details><summary>Files changed (4)</summary>

- `.gitignore` (+9/-1)
- `terraform/gcp_expressvpn/README.md` (+7/-0)
- `terraform/gcp_expressvpn/main.tf` (+101/-0)
- `terraform/gcp_expressvpn/variables.tf` (+21/-0)
</details>

## #70 add --pull always to docker run instruction
**State:** MERGED | **Author:** @arriven | **Date:** 2022-03-03 | **Branch:** docker-pull-image-on-run-readme → main | **+1/-2** | **Files:** 1

<details><summary>Files changed (1)</summary>

- `README.md` (+1/-2)
</details>

## #68 Use one less unnecessary defer
**State:** MERGED | **Author:** @jdoe7865623 | **Date:** 2022-03-03 | **Branch:** cleanup → main | **+8/-5** | **Files:** 1

<details><summary>Files changed (1)</summary>

- `main.go` (+8/-5)
</details>

## #66 added job specific logging
**State:** MERGED | **Author:** @securims | **Date:** 2022-03-03 | **Branch:** main → main | **+18/-0** | **Files:** 1

<details><summary>Files changed (1)</summary>

- `main.go` (+18/-0)
</details>

## #65 Minor log improvements
**State:** MERGED | **Author:** @arriven | **Date:** 2022-03-03 | **Branch:** minor-log-improvements → main | **+11/-9** | **Files:** 2

<details><summary>Files changed (2)</summary>

- `main.go` (+3/-2)
- `packetgen/utils.go` (+8/-7)
</details>

## #64 Default config restructure
**State:** MERGED | **Author:** @arriven | **Date:** 2022-03-03 | **Branch:** default-config-restructure → main | **+427/-3** | **Files:** 2

> Moved out default config into a separate file and populated it with some targets

<details><summary>Files changed (2)</summary>

- `defaultconfig.go` (+427/-0)
- `main.go` (+0/-3)
</details>

## #61 Allow setting multiple configs via commandline
**State:** MERGED | **Author:** @arriven | **Date:** 2022-03-03 | **Branch:** allow-setting-multiple-configs → main | **+16/-8** | **Files:** 1

<details><summary>Files changed (1)</summary>

- `main.go` (+16/-8)
</details>

## #60 Added pure k8s manifests for db1000n
**State:** MERGED | **Author:** @killabayte | **Date:** 2022-03-03 | **Branch:** main → main | **+51/-0** | **Files:** 3

> - Added pure k8s manifests for db1000n
> - Updated readme file according to k8s manifests usage

<details><summary>Files changed (3)</summary>

- `README.md` (+20/-0)
- `k8s-manifest/00_db1000n_namespace.yaml` (+4/-0)
- `k8s-manifest/01_db1000n_deployment.yaml` (+27/-0)
</details>

## #59 Add helm chart for Kubernetes installation
**State:** MERGED | **Author:** @Amet13 | **Date:** 2022-03-03 | **Branch:** main → main | **+191/-0** | **Files:** 7

> This is a helm chart for experienced users.
> 
> The app could be easily deployed to the Kubernetes cluster and it could be scaled to a thousand replicas just in one click

<details><summary>Files changed (7)</summary>

- `README.md` (+4/-0)
- `helm/.helmignore` (+23/-0)
- `helm/Chart.yaml` (+12/-0)
- `helm/README.md` (+18/-0)
- `helm/templates/_helpers.tpl` (+62/-0)
- `helm/templates/deployment.yaml` (+46/-0)
- `helm/values.yaml` (+26/-0)
</details>

## #56 Docker multistage build
**State:** MERGED | **Author:** @ichornyi | **Date:** 2022-03-03 | **Branch:** multistage-build → main | **+10/-7** | **Files:** 1

<details><summary>Comments (1)</summary>

- **@arriven** (2022-03-03): Ooh, I wanted to do this for more than 2 days now but didn't get a chance to get to it.  @paalomnikdev Thanks for the contribution!
</details>

<details><summary>Files changed (1)</summary>

- `Dockerfile` (+10/-7)
</details>

## #53 Fix crash on empty proxylist
**State:** MERGED | **Author:** @arriven | **Date:** 2022-03-02 | **Branch:** fix-crash-on-empty-proxylist → main | **+3/-0** | **Files:** 1

> Fix #47

<details><summary>Files changed (1)</summary>

- `main.go` (+3/-0)
</details>

## #52 Remove proxy warning
**State:** MERGED | **Author:** @arriven | **Date:** 2022-03-02 | **Branch:** remove-proxy-warning → main | **+3/-2** | **Files:** 1

<details><summary>Files changed (1)</summary>

- `main.go` (+3/-2)
</details>

## #51 Deploy to gh-pages
**State:** MERGED | **Author:** @dmitr101 | **Date:** 2022-03-02 | **Branch:** main → main | **+56/-13** | **Files:** 3

> it seems to work but there is a problem with CORS being disabled by default

<details><summary>Files changed (3)</summary>

- `.github/workflows/gh-pages-deploy.yml` (+17/-0)
- `.github/workflows/gh-pages.yml` (+18/-0)
- `site/assets/index.html` (+21/-13)
</details>

## #50 Add colorful logs for users :3
**State:** MERGED | **Author:** @arriven | **Date:** 2022-03-02 | **Branch:** use-go-log → main | **+40/-14** | **Files:** 4

<details><summary>Files changed (4)</summary>

- `go.mod` (+2/-0)
- `go.sum` (+12/-0)
- `logs/logs.go` (+18/-10)
- `main.go` (+8/-4)
</details>

## #48 Embed backup config into executable
**State:** MERGED | **Author:** @arriven | **Date:** 2022-03-02 | **Branch:** embed-backup-config-into-exe → main | **+96/-4** | **Files:** 2

<details><summary>Files changed (2)</summary>

- `main.go` (+94/-3)
- `testconfig.json` (+2/-1)
</details>

## #46 Added assets for website
**State:** MERGED | **Author:** @arriven | **Date:** 2022-03-02 | **Branch:** web-version → main | **+649/-0** | **Files:** 3

<details><summary>Files changed (3)</summary>

- `site/assets/db1000n.wasm` (+0/-0)
- `site/assets/index.html` (+13/-0)
- `site/assets/wasm_exec.js` (+636/-0)
</details>

## #45 Gracefully handle panic in jobs
**State:** MERGED | **Author:** @arriven | **Date:** 2022-03-02 | **Branch:** graceful-panic-handling → main | **+12/-0** | **Files:** 1

<details><summary>Files changed (1)</summary>

- `main.go` (+12/-0)
</details>

## #44 Add webassembly to release job
**State:** MERGED | **Author:** @arriven | **Date:** 2022-03-02 | **Branch:** wasm → main | **+14/-2** | **Files:** 1

<details><summary>Files changed (1)</summary>

- `.github/workflows/release-binaries.yaml` (+14/-2)
</details>

## #43 Copyright
**State:** MERGED | **Author:** @arriven | **Date:** 2022-03-01 | **Branch:** copyright → main | **+90/-0** | **Files:** 5

<details><summary>Files changed (5)</summary>

- `README.md` (+2/-0)
- `main.go` (+22/-0)
- `metrics/metrics.go` (+22/-0)
- `packetgen/packetgen.go` (+22/-0)
- `packetgen/utils.go` (+22/-0)
</details>

## #42 Copyright
**State:** MERGED | **Author:** @arriven | **Date:** 2022-03-01 | **Branch:** copyright → main | **+88/-0** | **Files:** 4

<details><summary>Files changed (4)</summary>

- `main.go` (+22/-0)
- `metrics/metrics.go` (+22/-0)
- `packetgen/packetgen.go` (+22/-0)
- `packetgen/utils.go` (+22/-0)
</details>

## #41 Backup config retrieval
**State:** MERGED | **Author:** @arriven | **Date:** 2022-03-01 | **Branch:** backup-config-retrieval → main | **+10/-4** | **Files:** 2

<details><summary>Files changed (2)</summary>

- `main.go` (+8/-2)
- `testconfig.json` (+2/-2)
</details>

## #40 Remove unnecessary error from http job
**State:** MERGED | **Author:** @arriven | **Date:** 2022-03-01 | **Branch:** remove-unnecessary-error-from-http-job → main | **+109119/-6** | **Files:** 2

<details><summary>Files changed (2)</summary>

- `main.go` (+15/-5)
- `proxylist.json` (+109104/-1)
</details>

## #39 Populate proxylist and improve parsing
**State:** MERGED | **Author:** @arriven | **Date:** 2022-03-01 | **Branch:** populate-proxylist → main | **+109118/-4** | **Files:** 2

<details><summary>Files changed (2)</summary>

- `main.go` (+14/-3)
- `proxylist.json` (+109104/-1)
</details>

## #38 Get url template
**State:** MERGED | **Author:** @arriven | **Date:** 2022-03-01 | **Branch:** get-url-template → main | **+75/-47** | **Files:** 3

<details><summary>Files changed (3)</summary>

- `main.go` (+73/-46)
- `proxylist.json` (+1/-0)
- `testconfig.json` (+1/-1)
</details>

## #37 Http and socks proxies config
**State:** MERGED | **Author:** @arriven | **Date:** 2022-03-01 | **Branch:** http-and-socks-proxies-config → main | **+77/-1** | **Files:** 3

<details><summary>Files changed (3)</summary>

- `README.md` (+5/-0)
- `main.go` (+69/-1)
- `testconfig.json` (+3/-0)
</details>

## #36 added local mac addr template
**State:** MERGED | **Author:** @arriven | **Date:** 2022-03-01 | **Branch:** get-local-ip-template → main | **+16/-0** | **Files:** 3

<details><summary>Files changed (3)</summary>

- `README.md` (+1/-0)
- `main.go` (+1/-0)
- `packetgen/utils.go` (+14/-0)
</details>

## #35 Add local ip template
**State:** MERGED | **Author:** @arriven | **Date:** 2022-03-01 | **Branch:** get-local-ip-template → main | **+32/-2** | **Files:** 4

<details><summary>Files changed (4)</summary>

- `README.md` (+1/-0)
- `main.go` (+9/-0)
- `packetgen/utils.go` (+17/-0)
- `testconfig.json` (+5/-2)
</details>

## #33 Disable sending metrics by default
**State:** MERGED | **Author:** @arriven | **Date:** 2022-03-01 | **Branch:** disable-sending-metrics → main | **+3/-3** | **Files:** 1

> storing metrics on backend turned out to be more expensive that I thought, disabling for now

<details><summary>Files changed (1)</summary>

- `main.go` (+3/-3)
</details>

## #32 Updated doc with packetgen
**State:** MERGED | **Author:** @arriven | **Date:** 2022-02-28 | **Branch:** documentation-config → main | **+30/-1** | **Files:** 1

<details><summary>Files changed (1)</summary>

- `README.md` (+30/-1)
</details>

## #31 Add packetgen
**State:** MERGED | **Author:** @arriven | **Date:** 2022-02-28 | **Branch:** add-packetgen → main | **+386/-5** | **Files:** 5

<details><summary>Files changed (5)</summary>

- `main.go` (+54/-5)
- `packetgen/constants.go` (+6/-0)
- `packetgen/packetgen.go` (+181/-0)
- `packetgen/utils.go` (+119/-0)
- `testconfig.json` (+26/-0)
</details>

## #30 Add configurable path to dump metrics
**State:** MERGED | **Author:** @arriven | **Date:** 2022-02-28 | **Branch:** configure-metrics → main | **+9/-4** | **Files:** 1

> I will change the default metrics path to be empty once this ends

<details><summary>Files changed (1)</summary>

- `main.go` (+9/-4)
</details>

## #29 Documentation for configuring the app
**State:** MERGED | **Author:** @arriven | **Date:** 2022-02-28 | **Branch:** documentation-config → main | **+74/-7** | **Files:** 2

<details><summary>Files changed (2)</summary>

- `README.md` (+66/-5)
- `main.go` (+8/-2)
</details>

## #27 Install script
**State:** MERGED | **Author:** @arriven | **Date:** 2022-02-28 | **Branch:** install-script → main | **+52/-6** | **Files:** 2

<details><summary>Files changed (2)</summary>

- `README.md` (+14/-6)
- `install.sh` (+38/-0)
</details>

## #26 Update docker build action to push to ghcr
**State:** MERGED | **Author:** @arriven | **Date:** 2022-02-28 | **Branch:** main → main | **+4/-6** | **Files:** 1

<details><summary>Files changed (1)</summary>

- `.github/workflows/release-docker.yaml` (+4/-6)
</details>

## #25 More randomness to synflood
**State:** MERGED | **Author:** @arriven | **Date:** 2022-02-28 | **Branch:** synflood-improvements → main | **+24/-15** | **Files:** 1

<details><summary>Files changed (1)</summary>

- `synfloodraw/synfloodraw.go` (+24/-15)
</details>

## #24 new relic
**State:** CLOSED | **Author:** @zmitry | **Date:** 2022-03-04 | **Branch:** new_relic → main | **+1922/-0** | **Files:** 22

> - add docker readme
> - add new relic metrics

<details><summary>Comments (1)</summary>

- **@arriven** (2022-03-04): Decided to go forward with google analytics as it's cheaper and is more in line with the current needs
</details>

<details><summary>Files changed (22)</summary>

- `.github/workflows/release-binaries.yaml` (+30/-0)
- `.github/workflows/release-docker.yaml` (+40/-0)
- `.github/workflows/test.yaml` (+20/-0)
- `.gitignore` (+4/-0)
- `Dockerfile` (+13/-0)
- `Makefile` (+10/-0)
- `README.md` (+146/-0)
- `go.mod` (+28/-0)
- `go.sum` (+114/-0)
- `install.sh` (+38/-0)
- `lib/utils.go` (+18/-0)
- `logs/logs.go` (+43/-0)
- `main.go` (+505/-0)
- `metrics/metrics.go` (+74/-0)
- `packetgen/constants.go` (+6/-0)
- `packetgen/packetgen.go` (+181/-0)
- `packetgen/utils.go` (+119/-0)
- `slowloris/slowloris.go` (+170/-0)
- `synfloodraw/constants.go` (+10/-0)
- `synfloodraw/synfloodraw.go` (+171/-0)
- `synfloodraw/utils.go` (+101/-0)
- `testconfig.json` (+81/-0)
</details>

## #23 add docker readme
**State:** MERGED | **Author:** @zmitry | **Date:** 2022-02-27 | **Branch:** readme-docker → main | **+18/-2** | **Files:** 1

<details><summary>Files changed (1)</summary>

- `README.md` (+18/-2)
</details>

## #21 Slowloris
**State:** MERGED | **Author:** @o-volkov | **Date:** 2022-02-27 | **Branch:** slowloris → main | **+226/-4** | **Files:** 3

<details><summary>Files changed (3)</summary>

- `main.go` (+50/-4)
- `slowloris/slowloris.go` (+170/-0)
- `testconfig.json` (+6/-0)
</details>

## #20 Randomize seq num
**State:** MERGED | **Author:** @arriven | **Date:** 2022-02-27 | **Branch:** synflood-improvements → main | **+3/-1** | **Files:** 1

<details><summary>Files changed (1)</summary>

- `synfloodraw/synfloodraw.go` (+3/-1)
</details>

## #17 docker
**State:** MERGED | **Author:** @zmitry | **Date:** 2022-02-27 | **Branch:** docker → main | **+38/-0** | **Files:** 1

> - release docker
> - add docker imag

<details><summary>Files changed (1)</summary>

- `.github/workflows/release-docker.yaml` (+38/-0)
</details>

## #14 fix go mod
**State:** MERGED | **Author:** @zmitry | **Date:** 2022-02-27 | **Branch:** goinstall → main | **+19/-3** | **Files:** 2

<details><summary>Files changed (2)</summary>

- `README.md` (+16/-0)
- `main.go` (+3/-3)
</details>

## #13 Init random user agents
**State:** MERGED | **Author:** @k0xxx | **Date:** 2022-02-27 | **Branch:** env → main | **+16/-0** | **Files:** 4

<details><summary>Files changed (4)</summary>

- `.gitignore` (+2/-0)
- `go.mod` (+1/-0)
- `go.sum` (+9/-0)
- `main.go` (+4/-0)
</details>

## #11 Debug flag
**State:** CLOSED | **Author:** @o-volkov | **Date:** 2022-02-27 | **Branch:** debug_flag → main | **+34/-24** | **Files:** 1

<details><summary>Comments (1)</summary>

- **@arriven** (2022-02-27): Already done, sorry
</details>

<details><summary>Files changed (1)</summary>

- `main.go` (+34/-24)
</details>

## #10 fixed Dockerfile
**State:** MERGED | **Author:** @o-volkov | **Date:** 2022-02-27 | **Branch:** fix_docker → main | **+1/-1** | **Files:** 1

<details><summary>Files changed (1)</summary>

- `Dockerfile` (+1/-1)
</details>

## #3 logs
**State:** MERGED | **Author:** @o-volkov | **Date:** 2022-02-27 | **Branch:** terrafrom_do → main | **+91/-13** | **Files:** 6

<details><summary>Files changed (6)</summary>

- `.gitignore` (+2/-0)
- `Dockerfile` (+2/-2)
- `Makefile` (+10/-0)
- `logs/logs.go` (+18/-0)
- `main.go` (+39/-11)
- `metrics/metrics.go` (+20/-0)
</details>