# -
// ==UserScript==
// @ScriptName        墨鱼去开屏V2.0
// @Author            @ddgksf2013, @blackmatrix7, @app2smile, @DivineEngine, @kyle, @Nick-workflow, @kkpp, @LE
// @TgChannel         𝐡𝐭𝐭𝐩𝐬://𝐭.𝐦𝐞/𝐝𝐝𝐠𝐤𝐬𝐟𝟐𝟎𝟐𝟏
// @TgBot             https://t.me/ddgksf2013_bot
// @WechatID          公众号墨鱼手记
// @Feedback          💡请通过邮件反馈问题『其它方式一概无视』：𝐝𝐝𝐠𝐤𝐬𝐟𝟐𝟎𝟏𝟑@𝟏𝟔𝟑.𝐜𝐨𝐦 💡
// @UpdateTime        2023-02-19
// @Please            如需引用请注明出处，谢谢合作！
// @Function          去除APP首页启动广告和部分应用内广告，如果有需要的去除广告的APP，可以公众号后台直接回复
// @ExtraTxt          Only provide the removal of open-screen advertisements for personally used apps
// @Attention         QuantumultX能去广告，不代表能去所有广告！
// @Mark              名字后面的*代表该应用启动倒计时仍然存在
// @Attention         如果广告仍然存在，请『卸载应用』重新安装，还是不行则表示『规则里没有或已失效』
// @ScriptURL         https://github.com/ddgksf2013/Rewrite/raw/master/AdBlock/StartUp.conf
// ==/UserScript==


# ======= 0~9 ======= #

# > 12123
^https:\/\/gab\.122\.gov\.cn\/eapp\/m\/sysquery url reject
# > 12306
^https?:\/\/ad\.12306\.cn\/ad\/ser\/getAdList url script-response-body https://github.com/ddgksf2013/Scripts/raw/master/12306.js


# ======= A ======= #

# > 阿里巴巴
^https?:\/\/acs\.m\.taobao\.com\/gw\/mtop\.alibaba\.advertisementservice\.getadv\/ url reject


# ======= B ======= #



# ======= C ======= #



# ======= D ======= #

# > 大师兄
^https?:\/\/sdk\.alibaba\.com\.ailbaba\.me\/.*?\/v\d\/(version|top_notice\?|advert\?position=[^2]+) url reject

# ======= E ======= #



# ======= F ======= #



# ======= G ======= #



# ======= H ======= #

# > 虎牙直播
^https?:\/\/business\.msstatic\.com\/advertiser\/material url reject

# ======= I ======= #

# > 爱思
^https?:\/\/list-app-m\.i4\.cn\/getopfstadinfo\.xhtml url reject


# ======= J ======= #

# > 京东
^https?:\/\/api\.m\.jd\.com\/client\.action\?functionId=(start|queryMaterialAdverts) url reject-200
^https?:\/\/(bdsp-x|dsp-x)\.jd\.com\/adx\/ url reject-200
^https?:\/\/api\.m\.jd\.com\/client\.action\?functionId=(hotWords|hotSearchTerms) url script-response-body https://github.com/ddgksf2013/Scripts/raw/master/jd_json.js
# > 京东金融
^https?:\/\/ms\.jr\.jd\.com\/gw\/generic\/aladdin\/(new)?na\/m\/getLoadingPicture url reject-200
# > 京东极速版
^https?:\/\/api\.m\.jd\.com\/client\.action\?functionId=lite_advertising url response-body jdLiteAdvertisingVO response-body ddgksf2013
^https?:\/\/api\.m\.jd\.com\/client\.action\?functionId=lite_SmartPush url response-body pushData response-body ddgksf2013


# ======= K ======= #

# >酷安
^https?:\/\/api\.coolapk\.com\/v6\/(feed\/(replyList|detail)|main\/indexV8|dataList) url script-response-body https://github.com/ddgksf2013/Scripts/raw/master/coolapk.js
^https?://api-access\.pangolin-sdk-toutiao\.com/api/ad/union/sdk url reject
^https?:\/\/api\.coolapk\.com\/v6\/search\?.*type=hotSearch url reject-dict

