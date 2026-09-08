Wil: 借用你们的import, 改了URL 是否可以做到这件事呢?理论上是可以的 但是至于你说,如果是这样的话,我怎样知道哪些是应该由 哪里去拿呢?我觉得是等商业去谈了先 因为我们商业还没谈这件事 我理解的就是,简单点说就是 暂时在我们的配置下,在恒生的配置下 因为那些file都放在KMS 所以那个URL是不能发送给我们的客户 OK,除非 我们要做某一些另外的 additional的mapping 例如说在KMS里面的metadata 里面加册某些东西 这个是Aware的 但是现在,Day 1 at the moment,我想先谈清楚 究竟如果Assume 所有CIO的data是从KMS的情况下 那个integration应该怎样做? 这个我没ok

Alvina: OK

Wil: 是的 我也是那句,Aware会没有发送给客户的能力 但是 那件事要跟商业合作,我们才可以知道究竟是 应该怎样 而我assume的就是如果真的做Raspberping,就借用你们的importer去再用 所以我想先处理了 那些file先,情况就是你当KMS的file是和你们的conference的data是一样 你们叫API去拿conference的raw file 同样地,你可以去拿到KMS的raw file 只不过我在想,回到刚才一开始说的那件事 给了raw file给你们,你们在那边做passing 本身我们也pass了一段的file 会不会就是两边各自都做一次passing 还是说我们直接给了pass的content给你们 然后你们去做 我就想看看你们的意见,其实两边都ok啊 其实不是很好,我不知道你们pass了的东西是什么 还有那个tracking method是我们那边去做的,还是你们那边 不要说你们那边,我们那边,是在哪个system里面做 我想看看你们那边的意见 given现在 KMS的情况是这样的话

Alvina: 但是你们pass还是pass 字用来的,还是怎样

Wil: 我们现在就只是pass了文字而已 没有说我用AI再把image给一个description,然后再做下去 没有做这件事

Alvina: 因为我听闻,我们在latest那些是要

Wil: 要digest image 你说的是听闻你们的意思是指

Alvina: 我们现在有些document有个graph PDF是不是有一张很漂亮的 我知道,我们会拆掉的

Wil: 等一下,你们要 拆掉的,是在说requirement到哪里

Alvina: 是,是wealth的requirement

Wil: wealth的requirement,明白

Alvina: 要拆掉,看2025年多少钱 但是你们的做法是什么,是经document studio

Wil: document intelligence document studio,还是你们直接自己 两个东西来的 gooer那个 document studio 是啊 因为他保养了,然后就用他们那个 不知道什么鬼的名字,我不知道他们改了什么鬼的名字 总之就是他们是用AI来describe所有的图 然后再把那些图变回RAG的context

Daniel: 再put回去

Wil: 但是你们有没有试过准确度

Kyle: OK的,我们转用了document intelligence去check data

Alvina: 图那边是ok的

Wil: 我们图的都是

Alvina: graph,当然不是很固定

Wil: 明白 听起来是这样的话,似乎你直接拿kms的raw file好一点 我觉得是,因为我怕我们两边的requirement不是很 不同 一来呢

Alvina: 二来就是似乎,如果你在说在wealth里面可能会有一些interpretation

Wil: 因为可能在kms里面,如果把kms里面的RAG的一个passing 强行放在你们那里,好像又会影响到那件事 那impact impact就是 我们会有一个double 的cause 因为在kms里面pass了一转,可能在wealth intelligence里面pass另外一转 但是如果我们给个raw file来的话,就有一个好处就是保留了在wealth里面的 世界specific的一个 passing process,可以standardize,无论是amh还是恒生 都是enjoy同一个wealth的passing process 明白 我想问现在我们有没有一个API可以拿到一个比如说daily的delta list 或者我假设,我想象的一件事是 每一天 either我用push或者pool的方法 我都要知道,identify到,比如说我们在CIO里面这个domain里面 今天的changes document是什么 有没有这个能力? 我的理解应该有的 最简单就是你可以想象 平时的process就是 我们的business 会定期update那些document上去的 根据我的理解就是business曾经有说过,他们很少甚至乎 不会 去改动一些已经upload了的document,因为suppose那些document已经出了街了 就算如果出了街的话,他们最终就找另一份新的 文件去盖的,所以我们不会存在就是说 我有些所谓的edit 或者delete的case的 我只会是newly add的case 我可以想象就是 我有些东西上去KMS里面 然后KMS是需要告诉 或者是 无论是KMSpush过去Wealth Intelligence,或者是Wealth Intelligence走过来pool 我们都需要知道 我set了daily一转 我就 shortcut n-1的就fully,你只是给n-1的 这样就避免了duplicate,因为如果不是的话我还需要去check那个duplication 我是不是拿了等等那个东西嘛 which is not make sense 那就是说 有没有一个能力就是说,我time base就是说我这一段时间 拿modify 不要拿create,拿modify,因为 given真的会有modify的时候 我都可以cater到嘛,如果是这样的话 有没有一个这样的能力 或者如果没有的话,我们就可能要build这个能力出来 因为我们拿了条list suppose那条list就可以reuse我们get document的那个url KMS现在是support both s2b和ib2b的嘛 因为如果这个是一个batch的action,我们就用ib2b就不可以用s2b了

