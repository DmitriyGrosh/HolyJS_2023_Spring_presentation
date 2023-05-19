---
---

<style>
.first-problem {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
  background-size: 100%;
  font-size: 3.2rem !important;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}

.text {
    font-size: 2rem !important;
}
</style>

<h1 class="first-problem">Что сделал Fiber ?</h1>


<div class="flex flex-col gap-4">
<div class="text" v-click>
    1. React выполняет работу в два основных этапа: render и commit.
</div>

<div class="text" v-click>
    2. Результатом фазы является дерево узлов Fiber, отмеченных побочными эффектами.
</div>

<div class="text" v-click>
    3. Работа на первом этапе render выполняется асинхронно.
</div>

<div class="text" v-click>
    4. Напротив, следующая фаза commit всегда синхронна.
</div>
</div>

---
src: ./34-histoty.md
---
