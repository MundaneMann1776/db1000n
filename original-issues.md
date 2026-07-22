# Issues — Arriven/db1000n

Total: **252** issues


## #569 warn failed to fetch config {"path": "", "error": "open : no such file or directory"} ----how do I fix this?
**State:** OPEN | **Author:** @SirMacDonalds | **Created:** 2024-05-15 | **Updated:** 2024-05-15 | **Comments:** 0

> Compiled the app on Android CPU: ARMv8 rev 4 (v8l) (4) @ 1.344GHz . It compiled file. However, when I run it, I get
> warn	failed to fetch config	{"path": "", "error": "open : no such file or directory"} ----how do I fix this?
> 
> root@localhost:~/db1000n# ./db1000n
> info	running db1000n	{"version":...

## #567 .
**State:** CLOSED | **Author:** @zuperspasm | **Created:** 2022-09-10 | **Updated:** 2022-10-29 | **Comments:** 2

> ## Expected Behavior
> 
> ## Actual Behavior
> 
> ## Steps to Reproduce the Problem
> 
> ## Specifications

<details><summary>Comments (2)</summary>

- **@arriven** (2022-09-21): @zuperspasm I'll need a full crash log to be able to determine what's causing it, can you launch the app with something like `db1000n 1> logs.txt 2>&1` and attaching the content here?
- **@zuperspasm** (2022-10-29): Hi Arriven... Please delete this Issue.  Old PC with lots of problems that was not capable of running the code.  Sorry for wasting your time.
</details>

## #566 Build unsuccesful by go install
**State:** CLOSED | **Author:** @Caranthir | **Created:** 2022-08-13 | **Updated:** 2022-08-19 | **Comments:** 4

> I should be able to build from the repository by myself by 
> `go install github.com/Arriven/db1000n@latest`
> It doesn't work. It seems that it cannot find the URLs for the configuration files, when I build it myself.
> 
> This is the log file:
> ```
> info	running db1000n	{"version": "v0.0.1", "pid":...

<details><summary>Comments (4)</summary>

- **@arriven** (2022-08-13): Yeah, if you build from the source you have to specify the path to the config manually via the `-c` flag. You can check the links in the prebuilt binary (`-help` should show default values) or in the...
- **@Caranthir** (2022-08-14): Thanks for the answer. Now when I enter the link to the config file, I get the following error: `warn	can't decrypt config	{"error": "encryption not supported"}` What am I missing?
- **@Caranthir** (2022-08-19): Latest release seems to have resolved the issue. But now I get the following error: `error	error running job	{"name": "", "type": "encrypted", "error": "no identity matched any of the...
- **@arriven** (2022-08-19): yes, that last one is expected when you're building from source since you don't have a private encryption key for some jobs (you can check #394 as to why they're needed at all)
</details>

## #563 Non-cumulative stats `[enhancement, priority: medium]`
**State:** CLOSED | **Author:** @sq2mo | **Created:** 2022-07-21 | **Updated:** 2022-08-01 | **Comments:** 1

> I use the -less-stats option and it is working great. Is there any option (or implementation possibility) to display a non-cumulative stats once a minute, like requests and Mb per second? Right now the counters are accumulated every minute and total number is displayed.

<details><summary>Comments (1)</summary>

- **@arriven** (2022-07-31): version 0.9.15 now outputs both cumulative and non-cumulative stats in format `(stat since last refresh)/(total stat)`. if you use json or console format instead of simple (which is default) it will...
</details>

## #561 Add new sites?
**State:** CLOSED | **Author:** @app/ | **Created:** 2022-07-18 | **Updated:** 2022-07-19 | **Comments:** 2

> Sorry if this is wrong place to ask, but can these sites `89.191.237.192`, `rttv.ru` and `rttv.co.uk` be added to list? These don't have DDOS protection from what I know.
> 
> RT is the biggest propaganda and it seems IT army or anonymous no longer interested since RT added ddos protection on main...

<details><summary>Comments (2)</summary>

- **@vitich** (2022-07-18): Hi. Go to https://itarmy.com.ua/instruction/?lang=en and press the big button "@Suggest Targets" at the top right.
- **@** (2022-07-19): > Hi. Go to https://itarmy.com.ua/instruction/?lang=en and press the big button "@Suggest Targets" at the top right.  Thanks! didnt realize there was a button for it
</details>

## #558 Config path is not available anymore for Digital Ocean deployment 
**State:** CLOSED | **Author:** @ridox | **Created:** 2022-06-27 | **Updated:** 2022-06-28 | **Comments:** 1

> The URL with targets list is not accessible anymore. Getting 404 status code.
> Please check out the link to the file below:
> https://github.com/arriven/db1000n/blob/d742de99591b374123b4cde96596534190fe821e/terraform/digital_ocean/variables.tf#L30

<details><summary>Comments (1)</summary>

- **@arriven** (2022-06-28): updated, thanks for pointing it out!
</details>

## #557 ERROR: HostClient can't follow redirects to a different protocol, please use Client instead
**State:** OPEN | **Author:** @wips | **Created:** 2022-06-25 | **Updated:** 2022-06-26 | **Comments:** 1

> ## Expected Behavior
> No error?
> 
> ## Actual Behavior
> ```
> 2022/06/25 19:23:18.173639 runner.go:103: New config received, applying
> 2022/06/25 19:23:18.175056 http.go:145: Attacking https://www....
> 2022-06-25T22:23:18.175+0300    ERROR   runner/runner.go:187    error running job       {"name":...

<details><summary>Comments (1)</summary>

- **@arriven** (2022-06-26): One of the targets is misconfigured, doesn't affect others but let me take a look
</details>

## #556 prometheus.go:298: Can't push metrics to gateway
**State:** CLOSED | **Author:** @wips | **Created:** 2022-06-25 | **Updated:** 2022-06-26 | **Comments:** 2

> ## Expected Behavior
> No error
> 
> ## Actual Behavior
> 2022/06/25 19:31:16.934473 prometheus.go:298: Can't push metrics to gateway, trying to change gateway
> 
> ## Steps to Reproduce the Problem
> 
>   1. Run db1000n_0.8.7_darwin_amd64 in mac terminal
>   2. Observe logs
> 
> ## Specifications
> 
>   -...

<details><summary>Comments (2)</summary>

- **@wips** (2022-06-25): duplicate
- **@arriven** (2022-06-26): For this one you can just update to latest
</details>

## #555 oom killed
**State:** OPEN | **Author:** @MidnightRAT | **Created:** 2022-06-21 | **Updated:** 2023-05-19 | **Comments:** 23

> started with ulimit -n 65535
> 
> [101236.553584] app invoked oom-killer: gfp_mask=0x100cca(GFP_HIGHUSER_MOVABLE), order=0, oom_score_adj=0
> [101236.649900] CPU: 0 PID: 5641 Comm: app Kdump: loaded Not tainted 5.4.17-2136.307.3.4.el8uek.x86_64 #2
> [101236.651576] Hardware name: QEMU Standard PC...

<details><summary>Comments (23)</summary>

- **@arriven** (2022-06-22): How much memory do you have?
- **@deputinizer** (2022-06-22): I have 2 GB of RAM and still getting OOM after a few days... ``` info    attacking       {"target": "http://xxie"} info    attacking       {"target": "http://xxsa"} info    attacking      ...
- **@arriven** (2022-06-22): A few days will be interesting to debug
- **@deputinizer** (2022-06-23): Next day... next kill... i have to pprof before it gets killed ```  |    --- |                --- |           --- |                --- |       --- |  |  Total |           13608405 |      13336567...
- **@deputinizer** (2022-06-23): Also, I got a very uncomfortable email...  Is there a way to lower the rate of TCP SYN / per second ?  ``` Dear Customer,  Abnormal activity has been detected on your VPS...
- **@deputinizer** (2022-06-23): And yet another panic... funny it's on a single-thread machine :laughing: so it's not race condition :worried:   ``` ... 6969 more lines ... goroutine 20488 [sleep]: time.Sleep(0x14f46b0400)   ...
- **@arriven** (2022-06-23): > Also, I got a very uncomfortable email... >  > Is there a way to lower the rate of TCP SYN / per second ?  Interesting, there isn't any tcp syn attacks implemented in the app because they are...
- **@deputinizer** (2022-06-24): > amount of attempts to build a connection  well that's called Dial  In stoppropaganda i've implmented rate limiting https://github.com/erkexzcx/stoppropaganda#dialspersecond  Edit: Here was...
- **@arriven** (2022-06-26): Yeah, there's already a rate limiting in place, I just didn't treat dial as a special case but maybe I should
- **@arriven** (2022-06-26): @deputinizer thinking about it more, I think you can already achieve the same results with existing configuration options. There's exponential backoff present on errors which you can configure to...
- **@arriven** (2022-06-26): regarding the actual memory issue, I've been debugging todays config for couple of hours and the memory usage was only fluctuating for couple of MBs. Testing it out on my benchmark server revealed...
- **@deputinizer** (2022-06-26): <details>   <summary>[Spoiler] fatal error: runtime: out of memory</summary>  `./db1000n 2> stderr.txt`   ``` ... info	attacking	{"target": "http://smev74.gosuslugi.ru"} fatal error:...
- **@arriven** (2022-06-30): @MidnightRAT @deputinizer should be fixed now, poke me if you still encounter it
- **@MidnightRAT** (2022-07-02): ``` [ 3449.257924] systemd-journal invoked oom-killer: gfp_mask=0x100cca(GFP_HIGHUSER_MOVABLE), order=0, oom_score_adj=-250 [ 3449.257933] CPU: 0 PID: 405 Comm: systemd-journal Not tainted...
- **@heximcz** (2022-07-03): ``` [ 1937.576964] db1000n invoked oom-killer: gfp_mask=0xcc0(GFP_KERNEL), order=0, oom_score_adj=0 [ 1937.576996] CPU: 2 PID: 850 Comm: db1000n Tainted: G         C        5.10.103-v7l+ #1529 [...
- **@AlexUkr73** (2022-07-16): the same issue on Ubuntu VM with 2 GB RAM with latest and older db1000n builds:   `Jul 16 07:13:11 azurea3 kernel: [64679.724233]...
- **@arriven** (2022-07-16): I've spent couple of days trying to repro this on my machine but I never got it to consume more than 500 mb of RAM. Did someone monitor the memory usage of db1000n before the oom kill? I'm wondering...
- **@AlexUkr73** (2022-07-17): @arriven  Regarding reproducing - I've noticed it is reproduced on VMs with only 1 CPU available and 1 GB RAM (Amazon AWS)  `-min-interval 5s`- tried everything but didn't expect adding letter...
- **@MidnightRAT** (2022-07-18): ``` [11514.036137] db1000n invoked oom-killer: gfp_mask=0x1100cca(GFP_HIGHUSER_MOVABLE), order=0, oom_score_adj=0 [11514.036146] CPU: 1 PID: 2173 Comm: db1000n Not tainted 5.15.0-1013-oracle...
- **@vitich** (2022-07-18): ``` sudo sysctl -a | grep "vm.overcommit_memory" ```` And if !=2 do  ``` sysctl -w vm.overcommit_memory=2 sysctl -w vm.overcommit_ratio=80 ```
- **@seriyps** (2022-12-30): It looks like there is some kind of memory leak. This is how my RAM consumption graph over 24h...
- **@rkoten** (2023-01-26): Getting OOM killed on 0.9.20 running on a Raspberry Pi 3B+ with 1GB RAM. Before this version I used to run various releases from around May 2022 and never got this issue.
- **@pashagolub** (2023-05-19): Probably the same issue on Windows causing OS to reboot
</details>

## #554 Add more stats (cpu/memory load, amount of open connections, etc.) `[enhancement, priority: medium]`
**State:** OPEN | **Author:** @arriven | **Created:** 2022-06-15 | **Updated:** 2022-06-15 | **Comments:** 0

> It would be both useful for monitoring and for external management of db1000n (see https://github.com/arriven/db1000n/issues/549#issuecomment-1154939869). Ideally we'd also want all of this info to be available as http endpoint

## #553 Can you add limit download/upload speed?
**State:** OPEN | **Author:** @1o1o1 | **Created:** 2022-06-14 | **Updated:** 2022-12-30 | **Comments:** 3

> Can you add limit download/upload speed?  :) 
> 
> trickle don't work whit db1000n)
> 
> I have this msg in logs:  "kernel: nf_conntrack: nf_conntrack: table full, dropping packet"  :)

<details><summary>Comments (3)</summary>

- **@arriven** (2022-06-14): you can use `--min-interval` for that. it will introduce artificial rate limiting to all the jobs. Another option would be to reduce the amount of jobs running by using `--scale` with some fractional...
- **@1o1o1** (2022-06-14): Ok)  looks like working well 👍  "-scale 0.6"  is good for Archlinux on a VPS ... "-min-interval 2s -scale 0.6" is well for archlinuxarm on my routerboard espressobin :)
- **@seriyps** (2022-12-30): First of all you may just increase the `nf_conntrack` limit with smth like ``` sudo sysctl net.netfilter.nf_conntrack_max=128000 ```  You may also limit the overall outgoing throughput of your...
</details>

## #550 Disk usage is increasing with Docker containers
**State:** CLOSED | **Author:** @MetaMmodern | **Created:** 2022-06-03 | **Updated:** 2022-06-04 | **Comments:** 5

> ## Expected Behavior
> 
> Disk usage remains the same from update to update.
> 
> ## Actual Behavior
> Disk usage is increasing. I guess this is happening because of some docker caching and layers in Dockerfile are not written correctly, so cache update is huge.
> Graph is for last 14 days of...

<details><summary>Comments (5)</summary>

- **@arriven** (2022-06-04): I don't think this is something I can fix on my end. This is just the way docker works (it keeps all the older versions of images even if you don't use those). You can clean the system up by using...
- **@MetaMmodern** (2022-06-04): > in different environments  @arriven what do you mean by this? Sounds cool, however AFAIK it's already possible to update db1000n without killing the container.   Forgot to say: thank you for...
- **@arriven** (2022-06-04): AFAIR, the only layer that changes between versions is the one where the executable resides and I doubt it'll be possible to cache that
- **@arriven** (2022-06-04): As for updates: docker tracks the container lifetime by existance of the process with PID 1. Any kind of version update requires to restart the process in order to update the code and the new process...
- **@MetaMmodern** (2022-06-04): Okay, I'll close this for how then. Thank you
</details>

## #549 Scale up db1000n automatically in order to utilize all available system resources
**State:** OPEN | **Author:** @kirealll | **Created:** 2022-06-03 | **Updated:** 2022-06-14 | **Comments:** 2

> It would be good if you introduce the ability to scale up db1000n (increase scale parameter) automatically in order to utilize all available system resources or up to the predefined limit. Similar logic is already implemented in DB1000NX100. It scales up step by step measuring the average CPU and...

<details><summary>Comments (2)</summary>

- **@roman-kruglov** (2022-06-11): I proposed something similar in https://github.com/arriven/db1000n/issues/501. Great to hear some similar logic is already implemented somewhere for a reference! I'll surely take a look how it's done...
- **@arriven** (2022-06-14): the main reason I haven't added this feature to the main codebase is because making a general-purpose scaling has a completely different set of problems (the most obvious one being that you need to...
</details>

## #546 Trojan
**State:** OPEN | **Author:** @KostDark | **Created:** 2022-05-31 | **Updated:** 2022-06-01 | **Comments:** 3

> Hi,
> 
> The Windows defender catched Trojan:Win32/Trickbot!ml and Trojan:Win32/Sabsik.FL.A!ml in the 0.9.5 and 0.9.6 db1000n_windows_amd64.zip

<details><summary>Comments (3)</summary>

- **@roman-kruglov** (2022-05-31): Confirm, the same in my case. You can tell Win Defender to ignore it and still run the app as a temporary workaround.
- **@arriven** (2022-06-01): Wait, but 0.9.4 and prior are not flagged? That's really weird as there aren't many changes between those
- **@arriven** (2022-06-01): it could be that someone reported the executable and it got flagged. I've got reports that eset doesn't even allow you to download the archive and flags it as `WinGo/DdosAgent.B` (which seems to be...
</details>

## #545 Can you compiling file or opkg  OpenWRT for MIPS, MIPSBE, MMIPS etc?  ;)
**State:** OPEN | **Author:** @1o1o1 | **Created:** 2022-05-30 | **Updated:** 2022-06-08 | **Comments:** 14

> Can you compiling file or opkg  OpenWRT for MIPS, MIPSBE, MMIPS etc? 
> Its will be cool to use in routers too)

<details><summary>Comments (14)</summary>

- **@arriven** (2022-05-30): went ahead and added all the goarch options that did compile with the code. I can't guarantee all the features will work though
- **@1o1o1** (2022-06-01): Ok) OpenWRT 19.07.8 on MikroTik SXT Lite2  CPU 600MHz AR9344  mips kernel-4.14.241...
- **@deputinizer** (2022-06-01): mipsle maybe?  https://go.dev/doc/install/source#environment ```   | linux | mips   | linux | mipsle   | linux | mips64   | linux | mips64le ```
- **@1o1o1** (2022-06-01): with mipsle   :)  [17:25][root@OpenWrt:~]# .bins/db1000n .bins/db1000n: line 1: syntax error: unexpected "("  It is MIPSBE  :)   https://mikrotik.com/product/RBSXT2nDr3  need to compile for...
- **@arriven** (2022-06-02): Based on what I'm seeing, I'm not sure go can cross compile for mipsbe but I'll check a bit more thoroughly in couple hours
- **@arriven** (2022-06-02): UPD: according to all the docs I've found mipsbe should be just mips. Go has an option to compile hardfloat vs softfloat (default being only hardfloat) though, maybe that could be the missing part?
- **@arriven** (2022-06-02): Ideally we'd want to try and install go on that machine and inspect env variables it sets here https://go.dev/doc/install/source#environment Not sure you'd be able to easily install go on microtik...
- **@1o1o1** (2022-06-02): No) I can't install go 99.5 MB) there's not enough space)  available 101.5 MB :)
- **@arriven** (2022-06-03): Have you tried mips_softfloat?
- **@1o1o1** (2022-06-03): yes   [08:55][root@OpenWrt:~]# nice -n 19 .bins/db1000n Segmentation fault
- **@arriven** (2022-06-03): hmm, I think segfault in this case means that this is the architecture to use but there's a bug somewhere in the code itself that doesn't present itself on other systems (maybe some of the packages...
- **@arriven** (2022-06-04): so I've tried running mips binary via qemu and it seems to be working fine (weirdly enough it works both with softfloat and hardfloat) As for "debug" build - I haven't managed to make a code that...
- **@arriven** (2022-06-07): @1o1o1 I think I know what the issue is. How much RAM does that router have? db1000n needs at least 200mb to be able to run properly (and you'd need to provide `--skip-encrypted` argument, otherwise...
- **@1o1o1** (2022-06-07): :)  MikroTik SXT Lite2  CPU 600MHz AR9344  (--> RAM 64Mb <--)   NAND 128Mb  with 256-512Mb is too much expensive and  usually with arm cpu :)
</details>

## #543 Simplify logs
**State:** CLOSED | **Author:** @Andrii-Asiox | **Created:** 2022-05-22 | **Updated:** 2022-06-20 | **Comments:** 8

> Вітаю, я маю невеличку ферму телефонів на яких запущено db1000n і дуже не зручно дивитися на це простирадло логів. Чи могли б ви зробити спрощений режим де просто буде якась оцінка якості атаки, щоб було зрозуміло варто змінювати впн з'єднання чи ні. Дякую

<details><summary>Comments (8)</summary>

