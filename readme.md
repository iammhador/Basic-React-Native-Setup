#### RUN PROJECT : npx expo start --tunnel

#### EXPO INSTALL AND TAILWIND PACKAGE INSTALL:

    npx create-react-native-app my-app
    cd my-app
    npm i nativewind
    npm i --dev tailwindcss

//# tailwind.config.js file

    module.exports = {
    content: ["./App.{js,jsx,ts,tsx}", "./screens/**/*.{js,jsx,ts,tsx}"],
    theme: {
        extend: {},
    },
    plugins: [],
    }

//# babel.config.js file

    module.exports = {
    plugins: ["nativewind/babel"],
    };

//# app.js starting code:

    import { StatusBar } from 'expo-status-bar';
    import React from 'react';
    import { Text, View } from 'react-native';

    export default function App() {
    return (
        <View className="flex-1 items-center justify-center bg-white">
            <Text>Open up App.js to start working on your app!</Text>
            <StatusBar style="auto" />
        </View>
        );
    }

#### Change expo version to 47.0.0. In terminal command npm init and initial a project. After that go to https://expo.dev/ website and create a project. Collect eas init id like this example " eas init --id 3cb3-c05a-4b10-872e-23ca3sqs1f79 " . Then run " eas build " . After completing the build, You will see a " app.json " and " eas.json " file. In the " app.json " file, You have to change " version and versionCode ". After that go to eas.json file. In the file you can add, In the development & production dependence to "autoIncrement": true," and run eas.build. More info on this site: " https://docs.expo.dev/archive/classic-updates/building-standalone-apps/ " .

#### When you first time build a project, expo build version and version code will get set automatically. You can check your project to use this link: " https://expo.dev/ "