Alvina: 你们的document有没有entitlement 某一个人才 某一个staff id才可以看到

Wil: 我们现在是group level的 应该是 我们set的所谓domain level就是说 我们在那个 你可以想象就是有一个 grouping virtual的,logical的 对了 local的就是说我这个local的 给到什么adgroup的人去access 这样 如果是CIO的document 其实suppose 就是我们要和business那边去align 这一堆东西我们会这样推过去wealthy intelligence 这堆东西是不是public的,是不是internal的 那就不应该是说只是一某部分的人看,因为我们不是pp所以没那么sensitive 我觉得应该这件事是会这样align 就是要拿这个alignment的

Alvina: 还有你们那个 delta list 是不是可以放document type的 我就是要cio view而已 CIO view是一个document type

Wil: 你们整个KMS有很多document suppose的就是我们在说我们CIO的 CIO给的upload上去的document就放在一个domain里面 如果你说除非这个东西可能我们要carefire的就是如果他们那个CIO upload的document除了CIO inside 另外做一些东西其实不需要放进去的话 我想可以在我们的category里面可以做到这件事 就是说简单点说就是如果我们那个delta的事情就要传统好像filebase这样 我可以base by一个time given的time after这个时间里面再做filtering 这个我想可能就要和我那边的business去夹 但是相对地你们就可以说我call你这个API我就拿得到 比如说n-1这段时间 或者n-2这段时间的那个date里面的一个file list 然后你们就逐个逐个去拿 那就变成在你们那边去骂一件事 可以去这样骂

Alvina: 但是那条file list都是filter了 by个category 又好 我想到时候API如果有API拿回这些

Daniel: 其实就会有些反应 就是我尽量逐一转一转 你们现在拿CIO的 是啊是啊

Alvina: 因为我

Daniel: 有个type就拿回来 但是你那个一定要戒到business要的那个

Alvina: 会会会

Wil: 我反而另外一样东西想问的就是 如果是这样 instead of wealth intelligence 去pull from KMS 有没有可能KMSpush过wealth intelligence 我push到某一块地方然后你们去吃 那变成了 你不需要理会究竟你有没有总之你给我的file我assume就是 应该要吃到wealth intelligence

Alvina: 你给错了 如果是这样的话

Wil: push去sv sftp

Kyle: 不是的那个要专利牌了

Wil: 不可以sftp 如果我要close cloud去做data file

Kyle: 你们在哪里

Wil: GCP啊 OK 所以那个我们要做data file 要走根据data data那边的话就应该要走jennifer 我想在哪个方便点而已 因为其实如果是file太大或者是太多其实push 用jennifer的方法好像好一点 美国limit大一点

Alvina: API一定有limit

Wil: 但是那个不好处就是什么呢?不好处就是我给你一个raw file 其实我里面有些metadata suppose你应该是要去 去连接KMS的嘛 就没有了 我又要再交多一个metadata file给你

Alvina: 我觉得 是啊 阿卡拉说我们现在去INR 都是用API

Kyle: 是的API

Alvina: 其实API我们就一定可以的 因为现在去INR也是这样

Kyle: 不过我们这条文是放DXP的

Alvina: 就是放 iGoogle 因为如果我经API呢其实我就备了

Wil: 我备了data那边的一个transaction file 因为API是standard

Alvina: 变了

