<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
<!--     <title>정도술 연혁</title> -->
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        /* Custom styles for the timeline */
        body {
            font-family: 'Inter', sans-serif;
            background-color: #f3f4f6; /* Light gray background */
        }
        .timeline-container {
            position: relative;
            max-width: 1000px; /* Max width for the timeline content */
            margin: 0 auto;
            padding: 20px 0;
        }

        /* The vertical line in the middle */
        .timeline-container::after {
            content: '';
            position: absolute;
            width: 4px;
            background-color: #6366f1; /* Indigo 500 */
            top: 0;
            bottom: 0;
            left: 50%;
            margin-left: -2px;
            @media (max-width: 768px) { /* On small screens, line is on the left */
                left: 20px;
                margin-left: 0;
            }
        }

        /* Container for timeline items */
        .timeline-item {
            padding: 10px 40px;
            position: relative;
            background-color: inherit;
            width: 50%; /* Half width for left/right items */
            @media (max-width: 768px) { /* On small screens, full width */
                width: 100%;
                padding-left: 60px; /* Space for the line and dot */
                padding-right: 10px;
            }
        }

        /* The circles on the timeline */
        .timeline-item::after {
            content: '';
            position: absolute;
            width: 20px;
            height: 20px;
            background-color: #6366f1; /* Indigo 500 */
            border: 4px solid #a5b4fc; /* Indigo 300 for border */
            top: 20px;
            border-radius: 50%;
            z-index: 1;
            @media (max-width: 768px) { /* On small screens, dot is on the left */
                left: 10px;
                margin-left: 0;
            }
        }

        /* Place the timeline item to the left */
        .left {
            left: 0;
            padding-right: 60px; /* Space for the dot and line */
            @media (max-width: 768px) {
                left: 0;
                padding-right: 10px;
            }
        }

        /* Place the timeline item to the right */
        .right {
            left: 50%;
            padding-left: 60px; /* Space for the dot and line */
            @media (max-width: 768px) {
                left: 0;
                padding-left: 60px;
            }
        }

        /* Fix the circle for left sided timeline items */
        .left::after {
            right: -10px; /* Position relative to the item */
            @media (max-width: 768px) {
                left: 10px;
            }
        }

        /* Fix the circle for right sided timeline items */
        .right::after {
            left: -10px; /* Position relative to the item */
            @media (max-width: 768px) {
                left: 10px;
            }
        }

        /* The actual content of the timeline item */
        .timeline-content {
            background-color: white;
            padding: 20px 30px;
            border-radius: 8px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            position: relative;
        }

        /* Arrow for left content */
        .left .timeline-content::before {
            content: " ";
            height: 0;
            position: absolute;
            top: 22px;
            width: 0;
            z-index: 1;
            right: -15px;
            border: medium solid white;
            border-width: 10px 0 10px 10px;
            border-color: transparent transparent transparent white;
            @media (max-width: 768px) {
                left: 45px;
                right: auto;
                border-width: 10px 10px 10px 0;
                border-color: transparent white transparent transparent;
            }
        }

        /* Arrow for right content */
        .right .timeline-content::before {
            content: " ";
            height: 0;
            position: absolute;
            top: 22px;
            width: 0;
            z-index: 1;
            left: -15px;
            border: medium solid white;
            border-width: 10px 10px 10px 0;
            border-color: transparent white transparent transparent;
            @media (max-width: 768px) {
                left: 45px;
                border-width: 10px 10px 10px 0;
                border-color: transparent white transparent transparent;
            }
        }
    </style>
