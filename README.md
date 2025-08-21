[index.html](https://github.com/user-attachments/files/21911687/index.html)
<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>박진우의 자기소개</title> <!-- 1. 본인 이름 넣기 -->

    <!-- Bootstrap CSS -->
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">

    <!-- Google Fonts - Pretendard -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://cdn.jsdelivr.net/gh/orioncactus/pretendard/dist/web/static/pretendard.css" rel="stylesheet">

    <!-- 2. style.css 파일 대신, <style> 태그 내에 스타일을 직접 작성 -->
    <style>
        /* style.css */
        /* 1. body 배경색 설정 (#f8f9fa 또는 원하는 색상) */
        body {
            background-color: #f8f9fa;
            font-family: 'Pretendard', sans-serif;
        }

        /* 2. hero-section 배경 그라데이션 설정 및 애니메이션 적용 */
        .hero-section {
            background: linear-gradient(-45deg, #667eea, #764ba2, #4ECDC4, #A6A9C8);
            background-size: 400% 400%;
            animation: gradient-shift 15s ease infinite;
            color: white;
            min-height: 500px;
            display: flex;
            align-items: center;
        }
        @keyframes gradient-shift {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }

        /* 3. 프로필 이미지 크기 설정 (150px ~ 200px 추천) */
        .profile-img {
            width: 180px;
            height: 180px;
            object-fit: cover;
            border: 5px solid white;  /* 4. 테두리 색상 설정 */
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
        }

        /* 5. 카드 호버 효과 추가 */
        .card {
            transition: transform 0.3s;
            border: none;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
            height: 100%;
        }

        .card:hover {
            transform: translateY(-5px);  /* 6. -5px 정도 추천 */
            box-shadow: 0 5px 20px rgba(0,0,0,0.2);  /* 7. 0.2 정도 추천 */
        }

        /* 8. 섹션 제목 스타일 */
        h2 {
            color: #343a40;
            font-weight: 700;
            position: relative;
            display: inline-block;
        }

        /* 9. 제목 아래 장식선 추가 */
        h2::after {
            content: '';
            position: absolute;
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
            width: 50px;
            height: 3px;
            background-color: #667eea;
        }

        /* 10. 버튼 커스텀 스타일 */
        .btn {
            padding: 12px 30px;
            font-size: 16px;
            border-radius: 25px;
            text-decoration: none;
            transition: all 0.3s;
        }
        .btn:hover {
            transform: scale(1.05);
        }

        /* 1. 타이핑 커서 효과 */
        .typing-cursor::after {
            content: '|';
            animation: blink 1s infinite;
        }
        @keyframes blink {
            0%, 50% { opacity: 1; }
            51%, 100% { opacity: 0; }
        }
        
        /* 텍스트 글로우 효과 */
        .glow-text {
            text-shadow: 0 0 10px #fff,
                         0 0 20px #fff,
                         0 0 30px #007bff,
                         0 0 40px #007bff;
            animation: glow 2s ease-in-out infinite alternate;
        }
        @keyframes glow {
            from { text-shadow: 0 0 10px #fff; }
            to { text-shadow: 0 0 20px #fff, 0 0 30px #007bff, 0 0 40px #007bff; }
        }

        /* 1. 태블릿 반응형 (768px ~ 991px) */
        @media (max-width: 991px) {
            .col-md-4 {
                margin-bottom: 20px;
            }
            section {
                padding: 40px 0;
            }
        }
        /* 2. 모바일 반응형 (768px 이하) */
        @media (max-width: 768px) {
            .profile-img {
                width: 120px;
                height: 120px;
            }
            .display-4 {
                font-size: 2rem;
            }
            .hero-section {
                min-height: 400px;
                padding: 30px 0;
            }
            .navbar-nav {
                text-align: center;
                width: 100%;
            }
        }
    </style>
</head>
<body>
    <!-- 네비게이션 바 -->
    <nav class="navbar navbar-expand-lg navbar-dark bg-dark">
        <div class="container">
            <!-- 3. 본인 이름이나 닉네임 넣기 -->
            <a class="navbar-brand" href="#">박진우</a>
            <div class="navbar-nav ms-auto">
                <!-- 4. 메뉴 3개 추가하기 -->
                <a class="nav-link" href="#about">소개</a>
                <a class="nav-link" href="#skills">기술</a>
                <a class="nav-link" href="#contact">연락처</a>
            </div>
        </div>
    </nav>

    <!-- 메인 소개 섹션 -->
   <section class="hero-section text-center py-5">
        <div class="container">
            <!-- 5. 프로필 이미지 src에 본인 사진 URL 넣기 -->
            <!-- Unsplash의 새로운 이미지로 업데이트했습니다. -->
            <img src="https://images.unsplash.com/photo-1486312338219-ce68d2c6f44d" alt="프로필 사진" class="profile-img rounded-circle mb-4">
            <!-- 6. 본인 이름과 한 줄 소개 넣기 -->
            <h1 class="display-4 glow-text">안녕하세요! <span class="typing-cursor">박진우</span>입니다</h1>
            <p class="lead">예술이 기술이 되는 시대. 그 위에 낭만을 심습니다.</p>
            <!-- 7. Bootstrap 버튼 색상 클래스 선택 -->
            <a href="#about" class="btn btn-primary">더 알아보기</a>
        </div>
    </section>


    <!-- About 섹션 -->
    <section id="about" class="py-5 bg-light">
        <div class="container">
            <h2 class="text-center mb-4">About Me</h2>
            <div class="row">
                <div class="col-md-8 mx-auto">
                    <!-- 8. 자기소개 3-4줄 작성 -->
                    <p>안녕하세요. 저는 AI 기술을 통해 새로운 가치를 창출하는 것을 목표로 삼고 있습니다. 기술 위에 낭만을 얹음으로써 생산성 위에 가치를 추구하고자 합니다.</p>
                    <p>이 포트폴리오는 저의 기본적인 기술 능력과 함께, AI 도구의 활용성을 보여주는 예시입니다. 부트스트랩과 CSS의 기본 개념을 이해하는 데서 나아가, AI 에이전트를 통해 단시간에 완성도 높은 결과물을 만들어낼 수 있습니다.</p>
                    <p>AI 기술을 통해서 인간 활동의 흐름을 끊기지 않게 해주는 것이 중요하다고 생각합니다. 언제든지 연락 주세요.</p>
                    <!-- B. Badge로 관심사 표현 -->
                    <h5 class="mt-4">관심 분야</h5>
                    <div class="interests mb-4">
                        <span class="badge bg-primary m-1">프롬프트 엔지니어링</span>
                        <span class="badge bg-success m-1">AI 모델 개발</span>
                        <span class="badge bg-info m-1">효율적인 협업</span>
                        <span class="badge bg-warning m-1">온디바이스 AI</span>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Skills 섹션 -->
    <section id="skills" class="py-5">
        <div class="container">
            <h2 class="text-center mb-4">My Skills</h2>
            <div class="row">
                <!-- 9. 본인의 스킬 3개 작성 -->
                <div class="col-md-4 mb-3">
                    <div class="card">
                        <div class="card-body text-center">
                            <h5 class="card-title">디지털 정신분석</h5>
                            <p class="card-text">온라인을 통해 신경증을 다루고<br>회복을 이끌어냅니다.</p>
                            <!-- A. Progress Bar로 스킬 레벨 표현 -->
                            <div class="skill-item mb-3">
                                <label>전문가</label>
                                <div class="progress">
                                    <div class="progress-bar bg-success" role="progressbar" style="width: 95%" aria-valuenow="95" aria-valuemin="0" aria-valuemax="100">95%</div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
                <!-- 10. 나머지 2개 카드도 위와 같이 완성하기 -->
                <div class="col-md-4 mb-3">
                    <div class="card">
                        <div class="card-body text-center">
                            <h5 class="card-title">책쓰기</h5>
                            <p class="card-text">디지털 정신분석 연구 등의<br>저서를 집필했습니다.</p>
                            <div class="skill-item mb-3">
                                <label>숙련자</label>
                                <div class="progress">
                                    <div class="progress-bar bg-info" role="progressbar" style="width: 85%" aria-valuenow="85" aria-valuemin="0" aria-valuemax="100">85%</div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="col-md-4 mb-3">
                    <div class="card">
                        <div class="card-body text-center">
                            <h5 class="card-title">AI 번역</h5>
                            <p class="card-text">AI를 활용한 번역의<br>정확도를 높입니다.</p>
                            <div class="skill-item mb-3">
                                <label>중급</label>
                                <div class="progress">
                                    <div class="progress-bar bg-warning" role="progressbar" style="width: 70%" aria-valuenow="70" aria-valuemin="0" aria-valuemax="100">70%</div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact 섹션 -->
    <section id="contact" class="py-5 bg-dark text-white">
        <div class="container text-center">
            <h2 class="mb-4">Contact Me</h2>
            <!-- 11. 연락처 정보 추가 -->
            <p>Email: stryperhan@naver.com</p>
            <p>Phone: 010-5120-4473</p>
            <p>Github: github.com/stryperhan-ctrl</p>
        </div>
    </section>

    <!-- Bootstrap JS -->
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js"></script>
</body>
</html>