Wil: 我的API就是我给你一条list之余 我可以有metadata 如果你们那边有需要存metadata去做process的话 例如说做个file association 然后我就给你一条link你再去拿 那就是变了 N加1这么多转 比如我有50个file 你扣5元一转 你拿个delta list然后就call50次去拿50个file回来这样 但是如果是这样,Daniel可能你要帮我和KMS那边合一合 如果做一个这样的API大概要多久 什么时候可以ready 因为我们business 是,阿娜你说

Alvina: 还有呢你说API应该是delta来的 Editial load 都要想 Editial load就未必用API了可能就是要 MENU也好,MENU accept那些file给我们也好

Wil: 你本身,你本身你们之前有说过的嘛,CIO的data其实你们都不会拿最 不会拿很旧的那些的嘛 是啊,就是我说的就是说

Alvina: 你问business 不是的,你

Wil: 你之前都一直跟着我说他们看最新的资料,我问我的business 我们可以问business的,如果那个

Alvina: Iniso delta我觉得可以再谈 是最新的,是最新的 不过呢 不同的document type呢,他们的expiry都不同的 在knowledge base 有些就 有些就一年,有些就三个月 想看 就是年报那种friend这样 我不知道为什么要存一年,不过有些就 如果他一年出一次的话,那我 就算存一年,我只是得一份而已,我觉得ok的 要看量有多少,用API 可以的,不过 不过,如果量多就

Wil: 这样说,我觉得Iniso可以再谈的 因为我们真的要跟business合,究竟他们会有多少 然后从而看究竟Iniso的量有多少的 反而你说的我daily delta 因为我assume是daily升,你们现在拿sale都是daily升的嘛 daily的嘛,你们那边

Kyle: 是的,daily

Wil: 我assume我们这里都是daily,这里可能我们需要问sale的 同事就是我daily的几个月份文件 这个KMS里面应该会有 一个记录 然后之后那件事就是说,我们刚才探讨的是 用一个push和pull嘛,那我filebase还是API,如果是真的API,大家都觉得这样去做的话 是好点这样的API,反而另外一件事就是,我想问在wealthy intelligence里面 你们比如说,你经过API去拿,除了说我知道了URL之后 其实 你还需要什么data,有没有需要其他任何的metadata

Alvina: 我现在就想问一下,如果是在那里,那里的那个

Kyle: 要看下,要看下,例如是那个 那个document的 那个分类 然后sale daily还是weekly report 跟着那个 date update的date 然后就去哪个

Alvina: publish date,update的date,然后那个是哪一个公司的

Kyle: report来特斯拉,或者什么类似的metadata 要的,因为我们要去

Wil: 老实说,里面呢,我不知道你们写的 或者那个solution有没有facetable 因为有某些data,其实你们是就着你们CIO平时写的手法来做的 我都要看下我们CIO的手法是否也是这样的 我不知道这件事是如何,可能这件事会有所影响,但是那个问题是

Kyle: 要看你们恒生的business,它怎么用那个variantation 因为 我们拿回这些data,其实要做 那个 起个vector 然后你做回那个indexing trunking那些东西,它怎么search 它那个question bank是怎样的,大概 你如果你是做过RAG,你要做trunking,suppose你都不会

Wil: 逐份逐份文件看的啦,你都是在说用那个algorithm去计 我做trunking,我embedding,我反而不担心去做那个unstructured 反而是你们有些structure的mapping,好像你刚才说的 一个文件,可能他们说我们要有些 asset class,例如说我这份文件其实是在说美股的周报 美股这个tag可能有associate,因为我不是based on那个 内容去 做个association,而是做tagging去做个association 这些我相信就是刚才Carol你说的,有些cathification等等 publish我理解啦,反而是company其实我不是很理解,就是我是不是要将每一个comp里面 每个company都要make it as a list 因为我们没有的嘛,我是理解的,CIO里面 所以我担心的就是如果是这样的话,这些tagging可能是怎样interpret data都摆在logic side里面 就变了其实恒生可以adopt到,从而拿到那个effect是有限 因为 本身那个data structure,本身那个source会有点不同 但是我想这样说,到底做到多少这件事,我想可能往后面再看,但是至少 可能看会不会你们有个list 去告诉我们,究竟其实有什么metadata是你们会用 是什么来的 然后看看究竟KMS那边是否可以provide,如果没有 我们这边要看怎样去解决这个问题 至少现阶段我们 谈的就是我们KMS会给一个API拿delta file 然后里面会包Metadata,就是这个file里面 有什么metadata,或者这个Daniel你再update一下 因为 拿file就没有metadata,如果是这样的话,就是说一条list 拿list的时候就会有metadata 那metadata我们可以包到什么呢 那我们就要做mapping