- **@arriven** (2022-05-23): So there are couple options to achieve something similar to what you need already: - you can specify `--log-format json` and then feed those to some json parser to only gather info you need (I think...
- **@PerchunPak** (2022-05-23): Чому в [документації](https://arriven.github.io/db1000n/advanced-docs/configuration/) немає нічого про ці опції?
- **@avoylenko** (2022-05-25): @PerchunPak i guess in most cases it's enough to run the binary without any provided options, but you can see all of them by running the db1000n instance with '-h' argument: `./db1000n -h`
- **@roman-kruglov** (2022-05-31): @arriven I'll implement it - an option to have only totals. I think it would be even better to have totals and each protocol as a target, something like:  ``` http  | stats... https |...
- **@roman-kruglov** (2022-06-03): Maybe a numeric options would be even better? Something like `-less-stats=20` would mean "show less info when the number of targets is higher than 20".
- **@roman-kruglov** (2022-06-10): Well, let's start with a simple boolean flag then https://github.com/arriven/db1000n/pull/552
- **@roman-kruglov** (2022-06-11): it's merged, should be in the next release. Maybe we could close this issue now.
- **@arriven** (2022-06-20): available in 0.9.10, thanks to @roman-kruglov
</details>

## #542 vpn load balancing script
**State:** OPEN | **Author:** @Gekaom | **Created:** 2022-05-18 | **Updated:** 2022-05-18 | **Comments:** 0

> Script developed for hotspotshield
> vpn.
> for Linux
> 1.installs db1000n script
> 2.install hotspotshield vpn
> 3.controls the connection to vpn, if disconnect, then reconnect
> 4. after a set time, changes the geolocation of the connection
> 5.verifies db1000n update
> the author abandoned it, I...

## #541 Error when pulling docker image
**State:** CLOSED | **Author:** @sentinalll | **Created:** 2022-05-18 | **Updated:** 2022-05-18 | **Comments:** 1

> ## Expected Behavior
> Docker image pull successful
> 
> ## Actual Behavior
> error pulling image configuration: download failed after attempts=1: unknown blob
> 
> ## Steps to Reproduce the Problem
> 
>   1. Try pulling the docker image
>   2.
>   3.
> 
> ## Specifications
> 
>   - Version:
>   - Platform:
>   -...

<details><summary>Comments (1)</summary>

- **@arriven** (2022-05-18): ghcr links got broken when I tweaked the account name (Arriven -> arriven, case sensitivity doesn't and shouldn't affect URLs at all, every other related functionality like working with the repo via...
</details>

## #540 Reference to db1000nX100 project
**State:** CLOSED | **Author:** @avoylenko | **Created:** 2022-05-16 | **Updated:** 2022-07-19 | **Comments:** 1

> Hello all,
> 
> Running a single instance of db1000n requires extra maintenance cost since IP could be banned/blocked temporary really fast and the instance becoming not effective. There is a really good project(https://github.com/ihorlv/db1000nX100) based on db1000n that solves this problem by...

<details><summary>Comments (1)</summary>

- **@vitich** (2022-07-18): https://itarmy.com.ua/instruction/#db1000n  Close the task pls
</details>

## #539 Things to optimize - performance
**State:** CLOSED | **Author:** @deputinizer | **Created:** 2022-05-08 | **Updated:** 2022-05-30 | **Comments:** 10

> - utils.Decode
> - templates.Parse
> - job.getNextPacket
> 
> <details>
>   <summary>[Spoiler] pprof CPU</summary>
>  ...

<details><summary>Comments (10)</summary>

- **@arriven** (2022-05-08): for `getNextPacket`: have you tried setting `StaticPacket` to true in the config? should work on tcp/udp jobs as well as they just forward that argument to packetgen
- **@deputinizer** (2022-05-08): Well I'm using the default config. https://github.com/db1000n-coordinators/LoadTestConfig/blob/e3ed4702c7d19347668ac5842d058172b596c329/config.v0.7.json#L435  There's no `StaticPacket` there
- **@arriven** (2022-05-08): I'm not sure you can optimize other two without defeating their purpose completely. The only other thing that could be done is porting that StaticPacket thing to http flood to enable sending more...
- **@deputinizer** (2022-05-08): Well there should be something faster, maybe: - just pure `function` and `arg` (`random_payload 10`) - JIT - just in time compiled template? Is there anything in go?
- **@deputinizer** (2022-05-08): Because compiling config is a no-go? :yum:  https://github.com/valyala/quicktemplate
- **@arriven** (2022-05-08): pure `function` and `arg` could work, but it would make the config even more bloated and I'm not completely sure it would be much faster, especially compared to `static` version which parses...
- **@arriven** (2022-05-08): > There's no StaticPacket there  Yeah, updating all the admin processes takes some time
- **@deputinizer** (2022-05-08): Nice, you added static :)  <details>   <summary>[Spoiler] Here's...
- **@arriven** (2022-05-08): hmm, having thought about it more, with current usage it might be easier to switch the code to use static by default and dynamic would have to be specified explicitly
- **@arriven** (2022-05-08): it won't affect memory usage but the CPU profile should get a lot better
</details>

## #537 SIGSEGV incoming
**State:** CLOSED | **Author:** @deputinizer | **Created:** 2022-05-08 | **Updated:** 2022-05-08 | **Comments:** 3

> This will cause memory issues. Nil pointer dereference probably
> ```golang
> req := fasthttp.AcquireRequest()
> fasthttp.ReleaseRequest(req)
> // using req later
> ```
> 
> https://github.com/Arriven/db1000n/blob/12b3db0d757d3bdcb83ff3b893555c6db6870a98/src/job/http.go#L149

<details><summary>Comments (3)</summary>

- **@arriven** (2022-05-08): ah, right. It doesn't cause SIGSEGV as it just returns the request to the pool, but it probably reuses it between different goroutines making a mess anyway
- **@deputinizer** (2022-05-08): It caused SIGSEGV in stoppropaganda :rofl:
- **@arriven** (2022-05-08): hmm, I've quickly run through the source of that pool and I'm not sure I see anything that could lead to a crash except race detection. Anyway that's not a good code and I fixed it already
</details>

## #534 To Skip, or not to Skip, that is the question
**State:** CLOSED | **Author:** @deputinizer | **Created:** 2022-05-06 | **Updated:** 2022-05-08 | **Comments:** 1

> Well, SkipBody does something different I think. 
> ```golang
> resp.SkipBody = true
> ```
> https://github.com/Arriven/db1000n/commit/3147170641eb0c3da75cfc74d68d9606d4e23d5a
> 
> The server sends body response but we are ignoring it, thus mishandling the HTTP...

<details><summary>Comments (1)</summary>

- **@arriven** (2022-05-08): the idea was to have a way to utilize cpu better by not needing to do unnecessary work if the goal is to just spam the target with traffic. I then realized that it's better done by utilizing...
</details>

## #533 Why is db1000n so slow...
**State:** CLOSED | **Author:** @deputinizer | **Created:** 2022-05-06 | **Updated:** 2022-05-08 | **Comments:** 2

> ![image](https://user-images.githubusercontent.com/100740281/167130319-13cc00bb-4cb0-4714-b4e0-1cad7bfb8008.png)
> 
> I'm pressing ctrl+C

<details><summary>Comments (2)</summary>

- **@deputinizer** (2022-05-06): And why is this metrics thing so retarded <details>   <summary>[Spoiler] pprof CPU</summary>  ...
- **@deputinizer** (2022-05-06): Resolver can be optimized like in stoppropaganda https://github.com/erkexzcx/stoppropaganda/tree/main/internal/spdnsclient <details>   <summary>[Spoiler] pprof CPU</summary>  ...
</details>

## #532 Killed. on 400MB ram machine
**State:** CLOSED | **Author:** @deputinizer | **Created:** 2022-05-05 | **Updated:** 2022-05-05 | **Comments:** 2

> So, how to scale the RAM usage down?
> 
> ## Actual Behavior
> ```console
> azureuser@azurevm:~/db$ ./db1000n
> [...]
> attacking       {"target": "https://fresh.1bitcloud.ru/"}
> Killed
> azureuser@azurevm:~/db$ 
> 
> ```
> 
> ## Steps to Reproduce the Problem
> 
>   1. Get an Azure account (maybe free 100$...

<details><summary>Comments (2)</summary>

- **@deputinizer** (2022-05-05): Swap helps a lot :)  ![image](https://user-images.githubusercontent.com/100740281/166939098-bd689fdb-6334-422c-bed6-29ec5a5da654.png)  From: https://linuxize.com/post/create-a-linux-swap-file/
- **@deputinizer** (2022-05-05): ```bash systemctl stop walinuxagent systemctl stop multipathd systemctl stop snapd ```
</details>

## #529 Implement --interface option for non-linux systems
**State:** OPEN | **Author:** @arriven | **Created:** 2022-05-04 | **Updated:** 2022-05-05 | **Comments:** 3

> --interface option uses syscall.BindToDevice which is only available for linux. It should be possible to use net.InterfaceByName inside conn.Control to get an addr that could then be transformed into sockaddr for regular syscall.Bind which is available for all unix systems. Doing it in the control...

<details><summary>Comments (3)</summary>

- **@arriven** (2022-05-04): I think I've implemented it in https://github.com/Arriven/db1000n/commit/9fbca3f1cc29d8a1e67655886f0ed57b6f9a1240 but it needs some additional testing  @deputinizer you were the one who initially...
- **@deputinizer** (2022-05-05): Looks like windows just binds to...
- **@arriven** (2022-05-05): Yeah, I'm not looking to implementing that on windows, just wanted to ensure that it works properly on unix without BindToDevice
</details>

## #528 Change country checker to use fasthttp with all network settings (proxy, interface, etc.) `[enhancement, priority: low]`
**State:** CLOSED | **Author:** @arriven | **Created:** 2022-05-04 | **Updated:** 2022-05-08 | **Comments:** 1

> Works with ipv6 ! But still small bug that was not present at pre 0.8x series - countrycheker still uses ipv4 addressing for country check :
> 
> ```
> utils/countrychecker.go:78      location info   {"country": ....
> ```
> 
> _Originally posted by @Sfinx in...

<details><summary>Comments (1)</summary>

- **@arriven** (2022-05-08): fixed in 060ae19ad8805ef0b7e0b161ac5a1a6f1df6e086
</details>

## #527 [Question to Developers/Maintainers] Is db1000nX100 considered as trusted rework of db1000n ?
**State:** CLOSED | **Author:** @dannysilence | **Created:** 2022-05-02 | **Updated:** 2022-05-03 | **Comments:** 3

> Hello there.
> 
> Was quiet impressed to read the description of this (https://github.com/ihorlv/db1000nX100), but feeling tentative about to which side of the force it belongs to, considering the fact what db1000n is doing and how easy it is to use it in some form of opposite direction or simply to...

<details><summary>Comments (3)</summary>

- **@arriven** (2022-05-03): Yes, it's trustworthy.  You can see the reference to that repo on official itarmy website (https://itarmy.com.ua/powerful/?lang=en) and some of the db1000n features were even added by request of...
- **@dannysilence** (2022-05-03): thank you!
- **@dannysilence** (2022-05-03): that may definitely help if anyone would have similar question in future as it looks like there were no references from quick look around as i thought yesterday
</details>

## #526 -local-address flag does not work
**State:** CLOSED | **Author:** @deputinizer | **Created:** 2022-05-02 | **Updated:** 2022-05-04 | **Comments:** 10

> ## Expected Behavior
> I wanted to run program only on interface/device `wlan1` from Raspberry Pi 2B.
> HTTP Requests should be sent just like in curl:
> ```bash
> $ curl --interface wlan1 'https://api.ipify.org'
> 1.2.3.4
> ```
> Similar problem fixed in Rust:...

<details><summary>Comments (10)</summary>

- **@deputinizer** (2022-05-02): Looks like Golang is just a lot more retarded than Rust... https://github.com/golang/go/issues/39293  I can't believe they didn't add this functionality for so many years.  There should be also...
- **@arriven** (2022-05-03): LocalAddress is called that way because it expects an address, not an interface name. Golang has features that would allow working with interface names (it would just fetch interface address under...
- **@arriven** (2022-05-03): Ah, wait, I see that you're using IP in repro steps, can you clarify that it's not working that way as your actual behavior showcases usage with interface name?
- **@deputinizer** (2022-05-03): >  I feel like exposing address gives user more control (i.e. an interface can have multiple addresses attached, especially in case of ipv6)  Well, DHCP is a ducktape. Local IP changes on WiFi....
- **@deputinizer** (2022-05-03): Should work in go: ```golang      dialer := &net.Dialer{         Control: func(network, address string, conn syscall.RawConn) error {             var operr error             if err :=...
- **@deputinizer** (2022-05-03): Temprorary solution ```bash while true; do sudo route del default gw 192.168.0.1 eth0; sleep 5; done ```
- **@deputinizer** (2022-05-03): Ok, another thing. How to limit resources on raspberry pi 1B ? - `-scale 1` argument seems to be the lowest already. - `-enable-primitive false` eats too much RAM.  In stoppropaganda, i've...
- **@deputinizer** (2022-05-03): Woooow thanks! https://github.com/Arriven/db1000n/commit/a7edd0071ee129712fe3ebdf643a75e24c3f1a0a
- **@deputinizer** (2022-05-03): Nice. It actually works. ```console pi@pi2:~ $ ./db1000n -interface wlan1 ... pi@pi2:~ $ vnstat -l -i wlan1 Monitoring wlan1...     rx:     3.24 Mbit/s   296 p/s          tx:   165.98 kbit/s  ...
- **@arriven** (2022-05-04): I'm a bit sad that it only works for linux as other systems don't have that particular syscall. I feel like there should be a way to hack around that by dynamically querying for the ip address of an...
</details>

## #525 Put attack on hold when VPN is disabled
**State:** OPEN | **Author:** @Geniy00 | **Created:** 2022-05-02 | **Updated:** 2022-05-08 | **Comments:** 4

> I'd like to suggest the next improvement:
> It could be much safer to put the attack on hold when VPN is disabled.
> I'm using my Windows 10 to run db1000n together with some VPN application. Sometimes when I have network issues my VPN application can be closed or disabled automatically, but db1000n...

<details><summary>Comments (4)</summary>

- **@arriven** (2022-05-04): would it work for you if the app would just crash/exit in that scenario and you had to restart it? assuming that you'd have to restart your vpn app anyway it feels like I could kill 2 birds with one...
- **@Geniy00** (2022-05-04): It will work for me.  I understand that some calls can be sent to the goal under attack, and my real IP can be leaked, but I think it's a good reason to stop attack ASAP
- **@tony1492** (2022-05-05): That is best idea hopefully that will work with linux too lol !
- **@arriven** (2022-05-08): Implemented it in https://github.com/Arriven/db1000n/commit/8951bbb66d98262e869bd4ca15ffc68fe6480c09 You'll need a combination of `--strict-country-check` and `--country-check-interval <interval>`...
</details>

## #524 Main db1000n network is unreachable when ovpn container is restarted
**State:** OPEN | **Author:** @palianycia123 | **Created:** 2022-05-02 | **Updated:** 2022-05-05 | **Comments:** 3

> I noticed that sometimes ovpn (service of docker-compose app) is restarted - which is ok because there might be some connectivity issue to VPN server. Autoheal container works perfectly here - it restarts ovpn container. But it doesn't restart main db1000n container because it doesn't have health...

<details><summary>Comments (3)</summary>

- **@arriven** (2022-05-04): I'm considering different ways to do it but it feels like this and #525 could be implemented in the same way. Or rather implementing that one would make it very easy to implement this one
- **@palianycia123** (2022-05-05): Well, simple app crashing/exiting in case of network issues, might not resolve this issue. According to [autheal doc](https://github.com/willfarrell/docker-autoheal), health check is the dependecy...
- **@arriven** (2022-05-05): I'm not completely sure but I assume autoheal would just restart the container if healthcheck fails. Crashing the main process would make the container restart anyway if correct restart policy is...
</details>

## #523 Question: is there a way to reduce a load on the network?
**State:** OPEN | **Author:** @nedis4 | **Created:** 2022-05-01 | **Updated:** 2022-05-02 | **Comments:** 1

> So, I run this via Docker on my NAS. Unfortunately, after recent updates it renders my whole DSL network connection unusable. Is there a way to reduce a load this program creates? I looked through documentation but did not find a way for this. A few versions back (from around 2 weeks ago) it worked...

<details><summary>Comments (1)</summary>

- **@arriven** (2022-05-02): You can utilize --min-interval to have artificial pauses between packets being sent (I think I remember that argument correctly but you can always check it in help message available via -h flag)
</details>

## #522 error: template: tpl:1:17: executing "tpl"
**State:** CLOSED | **Author:** @pashagolub | **Created:** 2022-05-01 | **Updated:** 2022-05-10 | **Comments:** 13

> ## Expected Behavior
> No error
> 
> ## Actual Behavior
> ```
> error executing template        {"error": "template: tpl:1:17: executing \"tpl\" at <index (split (.Value (ctx_key \"data.source\")) \"function() {\") 1>: error calling index: reflect: slice index out of range"}
> single http request    ...

<details><summary>Comments (13)</summary>

- **@sq2mo** (2022-05-01): Same issue here, also visible on non-docker launch.
- **@arriven** (2022-05-02): This is a job that is designed to bypass qrator failing due to qrator not being enabled by the target. As far as I remember this one should've been a warning but simple output doesn't display log...
- **@pashagolub** (2022-05-08): Would it be possible to address this issue somehow? It produces a visual garbage  ```single http request     {"target":...
- **@roman-kruglov** (2022-05-08): > This is a job that is designed to bypass qrator failing due to qrator not being enabled by the target. As far as I remember this one should've been a warning but simple output doesn't display log...
- **@arriven** (2022-05-08): I've moved those logs to debug output as it usually doesn't mean anything to a regular user, will be available with next release
- **@pashagolub** (2022-05-08): > -log-format console already has that additional information.   Is it a known issue with timestamp representation in this mode? ``` 1.6520072161734493e+09  info    job/http.go:69  single http...
- **@roman-kruglov** (2022-05-08): > Would it be possible to address this issue somehow? It produces a visual garbage >  > ``` > error executing template        {"error": "template: tpl:1:17: executing \"tpl\" at <index (split...
- **@roman-kruglov** (2022-05-08): > > -log-format console already has that additional information. >  > Is it a known issue with timestamp representation in this mode? >  > ``` > 1.6520072161734493e+09  info    job/http.go:69 ...
- **@arriven** (2022-05-08): I'd probably use something like `iso8601` or `rfc3339` for console layout but leave it as is for json one
- **@arriven** (2022-05-08): https://github.com/uber-go/zap/blob/6f34060764b5ea1367eecda380ba8a9a0de3f0e6/zapcore/encoder.go#L135 looks like it already has implementations for that
- **@roman-kruglov** (2022-05-08): > https://github.com/uber-go/zap/blob/6f34060764b5ea1367eecda380ba8a9a0de3f0e6/zapcore/encoder.go#L135 looks like it already has implementations for that  yep, just need to switch to another one
- **@roman-kruglov** (2022-05-08): here it goes https://github.com/Arriven/db1000n/pull/538 - changes the time format for `console` log format output
- **@roman-kruglov** (2022-05-09): these issues seem to be addressed, propose to close this issue
</details>

## #521 -local-address do not works with ipv6 addresses
**State:** CLOSED | **Author:** @Sfinx | **Created:** 2022-04-28 | **Updated:** 2022-05-17 | **Comments:** 9

> ```
> ./db1000n -local-address 2001:xxx...
> ```
> 
> just select first ipv4 interface

<details><summary>Comments (9)</summary>

- **@arriven** (2022-04-29): In order to use ipv6 interface this way you also need to provide an ipv6 zone (interface name) because in case of ipv6 you can have same link address for multiple interfaces. I had to add support for...
- **@Sfinx** (2022-04-29): Hint with %interface_name do not work. I think that problem is that my IPV6 interface has several IP addresses including IPV4 ones. The db1000n just picks up the first IPV4 one from this interface...
- **@arriven** (2022-04-29): weird, it seems to be working for me, let me check on my remote server if it's still up
- **@arriven** (2022-04-29): yeah, it seems to pickup the right interface, although my home network doesn't support ipv6 so I just get `network unreachable` (ping displays the same thing)
- **@deputinizer** (2022-05-02): For me `%interface` doesn't work either. `./db1000n -local-address 10.2.2.2%wlan1`
- **@arriven** (2022-05-03): @deputinizer %interface should only be specified for ipv6 addresses and it's designed that way because you can have the same ipv6 address for multiple interfaces
- **@deputinizer** (2022-05-03): @Sfinx Probably fixed in a7edd0071ee129712fe3ebdf643a75e24c3f1a0a
- **@Sfinx** (2022-05-03): Works with ipv6 ! But still small bug that was not present at pre 0.8x series - countrycheker still uses ipv4 addressing for country check :  ``` utils/countrychecker.go:78      location info  ...
- **@deputinizer** (2022-05-08): @Sfinx Fixed IPv6 and countrychecker
</details>

## #520 How to bind to specific interface ?
**State:** CLOSED | **Author:** @Sfinx | **Created:** 2022-04-27 | **Updated:** 2022-05-03 | **Comments:** 4

> Having several interfaces and need to force usage of specific one. How to do this ? There is must be option "-I" like ping has or so.

<details><summary>Comments (4)</summary>

- **@arriven** (2022-04-28): As of 0.8.32 you can specify `--local-address <ip>` to achieve that
- **@Sfinx** (2022-04-28): Thanks !
- **@deputinizer** (2022-05-03): Also fixed in a7edd0071ee129712fe3ebdf643a75e24c3f1a0a
- **@Sfinx** (2022-05-03): Works with ipv6 ! But still small bug that was not present at pre 0.8x series - countrycheker still uses ipv4 addressing for country check :  ``` utils/countrychecker.go:78      location info  ...
</details>

## #516 How to get the table output that was introduced in v8.0.23?
**State:** CLOSED | **Author:** @sadviq99 | **Created:** 2022-04-23 | **Updated:** 2022-04-28 | **Comments:** 6

> In the version v8.0.23 in the PR https://github.com/Arriven/db1000n/pull/484 was introduced a nice table output format, but now I don't see an option to enable it back. Is this possible or would it be possible in the future? 
> ```
>  --- Traffic stats ---
>  |            Target | Requests attempted |...

<details><summary>Comments (6)</summary>

- **@arriven** (2022-04-25): Right now this same output is printed as json, although there's also PRs #517 and #518 that might change the format a bit (I plan to switch default format to simple but json will be available as...
- **@arriven** (2022-04-25): I've also seen you discussed response rate in that issue you linked, the easiest way to calculate that now is to use requests_sent/requests_attempted but to have the most viable stats you should...
- **@sadviq99** (2022-04-25): @Arriven yes, I already updated my bot to use JSON output, I guess it was easier to parse than plain text in the table output. https://github.com/sadviq99/db1000n-setup/pull/6  Thank you very much...
- **@arriven** (2022-04-25): Just make sure to update the script for 0.8.31 which I plan to release tomorrow morning
- **@roman-kruglov** (2022-04-26): @Arriven @sadviq99  guys, I'm working on exactly this in #519 - to bring the table back for the simple terminal-oriented output. I hope to finish and polish it today's evening
- **@arriven** (2022-04-28): @sadviq99 0.8.32 brings back table format by default, but you can still use json one (which is probably better for automated parsing) by specifying `--log-format json`
</details>

## #515 v0.8.29: Docker version exits after printing out config
**State:** CLOSED | **Author:** @5har0varik | **Created:** 2022-04-23 | **Updated:** 2022-04-23 | **Comments:** 5

> ## Expected Behavior
> Normal work, regular updates with stats and russian warship go fuck yourself
> 
> ## Actual Behavior
> After printing out config process exit with no error
> `root@ubuntu-s-1vcpu-1gb-ams3-01:~# docker run --rm -it --pull always --network host ghcr.io/arriven/db1000n
> latest:...

<details><summary>Comments (5)</summary>

- **@arriven** (2022-04-23): How much memory is available to the container?
- **@arriven** (2022-04-23): Actually I've got an idea on how to fix that high memory usage, should be working with less than 500mb memory available once 0.8.30 finishes building (shouldn't take more than 10 minutes)
- **@5har0varik** (2022-04-23): > How much memory is available to the container?  That's 1GB container. Once I was able to proceed to attack but no more.
- **@5har0varik** (2022-04-23): > Actually I've got an idea on how to fix that high memory usage, should be working with less than 500mb memory available once 0.8.30 finishes building (shouldn't take more than 10 minutes)  Looks...
- **@5har0varik** (2022-04-23): Looks like resolved: attack go on, but during config print there are lines: `{"level":"warn","ts":1650718985.1054173,"caller":"templates/templates.go:175","msg":"error executing...
</details>

## #513 Config errors and no requests / traffic reporting after changing the logger
**State:** CLOSED | **Author:** @roman-kruglov | **Created:** 2022-04-22 | **Updated:** 2022-04-25 | **Comments:** 4

> tons of errors like:
> ```
> {"level":"error","ts":1650644178.083019,"caller":"job/runner.go:193","msg":"error running job","name":"","type":"encrypted","error":"no identity matched any of the...

<details><summary>Comments (4)</summary>

- **@maksidon** (2022-04-22): Kind of the same for me as well ```txt {"level":"error","ts":1650643872.5228965,"caller":"utils/utils.go:20","msg":"caught panic, recovering","err":"runtime error: invalid memory address or nil...
- **@matherfather** (2022-04-22): Have the same cloud provider + protonvpn , manual
- **@arriven** (2022-04-22): All of those should be fixed in 0.8.29
- **@roman-kruglov** (2022-04-25): I think these particular defects are addressed and fixed, closing the issue
</details>

## #512 Please add possibility to configure multipart/form-data request from config
**State:** CLOSED | **Author:** @Vitalii-Gozhenko | **Created:** 2022-04-21 | **Updated:** 2022-04-22 | **Comments:** 2

> It would be nice to have possibility to config `multipart/form-data` requests from config. Currently it is not possible because there is no possibility to insert newline character into the body

<details><summary>Comments (2)</summary>

- **@arriven** (2022-04-21): Hmm, it should be possible to input newline characters to both json and yaml which are accepted formats here but I'll take a look tomorrow
- **@arriven** (2022-04-22): yup, it does work, you can probably take look here for examples on how to specify multiline strings in yaml...
</details>

## #511 Crash and OS reboot on MacOS Monterey
**State:** OPEN | **Author:** @serg-music | **Created:** 2022-04-19 | **Updated:** 2022-04-23 | **Comments:** 3

> ## Expected Behavior
> No crash
> 
> ## Actual Behavior
> MacOS hangs and reboot after a while of using db1000n
> 
> ## Steps to Reproduce the Problem
> 
>   1. install db100n >= 0.8.23
>   2. Run db1000n --scale 10
> 
> 
> ## Specifications
> 
>   - Version: 0.8.23 , 0.8.24
>   - Platform: MacOS
>   - Subsystem:...

<details><summary>Comments (3)</summary>

- **@arriven** (2022-04-19): v0.8.23 introduced [this commit](https://github.com/Arriven/db1000n/commit/8596be29fea9e8f63d0bdbeef236bf62e6b8c776) which increases OS limit on connections open by a program to its maximum. This...
- **@serg-music** (2022-04-19): removing --scale helped. No more crashes. However, it blocks me from using whole network bandwidth.   The issue blocks my hardware configuration from using --scale.
- **@barnyiv** (2022-04-23): @serg-music https://stackoverflow.com/questions/7578594/how-to-increase-limits-on-sockets-on-osx-for-load-testing try this, should help.
</details>

## #510 Zero requests sent
**State:** CLOSED | **Author:** @sash-ko | **Created:** 2022-04-18 | **Updated:** 2022-04-18 | **Comments:** 2

> How can I check that db1000n actually sends requests? "Traffic stats" shows that the number of requests sent is always zero but the number of requests attempted is higher than zero. I see the same results no matter how I run it - with or without VPN, from the command line or as a Docker container,...

<details><summary>Comments (2)</summary>

- **@arriven** (2022-04-18): Right now it seems like the targets are using some heavy geo blocking and I don't think we can do anything about it, admins are evaluating whether it's better to continue or change the target
- **@sash-ko** (2022-04-18): Thank you for the quick answer
</details>

## #509 Country check from russia under vpn is blocked
**State:** CLOSED | **Author:** @zeratulus | **Created:** 2022-04-16 | **Updated:** 2022-04-24 | **Comments:** 1

> db1000n used with ProtonVPN, Ubuntu 20.04 and under VirtualBox.
> 
> I think it bad idea to check country because roskomnadzor can use this to detect DDoS attacks by this app...

<details><summary>Comments (1)</summary>

- **@zeratulus** (2022-04-19): Today, after updates seems like country detection works fine... ProtonVPN + russia
</details>

## #504 Terraform Docker Container Update
**State:** CLOSED | **Author:** @slavarazum | **Created:** 2022-04-13 | **Updated:** 2024-08-09 | **Comments:** 9

> Is there any instructions how to update and manipulate db1000n installed by terraform to VPS server like DigitalOcean?

<details><summary>Comments (9)</summary>

- **@arriven** (2022-04-14): that depends on your usage but the most common way would depend on whether terraform definitions use latest image or pin it to some specific version  if it uses latest image you can just call...
- **@slavarazum** (2022-04-14): @Arriven No specific configurations, just deployed 2 VPS in DigitalOcean and Vultr by terraform with these...
- **@arriven** (2022-04-14): so Vultr deployment script already does restart the container regularly and pulls latest image. digital ocean example uses their app platform and I can't seem to find any autoupdate features there...
- **@arriven** (2022-04-14): @Amet13 if I recall correctly you are the author of DO terraform, are you aware of any better way to update the app there?
- **@slavarazum** (2022-04-14): @Arriven So, Vultr containers has autoupdate, great!  How can I check current db1000n version on VPS?
- **@arriven** (2022-04-14): for vultr something like `ssh root@ip docker container ls` should give you info about the container which should include image version. If it doesn't have that info you can also grep docker logs for...
- **@Amet13** (2022-04-14): >@Amet13 if I recall correctly you are the author of DO terraform, are you aware of any better way to update the app there?  For Digital Ocean it takes the latest code from master branch and...
- **@slavarazum** (2022-04-14): @Amet13 Just made redeploy on DO, result: ``` 2022/04/14 17:19:06.816548 main.go:51: DB1000n [Version: v0.0.1][PID=42] ```  On Vultr autoupdates works fine 👍
- **@Amet13** (2022-04-14): It's still the latest version, as DO automatically builds a binary and not getting it from github, that's why it shows you v0.0.1
</details>

## #503 What's the best way to keep the script running on the remote server?
**State:** CLOSED | **Author:** @iblessedi | **Created:** 2022-04-12 | **Updated:** 2022-04-17 | **Comments:** 2

> I have a VPS server and I run the script there. However for some reason after some time of running the script stops working with the error message
> 2022/04/11 19:22:47.306448 main.go:137: Terminating
> 
> I use the Ubuntu server and run the script with the command
> `nohup ./db100n > log.log...

<details><summary>Comments (2)</summary>

- **@arriven** (2022-04-13): it depends on your goals and skill. The easiest way would probably be to wrap it in a loop like this https://www.cyberciti.biz/faq/bash-infinite-loop/  more complex approach would use something...
- **@iblessedi** (2022-04-17): Ok, so here is my script, maybe will be useful for somebody: 1. Create a file called run.sh 2. Add there the following script:  ``` #!/bin/bash NUMBER_OF_PROCESSES=$(ps aux | grep db1000n |...
</details>

## #501 Scale up automatically based on available file descriptors
**State:** OPEN | **Author:** @roman-kruglov | **Created:** 2022-04-10 | **Updated:** 2022-04-11 | **Comments:** 3

> Why don't we (I may try too) implement something like checking the (maximum) available number of file descriptors (possible ports / sockets / connections) on app's start and automatically scaling the number of jobs up to something close to this limit?
> 
> On my Mac the default max number of...

<details><summary>Comments (3)</summary>

- **@roman-kruglov** (2022-04-10): idea based on this comment https://github.com/Arriven/db1000n/issues/491#issuecomment-1090686644
- **@arriven** (2022-04-11): that would probably be something more fit for https://github.com/Arriven/db1000n/discussions/500
- **@roman-kruglov** (2022-04-11): I meant the app itself assessing available resources and taking up as much as is possible. But after a bit of experimentation I see problems there - e.g. it was a piece of cake for my Mac, but...
</details>

## #499 Is there a command line option to scale down power of attack ?
**State:** OPEN | **Author:** @HongKilDong | **Created:** 2022-04-09 | **Updated:** 2022-04-09 | **Comments:** 1

> I see there is a command line option scale up power of attack, but I need to scale down. What options do I have ?

<details><summary>Comments (1)</summary>

- **@arriven** (2022-04-09): it's not a direct scale down but you can make it use less resources by providing `--min-interval` to have artificial pauses between requests. It expects a duration value like `--min-interval 1s` or...
</details>

## #498 Make it possible to send sequence of packets via packetgen `[enhancement, priority: low]`
**State:** CLOSED | **Author:** @arriven | **Created:** 2022-04-09 | **Updated:** 2022-04-16 | **Comments:** 1

> Right now we can only send packets created via single template. In order to implement attacks similar to slowloris we need to be able to send a custom sequence of packets. Example configuration for slowloris would be something like this:
> 
> ```yaml
> jobs:
>   - type: packetgen
>     args:
>      ...

<details><summary>Comments (1)</summary>

- **@arriven** (2022-04-16): fixed in https://github.com/Arriven/db1000n/commit/853980b0d13c69aa698a85f0ee18aafc36a1bb09
</details>

## #495 How can I make the CPU usage less than 100%?
**State:** OPEN | **Author:** @vkorohod | **Created:** 2022-04-06 | **Updated:** 2022-05-30 | **Comments:** 10

> How can I manage CPU usage?
> 
> ![1](https://user-images.githubusercontent.com/52861439/162080295-799f39eb-091c-497d-9fbc-74a60b4309b9.jpg)

<details><summary>Comments (10)</summary>

- **@arriven** (2022-04-07): Which version are you running? There were issues with that in the past
- **@zdytch** (2022-04-07): Right now I have the same 100% CPU issue with the latest docker version  always ghcr.io/arriven/db1000n:latest
- **@arriven** (2022-04-07): @zdytch docker doesn't pull new versions unless `--pull always` is specified. The app should output its version when started, what does it show for you?
- **@zdytch** (2022-04-07): Status: Image is up to date for ghcr.io/arriven/db1000n:latest 2022/04/07 08:00:05.589425 main.go:51: DB1000n [Version: v0.8.20][PID=1]
- **@vkorohod** (2022-04-07): @Arriven [db1000n_0.8.19_windows_386.zip](https://github.com/Arriven/db1000n/releases/download/v0.8.19/db1000n_0.8.19_windows_386.zip),...
- **@vkorohod** (2022-04-07): @Arriven maybe you need to run with some parameters? I just double click to launch.
- **@arriven** (2022-04-07): we would certainly benefit from `--debug` argument being specified to get some more details into what's going on
- **@roman-kruglov** (2022-04-07): guys, a bit more details from me about high CPU usage starting from this comment here https://github.com/Arriven/db1000n/issues/491#issuecomment-1091560082
- **@alexnest-ua** (2022-04-14): > Right now I have the same 100% CPU issue with the latest docker version >  > always ghcr.io/arriven/db1000n:latest  That is a problem of Docker Dekstop, not of any script.
- **@1o1o1** (2022-05-30): https://stackoverflow.com/questions/4208/windows-equivalent-of-nice  ;)
</details>

## #494 Add more text template functions `[enhancement, priority: low]`
**State:** OPEN | **Author:** @arriven | **Created:** 2022-04-06 | **Updated:** 2022-04-06 | **Comments:** 0

> Things to consider:
> - hash functions (sha, md5)
> - type conversions (string to byte slice and vice versa)
> - random bearer token generation

## #493 Always get latest version
**State:** OPEN | **Author:** @alexnest-ua | **Created:** 2022-04-06 | **Updated:** 2022-04-11 | **Comments:** 8

> Please, make your releases with the same program names, that in auto-scripts, we could just get the latest version from one link (otherwise I'm already tired of always changing it [here](https://auto-ddos.notion.site/auto-ddos/DDoS-new-b6f56bf8e4cd4eebb5abfc85cbd77f93) ...)
> 
> For example:...

<details><summary>Comments (8)</summary>

- **@sivillakonski** (2022-04-07): @alexnest-ua, the way the software like this is being released, it's quite normal to have it with different names since the name contains a version in it. Usually, it's people expect to see what...
- **@arriven** (2022-04-07): I was actually considering that some time ago but didn't find enough arguments to switch. I think I'll change the naming pattern for now and reevaluate switching back to normal usage once the war...
- **@alexnest-ua** (2022-04-07): > @alexnest-ua, the way the software like this is being released, it's quite normal to have it with different names since the name contains a version in it. Usually, it's people expect to see what...
- **@arriven** (2022-04-07): first of all, there is an auto update feature present in the app and you can even enable it with `--enable-self-update --restart-on-update`. The problem with it is that I don't have resources to test...
- **@alexnest-ua** (2022-04-09): > first of all, there is an auto update feature present in the app and you can even enable it with `--enable-self-update --restart-on-update`. The problem with it is that I don't have resources to...
- **@arriven** (2022-04-10): I agree that auto update is a nice feature and that it solves a lot of problems but the main reason that feature is experimental (and not enabled by default) is because I need to heavily tweak my...
- **@dzhonzojdberg** (2022-04-10): >   You say very clever things, frankly and logically. Thank you for explaining the problem. I would like to make a more significant contribution, but I lack programming skills, but I will try to...
- **@cyroth** (2022-04-11): If you're happy to handle updates outside of the app, you could try [Watchtower](https://github.com/containrrr/watchtower/) for anyone using it via Docker.
</details>

## #492 Errors. Version 0.8.18
**State:** CLOSED | **Author:** @udjfvnsaoepna | **Created:** 2022-04-05 | **Updated:** 2022-04-09 | **Comments:** 3

> Errors.
> **Windows 10**
> Version **0.8.18**
> Start by: db1000n.exe --proxy http://***.***.***.***/proxy.txt --scale 10
> Proxy format user:password@ip:port
> 
> **Update**: checked version **0.8.17**, also with errors
> 
> ```
> goroutine 25329 [semacquire, 1...

<details><summary>Comments (3)</summary>

- **@arriven** (2022-04-05): hmm, not yet sure about the error but there are couple things wrong with your proxy setup that are not related to that:  1. proxy format should include protocol, not only host:port pair (good...
- **@arriven** (2022-04-05): can you try running it without those commandline arguments to see if they are affecting the behavior in any way? (also if you would be able to determine which exact combination of args leads to this...
- **@arriven** (2022-04-05): ok, fix incoming in 0.8.19
</details>

## #491 Q: How to use this tool more effectively on my laptop?
**State:** OPEN | **Author:** @DDushkin | **Created:** 2022-04-04 | **Updated:** 2022-04-10 | **Comments:** 25

> ## Expected Behavior
> I have 64G RAM + bought a good VPN with no limitation on connections and I want to use your tool the most effectively I can on my machine. Can you recommend the way how to use it? 
> 
> ## Actual Behavior
> Right now I just run this through the docker command. Also tried the...

<details><summary>Comments (25)</summary>

- **@** (2022-04-04): I think the most effective way is to run a native binary on your MacOS, because running it inside an amd64 docker container includes x86_64 virtualization on arm + linux VM on your host machine, that...
- **@arriven** (2022-04-05): You can use --scale parameter to spawn more threads (i.e. ./db1000n --scale 10) but make sure your ulimit -n is configured to be high enough for that
- **@roman-kruglov** (2022-04-06): @Arriven What's the default for threads? Do we need to use it (--scale parameter) for any multi-core instance? Or is there a sane default? Maybe it should set it to the number of cores by default?
- **@arriven** (2022-04-06): I don't think scaling it based on the CPU capacity is a good idea since you are more likely to hit a limit on network capacity (or the amount of sockets you can open). TCP traffic generation doesn't...
- **@roman-kruglov** (2022-04-07): I guess adding information about increasing descriptors / sockets maximum number for different platforms would be very useful - on my Mac it was something like 256 by default, when the allowed...
- **@roman-kruglov** (2022-04-07): @Arriven as for CPU - I noticed the app loads CPU a lot when used with IPv6, like 100%. But when it's IPv4 only - it generates a low CPU load like maybe 12%. Mind I used different VPNs for that. And...
- **@arriven** (2022-04-07): could be, I don't think I've tested ipv6 functionality well enough, can you tell which specific resources you tried with ipv6?
- **@roman-kruglov** (2022-04-07): > could be, I don't think I've tested ipv6 functionality well enough, can you tell which specific resources you tried with ipv6?  Hotspot Shield VPN seems to have only IPv6 for their servers. And I...
- **@roman-kruglov** (2022-04-07): ``` 2022/04/07 11:35:19.784759 config.go:69: Failed to fetch config from "https://raw.githubusercontent.com/db1000n-coordinators/LoadTestConfig/main/config.v0.7.json": Get...
- **@arriven** (2022-04-07): hmm, I have one idea of a potential cause, does it manage to get the proper config at least once in the configuration where you get that 100% CPU load? There is a config embedded into the app as a...
- **@roman-kruglov** (2022-04-07): yep, confirm, when I used Hotspot VPN and I ran the app, it was able to get an initial list and I think it updated a few times ok, but then started having those issues with updating the list. But the...
- **@arriven** (2022-04-07): If it was able to fetch the config at least once it won't get back to embedded config and that means that the problem is somewhere else, could you maybe send me some debug logs (--debug)?
- **@** (2022-04-07): Hotspotshield is a transparent proxy for TCP (L4). Hotspotshield has a limited connection tracking table for concurrent TCP streams that are terminated and proxied.. So probably it can be an issue.
- **@zdytch** (2022-04-08): In my case, no VPN used. I start the docker container with clean command from the docs and it stops after 3-10 seconds. The output freezes at this stage:  ``` 2022/04/07 09:06:18.878204...
- **@arriven** (2022-04-08): is it the output with debug enabled?
- **@zdytch** (2022-04-08): @Arriven it's a standard output w/o debug. Is there a simple way to pass debug argument inside the docker container?
- **@arriven** (2022-04-08): Yup, just add --debug to the end of the commandline
- **@zdytch** (2022-04-08): > Yup, just add --debug to the end of the commandline  Easy enough, thanks The output: https://pastebin.com/3zYdaSDw  The container stops at this point
- **@arriven** (2022-04-08): hmm, I don't see anything suspicious in the log. The only cases where something like this has happened before involved the process being killed due to OOM. I'm not sure that it's the case here but...
- **@zdytch** (2022-04-08): Seems to be memory issue, indeed. The container was 1GB when the issue appeared. After I resized it to 2GB, it worked. But according to stats, the regular memory consumption is always lower than...
- **@arriven** (2022-04-08): I might need to debug that additionally because I've only been seeing spikes to ~700MB with general usage being under 200MB (there was a bug that could lead to a spike of 2+ GB but it's been fixed...
- **@zdytch** (2022-04-08): So, generally 1GB is more than enough, right? That's good, as running 2GB can be costly for multiple instances. I don't use any custom configuration, just the plain command from the docs. If you get...
- **@roman-kruglov** (2022-04-09): > If it was able to fetch the config at least once it won't get back to embedded config and that means that the problem is somewhere else, could you maybe send me some debug logs (--debug)?  The...
- **@arriven** (2022-04-09): @roman-kruglov there was an issue in the config that could lead to some increased CPU usage but it shouldn't be that significant. Considering the amount of cpu being used by hotspot shield I wonder...
- **@roman-kruglov** (2022-04-10): > @roman-kruglov there was an issue in the config that could lead to some increased CPU usage but it shouldn't be that significant. Considering the amount of cpu being used by hotspot shield I wonder...
</details>

## #490 Suggestion: gzip header
**State:** OPEN | **Author:** @matherfather | **Created:** 2022-04-04 | **Updated:** 2022-04-23 | **Comments:** 1

> Add to the headers or similar:
> Accept-Encoding: br;q=1.0, gzip;q=0.8, *;q=0.1
> 
> Potentially it will force server to use archiving which can use more mem/ cpu per request.

<details><summary>Comments (1)</summary>

- **@roman-kruglov** (2022-04-23): @Arriven I wanted to implement this, but it seems the config already has such capabilities: ```           "headers": {             "Accept-Encoding": "gzip,deflate", ``` Does it make sense to...
</details>

## #489 --proxy not working if country-check failed
**State:** CLOSED | **Author:** @PerchunPak | **Created:** 2022-04-04 | **Updated:** 2022-04-05 | **Comments:** 14

> ## Config
> ```json
> {
>     "jobs":[
>       {
>         "type":"http",
>         "count":5,
>         "args":{
>           "request":{
>             "method":"GET",
>             "path":"https://iplogger.org/*******"
>           },
>           "client":{
>             "static_host":{
>              ...

<details><summary>Comments (14)</summary>

- **@PerchunPak** (2022-04-04): Command for docker used in Windows system. I don't know if it will work on Linux, so here tested command **only for Linux**: `docker run -d --name db1000n-test -v **ABSOLUTE PATH TO FOLDER WITH...
- **@PerchunPak** (2022-04-05): Could be caused by: > you might need a lot of retries for countrychecker to find working proxy (default is 3 but I didn't manage to get a result with this list even with 15 retries)  In [this...
- **@arriven** (2022-04-05): I found what the actual underlying issue is: current implementation supports only socks5 proxies and falls back to direct connection for other protocols. I've only used socks5 proxies for my testing...
- **@arriven** (2022-04-05): fixed falling back to direct connection in https://github.com/Arriven/db1000n/commit/36af0e5488ea2e4f962bd2601d7777facbd13760  looking on how to make it accept http and socks4 proxies as well
- **@arriven** (2022-04-05): fixed in v0.8.18 (being built right now)
- **@PerchunPak** (2022-04-05): Something with 0.8.18 really wrong. Command `docker run --rm --name db1000n ghcr.io/arriven/db1000n --proxy "{{ join (split (get_url...
- **@arriven** (2022-04-05): what exactly is wrong in that log? or you mean that it takes long time to output targets?
- **@arriven** (2022-04-05): ah, I see, you didn't redirect stderr to the log
- **@arriven** (2022-04-05): 0.8.19 with the fix incoming (I forgot that map is a reference type in go)
- **@PerchunPak** (2022-04-05): Seems like it force to use third proxy, even if it not working. ``` 2022/04/05 17:01:13.088470 main.go:51: DB1000n [Version: v0.8.19][PID=1] 2022/04/05 17:01:13.190811 countrychecker.go:57:...
- **@PerchunPak** (2022-04-05): Also, how about add timeout for switch proxies? Should I open new feature request?
- **@arriven** (2022-04-05): proxies used in countrycheck are independent from proxies used in actual jobs, you can check that same example with iplogger (great resource btw, thanks for it!) and see that you get a bunch of...
- **@arriven** (2022-04-05): example from my testing ![image](https://user-images.githubusercontent.com/20084245/161816895-ebfa922d-b9bf-4d85-b2db-0ced974333d4.png)
- **@PerchunPak** (2022-04-05): Working, thanks
</details>

## #486 Telegram Channel Coordination
**State:** CLOSED | **Author:** @app/ | **Created:** 2022-04-04 | **Updated:** 2022-04-04 | **Comments:** 2

> I'm thinking about central coordination based on telegram channels. Like IRC-channels were used for DDoS coordination earlier.
> For instance, I  trust this channel https://t.me/itarmyofukraine2022, they don't have some machine-readable format but probably we can ask moderator to do that. 
> 
> Any...

<details><summary>Comments (2)</summary>

- **@arriven** (2022-04-04): The targets are already controlled by their admins ;)
- **@** (2022-04-04): > The targets are already controlled by their admins ;)  @Arriven , Is there a compatible with db1000n json list of targets?
</details>

## #485 Android Application
**State:** OPEN | **Author:** @app/ | **Created:** 2022-04-04 | **Updated:** 2022-05-31 | **Comments:** 14

> I'm thinking about simple Android application.
> We can pack armv6-compatible ELF binary and just run it inside for PoC.
> Your thoughts?

<details><summary>Comments (14)</summary>

- **@arriven** (2022-04-04): I'm not sure if it would be very useful but I certainly wouldn't mind if someone were to make a mobile version. The only note I have is that it would be best to keep it as a separate repository to...
- **@** (2022-04-04): Not much progress, but I started to work on Android app, because friends asked about it: https://github.com/FPavlovskiy/Dzida
- **@roman-kruglov** (2022-04-06): I would run it on my phones too, just imagine the possible number of additional.. load testers. Everybody has one (a phone). Provided easy instructions.. the army of testers would grow...
- **@** (2022-04-07): > But imo it would be easier to see the releases here than to follow another repo. Also for every release of the app there should ideally be a release of an android app, right? so, it would be...
- **@arriven** (2022-04-07): The way I see it: you download android app once (or at least less frequently) and maintainer of that app regularly check for compatibility between the app and latest version of db1000n and just...
- **@roman-kruglov** (2022-04-10): @FPavlovskiy maybe this discussion could help https://github.com/Arriven/db1000n/discussions/465
- **@Andrii-Asiox** (2022-05-09): > Not much progress, but I started to work on Android app, because friends asked about it: https://github.com/FPavlovskiy/Dzida @FPavlovskiy  I use termux and arm version of db1000n on android...
- **@roman-kruglov** (2022-05-09): I'm intending to look into making an android app, but one which even a grandma could use - using termux is imo too complicated for non technically astute folks.  I would prefer to make a simple...
- **@** (2022-05-30): @roman-kruglov , I managed to build `fyne` app from https://github.com/Arriven/db1000n/discussions/465 and contacted code owner. Probably it is quickest solution and we will be able to merge it to...
- **@arriven** (2022-05-30): > @roman-kruglov , I managed to build `fyne` app from https://github.com/Arriven/db1000n/discussions/465 and contacted code owner. Probably it is quickest solution and we will be able to merge it to...
- **@** (2022-05-30): Ok, in this case it makes sense to use db1000n as submodule, but not as a monorepo to simplify patching
- **@roman-kruglov** (2022-05-31): @FPavlovskiy @arriven I was just working on it for several days. Had to use `fyne` too, no support for even a minimal GUI in gomobile. But my findings are - I can't embed a terminal emulator written...
- **@roman-kruglov** (2022-05-31): here it goes https://github.com/arriven/db1000n/pull/547
- **@** (2022-05-31): @roman-kruglov it was my plan as well. 1. Fork an OSS terminal emulator 2. Add code to download armv7 or armv8 `db1000n` binary 3. Run `elf` binary on the app start  But then I started to...
</details>

## #482 introduce timeout job `[enhancement, priority: low]`
**State:** CLOSED | **Author:** @arriven | **Created:** 2022-04-02 | **Updated:** 2022-04-04 | **Comments:** 3

> more tools to make complex scenarios

<details><summary>Comments (3)</summary>

- **@oherych** (2022-04-02): Can you please provide some examples?
- **@arriven** (2022-04-03): You can find some utility jobs in `src/job/util.go` and use them as a reference
- **@arriven** (2022-04-04): fixed by https://github.com/Arriven/db1000n/commit/ccecdf8e628af2e35b1c50987c43b19a90cb5c8e
</details>

## #481 introduce utility job wrapper to eat the error of a wrapped job `[enhancement, priority: low]`
**State:** CLOSED | **Author:** @arriven | **Created:** 2022-04-02 | **Updated:** 2022-04-04 | **Comments:** 1

<details><summary>Comments (1)</summary>

- **@arriven** (2022-04-04): fied by https://github.com/Arriven/db1000n/commit/a5190cae7be8225abe4a961dee0899136ee0d547
</details>

## #480 replace rawnet jobs with packetgen
**State:** CLOSED | **Author:** @arriven | **Created:** 2022-04-02 | **Updated:** 2022-04-04 | **Comments:** 1

> as of 0.8.15 (or 0.8.14, not sure) packetgen fully covers the functionality of rawnet jobs. Need to change them to just spawn a packetgen job with proper params for backward compatibility

<details><summary>Comments (1)</summary>

- **@arriven** (2022-04-04): fixed in https://github.com/Arriven/db1000n/commit/2c15d5f06f0facfe38b0af4ef5ebafa5f55b6f38
</details>

## #475 Proxy not work for Windows
**State:** CLOSED | **Author:** @OleksandrBlack | **Created:** 2022-04-01 | **Updated:** 2023-12-11 | **Comments:** 5

> ## Expected Behavior
> ![work](https://user-images.githubusercontent.com/13917465/161261358-b0e21332-6863-46b9-b33e-a0594bb084ec.jpg)
> 
> ## Actual Behavior
> ![win_error](https://user-images.githubusercontent.com/13917465/161260849-28f14f9c-7530-4ffc-be32-7ff2dc58fa87.jpg)
> 
> 
> ## Steps to Reproduce...

<details><summary>Comments (5)</summary>

- **@HongKilDong** (2022-04-02): I have the same issue on ubuntu
- **@arriven** (2022-04-03): Could you try it in powershell? I'm not an expert in windows commandline syntax so in case PowerShell doesn't work we'd need someone who's experienced in it to have a look on how to properly escape...
- **@PerchunPak** (2022-04-03): Fixed it by specify `--proxy "{{ join (split (get_url \"https://raw.githubusercontent.com/porthole-ascend-cinnamon/proxy_scraper/main/proxies.txt\") \"\n\") \",\" }}"` (replace all `"` with `\"` and...
- **@OleksandrBlack** (2022-04-04): >   ![err2](https://user-images.githubusercontent.com/13917465/161477768-a2102251-a181-49f0-9c15-e1db3e2cef1a.jpg) Not work @Arriven   can be simplified? just provide a link --proxylist...
- **@vasyl-bhd** (2022-04-05): Hi!  Have the same issue on my Digital Ocean instance. Is there any way to type country manually, OR bypass this check somehow?
</details>

## #472 Implement compatibility layer between snake case and camel case in utils.Decode `[enhancement, priority: low]`
**State:** CLOSED | **Author:** @arriven | **Created:** 2022-03-31 | **Updated:** 2022-03-31 | **Comments:** 2

> For historical reasons config values use snake_case and we need to support backward-compatibility right now. Need to implement a compatibility layer that would convert snake case to camel case when decoding and remove all mapstructure tags so that all the configs can both be in snake and camel case

<details><summary>Comments (2)</summary>

- **@arriven** (2022-03-31): based on initial assessment it should be possible to simply remove "_" from keys and provide a map of overrides for potential cases where I could introduce a shorter name in mapstructure tags
- **@arriven** (2022-03-31): fixed in 8de49ba441d51531358c1facf940da0961bd484c
</details>

## #471 Add more protocols to packetgen `[enhancement, help wanted, priority: medium]`
**State:** OPEN | **Author:** @arriven | **Created:** 2022-03-31 | **Updated:** 2022-04-09 | **Comments:** 2

> List of higher priority protocols to include (can be extended):
> 
> - [x] [HTTP](https://github.com/Arriven/db1000n/blob/8563935e67802cfeb46d04c9776f8ba68a725770/src/core/http/http.go#L66)
> - [ ] [TLS](https://pkg.go.dev/github.com/google/gopacket/layers#TLS)
> - [ ]...

<details><summary>Comments (2)</summary>

- **@arriven** (2022-03-31): Note: tls support over tcp is added in 66a620360432462064f3be19a532cbb688768b47 but ideally we still want to be able to send tls payload over raw connections
- **@arriven** (2022-04-09): http support added in https://github.com/Arriven/db1000n/commit/fa3d25fe832bc0a7bb92a09402313faf10a13da1
</details>

## #470 Make packetgen work over regular tcp/udp connections `[enhancement, priority: medium]`
**State:** CLOSED | **Author:** @arriven | **Created:** 2022-03-31 | **Updated:** 2022-03-31 | **Comments:** 1

> Need to make a `packetgen.Connection` interface that would have a single `Write(packetgen.Packet)` with implementations based on `net.Conn` and `ipv6.PacketConn`. `net.Conn` implementation should also support socks5 proxies similar to rawnet tcp jobs

<details><summary>Comments (1)</summary>

- **@arriven** (2022-03-31): implemented in 8b0bdac65db43dab9b57fb5a30c3fdf5f01aba0b
</details>

## #469 Packetgen improvements `[enhancement, priority: medium]`
**State:** OPEN | **Author:** @arriven | **Created:** 2022-03-31 | **Updated:** 2022-03-31 | **Comments:** 0

> Packetgen can be further improved in following ways:
> 
> - [x] #470
> - [ ] #471

## #464 can't connect to container
**State:** CLOSED | **Author:** @industral | **Created:** 2022-03-30 | **Updated:** 2022-03-30 | **Comments:** 4

> ```
> root@xxx:~# docker exec -it root_db100_proxy_15_1 /bin/sh
> OCI runtime exec failed: exec failed: container_linux.go:380: starting container process caused: exec: "/bin/sh": stat /bin/sh: no such file or directory: unknown
> root@xxx:~# docker exec -it root_db100_proxy_15_1 sh
> OCI runtime exec...

<details><summary>Comments (4)</summary>

- **@bitshape** (2022-03-30): Starting from v0.8.4 it’s using `ko` “distro-less” Docker builds so you can’t get into interactive mode as there’s no `bin/sh` anymore.
- **@industral** (2022-03-30): thanks for reply! so how to check let's say if container has internet or to do something else?
- **@arriven** (2022-03-30): you can, however, use db1000n-advanced for that, which is still based on alpine
- **@industral** (2022-03-30): thanks @Arriven !
</details>

## #463 C/C++ port
**State:** CLOSED | **Author:** @oxbee | **Created:** 2022-03-30 | **Updated:** 2022-03-30 | **Comments:** 2

> Let's say I have shell (SSH) access to device which would like to execute db1000n. But unfortunately nor docker or GO is available there.
> Thus, I would like to port db1000n into platform dependent executable via gcc / g++ compilation.
> Since i'm only C/C++ developer and know nothing about GO, i...

<details><summary>Comments (2)</summary>

- **@oxbee** (2022-03-30): Ok, after checking documentation I've found this magnificent  [link](https://github.com/Arriven/db1000n/releases/latest)
- **@arriven** (2022-03-30): I wish I could see your reaction when you find shell install script I crafted specifically for that case :) https://github.com/Arriven/db1000n/blob/main/docs/advanced-docs/advanced-and-devs.md
</details>

## #461 Is Seagull able to improve Your tool?
**State:** CLOSED | **Author:** @bw-development | **Created:** 2022-03-30 | **Updated:** 2022-03-31 | **Comments:** 1

> ## Expected Behavior
> Generate traffics that difficult to effectively block/recognize by gate fw/ids systems of target
> 
> About Seagull
> http://gull.sourceforge.net/index.html

<details><summary>Comments (1)</summary>

- **@arriven** (2022-03-30): I don't think I would be able to import it directly (using CGO would make it pain in the ass to support different platforms) but based on my initial overview of it I feel like my packetgen package...
</details>

## #457 After upgrade generated load is very very low
**State:** CLOSED | **Author:** @barnyiv | **Created:** 2022-03-29 | **Updated:** 2022-03-30 | **Comments:** 7

> ## Expected Behavior
> 100% cpu load
> 
> ## Actual Behavior
> 1-5% cpu load
> 
> ## Steps to Reproduce the Problem
> 
>   1. use 0.8.12 darwin arm64
>   
> Latest version that is working fine for me was 0.8.9. After upgrade to 0.8.12 issue occurred.
> 
> ## Specifications
> 
>   - Version: 0.8.12
>   - Platform:...

<details><summary>Comments (7)</summary>

- **@arriven** (2022-03-29): Most likely that 100% cpu usage was caused by a bug where the app was incorrectly handling OS limitations. Expecting 100% cpu load from the app that generates network load would be wrong as you...
- **@barnyiv** (2022-03-29): @Arriven ok, thanks, so whats the --scale should be for maximum load? or it's different for every machine?
- **@localdotcom** (2022-03-29): > @Arriven ok, thanks, so whats the --scale should be for maximum load? or it's different for every machine?  It depends on CPU cores and memory size.
- **@barnyiv** (2022-03-29): Ok, I've just tried with --scale [16, 32, 64, 128] For 1 m each it generated --------------> [104, 209, 411, 750] mbs of traffic respectively  should I just crank it up even more? I don't...
- **@arriven** (2022-03-30): It depends, the easiest way would be to compare response rate. If it goes down by a noticeable percentage after you increased the scale - most likely you've hit the limit Also be aware that a lot of...
- **@barnyiv** (2022-03-30): Response rate is 0%, doesn't matter at what scale.
- **@arriven** (2022-03-30): Seems like current default targets changed their IP addresses and started using qrator, in this case scaling the app won't really help until we switch targets
</details>

## #455 Please compile for FreeBSD 13.0-RELEASE amd64
**State:** CLOSED | **Author:** @bw-development | **Created:** 2022-03-29 | **Updated:** 2022-03-30 | **Comments:** 3

> There are a lot of FreeBSD users here in US, who glad to help Ukraine.
> (And many of them are students and hardware technicians, so old machines also may be used. Not to forget about i386 platform ;)
> 
> Thank You and good luck!

<details><summary>Comments (3)</summary>

- **@arriven** (2022-03-29): Added freebsd and bunch of other OS types (everything that compiled successfully) in 0.8.13, but can't guarantee it would work flawlessly as not enough testing was done
- **@bw-development** (2022-03-29): > Added freebsd and bunch of other OS types (everything that compiled successfully) in 0.8.1  Thank You so much! So, no any warnings during compilation?   > but can't guarantee it would work...
- **@arriven** (2022-03-30): Well, there's almost no OS-specific code there (I can inly recall auto update which is not a core feature) so as long as libraries support that OS there shouldn't be any problems. You could get...
</details>

## #454 Windows version doesn't start for me
**State:** CLOSED | **Author:** @yetamzd | **Created:** 2022-03-28 | **Updated:** 2022-03-29 | **Comments:** 8

> Hello! Can somebody help me please? My Windows version just doesn't work. I click on the file, it opens for a moment and then just closes. I've tried to reinstall the file for a couple of times, I've runned it with administrative rights, but nothing changed. I don't really understand all that...

<details><summary>Comments (8)</summary>

- **@arriven** (2022-03-29): Can you try launching it via terminal to see the logs? You can do that by searching for "cmd" or "PowerShell" in the start menu, then dragging the executable to that window (it will input the proper...
- **@yetamzd** (2022-03-29): That's what I got:  panic: runtime error: invalid memory address or nil pointer dereference [signal 0xc0000005 code=0x0 addr=0x4 pc=0x11875aa]  goroutine 1 [running]: main.main()        ...
- **@arriven** (2022-03-29): Hmm, which version are you running? The error message seems quite weird and would only be plausible if you are running something like v0.4.3 but I assume it's not the case?
- **@yetamzd** (2022-03-29): I don't know for sure which version I use, because I downloaded the file by the link posted in Telegram. But I guess that's the case, because the link was posted 1 month ago. So maybe I just need to...
- **@arriven** (2022-03-29): You can get the latest download link at https://arriven.github.io/db1000n/
- **@yetamzd** (2022-03-29): When I click on the download link, I get "Not found" error :(
- **@arriven** (2022-03-29): oops, forgot one update scenario, should be working now
- **@yetamzd** (2022-03-29): Thank you for help! Works perfectly!
</details>

## #450 Docker compose UPDATER_MODE type problem
**State:** CLOSED | **Author:** @andser | **Created:** 2022-03-27 | **Updated:** 2022-03-28 | **Comments:** 0

> ## Expected Behavior
> Should successfully run containers
> 
> ## Actual Behavior
> `
> $ docker-compose -f examples/docker/static-docker-compose.yml up
> ERROR: The Compose file './examples/docker/static-docker-compose.yml' is invalid because:
> services.updater.environment.UPDATER_MODE contains true,...

## #448 Introduce exponential backoff to some jobs `[enhancement, help wanted, priority: high]`
**State:** CLOSED | **Author:** @arriven | **Created:** 2022-03-27 | **Updated:** 2022-03-27 | **Comments:** 1

> Due to the nature of the app we usually ignore errors in loops that are caused by network errors (in case targets are temporary unavailable). This causes CPU usage problems when the actual error happens completely locally due to a misconfiguration (i.e. errors parsing address or ulimit related...

<details><summary>Comments (1)</summary>

- **@arriven** (2022-03-27): I'll only be able to properly work on it myself tomorrow so if someone wants to jump in - feel free to do so
</details>

## #447 Руський — це не правильно
**State:** CLOSED | **Author:** @adronstar | **Created:** 2022-03-27 | **Updated:** 2022-03-30 | **Comments:** 2

> Руський — це не правильно, бо Руський походить від слова Русь, тобто це історично — древня Україна, до чого росія не має жодного відношення.
> 
> Краще використовувати слово "русский", або "російський", чи "московитський" 
> 
> **Русский воєнний корабль іди нахуй!** 
> **Слава Україні!**

<details><summary>Comments (2)</summary>

- **@arriven** (2022-03-27): Already fixed in latest release AFAIR
- **@arriven** (2022-03-27): Even better - it's fixed starting from v0.8.8
</details>

## #444 Service "updater" is missing a healthcheck configuration
**State:** CLOSED | **Author:** @industral | **Created:** 2022-03-27 | **Updated:** 2022-03-29 | **Comments:** 3

> running docker-compose get the following issue
> 
> ```
> ERROR: for db1000n_38  Service "updater" is missing a healthcheck configuration
> 
> ERROR: for db1000n_31  Service "updater" is missing a healthcheck configuration
> 
> ERROR: for db1000n_03  Service "updater" is missing a healthcheck...

<details><summary>Comments (3)</summary>

- **@arriven** (2022-03-27): @bitshape seems like "service_started" condition also requires a healthcheck to be defined. I suggest we just enable pprof endpoint on it and use that endpoint/port availability as a healthcheck? Not...
- **@bitshape** (2022-03-27): @Arriven @industral No, it definitely doesn't need health check to be define for `service_started`: https://docs.docker.com/compose/compose-file/compose-file-v2/#depends_on  > In the above example,...
- **@industral** (2022-03-29): fixed in master code
</details>

## #443 Problem in v.0.8.9
**State:** CLOSED | **Author:** @mrdrebot | **Created:** 2022-03-27 | **Updated:** 2022-03-27 | **Comments:** 4

> ## Expected Behavior
> Turn on VPN and start file db1000n.exe, all should work.
> 
> ## Actual Behavior
> I use VPN in Chrome - Browsec VPN - Free VPN for Chrome and it work. I got new window with the list of th VPNs. In v.0.8.8 all worked good with this VPN and I didn`t get any window. If I stated...

<details><summary>Comments (4)</summary>

- **@Geniy00** (2022-03-27): I think that chrome extension doesn't mean that other apps on your PC use VPN. You need to run special VPN program for Windows, then db1000n will really use VPN
- **@arriven** (2022-03-27): There shouldn't be any significant difference between 0.8.8 and 0.8.9 so I'm almost completely sure the problem is related to the vpn setup itself but I'll take another look
- **@mrdrebot** (2022-03-27): Hello again!  When I use Browsec VPN - Free VPN for Chrome (see picture_1) my ip doesn`t changes for your program but your program write that all Ok and attack work and config download, see...
- **@mrdrebot** (2022-03-27): Hello!  Ignor my letter, you repaired all in new version.  27 березня 2022, 16:07:30, від "Maxim Drebot" ***@***.***>:  Hello again!  When I use Browsec VPN - Free VPN for Chrome (see...
</details>

## #439 Updater dont work in docker-compose
**State:** CLOSED | **Author:** @Pandanom | **Created:** 2022-03-26 | **Updated:** 2022-03-27 | **Comments:** 13

> ## Expected Behavior
> db1000n in updater mode, should fetch configuration bypassing VPN and store it in shared volume
> 
> ## Actual Behavior
> 
> Creating network "db1000nexpvpn_default" with the default driver
> Creating db1000nexpvpn_updater_1 ... error
> Creating autoheal                ......

<details><summary>Comments (13)</summary>

- **@arriven** (2022-03-26): @bitshape AFAIR you've been doing this docker compose? Can you take a look while I'm in a bunker?
- **@arriven** (2022-03-26): Ah wait, I think I know what could be the cause, can you try changing compose to use entrypoint instead of command or vice versa? (excluding exe name and leaving just arguments) Or alternatively...
- **@arriven** (2022-03-26): https://github.com/Arriven/db1000n/blob/main/src/runner/config/updater.go#L15 This one, it's more common to configure containers via environment variables rather then commandline flags and most other...
- **@Pandanom** (2022-03-26): Like this? It starts as regular db1000n  >     updater: >         image: ghcr.io/arriven/db1000n:latest >         restart: unless-stopped >         labels: >           autoheal: "true" >     ...
- **@arriven** (2022-03-26): @Pandanom something like this  ``` # [OPTIONAL]   # run db1000n in updater mode, which will fetch configuration bypassing VPN and store it in shared volume   updater:     image:...
- **@arriven** (2022-03-26): I have a feeling that healthcheck could be broken also since I've switched to a distroless image
- **@bitshape** (2022-03-26): @Arriven I’m taking a look
- **@bitshape** (2022-03-26): @Arriven check linked PR. I don't think it's `ko` issue, it's just that `--updater-mode` exists when it should not.
- **@bitshape** (2022-03-26): @Pandanom in addition to the fix proposed above, I think your config also needs some changes:  ```yaml updater:   image: ghcr.io/arriven/db1000n:latest   restart: unless-stopped   labels:    ...
- **@PerchunPak** (2022-03-26): @bitshape seems like you looking to old config, here all real changes that you made comparing with upstream (left - yours, right -...
- **@bitshape** (2022-03-26): @PerchunPak 👍 none of those parts are required and really depend on your particular setup so I omitted them from my suggestion on purpose.
- **@bitshape** (2022-03-26): @Arriven you might be right about `ko` but it doesn't seem to be related to the healthcheck.  v0.8.3 (pre ko build) Docker container runs fine v0.8.4 (ko introduced) this version isn't...
- **@bitshape** (2022-03-26): Part 2 of the fix: https://github.com/Arriven/db1000n/pull/442  1) If you're using health check for Docker containers, this is no longer is going to work 2) Volume mount path needs to be changed...
</details>

## #438 Download links in docs are broken
**State:** CLOSED | **Author:** @qyurila | **Created:** 2022-03-26 | **Updated:** 2022-03-27 | **Comments:** 3

> ## Expected Behavior
> 
> The download links work properly.
> 
> ## Actual Behavoir
> 
> The download links lead you to Not Found page.
> 
> ## Additional Information
> 
> Since 854f943f1964376dea4c0873fd8e10a781d663be commited, the filename scheme of released files have changed so that their version fields...

<details><summary>Comments (3)</summary>

- **@arriven** (2022-03-26): Oops, forgot about that one, will fix shortly
- **@arriven** (2022-03-26): Should be fixed now
- **@qyurila** (2022-03-27): Thank you!
</details>

## #435 Error while fetching config
**State:** OPEN | **Author:** @tvoretsmira | **Created:** 2022-03-26 | **Updated:** 2023-03-16 | **Comments:** 14

> ## Expected Behavior
> The config is expected to be fetched.
> 
> ## Actual Behavior
> 2022/03/26 10:47:04.100470 config.go:58: Failed to fetch config from "https://ra
> w.githubusercontent.com/db1000n-coordinators/LoadTestConfig/main/config.v0.7.jso
> n": Get...

<details><summary>Comments (14)</summary>

- **@arriven** (2022-03-26): Can you check if you can access that URL in browser or with curl? Most likely this is a connection problem (could be caused by VPN, I can point you to possible workarounds in that case)
- **@tvoretsmira** (2022-03-26): Upgraded to v0.8.9, issue persists.  I cannot access URL from Google Chrome when VPN is turned on. But I can do it if VPN is off.  I have tried another country in VPN. Google Chrome was able to...
- **@michaelKaefer** (2022-03-27): Same here (using v0.8.10 via Docker on Ubuntu): ```console $ docker run --rm -it --pull always ghcr.io/arriven/db1000n latest: Pulling from arriven/db1000n Digest:...
- **@arriven** (2022-03-27): @michaelKaefer you can try running the container with --network host or you can try a solution with one instance of db1000n running as updater publishing local copy of the config fetching it without...
- **@arriven** (2022-03-27): @tvoretsmira I'll try to write a quick command that would allow you to use a set of http proxies instead of relying on VPN but that might be less effective
- **@tvoretsmira** (2022-03-27): A lot depends on VPN. v0.8.10 with VPN in China does not display any config fetching error.
- **@bitshape** (2022-03-27): @tvoretsmira @michaelKaefer try following this example: https://github.com/Arriven/db1000n/blob/main/examples/docker/static-docker-compose.yml  This is exactly why I added updater mode to reliably...
- **@tvoretsmira** (2022-03-28): How do I use this file?
- **@arriven** (2022-03-28): @tvoretsmira as of v0.8.12 you can use this command without VPN to use `porthole-ascend-cinnamon` proxylist instead: `./db1000n --proxy '{{ join (split (get_url...
- **@arriven** (2022-03-28): obviously you should use `./db1000n.exe` instead of `./db1000n` on windows and can use it with docker run by just appending that `--proxy` flag to the end of the appropriate command
- **@tvoretsmira** (2022-03-28): Current version of docker does not seem to support Win7 x64. I had no success installing it. I'm still able to find VPN that causes no problems. Unfortunately, those VPN are not in Russia or...
- **@arriven** (2022-03-28): yes, in terms of effectiveness I'd put them in the following order: 1. VPN into "friendly" country 2. VPN into any country other than Ukraine 3. "Friendly" Proxies 4. Any non-Ukrainian...
- **@hobbsit** (2022-03-30): The problem for me was an overly persistent ovpn tunnel interface that would not refresh. Steps I took:  - Removing this tun interface: openvpn --rmtun --dev $tunX - Resetting VPN to the most...
- **@vadyochik** (2023-03-16): there is also a problem with outdated config - when the first github's url has failed for some reason, the other 2 bitbucket's ones are not actual. The one doesn't exist any more (404 error) and the...
</details>

## #434 App crashed on some azure linux vw
**State:** CLOSED | **Author:** @dberezhnenko | **Created:** 2022-03-26 | **Updated:** 2022-03-26 | **Comments:** 2

> When i run application with default config it halt after some target with output "Killed"
> -debug option doesnt show anything.
> 
> Last attacked target could be different on several runs in row.
> Problem repeated at several WM without any logic. Just today I stopped one process (which worked all...

<details><summary>Comments (2)</summary>

- **@arriven** (2022-03-26): Most likely it's being killed due to OOM, you can try disabling Prometheus and encryption to decrease memory usage and leave only essential functionality. There's been an instruction in one of the...
- **@dberezhnenko** (2022-03-26): it seems your advice helpped.  With options -prometheus_on=false -skip-encrypted=true app is working!
</details>

## #433 There is no any status indication in the Console output whether an attack is successful or not
**State:** CLOSED | **Author:** @oleg-bronzhaiev | **Created:** 2022-03-26 | **Updated:** 2022-03-26 | **Comments:** 1

> ## Expected Behavior
> **There is** some status indication in the Console output whether an attack is successful or not.
> At least, this could be fixed to the indication as it was in the prev version db1000n-**v0.8.2**-windows-amd64:
> "Атака проводиться успішно! Руський воєнний корабль іди...

<details><summary>Comments (1)</summary>

- **@arriven** (2022-03-26): Fixed in #436
</details>

## #432 Traffic stats are not displayed
**State:** CLOSED | **Author:** @sq2mo | **Created:** 2022-03-26 | **Updated:** 2022-03-26 | **Comments:** 3

> ## Expected Behavior
> 
> "Traffic stats" banner displayed periodically.
> 
> ## Actual Behavior
> 
> "Traffic stats" banner not displayed.
> The only visible logs are:
> config.go:63: Loading config from...

<details><summary>Comments (3)</summary>

- **@tvoretsmira** (2022-03-26): The same behavior is observed for Windows 7 x64.
- **@arriven** (2022-03-26): Fixed in #436 The issue was there from the very beginning but only manifested now due to issues with Google analytics backend, we've changed the code to output logs regardless of that
- **@sq2mo** (2022-03-26): Just tested and v0.8.9 works ok, closing.
</details>

## #427 Russian warship
**State:** CLOSED | **Author:** @stiltjack | **Created:** 2022-03-25 | **Updated:** 2022-03-25 | **Comments:** 1

> Any chance of getting rid of the "go fuck yourself"? It was funny the first time, less so the 500th time. How will people take you seriously?

<details><summary>Comments (1)</summary>

- **@arriven** (2022-03-25): yes, but after the war ends. Right now I consider that message to be more of a tribute rather than just something funny (google the origin if you want)
</details>

## #424 Підтримка проксі
**State:** CLOSED | **Author:** @OleksandrBlack | **Created:** 2022-03-25 | **Updated:** 2022-03-31 | **Comments:** 20

> https://github.com/Arriven/db1000n/issues/389
> 
> Завжди актуальний список проксі який використовується для спільної мети.
> https://github.com/porthole-ascend-cinnamon/mhddos_proxy/blob/820defda23342fdaf90f2149d94b3464099d155b/runner.py#L15
> 
> Розробник
> https://github.com/porthole-ascend-cinnamon

<details><summary>Comments (20)</summary>

- **@SomalianCoolhacker** (2022-03-26): За власним спостереженням додам, що переважна частина спільнот перейшла на цю програму саме завдяки відсутності мороки з VPN. Звісно, ті хто тямить прикрутять OpenVPN чи ротацію проксі прямо в...
- **@arriven** (2022-03-28): For anyone who want's to use this proxylist you can use following commandline flag: `--proxy '{{ join (split (get_url...
- **@arriven** (2022-03-28): You can also pass that argument via `SYSTEM_PROXY` environment variable, i.e. `SYSTEM_PROXY='{{ join (split (get_url...
- **@arriven** (2022-03-28): Please note that it only works starting from v0.8.12 release as `split <string> "\n"` was a bit broken before that
- **@OleksandrBlack** (2022-03-28): https://github.com/Arriven/db1000n/commit/dbd53bfbb9e02357fcb8598e718366f663dc9e46  --proxy '{{ join (split (get_url...
- **@OleksandrBlack** (2022-03-28): [Arriven](https://github.com/Arriven) Doesn't work for Windows ![error](https://user-images.githubusercontent.com/13917465/160397035-de5617cb-7d83-44f8-8b23-747e51c5fcdd.jpg)
- **@arriven** (2022-03-28): hmm, might be something to do with how powershell/cmd handle string arguments. Can you check if that approach works for you if you put everything into a docker-compose file like...
- **@OleksandrBlack** (2022-03-28): > hmm, might be something to do with how powershell/cmd handle string arguments. Can you check if that approach works for you if you put everything into a docker-compose file like this? >  >...
- **@arriven** (2022-03-28): Yeah, proxies get down often. In mhddos it first tries to check if the proxy is working and only then starts using it for DDoS. My implementation just uses the proxy straight away and falls back to a...
- **@arriven** (2022-03-29): To reiterate: those last error messages (`error sending request {"error": "socks connect ..."}`) indicate that the app has successfully parsed provided proxylist and uses it. Errors are there just...
- **@industral** (2022-03-29): autohealer service is not needed in case of using proxy, am I right?
- **@arriven** (2022-03-29): yeah, it shouldn't be needed
- **@industral** (2022-03-29): few things here. We need ability to:  1. reconnect to another IP after some time, in case IP will be blocked (either via ENV parameter with time or via docker exec command to send to container to...
- **@industral** (2022-03-29): Also, I'm not sure if proxy works...  I can't see it from logs  ``` 2022/03/29 18:05:32.403233 main.go:50: DB1000n [Version: v0.8.13][PID=1] 2022/03/29 18:05:32.403446 countrychecker.go:52:...
- **@arriven** (2022-03-30): @industral I've added proxy to countrychecker (should be available in 0.8.14) but be aware that with proxylist like this you might need a lot of retries for countrychecker to find working proxy...
- **@localdotcom** (2022-03-30): I added `SYSTEM_PROXY ` variable to the k8s deployment manifest ``` envVars: - name: "SYSTEM_PROXY"   value: '{{ join (split (get_url...
- **@industral** (2022-03-30): yeah, have the same after pull latest docker  ``` {"level":"warn","ts":1648652837.6963356,"caller":"templates/templates.go:175","msg":"error executing template","error":"template: tpl:1:16:...
- **@arriven** (2022-03-30): Context deadline exceeded usually means that it has timed out while fetching url. Can you check if the pod has access to the internet?
- **@localdotcom** (2022-03-30): @Arriven  I've tested it again with 1 pod replica, the error is gone. Before I ran 15 pods with scale_factor=25. But I'm not sure if it's related to amount of pods.
- **@arriven** (2022-03-30): if I were to guess I'd put my money on scale factor rather than the amount of pods. could be that the amount of connections used by the app exceeds the configured limit of file descriptors allowed...
</details>

## #423 Is checksum file correct since the last update about at 13h30 CET ?
**State:** CLOSED | **Author:** @ykerb2 | **Created:** 2022-03-25 | **Updated:** 2022-03-25 | **Comments:** 3

> Did i do wrong with my md5sum program ?

<details><summary>Comments (3)</summary>

- **@arriven** (2022-03-25): as of v0.8.4 the correct way to validate checksum is with `sha256sum` (or `shasum -a 256` on darwin)
- **@arriven** (2022-03-25): see install.sh for more details
- **@ykerb2** (2022-03-25): tks
</details>

## #422 Incorrect zipping for Window platform
**State:** CLOSED | **Author:** @art-c0der | **Created:** 2022-03-25 | **Updated:** 2022-03-25 | **Comments:** 1

> <img width="882" alt="Screen Shot 2022-03-25 at 12 23 30" src="https://user-images.githubusercontent.com/42999342/160112305-241e2b21-b828-44e5-82a1-b88de62a6e10.png">

<details><summary>Comments (1)</summary>

- **@arriven** (2022-03-25): fixing (should be ok since 0.8.6 which is being built now)
</details>

## #421 Change cloud guides and deployments to use regular image with ENABLE_PRIMITIVE=false `[documentation, help wanted, good first issue, priority: medium]`
**State:** CLOSED | **Author:** @arriven | **Created:** 2022-03-25 | **Updated:** 2022-03-25 | **Comments:** 2

> I want to get rid of advanced image bc it takes more than 20 minutes to build it (compared to 3-4 minutes when building regular one with ko). It's possible to make advanced image use ko for build as well but considering all the differences between advanced and regular images (just 1 param) having...

<details><summary>Comments (2)</summary>

- **@Amet13** (2022-03-25): @Arriven does it mean that we just need to pass `ENABLE_PRIMITIVE=false` to the container as env variable?
- **@arriven** (2022-03-25): @Amet13 yes. That would also remove the need for Dockerfile
</details>

## #420 Fix install.sh to work with goreleaser produced artifacts `[bug, help wanted, good first issue, priority: high]`
**State:** CLOSED | **Author:** @arriven | **Created:** 2022-03-25 | **Updated:** 2022-03-25 | **Comments:** 1

> Goreleaser introduces a lot of useful features but it uses different checksums format (sha256 with all sums in one file) and we need to adapt the script to it

<details><summary>Comments (1)</summary>

- **@arriven** (2022-03-25): fixed in 8dae06b02395e2771832f903da4b7615111d0490
</details>

## #419 EnablePrimitiveJobs parameter question
**State:** CLOSED | **Author:** @localdotcom | **Created:** 2022-03-25 | **Updated:** 2022-03-25 | **Comments:** 5

> I'm running db1000n on AWS EKS using helm chart. Under container log I see following message
> `{"level":"info","ts":1648202330.9562292,"caller":"runner/runner.go:152","msg":"There is a filter defined for a job but this client doesn't pass it - skip the job"}`
> I guess it happens because Docker...

<details><summary>Comments (5)</summary>

- **@arriven** (2022-03-25): it is expected behavior. udp jobs use a lot of traffic and are easily detected, this has led to some issues in the past (high cloud costs and people being banned bc clouds thought their machines were...
- **@arriven** (2022-03-25): that being said, it's probably better to just discontinue advanced image in favor of setting this parameter in all the guides and deployments, see #421
- **@localdotcom** (2022-03-25): Thank you! BTW when I'll run ~20 pod replicas will it be compromised? How much pod replicas can I run safely?
- **@arriven** (2022-03-25): hard to tell, the traffic that is produced by advanced images shouldn't be qualified as DDoS without manual inspection. It kinda behaves as a misconfigured/poorly designed API at best
- **@localdotcom** (2022-03-25): Thanks!
</details>

## #416 Build Android APK file to provide the huge possibility to attack via ru phone owners.
**State:** CLOSED | **Author:** @oleksiikoshlatyi | **Created:** 2022-03-25 | **Updated:** 2022-03-31 | **Comments:** 7

> I'm suggesting, this is a possible solution
> https://pkg.go.dev/golang.org/x/mobile/cmd/gomobile

<details><summary>Comments (7)</summary>

- **@Wendors** (2022-03-25): This link does not work
- **@oleksiikoshlatyi** (2022-03-25): The link is working ![image](https://user-images.githubusercontent.com/32518348/160140091-d5f1c7ef-2685-44a2-86be-15389be16048.jpeg)
- **@arriven** (2022-03-25): Seems like an interesting idea, but based on my limited experience with mobile it's likely that the main problem will be crafting a manifest with all the required permissions to use low level...
- **@oleksiikoshlatyi** (2022-03-25): The requirements (allow an application to use the network) will not be an issue. APK files can be distributed in many ways, even without a play market (or other applications catalogs). BTW, almost...
- **@mimihagi** (2022-03-25): Building and running db1000n in [termux](https://termux.org) on android works without issues. Steps are:  1. install termux 2. install golang, git and make (`apt update && apt install golang git...
- **@0xDF77-C0R3** (2022-03-26): People familiar with Termux can help even with [Slowloris](https://github.com/gkbrk/slowloris).  `pkg install python` `pip install slowloris` `python3 slowloris.py HTTP://URLTOATTACK`
- **@zlaya-sobaka** (2022-03-28): Привет, мы с ребятами придумали как можно использовать вашу библиотеку для мобильных устройств Android https://github.com/zlaya-sobaka/db1000n_mobile с помощью библиотеки fyne...
</details>

## #415 Google colab suggestion 
**State:** OPEN | **Author:** @ignitedevua | **Created:** 2022-03-24 | **Updated:** 2022-03-25 | **Comments:** 5

> * free
> * no VPN required
> * Google Account required
> * no local network load
> * up to 5 copies for each G-account (in separate tabs)
> * up to 12 hrs online  (free limitation)
> 
> db1000n v0.8.2
> https://colab.research.google.com/drive/1pqzNe9KvqTsDTb_Xn7ra8gYqpgOsFxIi?usp=sharing
> Runtime -> run all

<details><summary>Comments (5)</summary>

- **@ignitedevua** (2022-03-24): the file may be locked due to quotas, so save copies to your G-disk first
- **@stalkerdp500m** (2022-03-25): Error first step  Downloading an archive... curl: no URL specified! curl: try 'curl --help' or 'curl --manual' for more information
- **@arriven** (2022-03-25): @stalkerdp500m the issue is caused by #420 - hopefully will fix it today (worst case tomorrow)
- **@arriven** (2022-03-25): should be fixed now
- **@stalkerdp500m** (2022-03-25): > should be fixed now Thanks. work
</details>

## #413 DigitalOcean best app country/region select
**State:** CLOSED | **Author:** @asjustis | **Created:** 2022-03-24 | **Updated:** 2022-03-25 | **Comments:** 1

> Just launched db1000n instance on DigitalOcean. Attacks are logged as successful, but the response rate is simply 0.0%, so I am not sure it actually reaches the targets correctly. 
> 
> Thinking to switch it to another region, to a country that russia might have not restricted internet access yet....

<details><summary>Comments (1)</summary>

- **@asjustis** (2022-03-25): Ah, yes, I changed to Singapore (sgp) region, and now I have `[ Response rate ] 86.8%` instead of 0.1%. Maybe that helps somebody. Closing :)
</details>

## #412 Incorrect traffic stats calculation
**State:** CLOSED | **Author:** @asu-talk | **Created:** 2022-03-24 | **Updated:** 2022-03-24 | **Comments:** 7

> With the latest version, I see that db1000n generates a lot of traffic (assume this means outgoing traffic).
> But bmon shows much smaller numbers:
> 
> ![image](https://user-images.githubusercontent.com/54418113/159993656-a5e3dcaf-9dac-4a7b-bff3-c80415a714a7.png)
> 
> Could you please confirm that it`s...

<details><summary>Comments (7)</summary>

- **@arriven** (2022-03-24): yes, this is indeed am issue with stats calculation. This particular issue happens only with http jobs (which are the only ones being used in the config right now AFAIR). Any http request is done via...
- **@arriven** (2022-03-24): #408 should be already fixed for couple hours at least (although yes, that would explain that difference as the error would happen locally even before the app tries to establish the connection and I...
- **@asu-talk** (2022-03-24): > #408 should be already fixed for couple hours at least (although yes, that would explain that difference as the error would happen locally even before the app tries to establish the connection and...
- **@arriven** (2022-03-24): ah, ok, that one is a protocol mismatch in another recent optimization introduced to bypass this (https://github.com/Arriven/db1000n/issues/365#issuecomment-1070974009). Fixed it on the config side,...
- **@arriven** (2022-03-24): (it might take some time for the config to get populated to all cdn servers though)
- **@asu-talk** (2022-03-24): > ah, ok, that one is a protocol mismatch in another recent optimization introduced to bypass this ([#365 (comment)](https://github.com/Arriven/db1000n/issues/365#issuecomment-1070974009)). Fixed it...
- **@arriven** (2022-03-24): actually went ahead and fixed it today :D https://github.com/Arriven/db1000n/commit/386944f37987fc3af60fda634b5e194ffad9f765
</details>

## #410 Please create a support group
**State:** CLOSED | **Author:** @ignitedevua | **Created:** 2022-03-24 | **Updated:** 2022-03-31 | **Comments:** 6

> a lot of people faced with problems like this: 
> <pre>
> !Атака проводиться успішно! Руський воєнний корабль іди нахуй!
> !Attack is successful! Russian warship, go fuck yourself!
> ---------Traffic stats---------
>  [     Generated ] 39643.71 MB | 41569447185 bytes
>  [      Received ]     0.09 MB |   ...

<details><summary>Comments (6)</summary>

- **@arriven** (2022-03-24): Low response rates usually mean that targets can't manage the load we're producing
- **@iamtodor** (2022-03-25): @Arriven can we add it somewhere explicitly? Something like a response rate 0.0% means the app works as expected or so
- **@arriven** (2022-03-25): The fun part here is that this actually turned out to be an issue (too many requests were generated but never sent anywhere due to misconfiguration) so I'm not sure what to do with it. Low response...
- **@arriven** (2022-03-25): Probably best to just add that last sentence to FAQ  As for support group - there no groups dedicated to just this tool alone but considering the spread of it you can probably get some initial help...
- **@arriven** (2022-03-25): fe0c8c90e1178e57408031c7e85baf1cb1352f79 for the FAQ part
- **@arriven** (2022-03-31): Enabled github discussions for community help
</details>

## #409 Is adv config still relevant?
**State:** CLOSED | **Author:** @kurlyk-dev | **Created:** 2022-03-24 | **Updated:** 2022-03-24 | **Comments:** 1

> Is [adv config](https://raw.githubusercontent.com/db1000n-coordinators/LoadTestConfig/main/config.adv.json) still relevant?
> It hasn't been updated for 4 days, maybe I should switch to the common config?
> But I'am running a big fleet of instances on AWS, maybe it's risky, my previous account was...

<details><summary>Comments (1)</summary>

- **@arriven** (2022-03-24): Hey, advanced config is no longer relevant as since v0.8.0 the app has a filter to disable non-advanced jobs (it's not present in default config yet because we don't use jobs that are affected)
</details>

## #408 Full CPU use, errors in the debug output
**State:** CLOSED | **Author:** @sq2mo | **Created:** 2022-03-24 | **Updated:** 2022-03-25 | **Comments:** 10

> I've noticed 100% CPU usage - all cores are fully occupied.
> 
> using the -debug switch, following logs can be noticed:
>  {"error": "dial tcp: lookup xx.xx.xx.xx : no such host"}
>  {"error": "HostClient can't follow redirects to a different protocol, please use Client instead"}
> 
> Is this related to...

<details><summary>Comments (10)</summary>

- **@sq2mo** (2022-03-24): [v0.8.1](https://github.com/Arriven/db1000n/releases/tag/v0.8.1) does not seem to have this issue.
- **@arriven** (2022-03-24): Errors are caused by a typo here https://github.com/db1000n-coordinators/LoadTestConfig/blob/main/config.v0.7.json#L177 (Extra space), will fix in couple of minutes but it only affects one of the...
- **@sq2mo** (2022-03-25): I might be mistaken here, but it looks like CPU resources are eaten by frequent DNS lookups for a non-existent host. Perhaps we should not query the DNS again if we already know the FQDN does not...
- **@arriven** (2022-03-25): @Luceoria not really, that errored host was using a raw ip address so no dns query was done. it was just failing to parse it locally and since local parsing is almost instant it was able to perform...
- **@sq2mo** (2022-03-25): Understood. I had this impression since one of the hosts from the config file does not have a DNS record, as a result I have hundreds of DNS lookups per sec and CPU usage around 30-40%. If I...
- **@arriven** (2022-03-25): @Luceoria you are using custom config for that, right? if you mainly use http jobs you can utilize `client.static_host` parameter to set predefined address and tls usage (http vs https) for a target...
- **@sq2mo** (2022-03-25): I am using this one: https://github.com/db1000n-coordinators/LoadTestConfig/blob/main/config.v0.7.json  Just removed the sections with "jira8.cdek.ru" since this host does not resolve. This...
- **@arriven** (2022-03-25): Hm, weird, which executable version do you use? The "static_host" feature was added in v0.8.2 and as far as I see it should be used there. If your version is up to date can you send some logs my way...
- **@sq2mo** (2022-03-25): I use v0.8.1.
- **@sq2mo** (2022-03-25): Ok, could not replicate this problem on a newest 0.8.7. Going to production.
</details>

## #402 not work, does not start
**State:** CLOSED | **Author:** @RydIgorOk | **Created:** 2022-03-23 | **Updated:** 2022-03-23 | **Comments:** 1

> ![image](https://user-images.githubusercontent.com/22442729/159774068-b67b5dca-a98d-4866-a9d8-eac0827141f0.png)

<details><summary>Comments (1)</summary>

- **@RydIgorOk** (2022-03-23): you need to disable your antivirus
</details>

## #401 Failed to unmarshal job configs, will keep the current one: invalid character '}' looking for beginning of object key string
**State:** CLOSED | **Author:** @JeyM1 | **Created:** 2022-03-23 | **Updated:** 2022-03-23 | **Comments:** 6

> Full log:
> ```
> 2022/03/23 17:51:27.029769 main.go:58: DB1000n [Version: v0.7.12][PID=442416]
> 2022/03/23 17:51:27.030119 countrychecker.go:28: Checking IP address, attempt #0
> 2022/03/23 17:51:28.250122 countrychecker.go:97: Current country: Germany (138.68.81.60)
> 2022/03/23 17:51:28.349953...

<details><summary>Comments (6)</summary>

- **@DangelZM** (2022-03-23): Same issue for  >  > System Version: macOS 11.6 (20G165) > Kernel Version: Darwin 20.6.0
- **@ahalan** (2022-03-23): Same on Apple silicon M1 > System Version: macOS 12.0.1 (21A559) > Kernel Version: Darwin 21.1.0  ``` 2022/03/23 18:05:33.733442 config.go:40: Loading config from...
- **@oholubovskyi** (2022-03-23): Looks like its old version (v0.7.12).  Try the latest version https://github.com/Arriven/db1000n/releases/tag/v0.8.2
- **@oholubovskyi** (2022-03-23): > The issue reason is incorrect configuration json - redundant commas. While the issue is not fixed by the channel administrators we can (as a workaround): >  > 1. download configuration json...
- **@asu-talk** (2022-03-23): > > The issue reason is incorrect configuration json - redundant commas. While the issue is not fixed by the channel administrators we can (as a workaround): > >  > > 1. download configuration json...
- **@JeyM1** (2022-03-23): On newest version all is fine, thanks
</details>

## #399 Encrypted jobs and Prometheus stats
**State:** CLOSED | **Author:** @bitshape | **Created:** 2022-03-23 | **Updated:** 2022-03-23 | **Comments:** 1

> Assuming https://github.com/Arriven/db1000n/commit/620ba375b1ba5c13e439c0dfb88f3e2d0a3868b3 was removed so that wouldn't be possible to inspect encrypted config by polling from Prometheus server, this still leaves a possibility of indirectly observing encrypted config by setting up own Prometheus...

<details><summary>Comments (1)</summary>

- **@arriven** (2022-03-23): the thing is that we can't secure everything and it's just a question of slowing down those who want to get access to the encrypted config. You need to set up your own prometheus cluster in order to...
</details>

## #396 How to understand if tcp-targets are under attack or not?
**State:** CLOSED | **Author:** @UnitybaseExplorer | **Created:** 2022-03-22 | **Updated:** 2022-03-22 | **Comments:** 3

> Is there a way to see if tcp-targets are under attack or not? They are not logged in the output.
> 
> Custom config:
> ```
> {
> "jobs": [
> {
> "type": "http",
> "count": 10,
> "args": {
> "request": {
> "method": "GET",
> "path": "https://dolyami.com/"
> }
> }
> },
> {
> "type": "tcp",
> "args": {
> "address":...

<details><summary>Comments (3)</summary>

- **@arriven** (2022-03-22): @UnitybaseExplorer I'm currently working on improving the visibility there (the logs are already in main, tracking is incoming but github is experiencing issues so I'm waiting on CI to pass before...
- **@arriven** (2022-03-22): logs were added here https://github.com/Arriven/db1000n/commit/66b3c596749198fd96fe04ebfe8b8f73a5e86a65
- **@UnitybaseExplorer** (2022-03-22): Thx!!!
</details>

## #394 Why encrypted jobs?
**State:** CLOSED | **Author:** @Fahrenheit2539 | **Created:** 2022-03-22 | **Updated:** 2022-03-23 | **Comments:** 4

> One of the jobs in the config is encrypted.
> 
> `    {
>       "type": "encrypted",
>       "args": {
>         "format": "json",
>         "data": 
> ...`
> 
> Base64 decoding shown following header:
> `
> age-encryption.org/v1
> -> scrypt yKFNmP9oNK38ps7grEA12A 18
> `
> 
> I'm curious why? That does not help...

<details><summary>Comments (4)</summary>

- **@arriven** (2022-03-22): @Fahrenheit2539 you have an option to skip those jobs completely via `--skip-encrypted` commandline flags (see...
- **@Fahrenheit2539** (2022-03-22): Thanks, really appreciate quick response! Your arguments make sense, don't think you want to add more bureaucracy in this fast-moving process.  What would help is updating docs to briefly mention...
- **@arriven** (2022-03-22): I don't think that it would require a lot of bureaucracy, especially on my side. I would most likely delegate the trust establishment to someone else (whom I already trust).  And it would be...
- **@Fahrenheit2539** (2022-03-23): Can send me an email to fahrenheit2539 at hotmail.com? Interested to discuss how can I help.
</details>

## #392 OOM on hardware with low RAM
**State:** CLOSED | **Author:** @avoylenko | **Created:** 2022-03-22 | **Updated:** 2022-03-22 | **Comments:** 4

> Hello!
> I run the service on **RPi Zero** with just **512** of **RAM**, everything was okay, but starting from yesterday the service has started dying with OOM almost immediately as soon as it starts the jobs:
> 
> ```
> root@raspberrypi:~# ./db1000n -debug
> 2022/03/22 10:10:38.807231 main.go:57:...

<details><summary>Comments (4)</summary>

- **@arriven** (2022-03-22): hey, the system is not optimized to run on such hardware bc unfortunately making it work there would very likely require limiting the functionality on other systems. That being said, there are parts...
- **@avoylenko** (2022-03-22): @Arriven  It seems like the command line option `--prometheus_on=false` does not work as expected:  ``` root@raspberrypi:~# ./db1000n --prometheus_on=false 2022/03/22 10:59:49.305912 main.go:57:...
- **@arriven** (2022-03-22): Ah, yes, I didn't kickoff the release yet, will do it once the air hazard alarm ends 😅
- **@avoylenko** (2022-03-22): @Arriven '-prometheus_on=false' option help me to run the service with 512 mb RAM. Thank you for you valuable work.
</details>

## #390 Add http server listening port 8080 as parralel process in the App for Google Cloud Run compability
**State:** CLOSED | **Author:** @ubexplorer | **Created:** 2022-03-21 | **Updated:** 2022-03-26 | **Comments:** 2

> I've deployed docker containers with db1000n on GCP Cloud Run, which serves ingress traffic preferably and bills ingress requests as well, therefore GCP trial account with Cloud Run consumes ~ 1USD/day per 10 containers.
> But to deploy container in GCP Cloud Run I had to rebuild image with db1000n...

<details><summary>Comments (2)</summary>

- **@arriven** (2022-03-21): You can probably already utilize --pprof flag for that unless cloud run requires some specific API to be present
- **@sivillakonski** (2022-03-22): Hi @SerhiiZavalko, turning the `-enable-self-update` within the container won't work because it downloads and shuts down the current process in order to start a new process from a newer binary. The...
</details>

## #389 Proxy support
**State:** CLOSED | **Author:** @human1ty | **Created:** 2022-03-21 | **Updated:** 2022-03-24 | **Comments:** 2

> Is it possible to feed the proxy list either via a direct link or a local text file as an argument to a tool
> The intention is to apply a randomly selected proxy during the attack
> As a proposal - do a test for some N number of proxies in order to
> 1) Find out whether the proxy usable
> 2) Find out...

<details><summary>Comments (2)</summary>

- **@arriven** (2022-03-21): It's not implemented as a full blown feature but it's possible to achieve something of the following already by utilizing `--proxy` commandline flag. Accepts a comma separated list of proxies but...
- **@arriven** (2022-03-21): I'm not sure implementing full proxy rotation solution inside the app would be viable though, could be easier to setup a separate solution that would control proxies and just feed the list to db1000n
</details>

## #387 Something weird is going on, contact admins
**State:** CLOSED | **Author:** @MetaMmodern | **Created:** 2022-03-21 | **Updated:** 2022-03-21 | **Comments:** 1

> ![image](https://user-images.githubusercontent.com/42899786/159252632-cd9ca524-85d6-4529-ad5f-6005fca1466f.png)
> Started db1000n using tmux:
> 
> `tmux new -d "db1000n -enable-self-update"`
> 
> @Arriven What's wrong here? Worked fine until 10AM or so

<details><summary>Comments (1)</summary>

- **@arriven** (2022-03-21): the config has changed to include only tcp targets, see #386
</details>

## #386 ver 0.7.12 & ver.0.8.0
**State:** CLOSED | **Author:** @S767 | **Created:** 2022-03-21 | **Updated:** 2022-03-24 | **Comments:** 8

> Зі вчора генерує мало трафіку (через windows аплікейшн на AWS + ClearVPN) та сьогодні
> видає на версії 8
> 2022/03/21 10:58:47.659348 config.go:125: New config received, applying
> 2022/03/21 10:58:47.661349 runner.go:145: 14 job instances (re)started
> [Error] No traffic generated. If you see this...

<details><summary>Comments (8)</summary>

- **@udjfvnsaoepna** (2022-03-21): Same, **azure vps N1** (No traffic): ``` 2022/03/21 11:10:52.234623 main.go:57: DB1000n [Version: v0.8.0][PID=1] 2022/03/21 11:10:52.234884 countrychecker.go:28: Checking IP address, attempt...
- **@udjfvnsaoepna** (2022-03-21): Я понял в чем, проблема. В конфиге только TCP задания. https://raw.githubusercontent.com/db1000n-coordinators/LoadTestConfig/main/config.v0.7.json
- **@arriven** (2022-03-21): latest config is this one: https://t.me/itarmyofukraine2022/222 soon will be updated with this https://t.me/itarmyofukraine2022/223
- **@MetaMmodern** (2022-03-21): @udjfvnsaoepna  But why having only tcp's does not generate traffic?
- **@arriven** (2022-03-21): @MetaMmodern metrics for tcp jobs only take actual tcp payload into account but that gets sent only when connection is established. There is a task to track protocol headers as well but I haven't got...
- **@arriven** (2022-03-21): https://github.com/Arriven/db1000n/issues/12 The issue I was talking about
- **@MetaMmodern** (2022-03-21): Understood, it's just tracking) Thanks
- **@arriven** (2022-03-24): Closing this as #12 was already fixed
</details>

## #382 Load amount configuration
**State:** CLOSED | **Author:** @mErlin-sp | **Created:** 2022-03-21 | **Updated:** 2022-03-24 | **Comments:** 2

> Hello. I`ve looking into your project and it seems pretty good but i need to run up to 10 docker containers to utilize full of my cpu. Do we have a possibility to configurate amount of load (threads count, for example) in this software?

<details><summary>Comments (2)</summary>

- **@arriven** (2022-03-21): you can use `--scale 10` to achieve that same result
- **@arriven** (2022-03-21): no automatic cpu load detection for now (probably wouldn't be as good anyway since a lot of use cases are limited by network performance or amount of unique IP addresses you can get)
</details>

## #379 Prometheus charts
**State:** CLOSED | **Author:** @dzhonzojdberg | **Created:** 2022-03-20 | **Updated:** 2022-03-30 | **Comments:** 4

> Please make guest access to Prometheus charts.

<details><summary>Comments (4)</summary>

- **@Lagovas** (2022-03-23): for what you need it?  looking on such random nickname It looks strange. Personally, I prefer to close such issues from bots with strange requests)
- **@dzhonzojdberg** (2022-03-24): > for what you need it? looking on such random nickname It looks strange. Personally, I prefer to close such issues from bots with strange requests)  Hi, not a bot, a real person, actively using...
- **@arriven** (2022-03-26): @dzhonzojdberg you can use Prometheus endpoint if you use unencrypted build (i.e. you build the app from source) it's available at ":9090/metrics" when `--prometheus_on` is set to true (it's set to...
- **@dzhonzojdberg** (2022-03-29): @Arriven Thanks! That what I needed!)
</details>

## #377 please add to the guide that for some locations in aws config main instance type need to be changed from t2.micro to t3.micro `[documentation, help wanted]`
**State:** CLOSED | **Author:** @DTBLA | **Created:** 2022-03-19 | **Updated:** 2022-04-01 | **Comments:** 3

> <img width="355" alt="image" src="https://user-images.githubusercontent.com/36825912/159132664-6d0c5a0d-b214-4834-a394-fa5be0fbe939.png">

<details><summary>Comments (3)</summary>

- **@arriven** (2022-03-19): Probably would be best if you go ahead and make a PR yourself since as I understand it's not all regions that need this
- **@alexdanger** (2022-03-23): i suggest to add also graviton instances, as they have lowest prices and better cpu/mem throughput.
- **@Amet13** (2022-03-31): I believe it's already covered by https://github.com/Arriven/db1000n/pull/403/files#diff-e0beaf635e7e58ca4243047eed9acca64a5426826fb4c19579c3fef5c6cc6cc2R22
</details>

## #376 Built-in DDoS protection bypass
**State:** CLOSED | **Author:** @localdotcom | **Created:** 2022-03-19 | **Updated:** 2022-03-31 | **Comments:** 2

> Hi guys, does db1000n have built-in options to bypass DDoS protections like DDoS Guard, Cloudflare DDoS protection etc.?

<details><summary>Comments (2)</summary>

- **@arriven** (2022-03-19): It's not built in but it is already configurable enough to bypass some ddos-guard configurations and I'm working on functionality that would allow bypassing cloudflare and similar services
- **@arriven** (2022-03-31): CLosing this in favor of #293
</details>

## #371 Add ipv6 support to packetgen `[enhancement, priority: high]`
**State:** CLOSED | **Author:** @arriven | **Created:** 2022-03-18 | **Updated:** 2022-03-18 | **Comments:** 0

> This is required to be able to utilize more protocols and vulnerabilities like #360 
> A lot of the methods are already drafted in `src/core/packetgen/packetgen.go` and `src/core/packetgen/connection.go` but we still need a way to configure the job accordingly and also templates for ipv6 (like...

## #369 Linux version(amd64) doesn't start.
**State:** CLOSED | **Author:** @osomfinch | **Created:** 2022-03-18 | **Updated:** 2022-03-30 | **Comments:** 6

> Hi! first of all, I'm very grateful for your work. It's amazing, really!
> 
> Now, the Linux version won't start on ZorinOS(Ubuntu). I download it, unpack it, and then I try to run it and nothing happens. What could be the problem?
> 
> Interestingly, it seems to be working via wine just fine.

<details><summary>Comments (6)</summary>

- **@arriven** (2022-03-18): does it output any logs?
- **@osomfinch** (2022-03-19): > does it output any logs?  No. The app simply doesn't start. I press on it and nothing happens.
- **@sivillakonski** (2022-03-19): @osomfinch, - " I press on it" - I do understand that you are trying to run it thru the file manager, correct? Mind if I ask you to try to run it in a bit different way?  Open the terminal and...
- **@osomfinch** (2022-03-20): > Open the terminal and navigate...  Yes, it works now. Thank you!  But I don't see any reason to use it instead of the Windows' version now. Cause with the Windows version I open it in two...
- **@sivillakonski** (2022-03-20): @osomfinch, glad to hear that!  Basically, this is CLI oriented utility that runs, in most cases, on the machines without the User Interface at all. Since it's fully automatic tool that receives...
- **@osomfinch** (2022-03-20): > Basically, this is CLI oriented utility that runs...  Well, as we can see, I need it to be able to be run through GUI. It just goes to show how outdated the modern Linux desktop environment...
</details>

## #365 All db1000n targets are refusing connection. WAIDW?
**State:** CLOSED | **Author:** @app/ | **Created:** 2022-03-17 | **Updated:** 2022-03-26 | **Comments:** 9

> debug log:
> https://gist.github.com/s7aycool/3d51f00d45b5c747ed46288f7d6bbbf5

<details><summary>Comments (9)</summary>

- **@Lagovas** (2022-03-17): probably russian resources updated their web servers and validate Host header )) for example `141.105.69.219` now refuses connection but works as `https://infox.sg`.  So, maybe @Arriven should...
- **@** (2022-03-18): Any updates? I see a lot of people who are having troubles with that
- **@arriven** (2022-03-18): @s7aycool current config is using both hostname based targets (around 60-70% of them) and IP based ones. Successful attacks don't spam error logs so it might be not really noticeable but the overall...
- **@** (2022-03-18): @Arriven got you. Nevertheless, to be able to see % of successful attacks will be nice. Some kind of counter maybe?
- **@arriven** (2022-03-18): I thought about that but properly tracking success rate requires a separate set of tools that could turn out to be more complex than this one. I think it's better to use them instead if you want to...
- **@arriven** (2022-03-18): There are a counter with the amount of traffic generated by the app and the amount of traffic for which a target has returned some sort of response but not all attacks support that (some of them are...
- **@crocangIt** (2022-03-19): @Arriven  Hi, on all VM's I have similar status: see Received and Response rate Just restarted this one : -Traffic stats- ......  [      Received ]   0.05 MB |     49936 bytes  [ Response rate...
- **@arriven** (2022-03-19): From what I can tell - most alternatives tell their users that this behavior means that the targets are down (and that's actually quite likely the case). Ideally we'd want to confirm this by trying...
- **@crocangIt** (2022-03-20): > From what I can tell - most alternatives tell their users that this behavior means that the targets are down (and that's actually quite likely the case). Ideally we'd want to confirm this by trying...
</details>

## #363 Packetgen job write ip 0.0.0.0->xxx.xxx.xxx.xxx: sendmsg: invalid argument error
**State:** CLOSED | **Author:** @temorfeouz | **Created:** 2022-03-16 | **Updated:** 2022-03-16 | **Comments:** 4

> Hi! Trying build custom config file, tcp and udp jobs working great, make more traffic than mhddos)
> But ive faced with next error now:
> {"level":"error","ts":1647453131.335018,"caller":"runner/runner.go:133","msg":"error running job","error":"write ip 0.0.0.0->xxx.xxx.xxx.xxx sendmsg: invalid...

<details><summary>Comments (4)</summary>

- **@arriven** (2022-03-16): The most likely thing I would check first would be whether you are running in sudo mode or not (although that usually gives other kind of error) If that's not the case there are also configuration...
- **@arriven** (2022-03-16): Oh, btw, current implementation doesn't support specifying both tcp and udp payload in the same job at once and udp one prevails, you can try disabling udp payload there to see if it works
- **@temorfeouz** (2022-03-16): i run as sudo, ive tryed remove udp option right now but it nothing changed. I saw you inspired by https://github.com/bilalcaliskan/syn-flood i going to check how this project will do this
- **@temorfeouz** (2022-03-16): i`ve found out problem right now) problem in osx, when i run in docker all working good. here example of working config   {       "type": "packetgen",       "args": {          "host": "XX",    ...
</details>

## #362 DB1000N not working on Windows
**State:** CLOSED | **Author:** @ciegoo | **Created:** 2022-03-16 | **Updated:** 2022-10-11 | **Comments:** 6

> Hi friends, 
> 
> I am using your windows script file in different computers in order to attack as much as possible. I have tried some versions but only works good 5.12. This is the version that allows to send about 60 gB attack per day, other newer version doesn't work or send 2,4 gB per day. I am...

<details><summary>Comments (6)</summary>

- **@Lagovas** (2022-03-17): which versions did you try? 0.5.12 released 12 days ago and changed a lot since that time and has a lot of fixes. maybe you will try some fresh versions?)
- **@udjfvnsaoepna** (2022-03-17): Download last version https://github.com/Arriven/db1000n/releases
- **@ciegoo** (2022-03-18): Hi,  Fresh versions don't generate the same traffic weight than 5.12 does. Some new versions crashed, ut now with last update is working fine.  Thanks,  Regards     El jue., 17 mar. 2022 11:30,...
- **@arriven** (2022-03-18): @ciegoo are you actively comparing 5.12 with latest version or those numbers are historical values?
- **@ciegoo** (2022-03-20): Hi, Some version newer than 5.12 had problem working in Windows, but now release 7.12 works good. Thanks for your comments.
- **@ciegoo** (2022-10-11): Thanks,  Last version is working.  Regards   Un saludo,  Diego  El jue., 17 mar. 2022 12:13, udjfvnsaoepna ***@***.***> escribió:  > Download last version >...
</details>

## #361 Auto-installing failed on Windows and MacOS
**State:** OPEN | **Author:** @cawa-93 | **Created:** 2022-03-16 | **Updated:** 2022-04-01 | **Comments:** 3

> I tried run in github actions.
> https://github.com/cawa-93/dd0/blob/f477b9721249ed1fa96d3687b28c22882ecccaba/.github/workflows/lint.yml#L33-L35
> 
> But it works only on Linux. Auto-installing on Windows (in git-bash) and macos was failed....

<details><summary>Comments (3)</summary>

- **@Amet13** (2022-03-31): @cawa-93 it's already fixed by replacing md5sum->shasum: https://github.com/Arriven/db1000n/commit/8dae06b02395e2771832f903da4b7615111d0490
- **@cawa-93** (2022-04-01): @Amet13 Still not working, but now for other reasons https://github.com/cawa-93/dd0/runs/5783638850?check_suite_focus=true  ```bash Run source <(curl...
- **@Amet13** (2022-04-01): Not sure that this commit https://github.com/Arriven/db1000n/pull/212/files was tested properly. Could you try to use the version with pipe?...
</details>

## #360 New method of DoS?
**State:** CLOSED | **Author:** @Nereg | **Created:** 2022-03-16 | **Updated:** 2022-03-31 | **Comments:** 5

> CVE-2022-0742: Remote Denial of Service on Linux Kernel >=5.13
> 
> Flooding icmp6 messages of type 130 or 131 is enough to exploit a memory leak in the kernel and cause the host to go out-of-memory. The volume of traffic doesn't need to be particularly...

<details><summary>Comments (5)</summary>

- **@arriven** (2022-03-16): @Nereg looks good, and it should be possible to easily integrate icmp requests into packetgen
- **@arriven** (2022-03-16): Potentially could be a separate job though, packetgen requires root permission and it's probably not the best in terms of usability
- **@arriven** (2022-03-16): https://pkg.go.dev/golang.org/x/net/icmp#example-PacketConn-NonPrivilegedPing I'll leave it here for future reference along with https://pkg.go.dev/github.com/google/gopacket/layers#ICMPv6
- **@Nereg** (2022-03-17): Working on a POC with python's [scapy](https://scapy.readthedocs.io/en/latest/introduction.html#what-makes-scapy-so-special) tool because I can't find any POCs for this CVE
- **@Nereg** (2022-03-18): Sadly I can't replicate it on my kali machine. [Wireshark screenshot](https://prnt.sc/cQVhS8jvuSz2) [Memory graph while the attack is running](https://prnt.sc/46tBIYOjqRGg) Kernel version is...
</details>

## #353 switch debug logging to uber/go-zap `[enhancement, priority: low]`
**State:** CLOSED | **Author:** @arriven | **Created:** 2022-03-15 | **Updated:** 2022-03-16 | **Comments:** 0

> the main reason this logging library wasn't integrated yet is because structured logging is not as easily understood by users as raw logs, but that logic doesn't spread to debug logs which are not meant to be seen by users. it would also be easier to disable debug logging in encrypted contexts this...

## #349 Work with proxy with rotaion ip `[bug, priority: medium]`
**State:** CLOSED | **Author:** @udjfvnsaoepna | **Created:** 2022-03-15 | **Updated:** 2022-03-30 | **Comments:** 4

> I have mobile ru proxy with rotation ip every 1 min
> `http://login:password@proxyip:port`
> 
> I try 
> `db1000n.exe -proxy http://login:password@proxyip:port`
> 
> But program show my real ip:
> ```
> Checking IP address, attempt #0
> countrychecker.go:97: Current country: United States (my real...

<details><summary>Comments (4)</summary>

- **@arriven** (2022-03-15): ah, right, I forgot to pass the system proxy to the code that detects the ip :)  most likely the proxy is set up correctly and I'll fix the code soon to use proxy in the detection (so that you...
- **@arfgdev** (2022-03-20): It is a bit tricky task. I am not sure if it is a good idea check the country for each proxy if we have the list of 10000 proxies for example.
- **@human1ty** (2022-03-24): Vote for this. It would be great to know whether proxy is in use. Plus add to the output version of the tool. It can be not clear when many instances are running
- **@arriven** (2022-03-30): fixed in 0.8.14, see [comment](https://github.com/Arriven/db1000n/issues/424#issuecomment-1082907673) for some additional notes
</details>

## #348 prometheus.go:273: Can't push metrics to gateway, trying to change gateway...?
**State:** CLOSED | **Author:** @SamvSeer | **Created:** 2022-03-15 | **Updated:** 2022-03-15 | **Comments:** 2

> output while running job db1000n:
> 
> prometheus.go:273: Can't push metrics to gateway, trying to change gateway

<details><summary>Comments (2)</summary>

- **@arriven** (2022-03-15): we've enabled metrics to be able to see how much traffic we generate and be able to adapt our strategy accordingly. this message just means that we can't see the traffic you generate (so we're...
- **@SamvSeer** (2022-03-15): thanks for the feedback. will close the issue..btw running the job with VPN..currently from France.....same message occurs
</details>

## #347 Version 0.7.9 crashing on Windows10: need to fix `[bug, priority: high]`
**State:** CLOSED | **Author:** @crocangIt | **Created:** 2022-03-15 | **Updated:** 2022-03-15 | **Comments:** 9

> v0.7.8 is working, but v0.7.9:
> 
> C:\Users\Ivo\Desktop\db1000n-v0.7.9-windows-386>db1000n.exe
> 2022/03/15 12:40:03.255152 main.go:55: DB1000n [Version: v0.7.9][PID=4732]
> 2022/03/15 12:40:03.255152 countrychecker.go:28: Checking IP address, attempt #0
> 2022/03/15 12:40:06.134636...

<details><summary>Comments (9)</summary>

- **@arriven** (2022-03-15): OOM errors again, it seems like even with the latest change to encrypt only part of the config it still doesn't have enough memory to parse it. You can temporarily get around it by passing...
- **@crocangIt** (2022-03-15): >  It seems that some traffic is generated. It is busy for a few seconds and then it crashes completely: See the...
- **@Merfi745** (2022-03-15): > goroutine` 1806 [sleep]: >  > time.Sleep(0x14f46b0400) >         /usr/local/go/src/runtime/time.go:193 +0x146 > github.com/valyala/fasthttp.(*HostClient).connsCleaner(0x23d403c0) >        ...
- **@crocangIt** (2022-03-15): >   v0.7.9 try for now:  db1000n.exe --skip-encrypted
- **@arriven** (2022-03-15): @crocangIt are you by any chance using a machine with somewhere around 1 GB of RAM or are there more resources? want to confirm a suspicion
- **@AnatolHol** (2022-03-15): > @crocangIt are you by any chance using a machine with somewhere around 1 GB of RAM or are there more resources? want to confirm a suspicion  I have 24 GB RAM, Win10 x64, same problems.
- **@kurlyk-dev** (2022-03-15): Crashing on AWS `t3.small` instances too.
- **@crocangIt** (2022-03-15): > @crocangIt are you by any chance using a machine with somewhere around 1 GB of RAM or are there more resources? want to confirm a suspicion  For this I am using Win10 VMware virtual machines with...
- **@arriven** (2022-03-15): @crocangIt not removed, just "optimized": we discovered that when multiple threads try to decrypt the data in parallel - each of them have to create their own decryption key copy and each copy takes...
</details>

## #344 On AWS Windows t3.small
**State:** CLOSED | **Author:** @S767 | **Created:** 2022-03-15 | **Updated:** 2022-03-15 | **Comments:** 1

> Windows executable get error:
> 
> C:\Users\Administrator\Desktop>db1000n.exe
> 2022/03/15 07:47:17.100981 main.go:54: DB1000n [Version: v0.7.7][PID=3964]
> 2022/03/15 07:47:17.101527 countrychecker.go:28: Checking IP address, attempt #0
> 2022/03/15 07:47:18.806696 countrychecker.go:97: Current...

<details><summary>Comments (1)</summary>

- **@arriven** (2022-03-15): should be fixed in v0.7.8 (see #339 )
</details>

## #343 Config signing instead of encryption
**State:** OPEN | **Author:** @bitshape | **Created:** 2022-03-15 | **Updated:** 2022-03-17 | **Comments:** 6

> @Arriven wanted to ask you question before implementing something that you might have no interest in.
> 
> Having default configuration encrypted has two distinct downsides:
> 
> - It's uninspectable
> - It's not possible to compile `db1000n` binary or Docker container from fork (decryption error due to...

<details><summary>Comments (6)</summary>

- **@neatdecisions** (2022-03-15): Just to add a few cents, the decryption procedure is quite memory-hungry. I understand that the recommended minimum of RAM is 2GB, but it ran just fine on multiple SoC devices with 1GB (standalone...
- **@arriven** (2022-03-15): config encryption was implemented intentionally in order to utilize surprise element better. considering your feedback I'm working on changing it so that only specific jobs could be encrypted...
- **@arriven** (2022-03-15): @bitshape @neatdecisions I've changed the config to have only some parts of it encrypted, v0.7.9 can already work with that @bitshape config signing can also be implemented if you want
- **@Lagovas** (2022-03-17): > It's not possible to compile db1000n binary or Docker container from fork (decryption error due to missing key)  you can use your own key in your own fork. read [how it...
- **@Lagovas** (2022-03-17): > and therefore, my suggestion of implementing simple clear signature won't ever be merged  and what the goal of signing? all configuration sources under control of the author of binaries and...
- **@neatdecisions** (2022-03-17): > As I know about last fixes (#354), it should works well with 1GB too.  Yes, I confirm, this PR has fixed the high memory peak issues.
</details>

## #341 Feature request: "-use-advanced-config" flag for binary distribution
**State:** CLOSED | **Author:** @dmitry-salnikov | **Created:** 2022-03-14 | **Updated:** 2022-03-19 | **Comments:** 1

> Since you've added self-update for binary distribution - thanks! - could you please add the CLI option to use advanced config - same as used by docker image `ghcr.io/arriven/db1000n-advanced` mentioned in the docs.
> 
> It's preferrable to add kind of `-use-advanced-config` flag instead of specifying...

<details><summary>Comments (1)</summary>

- **@sivillakonski** (2022-03-15): Hi folks, thank you for your feedback! Lemme see what we can do with this :)
</details>

## #340 Create Terraform deployment for Amazon Elastic Container Service (ECS)
**State:** OPEN | **Author:** @ubexplorer | **Created:** 2022-03-14 | **Updated:** 2022-03-14 | **Comments:** 0

> Create terraform deployment for Amazon Elastic Container Service (ECS) with docker image, please, in addition to Amazon EC2.
> ECS consumes less resurces & have uniqe IP unlike VM instanse in EC2 with several docker containers.

## #339 Version 0.7.7 crashed on Windows10: need to fix
**State:** CLOSED | **Author:** @ubexplorer | **Created:** 2022-03-14 | **Updated:** 2022-03-15 | **Comments:** 7

> **Powershell**
> ```
> PS C:\Users\User\src\war\ddos\db1000n> .\db1000n
> 2022/03/14 22:16:05.301887 main.go:54: DB1000n [Version: v0.7.7][PID=236]
> 2022/03/14 22:16:05.301887 countrychecker.go:28: Checking IP address, attempt #0
> 2022/03/14 22:16:06.750456 countrychecker.go:97: Current country:...

<details><summary>Comments (7)</summary>

- **@5har0varik** (2022-03-14): Same issue  C:\repo\db1000n\scripts>goto StartApp  C:\repo\db1000n\scripts>rem Starts the app and if it returns 0 exit code it does "goto End", breaking...
- **@kt368** (2022-03-14): Same issue  C:\Users\kt368\Downloads\war\ddos\db1000n>db1000n.exe 2022/03/14 23:46:06.697718 main.go:54: DB1000n [Version: v0.7.7][PID=152360] 2022/03/14 23:46:06.697718 countrychecker.go:28:...
- **@sivillakonski** (2022-03-15): Hi there, chaps!  Thanks for reporting the issue. This is the fix to overcome this problem on Windows machines. Not so skilled to work with the Prometheus, but it should help I believe
- **@kt368** (2022-03-15): Could you please explain how to get a working executable file for windows 10 64-bit? My skills in programming is very low...
- **@zx6150** (2022-03-15): Probably the same. At startup this shows up and then app crashes  ``` 2022/03/15 06:24:05.437944 main.go:54: DB1000n [Version: v0.7.7][PID=8456] 2022/03/15 06:24:05.437944 countrychecker.go:28:...
- **@bitshape** (2022-03-15): You might want to wait until https://github.com/Arriven/db1000n/pull/342/files is merged as it seems to address this problem
- **@arriven** (2022-03-15): should be fixed in v0.7.8
</details>

## #335 User question: not clear wich version to use
**State:** CLOSED | **Author:** @crocangIt | **Created:** 2022-03-14 | **Updated:** 2022-03-15 | **Comments:** 6

> Hi,
> It is not clear which db1000n (Windows) version is advised to use. Are you still testing V7+ ? ( v6 and v7 are using different config files).
> 
> It would be better to hide  countrychecker messages in v0.7.5:"Can't check users country.** Please manually check that VPN is enabled or that you...

<details><summary>Comments (6)</summary>

- **@crocangIt** (2022-03-14): ![image](https://user-images.githubusercontent.com/101589346/158242117-e72bcedc-154d-49db-8dc1-83faf7e7ee23.png) Google drive doc- under Windows is old version. I know how to get the latest one. But...
- **@justsomeguy0** (2022-03-14): Latest v0.7.6 is not working for me at all (though my windows firewall prompt appeared and I allowed what it asked), previous one (v.0.7.5) works.
- **@iamtodor** (2022-03-14): @crocangIt g-doc is not up to date. it's not supported a long time ago. please read the official documentation - https://arriven.github.io/db1000n/en/#for-dummies -...
- **@AnatolHol** (2022-03-14): Versions 0.7.6 and 0.7.7 do not work under win10 21H2 (19044.1586), or am I doing something wrong ![Буфер...
- **@crocangIt** (2022-03-14): > Versions 0.7.6 and 0.7.7 do not work under win10 21H2 (19044.1586), or am I doing something wrong ![Буфер...
- **@arriven** (2022-03-15): @AnatolHol @crocangIt there was a bug in v0.7.6, should be fixed in v0.7.8 (see #339 )
</details>

## #331 Raspberry Pi Images
**State:** OPEN | **Author:** @app/ | **Created:** 2022-03-13 | **Updated:** 2022-08-15 | **Comments:** 9

> Is anyone working on Raspberry Pi images?
> Do we need it?
> 
> I can work on it! Just not sure that we need it

<details><summary>Comments (9)</summary>

- **@iamtodor** (2022-03-14): @FPavlovskiy it was implemented already. Please, take a look at https://github.com/Arriven/db1000n/issues/116
- **@** (2022-03-14): @iamtodor I talked about OS image.  Use case: someone gets a Raspberry and flash image to the SD card. Then just switch on and it just works? The only thing that is not clear, is what has to be...
- **@** (2022-03-14): https://www.vpngate.net/en/ can be used to discover and autoconnect to VPN
- **@arriven** (2022-03-15): @FPavlovskiy while the idea is interesting I'm not sure the app is mature enough for this use-case as new versions come out almost every day (sometimes multiple times a day). Your other issue with...
- **@Mancersoft** (2022-03-26): @FPavlovskiy I started the app on my Raspberry using ssh and screen, I'm not sure if Raspberry owners would want to reflash their sd cards entirely
- **@Amet13** (2022-03-31): It's hard to maintain OS, but it's easy to run it with systemd. Example of service file is here: https://github.com/Arriven/db1000n/blob/main/terraform/hetzner_cloud/user_data.yml#L11-L28
- **@dannysilence** (2022-05-02): Hm, I just use rc.local step to run db1000n in official Raspbian OS.  But yes, there is not a lot of sence to maintain specific OS image for that, just use new flashed OS with freshly downloaded...
- **@AdamMickiewich** (2022-08-15): Here is a deb package that we tested on raspberrypi and other armv7 based single board computer on Armbian: https://github.com/VolyaTeam/dzida-service. You can use one-line installer script as well:...
- **@AdamMickiewich** (2022-08-15): I think this issue could be closed, @arriven FYI
</details>

## #330 DEB package
**State:** OPEN | **Author:** @app/ | **Created:** 2022-03-13 | **Updated:** 2022-08-15 | **Comments:** 5

> Is anyone is working on DEB packages? 
> Interested especially for Rasberry PI. If no and someone needs it too, I can work on it.

<details><summary>Comments (5)</summary>

- **@Lagovas** (2022-03-17): I can only suggest to use [fpm](https://fpm.readthedocs.io/en/latest/) package that can generate DEBs/RPMs easily, and a lot other package types.
- **@sivillakonski** (2022-03-19): @FPavlovskiy , a quick question here. Do you want to have this DEB package to install as just a CLI utility or to run as a daemon?
- **@** (2022-04-04): @sivillakonski I thought about systemd.service
- **@** (2022-04-04): @Lagovas FPM is good, used it previously.
- **@AdamMickiewich** (2022-08-15): Here is a .deb package with systemd service https://github.com/VolyaTeam/dzida-service. Can be easily extended for RPM as well. `db1000n` is not included into a package for a few reasons: - The up...
</details>

## #327 Not sure this is an issue: Received HTTP 304 not modified..version 0.7.4
**State:** CLOSED | **Author:** @SamvSeer | **Created:** 2022-03-13 | **Updated:** 2022-03-13 | **Comments:** 4

> error message while running: Received HTTP 304 not modified..version 0.7.4...darwin arm64
> 
> <img width="535" alt="Schermafbeelding 2022-03-13 om 16 59 07" src="https://user-images.githubusercontent.com/25307892/158068473-8625f693-ec4a-40af-b5eb-0075ae9d155a.png">

<details><summary>Comments (4)</summary>

- **@arfgdev** (2022-03-13): could you describe the way to reproduce it?
- **@ChangeMe83** (2022-03-13): The same issue `2022/03/13 19:44:51.195001 config.go:103: Received HTTP 304 Not Modified 2022/03/13 19:44:51.195023 config.go:59: Loading config from...
- **@arfgdev** (2022-03-13): it is not an error.  it is an expected behavior https://github.com/Arriven/db1000n/blob/v0.7.4/src/runner/config/config.go#L103
- **@SamvSeer** (2022-03-13): ok..will close it. Just reported it because this message was not there in earlier versions.
</details>

## #322 v0.7.0 says  DB1000n [Version: v0.0.1]
**State:** CLOSED | **Author:** @su-hs | **Created:** 2022-03-13 | **Updated:** 2022-03-14 | **Comments:** 5

> I assume it's left over hardcoded version value or somewhere the code has not been changed properly
> 
> <img width="570" alt="Screenshot 2022-03-13 at 13 14 20" src="https://user-images.githubusercontent.com/100500001/158058905-acebb531-962b-4985-a289-63b785ee7fb3.png">
> 
> Reproduced via executables...

<details><summary>Comments (5)</summary>

- **@arfgdev** (2022-03-13): it seems that makefile does not add `ldflags` `+ go build -o build-artifacts-1647175086/db1000n ''` (https://github.com/Arriven/db1000n/runs/5527622054?check_suite_focus=true line 185 )
- **@arriven** (2022-03-13): Had some troubles setting up the release action to work with makefile (forgot that make is running on ubuntu for all targets, just uses different GOOS variable). Should be fixed in v0.7.4
- **@su-hs** (2022-03-13): I do confirm - FIXED in `v0.7.4`.
- **@su-hs** (2022-03-13): @Arriven hope u will get notif from closed issue, but, look,  ``` docker run --pull always ghcr.io/arriven/db1000n:latest # or this way docker run --rm -it --pull always...
- **@su-hs** (2022-03-14): @Arriven I do confirm, that latest `v0.7.5` is ALSO OK in regards to described issue:   ``` $ docker run --rm -it --pull always **ghcr.io/arriven/db1000n:latest**  latest: Pulling from...
</details>

## #318 Absolute path treated as a url when fetching config
**State:** CLOSED | **Author:** @arriven | **Created:** 2022-03-13 | **Updated:** 2022-03-13 | **Comments:** 0

> Ok, I think as a workaround for fetching config I should try to download it manualy with disabled vpn and then run db1000n container with overwritten entry point to specify path to the config.
> 
> ```
> vpn disconnect
> docker stop $(docker ps -a -q)
> docker pull...

## #315 Docker container can't send packets
**State:** CLOSED | **Author:** @dobrik | **Created:** 2022-03-12 | **Updated:** 2022-03-13 | **Comments:** 1

> I use docker to attack on two different PCs. 
> First is on windows OS with wsl (Ubuntu), on this configuration everything looks good, addesses changes, lines appear.
> Also I have Linux installed PC (Ubuntu 18.04.3 LTS (GNU/Linux 4.15.0-144-generic x86_64)) and on it I have an issue, process freezes...

<details><summary>Comments (1)</summary>

- **@arriven** (2022-03-13): It looks like the image you are using is quite old, this bug was fixed around a week ago (also it affects only one of the attacks with <1% chance) Try running docker with `--pull always`
</details>

## #313 OpenVPN can't connect: Exiting due to fatal error
**State:** CLOSED | **Author:** @industral | **Created:** 2022-03-12 | **Updated:** 2022-03-12 | **Comments:** 1

> Today after update, NordVPN stopped to work.
> 
> *.ovpn configs you can find here https://downloads.nordcdn.com/configs/archives/servers/ovpn.zip
> 
> 
> ```
> ---- Running with the following variables ----
> Kill switch: on
> HTTP proxy: off
> SOCKS proxy: off
> Proxy username secret: none
> Proxy password...

<details><summary>Comments (1)</summary>

- **@industral** (2022-03-12): Issue was due to wrong docker-compose config, using   ```yml     environment:       VPN_AUTH_SECRET: provider01_secret     secrets:       - provider02_secret ```  Strange OpenVPN error...
</details>

## #310 Broken download links in README file
**State:** CLOSED | **Author:** @artempolikarpov | **Created:** 2022-03-12 | **Updated:** 2022-03-13 | **Comments:** 1

> Unable to download due to broken tags in links (section Download an application for your platform)
> > [Windows]([https://github.com/Arriven/db1000n/releases/download/{{](https://github.com/Arriven/db1000n/releases/download/%7B%7B) git_latest_version_tag }}/db1000n-{{ git_latest_version_tag...

<details><summary>Comments (1)</summary>

- **@arriven** (2022-03-13): Fixed, forgot to update readme properly after switching to mkdocs. please use https://arriven.github.io/db1000n for all the docs related to this package
</details>

## #308 Azure - wrong (outdated) run command
**State:** CLOSED | **Author:** @exsesx | **Created:** 2022-03-12 | **Updated:** 2022-03-12 | **Comments:** 0

> Terraform Azure configuration is failing to start because of the wrong run command. Need to edit `attack_commands` variable in `terraform/azure/variables.tf`. 
> 
> https://github.com/Arriven/db1000n/blob/c4488e52315677f14ad7672dafa21d7d777213fb/terraform/azure/variables.tf#L13
> 
> Should...

## #303 Docker container stop work on targets after one minute
**State:** CLOSED | **Author:** @timsofteng | **Created:** 2022-03-12 | **Updated:** 2022-03-12 | **Comments:** 4

> Here is some logs.
> 
> ```
> 2022/03/12 08:25:06.012207 http.go:137: Attacking http://195.93.247.72:80
> 2022/03/12 08:25:06.013129 http.go:137: Attacking http://195.93.247.72:80
> 2022/03/12 08:25:06.014777 http.go:137: Attacking http://146.158.54.13:80
> 2022/03/12 08:25:06.016153 http.go:137:...

<details><summary>Comments (4)</summary>

- **@arriven** (2022-03-12): What makes you think it has stopped working on targets though?
- **@timsofteng** (2022-03-12): > What makes you think it has stopped working on targets though?  Log stops print targets.
- **@arriven** (2022-03-12): We changed that some time ago to print targets only when the app starts attacking them. It may be less obvious to users but it makes it a lot easier to diagnose problems. You can see that the app...
- **@timsofteng** (2022-03-12): > We changed that some time ago to print targets only when the app starts attacking them. It may be less obvious to users but it makes it a lot easier to diagnose problems. You can see that the app...
</details>

## #300 db1000n container doesn't have connection but vpn container has
**State:** CLOSED | **Author:** @industral | **Created:** 2022-03-11 | **Updated:** 2022-03-31 | **Comments:** 8

> I wrote a script to check what IP have containers, and found strange thing, that VPN containers itself have internet, but db1000n containers - don't.
> 
> **track.sh**
> 
> ```bash
> #!/bin/bash
> 
> containers=`docker ps --format "{{.Names}}" | grep root_db1000n_`
> 
> for p in $containers
> do
> 	echo "$p:...

<details><summary>Comments (8)</summary>

- **@bitshape** (2022-03-12): @industral https://github.com/Arriven/db1000n/pull/296 should fix it
- **@industral** (2022-03-12): I also tried that way, but it didn't work as it should be. I pulled latest code and it worked the same way it worked for me... Issue is - we loose db1000n containers...  ```bash # docker...
- **@industral** (2022-03-12): few things I found might be useful, but still not sure how to fix it  1. I'd increase `retries` for `db1000n`, since they should be at least +1 we have for ovpn, since if `ovpn` container was able...
- **@bitshape** (2022-03-12): @industral added one of your suggestions in the meantime https://github.com/Arriven/db1000n/pull/314/files
- **@industral** (2022-03-13): @bitshape thanks! but whole bug was not fixed yet as far as I understand, but ticket was closed... see item # 1 and 3
- **@arriven** (2022-03-13): @industral this is due to how github handles referencing issues in PR description. @bitshape I usually use "wip" instead of "fix/fixed" in these cases so that github does link the PR but doesn't...
- **@** (2022-03-13): +1  db1000n doesn't have internet access with vpn on Linux Ubuntu 20.14
- **@industral** (2022-03-13): so far so me works now the following config:  ```yaml   db1000n_01:     image: ghcr.io/arriven/db1000n-advanced     restart: unless-stopped     depends_on:       ovpn_01:         condition:...
</details>

## #298 HTTP job refactoring
**State:** CLOSED | **Author:** @bmirnoff | **Created:** 2022-03-11 | **Updated:** 2022-03-11 | **Comments:** 1

> This is hard to modify code as it is really procedural and is not allowed to effectively contribute.
> I am Providing PR with changes about it.

<details><summary>Comments (1)</summary>

- **@arriven** (2022-03-11): Fixed in #301
</details>

## #294 Network traffic limitation
**State:** CLOSED | **Author:** @vovagorodok | **Created:** 2022-03-11 | **Updated:** 2022-03-31 | **Comments:** 3

> There is any flag or config to limit network traffic? It's not possible to work at network from other PC when ddoser is turned on. Pages are not responsible. If it's possible to limit then will be nice to add this info to documentation. For me personally docker case is interesting one

<details><summary>Comments (3)</summary>

- **@bitshape** (2022-03-12): Make sure your PC is connected over Ethernet to your router if it isn't.  If you can setup Docker with VPN, it might be worth trying. VPN is unlikely to be as fast as your main connection so that's...
- **@srhlv** (2022-03-13): You can limit cpu usage per docker container with "--cpus=0.1" param, this will therefore limit net usage as well. (0.1 means 10% of your total cpu capacity)
- **@arriven** (2022-03-31): Apart from docker solution you can also use `--min-interval` to introduce artificial rate limiting to attacks (see --help for more details)
</details>

## #293 CloudFlare bypass 
**State:** OPEN | **Author:** @bmirnoff | **Created:** 2022-03-11 | **Updated:** 2022-03-20 | **Comments:** 7

> I think we need to add Cloudflare bypass https://github.com/MHProDev/MHDDoS/blob/2cd27e8b645d0dbf05048fa0e295844dc65a0671/start.py#L738 
> Also it might be configurable

<details><summary>Comments (7)</summary>

- **@arriven** (2022-03-11): yeah, I've been looking into it. it would require either adding python or javascript interpreter to be able to properly run checks, I have some ideas but need some more time to reflect on them. I've...
- **@bmirnoff** (2022-03-12): @Arriven  Sound good, `otto` for me also looks like a promising solution. I also can investigate this direction and share ideas here
- **@arriven** (2022-03-12): @bmirnoff what would probably be most important (especially in terms of using otto) and what I didn't have a chance to check yet is whether the anti-bot check requires an event loop or if it is just...
- **@bmirnoff** (2022-03-13): Just for everybody's information, reference impl for CFB can be https://github.com/Anorov/cloudflare-scrape js challenge is forked via node.js vm. Need to investigate actual process of solving a...
- **@bmirnoff** (2022-03-13): Here is actually how Cloudfare response looks like https://github.com/Arriven/db1000n/pull/324
- **@** (2022-03-14): Please, fix a TYPO in the tittle ClOudFlare
- **@crocangIt** (2022-03-20): > Just for everybody's information, reference impl for CFB can be https://github.com/Anorov/cloudflare-scrape js challenge is forked via node.js vm. Need to investigate actual process of solving a...
</details>

## #292 IP address spoofing
**State:** CLOSED | **Author:** @bmirnoff | **Created:** 2022-03-11 | **Updated:** 2022-03-31 | **Comments:** 1

> I observed code and see that config allows templating for headers and requests. But what about to add default IP address spoofing solution that adds headers for each HTTP attack 
> 
> https://github.com/MHProDev/MHDDoS/blob/main/start.py#L566
> `
> ("X-Forwarded-Proto: Http\"
>                ...

<details><summary>Comments (1)</summary>

- **@sivillakonski** (2022-03-12): @bmirnoff, The problem here is that `X-Forwarded-*` headers are usually set by the load balancers. I can't be 100% confident, but it feels like these headers would be overwritten by the reverse proxy...
</details>

## #287 700% CPU usage on MacOS - performance issue
**State:** CLOSED | **Author:** @su-hs | **Created:** 2022-03-10 | **Updated:** 2022-03-27 | **Comments:** 19

> Since `v0.6.2` and till now `v0.6.5` I download  executables from https://github.com/Arriven/db1000n/releases as suggested:
> - for my Intel CPU - https://github.com/Arriven/db1000n/releases/download/v0.6.5/db1000n-v0.6.5-darwin-amd64.tar.gz
> - for my M1 CPU -...

<details><summary>Comments (19)</summary>

- **@bitshape** (2022-03-12): I'm not maintainer so take my words with grain of salt but that's likely normal. It just means your CPU is very busy generating packets :)  Here's a screenshot of my M1:  ![Screen Shot 2022-03-12...
- **@arriven** (2022-03-12): Yeah, it is normal, the app is currently configured to hit quite a lot of targets, might need to think about a way to provide the ability to scale the amount of jobs via commandline and lower the...
- **@HorunS** (2022-03-12): yes, I have the same issue with my Macbook pro i9 processor. It gets hot within few minutes. Please fix or provide configs
- **@arriven** (2022-03-12): I've kicked off v0.7.0 - it has a way to scale resources dynamically via the commandline so I reduced the amount of jobs for that config to minimal, please check it out ( won't affect previous...
- **@su-hs** (2022-03-13): I confirm, that latest version `v0.7.0` seems OK, in regards CPU usage. I downloaded: - for Intel CPU...
- **@su-hs** (2022-03-13): But so far, I consider this issue can be closed now.
- **@su-hs** (2022-03-14): @Arriven NOT 700% but latest v`Test encryption` version uses now around 200-400% https://github.com/Arriven/db1000n/releases/tag/encryption-test And I also see 500-650% for latest version...
- **@su-hs** (2022-03-14): UPD. `v0.7.6` CPU usage is between 20-30 %
- **@su-hs** (2022-03-15): @Arriven  me again. Just wanna let u know, that version `v0.7.9` aka darwin arm64 causing now extremely noisy fan. CPU M1 - varies between 200% and with maximum I saw 666% CPU usage.   Value is OK,...
- **@arriven** (2022-03-15): @su-hs the key idea of this app - the configuration with all the attack targets is changed remotely. the config changes all the time and the amount of targets is different there meaning different...
- **@serg-music** (2022-03-27): @Arriven  v.0.8.10.  The issue still exists. After db1000n is started the CPU load hits 800%.  Statistics seems messed up: <img width="1119" alt="Снимок экрана 2022-03-27 в 13 34 44"...
- **@arriven** (2022-03-27): @serg-music what does it output when you just start it? Are there any errors about loading the config from github? Can you enable debug logs and send them here?
- **@serg-music** (2022-03-27): Here is the output after the start:  <img width="1093" alt="Снимок экрана 2022-03-27 в 13 43 41"...
- **@serg-music** (2022-03-27): [log_287.txt.zip](https://github.com/Arriven/db1000n/files/8357511/log_287.txt.zip) Debug logs collected after 1s of the run
- **@arriven** (2022-03-27): Ok, I see where this is coming from, seems like an issue with lower end systems that due to the nature of default error handling leads to even more load being generated (vicious circle). I'll see...
- **@serg-music** (2022-03-27): The system is hi-end (Macbook pro m1 pro-2021). Probably the problem is in my `ulimit` setting.
- **@arriven** (2022-03-27): ah, yes, that seems more like it, although it shouldn't create that much connections (current config uses around 800-900 if I'm not missing anything). Unless your ulimit is in that range or you scale...
- **@serg-music** (2022-03-27): ulimit -n 5000 solved the issue.  Not sure why the `file descriptors` is used. Probably the core generates the `file` that is somehow `read` during the sending request.
- **@arriven** (2022-03-27): On unix network connection is done via sockets and socket is very similar to a regular file. That's also true for pipes in your shell. Another cool thing in that regard is that there is /proc...
</details>

## #282 Support proxy list (--proxylist-url not work properly)
**State:** CLOSED | **Author:** @udjfvnsaoepna | **Created:** 2022-03-10 | **Updated:** 2022-03-13 | **Comments:** 0

> You need to enable support for proxy and socks lists, with periodic updates
> 
> I tried using --proxylist-url
> But this argument does not work properly, the program does not display any information on working with proxies
> 
> Proxy list must support different formats (without json, only text +...

## #281 What's the status on "Slow Loris" method?
**State:** CLOSED | **Author:** @SomalianCoolhacker | **Created:** 2022-03-10 | **Updated:** 2022-03-10 | **Comments:** 1

> Hi, when looking through changes in the main branch, I've discovered that, quote,
> 
> > `Warning`: slow-loris from `testconfig.json` is not yet finished and may overload the app due to not handling config refreshes
> 
> But the `slowloris.go` script is being updated frequently, so I'm wondering if it...

<details><summary>Comments (1)</summary>

- **@arriven** (2022-03-10): ah, right, forgot to remove that note, thanks for bringing it up!
</details>

## #280 Every time after 2Gb - doesn't seem to generate any traffic
**State:** CLOSED | **Author:** @Aljnk | **Created:** 2022-03-10 | **Updated:** 2022-03-10 | **Comments:** 0

> After starting the program, everything works until it reaches a value more then 2B bytes. Then start write - "doesn't seem to generate any traffic". Proceed works after restart until 2B bytes - then same.
> 
> 2022/03/10 11:36:41.789867 runner.go:162: Атака проводиться успішно! Руський воєнний...

## #279 Support of system variable like ALL_PROXY with schemes http://ip:port and socks5://ip:port for using with tor and packetgen job type `[enhancement, priority: medium]`
**State:** CLOSED | **Author:** @lollypot | **Created:** 2022-03-10 | **Updated:** 2022-03-31 | **Comments:** 3

> Continue of https://github.com/Arriven/db1000n/pull/207
> 
> For now we can set http proxy in two variants:
> 
> 1. By system variable like `HTTP_PROXY` or `http_proxy`
> 2. By app argument like `-proxy 172.17.0.1:8080`
> 
> Both variants are work very well. But it seems we have other types of jobs which...

<details><summary>Comments (3)</summary>

- **@arriven** (2022-03-10): that's actually a good question. I'd be looking at something like https://pkg.go.dev/golang.org/x/net/proxy#SOCKS5  I'm not sure whether it would be easier to embed it into packetgen or rawnet jobs...
- **@arriven** (2022-03-21): @lollypot considering the fact that socks5 proxies don't work for udp I feel like it would also be impossible to add them to packetgen but feel free to experiment
- **@arriven** (2022-03-31): Closing this as most proxies don't support udp or raw ip traffic (including tor)
</details>

## #278 Create forks of required Docker containers
**State:** OPEN | **Author:** @bitshape | **Created:** 2022-03-10 | **Updated:** 2022-03-10 | **Comments:** 1

> https://github.com/Arriven/db1000n/blob/main/docker-compose.yml
> 
> We're using the following two Docker containers:
> 
> - `willfarrell/autoheal:1.2.0`
> - `wfg/openvpn-client:2.1.0`
> 
> For further security hardening (especially for autoheal since it's running privileged) in case other two...

<details><summary>Comments (1)</summary>

- **@arriven** (2022-03-10): Thanks! Will take a look shortly
</details>

## #273 runner.go:112: error running job: write ip 0.0.0.0->60.60.121.145: sendmsg: not implemented on windows/amd64
**State:** OPEN | **Author:** @kirealll | **Created:** 2022-03-09 | **Updated:** 2022-03-10 | **Comments:** 2

> I get the following errors on all my Azure VM Windows servers:
> 
> 2022/03/09 20:31:20.432725 runner.go:112: error running job: write ip 0.0.0.0->60.60.121.145: sendmsg: not implemented on windows/amd64
> 
> OS: Windows Server 2022
> db1000n release: db1000n-v0.6.4-windows-amd64

<details><summary>Comments (2)</summary>

- **@arriven** (2022-03-10): this is one of the more advanced jobs that is not supported on all the systems. You can check the logs to see how many jobs are running there overall but the general idea is that app is configured to...
- **@kirealll** (2022-03-10): Ok, that makes sense. Thanks for the answer.
</details>

## #272 OOM killed
**State:** CLOSED | **Author:** @synapse-unix | **Created:** 2022-03-09 | **Updated:** 2022-03-16 | **Comments:** 3

> Got container **OOMkilled** today, from syslog:
> > Mar  9 18:14:14 http-service-0 kernel: [295692.212091] [  50111]     0 50111   224138    49259   520192        0             0 main
> > Mar  9 18:14:14 http-service-0 kernel: [295692.212094]...

<details><summary>Comments (3)</summary>

- **@nonchalant-enthusiast** (2022-03-09): Assuming you're on the latest build, it's probably related to the low RAM, it's recommended to have at least 2GB. See #54
- **@arriven** (2022-03-10): First of all I'd check for used version, the system you are running it on, how much memory is available to docker. If those seem plausible we can start digging deeper
- **@synapse-unix** (2022-03-10): It’s Azure’s Standard_D2s_v3 instance, 2 core CPU, 8Gb RAM. 1 container was running, Load average is about 2.0.  I just checked stats of the running for 10h containers, RAM usage is around 161Mb....
</details>

## #269 error running job: listen ip4:tcp 0.0.0.0: bind: An invalid argument was supplied
**State:** CLOSED | **Author:** @pashagolub | **Created:** 2022-03-09 | **Updated:** 2022-09-21 | **Comments:** 4

> ```shell
> PS> go version
> go version go1.17.6 windows/amd64
> 
> PS> git status
> On branch main
> Your branch is up to date with 'origin/main'.
> 
> nothing to commit, working tree clean
> 
> PS> git log --pretty=format:'%h' -n 1
> 9b6ad5e
> ```
> --
> 
> ```
> ..
> 2022/03/09 17:29:32.543983 runner.go:112:...

<details><summary>Comments (4)</summary>

- **@arriven** (2022-03-10): unless you run it with sudo this is kinda to be expected, see packetgen reference [here](https://github.com/Arriven/db1000n/blob/main/docs/configuration.md) you should be able to see in the logs how...
- **@pashagolub** (2022-03-10): terminal is running under admin role
- **@arriven** (2022-03-10): apparently, this feature is not supported in windows itself, see relevant issue for the go runtime https://github.com/golang/go/issues/6786
- **@pashagolub** (2022-03-10): Got it thanks. Maybe we should just exclude such kinds of jobs on the win platform? If you can provide me the info where to look, I can prepare the PR. Thanks
</details>

## #268 Windows 10: An attempt was made to access a socket in a way forbidden by its access permissions.
**State:** CLOSED | **Author:** @SLDay | **Created:** 2022-03-09 | **Updated:** 2022-03-09 | **Comments:** 0

> Hello, I keep on getting following error on four Windows 10 hosts. Can you please help?
> 
> `2022/03/09 16:49:24.851642 packetgen.go:66: Error building raw connection: listen ip4:tcp 0.0.0.0: socket: An attempt was made to access a socket in a way forbidden by its access permissions.`
> `2022/03/09...

## #265 Error building raw connection: listen ip4:tcp 0.0.0.0
**State:** CLOSED | **Author:** @Aljnk | **Created:** 2022-03-09 | **Updated:** 2022-03-09 | **Comments:** 3

> Starts from v.0.6 my log looks like this
> 
> **2022/03/09 14:36:00.109907 packetgen.go:66: Error building raw connection: listen ip4:tcp 0.0.0.0: socket: An attempt was made to access a socket in a way forbidden by its access permissions.
> 2022/03/09 14:36:00.110213 runner.go:112: error running job:...

<details><summary>Comments (3)</summary>

- **@arriven** (2022-03-09): it is to be expected if you are not running it with root permissions (or in docker). Some of mode advanced attacks are not working because of that but the rest are still there (and that rest is doing...
- **@Aljnk** (2022-03-09): Thanks
- **@SLDay** (2022-03-09): Dear Arriven, could you please advise how can I solve similar problem. I receive following errors when I run the tool in Windows 10 with Administrator previlages.  `2022/03/09 17:17:49.486864...
</details>

## #264 How to verify db1000n works as expected?
**State:** CLOSED | **Author:** @yaskravi | **Created:** 2022-03-09 | **Updated:** 2022-03-09 | **Comments:** 2

> How to verify db1000n works as expected?
> 1. In docker on virtual machines
> 2. In Kubernetes

<details><summary>Comments (2)</summary>

- **@arriven** (2022-03-09): Depending on what you want to verify you can check for logs, use external network monitoring tools, or set up you own test target and try attacking it with this tool (you'd need a custom config for...
- **@iamtodor** (2022-03-09): @Arriven I would rather just mention that seeing these logs: ``` Атака проводиться успішно! Руський воєнний корабль іди нахуй! Attack is successful! Russian warship, go fuck yourself! The app has...
</details>

## #249 sendmsg: invalid argument  - latest version
**State:** CLOSED | **Author:** @dvoinos | **Created:** 2022-03-09 | **Updated:** 2022-03-09 | **Comments:** 0

> 2022/03/09 07:16:27.979233 config.go:33: Loading config from "https://raw.githubusercontent.com/db1000n-coordina
> tors/LoadTestConfig/main/config.json"
> 2022/03/09 07:16:27.979263 config.go:91: New config received, applying
> 2022/03/09 07:16:27.979875 runner.go:118: 74 job instances...

## #248 Error looking up DNS / Error sending packet `[input needed]`
**State:** CLOSED | **Author:** @freey0urmind | **Created:** 2022-03-08 | **Updated:** 2022-03-10 | **Comments:** 2

> 2022/03/08 23:13:57.518243 utils.go:153: Error looking up DNS: lookup online.sberbank.ru on 24.200.210.241:53: read udp 172.17.0.2:41928->24.200.210.241:53: i/o timeout
> 2022/03/08 23:13:57.518279 packetgen.go:65: Error sending packet: lookup online.sberbank.ru on 24.200.210.241:53: read udp...

<details><summary>Comments (2)</summary>

- **@arriven** (2022-03-09): Both this and #247 seem to indicate that there are a lot of network problems on the instance you are running this app on. Can you check out if anything else is working?
- **@freey0urmind** (2022-03-09): The issue is not happening anymore without any actions on my side.  Thank you!
</details>

## #247 The app doesn't seem to generate any traffic `[input needed]`
**State:** CLOSED | **Author:** @freey0urmind | **Created:** 2022-03-08 | **Updated:** 2022-03-10 | **Comments:** 3

> 2022/03/08 23:04:12.337415 runner.go:157: The app doesn't seem to generate any traffic, please contact your admin
> 
> 2022/03/08 23:04:42.338450 config.go:29: Failed to fetch config from "https://raw.githubusercontent.com/db1000n-coordinators/LoadTestConfig/main/config.json": Get...

<details><summary>Comments (3)</summary>

- **@arriven** (2022-03-09): Can you check if you can download that config manually via curl from the corresponding instance? `curl https://raw.githubusercontent.com/db1000n-coordinators/LoadTestConfig/main/config.json` should...
- **@freey0urmind** (2022-03-09): >   Yes, I can download. The script was displayed directly in the terminal window.
- **@freey0urmind** (2022-03-09): One more thing the line " The app doesn't seem to generate any traffic, please contact your admin" is not coming anymore, instead I am getting the "The app has generated approximately XXXXXXXXXX...
</details>

## #244 terraform aws timeout
**State:** CLOSED | **Author:** @industral | **Created:** 2022-03-08 | **Updated:** 2022-03-13 | **Comments:** 0

> ```
> terraform apply -var-file="my.tfvars"
> ```
> 
> **my.tfvars**
> 
> ```
> region           = "eu-central-1"
> name             = "ir_db1000n"
> desired_capacity = 32
> min_size         = 0
> max_size         = 32
> instance_type    = "t3.nano"
> ```
> 
> Always timeout by `ir_db1000n": Waiting up to 10m0s:...

## #243 How to use proxylist with db1000n?
**State:** CLOSED | **Author:** @vjik-jig | **Created:** 2022-03-08 | **Updated:** 2022-03-08 | **Comments:** 1

> How to use proxylist with db1000n?
> Is it possible "out of the box"? What is the command to use?

<details><summary>Comments (1)</summary>

- **@arriven** (2022-03-08): See linked PR on how to configure it for an attack. You can also provide you own list via commandline (run it with `-h` for up to date reference)
</details>

## #241 Allow using system proxy settings in http job `[enhancement, priority: medium]`
**State:** CLOSED | **Author:** @arriven | **Created:** 2022-03-08 | **Updated:** 2022-03-08 | **Comments:** 0

> See https://github.com/valyala/fasthttp/blob/59f94a3f7137d0ad215bd262df7082d1e632a1f7/fasthttpproxy/proxy_env.go
> for example

## #234 Use mapstructure instead of json.rawmessage in configs in order to be able to switch config format easily `[enhancement, priority: medium]`
**State:** CLOSED | **Author:** @arriven | **Created:** 2022-03-08 | **Updated:** 2022-03-08 | **Comments:** 0

## #231 go install github.com/Arriven/db1000n@latest fails in golang:alpine docker
**State:** CLOSED | **Author:** @alexwestside | **Created:** 2022-03-08 | **Updated:** 2022-03-17 | **Comments:** 2

> Hi, 
> 
> i'm using Dockerfile like this:
> 
> ```
> FROM golang:alpine
> CMD go version
> RUN go install github.com/Arriven/db1000n@latest
> COPY run.sh ./run.sh
> CMD [ "./run.sh" ]
> ENTRYPOINT [ "sh", "-c" ]
> ```
> 
> Command go install github.com/Arriven/db1000n@latest fails with error 
> 
>  > [2/3] RUN go...

<details><summary>Comments (2)</summary>

- **@alexwestside** (2022-03-08): Update  RUN go get github.com/Arriven/db1000n@latest - helps
- **@MetaMmodern** (2022-03-14): @alexwestside I'm installing wothout docker. `go get` gives this error: ``` installing executables with 'go get' in module mode is deprecated.         Use 'go install pkg@version' instead.       ...
</details>

## #225 eats up 2 GB of RAM in ~2 mins and crashes with OOM error
**State:** CLOSED | **Author:** @nonchalant-enthusiast | **Created:** 2022-03-07 | **Updated:** 2022-03-08 | **Comments:** 3

> behavior is unstable on 2GB VPS, Ubuntu 20.04 using latest docker v0.15.8. while generating approx. the same amount of traffic
> 
> ![Screenshot (31)](https://user-images.githubusercontent.com/27624986/157137074-935b5e6f-aa0c-4de9-a431-9744b6a78119.png)
> 
> ![Screenshot...

<details><summary>Comments (3)</summary>

- **@sivillakonski** (2022-03-08): @nonchalant-enthusiast , thanks for submitting the issue. I didn't use the profiler this time, so there might be other memory leaks around. Please report if you keep observing any memory related...
- **@arriven** (2022-03-08): I think the issue might be deeper than the one addressed in the referenced PR. I also don't experience it running latest code as a regular executable but do experience it in docker. Looking at it
- **@arriven** (2022-03-08): ok, I've found what it is, poked the author and fixing now
</details>

## #224 What about AWS Lightsail Containers?
**State:** CLOSED | **Author:** @paqpaqpaqpaq | **Created:** 2022-03-07 | **Updated:** 2022-04-04 | **Comments:** 19

> Hi! 
> i found a guide https://telegra.ph/pigdogbomber-by-db1000n-over-AWS-LighSail-03-04
> 
> And then i understand, that i can create many free container services with Mi Micro power (1 gb ram 0.25 vCPUs).
> 2 container services per region (14 region), 5-7 containers per container services
> 2x14x5 =...

<details><summary>Comments (19)</summary>

- **@mazanuj** (2022-03-08): This is not quite the answer to the question, but rather an addition. I carry out most of the launches using Google Cloud Shell - it's more or less clear there. I have decided to expand to AWS...
- **@arriven** (2022-03-08): @mazanuj it seems like everything boils down to the error from the point 4 of your comment. It seems like on aws the app fails to properly detect local ip for some reason. Not sure what is the exact...
- **@arriven** (2022-03-08): Edit: everything except the country checker, although it also might be related
- **@bitshape** (2022-03-08): @Arriven running latest build locally (not AWS) with VPN I see the same issue as in point 4.
- **@arriven** (2022-03-08): @bitshape are you running it in docker or as an executable? And in case of latter do you use sudo?
- **@mazanuj** (2022-03-08): > @mazanuj it seems like everything boils down to the error from the point 4 of your comment. It seems like on aws the app fails to properly detect local ip for some reason. Not sure what is the...
- **@bitshape** (2022-03-08): @Arriven running in docker
- **@paqpaqpaqpaq** (2022-03-08): @Arriven, but still, i really don`t understand.. is AWS lightsail ddos method good and work correct?  my logs with `ghcr.io/arriven/db1000n:latest`...
- **@paqpaqpaqpaq** (2022-03-08): @mazanuj so do u think the GCS is better because it can give non-Ukraine IP?
- **@paqpaqpaqpaq** (2022-03-08): @Arriven, @mazanuj   In AWS when u create container u can chose port...
- **@arriven** (2022-03-09): @paqpaqpaqpaq from the logs it looks like only one of the attacks is not working (yes, it generates most of the traffic, but I'm already assuming that traffic can be easily blocked by almost any DDoS...
- **@mazanuj** (2022-03-10): @paqpaqpaqpaq  1. > @mazanuj so do u think the GCS is better because it can give non-Ukraine IP?  No, not in this case because both of these services work from non-Ukrainian IP. There are no such...
- **@paqpaqpaqpaq** (2022-03-10): @mazanuj i got banned on AWS :( AWS requested my personal info for verification and explanation my reasons for using Amazon Web Services  @Arriven, @mazanuj  you didn't get smth like that?
- **@amaestr0** (2022-03-28): Hey, folks! Sorry if I maybe dupplicate the question, but: using the doc https://telegra.ph/pigdogbomber-by-db1000n-over-AWS-LighSail-03-04 I decided to add more then 1 container per service and...
- **@arriven** (2022-03-29): I'm not an expert on AWS lightsail but can you show the error it throws?
- **@amaestr0** (2022-03-29): > I'm not an expert on AWS lightsail but can you show the error it throws?  @Arriven, thank you for your response. Sure, please see the logs from the container...
- **@arriven** (2022-03-31): How much memory does a single container have? if it's less than 512MB then you might want to disable encryption and prometheus as those lead to occasional memory spikes
- **@amaestr0** (2022-03-31): > How much memory does a single container have? if it's less than 512MB then you might want to disable encryption and prometheus as those lead to occasional memory spikes  1 GB RAM per container...
- **@Amet13** (2022-04-04): Terraform implementation:  https://github.com/Arriven/db1000n/pull/488
</details>

## #223 Container stop after minute of work on VPS server
**State:** CLOSED | **Author:** @timsofteng | **Created:** 2022-03-07 | **Updated:** 2022-03-07 | **Comments:** 1

> Container stop after one minute on VPS server. On local machine it works fine.
> 
> Logs last tail:
> ```
>  docker logs a4b1ae6eab115b900dbbc016c210436460868c7a56d15f6f03e1c3582e4825d0 --tail 100
> 2022/03/07 20:19:08.640356 http.go:71: Attacking http://194.54.14.168:80
> 2022/03/07 20:19:09.500612...

<details><summary>Comments (1)</summary>

- **@iamtodor** (2022-03-07): duplicate. should be closed @Arriven
</details>

## #222 terraform aws use spot instances 
**State:** CLOSED | **Author:** @industral | **Created:** 2022-03-07 | **Updated:** 2022-03-07 | **Comments:** 2

> So far we pay for on demand instances, and it takes money.
> Using spot instances - cheeper and allow to run more server for the same money :)
> 
> Need spot instances configuration for aws.
> Thanks :)

<details><summary>Comments (2)</summary>

- **@iamtodor** (2022-03-07): @industral @Arriven wasn't it implemented here https://github.com/Arriven/db1000n/pull/213 ?
- **@industral** (2022-03-07): Many thanks! You guys do changes too fast :)
</details>

## #221 Why it finishes working after a minute or less?
**State:** CLOSED | **Author:** @ivan-huligan | **Created:** 2022-03-07 | **Updated:** 2022-03-08 | **Comments:** 13

> The tool stops processing after a minute or less. There was no Russian ship or the traffic message at all, just the attacks

<details><summary>Comments (13)</summary>

- **@Tronerta** (2022-03-07): Same using docker
- **@arriven** (2022-03-07): Can you send the logs?
- **@Zinger1988** (2022-03-07): Same issue:  `runtime: failed to create new OS thread (have 962 already; errno=8) fatal error: runtime.newosproc  runtime stack: runtime.throw({0x7caf4f, 0x11})        ...
- **@arriven** (2022-03-07): kk, I see what's the issue here, will update the config to temporarily resolve it until I get an idea of a better fix
- **@timsofteng** (2022-03-07): Same here. Added issue with logs as well
- **@iamtodor** (2022-03-07): @timsofteng why did you create a new issue https://github.com/Arriven/db1000n/issues/223 instead of putting logs here in order to keep everything in one place?
- **@timsofteng** (2022-03-07): > @timsofteng why did you create a new issue #223 instead of putting logs here in order to keep everything in one place?  I've seen this after creating. Let me fix it.
- **@timsofteng** (2022-03-07): Same here. Container stop after one minute on VPS server. On local machine it works fine.  Logs last tail: ```  docker logs a4b1ae6eab115b900dbbc016c210436460868c7a56d15f6f03e1c3582e4825d0...
- **@arriven** (2022-03-07): if the issues started around 16:00 UTC (18:00 Kyiv time or ~5 hours ago) - the issue should be fixed now
- **@arriven** (2022-03-07): fun fact - this was due to an experimental feature aimed at maximizing resource usage for generating requests, but it turned out leaving it unsupervised is not a good idea (when I was testing it I...
- **@ivan-huligan** (2022-03-07): not fixed in v0.5.18. Still the same
- **@Zinger1988** (2022-03-08): In my case everything is fine at this moment. Issue was fixed. 0.5.17
- **@arriven** (2022-03-08): There were 2 different issues - one for the amount of OS thread used, another for metrics memory usage, both should be fixed as of 0.5.19
</details>

## #217 Failed to fetch config
**State:** CLOSED | **Author:** @pashagolub | **Created:** 2022-03-07 | **Updated:** 2022-03-31 | **Comments:** 24

> The latest 0.5.15 built from sources with go1.17.6 windows/amd64 produces a lot of errors:
> ```
> ...
> 2022/03/07 17:57:30.176608 runner.go:160: Failed to fetch config from "https://raw.githubusercontent.com/db1000n-coordinators/LoadTestConfig/main/config.json": Get...

<details><summary>Comments (24)</summary>

- **@freey0urmind** (2022-03-08): The same issue on Ubuntu 18.04. At the moment the script is generating much less trafic as it was earlier.
- **@industral** (2022-03-08): yeah had the same as well, and agree on traffic. But it might be `-advanced` image, that try to work in stealth mode. In my case traffic is about 3-12Kb when app show avg traffic. It's super low, in...
- **@vladdancer** (2022-03-08): @industral , I'm using avanced image and having similar problem: ``` Failed to fetch config from "https://raw.githubusercontent.com/db1000n-coordinators/LoadTestConfig/main/config.adv.json":  Get...
- **@industral** (2022-03-08): What I saw when it happened, because db1000n container started and openvpn container failed at some point. And also tried to check connection from container and it was without internet...
- **@bitshape** (2022-03-08): Docker VPN container already has health check to see if Internet is up:  https://github.com/wfg/docker-openvpn-client/blob/master/Dockerfile#L26  I'll investigate VPN angle as well a bit more as...
- **@arriven** (2022-03-08): > - `Body' expected type 'string', got unconvertible type 'map[string]interface {}', value: 'map[login:{{ random_uuid }} password:{{- random_int -}}{{- random_int -}}{{- random_int -}}{{- random_int...
- **@bitshape** (2022-03-08): ```diff diff --git a/main.go b/main.go index 37207e4..1491922 100644 --- a/main.go +++ b/main.go @@ -75,6 +75,9 @@ func main() {                 templates.SetProxiesUrl(proxiesURL)        ...
- **@freey0urmind** (2022-03-09): Even though the fetch line is till there I believe the situation is better now but I am kinda confused ))  ``` 2022/03/09 19:21:20.691044 config.go:82: **Could not load new config, proceeding with...
- **@freey0urmind** (2022-03-10): The fetch error line and the "Could not load new config, proceeding with the backup one" has gone. Thank you!
- **@bitshape** (2022-03-10): I've opened two PRs that might help with this issue or at least make it happen less often:  https://github.com/Arriven/db1000n/pull/275 https://github.com/Arriven/db1000n/pull/274
- **@vladdancer** (2022-03-10): Thank you @bitshape, @Arriven. But I'm still having the same erros from the above. The only issue that has gone: `Body' expected type 'string', got unconvertible type 'map[string]interface `  The...
- **@arriven** (2022-03-10): @vladdancer PRs @bitshape has referenced were only included in v0.6.5 which was kicked off 5 minutes ago. It's not going to remove the issue completely but still worth checking
- **@vladdancer** (2022-03-10): Thank you @Arriven . Yeah, I've updated docker image to the lates 0.6.5. But still having error with fetching advanced config, when enabled VPN outside of container.
- **@bitshape** (2022-03-10): @vladdancer can you share relevant logs?
- **@vladdancer** (2022-03-10): I'm running the next script: ``` expressvpn disconnect docker stop $(docker ps -a -q) docker pull ghcr.io/arriven/db1000n-advanced:latest expressvpn connect smart sleep 10 docker run --rm...
- **@freey0urmind** (2022-03-10): I was too fast saying the fetch issue had gone. Actually it does not occur just when I am vpn connected to one specific country. In that case like a hundred of jobs are available (IPs). When I am...
- **@vladdancer** (2022-03-12): Ok, I think as a workaround for fetching config I should try to download it manualy with disabled vpn and then run db1000n container with overwritten entry point to specify path to the...
- **@arriven** (2022-03-13): @vladdancer that one might actually be a bug. The way I did file vs url checking is probably detecting full path as some malformed protocol, I'll make a fix shortly, meanwhile you can try that same...
- **@arriven** (2022-03-13): @vladdancer I've merged a fix for that particular problem, try using `db1000n-beta` image to confirm it works with your setup with passing config to the program via docker volume
- **@bitshape** (2022-03-13): @vladdancer i’m working on Docker solution that should fix this hopefully for good.
- **@vladdancer** (2022-03-13): Thank you Arriven! It was not obvious to get right app path for the beta image, but I've managed it :) Thanks god there is a tool https://github.com/wagoodman/dive and `docker inspect`  ``` curl ...
- **@vladdancer** (2022-03-15): Guys, you're so fast with recent updates) I got broken db1000n. Any ideas why the app doesn't generate traffic anymore?   ``` docker run --rm  -v "$(pwd)"/config.adv.json:/ko-app/config.adv.json...
- **@arriven** (2022-03-15): @vladdancer the problem was this line `config.go:135: Can't decrypt config` beta images don't contain proper encryption keys and at the time whole config was encrypted. I've changed it to encrypt...
- **@arriven** (2022-03-15): unless you want to help testing out new functionality, but even then it's better running most of your instances on regular images and only 1 or 2 on beta to be able to spot issues in new features...
</details>

## #216 docker-compose example doesn't work
**State:** CLOSED | **Author:** @industral | **Created:** 2022-03-07 | **Updated:** 2022-03-07 | **Comments:** 1

> Using slightly modified docker-compose example from https://github.com/Arriven/db1000n/blob/main/docker-compose.yml
> 
> ```yaml
> version: "3.3"
> 
> services:
>   # creates OpenVPN Docker container to first provider that randomly picks .conf file
>   ovpn_01:
>     image:...

<details><summary>Comments (1)</summary>

- **@industral** (2022-03-07): `VPN_CONFIG_FILE: "*.ovpn"`  should be `VPN_CONFIG_PATTERN` 🤦‍♂️
</details>

## #214 A lot of exceptions
**State:** CLOSED | **Author:** @Vladisl0ve | **Created:** 2022-03-07 | **Updated:** 2022-03-08 | **Comments:** 6

> Version: 0.5.15
> OS: Windows 
> 
> After 5-15 seconds starts to spam exceptions to the cmd.
> 
> https://imgur.com/a/PPvN0Tw

<details><summary>Comments (6)</summary>

- **@pvlvld** (2022-03-07): The same problem Win 11 AMD v0.5.15
- **@arriven** (2022-03-07): Can you paste the log here? The way the app is designed it doesn't impact it as a whole but rather just some of the attacks but it would be nice to be able to assess the impact
- **@pvlvld** (2022-03-07): >  I can not record the moment of the fall, the error fills the entire console buffer! https://anonfiles.com/j7T48cMfxb/piece_of_log_txt
- **@arriven** (2022-03-07): use log redirection to file and attach that file to the issue
- **@Vladisl0ve** (2022-03-08): With new patch (0.5.20) there are no problems. I'm gonna close issue if @Liar4u also has no exceptions in cmd
- **@pvlvld** (2022-03-08): @Vladisl0ve fixed.
</details>

## #211 Installation trough pipe doesn't work on Debian
**State:** CLOSED | **Author:** @olegykz | **Created:** 2022-03-07 | **Updated:** 2022-03-07 | **Comments:** 2

> ```
> admin@ip-XXX:~$ uname -a
> Linux ip-XXX 4.19.0-14-cloud-amd64 #1 SMP Debian 4.19.171-2 (2021-01-30) x86_64 GNU/Linux
> 
> admin@ip-XXX:~$ curl https://raw.githubusercontent.com/Arriven/db1000n/main/install.sh | sh
>   % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
>  ...

<details><summary>Comments (2)</summary>

- **@olegykz** (2022-03-07): Installation through `source` works fine:  ``` admin@ip-XXX:~$ source <(curl https://raw.githubusercontent.com/Arriven/db1000n/main/install.sh)   % Total    % Received % Xferd  Average Speed  ...
- **@olegykz** (2022-03-07): Shall I create an appropriate fix for the README?
</details>

## #210 I have created DO terraform module, but I can't make pull requests.
**State:** CLOSED | **Author:** @dddbbbsss | **Created:** 2022-03-07 | **Updated:** 2022-03-31 | **Comments:** 1

> This module creates a number of servers in each of provided region. If you set count = 2 and regions = ["nyc1", "nyc2", "nyc3"] this will create six servers total. Two servers in each of regions.
> [repo](https://github.com/dddbbbsss/terraform_db1000n)

<details><summary>Comments (1)</summary>

- **@sivillakonski** (2022-03-08): Hi @dddbbbsss, thanks for the contribution! Can you please create a fork of this repo, add your changes, and later just create a PR request from your...
</details>

## #208 Incorrect traffic statistics displaying
**State:** CLOSED | **Author:** @IvanFromUa | **Created:** 2022-03-07 | **Updated:** 2022-03-07 | **Comments:** 2

> Displayed traffic statistic is not match with Task manager data about using network.
> While Task manager is showing this:
> ![Perfomance_NET_07032022](https://user-images.githubusercontent.com/26162607/157021656-60fed17c-0442-4c8e-9e1f-44b337671b38.png)
> 
> db1000n via commad line is displaying: "The...

<details><summary>Comments (2)</summary>

- **@arriven** (2022-03-07): The metrics in the app are approximate as it doesn't count some internal protocol data, unless the numbers displayed by the app are higher than traffic usage I wouldn't focus on it yet (but if anyone...
- **@IvanFromUa** (2022-03-07): This answer satisfies me. Thanks!
</details>

## #206 New targets for attack 
**State:** CLOSED | **Author:** @iamtodor | **Created:** 2022-03-07 | **Updated:** 2022-03-31 | **Comments:** 7

> The targets from https://dou.ua/forums/topic/36969/
> Author is @dmytro-bilokha

<details><summary>Comments (7)</summary>

- **@dmytro-bilokha** (2022-03-07): I suggest targeting API gateways of payment processors and banks: web.rbsuat.com 62.76.205.112 3dsec.sberbank.ru 62.76.205.110 auth.robokassa.ru 104.18.26.14 auth.robokassa.ru...
- **@dmytro-bilokha** (2022-03-07): If you are interested in payment API gateways, I could find more.
- **@dmytro-bilokha** (2022-03-07): Here is the JSON snippet for the mentioned hosts: ```json {     "type": "http",     "args": { 	"method": "GET", 	"path": "https://104.18.26.14:443", 	"interval_ms": 1, 	"client": { 	   ...
- **@iamtodor** (2022-03-07): @Arriven please take a look
- **@freey0urmind** (2022-03-10): The script has started targeting a lot of IPs instead of a few urls recently. Is it normal? Thank you.
- **@arriven** (2022-03-10): @freey0urmind yes, it is normal
- **@dmytro-bilokha** (2022-03-10): @Arriven should I try to find more payment providers? Do you have a capacity to target them?
</details>

## #204 If Russia blocks github, config won't load when using RU VPN
**State:** CLOSED | **Author:** @Devaniti | **Created:** 2022-03-07 | **Updated:** 2022-03-31 | **Comments:** 10

> We need to make some kind of mirror, for RU VPN users

<details><summary>Comments (10)</summary>

- **@Devaniti** (2022-03-07): Preferably, it should be some large HTTPS website, so they can't easily block it
- **@arriven** (2022-03-07): This is a good idea. I'll add that the app can already be configured to fetch config from multiple sources so the only part we need is to get that mirror up and running
- **@Devaniti** (2022-03-07): I'll try to do it
- **@bitshape** (2022-03-07): We could setup AWS Route 53-backed DNS with really low TTL (5 seconds) with Geo DNS. If request comes from RU, we route it to a known good mirror that can be accessed through RU VPN. If that mirror...
- **@Devaniti** (2022-03-07): @bitshape I'll setup mirror for git repo on another hosting, and you can setup AWS mirror more mirrors is good, just in case
- **@bitshape** (2022-03-10): @Devaniti I've looked into setting this up on AWS S3 as mirror and if Docker image download stats are any indication, it's going to cost prohibitive for me to run (~$3.5K/month).
- **@Devaniti** (2022-03-10): @bitshape that's sad. Hopefully, small percentage of people will need to use that mirror, and they will load small config file. But they will reload it every minute. So it's hard to know for sure...
- **@makbar1234** (2022-03-14): > We could setup AWS Route 53-backed DNS with really low TTL (5 seconds) with Geo DNS. If request comes from RU, we route it to a known good mirror that can be accessed through RU VPN. If that mirror...
- **@bitshape** (2022-03-14): @makbar1234 one reason I haven't set up Route 53 yet is that I don't have good solution to the following problem: the weak point becomes domain name used for mirrors as that can be blocked in Russia,...
- **@Lagovas** (2022-03-17): additionally, db1000n supports embedding config file into the binary. so it can work without remote config files plus, someone can use yandex disc and share there config file by link )
</details>

## #201 Strange network traffic statistics
**State:** CLOSED | **Author:** @novikor | **Created:** 2022-03-07 | **Updated:** 2022-03-07 | **Comments:** 4

> **Preconditions**:
> Linux mint + docker
> 
> **Steps to reproduce:**
> run `docker run --rm ghcr.io/arriven/db1000n:latest`
> 
> **Expected result:**
> Incoming traffic in less than outcoming one
> 
> **Actual...

<details><summary>Comments (4)</summary>

- **@arriven** (2022-03-07): I'll check out the config in a minute but I'd assume that this means that targets it attacks don't use any DDoS protection and actually process and respond to requests. I'm not completely sure but it...
- **@Devaniti** (2022-03-07): ddosing you back is certainly not happening here, you can clearly see that incoming traffic triggered by starting the app so I'd too say that it works as expected
- **@arriven** (2022-03-07): I think I know which attack is triggering this behavior and this graph is a good indication that the attack is not detected as DDoS by the receiving party. Having inspected the attack I also suspect...
- **@novikor** (2022-03-07): @Arriven , thank you!
</details>

## #200 Figure out a way to run packetgen without root permissions `[priority: low]`
**State:** CLOSED | **Author:** @arriven | **Created:** 2022-03-07 | **Updated:** 2022-03-31 | **Comments:** 2

> Currently packetgen jobs send this type of message when you run the program under regular user
> `2022/03/07 06:51:38.219638 packetgen.go:77: Error sending packet: listen ip4:tcp 0.0.0.0: socket: operation not permitted`
> This is happening because it needs raw connection in order to be able to...

<details><summary>Comments (2)</summary>

- **@Boostro** (2022-03-08): I have a similar issue. `packetgen.go:65: Error sending packet: listen ip4:tcp 0.0.0.0: bind: An invalid argument was supplied.`
- **@neuton** (2022-03-21): I believe the only alternative way (under Linux) is to set CAP_NET_RAW capability on the executable, as mentioned by answers here...
</details>

## #195 missing value for "attack_environment_variables" for azure terraform config
**State:** CLOSED | **Author:** @nonchalant-enthusiast | **Created:** 2022-03-06 | **Updated:** 2022-03-07 | **Comments:** 0

> empty default value was removed from the variable: https://github.com/Arriven/db1000n/blame/main/terraform/azure/bomblet/variables.tf#L21
> now the terraform deployment is failing because of it

## #194 docs with mkdocs
**State:** CLOSED | **Author:** @m-v-kalashnikov | **Created:** 2022-03-06 | **Updated:** 2022-03-31 | **Comments:** 1

> As soon as project have multilanguage and as I see here will be quite big documentation I assume that it'll be better to use mkdocs.
> If you find this helpful, I can take care of this.
> Thanks

<details><summary>Comments (1)</summary>

- **@arriven** (2022-03-09): @m-v-kalashnikov sorry, only got to this issue now. Not sure that this project is at that stage yet or if it will get to that stage at all but it would be cool to see how mkdocs work so if you want...
</details>

## #191 Update tutorial on Google Drive
**State:** CLOSED | **Author:** @Amet13 | **Created:** 2022-03-06 | **Updated:** 2022-03-07 | **Comments:** 6

> This doc was mentioned in the large telegram channel: https://docs.google.com/document/d/1onvSrNu1FnNKDHD0Mtwf0KoOSuZJOClHqHOs5cu20Mc/edit#
> 
> If someone has access to it, it would be great to update it, at least links to binaries
> 
> @Arriven fyi

<details><summary>Comments (6)</summary>

- **@iamtodor** (2022-03-06): @Amet13 I see no point to maintain this doc as well. We have two READMEs: - https://github.com/Arriven/db1000n/blob/main/README.md - https://github.com/Arriven/db1000n/blob/main/README-ua.md  I...
- **@Amet13** (2022-03-06): agree with that
- **@iamtodor** (2022-03-07): @Amet13 have any actions been applied? I see that the content of the file wasn't changed. @Arriven let's update the doc itself by providing links to READMEs Until that I suggest don't close this...
- **@Amet13** (2022-03-07): AFAIK, we don't have access to this doc. Seems like someone just copy-pasted readme some time ago and we can't help with updating or deleting this doc
- **@iamtodor** (2022-03-07): @Amet13 hmmmm.. I thought @Arriven is the author of the doc, no? :D
- **@Amet13** (2022-03-07): I don't know, as I said, I found link to this doc in the large telegram channel
</details>

## #190 docker compose random VPM
**State:** CLOSED | **Author:** @industral | **Created:** 2022-03-06 | **Updated:** 2022-03-07 | **Comments:** 3

> So far I see in docker compose we have predefined VPN endpoints
> 
> https://github.com/Arriven/db1000n/blob/main/docker-compose.yml `VPN_CONFIG_FILE: provider01.endpoint01.conf`
> 
> I like the approach you did when you provide openvpn folder and it select VPN randomly.
> it might be very useful to...

<details><summary>Comments (3)</summary>

- **@bitshape** (2022-03-06): @industral I'm working on this, PR incoming in a bit
- **@bitshape** (2022-03-06): @industral https://github.com/Arriven/db1000n/pull/193
- **@industral** (2022-03-07): nice! thank you!
</details>

## #189 [Discussion] Providing certain restricted access to the repo
**State:** CLOSED | **Author:** @iamtodor | **Created:** 2022-03-06 | **Updated:** 2022-03-07 | **Comments:** 6

> As a follow up to the PR https://github.com/Arriven/db1000n/pull/187
> Please take a look at the docs:
> -  https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/managing-repository-settings/managing-teams-and-people-with-access-to-your-repository 
> -...

<details><summary>Comments (6)</summary>

- **@synapse-unix** (2022-03-06): Please note paths how this MR was submitted https://github.com/db1000n-coordinators/LoadTestConfig/commit/b8886cce0aa5787260046e4acbab35832a347ec5  It broke async load once again! We can have more of...
- **@iamtodor** (2022-03-06): @dmy3tka I'm not sure whether your comment relates to the topic
- **@synapse-unix** (2022-03-06): @iamtodor what is intend of your activity, to limit possibility of merging MRs that broke things from unreliable sources? As you can check, the merged commit above removed async, that degrades CPU...
- **@iamtodor** (2022-03-06): @synapse-unix `what is intend of your activity, to limit the possibility of merging MRs that broke things from unreliable sources?` - actually no. I would like to have the access to issues / PRs.  I...
- **@arriven** (2022-03-06): @iamtodor it looks like personal repos don't support triage access. I'd need to create an organization and move the repo there to be able to manage access at that level. Let's see if that is required...
- **@iamtodor** (2022-03-07): @Arriven I cannot accept the invitation <img width="620" alt="image" src="https://user-images.githubusercontent.com/12586108/156991518-e9b0e19b-b208-43bf-b23a-feb23cdfd7b2.png">
</details>

## #183 Online config won't update when using proxychains-ng
**State:** CLOSED | **Author:** @SomalianCoolhacker | **Created:** 2022-03-06 | **Updated:** 2022-03-31 | **Comments:** 4

> Hi, my VM (Ubuntu 20.04 LTS) can't reach online config using proxychains (country RU, socks4/5 proxies):
> > ~$: sudo proxychains ./db1000n
> > [WARN] Failed to fetch config from "https://raw.githubusercontent.com/db1000n-coordinators/LoadTestConfig/main/config.json": Get...

<details><summary>Comments (4)</summary>

- **@arriven** (2022-03-06): You can download the config and pass the path to it via `-c path/to/file.json` as a workaround
- **@SomalianCoolhacker** (2022-03-06): Thanks! If I'll create a script that redownloads config occasionally, will an already running db1000n update targets as well?
- **@arriven** (2022-03-06): db1000n updates targets automatically regardless whether it's pointed at remote or local config. You should even be able to do something like `-c https://remote/config/url,path/to/local/config`- that...
- **@arriven** (2022-03-31): Closing this as there are already multiple solutions like the one in `examples/docker/static-docker-compose.yml`
</details>

## #182  The app doesn't seem to generate any traffic, please contact your admin
**State:** CLOSED | **Author:** @ivan-huligan | **Created:** 2022-03-06 | **Updated:** 2022-03-06 | **Comments:** 6

> After updating from the release v0.5.13 to the release v0.5.14 the error message constantly appears
> ` The app doesn't seem to generate any traffic, please contact your admin`

<details><summary>Comments (6)</summary>

- **@su-hs** (2022-03-06): I confirm, I also see this warning.
- **@mxmCherry** (2022-03-06): Seems to be a problem with metrics tracking. The app itself seem to be working fine (traced it properly - it still generates traffic).
- **@mxmCherry** (2022-03-06): UPD: actually nope, metrics are "fine" (metric design choices are questionable, but they kinda work). What actually happens is:  - approx bytes written are stored only for last second measured -...
- **@arriven** (2022-03-06): Yeah, metrics were added rather quickly with focus on showing users at least something (remember, the app is just a bit more than a week old). I think I'll change it to track overall traffic...
- **@mxmCherry** (2022-03-06): Right now my question is "**shoud we decrease default timeout in the program? I suggest 1-5 seconds default, not more**" so if load-testing target doesn't hold the load app from testing other...
- **@arriven** (2022-03-06): For async=true ideally we'd implement sending http frames into packetgen or use something similar to send http frames without waiting for response in a more efficient manner. We need to consider ROI...
</details>

## #177 fix ip
**State:** CLOSED | **Author:** @krotoveugene | **Created:** 2022-03-06 | **Updated:** 2022-03-06 | **Comments:** 4

> https://raw.githubusercontent.com/db1000n-coordinators/LoadTestConfig/main/config.adv.json
> ```{
>             "type": "http",
>             "args": {
>                 "method": "GET",
>                 "path": "https://1185.114.138.220:443", !!!!!!! 
>                 "interval_ms": 1
>             }
> ...

<details><summary>Comments (4)</summary>

- **@krotoveugene** (2022-03-06): @arfgdev need to fix typo in IP - https://1185.114.138.220:443
- **@5har0varik** (2022-03-06): I may create PR but cant locate file in repo =\
- **@mxmCherry** (2022-03-06): Already PR-ed in relevant repo, even twice:  - https://github.com/db1000n-coordinators/LoadTestConfig/pull/10 - https://github.com/db1000n-coordinators/LoadTestConfig/pull/9
- **@arriven** (2022-03-06): This was fixed 5 hours ago, thanks for heads up though!
</details>

## #175 Change cloud instructions to use db1000n-advanced by default `[documentation, priority: high]`
**State:** CLOSED | **Author:** @arriven | **Created:** 2022-03-06 | **Updated:** 2022-03-06 | **Comments:** 0

> I've created a separate image pointing to another config instance using specific attacks that are harder to detect and don't impact bills as much. We should switch guides for clouds to use it by default to avoid issues like high traffic billing or cloud provider locking up the instance thinking it...

## #174 ignore
**State:** CLOSED | **Author:** @su-hs | **Created:** 2022-03-06 | **Updated:** 2022-03-06 | **Comments:** 0

> false alarm

## #170 DDoS effectiveness is not directly tied to the amount of traffic generated `[documentation, help wanted, priority: medium]`
**State:** CLOSED | **Author:** @arriven | **Created:** 2022-03-06 | **Updated:** 2022-03-06 | **Comments:** 5

> The app is configurable to generate set amount of traffic (controlled by the number of targets, their type, and attack interval for each of them). The main reason it works that way is because there are two main types of ddos:
> 
> - Straightforward load generation (easy to implement, easy to defend...

<details><summary>Comments (5)</summary>

- **@arriven** (2022-03-06): @Amet13 @iamtodor tagging you here
- **@Amet13** (2022-03-06): My proposal is to create a separate document called `FAQ.md` (for non-technical, let's say questions).  In this document add information in format `question` - `answer`.  For example, issues...
- **@arriven** (2022-03-06): I'm also adding another docker image which points to another config file to be used by advanced users that understand this (especially in clouds). We'll probably need to update advanced users docs...
- **@iamtodor** (2022-03-06): @Amet13 I also have something to add in FAQ
- **@iamtodor** (2022-03-06): as just general question/answer
</details>

## #165 Next Milestone | BLOCK
**State:** CLOSED | **Author:** @bmirnoff | **Created:** 2022-03-06 | **Updated:** 2022-03-06 | **Comments:** 3

> This is a strategic post. 
> 
> I think next milestone might be a shift from chaos dos to a situation when doing it is profitable or makes achievements.  
> This might be done like a blockchain. Proposal:
> 
> Layer 2 tokens that might be minted during the execution of attacks. 
> For instance
> - each...

<details><summary>Comments (3)</summary>

- **@bmirnoff** (2022-03-06): Goals: - gamification for all remaining world  - maintain **interest**   I think these are important actions and effects from each of them hard to estimate.
- **@bmirnoff** (2022-03-06): Issues: - tokens might be a part of illegal activity, but who cares now?  - impact on the chain community, also hard to estimate. There are a lot of scum there, so the key point is that this...
- **@arriven** (2022-03-06): We're currently forced to work in a gray hat area by this awful situation. Minting tokens with this would turn this into black hat. I want to turn it into white hat to be used by security...
</details>

## #162 Old targets for Linux users
**State:** CLOSED | **Author:** @Vladisl0ve | **Created:** 2022-03-05 | **Updated:** 2022-03-07 | **Comments:** 3

> Targets on Windows:
>  
> ![image](https://user-images.githubusercontent.com/36882979/156900359-2be5905b-9771-4b5f-b930-dbab3e96d0a6.png)
> 
> Targets on Linux (Ubuntu 21.04) even with some errors on the...

<details><summary>Comments (3)</summary>

- **@Amet13** (2022-03-05): Could you please run the command:  ```bash docker inspect ghcr.io/arriven/db1000n ``` on both Windows and Linux?  Errors on the 2nd screenshot seems related to DNS issues on the host
- **@Vladisl0ve** (2022-03-05): >   Linux: ``` uladzislau@y700-linux-server:~/russia_ddos$ sudo docker inspect ghcr.io/arriven/db1000n [     {         "Id":...
- **@Vladisl0ve** (2022-03-07): @Amet13 after last update (0.5.15) works fine  Thank you :)
</details>

## #157 Creating a list of required protocols to support
**State:** CLOSED | **Author:** @sivillakonski | **Created:** 2022-03-05 | **Updated:** 2022-03-07 | **Comments:** 0

> Hi there, folks,
> 
> I see how many people are currently working on a project, it's just brilliant.
> Not to intersect with each other, is it possible to have a list of protocols to benchmark?
> 
> For example:
> * VPN jamming
> * SIP high-load test
> * etc.

## #153 Yesterday traffic eat a huge amount of money `[documentation, priority: critical]`
**State:** OPEN | **Author:** @vgoncharenko | **Created:** 2022-03-05 | **Updated:** 2022-03-25 | **Comments:** 11

> Guys, do we have any coupons for AWS? yesterdays traffic eat huge amount of money.
> 
> Bandwidth$4,934.30
> $0.000 per GB - data transfer in per month339.145 GB$0.00
> $0.000 per GB - data transfer out under the monthly global free tier100.000 GB$0.00
> $0.000 per GB - regional data transfer under the...

<details><summary>Comments (11)</summary>

- **@industral** (2022-03-05): yes, write to them.. but I don't know how you'll explain that traffic. They might forgive you that and might issue coupon to redeem.
- **@arriven** (2022-03-06): This would happen with other DDoS solutions running on clouds as well but we need to add a warning to instructions since not everyone might be aware that most big cloud providers bill you for...
- **@Amet13** (2022-03-06): @Arriven yep.  https://github.com/Arriven/db1000n/pull/168/commits/1c4fe4787d7064b6b89ba8731e07c0a8cd2d345f
- **@arriven** (2022-03-06): I'll leave this issue as open for people to be aware at least until this war ends
- **@Amet13** (2022-03-06): Maybe it would be great to label it somehow to highlight it from other issues (or pin it somehow at the top). _Not sure that GitHub allows issues pinning_
- **@arriven** (2022-03-06): I'll create a separate docker release for that in a minute but please use https://raw.githubusercontent.com/db1000n-coordinators/LoadTestConfig/main/config.adv.json as your config on clouds to avoid...
- **@iamtodor** (2022-03-06): relates to https://github.com/Arriven/db1000n/issues/54
- **@vgoncharenko** (2022-03-16): AWS team have approved bill adjustments for my acc: `We’ve approved a billing adjustment of $5,099.73 USD for charges on your March bill, which has been applied as a credit to your account. This...
- **@industral** (2022-03-16): congrats!
- **@kurlyk-dev** (2022-03-24): @Arriven Is [adv](https://raw.githubusercontent.com/db1000n-coordinators/LoadTestConfig/main/config.adv.json) config still relevant? It hasn't been updated for 4 days, maybe I should switch to the...
- **@khardho120777** (2022-03-25): bahala kayo sa buhay mo problema nyu na yan masstress lang ako sainyo
</details>

## #148 Move proxylist url to commandline parameters `[help wanted, good first issue, priority: medium]`
**State:** CLOSED | **Author:** @arfgdev | **Created:** 2022-03-05 | **Updated:** 2022-03-06 | **Comments:** 1

> can I provide my own link to proxy file in config?

<details><summary>Comments (1)</summary>

- **@arriven** (2022-03-05): As of now you'll need to recompile the binary for that but it's quite easy to move that setting into the commandline. I think we should do it, will set medium priority and help wanted labels to this...
</details>

## #146 gcp-installation-ua.md  not working 
**State:** CLOSED | **Author:** @sergnochevny | **Created:** 2022-03-05 | **Updated:** 2022-03-06 | **Comments:** 4

> cloud instance becomes unavailable after running openvpn3.sh from gcp-installation-ua.md
> checked on DO and GCP

<details><summary>Comments (4)</summary>

- **@Amet13** (2022-03-05): @Arriven @iamtodor as I mentioned before in this comment: https://github.com/Arriven/db1000n/issues/118#issuecomment-1059743438 this doc looks a bit strange. Can we find an author of it to review...
- **@iamtodor** (2022-03-05): @Amet13 @Arriven as I suggested before let's keep only English version
- **@arriven** (2022-03-05): Let's find the author first, if we get no feedback in 12 hours we can delete it but there's no rush yet since these guides expect at least some level of technical expertise which might be enough to...
- **@arriven** (2022-03-05): I think we should also enforce the rule where at least two other people should validate new guides/big changes to guides and different scripts/terraform/k8s_manifests/docker-compose files which we...
</details>

## #145 Incorrect color output in default windows command prompt `[bug, priority: low]`
**State:** CLOSED | **Author:** @MAKMED1337 | **Created:** 2022-03-05 | **Updated:** 2022-03-31 | **Comments:** 11

> Logs looks bad at windows 
> ![image](https://user-images.githubusercontent.com/50710486/156887852-aeb78999-8021-4cd5-9fc0-fc6b5498649f.png)

<details><summary>Comments (11)</summary>

- **@Devaniti** (2022-03-05): You can use Windows Terminal to get better output
- **@Amet13** (2022-03-05): @Devaniti could you reproduce it on Windows? Unfortunately don't use it
- **@Devaniti** (2022-03-05): @Amet13 Yes, it's reproducible with default "cmd" console But with new "Windows Terminal" it works as expected
- **@Amet13** (2022-03-06): Seems like not an issue then?
- **@Devaniti** (2022-03-06): Windows Terminal is only available on Windows 10 But I'd say it's minor issue either way
- **@iamtodor** (2022-03-06): @Devaniti @Amet13 @MAKMED1337 do we have this issue while running binaries? what is the proper way to run it in Windows 10 then? I'd suggest to add a mention in our doc how to run it in Windows 10
- **@Amet13** (2022-03-06): @iamtodor I would say it works properly on the screenshot except for colors in default Terminal 😄
- **@iamtodor** (2022-03-06): @Amet13 okay, then I think we are free to close this issue right? Or we can leave it as open but change the title in order to not confuse ourselves
- **@Devaniti** (2022-03-06): I'd change the title to something like "Incorrect color output in default windows command prompt"
- **@iamtodor** (2022-03-06): @Devaniti fully agrees!   Only @MAKMED1337 and @Arriven are able to change the title or are there some people who have the rights and access? cc @Amet13
- **@pashagolub** (2022-03-06): Use PowerShell instead https://github.com/PowerShell/PowerShell
</details>

## #143 Consider adding codesenberg/bombardier with proxy attack
**State:** CLOSED | **Author:** @PXEiYyMH8F | **Created:** 2022-03-05 | **Updated:** 2022-03-31 | **Comments:** 1

> https://github.com/mariotrucco/bombardier/compare/78-add-proxy-support
> You can run it in 100+ threads and receive superpower (50k https req/s).
> 
> ```shell
> mkdir bombardier_tmp
> cd bombardier_tmp
> go mod init bombardier_tmp
> go mod edit -replace...

<details><summary>Comments (1)</summary>

- **@arriven** (2022-03-06): Can you try comparing it with this tool being configured to run single http job with "client.async":true and "count":100?
</details>

## #137 No matching manifest for linux/arm/v7 in the manifest list entries
**State:** CLOSED | **Author:** @YuriyKu | **Created:** 2022-03-05 | **Updated:** 2022-03-06 | **Comments:** 5

> Hello,
> I'm trying to run db1000n on raspberry pi3 with next error:
> 
> Unable to find image 'ghcr.io/arriven/db1000n:latest' locally
> latest: Pulling from arriven/db1000n
> docker: no matching manifest for linux/arm/v7 in the manifest list entries.
> 
> My system is:
> $ cat...

<details><summary>Comments (5)</summary>

- **@iamtodor** (2022-03-05): @YuriyKu take a look on https://github.com/Arriven/db1000n/issues/116
- **@Amet13** (2022-03-05): Support for arm/v7 already in master. In the next release, it will be deployed. Keep following https://github.com/Arriven/db1000n/pkgs/container/db1000n
- **@Amet13** (2022-03-06): @YuriyKu please try to pull the latest image again, it should work. Introduced arm/v7 support in 0.5.13  <img width="764" alt="Screenshot 2022-03-06 at 12 04 37"...
- **@YuriyKu** (2022-03-06): Hello, it works now. Thanks a lot.
- **@YuriyKu** (2022-03-06): Issue has been resolved. Thanks. Have a nice day.
</details>

## #136 Performance and multithreading
**State:** CLOSED | **Author:** @Devaniti | **Created:** 2022-03-05 | **Updated:** 2022-03-06 | **Comments:** 4

> On my machine, even with free VPN, I can get at least 10x performance by launching multiple instances
> We need to implement multithreading, so it can utilize all available resources
> Will try to do myself, but since I'm not that good at Golang I may need some help

<details><summary>Comments (4)</summary>

- **@Devaniti** (2022-03-05): ok, it seems that there's multithreading, but there's still bottleneck somewhere
- **@Devaniti** (2022-03-05): this is the offender, `for i := 0; i < jobDesc.Count; i++ {` `jobDesc.Count` is just too low
- **@arriven** (2022-03-05): @Devaniti I wouldn't call it a bottleneck but rather a design limitation. The app is configurable to generate set amount of traffic (controlled by the number of targets, their type, and attack...
- **@lomchik** (2022-03-06): So probably we should update targets to attack for example search endpoints  like https://www.rt.com/search?q=stupid+russian+bitches.
</details>

## #133 Network activity went down today. `[bug, priority: high]`
**State:** CLOSED | **Author:** @vgoncharenko | **Created:** 2022-03-05 | **Updated:** 2022-03-06 | **Comments:** 15

> Guys, something happened around 2:20 UTC.
> my command: docker run --pull=always ghcr.io/arriven/db1000n:latest
> Unfortunately, cant track if it was config changes.
> <img width="1095" alt="Screen Shot 2022-03-05 at 5 36 33 AM"...

<details><summary>Comments (15)</summary>

- **@arriven** (2022-03-05): I don't recall any config changes at that time. Need to investigate
- **@vgoncharenko** (2022-03-05): I don't have vpn, btw.  And there is no packet loss:  eth0: flags=4163<UP,BROADCAST,RUNNING,MULTICAST>  mtu 9001        ...
- **@arriven** (2022-03-05): I don't have any ideas on possible cause yet so there's no ETA yet. I'll try to look into it between other critical and high priority tasks since I'm genuinely interested in finding the cause but the...
- **@KarboDuck** (2022-03-05): Maybe it's just a case of new json file with smaller list of sites?  If you launch db1000n with previous json (from github history) net load is still high.  `./db1000n -c...
- **@synapse-unix** (2022-03-05): > Maybe it's just a case of new json file with smaller list of sites? >  >  >  > If you launch db1000n with previous json (from github history) net load is still high. >  >  >  > `./db1000n -c...
- **@KarboDuck** (2022-03-05): > Can you please give approximate numbers on how many targets was, and is now? I hardly believe it can go down from 1 container consumes 80% cpu core to < 10% cpu core because of a smaller target...
- **@vgoncharenko** (2022-03-05): Yes, I can confirm with that configuration metrics went up to where it...
- **@synapse-unix** (2022-03-05): The difference is, that in conf with higher usage, there is a "client": {"async": "true"}. Not sure who and why removed this option from some of the targets. @securims can you shed some light on...
- **@industral** (2022-03-05): confirm, have the same issue. CPU load is down, network - almost 0
- **@arriven** (2022-03-06): I've been referencing this in other issues, but essentially more traffic doesn't always mean better DDoS. We're trying different patterns to see whether they get blocked by the target (and even...
- **@synapse-unix** (2022-03-06): @Arriven so can you confirm now that async requests are not necessary now in the current load config? In such way, we will need to run more containers per cpu core if we stick to not use async as of...
- **@arriven** (2022-03-06): I've tried to explain some basic ideas on DDoS performance [here](https://github.com/Arriven/db1000n/issues/136)
- **@synapse-unix** (2022-03-06): Ok I see that you are trying to implement here. So 1 container is sufficient for this type of attack (as unique VM IP is required). To utlilize VM resources available for me, I will sidecar some...
- **@arriven** (2022-03-06): I think we'll do it the following way: create a separate config file that uses advanced techniques and generate less traffic and create a separate docker image pointing to that config. Regular users...
- **@industral** (2022-03-06): so was the bug fixed or not? I just tried to pull docker and didn't see any traffic again... config still the same..
</details>

## #132 Always same targets
**State:** CLOSED | **Author:** @YuriyChmil | **Created:** 2022-03-05 | **Updated:** 2022-03-07 | **Comments:** 15

> Hey. I am running this image on AWS via terraformm.
> From logs, I see that it attack only one IP with different port
> is it ok?
> `
> Attacking http://82.202.190.240:8010
> [INFO]  2022/03/05 11:22:21 [INFO] Attacking http://82.202.190.240:443
> [INFO]  2022/03/05 11:22:21 [INFO] Attacking...

<details><summary>Comments (15)</summary>

- **@vgoncharenko** (2022-03-05): same on my aws
- **@pavliukvlad** (2022-03-05): The same. I use docker image.
- **@iamtodor** (2022-03-05): same here
- **@arriven** (2022-03-05): I'll get back to take a closer look at this in couple minutes but for now can somebody check it against the config present...
- **@iamtodor** (2022-03-05): might relates to https://github.com/Arriven/db1000n/issues/121
- **@vgoncharenko** (2022-03-05): just about a minute ago it got fixed. Many new targets started showing up:  [INFO]  2022/03/05 12:32:58 [INFO] Attacking http://82.202.190.240:80 [INFO]  2022/03/05 12:32:58 [INFO] Attacking...
- **@pavliukvlad** (2022-03-05): I can confirm as well that there are a lot of new targets now.
- **@vgoncharenko** (2022-03-05): But all metrics went down dramatically as well: throughput went down from 470Mb/min to 200kb/min: And everything, CPU, packets. <img width="1122" alt="Screen Shot 2022-03-05 at 6 43 59 AM"...
- **@pavliukvlad** (2022-03-05): I also noticed that  ![image](https://user-images.githubusercontent.com/26973559/156883766-582a9f2f-e6cb-422c-add0-1f0e5adb1de8.png)
- **@iamtodor** (2022-03-05): can confirm the same. new targets have arrived @Arriven could you please shed some light on the issue? have you changed something? what was wrong or what was fixed?
- **@vgoncharenko** (2022-03-05): Looks like targets very week but still reachable:  Target 1: ``` PING 193.228.161.83 (193.228.161.83) 56(84) bytes of data. 64 bytes from 193.228.161.83: icmp_seq=1 ttl=34 time=133 ms 64 bytes...
- **@synapse-unix** (2022-03-05): Why CPU utilisation is dropped so drastically, do we fix resource leakage in code or rps is so week now and things broke?
- **@arriven** (2022-03-06): https://github.com/Arriven/db1000n/issues/136#issuecomment-1059756173
- **@iamtodor** (2022-03-06): @Arriven @Amet13 I think we can close this issue for now. What do you think?
- **@synapse-unix** (2022-03-06): We can close the issue. We don't have issue with targets update inside running containers.
</details>

## #131  Error response from daemon: invalid mount config for type "bind": bind source path does not exist: /root/openvpn.
**State:** CLOSED | **Author:** @mykola-dev | **Created:** 2022-03-05 | **Updated:** 2022-03-31 | **Comments:** 2

> Guys, need help with running on ubuntu with custom ovpn config. i put the .ovpn into the openvpn dir. running with ./run.sh
> get this error:
> ```
> ubuntu@ip-xxxxxxxxx:~/db1000n$ sudo ./run.sh
> ./run.sh: 1: Bad substitution
> unable to prepare context: unable to evaluate symlinks in Dockerfile path:...

<details><summary>Comments (2)</summary>

- **@vgoncharenko** (2022-03-05): If you add: set -ex  at the top of run.sh, it will print you everything it's going to run.  For some reason, it tries to use root's dir as current. Just to confirm it, add that command and try...
- **@arriven** (2022-03-05): @bitshape seems like this is your area of expertise
</details>

## #129 k8s. HealthCheck
**State:** CLOSED | **Author:** @oleksdovz | **Created:** 2022-03-05 | **Updated:** 2022-03-05 | **Comments:** 4

> k8s. HealthCheck
> Було б добре мати для аплікухи якийсь HealthCheck
> Тобто якшо пода залипла то її рестартнутию

<details><summary>Comments (4)</summary>

- **@oleksdovz** (2022-03-05): Крім того я знайшов такий ресурс із проксі - https://t.me/proxy_list_misha можливо можна інтегрувати для постійного оновленння або перечитання проксі коли пода рестартує
- **@Amet13** (2022-03-05): Я тестив функціонал імежду, якшо щось не так з аппкою, вона вилітає и кубер автоматично перезапскає под
- **@oleksdovz** (2022-03-05): ок, добре,  там проксі http?  як щодо файлів із  https://t.me/proxy_list_misha? вони оновлюються дуже часто. в теорії  список http proxy  можна оновляти при старті контейнера в поді, тільки  файл...
- **@arriven** (2022-03-05): @oleksdovz to be completely honest I'm still not convinced proxies actually improve the quality of attacks as there are different opinions on the topic and most of them say that it depends. This...
</details>

## #126 Groups  by different types of attack
**State:** CLOSED | **Author:** @bmirnoff | **Created:** 2022-03-05 | **Updated:** 2022-03-06 | **Comments:** 2

> Register each running client somewhere and assign the type of attack for each group.

<details><summary>Comments (2)</summary>

- **@arriven** (2022-03-05): @bmirnoff can you provide more info on what you mean and what benefit you want to get? There are a lot of improvement areas in this app now and it would help to prioritize work
- **@bmirnoff** (2022-03-06): Yes I think it makes 0 sense @Arriven
</details>

## #125 How use alpine/bombardier via vpn? `[question]`
**State:** CLOSED | **Author:** @ilwsm | **Created:** 2022-03-05 | **Updated:** 2022-03-31 | **Comments:** 4

> For example how use ?
> `docker run -ti --rm alpine/bombardier -c 1000 -d 3600s -l https://mil.ru`
> 
> like in https://github.com/Arriven/db1000n/blob/main/run.sh

<details><summary>Comments (4)</summary>

- **@iamtodor** (2022-03-05): @goodandrewsoft could you please expand your question? Basically, all you need is to turn on VPN and run `docker run ghcr.io/arriven/db1000n` or just run binaries. You don't need `alpine/bombardier`...
- **@ilwsm** (2022-03-05): I know that. I'm already use db1000n via [run.sh](https://github.com/Arriven/db1000n/blob/main/run.sh)  But, sometimes, i want use `alpine/bombardier` manually and i want automate my process like...
- **@arriven** (2022-03-05): I'll assign this to @bitshape as he's the author of that implementation and knows about it more than me.
- **@vgoncharenko** (2022-03-05): It's not detailed instruction, but you asked a question in the wrong repo. It's a different project from bombardier. So I have no knowledge about db1000n or bombardier, I'm just like you - a user,...
</details>

## #124 How to stop the program?
**State:** CLOSED | **Author:** @mzahar | **Created:** 2022-03-05 | **Updated:** 2022-03-05 | **Comments:** 3

> Is there a way to stop program? Or I need only uninstall it to stop?
> Device: Mac Book Pro Intel

<details><summary>Comments (3)</summary>

- **@iamtodor** (2022-03-05): @mzahar you run it as binary file?
- **@Devaniti** (2022-03-05): If you don't see terminal window with program then it's not running
- **@arriven** (2022-03-05): Anything that would work for a regular program would work here (I'm assuming you use binary install which is described in the instruction for users). If you see the terminal where the program is...
</details>

## #123 [improvement] [win] BAT file with supervisor/guardian
**State:** CLOSED | **Author:** @5har0varik | **Created:** 2022-03-05 | **Updated:** 2022-03-05 | **Comments:** 2

> To prevent windows crash add simple supervisor in .bat file. Add .bat file to .zip package. 
> For example:
> ```
> echo starting
> :start
> start /w db1000n.exe
> echo restarting
> goto start
> ```

<details><summary>Comments (2)</summary>

- **@5har0varik** (2022-03-05): I may create a PR, tell me what changes needed (Script location, doc changes, etc)
- **@arriven** (2022-03-05): @5har0varik PR would be nice, not sure about the location, I'd probably make the scripts/ subfolder for the script (and move install.sh there).   Also see...
</details>

## #121 Docker image is not being updated for 21 hours - new targets are not applied
**State:** CLOSED | **Author:** @synapse-unix | **Created:** 2022-03-05 | **Updated:** 2022-03-06 | **Comments:** 10

> Targets config in the separate repo is being updated multiple times, but actual Docker image (that is currently running on VMs) hits outdated targets list. Please push new image ASAP.
> 
> P.S.: I can develop CI stage to build and push new image, once MR is merged. Should I start?

<details><summary>Comments (10)</summary>

- **@arriven** (2022-03-05): Targets are configured outside of the image and executable (and repo because it's easier to manage that way). There is a backup config embedded into the exe but it's used as a backup if the app can't...
- **@arriven** (2022-03-05): If you see that docker image really hits outdated list I suggest checking if it can connect to the proper target list in your setup. Might be a problem there and we need to discuss/debug it...
- **@arriven** (2022-03-05): See https://github.com/Arriven/db1000n/issues/115 for more info on networking problems in clouds
- **@synapse-unix** (2022-03-05): Ok, thanks. Checking from inside Docker. Will post the results. Use tcpdump to check packets sending.
- **@synapse-unix** (2022-03-05): @Arriven can confirm, that targets are not being updated. We need to push an image each time we have a MR merged to https://github.com/db1000n-coordinators/LoadTestConfig to take a benefit of the...
- **@synapse-unix** (2022-03-05): @Arriven ok, I see where we get conf url and update it. Can you confirm, that this loop overrides targets config each time in the container? -...
- **@bitshape** (2022-03-05): @dmy3tka disagree because 1hr refresh means it will take up to an hour to get all clients refreshed. For successful results you want very quick switch of conf in order to maximize efficiency.
- **@synapse-unix** (2022-03-06): > @dmy3tka disagree because 1hr refresh means it will take up to an hour to get all clients refreshed. For successful results you want very quick switch of conf in order to maximize efficiency.  Do...
- **@arriven** (2022-03-06): github is a CDN, which is designed for this specific type of load we use it for (it can and should be able to handle A LOT more load than this). This is the core of an app and I was very careful when...
- **@synapse-unix** (2022-03-06): I am closing this issue, as I see targets was updated, with the new image
</details>

## #119 Announcement to contributors: Code restructure `[priority: critical]`
**State:** CLOSED | **Author:** @arriven | **Created:** 2022-03-05 | **Updated:** 2022-03-05 | **Comments:** 0

> Considering the amount of contributions I decided to spend an hour or two restructuring the code a bit to reduce chances of merge conflicts in the future. Please avoid doing any major work until I resolve this issue or make sure you will be able to re-apply your work after I commit the code...

## #118 Documentation structure `[documentation, help wanted, good first issue, priority: medium]`
**State:** CLOSED | **Author:** @arriven | **Created:** 2022-03-05 | **Updated:** 2022-03-10 | **Comments:** 18

> As new PRs come in the docs start to be a little chaotic. I think it's important to make the structure clearer to enable faster contributions.
> 
> I'm thinking about the following structure:
> 
> - README.md - general info about the repository, links to docs/new-users.md and docs/technical-users.md...

<details><summary>Comments (18)</summary>

- **@arriven** (2022-03-05): @iamtodor since you're probably the biggest contributor to the docs yet, could you take a look at this?
- **@iamtodor** (2022-03-05): @Arriven to be honest, I had literally the same assumption. The reason I didn't suggest it is I thought it would bring additional efforts
- **@arriven** (2022-03-05): Yeah, started with that opinion as well but seeing the amount of contributions changed my mind 😅
- **@iamtodor** (2022-03-05): would you like to move vpn list to a separate page from readme? but still having a link from readme
- **@Amet13** (2022-03-05): @iamtodor @Arriven I'll prepare a proof of concept of the structure of the new doc in 10-30 mins. Let's discuss it after I finish
- **@iamtodor** (2022-03-05): @Amet13 sounds good to me!
- **@arriven** (2022-03-05): VPN instructions can be a separate page, but probably also nice to include some options directly into the instructions for new users
- **@arriven** (2022-03-05): @Amet13 agreed
- **@Amet13** (2022-03-05): @Arriven @iamtodor let's review this one: https://github.com/Arriven/db1000n/pull/128/files
- **@Amet13** (2022-03-05): The idea is to keep the main readme pretty clean. There is also a duplicate of it in Ukrainian. Crosslinking between ua and en versions of README.  Tool-specific docs are in their directories...
- **@iamtodor** (2022-03-05): @Amet13 @Arriven I am not sure whether we need to keep Ukrainian instruction. I think all of us (I mean the IT community) know English at, at least pre-intermediate level. But keeping 2 separate...
- **@Amet13** (2022-03-05): @iamtodor agree, just moved it to not to break current docs. But if we write README just once, maybe it won't be a really big effort to keep both versions
- **@arriven** (2022-03-05): I think it's worth keeping the instruction for new users in Ukrainian, everything else can be English only. I'll merge PR from @Amet13 as is
- **@iamtodor** (2022-03-06): @Amet13 @Amet13 I would suggest having somewhere in docs (maybe for developers or it's up to your where to leave it) the following...
- **@Amet13** (2022-03-06): I think it could be forced by implementing [CODEOWNERS](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/about-code-owners)...
- **@iamtodor** (2022-03-07): CODEOWNERS functionality was implemented in https://github.com/Arriven/db1000n/pull/187
- **@iamtodor** (2022-03-07): @Arriven @Amet13 I think we can close this issue
- **@m-v-kalashnikov** (2022-03-08): @Arriven @Amet13 I can move all docs to MKdocs which would be hosted on GitHub pages
</details>

## #116 ARM and RaspberryPi support
**State:** CLOSED | **Author:** @vovagorodok | **Created:** 2022-03-05 | **Updated:** 2022-03-05 | **Comments:** 0

> For latest raspberry pi os:
> ```
> ~/db1000n $ docker run ghcr.io/arriven/db1000n
> Unable to find image 'ghcr.io/arriven/db1000n:latest' locally
> latest: Pulling from arriven/db1000n
> docker: no matching manifest for unknown in the manifest list entries.
> See 'docker run --help'.
> ```

## #115 DigitalOcean Networking disabled error
**State:** CLOSED | **Author:** @Leta0n | **Created:** 2022-03-04 | **Updated:** 2022-03-06 | **Comments:** 2

> Can I limit network usage somehow? DO keep banning my droplets because of network abuse
> ![IMG_FF722C95255B-1](https://user-images.githubusercontent.com/3305500/156847961-2f8709fc-4f1f-46e1-8e3b-d5fbf0cf61b6.jpeg)

<details><summary>Comments (2)</summary>

- **@arriven** (2022-03-05): You can use custom config for that (see ##Configuration part of the README for reference). I'm currently working with admins to try creating a separate config to use with cloud providers that would...
- **@Leta0n** (2022-03-06): Works great now, thanks!
</details>

## #111 Embedded VPN
**State:** CLOSED | **Author:** @ctukraine22 | **Created:** 2022-03-04 | **Updated:** 2022-03-05 | **Comments:** 2

> Народ, можливо варто додати вбудовану роботу через vpn?
> ось у мене є приклад на docker compose https://github.com/ctukraine22/runner
> суть в тому, що підіймається контейнер з vpn, і контейнер з db1000n, потім періодично vpn перепідключається.
> Щоб запустити достатньо тільки дати налаштування для...

<details><summary>Comments (2)</summary>

- **@arriven** (2022-03-04): Check out supervisord/ and run/ subfolders for that, feel free to open a PR if it can be further improved
- **@ctukraine22** (2022-03-05): бачу вже доку додали https://github.com/Arriven/db1000n/blob/main/docs/advanced-users-and-devs.md#docker--openvpn
</details>

## #110 Check if user enabled VPN and so whether attack will be effective
**State:** CLOSED | **Author:** @Devaniti | **Created:** 2022-03-04 | **Updated:** 2022-03-05 | **Comments:** 0

> If user's IP address detected as Ukrainian, open page in browser with instruction on how to setup VPN.
> Will try to do myself.

## #109 Some proxies in proxylist have port 8010 instead of 1080 `[invalid]`
**State:** CLOSED | **Author:** @constantin-ukr | **Created:** 2022-03-04 | **Updated:** 2022-03-31 | **Comments:** 2

> Into file proxylist.json
> 
> has Ip with port *8010* but general used *1080*.
> 
> "124.172.232.49:8010",
> "89.108.112.1:8010",
> etc.
> 
> Is it issue or correct?

<details><summary>Comments (2)</summary>

- **@arfgdev** (2022-03-05): could you describe a way to reproduce it?
- **@constantin-ukr** (2022-03-05): As I understand the target takes from the list "proxylist.json", and if open it and find the text ":8010" you can over 20 matches. I do not say that is incorrect but should check. Thanks
</details>

## #105 OOM issue 
**State:** CLOSED | **Author:** @kuzm1ch | **Created:** 2022-03-04 | **Updated:** 2022-03-31 | **Comments:** 1

> <img width="766" alt="Screenshot 2022-03-04 at 20 49 13" src="https://user-images.githubusercontent.com/32264674/156824221-c20172b9-4e72-4da1-89af-008f6ebed1ca.png">
> 
> ```
> $ docker ps -a
> CONTAINER ID   IMAGE                             COMMAND                  CREATED          STATUS            ...

<details><summary>Comments (1)</summary>

- **@arriven** (2022-03-04): ```bash $ docker ps -a CONTAINER ID   IMAGE                             COMMAND                  CREATED          STATUS                        PORTS     NAMES 12b8c086e5ec   12b8c086e5ec         ...
</details>

## #101 [infrastructure as a code]: DigitalOcean `[help wanted]`
**State:** CLOSED | **Author:** @iamtodor | **Created:** 2022-03-04 | **Updated:** 2022-03-05 | **Comments:** 5

> The same way we have it on GCP https://github.com/Arriven/db1000n/tree/main/terraform/gcp_expressvpn We need the infra for DigitalOcean droplets

<details><summary>Comments (5)</summary>

- **@arriven** (2022-03-04): There was an example committed by @o-volkov to another repo when back when I wanted to use multirepo approach for this. I think we should make a PR to move it here...
- **@arriven** (2022-03-04): Note that I've got several reports of DO banning droplets using this framework, will try to research if this is caused by a specific attack pattern or something else and if it can be easily solved
- **@iamtodor** (2022-03-04): @Arriven perhaps this article might be in use for you https://dou.ua/forums/topic/36874
- **@iamtodor** (2022-03-05): relates to https://github.com/Arriven/db1000n/issues/115
- **@Amet13** (2022-03-05): Implemented there: https://github.com/Arriven/db1000n/pull/142
</details>

## #100 [infrastructure as a code]: Azure `[help wanted, triage needed]`
**State:** CLOSED | **Author:** @iamtodor | **Created:** 2022-03-04 | **Updated:** 2022-03-07 | **Comments:** 11

> The same way we have it on GCP https://github.com/Arriven/db1000n/tree/main/terraform/gcp_expressvpn We need the infra for Azure virtual machines

<details><summary>Comments (11)</summary>

- **@Amet13** (2022-03-05): If someone have account on Azure I can help with writing terraform code and documentation for it
- **@crabulik** (2022-03-05): Hi folks. I have created a setup for Azure Container Instances with terraform.
- **@Amet13** (2022-03-05): Cool @crabulik could you make a PR?
- **@crabulik** (2022-03-05): I am not so good at working with GitHub. I created a branch and tried to push it, but received the message that I do not have Write access. Do I have to perform some additional configuration?
- **@Amet13** (2022-03-05): @crabulik you have to fork a repo, then clone your repo, create a branch, make changes, push to github and then create a PR to this repo. If you have any issues with that, just send files there and...
- **@crabulik** (2022-03-05): @Amet13 Thanks, created PR: https://github.com/Arriven/db1000n/pull/158
- **@Amet13** (2022-03-06): Seems like can close it
- **@iamtodor** (2022-03-06): @Amet13 @crabulik @Arriven shall we follow this agreement https://github.com/Arriven/db1000n/issues/146#issuecomment-1059794244 ? Can we do cross-check if the infra works from the scratch?
- **@Amet13** (2022-03-06): It would be great to do a check, but without access to the cloud, it's impossible. For those changes related to terraform we could ask for `terraform plan` output to review changes at least
- **@iamtodor** (2022-03-06): @Amet13 yeah, I suppose we need to have the individual account
- **@arriven** (2022-03-07): I've created a "triage needed" label for those types of PRs to mark that we need someone other than author to check that the change is working. I'll add that label here just so that you could find it...
</details>

## #99 [infrastructure as a code]: AWS
**State:** CLOSED | **Author:** @iamtodor | **Created:** 2022-03-04 | **Updated:** 2022-03-04 | **Comments:** 1

> The same way we have it on GCP https://github.com/Arriven/db1000n/tree/main/terraform/gcp_expressvpn We need the infra for AWS EC2 instances

<details><summary>Comments (1)</summary>

- **@arriven** (2022-03-04): Should be fixed by https://github.com/Arriven/db1000n/commit/2d5a4bab050d9d366182282a4b6f10986c227570
</details>

## #96 Is there a benefit to running the program around the clock? 
**State:** CLOSED | **Author:** @TarasKasprik | **Created:** 2022-03-04 | **Updated:** 2022-03-04 | **Comments:** 1

> Is there a benefit to running the program around the clock? 
> Do you need to run it only after receiving a command from the coordinators? 
> 
> Different sources have different information on this issue.

<details><summary>Comments (1)</summary>

- **@arriven** (2022-03-04): You can safely run this app around the clock. You can assume it restarts itself every minute and gets new targets  Restarts is an approximation, in reality it's a bit smarter than that but I won't...
</details>

## #89 install.sh failed on arm architecture
**State:** CLOSED | **Author:** @Bleach665 | **Created:** 2022-03-04 | **Updated:** 2022-03-10 | **Comments:** 6

> Reproduced on Oracle cloud ampere instance.
> 
> `sudo ./install.sh`
> failed with error 
> `unknown: aarch64`.
> 
> `uname -a` output
> `Linux arm 5.11.0-1028-oracle #31~20.04.1-Ubuntu SMP Wed Jan 26 14:20:52 UTC 2022 aarch64 aarch64 aarch64 GNU/Linux`
> 
> `echo $OSTYPE` output
> `linux-gnu`
> 
> `echo...

<details><summary>Comments (6)</summary>

- **@arriven** (2022-03-04): ah, right, I forgot I take `$OSARCH` from uname -m taking a look
- **@arriven** (2022-03-04): while I was looking @securims proposed a PR #98 which as far as I can tell will allow you to install the app with something like `OSARCH=arm ./install.sh`
- **@arriven** (2022-03-04): @Bleach665 if the command from my previous comment works for you - I can probably safely assume that simply specifying `aarch64` to download arm64 binary would be a proper fix. Please respond once...
- **@Bleach665** (2022-03-04): @Arriven . Specifying `OSARCH` as `arm` or `aarch64` dont resolve this.
- **@arriven** (2022-03-04): Ok, hopefully I'll be able to find time to setup a test machine to debug this tomorrow
- **@Kirill-Karmazin** (2022-03-05): The `instal.sh` is basically a lazy way to select the proper archive with the program for your computer on this page: https://github.com/Arriven/db1000n/releases   If you're running `sh` and...
</details>

## #85 dynamic targets list `[enhancement, help wanted]`
**State:** CLOSED | **Author:** @Yneth | **Created:** 2022-03-04 | **Updated:** 2022-03-31 | **Comments:** 2

> I have created an API for targets, currently it has info on cloudflare, UP/DOWN, ips and other stuff.
> I am planning to add open ports info and add sorting based on popularity.
> 
> If you'd like I can share an access with you.
> 
> You can check it out here:
> http://164.92.247.88:9300/

<details><summary>Comments (2)</summary>

- **@arriven** (2022-03-04): Can you get in touch with @Andrmist ? He volunteered to write an automated config generator which would be used by admins and I think it would be best to integrate an option to fetch list of targets...
- **@arriven** (2022-03-04): See #78 for reference
</details>

## #82 The app doesn't seem to generate any traffic, please contact your admin
**State:** CLOSED | **Author:** @QDanteQ | **Created:** 2022-03-04 | **Updated:** 2022-03-04 | **Comments:** 1

> WARN]  2022/03/04 12:49:51 [WARN] The app doesn't seem to generate any traffic, please contact your admin
> [ERROR] 2022/03/04 12:49:51 github.com/Arriven/db1000n/logs.Logger.Error:logs.go:50 [ERROR] error sending packet: listen ip4:tcp 0.0.0.0: socket: operation not permitted
> [ERROR] 2022/03/04...

<details><summary>Comments (1)</summary>

- **@arriven** (2022-03-04): There was a small misconfiguration by the new admin, it was fixed within 10 minutes (see https://github.com/db1000n-coordinators/LoadTestConfig/commit/831f3fcaeed704aa294a5d12e1295e09389eb5c1)
</details>

## #79 if you do not have time to update the hosts, who will then take my PR? `[question]`
**State:** CLOSED | **Author:** @KhalupiakYaroslav | **Created:** 2022-03-04 | **Updated:** 2022-03-31 | **Comments:** 2

<details><summary>Comments (2)</summary>

- **@arriven** (2022-03-04): The problem right now is that I don't have enough time near my laptop to do that. I'm currently organizing admins to take care of the config but regardless of that if you author a PR I can review and...
- **@KhalupiakYaroslav** (2022-03-04): дякую! тримайся друже, ви мега круті
</details>

## #78 Write config generator so simplify management `[enhancement, help wanted]`
**State:** CLOSED | **Author:** @Andrmist | **Created:** 2022-03-04 | **Updated:** 2022-03-31 | **Comments:** 5

> Доброго дня! Хочу запропонувати написати (готовий це зробити сам) авто генератор конфігу, потрібні сайти будуть братись з телеграму або діскорду.

<details><summary>Comments (5)</summary>

- **@arriven** (2022-03-04): That's a very good idea! You can check defaultconfig.go for an example of a simple but quite effective config (feel free to improve on that as well)
- **@arriven** (2022-03-04): I'll assign the issue to you and hope you don't mind me changing the title to english
- **@Yneth** (2022-03-04): @Andrmist  Hi, according to https://github.com/Arriven/db1000n/issues/85 I have already developed and continue updating the API for targets, it would be nice to cooperate.
- **@Andrmist** (2022-03-06): https://github.com/Andrmist/db1000n_target_generator
- **@securims** (2022-03-19): I've written a small helm chart to save myself from copy-pasting simple jobs over and over, feel free to use it to save some time - https://github.com/securims/db1000n-config-generator
</details>

## #77 Хто координує дії?? 
**State:** CLOSED | **Author:** @KhalupiakYaroslav | **Created:** 2022-03-04 | **Updated:** 2022-03-04 | **Comments:** 1

> Отримав посилання на image від кібер козаків, але хости які атакує скрипт не співпадають з тим що вони пишуть у себе в групі

<details><summary>Comments (1)</summary>

- **@arriven** (2022-03-04): Yeah, we're still organizing the process with admins (we need to set up a training but human interactions take time especially since most of us are in Ukraine and have to regularly run to shelter)....
</details>

## #75  ERRO[0174] error waiting for container: EOF 
**State:** CLOSED | **Author:** @mvkorobkov | **Created:** 2022-03-04 | **Updated:** 2022-03-04 | **Comments:** 3

> останавливается по ошибке
> добавьте докеркомпоз с авторестартом и заодно многопоточностью

<details><summary>Comments (3)</summary>

- **@mvkorobkov** (2022-03-04): docker-compose.yml:  version: '3' services:   d1:     image: ghcr.io/arriven/db1000n:latest     restart: always  ----- docker-compose up --scale d1=5
- **@mvkorobkov** (2022-03-04): похоже падает сам докер, нужно другое решение
- **@arriven** (2022-03-04): Feel free to make a pull request with that docker compose or use an executable directly on your system. You can check #54 for the most common issue with docker/cloud and check for workarounds...
</details>

## #73 .
**State:** CLOSED | **Author:** @vinnik-dmitry07 | **Created:** 2022-03-03 | **Updated:** 2022-03-04 | **Comments:** 1

<details><summary>Comments (1)</summary>

- **@arriven** (2022-03-04): There are more effecient jobs in this program that do that task more effeciently (See #57 for some explanations on the topic). Also it seems like @securims just authored a PR (#76) that allows to use...
</details>

## #72 Panic 
**State:** CLOSED | **Author:** @izac1 | **Created:** 2022-03-03 | **Updated:** 2022-03-04 | **Comments:** 1

> ```2022/03/03 21:59:31 178.248.236.218 is already an IP address, skipping DNS resolution
> 2022/03/03 21:59:31 178.248.236.218 is already an IP address, skipping DNS resolution
> ^M^M^M⠋ Flood is in progress, target=178.248.236.218:80, floodType=random, payloadLength=1000 (348 kB, 3.397 MB/s) ^M^M^M⠙...

<details><summary>Comments (1)</summary>

- **@arriven** (2022-03-04): The stack looks like crash due to OOM - it lacks RAM to parse the config and attack all the targets it's configured to. Check #54 for possible workarounds and more info
</details>

## #69 Update Google Doc with latest versions
**State:** CLOSED | **Author:** @bunge12 | **Created:** 2022-03-03 | **Updated:** 2022-03-04 | **Comments:** 3

> I can volunteer to keep updated :)

<details><summary>Comments (3)</summary>

- **@arriven** (2022-03-03): I'll poke guys who manage it and suggest them your help
- **@iamtodor** (2022-03-04): @Arriven once you merge #88 PR this issue won't be relevant
- **@iamtodor** (2022-03-04): the issue can be closed as PR has been merged @bunge12 @Arriven
</details>

## #67 Docker image won't run on arm64 devices `[bug, enhancement]`
**State:** CLOSED | **Author:** @Wirtos | **Created:** 2022-03-03 | **Updated:** 2022-03-04 | **Comments:** 9

> `WARNING: The requested image's platform (linux/amd64) does not match the detected host platform (linux/arm64/v8) and no specific platform was requested`
> Probably should be universal single-image-fits-all for easier scaling?

<details><summary>Comments (9)</summary>

- **@arriven** (2022-03-03): Yup, need to take a look into it
- **@arriven** (2022-03-03): I anyone already knows how to do it - feel free to contribute
- **@Bleach665** (2022-03-03): Also pls fix this for ````install.sh````.
- **@securims** (2022-03-04): this is just a warning and it should be working still, if it bothers you run the command with the additional flag `docker run --platform linux/amd64 --pull always ghcr.io/arriven/db1000n:latest`
- **@arriven** (2022-03-04): The issue was fixed in #80 and also there was a fix for install.sh in #81  Thanks authors of those requests for help!
- **@Bleach665** (2022-03-04): @Arriven  > and also there was a fix for install.sh in https://github.com/Arriven/db1000n/pull/81  Unfortunately not.   ````sudo ./install.sh````  failed with error  ````unknown: aarch64````.
- **@arriven** (2022-03-04): @Bleach665 hmm, seems like it can't detect your platform properly, which system are you running it on? Also can you try without sudo?
- **@Bleach665** (2022-03-04): @Arriven . Oracle cloud arm instance. ````Linux arm 5.11.0-1028-oracle #31~20.04.1-Ubuntu SMP Wed Jan 26 14:20:52 UTC 2022 aarch64 aarch64 aarch64 GNU/Linux````  Without `sudo` the result is same.
- **@arriven** (2022-03-04): Ah, okay, I see, can you open a new issue and provide the value of your OSARCH and OSTYPE variables?
</details>

## #63 Docker stopped after several seconds  `[bug, duplicate]`
**State:** CLOSED | **Author:** @b0nn1e | **Created:** 2022-03-03 | **Updated:** 2022-03-03 | **Comments:** 1

> Hi!
> 
> After several second docker has been stopped. Log below
> 
> ```
> root@vds2140872:~# docker run ghcr.io/arriven/db1000n:latest
> 2022/03/03 16:56:31 178.248.236.218 is already an IP address, skipping DNS resolution
> 2022/03/03 16:56:31 178.248.236.218 is already an IP address, skipping DNS...

<details><summary>Comments (1)</summary>

- **@arriven** (2022-03-03): How much RAM is allocated to docker? See #54 as it seems to have pretty similar symptoms. If it turns out to be something else and increasing the allocated RAM doesn't fix the issue feel free to...
</details>

## #62 fetching json config: unexpected end of JSON input
**State:** CLOSED | **Author:** @Firefret | **Created:** 2022-03-03 | **Updated:** 2022-03-03 | **Comments:** 1

> Title

<details><summary>Comments (1)</summary>

- **@arriven** (2022-03-03): I don't remember if it was a warning or an error. I think it was a warning and thus not critical to the performance of the tool. Anyway the latest release (v0.5.9) already has this fixed and further...
</details>

## #58 Only seems to attack 3 IPs `[bug]`
**State:** CLOSED | **Author:** @WeGoToMars | **Created:** 2022-03-03 | **Updated:** 2022-03-04 | **Comments:** 10

> With -i 0 flag on launch, the only IPs visible in the log are
> `[DEBUG] 194.54.14.187:53 started at XYZ`
> `[DEBUG] 194.54.14.186:53 started at XYZ`
> `[DEBUG] 194.67.2.109:53 started at XYZ`
> No other targets are visible
> 
> Sometimes there are fail messages like 
> `[DEBUG] GET...

<details><summary>Comments (10)</summary>

- **@alextatarinov** (2022-03-03): Similar issue - targets only one IP ![image](https://user-images.githubusercontent.com/17722304/156619264-56fcb8a1-48d6-42e3-84a6-4e587dcd0f4f.png)
- **@arthur2406** (2022-03-03): > Similar issue - targets only one IP ![image](https://user-images.githubusercontent.com/17722304/156619264-56fcb8a1-48d6-42e3-84a6-4e587dcd0f4f.png)  The same issue
- **@bunge12** (2022-03-03): My output looks different, but I can also see only one IP (`178.248.236.218`)  ![image](https://user-images.githubusercontent.com/54365622/156629706-c2584b85-9ae7-4f05-8519-f0ad9218b646.png)
- **@arriven** (2022-03-03): @alextatarinov @arthur2406 @bunge12 you're using a mode that only shows important logs, the IP there is from one of the experimental jobs that doesn't respect that (and there's already a bit more...
- **@WeGoToMars** (2022-03-03): @Arriven downloaded latest build for amd64, running on win11 here is a piece of the log I'm seeing https://pastebin.com/raKTKG8n, it's not a full minute because pastebin has limit for free users,...
- **@su-hs** (2022-03-03): My results:   `docker run --rm -it ghcr.io/arriven/db1000n:latest`    <img width="1479" alt="Screenshot 2022-03-03 at 20 43 07"...
- **@arriven** (2022-03-03): @WeGoToMars the log you provided this time also doesn't seem to include debug logs :) The main reason network usage drifts up and down here is that the job outputting it's IP doesn't contribute to...
- **@WeGoToMars** (2022-03-03): @Arriven `-c https://blah` completely fixed the issue for me, it now works on multiple IPs and shows logs correctly. Thanks!
- **@arriven** (2022-03-04): @WeGoToMars cool, but please check https://github.com/db1000n-coordinators/LoadTestConfig and remove that commandline argument as soon as activity starts there to keep being up to date with current...
- **@WeGoToMars** (2022-03-04): @Arriven `db1000n.exe -c https://github.com/db1000n-coordinators/LoadTestConfig/blob/main/config.json` seems to work now  Without any arguments, the logging works differently(?)  db1000n.exe -c...
</details>

## #57 Question: How this program works? `[question]`
**State:** CLOSED | **Author:** @antl31 | **Created:** 2022-03-03 | **Updated:** 2022-03-03 | **Comments:** 1

> Hello dear Author. I have tested your program wth custom config on my default apache server. Config has type: http , get method. 
> Also i have tested other tools, https://github.com/codesenberg/bombardier and https://github.com/MHProDev/MHDDoS 
> So you can see that bombarier has a lot of RPC...

<details><summary>Comments (1)</summary>

- **@arriven** (2022-03-03): So there are couple things I'd like to note here:  - This tool supports not only HTTP/HTTPS requests but also TCP/UDP/IP flood configurable enough to support more complex attack patterns like syn...
</details>

## #55 Security issue because of public repo `[wontfix]`
**State:** CLOSED | **Author:** @makbar1234 | **Created:** 2022-03-03 | **Updated:** 2022-03-31 | **Comments:** 5

> Росіяни чи про-російськи можуть взяти ваш код, підправити шлях до конфігу - і досити українські ресурси!
> 
> сховайте код, не робіть роботу за окупанта
> роздавайте докер імідж і то краще б якось обережно імідж робити, щоб код не взяли звідти

<details><summary>Comments (5)</summary>

- **@Zip753** (2022-03-03): з одного боку так, але з іншого боку і так чат в телеграмі відкритий, тож великої секретності ми не заховаємо в будь якому випадку
- **@arriven** (2022-03-03): In theory yes, in reality it is a question of organization and resources and for now the pros of having open source approach (trust of users and collaboration: I think around 10% of the work here is...
- **@kuzm1ch** (2022-03-03): completely agree to have it opensource. At list people should be aware what they are running on their machines.
- **@makbar1234** (2022-03-04): people in channel are still coordinating and running soft manually. they are confused that this repo is not synched with the targets admins set. So, the pros are not working because of...
- **@arriven** (2022-03-04): @makbar1234 the process of finding and training admins to use this took some time because of war in the country and regular need for both me and admins to run to the shelter due to air hazards. First...
</details>

## #54 Unusable on cloud servers (OOM) `[bug]`
**State:** CLOSED | **Author:** @mik9 | **Created:** 2022-03-03 | **Updated:** 2022-03-31 | **Comments:** 7

> Eats 1Gb RAM in few seconds and hangs machine.
> Tried running docker image on Linux.

<details><summary>Comments (7)</summary>

- **@MaxGenash** (2022-03-03): The same for me: ``` 2022/03/03 14:35:55 178.248.236.218 is already an IP address, skipping DNS resolution 2022/03/03 14:35:55 178.248.236.218 is already an IP address, skipping DNS...
- **@artemkomyshan** (2022-03-03): Same for me with the manual build and run.
- **@jdoe7865623** (2022-03-03): Works on machines with 2GB RAM. At 1GB indeed gets killed on OOM. Until this is fixed, stick to 2 GB machines.
- **@arriven** (2022-03-03): Considering that there are workarounds I'll set a low priority to this issue for now. If you want to help with debugging this you can consider creating custom configs that only use single job and see...
- **@b0nn1e** (2022-03-03): What is the best VPS configuration for this docker image?
- **@b0nn1e** (2022-03-03): Works good with 3 CPU 4 GB RAM
- **@iffixit** (2022-03-10): >   use container instances instead
</details>

## #49 Add DNS protocol support to packetgen jobs `[enhancement]`
**State:** CLOSED | **Author:** @arriven | **Created:** 2022-03-02 | **Updated:** 2022-03-31 | **Comments:** 2

> see https://pkg.go.dev/github.com/google/gopacket/layers#DNS for reference

<details><summary>Comments (2)</summary>

- **@alexdanger** (2022-03-18): @Arriven is still relevant? if yes, could add a bit more details, thanks.
- **@arriven** (2022-03-18): @alexdanger yes, it's still relevant in terms of packetgen. That module is intended to be able to generate any kind of network packets based on the configuration and it would be good to add support...
</details>

## #47 Crash on DigitalOcean droplet `[bug]`
**State:** CLOSED | **Author:** @AndriiNytsyk | **Created:** 2022-03-02 | **Updated:** 2022-03-02 | **Comments:** 8

> Tool crashes on DigitalOcean droplet (Shared CPU, 2 vCPUs, 4 GB, 25 GB, 4 TB). Startup method: docker install.
> 
> goroutine 44381 [running]:
> math/rand.(*Rand).Intn(0x80acea, 0x46817b)
>         /usr/local/go/src/math/rand/rand.go:168 +0x65
> math/rand.Intn(...)
>        ...

<details><summary>Comments (8)</summary>

- **@arriven** (2022-03-02): @AndriiNytsyk Can you send the config you are using in case it's not default?
- **@AndriiNytsyk** (2022-03-02): I use default configuration according to instruction "docker install".
- **@scamp** (2022-03-02): Please add swapfile:  dd if=/dev/zero of=/swapfile bs=1M count=1024  mkswap /swapfile  chmod 600 /swapfile  swapon /swapfile
- **@AndriiNytsyk** (2022-03-02): I've checked proposed solution but it didn't help. Swap size range I used: 600 MB - 8 GB  panic: invalid argument to Intn                                                                            ...
- **@arriven** (2022-03-02): ok, I guess I know what's happening, I didn't consider the case when proxylist is a valid json but has no proxy entries in it, should be easy to fix
- **@arriven** (2022-03-02): @AndriiNytsyk check v0.5.8, although it shouldn't have been crashing since some earlier release (checking which one rn)
- **@arriven** (2022-03-02): ^ Since https://github.com/Arriven/db1000n/releases/tag/v0.5.2
- **@AndriiNytsyk** (2022-03-02): Fixed on v0.5.8. Thanks!
</details>

## #34 Add ability to configurate http/socks proxies via config for each attack `[enhancement]`
**State:** CLOSED | **Author:** @arriven | **Created:** 2022-03-01 | **Updated:** 2022-03-31 | **Comments:** 0

## #28 Document config `[documentation, good first issue]`
**State:** CLOSED | **Author:** @arriven | **Created:** 2022-02-28 | **Updated:** 2022-03-02 | **Comments:** 1

> Write understandable documentation for the config so that people could use their own setup when deploying to clusters

<details><summary>Comments (1)</summary>

- **@arriven** (2022-03-02): Done
</details>

## #22 bash and power-shell script of ease of installation
**State:** CLOSED | **Author:** @zmitry | **Created:** 2022-02-27 | **Updated:** 2022-02-28 | **Comments:** 0

> We need script similar to brew and other single line install scripts which will install appropriative binary/os and run the code. 
> 
> ```
> /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
> ```

## #19 Gather list of free vpns and best vpn locations to use(ideally russian) `[documentation, good first issue]`
**State:** CLOSED | **Author:** @zmitry | **Created:** 2022-02-27 | **Updated:** 2022-03-07 | **Comments:** 8

> ideally it would be good to spin up russian vpn for attacks

<details><summary>Comments (8)</summary>

- **@zmitry** (2022-02-27): tunnel bear gives 10gb of traffic for free https://www.tunnelbear.com/   swiss and Bulgaria seems to work fine for russia.
- **@sanohin** (2022-02-27): Free with a promocode https://my.clearvpn.com/promo/redeem?code=SAVEUKRAINE
- **@maxkoshevoi** (2022-02-28): [UrbanVPN](https://www.urban-vpn.com/) is also a possible candidate. It worked well before, needs validation if it works now
- **@quiberr** (2022-03-03): windscribe 15gb via confirm tempmail
- **@horodchukanton** (2022-03-03): windscribe 30gb with promo ПИЗДЕЦ
- **@iamtodor** (2022-03-04): @Arriven please close the issue as it was implemented in https://github.com/Arriven/db1000n/pull/94
- **@iamtodor** (2022-03-04): update: was re-implemented in https://github.com/Arriven/db1000n/pull/104 @Arriven
- **@iamtodor** (2022-03-06): @zmitry @Arriven @Amet13 please close this issue
</details>

## #18 better list of resources to attack. `[documentation, good first issue]`
**State:** CLOSED | **Author:** @zmitry | **Created:** 2022-02-27 | **Updated:** 2022-03-31 | **Comments:** 2

> gather list from different places https://t.me/itarmyofukraine2022.

<details><summary>Comments (2)</summary>

- **@arriven** (2022-02-27): You can also go ahead and add those targets through a PR here https://github.com/db1000n-coordinators/LoadTestConfig
- **@sanohin** (2022-02-28): `https://api.mosgorpass.ru/v8.2/stop` - query all bus stops `https://api.mosgorpass.ru/v8.2/stop/{{ stop_id }}` - `stop_id` from the list from the prev endpoint
</details>

## #16 httpstorm
**State:** CLOSED | **Author:** @arriven | **Created:** 2022-02-27 | **Updated:** 2022-03-03 | **Comments:** 0

## #15 slowloris
**State:** CLOSED | **Author:** @arriven | **Created:** 2022-02-27 | **Updated:** 2022-03-03 | **Comments:** 2

> integrate https://github.com/valyala/goloris

<details><summary>Comments (2)</summary>

- **@zmitry** (2022-02-27): will take it
- **@zmitry** (2022-02-27): https://github.com/Arriven/db1000n/pull/21
</details>

## #12 (improve metrics) track traffic generated by protocol headers and utility messages not exposed to go runtime
**State:** CLOSED | **Author:** @arriven | **Created:** 2022-02-27 | **Updated:** 2022-03-22 | **Comments:** 0

## #9 Improve logging `[enhancement, help wanted, good first issue]`
**State:** CLOSED | **Author:** @arriven | **Created:** 2022-02-27 | **Updated:** 2022-02-27 | **Comments:** 2

> Logs are formatted pretty poorly right now. Ideally we want to have an ability to write logs to different log levels (debug, info, warning, error, etc.) with better formatting.
> After that we'd also need a cmdline option to set minimal logging level with everything below turning into noop to not...

<details><summary>Comments (2)</summary>

- **@arriven** (2022-02-27): Still need to implement disabling particular log levels
- **@arriven** (2022-02-27): Implemented in https://github.com/Arriven/db1000n/commit/7728c69990055eaacd903501c17f60a04bb55511
</details>

## #8 DNS stress
**State:** CLOSED | **Author:** @arriven | **Created:** 2022-02-27 | **Updated:** 2022-03-09 | **Comments:** 4

> - could integrate https://github.com/MickaelBergem/dnsstresss/blob/master/dnsstresss.go

<details><summary>Comments (4)</summary>

- **@lonli078** (2022-02-27): I will do it
- **@arfgdev** (2022-03-05): @lonli078 how is it going? do you need any help?
- **@AndriiChuzhynov** (2022-03-05): working on it
- **@AndriiChuzhynov** (2022-03-07): I think this can be closed
</details>

## #7 Implement or integrate more sophisticated attack patterns `[documentation, enhancement]`
**State:** CLOSED | **Author:** @arriven | **Created:** 2022-02-27 | **Updated:** 2022-03-31 | **Comments:** 2

> syn-flood already integrated from https://github.com/bilalcaliskan/syn-flood
> 
> Use this commit as an example for integrations https://github.com/Arriven/db1000n/commit/9470ea16033a140cd130b722a7693d896988b9ac
> 
> List of potential options:
> 
> - [x] #8
> - [x] #15
> - [x] #16

<details><summary>Comments (2)</summary>

- **@arriven** (2022-02-27): Feel free to add more options with technical info, I'll be creating sub-tasks
- **@o-volkov** (2022-02-27): slowloris - https://github.com/valyala/goloris
</details>

## #6 Integrate write hooks to metrics storage into actual worker code
**State:** CLOSED | **Author:** @arriven | **Created:** 2022-02-27 | **Updated:** 2022-02-27 | **Comments:** 1

<details><summary>Comments (1)</summary>

- **@arriven** (2022-02-27): Integrated basic implementation, need to improve and all the protocol info not directly exposed to go
</details>

## #5 Implement background thread to read and output these metrics into logs on regular interval
**State:** CLOSED | **Author:** @arriven | **Created:** 2022-02-27 | **Updated:** 2022-02-27 | **Comments:** 0

## #4 Define and implement global metrics storage with thread-safe read-write operations to be used by other parts
**State:** CLOSED | **Author:** @arriven | **Created:** 2022-02-27 | **Updated:** 2022-02-27 | **Comments:** 1

<details><summary>Comments (1)</summary>

- **@arriven** (2022-02-27): Implemented in https://github.com/Arriven/db1000n/commit/c2186cf9cfdb9b1a5c0ca1affab6773bc0857736
</details>

## #2 Metrics `[enhancement]`
**State:** CLOSED | **Author:** @arriven | **Created:** 2022-02-27 | **Updated:** 2022-03-31 | **Comments:** 3

> It'd be good to have more informative indicators on the tool progress.
> Potential metrics:
> - Amount of traffic sent per job/job type/overall
> - Statuses of targets (at least http)
> - CPU/RAM/Network usage
> The most important metric would be the overall amount of traffic.
> To avoid impact on...

<details><summary>Comments (3)</summary>

- **@arriven** (2022-02-27): This is needed in order for coordinators to understand how many resources they have to better choose attack targets according to that
- **@kurlyk-dev** (2022-03-14): We have a big farm of instances on AWS but it's really difficult to understand the efficiency of this staff without metrics.
- **@arriven** (2022-03-14): @kurlyk-dev you can enable Prometheus via the commandline, it's not a lot but could be useful for your use case
</details>

## #1 Add build job for every PR and push to main `[enhancement]`
**State:** CLOSED | **Author:** @arriven | **Created:** 2022-02-26 | **Updated:** 2022-02-27 | **Comments:** 2

> Sometimes I edit the code directly through the web interface and that may lead to stupid mistakes :)

<details><summary>Comments (2)</summary>

- **@Brukkil** (2022-02-27): Do you need help with it?
- **@arriven** (2022-02-27): @Brukkil Sorry, didn't notice it before implementing and it's already done. Poke me if you want to help and be added to the slack channel I've recently created to organize cooperation
</details>