---
layout: post
title:  "내가 만약 카톡 선물하기의 분석가라면"
subtitle: "데이터리안 프로덕트 스터디"
type: "🧪 데이터 분석가들의 프로덕트 스터디"
blog: true
text: true
author: Bomin Lee
post-header: true
order: 8
---
친구, 지인에게 생일 선물을 보낼 때 어떤 서비스를 이용하시나요?

신선식품 하면 마켓컬리, 빠른 배송하면 쿠팡을 자연스럽게 떠올리는 것처럼 모름지기 이커머스 서비스라면 각각의 강점이 뚜렷하게 있는 편이 비지니스 관점에서 훨씬 좋을텐데요. 오늘은 쿠팡, 마켓컬리처럼 많은 사람들에 의해 분석되거나 언론에서 자주 언급되지는 않지만, 마찬가지로 타겟군이 뚜렷한 이커머스 서비스로 주목해볼 수 있는 서비스인 **카카오톡 선물하기**를 분석가 관점에서 한번 뜯어볼까 합니다.  
<span style="color:white">.</span>  
결론부터 말씀드리면, **제가 만약 카카오톡 선물하기 분석가였다면 아래 네가지 지표를 주요하게 볼 것 같아요.** 이 지표를 봐야하는 자세한 이유는 마지막에 자세하게 설명드릴테니 잘 따라와주세요 😉    
  
> 1. N회 이상 선물을 받은 유저들의 수
> 2. 나에게 선물하기를 하는 비율
> 3. 특정 세그먼트 유저(MZ 세대로 불리우는)들의 유입량
> 4. 검색 관련 지표  
  

## <span style="color:#ed4e14">숫자로 보는 카카오톡 선물하기</span>

먼저 몇가지 수치를 통해 카카오톡 선물하기에 대해 알아볼게요.

> 1. **국민 10명중 7명은 카카오톡 선물하기를 통해 선물을 주고 받은 적이 있다.**
> 2. 2010년 12월 세상에 처음 선보인 선물하기 서비스는 15개 제휴사 100여개 상품으로 시작해서 **2020년 8월 현재 8000개 제휴사 50만개 상품으로 확장**되었다.
> 3. **가장 많이 판매된 상품은 커피(하루 평균 20만잔)**, 20~30대 젊은 남성 유저들이 늘어나면서 치킨이 그 뒤를 바짝 쫒고 있다.
> 4. 카카오톡 선물하기는 출범 10년 만인 지난해 **거래액이 약 3조원** 규모로 성장했다. 카카오에 따르면, 지난해 선물하기 매출은 전년 대비 52% 신장했다.  

저희도 카카오톡 선물하기 거래액이 3조원이나 된다는 것을 처음 알게되었는데요. 카톡 선물하기를 통해 거의 선물을 안받아본 사람이 없을만큼 범용적으로 사용되고 있는 서비스인 것은 분명한 것 같습니다. 

## <span style="color:#ed4e14">카카오톡 선물하기의 타겟 유저군과 사업모델</span>

분석가 관점에서 카카오톡 선물하기 서비스를 바라보았을 때 어떤 것들을 생각해볼 수 있을까요? 우선 타겟 유저는 누구인지, 비지니스가 전체적으로 어떤 모양으로 생겼는지를 한번 생각해보겠습니다.

카카오톡을 사용하지 않는 사람이 카카오톡 선물하기를 사용하지는 않겠죠. 그렇다면 우선 타겟이 되는 유저는 '국내에서 카카오톡을 주 메신저로 사용하는 사용자 전체'가 될 것 같습니다. 어떤 상황에서 선물하기를 사용하게 되는지 생각해보면 '친구, 지인과의 작은 이벤트(주로 생일)을 챙길 일이 있는 사용자'라고도 생각할 수 있겠네요.

카카오톡 선물하기의 비지니스 모델은 크게 보면 B2C 비지니스와 B2B 비지니스가 모두 존재하는 **마켓플레이스 모델**이라고 할 수 있습니다. B2C로는 알겠는데 B2B는 어떤 비지니스가 있는지 잘 모르시겠다구요?  