Alvina: 这个ok 然后我们就拿回香港的API

Daniel: 或者你问KMS

Alvina: 问KMS 他们需要什么metadata

Wil: 对了,还有一些位置如果真的没有的话,其实有多大影响对于wealth intelligence里面 因为我们CIO同时去做那个分那个 mapping的时候,都讲到明,我们的tagging都写在CIO document里面 我估计你那边做OCL拿了所有tagging的,那些tagging你就知道了 我就不想再加下去了 我们的business是可以去到这样的地步的 所以我都要看的就是,有某些位置,可能tagging里面有,我们已经拿到 或者我们要再传下去,再拿,这件事是合理的,但是我暂时担心不是全部拿到 我看到的是

Alvina: 我走的而已 你说走都可以啦,因为我不熟悉的影片都是这样的 我的意思是你没有那些东西,就给个AI去判断,准不准 另外一件事,那些metadata的tagging 唯一的帮手就是 Synergy Synergy 所以如果我们知道了existent有什么tag,然后我们尽量map,map不到的

Wil: 我们就看看有没有解决,没有解决就听天由命,我觉得OK的

Alvina: 如果真的不行,就建立一些rules去做,去拆啦 可以,可以

Wil: 可以,那what's next? 就可能看,麻烦Carol给我们一条list,你send给Daniel和我 share出来,Daniel就麻烦你量一量跟Given他们做一件 做这个API,这个API是support整个wealth 他没得不做的,他不做的,我要搬老板出来

Daniel: 我刚才问了Rollin,他们超过排了,不要紧,你照问他,他说没有,就先输了

Wil: 是啊,如果没有的话就找 找Alex去谈

Alvina: 因为那件事是

Wil: 你先说吧

Alvina: 没有,我说Carol你找Chinson 说一说,我觉得问题很大,Given我们已经在做这个Pattern 因为我做不到,我本身有想过做一个standalone的file movement

Wil: 如果是做file movement的话,其实那个effort就变成了放在 Wealth intelligence那里,因为我们 做file movement就是,可能我会有两个file同名,一个就是Jason,一个就是Lon在Wallfile 明白明白,所以我只是和他说一声而已,先让他听一下

Alvina: 应该没问题 但是你们什么时候出呢

Wil: Business的口吻当然是越快越好

Alvina: 我看到Tony恒生都没过,你们现在出什么,Viltel还是CNBC CNBC就预了下年一Q出的

Wil: 恒生Viltel要做先 恒生Viltel本身说不出 但是两个星期之后突然间就说要,又是9月10月,突然间说要

Alvina: 总之他说

Wil: 突然间就说我们老板要出了声,要这件事,你IT死出来了 那种情况

Alvina: Tony知道的嘛,因为我看他上个星期才做了一个

Wil: 那个问题是,就算,我这样说,就是我们的solution先不要理会他有没有resources,因为他有没有resources 不影响我们的solution 除非我们有两个option,一个是要浪费时间做点 但还是要看究竟哪个叫做合理点,proper点 这样 我想可能这样说吧,看你们那边会不会都可以问到,比如Twins,如果做一个file base的话 究竟是怎样,因为 file base里面都有effort 我觉得是看有没有什么大家拿出来称,因为暂时我觉得

Alvina: 还有一个考虑的,你们其实一天会有多少,应该不多的

Wil: 我问回,这个我问回

Alvina: 如果你说一天 一天 50-100条 拿不是问题 拿完之后都要process 是不是真的这么完美地,六个小时内做完呢 我当我半夜 cut off 12点 你们又搞了两天

Wil: 我明白,我明白,所以其实 如果你这样说的话 如果真的要这样cater 理论上file base是最理想的 因为我就不断搬file过去,你们consumer就抹走 这个是最理想的

Alvina: 所以要看量,如果你说 没有的,每个礼拜 只有几份,一天几份,可能weekend多一点 但是weekend你不用开行嘛 就是礼拜天慢慢做都可以 那 我觉得API都ok的,如果你不是说每晚有几十份

Wil: 我要问一问,但是你提完我之后,我又突然起了一条筋,我觉得file base好像 安全点

Alvina: 两种也好也不好

