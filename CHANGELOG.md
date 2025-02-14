# ChangeLog

## 0.5

### 0.5.4

- Fix incorrect index creation order. (#151)
- Not catch exception when import config. (#164)
- Support `drop column` for sqlite. (#40)

### 0.5.3

- Fix postgre alter null. (#142)
- Fix default function when migrate. (#147)

### 0.5.2

- Fix rename field on the field add. (#134)
- Fix postgres field type change error. (#135)
- Fix inspectdb for `FloatField`. (#138)
- Support `rename table`. (#139)

### 0.5.1

- Fix tortoise connections not being closed properly. (#120)
- Fix bug for field change. (#119)
- Fix drop model in the downgrade. (#132)

### 0.5.0

- Refactor core code, now has no limitation for everything.

## 0.4

### 0.4.4

- Fix unnecessary import. (#113)

### 0.4.3

- Replace migrations separator to sql standard comment.
- Add `inspectdb` command.

### 0.4.2

- Use `pathlib` for path resolving. (#89)
- Fix upgrade in new db. (#96)
- Fix packaging error. (#92)

### 0.4.1

- Bug fix. (#91 #93)

### 0.4.0

- Use `.sql` instead of `.json` to store version file.
- Add `rename` column support MySQL5.
- Remove callable detection for defaults. (#87)
- Fix `sqlite` stuck. (#90)

## 0.3

### 0.3.3

- Fix encoding error. (#75)
- Support multiple databases. (#68)
- Compatible with models file in directory. (#70)

### 0.3.2

- Fix migrate to new database error. (#62)

### 0.3.1

- Fix first version error.
- Fix init error. (#61)

### 0.3.0

- Refactoring migrate logic, and this version is not compatible with previous version.
- Now there don't need `old_models.py` and it store in database.
- Upgrade steps:
    1. Upgrade aerich version.
    2. Drop aerich table in database.
    3. Delete `migrations/{app}` folder and rerun `aerich init-db`.
    4. Update model and `aerich migrate` normally.

## 0.2

### 0.2.5

- Fix windows support. (#46)
- Support `db_constraint` in fk, m2m should manual define table with fk. (#52)

### 0.2.4

- Raise error with SQLite unsupported features.
- Fix Postgres alter table. (#48)
- Add `Rename` support.

### 0.2.3

- Fix tortoise ssl config.
- PostgreSQL add/drop index/unique.

### 0.2.2

- Fix postgres drop fk.
- Fix version sort.

### 0.2.1

- Fix bug in windows.
- Enhance PostgreSQL support.

### 0.2.0

- Update model file find method.
- Set `--safe` bool.

## 0.1

### 0.1.9

- Fix default_connection when upgrade
- Find default app instead of default.
- Diff MySQL ddl.
- Check tortoise config.

### 0.1.8

- Fix upgrade error when migrate.
- Fix init db sql error.
- Support change column.

### 0.1.7

- Exclude models.Aerich.
- Add init record when init-db.
- Fix version num str.

### 0.1.6

- update dependency_links

### 0.1.5

- Add sqlite and postgres support.
- Fix dependency import.
- Store versions in db.

### 0.1.4

- Fix transaction and fields import.
- Make unique index worked.
- Add cli --version.

### 0.1.3

- Support indexes and unique_together.

### 0.1.2

- Now aerich support m2m.
- Add cli cmd init-db.
- Change cli options.

### 0.1.1

- Now aerich is basic worked.
