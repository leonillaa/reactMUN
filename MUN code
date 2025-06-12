// App.js
import React, { useState } from 'react';
import {
  View,
  Text,
  StyleSheet,
  TextInput,
  TouchableOpacity,
  FlatList,
  ScrollView,
} from 'react-native';
import { NavigationContainer } from '@react-navigation/native';
import { createNativeStackNavigator } from '@react-navigation/native-stack';
import { createBottomTabNavigator } from '@react-navigation/bottom-tabs';
import MaterialCommunityIcons from 'react-native-vector-icons/MaterialCommunityIcons';
import Checkbox from 'expo-checkbox';

function PrepScreen() {
  const [steps, setSteps] = useState({
    research: false,
    positionPaper: false,
    speech: false,
    rules: false,
    suit: false,
    allies: false,
    strategy: false,
    notes: false,
    questions: false,
    logistics: false,
    registration: false,
    rehearsal: false,
    documents: false,
    confidence: false,  
  });

  const checklist = {
   research: 'Досліджено тему комітету',
positionPaper: 'Написано позицію (Position Paper)',
speech: 'Підготовлено промову (Opening Speech)',
rules: 'Вивчено правила процедури',
suit: 'Підготовано діловий одяг',
allies: 'Визначено союзників',
strategy: 'Складено стратегію дебатів',
notes: 'Підготовлено нотатки',
questions: 'Підготовлено відповіді на можливі питання',
logistics: 'Вирішено питання логістики',
registration: 'Зареєстровано участь',
rehearsal: 'Проведено репетицію промови',
documents: 'Підготовлено всі необхідні документи',
confidence: 'МОРАЛЬНО ПІДГОТОВЛЕНИЙ!!!!!',

  };

  const toggleStep = (key) => {
    setSteps((prev) => ({ ...prev, [key]: !prev[key] }));
  };

  return (
    <ScrollView contentContainerStyle={styles.container}>
      <Text style={styles.title}>Чеклист підготовки до MUN</Text>
      {Object.keys(checklist).map((key) => (
        <View key={key} style={styles.product}>
          <Checkbox
            value={steps[key]}
            onValueChange={() => toggleStep(key)}
            color={steps[key] ? 'green' : undefined}
            style={styles.checkbox}
          />
          <View style={styles.productInfo}>
            <Text style={styles.name}>{checklist[key]}</Text>
          </View>
        </View>
      ))}
    </ScrollView>
  );
}

// ===
function ScheduleScreen() {
  return (
    <ScrollView contentContainerStyle={styles.container}>
      <Text style={styles.title}>Розклад</Text>

      <View style={styles.scheduleDay}>
        <Text style={styles.dayTitle}>День 1 — 15 лютого (IST)</Text>
        <Text style={styles.scheduleItem}>14:00 – 14:15  • Відкриття конференції</Text>
        <Text style={styles.scheduleItem}>14:30 – 15:30  • Сесія 1</Text>
        <Text style={styles.scheduleItem}>15:45 – 16:45  • Перерва</Text>
        <Text style={styles.scheduleItem}>17:15 – 18:00  • Сесія 2</Text>
        <Text style={styles.scheduleItem}>18:00 – 18:30  • Перерва</Text>
        <Text style={styles.scheduleItem}>18:30 – 20:30  • Сесія 3</Text>
      </View>

      <View style={styles.scheduleDay}>
        <Text style={styles.dayTitle}>День 2 — 16 лютого (IST)</Text>
        <Text style={styles.scheduleItem}>14:30 – 15:30  • Сесія 1</Text>
        <Text style={styles.scheduleItem}>15:30 – 16:30  • Перерва</Text>
        <Text style={styles.scheduleItem}>16:30 – 17:30  • Сесія 2</Text>
        <Text style={styles.scheduleItem}>17:30 – 17:45  • Перерва</Text>
        <Text style={styles.scheduleItem}>17:45 – 18:45  • Сесія 3 + МОЕ</Text>
        <Text style={styles.scheduleItem}>18:45 – 19:45  • Закриття конференції</Text>
      </View>

      <Text style={styles.note}>
        * Усі часові позначення — за індійським стандартним часом (IST). Можливо, це буде попередній день у вашому часовому поясі.
      </Text>
    </ScrollView>
  );
}

