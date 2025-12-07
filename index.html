import streamlit as st

# =========================
# ページ設定
# =========================
st.set_page_config(
    page_title="災害対策セルフチェック診断",
    page_icon="⛑️",
    layout="centered",
)

# =========================
# CSS（背景クリーム色・ボタンカラー完全反映版）
# =========================
st.markdown("""
<style>
.stApp {
    background-color: #FFF8E7;
    font-family: -apple-system, BlinkMacSystemFont, "Helvetica Neue", sans-serif;
}

/* 質問カード */
.question-card {
    background-color: white;
    padding: 1.4rem 1.6rem;
    border-radius: 1rem;
    box-shadow: 0 2px 8px rgba(0,0,0,0.08);
    margin-bottom: 1.3rem;
}

/* はい（赤） */
.yes-btn {
    background-color: #FF6B6B !important;
    color: white !important;
    border: none;
    padding: 0.7rem 1.4rem;
    border-radius: 999px;
    font-weight: 600;
    width: 100%;
}
.yes-btn:hover {
    opacity: 0.9;
}

/* いいえ（緑） */
.no-btn {
    background-color: #4CAF50 !important;
    color: white !important;
    border: none;
    padding: 0.7rem 1.4rem;
    border-radius: 999px;
    font-weight: 600;
    width: 100%;
}
.no-btn:hover {
    opacity: 0.9;
}

/* ナビゲーション（前へ・トップへ） */
.nav-btn {
    background-color: #EEEEEE !important;
    border: 1px solid #CCCCCC !important;
    color: #333333 !important;
    padding: 0.6rem 1.2rem;
    border-radius: 999px;
    font-weight: 500;
}
.nav-btn:hover {
    background-color: #E0E0E0 !important;
}
</style>
""", unsafe_allow_html=True)

# =========================
# 質問データ（ここに追加していく）
# =========================
QUESTIONS = [
    {"id": 1, "genre": "goods", "label": "防災グッズ", "text": "非常持ち出し袋を置いていますか？"},
    {"id": 2, "genre": "goods", "label": "防災グッズ", "text": "中身を年1回以上見直していますか？"},
    {"id": 3, "genre": "evac",  "label": "避難生活", "text": "避難所の場所を把握していますか？"},
    {"id": 4, "genre": "evac",  "label": "避難生活", "text": "家族との連絡手段を決めていますか？"},
]

# =========================
# セッション初期化
# =========================
if "page" not in st.session_state:
    st.session_state.page = "home"

if "i" not in st.session_state:
    st.session_state.i = 0

if "ans" not in st.session_state:
    st.session_state.ans = {}

# =========================
# ページ遷移管理
# =========================
def go_home():
    st.session_state.page = "home"
    st.session_state.i = 0
    st.session_state.ans = {}
    st.rerun()

def start_quiz():
    st.session_state.page = "quiz"
    st.session_state.i = 0
    st.session_state.ans = {}
    st.rerun()

def choose_answer(answer: bool):
    """はい/いいえを押した瞬間に次へ遷移"""
    qid = QUESTIONS[st.session_state.i]["id"]
    st.session_state.ans[qid] = answer

    # 最終問題なら結果へ
    if st.session_state.i == len(QUESTIONS) - 1:
        st.session_state.page = "result"
    else:
        st.session_state.i += 1

    st.rerun()

def go_prev():
    if st.session_state.i > 0:
        st.session_state.i -= 1
        st.rerun()


# =========================
# ホーム画面
# =========================
def show_home():
    st.title("災害対策セルフチェック診断 ⛑️")
    st.subheader("あなたの備えタイプを2つの軸で診断します")

    st.write("""
このアプリでは、

- 防災グッズがどれくらい準備できているか  
- 避難生活をどれくらい具体的に想定できているか  

の2つを「はい / いいえ」で答えるだけで診断できます。
""")

    if st.button("診断を開始する ▶", key="start"):
        start_quiz()


# =========================
# 質問画面
# =========================
def show_quiz():
    idx = st.session_state.i
    q = QUESTIONS[idx]

    st.write(f"**質問 {idx+1} / 全 {len(QUESTIONS)}**")
    st.progress((idx+1) / len(QUESTIONS))

    st.markdown(f"""
        <div class="question-card">
            <div style="color:#666;font-size:0.9rem;font-weight:600;margin-bottom:0.3rem;">{q["label"]}</div>
            <div style="font-size:1.1rem;">{q["text"]}</div>
        </div>
    """, unsafe_allow_html=True)

    col1, col2 = st.columns(2)

    # はい（赤）
    with col1:
        if st.button("はい", key=f"yes_{idx}"):
            choose_answer(True)
        st.markdown('<script>$("button:contains(\'はい\')").addClass("yes-btn")</script>',
                    unsafe_allow_html=True)

    # いいえ（緑）
    with col2:
        if st.button("いいえ", key=f"no_{idx}"):
            choose_answer(False)
        st.markdown('<script>$("button:contains(\'いいえ\')").addClass("no-btn")</script>',
                    unsafe_allow_html=True)

    st.write("---")

    nav1, nav2 = st.columns(2)

    # 前へ
    with nav1:
        if st.button("前へ", key="prev", disabled=(idx == 0)):
            go_prev()
        st.markdown('<script>$("button:contains(\'前へ\')").addClass("nav-btn")</script>',
                    unsafe_allow_html=True)

    # トップへ
    with nav2:
        if st.button("トップへ戻る", key="top"):
            go_home()
        st.markdown('<script>$("button:contains(\'トップへ戻る\')").addClass("nav-btn")</script>',
                    unsafe_allow_html=True)


# =========================
# 結果画面（仮の形）
# =========================
def show_result():
    st.title("診断結果")
    st.write("ここにタイプ判定と説明が入ります（あとで本実装します）。")

    if st.button("もう一度診断する"):
        go_home()


# =========================
# メイン画面切り替え
# =========================
if st.session_state.page == "home":
    show_home()
elif st.session_state.page == "quiz":
    show_quiz()
else:
    show_result()
