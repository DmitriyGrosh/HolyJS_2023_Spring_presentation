---
---
<style>
.first-problem {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
  background-size: 100%;
  font-size: 3rem !important;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}

.text {
    font-size: 1.9rem !important;
}
</style>

<h1 class="first-problem">Transitions</h1>

<div v-click>
    1. Высокоприоритетная таска прерывает низкоприоритктную
</div>
<div v-click>
    2. Если компонент начала рендерится, то он должен дойти до return
</div>

<div v-click>
    3. Компонент нельзя прервать
</div>

<div v-click>
    4. Низкоприоритетные таски могут возвращать свой предыдущий стейт
</div>


---
src: ./55-transition-4-point.md
---