function NotesScreen() {
  return (
    <ScrollView style={{ padding: 20 }}>
      <Text style={{ fontSize: 20, fontWeight: 'bold', marginBottom: 10 }}>
        Нотатки для новачків МАН-конференції
      </Text>

      <Text style={{ fontSize: 16, fontWeight: '600', marginTop: 10 }}>
        Основні комітети та їх абревіатури:
      </Text>

      <Text style={{ fontWeight: '600', marginTop: 10 }}>1. UNSC — United Nations Security Council</Text>
      <Text>Рада Безпеки ООН. Суть: Найважливіший комітет, що займається миром і безпекою.</Text>

      <Text style={{ fontWeight: '600', marginTop: 10 }}>2. UNGA — United Nations General Assembly</Text>
      <Text>Генеральна Асамблея ООН. Суть: Обговорення глобальних питань усіма країнами-членами.</Text>

      <Text style={{ fontWeight: '600', marginTop: 10 }}>3. ECOSOC — Economic and Social Council</Text>
      <Text>Економічна та соціальна рада ООН. Суть: Економіка, соціальна справедливість, охорона здоров’я.</Text>

      <Text style={{ fontWeight: '600', marginTop: 10 }}>4. WHO — World Health Organization</Text>
      <Text>Всесвітня організація охорони здоров’я. Суть: Здоров’я, епідемії, медичні стандарти.</Text>

      <Text style={{ fontWeight: '600', marginTop: 10 }}>5. UNHRC — United Nations Human Rights Council</Text>
      <Text>Рада з прав людини. Суть: Захист прав людини, розслідування порушень.</Text>

      <Text style={{ fontWeight: '600', marginTop: 10 }}>6. DISEC — Disarmament and International Security Committee</Text>
      <Text>Комітет з роззброєння. Суть: Озброєння, безпека, контроль над зброєю.</Text>

      <Text style={{ fontSize: 16, fontWeight: '600', marginTop: 20 }}>
        Основні поняття:
      </Text>

      <Text style={{ fontWeight: '600', marginTop: 10 }}>Позиційний папір</Text>
      <Text>Документ із позицією країни щодо питання. Проблеми, позиція, пропозиції.</Text>

      <Text style={{ fontWeight: '600', marginTop: 10 }}>Промова</Text>
      <Text>Усне звернення делегата. Має бути чітке, аргументоване, коротке.</Text>

      <Text style={{ fontWeight: '600', marginTop: 10 }}>Резолюція</Text>
      <Text>Офіційне рішення комітету щодо обговорюваного питання.</Text>

      <Text style={{ fontWeight: '600', marginTop: 10 }}>Формальні/неформальні дебати</Text>
      <Text>Формальні — за регламентом. Неформальні — для переговорів і коаліцій.</Text>

      <Text style={{ fontSize: 16, fontWeight: '600', marginTop: 20 }}>
        Корисні поради:
      </Text>
      <Text>
        - Вивчи документи своєї країни.{"\n"}
        - Пиши логічний позиційний папір.{"\n"}
        - Виступай впевнено.{"\n"}
        - Слухай інших делегатів.{"\n"}
        - Не бійся говорити.
      </Text>
    </ScrollView>
  );
}



function TipsScreen() {
  const tips = [
    'Ретельно підготуй свою позицію заздалегідь.',
    'Слухай інших делегатів уважно.',
    'Говори чітко і впевнено.',
    'Пам’ятай про правила процедури.',
    'Підготуй коротку, але змістовну промову.',
    'Не бійтеся задавати питання.',
    'Співпрацюй зі своїми союзниками.',
    'Будь ввічливим і професійним.',
    'Звертай увагу на невербальну комунікацію.',
    'Відпочивай та слідкуй за своїм настроєм.',
  ];

  const [currentTip, setCurrentTip] = useState(null);

  const showRandomTip = () => {
    const randomIndex = Math.floor(Math.random() * tips.length);
    setCurrentTip(tips[randomIndex]);
  };

  return (
    <View style={styles.container}>
      <Text style={styles.title}>Поради</Text>

      <TouchableOpacity style={styles.button} onPress={showRandomTip}>
        <Text style={styles.buttonText}>Показати пораду</Text>
      </TouchableOpacity>

      {currentTip && <Text style={styles.tipText}>{currentTip}</Text>}
    </View>
  );
}

