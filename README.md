<!DOCTYPE html>
<html lang="ja">
<head>
    <meta charset="UTF-8">
    <title>バレエタイプ診断16</title>
    <style>
        /* 画面全体の共通設定 */
        body {
            font-family: sans-serif;
            max-width: 600px;
            margin: 0 auto; /* 左右のマージンを自動にして、コンテンツ全体を中央寄せ */
            padding: 40px 20px;
            background-color: #F5FFFA;
        }

        /* 質問画面と結果画面を中央寄せにする設定 */
        #quiz-screen, #result-screen {
            display: flex;
            flex-direction: column; /* 中の要素を上から下に縦に並べる */
            align-items: center;    /* 縦に並んだ要素を 「左右中央」 に寄せる */
            text-align: center;     /* テキスト事態も中央揃えにする */
        }
        /* 質問１つひとつのボックス */
        .question {
            width: 100%; /* 横幅いっぱいに広げる */
            margin-bottom: 30px;
            border-bottom: 1px solid #eee;
            padding-bottom: 20px;
            text-align: left; /* ★質問文と選択肢は左詰め */
        }

        /* ラジオボタンの選択肢の間隔を少しあける */
        .question label {
            margin: 0 15px;
            cursor: pointer;
            display: inline-block;
        }

        /* 診断するボタン・もう一度ボタンのデザイン */
        button {
            margin-top: 20px;
            padding: 12px 40px; /* 上下左右の余白を広げて押しやすく */
            font-size: 18px; /* 文字を少し大きく */
            font-weight: bold;
            background-color: #00BFFF;
            color: white;
            border: none;
            border-radius: 25px; /* ボタンの角を丸くして今風のデザインに */
            cursor: pointer;
            transition: background 0.3s; /* ホバー時のアニメーション */
        }

        /* ボタンにマウスを乗せたときの色 */
        button:hover {
            background-color: #d35400;
        }

        /* １行目：「あなたのタイプは：」のスタイル */
        .result-label {
            font-size: 16px;
            color: #666;
            margin-bottom: 8px
        }

        /* ２行目：「○○タイプ」のスタイル */
        .result-type-name {
            font-size: 32px;
            font-weight: bold;
            color: #e67e22;
            margin-bottom: 8px; /* ３行目との間隔を少し調整 */
            letter-spacing: 1px;
        }

        /* ３行目：「英字４文字」のスタイル */
        .result-type-code {
            font-size: 18px;
            font-weight: bold;
            color: #999;
            margin-bottom: 20px;
            letter-spacing: 2px;
        }

        /* 解説テキストの角丸枠のスタイル */
        #result-description-box {
            margin-top: 25px;
            padding: 20px;
            width: 100%;
            box-sizing: border-box;
            background-color: #ffffff;
            border: 1px solid #e0e0e0;
            border-radius: 15px;

            /* 上下中央揃え・左右左揃えのための設定 */
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: flex-start;
            text-align: left;

            /* イタリック（斜体）とフォントの調整 */
            font-style: italic;
            font-size: 15px;
            line-height: 1.6;
            color: #444444;
        }

        /* 要素を非表示にするためのクラス */
        .hidden {
            display: none !important;
        }
    </style>
</head>
<body>

