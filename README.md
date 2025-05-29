``` C++
#include <iostream>
#include <cstdint>
#include <vector>
#include <unordered_map>
#include <string>

class LunaticLegacy : public homo_sapiens {
public:
  static LunaticLegacy& getInstance() {
    static LunaticLegacy luna;
    return luna;
  }

private:
  static unordered_map<std::string, std::string> skillMap;

  LunaticLegacy() {
    skillMap = {
      {"有什么技能", "C++、Python（尤其torch），单片机一点的话玩过ESP32，前端会一点html、CSS、JS"},
      {"喜欢做什么", "摸鱼、发白丝、写点奇奇怪怪的小说文本（C++daisuki）"},
      {"计划中要学什么", "Lingua Latina, Esparanto, 日本語, More C++, 社交能力, etc."},
      {"一句话介绍一下你自己吧", "🐾一个摸鱼的大型猫科动物。"}
    }
  }

  // attributes
  int age() const { return 21; }
  std::string& gender() const { return std::string("femboy").substr(3); }

  // what happened if i'm dead
  ~LunaticLegacy(){
    std::terminate();
  }
}

```