// ===
const countries = [
  {
    name: 'України',
    committees: {
      UNSC: 'Україна виступає за міжнародну підтримку у конфліктах. Вимагає санкцій проти агресорів',
      DISEC: 'Підтримує роззброєння і міжнародний контроль за зброєю. Закликає до заборони поставок зброї в зони конфлікту.',
      UNHRC: 'Наголошує на порушеннях прав людини на окупованих територіях. Просить про міжнародну допомогу переселенцям.',
      WHO: 'Потребує медичної допомоги для постраждалих регіонів. Працює над відновленням системи охорони здоров’я.',
      ECOSOC: 'Просить підтримки у післявоєнному економічному відновленні. Зацікавлена у міжнародних інвестиціях.',
      SOCHUM: 'Захищає права меншин і внутрішньо переміщених осіб. Підтримує освіту та культуру навіть під час війни.',
      UNEP: 'Боротьба з екологічними наслідками війни — пріоритет. Підтримує міжнародні програми з відновлення довкілля.',
    },
  },
  {
    name: 'США',
    committees: {
      UNSC: 'Підтримує глобальну безпеку і часто ініціює резолюції. Виступає за санкції проти країн-порушників.',
      DISEC: 'Проти розповсюдження зброї масового знищення. Підтримує модернізацію оборонних систем.',
      UNHRC: 'Захищає свободу слова та релігії. Виступає за покарання за грубі порушення прав людини.',
      WHO: 'Фінансує медичні дослідження і вакцинацію. Допомагає країнам, що розвиваються.',
      ECOSOC: 'Підтримує сталий розвиток і цифровізацію. Працює над глобальною освітою.',
      SOCHUM: 'Активно бореться з расизмом і дискримінацією. Просуває права ЛГБТ+ спільноти.',
      UNEP: 'Лідер у боротьбі з кліматичними змінами. Підтримує перехід до чистої енергії.',
    },
  },
  {
    name: 'Китая',
    committees: {
      UNSC: 'Часто утримується в голосуваннях. Підтримує стабільність і невтручання.',
      DISEC: 'Виступає за роззброєння, але проти зовнішнього тиску. Розвиває власну оборону.',
      UNHRC: 'Вважає, що кожна країна має право сама вирішувати внутрішні справи. Заперечує звинувачення у порушеннях.',
      WHO: 'Активно допомагає країнам Азії. Працює над профілактикою хвороб.',
      ECOSOC: 'Інвестує в інфраструктуру країн, що розвиваються. Просуває програму "Один пояс – один шлях".',
      SOCHUM: 'Підтримує культурне різноманіття. Проти втручання у свої внутрішні політики.',
      UNEP: 'Прагне зменшити викиди CO₂. Розвиває зелений транспорт та енергію.',
    },
  },
  {
    name: 'Канади',
    committees: {
      UNSC: 'Підтримує дипломатичні шляхи вирішення конфліктів. Виступає за миротворчі місії.',
      DISEC: 'Підтримує міжнародний контроль над озброєннями. Проти поширення зброї серед цивільного населення.',
      UNHRC: 'Активно підтримує права жінок, меншин і ЛГБТ+. Працює з переселенцями та біженцями.',
      WHO: 'Розвиває охорону здоров’я у бідних країнах. Підтримує вакцинацію.',
      ECOSOC: 'Вкладає в освіту та гендерну рівність. Працює над подоланням бідності.',
      SOCHUM: 'Захищає свободу віросповідання та вираження. Підтримує інклюзивне суспільство.',
      UNEP: 'Боротьба з глобальним потеплінням — пріоритет. Захищає ліси та водойми.',
    },
  },
  {
    name: 'Німмеччини',
    committees: {
      UNSC: 'Підтримує санкції та мирні переговори. Проти агресивних дій.',
      DISEC: 'Пропонує контроль за експортом озброєння. Підтримує роззброєння у конфліктних зонах.',
      UNHRC: 'Виступає за захист прав біженців. Підтримує незалежні розслідування порушень.',
      WHO: 'Інвестує у вакцини і профілактику. Допомагає країнам Європи та Африки.',
      ECOSOC: 'Просуває цифрову економіку. Підтримує зелену енергетику.',
      SOCHUM: 'Захищає свободи і толерантність. Працює над культурною інтеграцією.',
      UNEP: 'Активно бореться зі зміною клімату. Лідер у відновлюваній енергетиці.',
    },
  },
  {
    name: 'Бразилії',
    committees: {
      UNSC: 'Закликає до діалогу і мирних ініціатив. Проти зовнішнього тиску на регіон.',
      DISEC: 'Підтримує контроль над зброєю, але захищає нацбезпеку. Проти втручання у внутрішні справи.',
      UNHRC: 'Працює над правами корінних народів. Боротьба з соціальною нерівністю — пріоритет.',
      WHO: 'Фокусується на боротьбі з тропічними хворобами. Підтримує медичну інфраструктуру.',
      ECOSOC: 'Розвиває аграрний сектор і освіту. Підтримує сталий розвиток.',
      SOCHUM: 'Працює над правами жінок та молоді. Проти расової дискримінації.',
      UNEP: 'Захищає тропічні ліси. Боротьба з незаконною вирубкою — головна ціль.',
    },
  },
  {
    name: 'Афганістану',
    committees: {
      UNSC: 'Потребує підтримки у боротьбі з тероризмом. Закликає до стабільності.',
      DISEC: 'Хоче допомоги у роззброєнні бойових груп. Прагне міжнародної безпеки.',
      UNHRC: 'Підтримує права жінок та освіту для дівчат. Потребує захисту цивільного населення.',
      WHO: 'Потребує медичної допомоги та вакцин. Система охорони здоров’я нестабільна.',
      ECOSOC: 'Залежить від гуманітарної підтримки. Прагне відбудови економіки.',
      SOCHUM: 'Боротьба з насильством над жінками — ключова тема. Права дітей — пріоритет.',
      UNEP: 'Має проблеми з дефіцитом води. Потребує допомоги у збереженні довкілля.',
    },
  },
];