<div id="quiz-screen">
    <h1>バレエタイプ診断16</h1>
    
    <div class="question">
        <p>01.誰もが一度は耳にしたことがあるような「超王道の定番名作」を鑑賞するのが好きだ。</p>
        <label><input type="radio" name="q1" value="T"> はい</label>
        <label><input type="radio" name="q1" value="I"> いいえ</label>
    </div>

    <div class="question">
        <p>02.舞台やライブでは、静かに座って物語を追うものよりも、一瞬の超絶技巧や派手な演出、その場の「ライブ感の熱狂」にアドレナリンが出る作品が好きだ。</p>
        <label><input type="radio" name="q2" value="E"> はい</label>
        <label><input type="radio" name="q2" value="D"> いいえ</label>
    </div>
    
    <div class="question">
        <p>03.アクションシーンを見るとテンションが上がる。</p>
        <label><input type="radio" name="q3" value="P"> はい</label>
        <label><input type="radio" name="q3" value="G"> いいえ</label>
    </div>

    <div class="question">
        <p>04.アニメやドラマは毎週１話ずつ考察を楽しんだり、何日もかけてじっくり味わうのが好きだ。</p>
        <label><input type="radio" name="q4" value="S"> はい</label>
        <label><input type="radio" name="q4" value="C"> いいえ</label>
    </div>

    <div class="question">
        <p>05.お金は貯金で眠らせるよりも、自己投資や投資信託といった攻めの資産運用に回したい。</p>
        <label><input type="radio" name="q5" value="I"> はい</label>
        <label><input type="radio" name="q5" value="T"> いいえ</label>
    </div>

    <div class="question">
        <p>06.物語はハッピーエンドよりも、バッドエンドやビターエンドの方が好きだ。</p>
        <label><input type="radio" name="q6" value="D"> はい</label>
        <label><input type="radio" name="q6" value="E"> いいえ</label>
    </div>

    <div class="question">
        <p>07.周囲から「仕事が早いね」と言われるよりも、「仕事が丁寧で正確だね」と言われる方が嬉しい。</p>
        <label><input type="radio" name="q7" value="G"> はい</label>
        <label><input type="radio" name="q7" value="P"> いいえ</label>
    </div>

    <div class="question">
        <p>08.イントロや間奏が長い曲よりも、サビから始まったりキャッチーなメロディが繰り返される曲に惹かれる。</p>
        <label><input type="radio" name="q8" value="C"> はい</label>
        <label><input type="radio" name="q8" value="S"> いいえ</label>
    </div>

    <div class="question">
        <p>09.休日の予定は、当日になって決めるよりも、あらかじめ行く場所や時間をスケジュールしておきたい。</p>
        <label><input type="radio" name="q9" value="T"> はい</label>
        <label><input type="radio" name="q9" value="I"> いいえ</label>
    </div>

    <div class="question">
        <p>10.「人生、楽しまなきゃ損だ」という言葉に強く共感する。</p>
        <label><input type="radio" name="q10" value="E"> はい</label>
        <label><input type="radio" name="q10" value="D"> いいえ</label>
    </div>
    
    <div class="question">
        <p>11.洗練されたスマートさよりも、泥臭くても全力で限界に挑んでいる姿にこそ本物の美しさを感じる。</p>
        <label><input type="radio" name="q11" value="P"> はい</label>
        <label><input type="radio" name="q11" value="G"> いいえ</label>
    </div>

    <div class="question">
        <p>12.話をするとき、結論だけをズバッと言われるよりも、そこに至るまでの経緯や背景も一緒に聞きたい。</p>
        <label><input type="radio" name="q12" value="S"> はい</label>
        <label><input type="radio" name="q12" value="C"> いいえ</label>
    </div>

    <div class="question">
        <p>13.洋服やヘアスタイルは、「みんなと同じ」を避け、どこかに自分らしいエッジや個性を入れたい。</p>
        <label><input type="radio" name="q13" value="I"> はい</label>
        <label><input type="radio" name="q13" value="T"> いいえ</label>
    </div>

    <div class="question">
        <p>14.激しい葛藤やドロドロとした愛憎劇を繰り広げているシーンほど、目が離せない。</p>
        <label><input type="radio" name="q14" value="D"> はい</label>
        <label><input type="radio" name="q14" value="E"> いいえ</label>
    </div>

    <div class="question">
        <p>15.何事も、涼しい顔でそつなくこなす姿に憧れる。</p>
        <label><input type="radio" name="q15" value="G"> はい</label>
        <label><input type="radio" name="q15" value="P"> いいえ</label>
    </div>

    <div class="question">
        <p>16.日常生活の中で「タイムパフォーマンス」を意識して行動することが多い。</p>
        <label><input type="radio" name="q16" value="C"> はい</label>
        <label><input type="radio" name="q16" value="S"> いいえ</label>
    </div>

    <div class="question">
        <p>17.物事を進めるときは、独自のアイデアを試すよりも、過去の成功例やマニュアルに従う方が確実で好きだ。</p>
        <label><input type="radio" name="q17" value="T"> はい</label>
        <label><input type="radio" name="q17" value="I"> いいえ</label>
    </div>

    <div class="question">
        <p>18.小難しいものよりも、直観的に楽しめるものをつい選びがちだ。</p>
        <label><input type="radio" name="q18" value="E"> はい</label>
        <label><input type="radio" name="q18" value="D"> いいえ</label>
    </div>
    
    <div class="question">
        <p>19.デートで行くなら、静かで落ち着いたカフェよりもお祭りのような賑わった場所の方がいい。</p>
        <label><input type="radio" name="q19" value="P"> はい</label>
        <label><input type="radio" name="q19" value="G"> いいえ</label>
    </div>

    <div class="question">
        <p>20.「とりあえずやってみる」という言葉は、見通しが甘い気がして、自分からはあまり使いたくない。</p>
        <label><input type="radio" name="q20" value="S"> はい</label>
        <label><input type="radio" name="q20" value="C"> いいえ</label>
    </div>

    <div class="question">
        <p>21.何事も「現状維持」ではなく、常に変化やアップデートを繰り返したい。</p>
        <label><input type="radio" name="q21" value="I"> はい</label>
        <label><input type="radio" name="q21" value="T"> いいえ</label>
    </div>

    <div class="question">
        <p>22.苦しみや挫折、葛藤こそが、人間を最も成長させ、深みを与えてくれると思う。</p>
        <label><input type="radio" name="q22" value="D"> はい</label>
        <label><input type="radio" name="q22" value="E"> いいえ</label>
    </div>

    <div class="question">
        <p>23.スマートな身のこなしや、品格のある佇まいに憧れる。</p>
        <label><input type="radio" name="q23" value="G"> はい</label>
        <label><input type="radio" name="q23" value="P"> いいえ</label>
    </div>

    <div class="question">
        <p>24.アプリの通知バッジは、見つけたらすぐに既読にして消したい。</p>
        <label><input type="radio" name="q24" value="C"> はい</label>
        <label><input type="radio" name="q24" value="S"> いいえ</label>
    </div>

    <div class="question">
        <p>25.物の価値を決める上で、「歴史の長さ」や「受け継がれてきた伝統」は非常に重要な要素だと思う。</p>
        <label><input type="radio" name="q25" value="T"> はい</label>
        <label><input type="radio" name="q25" value="I"> いいえ</label>
    </div>

    <div class="question">
        <p>26.努力は必ず報われると思う。</p>
        <label><input type="radio" name="q26" value="E"> はい</label>
        <label><input type="radio" name="q26" value="D"> いいえ</label>
    </div>
    
    <div class="question">
        <p>27.周りの人たちが盛り上がっている場面では、自然と自分も感情が昂る。</p>
        <label><input type="radio" name="q27" value="P"> はい</label>
        <label><input type="radio" name="q27" value="G"> いいえ</label>
    </div>

    <div class="question">
        <p>28.交友関係やコンテンツの楽しみ方は、「広く浅く」よりも「狭く深く」を求めるタイプだ。</p>
        <label><input type="radio" name="q28" value="S"> はい</label>
        <label><input type="radio" name="q28" value="C"> いいえ</label>
    </div>

    <button onclick="calculateResult()">診断する</button>