카카오톡 선물하기 서비스 자체에서 상품을 제작하거나 사입하여 판매를 하는 것이 아니고, 여러 브랜드들의 입점하여 그들의 상품 판매를 돕는 플랫폼으로 기능하고 있습니다. 서비스 내에 각 브랜드들은 상품이 판매될 때마다 <u>판매 수수료</u>를 선물하기 측에 지불하고 있으며, 여러 페이지에서 상품이 잘 노출될 수 있게끔 하는 여러가지 <u>광고 영역</u>도 유료로 판매가 되고 있습니다.

## <span style="color:#ed4e14">카카오톡 선물하기에서 봐야할 4가지 지표</span>

카카오톡 선물하기 서비스의 전체적인 그림이 이제 조금 보이시나요?  
그럼 이제 본격적으로 데이터 얘기를 해보겠습니다.  

유저 인입부터 유저 활성화, 리텐션, 결제와 관련된 부분 등등 여러가지에 면에서 프로덕트를 뜯어보았는데요. 그 중에서도 **'내가 만약 카카오톡 선물하기 부서에서 일하고 있는 분석가라면 서비스의 성장을 위해 이 데이터를 중요하게 보고 있을 것(또는 봐야할 것) 같다'고 생각되는 4가지 포인트**를 꼽아보았습니다. 이 네가지 지표는 현상 유지, 돌발 이슈 파악을 위한 데이터라기 보다는 앞으로 선물하기 서비스를 더 확장시키고 성장시키기 위해 확인해 보아야 하는 데이터들로만 추려진 내용입니다.

중심이 되는 포인트는 두가지 인데요. 비지니스 성장을 위해서는 **신규 유저들을 더 데려오거나, 기존에 있는 유저들이 더 많이, 자주 선물하기 서비스를 사용하게끔** 해야합니다.  
<span style="color:white">.</span>  

**1. 특정 세그먼트 유저(MZ 세대)들의 유입량**

위에서도 언급했 듯 카카오톡을 아예 사용하지 않는 유저들이 선물하기를 사용하기 위해서 카톡에 가입하는 것은 조금 어려운 일이 아닐까 싶습니다. 여러가지 매체에서 <u>MZ 세대들의 특징으로 주 메신저를 카카오톡으로 사용하지 않는다</u>는 것을 이야기하고 있는데요. 그렇다면 마찬가지로 카카오톡 선물하기 서비스로 유입되는 유저들 중 MZ 세대의 비율 또한 다른 연령대에 비해 적을 것으로 생각됩니다.

실제로 데이터가 그러하다면, 이 데이터를 지속적으로 모니터링하며 MZ 세대의 유입량을 변화시킬 수 있을 만한 방안을 만들어가야할 것으로 생각이 됩니다. 최근 선물하기 서비스 내에 명품 브랜드들의 입점이 늘었다고 하는데요. 명품 소비를 상대적으로 많이한다고 알려진 MZ 세대들의 유입량에 변화가 있었는지도 궁금해지는 지점입니다.  
<span style="color:white">.</span>  

**2. 구매 경험 없는 유저들 중 N회 이상 선물 받은 유저들의 수 or 비율**