function CountryListScreen({ navigation }) {
  return (
    <View style={styles.container}>
      <Text style={styles.title}>Оберіть країну:</Text>
      <FlatList
        data={countries}
        keyExtractor={(item) => item.name}
        renderItem={({ item }) => (
          <TouchableOpacity
            style={styles.button}
            onPress={() => navigation.navigate('CommitteeSelect', { country: item })}
          >
            <Text style={styles.buttonText}>{item.name}</Text>
          </TouchableOpacity>
        )}
      />
    </View>
  );
}

function CommitteeSelect({ route, navigation }) {
  const { country } = route.params;

  return (
    <View style={styles.container}>
      <Text style={styles.title}>Комітети для {country.name}:</Text>
      {Object.keys(country.committees).map((committee) => (
        <TouchableOpacity
          key={committee}
          style={styles.button}
          onPress={() =>
            navigation.navigate('PositionView', {
              countryName: country.name,
              committeeName: committee,
              position: country.committees[committee],
            })
          }
        >
          <Text style={styles.buttonText}>{committee}</Text>
        </TouchableOpacity>
      ))}
    </View>
  );
}

function PositionView({ route }) {
  const { countryName, committeeName, position } = route.params;

  return (
    <ScrollView contentContainerStyle={styles.container}>
      <Text style={styles.title}>
        Позиція {countryName} в {committeeName}
      </Text>
      <Text style={styles.text}>{position}</Text>
    </ScrollView>
  );
}

const CountryStack = createNativeStackNavigator();
function CountryScreen() {
  return (
    <CountryStack.Navigator screenOptions={{ headerShown: false }}>
      <CountryStack.Screen name="CountryList" component={CountryListScreen} />
      <CountryStack.Screen name="CommitteeSelect" component={CommitteeSelect} />
      <CountryStack.Screen name="PositionView" component={PositionView} />
    </CountryStack.Navigator>
  );
}

