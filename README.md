# 🛠 survey-sync-react-native-sdk 

A React Native component designed by [Survey Sync](https://survey-sync.com) for seamlessly integrating surveys into your mobile applications.

## 🤔 How to start?
- Sign in to [Survey Sync](https://survey-sync.com)
- Create Survey;
- Publish Survey;
- Extract alias and follow the instruction below.
  ![](https://github.com/alikri/survey-sync-assets/blob/main/survey-alias.png)

## 🔧 Installation

```sh
npm install survey-sync-react-native-sdk
```


## 📖 Usage

```js
interface SurveyProps {
  surveyAlias: string;
  onFinishedSurvey?: (respondentId: string) => void;
  theme?: 'light' | 'dark';
  searchParams?: Record<string, string | string[]>;
}
```

```js
import Survey from 'survey-sync-react-native-sdk';

const App = () => {

  const theme = 'dark';

  const alias = '7TRpmpzK' // your alias string 

  const searchParams = { testParam1: '1', testParam2: '2' } // your params

  const onFinishedSurvey = (respondentId: string) => {
    console.log('Survey finished with respondentId:', respondentId);
  };

  return (
    <Survey surveyAlias={alias} onFinishedSurvey={onFinishedSurvey} theme={theme} searchParams={searchParams} />
  );
};
```


## ⚙️ Typescript Settings:
If you encounter issues related to the 'moduleResolution' setting, add the following to your ```tsconfig.json```

```
{
  "compilerOptions": {
    "moduleResolution": "Bundler",
    "resolvePackageJsonImports": false
  }
}
```

## ⚙️ Potential issue in Expo App:
If you encounter issues related to the 'RNCMaterialDatePicker' it means that the native module for the material date picker isn’t included in your current Expo Go client. In previous versions, this module might have worked without extra configuration, but with the newer Expo client, native modules not built into Expo Go must be explicitly added.
To fix this, run:

```sh
npx expo install @react-native-community/datetimepicker react-native-modal-datetime-picker
```

## 💬 Contact

If you encounter any issues apart from the ones mentioned above during SDK installation, feel free to reach out on [Discord](https://discord.gg/GWCZThVX) – I'm happy to help!

## 💻 Contributing

See the [contributing guide](CONTRIBUTING.md) to learn how to contribute to the repository and the development workflow.

## License

MIT

---

Made with [create-react-native-library](https://github.com/callstack/react-native-builder-bob)
