# Álláskereső és Toborzó Rendszer (Szakvizsga Projekt)
*Mark & Erik prod.*

Ez a projekt egy Python alapú, grafikus felhasználói felülettel (PySimpleGUI) ellátott álláskereső és toborzó alkalmazás. A rendszer tiszta objektumorientált (OOP) architektúrára épül, logikusan elkülönítve az adatmodelleket, az üzleti logikát és a felületet. 

Az alkalmazás két fő felhasználói kört és jogosultsági szintet szolgál ki:

- **Admin (Munkáltató):** 
  - Új álláshirdetéseket hozhat létre és törölhet meglévőket.
  - Listázhatja az összes pozíciót, vagy szűrheti őket adott részlegek (department) szerint.
  - Megtekintheti egy-egy konkrét pozícióra jelentkező személyek listáját.

- **Jelentkező (Applicant):** 
  - Böngészhet az elérhető állások között.
  - Jelentkezhet a kiválasztott pozíciókra (név és CV link megadásával).
  - Kereshet a legmagasabb fizetést kínáló állások között a megadott tapasztalati évek alapján (a háttérben Bubble Sort algoritmussal rendezve).

## Fájlok és Struktúra
- `entities.py`: Az adatmodellek (`Job`, `Applicant`) definíciója. Kapszulázva tárolja az állások és a jelentkezők tulajdonságait.
- `service.py`: Az üzleti logika (Service réteg). Ez felel a listák kezeléséért, a jelentkezések feldolgozásáért, valamint a rendezési és keresési funkciókért.
- `ui.py`: A PySimpleGUI alapú vizuális felület, amely biztosítja az interakciót a felhasználó és a háttérrendszer között.
