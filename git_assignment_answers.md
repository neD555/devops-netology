Ответы по заданию GIT Terraform

1 Полный хеш и комментарий коммита aefea
aefead2207ef7e2aa5dc81a34aedf0cad4c32545 Update CHANGELOG.md

2 Какому тегу соответствует 85024d3
v0.12.23

3 Сколько родителей у b8d720 и их хеши
2 родителя
56cd7859e05c36c06b56d013b55a252d0bb7e158
9ea88f22fc6269854151c571162c5bcf958bee2b

4 Коммиты между v0.12.23 и v0.12.24
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

5 Коммит где создана функция providerSource
8c928e8358 main: Consult local directories as potential mirrors of providers

6 Коммиты где изменялась функция globalPluginDirs
8364383c35 Push plugin discovery down into command package
7c4aeac5f3 stacks: load credentials from config file on startup (#35952)

7 Автор функции synchronizedWriters
Martin Atkins <mart@degeneration.co.uk>

Как получены ответы
git show -s --format="%H %s" aefea
git describe --tags --exact-match 85024d3
git show -s --format="%P" b8d720
git log --oneline v0.12.23..v0.12.24
git log -S"func providerSource(" --reverse --oneline
git log -G '^func globalPluginDirs' --oneline
git log -S"func synchronizedWriters(" --reverse --oneline и git show -s --format="%an <%ae>" ХЕШ
