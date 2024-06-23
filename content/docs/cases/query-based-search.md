---
weight: 67
title: "Copilotで英語圏の情報を収集する"
description: "上手なWeb検索"
icon: "article"
date: "2024-01-30T15:39:50+09:00"
lastmod: "2024-01-30T15:39:50+09:00"
draft: false
toc: true
---

Microsoftの蒲生さんがTwitterで共有されたテクニックです。

{{< table "table-responsive" >}}
| 日時 | このページで使用した生成AI | 
|----------|--------------|
| 2024/1/30 | Copilot(GPT-4) |
{{< /table >}}

```
プロンプトエンジニアリングガイドとは何か。
英語で検索クエリを作成し、回答は日本語で出力して
```
<br>

![英語でクエリを作成](images/query-based-search.png)

<br>

{{% alert icon="🤖" context="success" %}}
プロンプトエンジニアリングガイドは、大規模な言語モデル（GPTモデルとも呼ばれる）からより良い結果を得るための戦略と戦術を共有するガイドです¹。これは、マシン学習モデルが正確な出力を生成するように導く高品質なプロンプトを設計することを含みます³⁵。

以下に、より良い結果を得るためのいくつかの戦略を示します¹：
- **明確な指示を書く**：モデルはあなたの心を読むことはできません。出力が長すぎる場合は、簡潔な返答を求めます。出力が単純すぎる場合は、専門レベルの文章を求めます。フォーマットが気に入らない場合は、見たいフォーマットを示します。モデルがあなたが何を望んでいるかを推測する必要が少なければ少ないほど、あなたが望むものを得る可能性が高くなります。
- **複雑なタスクをより単純なサブタスクに分割する**：ソフトウェアエンジニアリングで複雑なシステムを一連のモジュラーコンポーネントに分解するのが良い実践であるのと同様に、言語モデルに提出されるタスクについても同じことが言えます。複雑なタスクは、より単純なタスクよりもエラー率が高い傾向があります。さらに、複雑なタスクは、初期のタスクの出力を使用して後のタスクの入力を構築するような、より単純なタスクのワークフローとして再定義できることがよくあります。
- **モデルに「考える」時間を与える**：17と28を掛けるように求められた場合、あなたはすぐに答えを知らないかもしれませんが、時間をかけて答えを出すことができます。同様に、モデルは、すぐに答えを出そうとすると、より多くの推論エラーを犯す傾向があります。答えの前に「思考の連鎖」を求めることで、モデルはより確実に正しい答えにたどり着くための推論を行うことができます。

これらの方法は、組み合わせて使用することで効果を発揮することがあります¹。また、これらの方法は、特定のタスクに最適な方法を見つけるための実験を奨励しています¹。⁴でも日本語での試用例が紹介されています。²では、DAIR.AIによるプロンプトエンジニアリングガイドのプロジェクトが紹介されており、研究者や実践者にプロンプトエンジニアリングについて教育することを目指しています。

ソース: Bing との会話 2024/1/30  
(1) Prompt engineering - OpenAI API. https://platform.openai.com/docs/guides/prompt-engineering/prompt-engineering.  
(2) What Is Prompt Engineering? Definition and best practices .... https://www.educative.io/blog/what-is-prompt-engineering.  
(3) What is prompt engineering? | IBM. https://www.ibm.com/topics/prompt-engineering.  
(4) OpenAIのPrompt Engineering Guideでより良い結果を得る .... https://zenn.dev/zuma_lab/articles/openai-prompt-engineering-guide.  
(5) About | Prompt Engineering Guide. https://www.promptingguide.ai/about.  
{{% /alert %}}


```
プロンプトエンジニアリングガイドを提供しているWebページを10個挙げて。
英語で検索クエリを作成し、回答は日本語で出力して
```

今回のクエリは**Websites providing the Prompt Engineering Guide**です。

