 <!DOCTYPE html>
<html lang="zh">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>音乐风格与元标签指南</title>
    <style>
        body {
            font-family: "Microsoft YaHei", sans-serif;
            margin: 0;
            padding: 0;
            background: url('https://www.rollingstone.com/wp-content/uploads/2019/12/RapAlbums.jpg?resize=1800') no-repeat center center fixed;
            background-size: cover;
            color: #fff;
            overflow-x: hidden;
        }

        /* 动态模糊背景 */
        body::before {
            content: "";
            position: fixed;
            top: 0; left: 0;
            width: 100%; height: 100%;
            backdrop-filter: blur(8px);
            z-index: -1;
        }

        h1, h2, h3 {
            color: #ffd700;
            text-shadow: 1px 1px 3px rgba(0,0,0,0.7);
        }

        h1 {
            text-align: center;
            margin-top: 40px;
            font-size: 3em;
        }

        section {
            background: rgba(0, 0, 0, 0.5);
            border-radius: 10px;
            padding: 25px 30px;
            margin: 40px auto;
            max-width: 900px;
            transition: transform 0.6s, box-shadow 0.6s, background 0.6s;
        }

        /* 高亮效果 */
        section.active {
            transform: scale(1.03);
            box-shadow: 0 10px 30px rgba(0,0,0,0.6);
            background: rgba(0, 0, 0, 0.8);
        }

        ul {
            list-style-type: disc;
            margin-left: 20px;
        }

        code {
            background: rgba(255, 255, 255, 0.2);
            padding: 2px 6px;
            border-radius: 4px;
        }
    </style>