Wil: 我觉得这样说吧,我as Aki 在座大家都是architect 如果我用API call可能叫做more pretty点,但是问题是我cater不到你们刚才说的量 因为他突然间真的有些东西突然间cater 真的会出的话 我因为 我on daily的话,我API不够facible enough 除非我会有个,你们那边会记住了 我上次ask的是这个时间 然后呢 你给了我一个list,我还会记录下我哪几个success,哪几个file 我处理不切 下一次我再怎么separate,怎么处理,如果不是的话,我没有这个 catering的话,我resilience是顶不到的

Alvina: 因为现在我们问INR,是daily的吗

Kyle: daily的,但是我back回来一点,因为 INR去API那边metadata很齐张 但是如果 如果是conference 你KMX那边的metadata 有多少呢,我就想 我都不知道 先探讨一下

Alvina: 我的integration metadata 没有人回答,要business下场,还有要看report

Kyle: 回来INR,是daily,我们是去callAPI,去识别到哪些是 Delta参与的document

Alvina: 但是他是怎样的,他是一条API问完,他给了我list,然后我cache 我把delta的list放到staging 然后逐个去拿,还是怎样的

Kyle: 我要出场 等一会

Alvina: 对啊,你讲conference 对的,可以称用filebase,或者用API 我今天也找个时间问一下 因为如果你们那边,我是不是都拿了你的list,我慢慢consume

Wil: 就跟user说,我们mode是t-1,但是有时会delay 这个是其中一个,但是如果说我总之搬过来了,你们慢慢consume的话,照理说你们就更clean 因为你们做的东西就是,总之我看到 file有10个,就做10个

Alvina: 没错,我就不需要说,又要cache低,然后又要记录下哪个record做了,哪个没做

Wil: 你里面的logical似乎更麻烦

Alvina: 对啊,我要staging,要逐个去conference 对啊,如果不是我放在sv,那它已经有足够的sla

Wil: 还有足够的resilience 我又不会再担心file loss了,那唯一的是什么呢,唯一一个不好处就是 我们没办法check到究竟那个consumption rate,我只能够check, wealth intelligence有没有这个file 但是我就没有一个figures,究竟total有多少个 我真的各自有%concern 但是你问我,我觉得 business未必需要这么real time知道,我有多少file我没consume,你要和我消多少

Alvina: 但是我们web intelligence有个pick 是看source的 就是给一个rm或者staff去 所以那个我会在metadata,就是suppose如果真的有

Wil: 那个我都要回你kms的url 要的要的,因为到最后如果是这样做的话,我甚至乎可以做的就是,我在kms里面做一个batch 然后就说 我自己detect到,然后我就把那个file拿过来,和一个jsonfile 那个jsonfile可能是同一个document name 然后里面就包了你们想要的metadata,或者我们可以准备的metadata 包括了那个url 那个url是kms的url,还是那个web site的url呢就fathable了 因为我可以kms在里面

Alvina: 对,所以变成了日后你再说,我们business那边真的要找,我真的要send给那个客户,这个jsony

Wil: 我觉得ok,因为我个人都觉得是合理的 我没理由空口和那个 user说话,那个customer说话,我们是这样写的

Alvina: 因为你给我我都会问,那你有没有一个link给我看一份document

Wil: 你自己找吧,这件事就不make sense了

Alvina: 但是如果我是

Wil: January的话,我就入后就是,我在kms里面maintain的时候,maintain完,然后showdown我就可以 扔给你的时候 你不需要 改wealth intelligence里面的logic 就已经可以做得到 这件事了 我觉得这样可能会好一点 Daniel 如果是这样,我明天跟你合作 我今天跟你合作

Alvina: 我们也拼一下同事

Wil: Daniel我跟你合作的,是两边,我想都要问的,不过如果可以做到filebase,你问我 我个人我会建议filebase 一来他cater fail之后 他做resilience那件事,ok,因为 kms知道我push是file,我就再在January过 那也同一个方法,其实可以cater到inisolo

Daniel: 那还需要问他拿吗 还需要开头有一个API就拿 两类方法来的,如果file我们

Wil: 两边都consider,但是纯粹on solution wise 我暂时觉得 一个用API拿delta,再逐个file拿 vs kms去做push,放到sv,然后wealth intelligence 自己consume filebase有个好处就是de-couple 我知道我搬file过去,file我就自己再搬过 对wealth intelligence来说,我看到有file我就consume,没有file我就不consume 整件事是 multi-couple的,第一 第二就是 我可以cater inisolo 第三就是 如果我这个file死了,我日后第二天再 再兑过来,其实大家都more flexible的 这样 但是 我都想问,就是kms那边如果提供一个API的情况去做个data去拿的话 那个情况会是怎样,如果真的 filebase不work的话,我们都有另一个backup solution 我会这样建议

