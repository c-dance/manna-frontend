<template>
  <div class="container l--table">
    <div class="l--cell">
    <div class="box box--m">
      <h1 class="heading--title">
        약속 후보 등록
      </h1>
      <div class="form">
      <div class="">
        <span for="userEmail" class="label">약속명</span>
        <span>목요 한강 캠핑</span>
      </div>
      <div class="">
        <span for="userEmail" class="label">참여자</span>
        <div class="inline__wrap">
            <span>가가</span>
        </div>
      </div>
      <fieldset class="input--wrap">
        <label class="label">
          날짜 추가
          <span class="l--block">(새로운 날짜를 추가해 주세요. 날짜는 3개까지 추가 할 수 있습니다.)</span>
        </label>
        <div class="l--flex--row jt--space">
            <div class="calendar--add">
            <v-date-picker
              is-expanded
              v-model="pickdate"
              :attributes="attrs"
              :model-config="modelConfig"
              is-required
            />
            </div>
            <div>
                <button class="btn--submit btn--submit--s">추가</button>
            </div>
        </div>
        </fieldset>
        <div class="list__wrap">
            <p class="list__title">추가된 날짜</p>
            <ul class="list">
              <li class="list__item">6월 12일</li>
              <li class="list__item">6월 19일</li>
            </ul>
        </div>
      <fieldset class="input--wrap">
        <label class="label">
             장소 추가 
            <span class="l--block">(새로운 장소를 추가해 주세요. 장소는 제한없이 추가할 수 있습니다.)</span>
        </label>
        <div class="l--flex--row jt--space">
        <input type="text" placeholder="장소를 입력해 주세요" class="input--text input--text--white">
        <button  class="btn--submit btn--submit--s">
            추가
          </button>
        </div>
      </fieldset>
        <div class="list__wrap">
            <p class="list__title">장소</p>
            <ul class="list">
              <li class="list__item">노량진 청년다방</li>
              <li class="list__item">노량진 스타벅스</li>
            </ul>
        </div>
      <button class="btn--submit mg--m">후보 등록 하기</button>
      </div>
    </div>
    </div>
  </div>
</template>