# ======= L ======= #


# ======= M ======= #

# > 美团外卖
^https?:\/\/img\.meituan\.net\/(bizad|brandCpt)\/\w+\.(png|jpg) url reject
^https?:\/\/wmapi\.meituan\.com\/api\/v\d\/(openscreen\?ad|loadInfo\?|startpicture) url reject
^https?:\/\/www\.meituan\.com\/api\/v\d\/appstatus\?ad url reject


# ======= N ======= #


# ======= O ======= #



# ======= P ======= #


# > 拼多多
^https?:\/\/api\.(pinduoduo|yangkeduo)\.com\/api\/cappuccino\/splash url reject


# ======= Q ======= #


# ======= R ======= #


# ======= S ======= #

# > Soul
^https:\/\/data-collector\.soulapp\.cn\/api\/data\/report$ url reject


# ======= T ======= #


# ======= U ======= #


# ======= V ======= #


# ======= W ======= #


# > WeChat110
^https\:\/\/(weixin110\.qq|security.wechat)\.com\/cgi-bin\/mmspamsupport-bin\/newredirectconfirmcgi\? url script-response-body https://raw.githubusercontent.com/zZPiglet/Task/master/asset/UnblockURLinWeChat.js


# ======= X ======= #



# ======= Y ======= #


# ======= Z ======= #

# > 掌上生活
#^https?:\/\/mlife\.cmbchina\.com\/ClientFaceService\/api\/mlife\.clientface\.clientservice\.api\.advertiseService\/preCacheAdvertiseSec url reject
# > 中国移动
^https?:\/\/client\.app\.coc\.10086\.cn\/biz-orange\/DN\/init\/startInit url reject
^https?:\/\/client\.app\.coc\.10086\.cn\/biz-orange\/DN\/explorePage\/getAdverList url reject
# > 招商银行
^https?:\/\/webappcfg\.paas\.cmbchina\.com\/v1\/func\/getmarketconfig url reject
# > 中国联通
^https?:\/\/m\.client\.10010\.com\/mobileService\/(activity|customer)\/(accountListData|get_client_adv|get_startadv) url reject
^https?:\/\/m\.client\.10010\.com\/uniAdmsInterface\/(getHomePageAd|getWelcomeAd) url reject
# > 知乎
^https?:\/\/static\.zhihu\.com\/[^\/]+\/(main|column)\.signflow\.[^.]+.js url reject
# > zhuishushenqi
^https?:\/\/adx-cn\.anythinktech\.com\/bid url reject
# > 中国银行
#^https?:\/\/mbs\.boc\.cn\/ubas-mgateway-static\/images\/advertType\/.+.jpg url reject-img
# > 中国移动广东
^https?:\/\/gd\.10086\.cn\/gmccapp\/serv\/\?servicename=GMCCAPP_704_002_001_001 url reject





hostname = gd.10086.cn, jdread-api.jd.com, ms.jr.jd.com, bdsp-x.jd.com, dsp-x.jd.com, api.m.jd.com, router-app-api.jdcloud.com, app.homeinns.com, cdn-evone-ceph.echargenet.com, mlol.qt.qq.com, acs.m.taobao.com, ad.12306.cn, sdk.alibaba.com.ailbaba.me,  client.app.coc.10086.cn, api.pinduoduo.com, acs.m.taobao.com, www.meituan.com, mp.weixin.qq.com, security.wechat.com, weixin110.qq.com, cdn.*.chelaileapp.cn, api.coolapk.com, app3.qdaily.com, daoyu.sdo.com, img.jiemian.com, ccsp-egmas.sf-express.com,  app.ap.d3yuiw4.com, static.zhihu.com, elemecdn.com, fuss10.elemecdn.com, www1.elecfans.com,  p*.meituan.net, wmapi.meituan.com, 
