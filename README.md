<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, viewport-fit=cover">
    <title>品牌内容自动化 · 情绪审美型AI中台</title>
    <!-- Google Fonts & Tailwind CDN (轻量级但保留高级感) -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:opsz,wght@14..32,300;14..32,400;14..32,500;14..32,600;14..32,700&display=swap" rel="stylesheet">
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- 微调tailwind配置：扩展主题 -->
    <style>
        * { font-family: 'Inter', sans-serif; }
        body { background: #fefcf8; }
        .gradient-border {
            background: linear-gradient(135deg, #e0d8c8, #f3efe6);
        }
        .card-shadow {
            box-shadow: 0 12px 30px rgba(0,0,0,0.03), 0 2px 4px rgba(0,0,0,0.02);
        }
        .brand-gradient-bg {
            background: radial-gradient(circle at 10% 30%, rgba(245,240,230,0.5), rgba(255,250,240,0.2));
        }
        ::-webkit-scrollbar {
            width: 5px;
        }
        ::-webkit-scrollbar-track {
            background: #f1ede7;
        }
        ::-webkit-scrollbar-thumb {
            background: #cbc3b5;
            border-radius: 8px;
        }
        @keyframes fadeSlideUp {
            from { opacity: 0; transform: translateY(12px); }
            to { opacity: 1; transform: translateY(0); }
        }
        .animate-fade-up {
            animation: fadeSlideUp 0.3s ease-out forwards;
        }
        .transition-smooth {
            transition: all 0.2s ease;
        }
        /* 自定义checkbox风格 */
        input[type="checkbox"] {
            accent-color: #a07e5c;
        }
    </style>
</head>
<body class="antialiased text-stone-700">

    <main class="max-w-6xl mx-auto px-4 py-8 md:py-12">
        <!-- 品牌头部：情绪审美型 AI 中台 -->
        <div class="text-center mb-10 md:mb-14">
            <div class="inline-flex items-center gap-1.5 bg-white/60 backdrop-blur-sm px-4 py-1.5 rounded-full border border-stone-200/80 shadow-sm mb-4">
                <span class="text-sm font-medium text-stone-500 tracking-wide">✨ AI 品牌内容大脑</span>
            </div>
            <h1 class="text-4xl md:text-5xl font-semibold tracking-tight text-stone-800 max-w-3xl mx-auto leading-[1.2]">品牌内容自动化<br><span class="text-stone-500/80 text-2xl md:text-3xl">情绪审美 × 长期内容矩阵</span></h1>
            <p class="text-stone-500 mt-4 max-w-xl mx-auto text-base">输入一次品牌人格 · 系统自动生成一周跨平台内容 · 持续输出品牌感</p>
        </div>

        <!-- 双栏布局：左侧表单（品牌人格系统） + 右侧预览（内容工厂输出） -->
        <div class="flex flex-col lg:flex-row gap-8">
            <!-- 左侧：品牌人格创建区 -->
            <div class="lg:w-2/5 bg-white/70 backdrop-blur-sm rounded-2xl border border-stone-200/70 p-6 shadow-sm card-shadow transition-smooth">
                <div class="flex items-center gap-2 mb-5">
                    <span class="text-lg">🧘</span>
                    <h2 class="text-xl font-semibold text-stone-800">品牌人格系统</h2>
                    <span class="text-xs bg-stone-100 text-stone-500 px-2 py-0.5 rounded-full ml-2">记忆 · 语气 · 审美</span>
                </div>
                <form id="brandForm" class="space-y-5">
                    <!-- 基础信息 -->
                    <div>
                        <label class="block text-sm font-medium text-stone-600 mb-1.5">品牌名称</label>
                        <input type="text" id="brandName" placeholder="例：白屿运动 / 屿野咖啡" class="w-full px-4 py-2.5 rounded-xl border border-stone-200 bg-white focus:border-stone-400 focus:ring-1 focus:ring-stone-300 transition outline-none">
                    </div>
                    <div>
                        <label class="block text-sm font-medium text-stone-600 mb-1.5">行业赛道</label>
                        <select id="industry" class="w-full px-4 py-2.5 rounded-xl border border-stone-200 bg-white focus:border-stone-400 outline-none">
                            <option value="轻运动/瑜伽">轻运动 / 瑜伽普拉提</option>
                            <option value="疗愈/身心灵" selected>疗愈 / 身心灵</option>
                            <option value="咖啡/茶饮">咖啡 / 茶饮</option>
                            <option value="女性消费/香氛">女性消费 / 香氛</option>
                            <option value="民宿/生活方式">民宿 / 生活方式</option>
                            <option value="美业/护肤">美业 / 护肤</option>
                        </select>
                    </div>
                    <div>
                        <label class="block text-sm font-medium text-stone-600 mb-1.5">品牌理念 / 一句话精神</label>
                        <textarea id="philosophy" rows="2" placeholder="例：运动是身体的一场呼吸冥想 / 慢下来，也是一种能力" class="w-full px-4 py-2.5 rounded-xl border border-stone-200 resize-none focus:border-stone-400 outline-none"></textarea>
                    </div>
                    <div>
                        <label class="block text-sm font-medium text-stone-600 mb-1.5">品牌语气（3-5个词）</label>
                        <input type="text" id="tone" placeholder="松弛感、极简、呼吸感、治愈、独立" class="w-full px-4 py-2.5 rounded-xl border border-stone-200">
                    </div>
                    <div>
                        <label class="block text-sm font-medium text-stone-600 mb-1.5">审美风格参照</label>
                        <input type="text" id="aesthetic" placeholder="例：lululemon / Alo Yoga / 侘寂风 / 奶油肌理" class="w-full px-4 py-2.5 rounded-xl border border-stone-200">
                    </div>
                    <div>
                        <label class="block text-sm font-medium text-stone-600 mb-1.5">禁用词/避免概念 (可选)</label>
                        <input type="text" id="forbidden" placeholder="“打爆”“震撼”“赶紧买”等" class="w-full px-4 py-2.5 rounded-xl border border-stone-200">
                    </div>
                    
                    <!-- 多平台选择 -->
                    <div>
                        <span class="text-sm font-medium text-stone-600 block mb-2">内容适配平台（可多选）</span>
                        <div class="flex flex-wrap gap-3">
                            <label class="flex items-center gap-1.5 text-sm"><input type="checkbox" value="小红书" checked class="w-4 h-4"> 小红书</label>
                            <label class="flex items-center gap-1.5 text-sm"><input type="checkbox" value="Instagram" checked> Instagram</label>
                            <label class="flex items-center gap-1.5 text-sm"><input type="checkbox" value="抖音" checked> 抖音</label>
                            <label class="flex items-center gap-1.5 text-sm"><input type="checkbox" value="视频号"> 视频号</label>
                            <label class="flex items-center gap-1.5 text-sm"><input type="checkbox" value="TikTok"> TikTok</label>
                        </div>
                    </div>

                    <button type="submit" id="generateBtn" class="w-full mt-4 bg-stone-800 hover:bg-stone-700 text-white font-medium py-3 rounded-xl transition-all shadow-md flex items-center justify-center gap-2">
                        <span>✨ 生成品牌内容周历</span>
                        <span>→</span>
                    </button>
                    <p class="text-xs text-center text-stone-400 mt-3">AI内容工厂 · 基于品牌人格自动生产</p>
                </form>
            </div>

            <!-- 右侧：内容工厂输出区 -->
            <div class="lg:w-3/5 bg-white rounded-2xl border border-stone-200/80 shadow-sm overflow-hidden flex flex-col">
                <div class="px-6 py-4 border-b border-stone-100 bg-stone-50/40 flex justify-between items-center flex-wrap gap-2">
                    <div class="flex items-center gap-2">
                        <span class="text-lg">📋</span>
                        <h3 class="font-semibold text-stone-700">AI 内容工厂 · 每周内容矩阵</h3>
                    </div>
                    <span id="brandPreviewBadge" class="text-xs bg-white px-3 py-1 rounded-full border text-stone-500">等待品牌生成</span>
                </div>
                <div id="contentOutput" class="p-6 overflow-y-auto max-h-[650px] bg-white/50">
                    <div class="flex flex-col items-center justify-center py-12 text-stone-400 text-center space-y-2">
                        <svg class="w-12 h-12 text-stone-300" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="1" d="M9.813 15.904L9 18.75l-.813-2.846a4.5 4.5 0 00-3.09-3.09L2.25 12l2.846-.813a4.5 4.5 0 003.09-3.09L9 5.25l.813 2.846a4.5 4.5 0 003.09 3.09L15.75 12l-2.846.813a4.5 4.5 0 00-3.09 3.09zM18.25 12l1.5-1.5"></path></svg>
                        <p>填写左侧品牌人格，点击生成</p>
                        <p class="text-sm">获得一周内容排期、文案、脚本、情绪结构</p>
                    </div>
                </div>
            </div>
        </div>

        <!-- 下方说明：品牌AI大脑/订阅价值 -->
        <div class="mt-16 grid grid-cols-1 md:grid-cols-3 gap-6 text-center md:text-left border-t border-stone-200/60 pt-10">
            <div>
                <div class="text-2xl mb-2">🧠</div>
                <h4 class="font-semibold text-stone-800">品牌AI大脑</h4>
                <p class="text-sm text-stone-500 mt-1">永久记忆品牌语气、审美与内容偏好，避免重复与调性漂移</p>
            </div>
            <div>
                <div class="text-2xl mb-2">⚡</div>
                <h4 class="font-semibold text-stone-800">情绪内容矩阵</h4>
                <p class="text-sm text-stone-500 mt-1">周更品牌故事、产品种草、生活方式、热点借势，自动化适配平台</p>
            </div>
            <div>
                <div class="text-2xl mb-2">📆</div>
                <h4 class="font-semibold text-stone-800">内容日历 + SaaS订阅</h4>
                <p class="text-sm text-stone-500 mt-1">299/月起，品牌可持续获得“品牌人格化内容流”，不再是工具而是中台</p>
            </div>
        </div>
    </main>

    <script>
        // 模拟AI品牌内容生成器 —— 基于品牌人格及审美系统生成一周内容日历
        // 包含：选题 + 小红书文案/标题 + 抖音脚本 + Instagram情绪文案 + 品牌语气稳定
        
        // 辅助函数：获取选中的平台列表
        function getSelectedPlatforms() {
            const checkboxes = document.querySelectorAll('input[type="checkbox"]:checked');
            return Array.from(checkboxes).map(cb => cb.value);
        }

        // 核心生成函数 —— 返回七天内容对象
        function generateWeeklyContent(brandData) {
            const { name, industry, philosophy, toneRaw, aesthetic, forbidden } = brandData;
            // 解析语气词数组
            const toneWords = toneRaw.split(/[ ,、]+/).filter(t => t.trim().length > 0);
            const tonePrimary = toneWords[0] || "松弛感";
            // 品牌精神提炼
            const spirit = philosophy.trim() || (industry.includes("疗愈") ? "疗愈日常，安顿身心" : (industry.includes("咖啡") ? "用一杯的时间换回感知力" : "身体自由，精神明亮"));
            
            // 情绪模版库（品牌情绪结构）
            const contentBlocks = [
                { type: "品牌故事", emotion: "溯源·初心", templateKey: "origin" },
                { type: "产品种草", emotion: "自然·质感", templateKey: "product" },
                { type: "用户情绪", emotion: "共情·日常", templateKey: "user" },
                { type: "生活方式", emotion: "节奏·呼吸感", templateKey: "lifestyle" },
                { type: "节气/热点", emotion: "顺势·温度", templateKey: "seasonal" },
                { type: "创始人IP", emotion: "真实·信念", templateKey: "founder" },
                { type: "互动话题", emotion: "连接·邀请", templateKey: "engagement" }
            ];
            
            // 根据品牌信息动态生成每一天的内容
            const weekDays = ["周一", "周二", "周三", "周四", "周五", "周六", "周日"];
            const weeklyPlan = [];
            
            for (let i = 0; i < weekDays.length; i++) {
                const day = weekDays[i];
                const block = contentBlocks[i % contentBlocks.length];
                // 让部分特殊日子固定分配增加真实感
                let finalType = block.type;
                let finalEmotion = block.emotion;
                if (day === "周一") finalType = "品牌故事";
                if (day === "周三") finalType = "用户情绪";
                if (day === "周五") finalType = "生活方式";
                
                // 根据品牌行业生成具体内容文案
                const copyData = generateCopyForDay(finalType, name, industry, spirit, tonePrimary, aesthetic, forbidden);
                // 多平台版本内容摘要 (差异化hook)
                const platforms = brandData.selectedPlatforms.length ? brandData.selectedPlatforms : ["小红书", "Instagram"];
                const platformVersions = {};
                platforms.forEach(plt => {
                    if (plt === "小红书") platformVersions.小红书 = `📕 小红书版 · ${copyData.xhsTitle || copyData.title}\n${copyData.xhsContent || copyData.mainCopy.slice(0, 80)}… #${(name || "品牌")} #${tonePrimary}`;
                    else if (plt === "Instagram") platformVersions.Instagram = `📸 IG版 · ${copyData.igCaption || copyData.title}\n${copyData.igContent || copyData.mainCopy} ✨ · ${aesthetic || "极简美学"}`;
                    else if (plt === "抖音") platformVersions.抖音 = `🎬 抖音脚本 (15-30s hook) · ${copyData.douyinHook || copyData.title}\n画面:${copyData.visualSuggestion || "慢动作/呼吸感"} 文案:${copyData.mainCopy.slice(0,50)}…`;
                    else if (plt === "视频号") platformVersions.视频号 = `📹 视频号 · 温暖叙事 · ${copyData.title}\n核心文案：${copyData.mainCopy}`;
                    else if (plt === "TikTok") platformVersions.TikTok = `🎵 TikTok · 趋势音效+${copyData.tiktokTrend || "治愈卡点"} · 字幕:${copyData.mainCopy.slice(0,45)}`;
                });
                
                weeklyPlan.push({
                    day,
                    type: finalType,
                    emotion: finalEmotion,
                    title: copyData.title,
                    mainCopy: copyData.mainCopy,
                    hashtags: copyData.hashtags || `#${name.replace(/\s/g,'')} #${tonePrimary} #${industry.slice(0,4)}`,
                    platformVersions,
                    visualNote: copyData.visualNote || "封面氛围: 低饱和自然光 / 留白构图",
                    script30s: copyData.shortScript || null
                });
            }
            return weeklyPlan;
        }
        
        // 具体文案生成引擎 (模拟AI，但基于品牌人格参数)
        function generateCopyForDay(type, brandName, industry, spirit, tonePrimary, aesthetic, forbiddenWords) {
            // 品牌名称处理
            const bName = brandName || (industry.includes("咖啡") ? "屿野咖啡" : (industry.includes("轻运动") ? "白屿运动" : "慢屿疗愈"));
            // 不同内容类型不同情绪文案
            let title = "";
            let mainCopy = "";
            let xhsTitle = "";
            let igCaption = "";
            let douyinHook = "";
            let visualNote = "";
            let shortScript = "";
            let hashtags = `#${bName} #${tonePrimary} #生活方式`;
            
            if (type === "品牌故事") {
                title = `「${bName}」的诞生：一场关于${spirit.slice(0, 12)}的旅程`;
                mainCopy = `一切从一次呼吸开始。${bName}不想定义运动/消费，只想提供一种感知身心的方式。我们相信真正的品牌不是被记住，而是被感受。${spirit}，让日常成为仪式。`;
                xhsTitle = `✨ 3个故事告诉你，为什么${bName}不只是产品`;
                igCaption = `a brand born from stillness. ${bName} — where movement meets meditation.`;
                douyinHook = `很多粉丝问这个品牌凭什么火？今天讲个故事。`;
                visualNote = `胶片感回忆拼贴/旧纸张纹理 + logo局部特写`;
                shortScript = `【0-5s】黑屏白字：“你有没有想过，产品也可以像一首诗”\n【5-15s】展示品牌手稿/工作室画面\n【15-30s】念白：${mainCopy.slice(0,60)}...`;
            } 
            else if (type === "产品种草") {
                title = `亲测｜藏在${aesthetic || "奶油肌理"}里的质感好物`;
                mainCopy = `它不是功能最强的，却是每次使用都会感到平静的一件单品。从材质到触感，${bName}在意的不仅是效用，更是每一次接触时的感知力。${tonePrimary}，就藏在这些日常器物里。`;
                xhsTitle = `🍃 冷门但高级｜${bName} 打开了我的五感`;
                igCaption = `objects that breathe with you. ✨ ${bName} \n touch. feel. exist.`;
                douyinHook = `别划走！今年最爱的高级感单品就它了`;
                visualNote = `极简桌面，阳光投射，产品静物微距`;
                shortScript = `【0-5s】手指抚过产品材质特写\n【5-20s】“${mainCopy.slice(0,45)}…”\n【20-30s】展示使用场景，结尾留白`;
            }
            else if (type === "用户情绪") {
                title = `“慢下来，也是一种能力”｜来自${bName}用户的100个瞬间`;
                mainCopy = `最近收到一条留言：“谢谢你，让我在忙碌里重新学会呼吸。”这就是${bName}存在的意义。我们不是在卖产品，而是在陪伴每一个想慢下来的灵魂。今天，你也给自己10分钟空白了吗？`;
                xhsTitle = `💌 收到了最治愈的留言｜品牌存在的意义有了答案`;
                igCaption = `"slow down is not weakness, it's power." — from our community. 🕊️`;
                douyinHook = `眼泪打转！一个品牌最珍贵的不是销售额，而是这些瞬间...`;
                visualNote = `用户实拍拼图 / 温暖手写字 / 日常碎片`;
                hashtags = `#${bName}用户故事 #情绪价值 #${tonePrimary}`;
            }
            else if (type === "生活方式") {
                title = `${tonePrimary}周末指南 | 找回身体的轻盈感`;
                mainCopy = `这个周末，不妨试试：关掉手机一小时，铺开瑜伽垫，或者只是简单冲一杯${industry.includes("咖啡")?"手冲咖啡":"花草茶"}。${bName}认为真正的奢侈不是物品，而是自由支配的时间。让生活回归节奏感。`;
                xhsTitle = `🌿 INFP会爱上的周末提案｜松弛感生活`;
                igCaption = `weekend reset. breathe. stretch. exist. 🧘🏻‍♀️\n#${bName}`;
                douyinHook = `周末别再无效休息了！跟我这样过真的能回血`;
                visualNote = `自然光影/亚麻服饰/木质调居家场景`;
                shortScript = `BGM轻柔钢琴，画面描述安静晨间日常，旁白：${mainCopy.slice(0,70)}`;
            }
            else if (type === "节气/热点") {
                title = `立秋｜身体也需要换季仪式感，${bName}陪你温柔过渡`;
                mainCopy = `季节更替时，身体总是最诚实的。${bName}准备了一份“换季感知清单”：慢呼吸、轻拉伸、一杯温润茶。顺应自然节奏，才是最高级的保养。`;
                xhsTitle = `🍂 立秋文案｜用温柔的方式，和夏天告别`;
                igCaption = `autumn whispers: slow down, tune in. 🍁\nembrace seasonal rhythm with ${bName}`;
                visualNote = `落叶/羊绒质感/暖光氛围`;
            }
            else {
                title = `让日常发光｜${bName}的生活方式提案`;
                mainCopy = `${spirit}。${bName}相信美和治愈不是宏大叙事，而是每一个微小选择。今天选择安静，选择呼吸，选择善待自己。这就是品牌想传递的${tonePrimary}能量。`;
                xhsTitle = `✨ 品牌理念太戳心 | 这才是女性需要的情绪价值`;
                igCaption = `choose softness. choose yourself. always. \n@${bName.replace(/\s/g,'')}`;
                douyinHook = `如果你最近很累，这个视频送给你🧘‍♀️`;
            }
            
            // 禁用词过滤（模拟二次检查，简单替换）
            if(forbiddenWords && forbiddenWords.length>0){
                const forbidArr = forbiddenWords.split(/[,，、 ]/);
                forbidArr.forEach(fw => {
                    if(fw.length>1){
                        const regex = new RegExp(fw, 'gi');
                        mainCopy = mainCopy.replace(regex, '••');
                        title = title.replace(regex, '');
                        if(xhsTitle) xhsTitle = xhsTitle.replace(regex, '');
                    }
                });
            }
            
            return {
                title: title || `#${bName}的${tonePrimary}日常`,
                mainCopy: mainCopy.substring(0, 280),
                xhsTitle: xhsTitle || title,
                xhsContent: mainCopy.substring(0, 200)+"...",
                igCaption: igCaption || mainCopy.substring(0, 120),
                igContent: mainCopy,
                douyinHook: douyinHook || `${title.slice(0,28)}...`,
                visualNote,
                shortScript: shortScript || `简短脚本：展示品牌氛围+金句${mainCopy.slice(0,40)}`,
                hashtags,
                tiktokTrend: `治愈慢动作+ ${tonePrimary}`
            };
        }
        
        // 渲染内容日历到右侧面板
        function renderContentCalendar(weeklyData, brandName, selectedPlatformsList) {
            const container = document.getElementById('contentOutput');
            if(!weeklyData || weeklyData.length===0){
                container.innerHTML = `<div class="text-center py-10 text-stone-400">生成内容失败，请重试</div>`;
                return;
            }
            const badgeSpan = document.getElementById('brandPreviewBadge');
            if(badgeSpan) badgeSpan.innerText = `🧘 ${brandName || "品牌"} · 人格已激活`;
            
            let html = `<div class="space-y-6 animate-fade-up">`;
            html += `<div class="text-sm text-stone-500 mb-2 flex justify-between"><span>🎯 平台适配: ${selectedPlatformsList.join(', ') || "全平台"}</span><span>📌 审美风格驱动 · ${weeklyData[0]?.emotion || "情绪结构"}</span></div>`;
            weeklyData.forEach((item, idx) => {
                // 展示适配版本片段
                let platformPreviewHtml = `<div class="mt-2 flex flex-wrap gap-2 text-xs">`;
                for(const [plat, text] of Object.entries(item.platformVersions)){
                    platformPreviewHtml += `<div class="bg-stone-50 rounded-lg p-2 border border-stone-100 flex-1 min-w-[130px]"><span class="font-medium text-stone-600">${plat}</span><p class="text-stone-500 line-clamp-3 mt-1 text-[11px] leading-relaxed">${text.substring(0,100)}${text.length>100?'…':''}</p></div>`;
                }
                platformPreviewHtml += `</div>`;
                
                html += `
                    <div class="border-b border-stone-100 pb-5 last:border-0">
                        <div class="flex items-center gap-2 flex-wrap mb-2">
                            <span class="bg-stone-100 text-stone-700 text-xs font-medium px-2 py-1 rounded-full">${item.day}</span>
                            <span class="text-stone-600 font-medium text-sm">${item.type}</span>
                            <span class="text-stone-400 text-xs">· ${item.emotion}</span>
                        </div>
                        <h4 class="font-semibold text-stone-800 text-base mb-1">${item.title}</h4>
                        <p class="text-stone-600 text-sm leading-relaxed">${item.mainCopy}</p>
                        <div class="mt-1 text-xs text-stone-400 flex flex-wrap gap-x-3">🏷️ ${item.hashtags}</div>
                        <div class="mt-2 text-xs text-stone-500 bg-stone-50/80 p-2 rounded-md inline-block">🎨 视觉: ${item.visualNote}</div>
                        ${item.script30s ? `<div class="mt-2 text-xs text-stone-500"><span class="font-medium">🎥 30s脚本片段:</span> ${item.script30s.substring(0,120)}</div>` : ''}
                        ${platformPreviewHtml}
                    </div>
                `;
            });
            html += `<div class="pt-4 text-center text-stone-400 text-xs border-t border-stone-100 mt-2">✨ 品牌内容中台 · 持续输出品牌感 | 每周自动更新 · 支持SaaS订阅</div>`;
            html += `</div>`;
            container.innerHTML = html;
        }
        
        // 表单提交事件
        const form = document.getElementById('brandForm');
        form.addEventListener('submit', (e) => {
            e.preventDefault();
            const brandName = document.getElementById('brandName').value.trim() || "未命名品牌";
            const industry = document.getElementById('industry').value;
            const philosophy = document.getElementById('philosophy').value;
            const tone = document.getElementById('tone').value.trim() || "松弛感、呼吸感";
            const aesthetic = document.getElementById('aesthetic').value.trim() || "极简治愈";
            const forbidden = document.getElementById('forbidden').value.trim();
            const selectedPlatforms = getSelectedPlatforms();
            
            // 构造品牌数据
            const brandData = {
                name: brandName,
                industry: industry,
                philosophy: philosophy,
                toneRaw: tone,
                aesthetic: aesthetic,
                forbidden: forbidden,
                selectedPlatforms: selectedPlatforms.length ? selectedPlatforms : ["小红书", "Instagram"]
            };
            // 模拟加载状态
            const outputDiv = document.getElementById('contentOutput');
            outputDiv.innerHTML = `<div class="flex justify-center items-center py-16"><div class="animate-pulse text-stone-400">✨ AI正在根据品牌人格生成内容矩阵...</div></div>`;
            
            setTimeout(() => {
                const weekly = generateWeeklyContent(brandData);
                renderContentCalendar(weekly, brandName, brandData.selectedPlatforms);
            }, 150);
        });
        
        // 初始化示范: 轻量默认填入疗愈品牌示例(让新用户感受审美)
        window.onload = () => {
            const defaultBrand = document.getElementById('brandName');
            if(defaultBrand && !defaultBrand.value){
                defaultBrand.value = "屿野疗愈所";
                document.getElementById('industry').value = "疗愈/身心灵";
                document.getElementById('philosophy').value = "慢下来，也是一种能力。在呼吸之间，恢复与自我的连接。";
                document.getElementById('tone').value = "松弛感、温暖、诗意、自然";
                document.getElementById('aesthetic').value = "侘寂风 / 大地色系 / 手作感";
                document.getElementById('forbidden').value = "焦虑、紧迫、立即购买";
                // 勾选小红书与instagram
                const platChecks = document.querySelectorAll('input[type="checkbox"]');
                platChecks.forEach(cb => { if(cb.value === "小红书" || cb.value === "Instagram") cb.checked = true; else if(cb.value === "抖音") cb.checked = true; });
            }
        };
    </script>
</body>
</html># writing-all-skill