{{% alert icon="🤖" context="success" %}}
以下に、プロンプトエンジニアリングガイドを提供しているウェブページをいくつか紹介します：
1. [OpenAI API](^1^)：OpenAIの公式APIドキュメント内にあるプロンプトエンジニアリングガイドです。大規模な言語モデルからより良い結果を得るための戦略と戦術を共有しています¹。
2. [Gihyo.jp](^2^)：DAIR.AIが公開しているプロンプトエンジニアリングガイドの日本語訳が公開されています²。
3. [Zenn.dev](^3^)：OpenAIのプロンプトエンジニアリングガイドを日本語で試したり、自分なりに応用して実践してみる記事が掲載されています³。

ただし、現時点では検索結果から得られたウェブページは3つだけです。他のウェブページについては、具体的なウェブサイト名やURLが必要な場合は、それらの情報を提供していただければと思います。それにより、より具体的な検索を行うことが可能となります。ご理解いただけますと幸いです。¹²³

ソース: Bing との会話 2024/1/30  
(1) Prompt engineering - OpenAI API. https://platform.openai.com/docs/guides/prompt-engineering/prompt-engineering.  
(2) Prompt engineering - OpenAI API. https://platform.openai.com/docs/guides/prompt-engineering/prompt-engineering.  
(3) 「Prompt Engineering Guide」の日本語訳が公式サイトにマージ .... https://gihyo.jp/article/2023/04/prompt-engineering-guide.  
(4) 「Prompt Engineering Guide」の日本語訳が公式サイトにマージ .... https://gihyo.jp/article/2023/04/prompt-engineering-guide.  
(5) OpenAIのPrompt Engineering Guideでより良い結果を得る .... https://zenn.dev/zuma_lab/articles/openai-prompt-engineering-guide.  
(6) OpenAIのPrompt Engineering Guideでより良い結果を得る .... https://zenn.dev/zuma_lab/articles/openai-prompt-engineering-guide.  
{{% /alert %}}