// =====
const Tab = createBottomTabNavigator();
function AppTabs() {
  return (
    <Tab.Navigator
      screenOptions={({ route }) => ({
        headerShown: false,
        tabBarIcon: ({ color, size }) => {
          let iconName;
          if (route.name === 'Підготовка') iconName = 'book-open-outline';
          else if (route.name === 'Країни') iconName = 'flag-outline';
          else if (route.name === 'Розклад') iconName = 'calendar';
          else if (route.name === 'Нотатки') iconName = 'notebook-outline';
          else if (route.name === 'Порада') iconName = 'lightbulb-outline';
          return <MaterialCommunityIcons name={iconName} size={size} color={color} />;
        },
      })}
    >
      <Tab.Screen name="Підготовка" component={PrepScreen} />
      <Tab.Screen name="Країни" component={CountryScreen} />
      <Tab.Screen name="Розклад" component={ScheduleScreen} />
      <Tab.Screen name="Нотатки" component={NotesScreen} />
      <Tab.Screen name="Порада" component={TipsScreen} />
    </Tab.Navigator>
  );
}

// ========== Login Screen ==========
function LoginScreen({ navigation }) {
  const [username, setUsername] = useState('');
  const [password, setPassword] = useState('');

  const handleLogin = () => {
    if (username && password) {
      navigation.replace('MainApp');
    } else {
      alert('Будь ласка, введіть логін і пароль');
    }
  };

  return (
    <View style={styles.container}>
      <Text style={styles.title}>Додаток для MUN конференції ''Створений за мотивами існуючої конференції''</Text>
      <TextInput
        style={styles.input}
        placeholder="Логін"
        value={username}
        onChangeText={setUsername}
      />
      <TextInput
        style={styles.input}
        placeholder="Пароль"
        value={password}
        onChangeText={setPassword}
        secureTextEntry
      />
      <TouchableOpacity onPress={handleLogin} style={styles.button}>
        <Text style={styles.buttonText}>Увійти</Text>
      </TouchableOpacity>
    </View>
  );
}

// ========== Root Stack ==========
const RootStack = createNativeStackNavigator();
export default function App() {
  return (
    <NavigationContainer>
      <RootStack.Navigator screenOptions={{ headerShown: false }}>
        <RootStack.Screen name="Login" component={LoginScreen} />
        <RootStack.Screen name="MainApp" component={AppTabs} />
      </RootStack.Navigator>
    </NavigationContainer>
  );
}

const styles = StyleSheet.create({
  container: {
    flex: 1,
    backgroundColor: '#FDF9F2',
    alignItems: 'center',
    justifyContent: 'center',
    padding: 20,
  },
  title: {
    fontSize: 22,
    marginBottom: 20,
    fontWeight: '600',
    textAlign: 'center',
  },
  button: {
    backgroundColor: '#6D4C41',
    padding: 12,
    marginVertical: 8,
    borderRadius: 10,
    width: '80%',
  },
  buttonText: {
    color: 'white',
    fontSize: 16,
    textAlign: 'center',
  },
  text: {
    fontSize: 16,
    padding: 15,
    textAlign: 'center',
  },
  input: {
    borderWidth: 1,
    borderColor: '#999',
    borderRadius: 8,
    padding: 10,
    width: '80%',
    marginVertical: 10,
    backgroundColor: '#fff',
  },
  product: {
    flexDirection: 'row',
    alignItems: 'center',
    borderWidth: 1,
    borderColor: 'rgb(163, 122, 83)',
    borderRadius: 15,
    backgroundColor: 'rgb(246, 236, 223)',
    padding: 10,
    marginBottom: 15,
    width: '100%',
  },
  checkbox: {
    marginRight: 10,
  },
  productInfo: {
    flexDirection: 'column',
  },
  name: {
    fontSize: 16,
  },
scheduleDay: {
  backgroundColor: '#FFF8E1',
  borderRadius: 16,
  padding: 16,
  marginVertical: 10,
  width: '100%',
  shadowColor: '#000',
  shadowOffset: { width: 0, height: 2 },
  shadowOpacity: 0.1,
  shadowRadius: 4,
},
dayTitle: {
  fontSize: 20,
  fontWeight: '700',
  color: '#5D4037',
  marginBottom: 8,
  textAlign: 'center',
},
scheduleItem: {
  fontSize: 16,
  paddingVertical: 4,
  color: '#3E2723',
  textAlign: 'left',
},
note: {
  fontSize: 14,
  fontStyle: 'italic',
  color: '#6D4C41',
  marginTop: 20,
  textAlign: 'center',
  
},


  
});