</head>
<body>
    <div class="min-h-screen flex flex-col items-center py-10 bg-gray-100">
        <h1 class="text-4xl font-extrabold text-gray-800 mb-10 text-center">정도술 연혁</h1>

        <div class="timeline-container">
            <div class="timeline-item left">
                <div class="timeline-content">
                    <h2 class="text-xl font-semibold text-indigo-700">~1941</h2>
                    <p class="text-gray-700 mt-2">안복용 대선사 금강산 장안사에서 가전비술인 정도술 수련</p>
                </div>
            </div>

            <div class="timeline-item right">
                <div class="timeline-content">
                    <h2 class="text-xl font-semibold text-indigo-700">1941 ~ 1947</h2>
                    <p class="text-gray-700 mt-2">정도술의 조사 안복용 대선사로부터 안일력 대정사가 가전비술인 정도술을 전수받음 (고창 선운사 장군봉 일대)</p>
                </div>
            </div>

            <div class="timeline-item left">
                <div class="timeline-content">
                    <h2 class="text-xl font-semibold text-indigo-700">1957</h2>
                    <p class="text-gray-700 mt-2">안일력 대정사가 서울 최초 수련생들에게 정도술 지도</p>
                </div>
            </div>

            <div class="timeline-item right">
                <div class="timeline-content">
                    <h2 class="text-xl font-semibold text-indigo-700">1958. 04. 05 (음력)</h2>
                    <p class="text-gray-700 mt-2">최초 정도술 발표 시범 실시 (효창동 백범 김구 선생 묘소)</p>
                </div>
            </div>

            <div class="timeline-item left">
                <div class="timeline-content">
                    <h2 class="text-xl font-semibold text-indigo-700">1958. 10. 03 (음력)</h2>
                    <p class="text-gray-700 mt-2">최초 정도술 수련장 설립 및 현판식 (서울 서대문구 응암동 군용텐트 설치 : 안일력 대정사 초대 사범 취임)</p>
                </div>
            </div>

            <div class="timeline-item right">
                <div class="timeline-content">
                    <h2 class="text-xl font-semibold text-indigo-700">1959. 10. 09</h2>
                    <p class="text-gray-700 mt-2">대한 정도술 회관 건립 (서대문구 응암동 418)</p>
                </div>
            </div>

            <div class="timeline-item left">
                <div class="timeline-content">
                    <h2 class="text-xl font-semibold text-indigo-700">1960. 10. 09</h2>
                    <p class="text-gray-700 mt-2">정도술 1기생 자격 심사 실시</p>
                </div>
            </div>

            <div class="timeline-item right">
                <div class="timeline-content">
                    <h2 class="text-xl font-semibold text-indigo-700">1961. 06. 24</h2>
                    <p class="text-gray-700 mt-2">대한정도술회관 이전 및 ‘대한 정도술 중앙수련관’으로 명의 개칭 (홍제동)</p>
                </div>
            </div>

            <div class="timeline-item left">
                <div class="timeline-content">
                    <h2 class="text-xl font-semibold text-indigo-700">1962. 04. 05</h2>
                    <p class="text-gray-700 mt-2">‘대한 정도술 중앙수련관’ 야회 수련관 설치 (수유동 488)</p>
                </div>
            </div>

            <div class="timeline-item right">
                <div class="timeline-content">
                    <h2 class="text-xl font-semibold text-indigo-700">1963. 05. 14</h2>
                    <p class="text-gray-700 mt-2">정도술 시범대회 개최 (진명여고 강당 3.1당에서)</p>
                </div>
            </div>

            <div class="timeline-item left">
                <div class="timeline-content">
                    <h2 class="text-xl font-semibold text-indigo-700">1965. 05. 03-04</h2>
                    <p class="text-gray-700 mt-2">한.중 친선무술대회 개최 (장충체육관) - 후원 : 조선일보사</p>
                </div>
            </div>

            <div class="timeline-item right">
                <div class="timeline-content">
                    <h2 class="text-xl font-semibold text-indigo-700">1966. 03. 01</h2>
                    <p class="text-gray-700 mt-2">‘3.1절’ 경축 정도술 시범대회 개최 (장중체육관)</p>
                </div>
            </div>

            <div class="timeline-item left">
                <div class="timeline-content">
                    <h2 class="text-xl font-semibold text-indigo-700">1968. 04. 05</h2>
                    <p class="text-gray-700 mt-2">‘대한 정도술 중앙수련관’을 ‘대한 정도술 총 수련관’으로 명의 개칭</p>
                </div>
            </div>

            <div class="timeline-item right">
                <div class="timeline-content">
                    <h2 class="text-xl font-semibold text-indigo-700">1968. 11. 30</h2>
                    <p class="text-gray-700 mt-2">‘대한 정도술 총 수련관’ 이전 (중구 충무로4가 95번지 일우빌딩)</p>
                </div>
            </div>

            <div class="timeline-item left">
                <div class="timeline-content">
                    <h2 class="text-xl font-semibold text-indigo-700">1969. 02. 16</h2>
                    <p class="text-gray-700 mt-2">정도술 시범 공개 발표 (KBS TV)</p>
                </div>
            </div>

            <div class="timeline-item right">
                <div class="timeline-content">
                    <h2 class="text-xl font-semibold text-indigo-700">1969. 05. 13</h2>
                    <p class="text-gray-700 mt-2">정도술 시범 대회 개최 (서울 운동장)</p>
                </div>
            </div>

            <div class="timeline-item left">
                <div class="timeline-content">
                    <h2 class="text-xl font-semibold text-indigo-700">1969. 06. 17</h2>
                    <p class="text-gray-700 mt-2">일본 후지TV초청시범 (신술, 단검술, 출하술) *지상 11M로부터 출하, 세계기록 수립</p>
                </div>
            </div>

            <div class="timeline-item right">
                <div class="timeline-content">
                    <h2 class="text-xl font-semibold text-indigo-700">1970. 08. 16</h2>
                    <p class="text-gray-700 mt-2">정도술 시범 공개 발표 (TBC TV)</p>
                </div>
            </div>

            <div class="timeline-item left">
                <div class="timeline-content">
                    <h2 class="text-xl font-semibold text-indigo-700">1971. 06. 20</h2>
                    <p class="text-gray-700 mt-2">‘대한 정도술 총 수련관 이전 (중구 주교동 144 협동빌딩)</p>
                </div>
            </div>

            <div class="timeline-item right">
                <div class="timeline-content">
                    <h2 class="text-xl font-semibold text-indigo-700">1975. 05. 20</h2>
                    <p class="text-gray-700 mt-2">‘대한 정도술 총 수련관 이전 (보문동 1가 128 고명빌딩)</p>
                </div>
            </div>

            <div class="timeline-item left">
                <div class="timeline-content">
                    <h2 class="text-xl font-semibold text-indigo-700">1975. 08. 01</h2>
                    <p class="text-gray-700 mt-2">정도술 일본 중앙수련관 설립 (일본 동경)</p>
                </div>
            </div>

            <div class="timeline-item right">
                <div class="timeline-content">
                    <h2 class="text-xl font-semibold text-indigo-700">1975. 09. 12</h2>
                    <p class="text-gray-700 mt-2">전국 무술단체장 안보 단합대회 주관 (세종호텔 해금강홀)</p>
                </div>
            </div>

            <div class="timeline-item left">
                <div class="timeline-content">
                    <h2 class="text-xl font-semibold text-indigo-700">1975. 10. 09</h2>
                    <p class="text-gray-700 mt-2">대한민국 ‘정도술 협회’ 창립</p>
                </div>
            </div>

            <div class="timeline-item right">
                <div class="timeline-content">
                    <h2 class="text-xl font-semibold text-indigo-700">1975. 10. 19</h2>
                    <p class="text-gray-700 mt-2">대한민국 무술 총 연합회 창립 주관</p>
                </div>
            </div>

            <div class="timeline-item left">
                <div class="timeline-content">
                    <h2 class="text-xl font-semibold text-indigo-700">1975. 11</h2>
                    <p class="text-gray-700 mt-2">대한민국 정도술 재일교포 수련관 설립 (요코하마시)</p>
                </div>
            </div>

            <div class="timeline-item right">
                <div class="timeline-content">
                    <h2 class="text-xl font-semibold text-indigo-700">1976. 02. 06</h2>
                    <p class="text-gray-700 mt-2">정도술 시범 공개 발표 (MBC TV)</p>
                </div>
            </div>

            <div class="timeline-item left">
                <div class="timeline-content">
                    <h2 class="text-xl font-semibold text-indigo-700">1976. 02. 14</h2>
                    <p class="text-gray-700 mt-2">제 1회 전국 무술 경연대회 출전 및 주관 (문화 체육관) * 대한민국 무술 총 연합회, 문화방송, 경향신문 공동주최</p>
                </div>
            </div>

            <div class="timeline-item right">
                <div class="timeline-content">
                    <h2 class="text-xl font-semibold text-indigo-700">1976. 05. 30</h2>
                    <p class="text-gray-700 mt-2">부산 ‘구덕 체육관’, 전북 ‘군산여상’ 시범</p>
                </div>
            </div>

            <div class="timeline-item left">
                <div class="timeline-content">
                    <h2 class="text-xl font-semibold text-indigo-700">1976. 09. 18</h2>
                    <p class="text-gray-700 mt-2">정도술 시범대회 (육군 제2훈련소)</p>
                </div>
            </div>

            <div class="timeline-item right">
                <div class="timeline-content">
                    <h2 class="text-xl font-semibold text-indigo-700">1976. 10. 02</h2>
                    <p class="text-gray-700 mt-2">정도술 시범대회 (공수단에서)</p>
                </div>
            </div>

            <div class="timeline-item left">
                <div class="timeline-content">
                    <h2 class="text-xl font-semibold text-indigo-700">1977. 01. 15 ~ 03. 16</h2>
                    <p class="text-gray-700 mt-2">정도술 재일 수련관 지휘자 지도차 안호해(안길원) 일본파견</p>
                </div>
            </div>

            <div class="timeline-item right">
                <div class="timeline-content">
                    <h2 class="text-xl font-semibold text-indigo-700">1977. 02. 19</h2>
                    <p class="text-gray-700 mt-2">제2회 전국 무술 대회 출전 및 주관</p>
                </div>
            </div>

            <div class="timeline-item left">
                <div class="timeline-content">
                    <h2 class="text-xl font-semibold text-indigo-700">1977. 06. 23</h2>
                    <p class="text-gray-700 mt-2">정도술 시범대회 (청룡부대)</p>
                </div>
            </div>

            <div class="timeline-item right">
                <div class="timeline-content">
                    <h2 class="text-xl font-semibold text-indigo-700">1977. 08. 04</h2>
                    <p class="text-gray-700 mt-2">정도술 재일본 대학생 수련단 제5차 내한수련</p>
                </div>
            </div>

            <div class="timeline-item left">
                <div class="timeline-content">
                    <h2 class="text-xl font-semibold text-indigo-700">1977. 09. 14</h2>
                    <p class="text-gray-700 mt-2">대한민국 정도술(호국무술) 청와대 특별초청 시범발표 (청와대 연무관) * 박정희 대통령으로 부터 극찬 격려 받음</p>
                </div>
            </div>

            <div class="timeline-item right">
                <div class="timeline-content">
                    <h2 class="text-xl font-semibold text-indigo-700">1977</h2>
                    <p class="text-gray-700 mt-2">안성 수련관 개관</p>
                </div>
            </div>

            <div class="timeline-item left">
                <div class="timeline-content">
                    <h2 class="text-xl font-semibold text-indigo-700">1978. 01. 16</h2>
                    <p class="text-gray-700 mt-2">서울 신당동수련관과 경기도 수택리 수련관 개관, 특전 사령부시범, 특전사 3공수단 시범, 육군본부 특별 경호대 수련과 특전사령부 3공수여단 수련</p>
                </div>
            </div>

            <div class="timeline-item right">
                <div class="timeline-content">
                    <h2 class="text-xl font-semibold text-indigo-700">1979</h2>
                    <p class="text-gray-700 mt-2">화성수련관, 용인 수련관 개관</p>
                </div>
            </div>

            <div class="timeline-item left">
                <div class="timeline-content">
                    <h2 class="text-xl font-semibold text-indigo-700">1980. 05. 31</h2>
                    <p class="text-gray-700 mt-2">제 5회 전국 무술 대회 주관</p>
                </div>
            </div>

            <div class="timeline-item right">
                <div class="timeline-content">
                    <h2 class="text-xl font-semibold text-indigo-700">1980. 10. 09</h2>
                    <p class="text-gray-700 mt-2">전두환 대통령 취임 축하 전국 무술 대회 주관 (장충체육관)</p>
                </div>
            </div>

            <div class="timeline-item left">
                <div class="timeline-content">
                    <h2 class="text-xl font-semibold text-indigo-700">1981</h2>
                    <p class="text-gray-700 mt-2">홍제동 수련관, 암행어사 출연 및 무술지도</p>
                </div>
            </div>

            <div class="timeline-item right">
                <div class="timeline-content">
                    <h2 class="text-xl font-semibold text-indigo-700">1982</h2>
                    <p class="text-gray-700 mt-2">단국대 정도술모임 단정회 창립 (안용주, 황순동), 충북대 정도술연구회 창립</p>
                </div>
            </div>

            <div class="timeline-item left">
                <div class="timeline-content">
                    <h2 class="text-xl font-semibold text-indigo-700">1984</h2>
                    <p class="text-gray-700 mt-2">수원 서문수련관, 고생동수련관 개관</p>
                </div>
            </div>

            <div class="timeline-item right">
                <div class="timeline-content">
                    <h2 class="text-xl font-semibold text-indigo-700">1985</h2>
                    <p class="text-gray-700 mt-2">괴산 수련관 개관</p>
                </div>
            </div>

            <div class="timeline-item left">
                <div class="timeline-content">
                    <h2 class="text-xl font-semibold text-indigo-700">1986</h2>
                    <p class="text-gray-700 mt-2">천호동 수련관 개관</p>
                </div>
            </div>

            <div class="timeline-item right">
                <div class="timeline-content">
                    <h2 class="text-xl font-semibold text-indigo-700">1987</h2>
                    <p class="text-gray-700 mt-2">경희대 정도술수련회 창립</p>
                </div>
            </div>

            <div class="timeline-item left">
                <div class="timeline-content">
                    <h2 class="text-xl font-semibold text-indigo-700">1992</h2>
                    <p class="text-gray-700 mt-2">화성 남양수련관 개관</p>
                </div>
            </div>

            <div class="timeline-item right">
                <div class="timeline-content">
                    <h2 class="text-xl font-semibold text-indigo-700">1993</h2>
                    <p class="text-gray-700 mt-2">화성 사강수련관 개관</p>
                </div>
            </div>

            <div class="timeline-item left">
                <div class="timeline-content">
                    <h2 class="text-xl font-semibold text-indigo-700">1993. 04. 04</h2>
                    <p class="text-gray-700 mt-2">신한국 건설 새시대맞이 전국무술 대구대회 주관</p>
                </div>
            </div>

            <div class="timeline-item right">
                <div class="timeline-content">
                    <h2 class="text-xl font-semibold text-indigo-700">1996</h2>
                    <p class="text-gray-700 mt-2">수원 세류동수련관, 전곡수련관 보문동수련관 개관</p>
                </div>
            </div>

            <div class="timeline-item left">
                <div class="timeline-content">
                    <h2 class="text-xl font-semibold text-indigo-700">1997</h2>
                    <p class="text-gray-700 mt-2">수원 구운동수련관 개관</p>
                </div>
            </div>

            <div class="timeline-item right">
                <div class="timeline-content">
                    <h2 class="text-xl font-semibold text-indigo-700">2008</h2>
                    <p class="text-gray-700 mt-2">수원 정자1동 수련관 개관</p>
                </div>
            </div>

            <div class="timeline-item left">
                <div class="timeline-content">
                    <h2 class="text-xl font-semibold text-indigo-700">2023</h2>
                    <p class="text-gray-700 mt-2">대림동 수련관 개관</p>
                </div>
            </div>

            <div class="timeline-item right">
                <div class="timeline-content">
                    <h2 class="text-xl font-semibold text-indigo-700">2024. 03. 02</h2>
                    <p class="text-gray-700 mt-2">‘대한 정도술 총 수련관’ 개관 (송내동)</p>
                </div>
            </div>

            <div class="timeline-item left">
                <div class="timeline-content">
                    <h2 class="text-xl font-semibold text-indigo-700">2024. 03 ~ 04</h2>
                    <p class="text-gray-700 mt-2">안일력 대정사님께서 1975.10. 09에 준비중이시던 ‘정도술 협회’ 법인설립 추진</p>
                </div>
            </div>

            <div class="timeline-item right">
                <div class="timeline-content">
                    <h2 class="text-xl font-semibold text-indigo-700">2024. 04. 02</h2>
                    <p class="text-gray-700 mt-2">‘정도술 협회’ 창립</p>
                </div>
            </div>

            <div class="timeline-item left">
                <div class="timeline-content">
                    <h2 class="text-xl font-semibold text-indigo-700">2024년 ~</h2>
                    <p class="text-gray-700 mt-2">정도술의 부활과 재건 시작중</p>
                </div>
            </div>
        </div>

        <p class="text-gray-600 text-center mt-8">이외에도 다수의 수련관 개관과 전국 무술대회의 활동들이 있었습니다.</p>
    </div>
</body>
</html>