Alvina: 但我想问jonipa会做这些东西吗,因为我之前用jonipa 真的 是一个data file的形式 对呀,简单点说就是我们会将

Wil: 我放了 放了一堆file在staging里面 然后给juniper,juniper就去吃,就说你确定会把这个staging里面的file搬去target sv这样

Alvina: 他不会做任何事情的 我以前用juniper是set 多少点send一个file,那个file叫abc.csv 不是的,我们是可以filebase,可以fotobase的嘛,总之你把整个foto里面的data

Wil: 搬过去 不会做个周快乐搬的 他唯一不好处的是 他唯一不好处的是什么呢,慢 不是guarantee的一个sla来的 他有可能是很快,五分钟里面send到,或者可能你等几个钟都send不到的 但是in close cloud我们就一定要用juniper 我们没办法,但是似乎就这样听下去 好像大家做的东西相对独立和小型的 好多 那变成我们要配合的就是 那个file naming,就是raw file的naming,和本身json data的那个file

Alvina: 那个metadata

Wil: 那个file怎么配合呢,比如说我见到这里,我就改了个 后面的extension做json,我就expect是拿到那个metadata 第二就是那个meta file里面的structure是怎样,就只配这两样东西 那似乎少点东西配合

Alvina: 是的

Wil: 还有error handling就是各自理会,我们不需要大家夹大家的error handling

Alvina: 还有很多时候升回,我之前问过他们,很多时候都是用it support 不知道为什么对加 那条link有事

Wil: 你说的是 url base API base

Alvina: 可能是,API死了又拿不到,其实最后都是用it去 是呀,这个最通常,为什么你吃不到,可能是

Wil: 我最担心的就是,他的API不是做到 不是做到,我拿n-1或者n-2,我死了一只,我再拿过,我怎么拿呢 然后就要,我要特意去找哪一个发生死了 那件事就算我那边排行公司也有这么generic的API 你那边又要cater这件事

Alvina: 是啊 是啊

Wil: 如果你那边有cater,大家也要cater 那些effort都大了,不如用回我file base 我宁愿推file base 是啊,还有你会有很多API traffic的嘛

Alvina: 如果要reload啊,或者 不知道为什么

Wil: 是啊,还有我觉得对我们来说呢 KMS我prefer去宁愿自己在1月的div file放在某个地方 好过他provide一个API出来,其实是否有很大的reusability,其实又不一定

Alvina: 这样吧,我们暂时

Wil: 按着两个方向先啦

Alvina: file base好像比较好点 问问大家,问问lgmateam的意见先啦

Wil: 是啊,然后之于effortwise可能就要靠他们啦 我就问回,我就问回CIO的同事,或者我们那边,究竟大概量是多少啦 但是如果用这个方法的话,量应该不算很大问题

Alvina: 我觉得 我们暂定去这个方向先啦

Wil: 那我看一下,尝试 我希望有时间send回个wrap up的email啦,我记得不记得而已因为 这样啦,Daniel你没有什么特别问题呀,on这个sing up

Daniel: 是啊

Wil: 你觉得

Daniel: 我唯一的东西就是 如果one off的话呢 其实他就只不过我们都会谈到,几时几月这样子 多久的伤害出来,一次就夹,但是如果你之后再有其他file type 就每一次都要夹一次啦,这个就不像是一样

Alvina: 是啊,我们现在又遇到,当初就是从古初开始呢 那个vcr可能support三类document的啦 可能是CIO weekly 或者daily digest,ingest那些这样啦,然后呢 其实我们现在on going每一个月都帮他们加约的document type 香港也是这样的 所以其实 加document type的type意思是指category 是啊是啊是啊,projective有个confirmation 他们有成 初初只有五六种document啦 CIO view 现在记到这么多,其实这两年他们 不停地做

Wil: 我理解 我的理解是他们那些所谓的category是virtual attacking来的嘛

Alvina: 是啊是啊,是不是virtual,他们都是那个document的名字

Wil: 名字difference不是很合理的吗

Alvina: 他们是这样的,category全部都是CIO来的,但是report名 其实你看到他们每个report的frequency都不同啦,calcification不同啦 然后expiry time都不同的 当初没有那么多的,现在加一下呢,我们下面还在做的 spirey有不同的

