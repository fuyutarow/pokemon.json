# pokemon.json

This is all the data for generations 1~8 of Pokémon.
The data is based on @SciresM's mining data, so the names of Form Changes and Mega-Syncers are 00-1 and so on.
Updates will be made as soon as I can observe @SciresM's mining data. (He is a famous data miner, so there will be almost no interruption in updates.)

## Credit
- [@ScriesM](https://twitter.com/sciresm)
- @dayu_282_


## References
https://pastebin.com/u/SciresM


## `pokemon.json`

- [en/pokemon.json](https://github.com/fuyutarow/pokemon.json/blob/master/en/pokemon.json)
- [ja/pokemon.json](https://github.com/fuyutarow/pokemon.json/blob/master/ja/pokemon.json)

### [schema.json](https://github.com/fuyutarow/pokemon.json/blob/master/schema.json)
```json:schema.json
{
  "$id": "http://json-schema.org/draft-04/schema#",
  "$schema": "http://json-schema.org/draft-04/schema#",
  "type": "object",
  "properties": {
    "no": {
      "type": "integer"
    },
    "name": {
      "type": "string"
    },
    "stage": {
      "type": "integer"
    },
    "galar_dex": {
      "type": "integer"
    },
    "base_stats": {
      "description": "HP, Attack, Defense, Sp.Attack, Sp.Defense, Speed",
      "type": "array",
      "minItems": 6,
      "maxItems": 6,
      "items": {
        "type": "integer"
      }
    },
    "ev_yeild": {
      "description": "effort value yield (When a Pokémon is defeated in battle, it will give effort values to the Pokémon that participated in the battle against it)",
      "type": "array",
      "minItems": 6,
      "maxItems": 6,
      "items": {
        "type": "integer"
      }
    },
    "gender-ratio": {
      "type": "integer"
    },
    "catch-rate": {
      "type": "integer"
    },
    "abilitiese": {
      "description": "ability1, ability2, hidden ability",
      "type": "array",
      "items": {
        "type": "string"
      }
    },
    "types": {
      "type": "array",
      "maxItems": 2,
      "items": {
        "type": "string"
      }
    },
    "items": {
      "type": "array",
      "items": [
        {
          "type": "string"
        },
        {
          "type": "integer"
        }
      ]
    },
    "exp-group": {
      "type": "string"
    },
    "egg-group": {
      "type": "array",
      "items": {
        "type": "string"
      }
    },
    "height": {
      "type": "number"
    },
    "weight": {
      "type": "number"
    },
    "color": {
      "description": "main color of Pokémon (the most used color)",
      "type": "string"
    },
    "evolutions": {
      "type": "array",
      "items": {
        "properties": {
          "species": {
            "type": "string"
          },
          "method": {
            "type": "string"
          },
          "method_value": {
            "type": "string"
          }
        }
      }
    },
    "level_up_moves": {
      "type": "array",
      "items": [
        {
          "type": "integer"
        },
        {
          "type": "string"
        }
      ]
    },
    "tms": {
      "description": "Technical Machines",
      "type": "array",
      "items": [
        {
          "type": "integer"
        },
        {
          "type": "string"
        }
      ]
    },
    "egg-moves": {
      "type": "array",
      "items": {
        "type": "string"
      }
    },
    "trs": {
      "description": "Technical Records",
      "type": "array",
      "items": [
        {
          "type": "integer"
        },
        {
          "type": "string"
        }
      ]
    }
  }
}
```

---


[8世代対応全ポケモンの.jsonファイルを作ってみた](https://qiita.com/dayu_282_/items/f03edc0f4266c5d67d69)


## pokemon-data.json
１~8世代までのすべてのデータです。英語版と日本語版を作成したのでご自由にお使いください。
また、 @SciresM 氏のマイニングデータを参考にしているのでフォルムチェンジとかメガシンカなどの
名称は〇〇-1などになります。アップデートは @SciresM 氏などのマイニングデータを観測でき次第随時アップデートします。
(有名なデータマイナーなのでほぼ更新は途絶えることはないでしょう。)またこのデータは教育目的として作成しましたので予めご了承ください。

## 収集データ※上から順番に
- 図鑑ナンバー(全国)※891番以降はフォルムナンバーです。
- ポケモン名
- 進化階層
- 図鑑ナンバー(ガラル)
- 種族値
- 倒したときに貰える種族値
- 性比
- 捕獲率
- 特性(通常1/通常2/夢)
- タイプ
- 成長速度のカテゴリー
- タマゴグループ
- タマゴ歩数(何歩でタマゴが孵化できるか)
- 高さ
- 重さ
- ポケモンの主な色(一番使われている色)
- 進化先/進化方法
- レベル技
- タマゴ技
- わざマシン(tms)
- わざレコード(trs)

## 間違いなどの報告
英語版のファイルはほぼ間違いはないとは思いますが日本語ファイルは置換スクリプトを走らせて変換
させたので変な名称になっている場合があるので間違いを報告する場合は @dayu_282_ までリプライまたは
DMを飛ばしてください。
