``` C++
#include <iostream>
#include <cstdint>
#include <vector>
#include <unordered_map>
#include <string>

extern class homo_sapiens {};

class LunaticLegacy : public homo_sapiens {
public:
  static LunaticLegacy& getInstance() {
    static LunaticLegacy luna;
    return luna;
  }

  void Nya() const {
    std::cout << LunaticLegacy::NekoMimi;
  }

private:
  static unordered_map<std::string, std::string> skillMap;

  // me.
  LunaticLegacy() {
    Nya();
  };

  // attributes
  int age() const { return 21; }
  std::string gender() const { return std::string("femboy").substr(3); }
  std::string email() const { return "lunaticlegacy@163.com" }

  // needing
  virtual void* findFriend() = 0;
  virtual void* waifu() = 0;

  // support for nya
  static constexpr const char* NekoMimi =
        "   /\\_/\\\n"
        "  ( o.o )\n"
        "   > ^ <\n"
  ;

  // what happened if i'm dead
  virutal ~LunaticLegacy() {
    std::terminate();
  }
}

std::unordered_map<std::string, std::string> LunaticLegacy::skillMap = {
    {"有什么技能", "C++、Python（尤其torch），单片机一点的话玩过ESP32，前端会一点html、CSS、JS"},
    {"喜欢做什么", "摸鱼、发白丝、写点奇奇怪怪的小说文本（C++daisuki）"},
    {"计划中要学什么", "Lingua Latina, Esparanto, 日本語, More C++, Git怎么用, 社交能力, etc."},
    {"正在面对什么", "毕业论文喵！！我要疯了喵嗷嗷嗷嗷啊啊啊啊啊——"}.
    {"一句话介绍一下你自己吧", "🐾一个摸鱼的大型猫科动物。"}
};
```