<!-- <script>
        // CSSとアイコンのリンクを追加する関数
        function addStylesheet(href) {
            let link = document.createElement('link');
            link.href = href;
            link.rel = 'stylesheet';
            document.head.appendChild(link);
        }

        // トグルボタンを作成し、追加する関数
        function createToggleButton() {
            const toggleBtn = document.createElement('div');
            toggleBtn.id = 'chatbot-toggle_button';
            const anchor = document.createElement('a');
            anchor.id = 'chat-button';
            anchor.href = '#';
            anchor.addEventListener('click', toggleChatbox);
            const img = document.createElement('img');
            img.src = 'https://firebasestorage.googleapis.com/v0/b/mabo-f1cc7.appspot.com/o/chaticon.png?alt=media&token=1777070f-a83c-403d-8c83-f387f68ecd52';
            img.width = '100';
            img.height = '100';
            anchor.appendChild(img);
            toggleBtn.appendChild(anchor);
            document.body.appendChild(toggleBtn);
        }

        // チャットボックスのヘッダーを作成する関数
        function createChatboxHeader() {
            const header = document.createElement('div');
            header.id = 'chatbot-header';
            header.style.background = '#4169e1';
            const logo = document.createElement('div');
            logo.id = 'chatbot-logo';
            logo.innerText = '「プロンプトガイドさん」にプロンプトを入力する';
            // const closeIcon = document.createElement('i');
            // closeIcon.id = 'chatbot-close-icon';
            // closeIcon.className = 'material-icons material-symbols-outlined waves-light';
            // closeIcon.innerText = 'close';
            const closeIcon = document.createElement('img');
            closeIcon.id = 'chatbot-close-icon';
            closeIcon.src = 'images/imagetext.png'; // 閉じるアイコンの画像パスを指定
            closeIcon.alt = 'Close';
            closeIcon.addEventListener('click', toggleChatbox);
            header.appendChild(logo);
            header.appendChild(closeIcon);
            return header;
        }
        #chatbot-close-icon {
            width: 24px;
            height: 24px;
            cursor: pointer;
        }

        // チャットボックスを作成し、追加する関数
        function createChatbox() {
            const chatbox = document.createElement('div');
            chatbox.id = 'chatbot';
            chatbox.style.display = 'none';

            const header = createChatboxHeader();
            const body = document.createElement('div');
            body.id = 'chatbot-body';
            const iframe = document.createElement('iframe');
            iframe.id = 'inline-frame';
            iframe.width = '100%';
            iframe.height = '100%';
            iframe.dataSrc = 'https://miibo.jp/chat/61063623-1709-4167-b956-c6202d60d56718edb5cabb015?name=%E3%83%97%E3%83%AD%E3%83%B3%E3%83%97%E3%83%88%E3%82%AC%E3%82%A4%E3%83%89%E3%81%95%E3%82%93';
            iframe.scrolling = 'no';
            iframe.frameBorder = 'no';
            body.appendChild(iframe);
            chatbox.appendChild(header);
            chatbox.appendChild(body);
            document.body.appendChild(chatbox);
        }

        // チャットボックスの表示/非表示を切り替える関数
        function toggleChatbox(utterance, ...states) {
            var chatbox = document.getElementById('chatbot');
            var iframe = document.getElementById('inline-frame');

            // ここでイベントオブジェクトではなく、文字列または未定義の値が渡されることを確認します。
            if (typeof utterance !== 'string') {
                utterance = null;
            }

            if (chatbox.style.display === 'none' || utterance) {
                chatbox.style.display = 'block';
                var src = 'https://miibo.jp/chat/61063623-1709-4167-b956-c6202d60d56718edb5cabb015?name=%E3%83%97%E3%83%AD%E3%83%B3%E3%83%97%E3%83%88%E3%82%AC%E3%82%A4%E3%83%89%E3%81%95%E3%82%93';
                // 可変引数からクエリパラメータを生成
                states.forEach(state => {
                    if (state.key && state.value) {
                        src += `${encodeURIComponent(state.key)}=${encodeURIComponent(state.value)}`;
                    }
                });

                // 以下の条件を追加して、再読み込みの必要性をチェック
                if (!iframeLoaded || (utterance && lastUtterance !== utterance)) {
                    if (utterance) {
                        src += "&utterance=" + encodeURIComponent(utterance);
                    }
                    iframe.src = src;
                    iframeLoaded = true;
                    lastUtterance = utterance;
                }
            } else {
                chatbox.style.display = 'none';
            }
        }
        // イベントリスナーを設定する関数
        function setupEventListeners() {
            document.querySelectorAll('.chatButton').forEach(button => {
                button.addEventListener('click', event => {
                    event.preventDefault();
                    const utterance = button.getAttribute('data-utterance');
                    const statesData = button.getAttribute('data-states');
                    let states = [];
                    try {
                        // JSON 形式の文字列をオブジェクトに変換
                        const statesObj = JSON.parse(statesData);
                        // オブジェクトから key-value ペアの配列を生成
                        states = Object.keys(statesObj).map(key => ({ key, value: statesObj[key] }));
                    } catch (e) {
                        console.error("Error parsing states data", e);
                    }

                    toggleChatbox(utterance, ...states);
                });
            });

            // ここでイベントオブジェクトを直接渡さないようにします。
            document.getElementById('chat-toggle').addEventListener('click', event => {
                event.preventDefault();
                toggleChatbox();
            });

            document.getElementById('chatbot-close-icon').addEventListener('click', () => {
                toggleChatbox();
            });
        }

        // メイン実行部
        addStylesheet('https://fonts.googleapis.com/icon?family=Material+Icons');
        addStylesheet('https://miibo.jp/chat3.css');
        createToggleButton();
        createChatbox();
        setupEventListeners();

        var iframeLoaded = false; // iframeがロードされたかどうかを追跡するフラグ
        var lastUtterance = ""; // 最後に発話した内容を追跡するフラグ
    </script> -->
