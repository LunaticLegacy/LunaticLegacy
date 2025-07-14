``` C++
#include <iostream>
#include <cstdint>
#include <vector>
#include <unordered_map>
#include <string>

class homo_sapiens;

class LunaticLegacy : public homo_sapiens {
public:
  static LunaticLegacy& getInstance() {
    static LunaticLegacy luna;
    return luna;
  }

  void Nya() const {
    std::cout << NekoMimi << std::endl;
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
  std::string email() const { return "lunaticlegacy@163.com"; }
  std::string github_id() const { return "lunaticlegacy"; }
  std::string gitee_id() const { return "LunaNeko"; }

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
    {"有什么技能", "C++、Python（尤其torch），单片机一点的话玩过ESP32，前端会一点html、CSS、JS。"},
    {"喜欢做什么", "摸鱼、写代码、写点奇奇怪怪的小说文本（C++ daisuki）。"},
    {"计划中要学什么", "Lingua Latina, Esparanto, 日本語, More C++, Rust, Git怎么用, 社交能力, angular, etc."},
    {"正在面对什么", "本科GIS系毕业，即将启动计算机科学第二学位。"},
    {"一句话介绍一下你自己吧", "🐾一个摸鱼的大型猫科动物。"},
    {"为什么要用C++的方式介绍自己", "因为喜欢这种事情。"}
};
```
