### 1. Найдите полный хеш и комментарий коммита, хеш которого начинается на aefea

git show -s --format="%H %s" aefea

### Ответ:
aefead2207ef7e2aa5dc81a34aedf0cad4c32545 Update CHANGELOG.md

### 2. Какому тегу соответствует коммит 85024d3

git describe --tags --exact-match 85024d3 2>/dev/null || git tag --contains 85024d3

### Ответ:
v0.12.23

### 3. Сколько родителей у коммита b8d720 и их хеши

git show -s --format="%P" b8d720

### Ответ:
2 родителя
56cd7859e05c36c06b56d013b55a252d0bb7e158
9ea88f22fc6269854151c571162c5bcf958bee2b

###  4. Перечислите хеши и комментарии всех коммитов между тегами v0.12.23 и v0.12.24

git log --oneline v0.12.23..v0.12.24

###  Ответ:
225466bc3e Cleanup after v0.12.23 release
dd01a35078 Update CHANGELOG.md
4b6d06cc5d Update CHANGELOG.md
d5f9411f51 command: Fix bug when using terraform login on Windows
06275647e2 Update CHANGELOG.md
5c619ca1ba website: Remove links to the getting started guide's old location
6ae64e247b registry: Fix panic when server is unreachable
3f235065b9 Update CHANGELOG.md
b14b74c493 [Website] vmc provider links
33ff1c03bb v0.12.24

### 5. Найдите коммит, в котором была создана функция func providerSource(...)

git log -S"func providerSource(" --reverse --oneline | head -n1

### Ответ:
8c928e8358 main: Consult local directories as potential mirrors of providers

### 6. Найдите все коммиты, в которых была изменена функция globalPluginDirs

git log -G '^func globalPluginDirs' --oneline

### Ответ:
8364383c35 Push plugin discovery down into command package
7c4aeac5f3 stacks: load credentials from config file on startup (#35952)

### 7. Кто автор функции synchronizedWriters

FIRST=$(git log -S"func synchronizedWriters(" --reverse --format="%H" | head -n1)
git show -s --format="%an <%ae>" "$FIRST"

### Ответ:
Martin Atkins mart@degeneration.co.uk
