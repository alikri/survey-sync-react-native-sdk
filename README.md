# survey-sync-react-native-sdk

A React Native component designed by Survey Sync for seamlessly integrating surveys into your mobile applications.

## Installation

```sh
yarn add survey-sync-react-native-sdk
```

or

```sh
npm install survey-sync-react-native-sdk
```

## Usage

```js
import { Survey } from 'survey-sync-react-native-sdk';

const App = () => {
  const theme = 'dark';
  const onFinishedSurvey = (respondentId: string) => {
    console.log('Survey finished with respondentId:', respondentId);
  };

  return (
    <Survey surveyAlias="7TRpmpzR" onFinishedSurvey={onFinishedSurvey} theme={theme} />
  );
};
```

## Props
```
interface AppProps {
  surveyAlias: string;
  onFinishedSurvey?: (respondentId: string) => void;
  theme?: 'light' | 'dark';
}
```


## Contributing

See the [contributing guide](CONTRIBUTING.md) to learn how to contribute to the repository and the development workflow.

## License

MIT

---

Made with [create-react-native-library](https://github.com/callstack/react-native-builder-bob)