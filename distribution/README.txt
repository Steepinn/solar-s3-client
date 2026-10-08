Файлы для раздачи игрокам через GitHub (raw + Releases).

1) python tools/publish_distribution.py --base-url https://github.com/ORG/REPO/releases/download/pack-mods --workshop-base https://github.com/ORG/REPO/releases/download/workshop-mods

2) Залей distribution/jars/*.jar в Release "pack-mods"
   и distribution/workshop-jars/*.jar в Release "workshop-mods"

3) Закоммить distribution/manifest.json и distribution/community_mods.catalog.json

4) В config.json у игроков:
   manifest.mode = github
   manifest.url = raw URL на manifest.json
   community_mods.catalog_url = raw URL на community_mods.catalog.json
   community_mods.auto_install_catalog_on_sync = true