</head>
<body>

    <h1>音乐风格与元标签指南</h1>

    <section>
        <h2>1. 什么是元标签（Meta Tags）</h2>
        <p>在音乐生成 AI 中，<strong>元标签（Meta Tags）</strong> 是一类特殊的指令或关键词，用于指导 AI 在音乐或音频生成过程中：</p>
        <ul>
            <li>结构化歌曲内容</li>
            <li>指定音乐风格或流派</li>
            <li>引导音效、氛围或演唱表达</li>
            <li>调整节奏、表现方式、动态效果</li>
        </ul>
        <p>这些标签一般用" <code>方括号</code>" 或直接英文单词表示，它们不会在输出中明显表达，而是作为生成的“指令”被模型理解和执行。</p>
    </section>

    <section>
        <h2>2. 环境与音效相关的元标签</h2>
        <h3>音效类</h3>
        <ul>
            <li>Barking — 狗叫声</li>
            <li>Beeping — 哔哔声</li>
            <li>Bell dings — 铃声</li>
            <li>Birds chirping — 鸟鸣</li>
            <li>Bleep — 高音哔声</li>
            <li>Cheering — 欢呼</li>
            <li>Cheers and applause — 欢呼喝彩和掌声</li>
            <li>Chuckles — 轻笑</li>
            <li>Clapping — 鼓掌</li>
            <li>Cough — 咳嗽</li>
            <li>Groaning — 呻吟</li>
            <li>Phone ringing — 电话铃声</li>
            <li>Ringing — 一般铃声</li>
            <li>Screams — 尖叫</li>
            <li>Sighs — 叹息</li>
            <li>Squawking — 嘎嘎叫</li>
            <li>Whispers — 耳语</li>
            <li>Whistling — 吹口哨声</li>
        </ul>

        <h3>声音表达类</h3>
        <ul>
            <li>Announcer — 播音员</li>
            <li>Audience laughing — 观众笑声</li>
            <li>Female narrator — 女性解说</li>
            <li>Giggling — 咯咯笑</li>
            <li>Man — 男性</li>
            <li>Reporter — 记者</li>
            <li>Woman — 女性</li>
            <li>Boy — 男孩</li>
            <li>Girl — 女孩</li>
        </ul>

        <h3>静态效果类</h3>
        <ul>
            <li>Applause — 掌声</li>
            <li>Clears throat — 清嗓</li>
            <li>Censored — 被审查的静音</li>
            <li>Silence — 完全无声</li>
        </ul>
    </section>

    <section>
        <h2>3. 音乐结构和风格标签</h2>

        <h3>3.1 歌曲结构标签</h3>
        <ul>
            <li>Chorus — 合唱部分</li>
            <li>Intro — 前奏</li>
            <li>Outro — 结尾</li>
            <li>Verse — 主歌段</li>
        </ul>
    </section>

    <section>
        <h2>4. 音乐风格与流派标签</h2>
        <ul>
            <li>Acoustic — 原声风格</li>
            <li>African — 非洲音乐风格</li>
            <li>Alternative metal — 另类金属</li>
            <li>Alternative pop — 另类流行</li>
            <li>Ambient — 环境音乐</li>
            <li>Atlanta rap — 亚特兰大说唱风格</li>
            <li>Ballad — 抒情歌曲</li>
            <li>Baroque — 巴洛克风格</li>
            <li>Blues — 蓝调</li>
            <li>Boom bap — 嘻哈次风格</li>
            <li>Cello — 大提琴特色音乐</li>
            <li>Chill — 轻松氛围音乐</li>
            <li>Christian & Gospel — 基督教与福音音乐</li>
            <li>Christmas — 圣诞主题音乐</li>
            <li>Country & Americana — 乡村及美国民谣</li>
            <li>Dance & Electronic — 舞曲与电子</li>
            <li>Drums — 以鼓为中心的音乐</li>
            <li>EDM — 电子舞曲</li>
            <li>Girl group — 女子组合风</li>
            <li>Gospel — 福音音乐</li>
            <li>Hardcore rap — 激进嘻哈</li>
            <li>Heavy metal — 重金属</li>
            <li>Hip hop — 嘻哈音乐</li>
            <li>Indie — 独立音乐</li>
            <li>Indie rock — 独立摇滚</li>
            <li>J-pop — 日本流行乐</li>
            <li>Jazz — 爵士乐</li>
            <li>K-pop — 韩国流行音乐</li>
            <li>Lo‑fi — 低保真音乐</li>
            <li>Orchestra — 管弦乐特色</li>
            <li>Party — 派对风格</li>
            <li>Piano — 钢琴音乐特色</li>
            <li>Pop — 流行音乐</li>
            <li>Pop‑Rock — 流行摇滚</li>
            <li>Post‑Hardcore — 后硬核</li>
            <li>Punk Rock — 朋克摇滚</li>
            <li>R&B — 节奏蓝调</li>
            <li>R&B & Soul — 蓝调与灵魂</li>
            <li>Rap — 说唱</li>
            <li>Reggae — 雷鬼</li>
            <li>Rock — 摇滚</li>
            <li>Romantic — 浪漫风</li>
            <li>Soul — 灵魂音乐</li>
            <li>Synth — 合成器电子</li>
            <li>Synth pop — 合成器流行</li>
            <li>Techno — 技术舞曲</li>
        </ul>
    </section>

    <section>
        <h2>使用说明</h2>
        <ul>
            <li>定义音乐元标签是什么（解释作用与用途）</li>
            <li>展示各种音效/声音表达标签（环境增强与模拟）</li>
            <li>介绍音乐结构标签（歌曲组成和段落结构）</li>
            <li>列出音乐风格与流派标签（从流行到电子、古典等）</li>
            <li>说明示例用法（如如何结合多个标签生成特定风格音乐）</li>
        </ul>
    </section>

    <script>
        // 滚动高亮
        const sections = document.querySelectorAll('section');
        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if(entry.isIntersecting){
                    entry.target.classList.add('active');
                } else {
                    entry.target.classList.remove('active');
                }
            });
        }, {threshold: 0.5});

        sections.forEach(section => observer.observe(section));
    </script>

</body>
</html>