Wil: 我不知道,我觉得

Alvina: 他们的expiry不同,应该是给我们看的,我们自己用的 是的 我的意思是他们每一年都会加几份report的

Wil: 我在想是不是group了他们,就是当是我有几类group,这个group A就是这样的 你加file,我带个问题 file name照样不应该影响到那件事的嘛,我们不会基于file name来做logic的嘛

Alvina: 最主要应该是这些 要看放了knowledge bay的那个多久啦 接着要拿回来看,retention放多久啦 所以就group了他们,比如说我不会profile给他们任选的嘛,而是说

Wil: 比如说type A 你就是resilience那么多 然后这个那么多 我们去谈那个group是容易的嘛

Alvina: 是的,那个integration是一样的,但是他们这里我们为什么要做呢,很多时候都是要做logic simulatty check的logic,所以你看到,我的意思,我想带出的意思就是可能今天 我明白我明白,20份report,每一年都在加一下,所以用batch,pro,你one of low 就容易点搞 哦,我明白,我明白

Wil: 老实说 我觉得那个位置是 这个我之后大家再夹,就是比如说里面究竟我们是否可以在恒生里面和user说 只有几个category,你一是选这个,retention就一定是这么多的啦 那看可不可以这样局他们 这样就simplify这个logic 你问我,我尝试这样做

Alvina: 他们通常后加的东西 就是这些report,他们无端端说,我们business是做多了三分之一 没有的啦,加上

Wil: 这个category,至少logical process,我知道,我只会有多少份retention是五日这样 或者七日 但是我处理logical,我比较type,那你那份document就map了,原来这个type,我在metadata里面加上 它是type really,type叫really 这样 那变成了,我不知道,我未完全踩进去看究竟logic是不是应该这样做,但是我纯粹这样想而已 这个再谈吧,我觉得

Alvina: 我们要做的,也要看report的sample 因为我们拆的时候,他们有些东西 没有了,我等给business自己处理,或者给RTF自己处理

Wil: 就是开播做implementation的时候

Alvina: 因为要执得 要 真的有些logic要做,才会 才会弄到 acuracy那么高

Wil: 我觉得这样看,如果你说我们要执的,在import里面的process 要做某些东西的 要去document去行的,不是一个generic的RAG,而是一个 per type的customer的RAG 如果真的要做到这样的话,我只能够说,就是based on user,到时候就真的 一拍一拍看,但是我不知道,我觉得那个位置 是不是真的需要做到这个地步呢

Alvina: 我初时也觉得不需要这样 证明他们真的这样做 不要紧啦,我们 不要紧,我们之后再做吧,我觉得试了

Wil: 我觉得试了先,比如说我们align了一个solution 然后就各自去pass,有需要过会就过会,没有需要过会就align,至少我们align了 然后share 然后如果两边需要各自做事,就要看要多久的effort,然后再给business 坐底可能要11月

Alvina: 但是你们现在只是做KMS的事 你们不要其他source的了

Wil: 例如呢

Alvina: 这样说吧,CIO我们之前就放了sharepoint,但是就没有integrate

Wil: 那好啦,然后 年头就demise 有谈过究竟是不是应该在wealth的世界做一个CIO的system的 knowledge system的maintenance 到最后呢,我们wealth没钱 大家就agree了 全世界 全世界 wealth的IT啦 wealth的IT啦 然后我们AI的case AI lead啦 Architect啦,就aligned了 我们将CIO的document放在KMS 所以对于我们来说呢,KMS就会是CIO的knowledge的source 我们就不会说 我会放一些conference,会放一些DXP 大不了的就是我这份文件可以通过一个什么的URL可以在access到 这样而已 所以暂时我见到CIO是 是standard的 然后其他的news那些东西,大家都是经MDS,refinitiv,etdat等等那些东西 那都是standard的

Alvina: 不行啦,refinitiv要改用mcp contract的问题 今早我先和Tony解释过一段 应该是refinitiv 就是LSEP 他们被人收购了,现在叫LSEP 他们说以前那张contract,dap 那些usage不是for AI的 现在应该是Business和他们在谈一份新的contract 谈完之后,就要拿market news的那个piece 应该转去call他们的mcp

Wil: 这样说吧,如果转了mcp,那个integration要再谈,要再过会,问题是 我和Business那边share过 如果他转了mcp 到底他
