<template>
  <div class="introduction">
    <header class="intro-header">
      <div class="intro-content">
      <img src="C:\Users\User\Desktop\MCH\MCH_Dev-Interview-Project\frontend\src\assets\me.jpg"  alt="my photo" class="profile-pic">
      <div class="intro-text">
        <h2>自我介紹</h2>
        <p>
          大家好！我是清大資工系大二的蔡佳倩，來自一年四季都很熱的高雄，對網頁和軟體開發有興趣，也喜歡學習新的技術跟挑戰自我，希望可以認識好強的大家！
        </p>
        <button class="contact"> <a href="https://www.instagram.com/imchien.12o1_/" target="_blank">我的ig</a></button>     
      </div>
      </div>  
    </header>

    <section class="about-section">
      <h3>個人資訊補充</h3>
      <ul>
        <li>日常嗜好：跳舞、聽音樂、看書</li>
        <li>個性：INFJ，小慢熟但認識之後蠻活潑的</li>
        <li>會的語言：英文、日文、韓文、德文，當然也有程式語言啦但太菜了不好說</li>
        <li>個人目標：希望可以變得好會寫網頁</li>
      </ul>
    </section>

  </div>
</template>


<style scoped>
.introduction {
  padding: 40px 20px;
  max-width: 800px;
  margin: 0 auto;
}

.intro-header {
  background-color:#dcdcdc;
  padding: 40px;
  border-radius: 12px;
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
}

.intro-content {
  display: flex;
  align-items: center;
  gap: 20px;
}

.profile-pic {
  width: 250px; 
  height: 250px;
  border-radius: 50%;
  object-fit: cover; 
  border: 3px solid #ccc;
}

.intro-text h2 {
  font-size: 1.8rem;
  margin-bottom: 10px;
}

.intro-text p {
  font-size: 1.1rem;
  margin-bottom: 20px;
}

.contact-button {
  padding: 10px 20px;
  background-color: #656d73;
  border: none;
  border-radius: 5px;
  color: #fff;
  cursor: pointer;
}

.contact-button:hover {
  background-color: #36383a;
}

.about-section {
  margin-top: 40px;
  padding: 0 40px;
}

.about-section h3 {
  font-size: 1.6rem;
  margin-top: 20px;
  margin-bottom: 10px;
}

.about-section p {
  font-size: 1rem;
  line-height: 1.6;
}
</style>
