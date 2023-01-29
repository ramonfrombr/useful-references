## Run Tailwind watcher

`npm run dev:tailwind`

## Run app on browser

`npx expo start --web`

## Run app with new environment variables

`npx expo start --web --clear`

## Run the app on production mode

`npx expo start --no-dev --minify`

## Build installable apk for preview

`eas build -p android --profile preview`

## Push environment secrets to Expo

`eas secret:push --scope project --env-file .env`
