# Itay Fliess

**Software Lead @ Orbit 1690**

[GitHub](https://github.com/glitchfl) · [Email](mailto:itayfliss@gmail.com) · Discord `GlitchFL`

```dart
enum Level { specialist, workingKnowledge, basics }

enum WantToLearn { go, c, scala }

class Language {
  const Language(this.name, this.level);
  final String name;
  final Level level;
}

abstract class Developer {
  String get name;
  int get age;
  Future<void> build();
}

class Itay implements Developer {
  @override
  String get name => 'Itay Fliess';

  @override
  int get age => 17;

  static const role = 'Software Lead @ Orbit 1690';

  static const stack = [
    Language('Dart', Level.specialist),
    Language('Python', Level.specialist),
    Language('TypeScript', Level.specialist),
    Language('Shell', Level.workingKnowledge),
    Language('Java', Level.basics),
    Language('C#', Level.basics),
  ];

  static const nextUp = [WantToLearn.go, WantToLearn.c, WantToLearn.scala];

  static const interests = [
    'mathematical modeling',
    'statistics & probability',
    'anything with a state space worth searching',
  ];

  @override
  Future<void> build() async {
    while (true) {
      await learnSomething();
      ship();
    }
  }

  Future<void> learnSomething() async {}
  void ship() {}

  @override
  String toString() => '$name | $age | $role';
}

extension OffTheClock on Itay {
  Map<String, String> get elsewhere => const {
    'Valorant': 'peak Immortal 3',
    'Chess': '1700 elo',
    "Rubik's Cube": '15s avg (top 1% of solvers)',
  };
}

class Contact {
  static const discord = 'GlitchFL';
  static const github = '@glitchfl';
  static const email = 'itayfliss@gmail.com';
}

void main() {
  final me = Itay();

  print(me); // Itay Fliess | 17 | Software Lead @ Orbit 1690

  // @glitchfl | GlitchFL | itayfliss@gmail.com
  print('${Contact.github} | ${Contact.discord} | ${Contact.email}');

  me.build(); // still running
}
```