</div> <div id="result-screen" class="hidden">
    <h1>診断結果</h1>
    <div id="result"></div>

    <br><br>
    <button onclick="location.reload()" style="background-color:  #bbb;">もう一度診断する</button>
</div>

    <script>
        // 16タイプごとの「考案済みワード」の定義
        const typeNames = {
            "TEPS": "ドン・キホーテ タイプ",
            "TEPC": "サタネラ タイプ",
            "IEPS": "ピーターパン タイプ",
            "IEPC": "タリスマン タイプ",
            "TEGS": "くるみ割り人形 タイプ",
            "TEGC": "ゼンツァーノ タイプ",
            "IEGS": "シンデレラ タイプ",
            "IEGC": "エチュード タイプ",
            "TDPS": "パリの炎 タイプ",
            "TDPC": "シェヘラザード タイプ",
            "IDPS": "ザ・カブキ タイプ",
            "IDPC": "カルメン タイプ",
            "TDGS": "ジゼル タイプ",
            "TDGC": "ラ・シルフィード タイプ",
            "IDGS": "マノン タイプ",
            "IDGC": "セレナーデ タイプ"
        };

        // 16パターンごとの「解説テキスト」
        const typeDescriptions = {
            "TEPS": "。",
            "TEPC": "。",
            "IEPS": "。",
            "IEPC": "。",
            "TEGS": "。",
            "TEGC": "。",
            "IEGS": "。",
            "IEGC": "。",
            "TDPS": "。",
            "TDPC": "。",
            "IDPS": "。",
            "IDPC": "。",
            "TDGS": "。",
            "TDGC": "。",
            "IDGS": "。",
            "IDGC": "。"
        };

        function calculateResult() {
            let scores = { T: 0, I: 0, E: 0, D: 0, P: 0, G: 0, S: 0, C: 0 };
            
            // 選択された回答をチェック
            const answers = document.querySelectorAll('input[type="radio"]:checked');
            answers.forEach((ans) => {
                scores[ans.value]++;
            });

            // 4つの指標を判定
            let type = "";
            type += scores.T > scores.I ? "T" : "I";
            type += scores.E > scores.D ? "E" : "D";
            type += scores.P > scores.G ? "P" : "G";
            type += scores.S > scores.C ? "S" : "C";

            // 16パターンの辞書から、該当する日本語ワードを取得
            const JapaneseTypeName = typeNames[type];

            // HTML構造を３行に分けて流し込み
            document.getElementById("result").innerHTML = `
                <div class="result-label">あなたのタイプは：</div>
                <div class="result-type-name">${JapaneseTypeName}</div>
                <div class="result-type-code">（${type}）</div>
            `;

            // 割り出されたタイプに応じた解説テキストを枠の中に流し込む
            const descriptionBox = document.getElementById("result-description-box");
            if (descriptionBox) {
                descriptionBox.innerText = typeDescriptions[type];
            }

            // 画面の切り替え処理
            // 1. 質問画面に 「hidden」 クラスをつけて隠す
            document.getElementById("quiz-screen").classList.add("hidden");

            // 2. 結果画面から 「hidden」 クラスを取り除いて表示する
            document.getElementById("result-screen").classList.remove("hidden");

            // 3. 画面を一番上までスクロールさせる
            window.scrollTo(0,0);
        }
    </script>
</body>
</html>
