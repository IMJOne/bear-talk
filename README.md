![beartalk](https://user-images.githubusercontent.com/110226567/216779047-26492282-58ae-47d0-a7bc-48532d2b1007.png)

# π» BearTalk

λͺ¨λ°μΌ μ±νμ‘ UI κ΅¬ν μ¬μ΄νΈ π [Demo](https://imjone.github.io/bear-talk/)

<br />

## π’ νλ‘μ νΈ κ°μ

μ μ μ΅μ’ λͺ©ν μ€ νλκ° λ°λ‘ μ±ν μ΄νλ¦¬μΌμ΄μ κ°λ°μ΄μμ΅λλ€.<br />
μμ§ μλ²μ λν μ§μμ μκΈ°μ, UIμ μΈ λΆλΆλ§μ΄λΌλ λ§λ€μ΄λ³΄κ³  μΆμμ΅λλ€.<br />
PC μΉ΄μΉ΄μ€ν‘ λμμΈμ μ°Έκ³ νμμΌλ©°, SCSS λ¬Έλ²μ ν΅ν΄ λΉ λ₯΄κ² μ€νμΌλ§νμμ΅λλ€.

<br />

## π¨οΈ μ¬μ© κΈ°μ 

<p>
  <img src="https://img.shields.io/badge/HTML-E34F26?style=flat-square&logo=HTML5&logoColor=white"/>
  <img src="https://img.shields.io/badge/SCSS-CC6699?style=flat-square&logo=Sass&logoColor=white"/>
  <img src="https://img.shields.io/badge/JavaScript-f7df1e?style=flat-square&logo=JavaScript&logoColor=white"/>
</p>

<br />

## π μ£Όμ κΈ°λ₯

- μμ΄λμ λΉλ°λ²νΈλ₯Ό μλ ₯ν  μ μλ λ‘κ·ΈμΈνΌ
- μ±ν λ΄μ© λ° μλ νλ‘ν λ―Έλ¦¬λ³΄κΈ° νμ΄μ§
- μ±νλ°© λ΄ κ°λ¨ν λ©μμ§ μ μ‘ κΈ°λ₯

<br />

## π» μμ€ μ½λ

μ μ²΄ μ½λ λ³΄λ¬ κ°κΈ° π [Notion](https://imjone.notion.site/BearTalk-31aa513be24941818f2ee5c65ec71eef)

### π λ©μμ§ μ μ‘

`createElement` λ©μλλ₯Ό ν΅ν΄ μλ‘μ΄ DOM μμλ₯Ό μμ±ν ν,<br />
μ±νλ°© λ΄ μμ μμλ‘ μΆκ°νμ¬ λ©μμ§ μ μ‘ ν¨κ³Όλ₯Ό κ΅¬ννμμ΅λλ€.

```javascript
const chatScreen = document.querySelector('.chat_screen');
const textInput = document.querySelector('.chat_form-msg');

const newMsg = document.createElement('li');
newMsg.setAttribute('class', 'chat_content right');
newMsg.innerHTML = `
  <div class="chat_photo"></div>
  <div class="chat_bubble">${textInput.value}</div>`;

chatScreen.appendChild(newMsg);
newMsg.scrollIntoView({ block: 'center' });
textInput.value = '';
textInput.focus();
```

### π μ ν¨μ± κ²μ¬

`submit` μ΄λ²€νΈ λ°μ μ κ°λ¨ν μ ν¨μ±μ κ²μ¬λ₯Ό μ§ννλ©°,<br />
λ©μμ§μ°½μ μλ ₯λ νμ€νΈκ° κ³΅λ°± λΏμΌ κ²½μ° μλ¦Όμ°½μ λμλλ€.

```javascript
const chatForm = document.querySelector('.chat_form');

chatForm.addEventListener('submit', e => {
  e.preventDefault();
  if (textInput.value.trim() === '') {
    alert('λ©μμ§ λ΄μ©μ μλ ₯ν΄μ£ΌμΈμ.');
    textInput.value = '';
    return;
  }
});
```

<br />

## π λ°°μ΄ μ  λ° λλ μ 

- λΉ λ₯΄κ³  ν¨μ¨μ μΈ μ€νμΌλ§μ΄ κ°λ₯ν SCSS λ¬Έλ²μ λ§€λ ₯μ λκΌμ΅λλ€.
- λμ± λ€μνκ³  μ¬μ€μ μΈ UI μμ λ° κΈ°λ₯ κ΅¬νμ λν μμ¬μμ΄ λ§μ΄ λ¨μ΅λλ€.
- μνλ κΈ°λ₯μ μ΄λ€ μμΌλ‘ κ΅¬νν  μ μμμ§ κ³ λ―Όνλ©° νκ΅¬λ ₯μ κΈ°λ₯Ό μ μμμ΅λλ€.