선물하기를 사용해보지 않은 유저가 [구매를 하는 유저가 되기까지 평균 4회 정도의 선물을 받는 경험을 한다](https://www.donga.com/news/Economy/article/all/20200831/102727097/1)고 합니다. 이 지표는 아직 구매 경험이 없는 유저들을 구매 유저로 끌어올리기 위해 확인해야하는 사전지표라고 할 수 있겠는데요. 이 숫자가 증가한다면 구매 경험이 없는 유저 중 구매 유저로 전환될 가능성이 높은 유저들이 어느 정도나 있는지를 알 수가 있겠죠. 
기존에 카카오톡을 메신저로 사용은 하지만 선물하기를 잘 사용하지 않았던 유저들을 구매 유저로 전환시키기 위해 모니터링해야하는 사전지표라고 생각됩니다.  
<span style="color:white">.</span>  

**3. 나에게 선물하기를 하는 비율**

신규 유저들과 관련된 지표들을 두개 살펴봤으니 기존에 있던 유저들과 관련된 지표도 살펴보아야 겠죠? 사실 <u>'선물하기'라는 카테고리의 특성상 주변에 선물할 만한 이벤트가 발생하지 않으면 서비스를 사용할 일이 딱히 없다는 단점</u>이 있는데요. 이 부분을 카톡 선물하기에서는 '나에게 선물하기'라는 기능을 넣음으로서 보완을 하려고 하는 것 같습니다.

나에게 선물하기라니 말이 선물이지 그냥 물건을 사러 선물하기에 들어온다는 것과 같은 말이죠. 확실히 어떤 특별한 이벤트가 있을 때, 타인을 위한 선물을 위해 서비스에 들어오는 것보다는 자신이 필요한 물건을 사기 위해 쇼핑을 하는 경우가 그 빈도수는 훨씬 더 높을 것 같습니다.

때문에 전체 구매량 중 나에게 선물하기를 하는 비율이 높아질 수록 선물하기 플랫폼에 특정 이벤트 때문에 들어오는 유저들보다 그냥 쇼핑을 위해 들어오는 유저들의 비율이 높아진다고 볼 수 있을 것 같아요. 그렇게되면 <u>결과적으로는 재구매 리텐션 또한 증가하여 비즈니스에 긍정적인 영향이 될 것</u>으로 생각됩니다.  
<span style="color:white">.</span>  

**4. 검색 관련 지표**

마지막으로 재방문 리텐션, 재구매 리텐션과 관련한 지표로 <u>검색 관련 지표</u>들을 봐야한다는 생각이 들어요.

몇 분의 경험을 들어보니 보통 타인의 선물을 고를 때에는 뭘 갖고 싶어 할지 잘 모르는 경우가 많고 가격대 등도 모두 고려해야하기 때문에 검색보다는 추천 영역이나 카테고리들을 훑어보면서 무엇을 선물해야할지 고민하는 경우가 많다고 합니다. 반면에 <u>자신이 사고 싶었던 것을 사러 들어갈 때에는 바로 검색을 하는 경우가 많다</u>는 것을 알게되었어요.

만약, 카카오톡 선물하기가 좀 더 일반 쇼핑의 영역까지 저변을 넓히고 싶은게 맞다면 유저들이 직접 검색을 하는지 모니터링하고 해당 지표를 개선하기 위한 방안을 적용시키는 것이 맞지 않을까 생각해보았습니다.  

<span style="color:white">.</span>  
<span style="color:white">.</span>  
<span style="color:white">.</span>  

<span style="color:gray"> # 이 글은 데이터리안 프로덕트 스터디 중 일부를 정리한 내용입니다.</span>  

<span style="color:white">.</span>  

**<span style="color:gray">참고 자료</span>**

[카카오톡 선물하기서 많이 팔리는 상품 2위 치킨…1위는?](https://www.donga.com/news/Economy/article/all/20200831/102727097/1) <동아일보> 2020.08

[“어머님, 카톡으로 보냈어요”...코로나에 훌쩍 큰 ‘모바일 선물하기'](https://biz.chosun.com/site/data/html_dir/2021/02/14/2021021400015.html#:~:text=%EC%84%A0%EB%AC%BC%ED%95%98%EA%B8%B0%20%EC%84%9C%EB%B9%84%EC%8A%A4%EC%9D%98%20%EC%9B%90%EC%A1%B0,2173%EB%A7%8C%EB%AA%85%EC%9C%BC%EB%A1%9C%20%EC%A7%91%EA%B3%84%EB%90%90%EB%8B%A4.) <조선비즈> 2021.04

[‘카카오톡 선물하기’가 잘될 수밖에 없는 이유](https://ppss.kr/archives/178364) <ㅍㅍㅅㅅ> 2018.11

[카카오 선물하기의 급성장을 만든 4개의 변화](https://byline.network/2020/11/25-111/)

[카카오 선물하기 이렇게 비싼데 왜 쓰냐고?](https://beyondx.ai/%ec%b9%b4%ec%b9%b4%ec%98%a4-%ec%84%a0%eb%ac%bc%ed%95%98%ea%b8%b0-%ec%9d%b4%eb%a0%87%ea%b2%8c-%eb%b9%84%ec%8b%bc%eb%8d%b0-%ec%99%9c-%ec%93%b0%eb%83%90%ea%b3%a0/)

[카카오톡 선물하기 - 카카오 커머스 기업사이트](https://www.kakaocommerce.com/service/gift)  

<span style="color:white">.</span>  
  