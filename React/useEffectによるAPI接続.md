```
    useEffect(() => {
        const access_weather = async () => {
            const response = await fetch(
                `https://api.openweathermap.org/APPID=${
                    import.meta.env.VITE_WEATHER_API_KEY
                }`,
            )
            const body = await response.json()
            setWeathers(body)
            console.log(body)
        }
        return () => {
            access_weather()
        }
    }, [])
```
# 其１ APIKEYは.envファイルに格納！
VITEで環境を作った場合はVITE_で始まる文字で記述する。
```
//.env
VITE_WEATHER_API_KEY=rlniuahgl34875y875210
```
アクセスする際は、import.meta.env.つけた名前。
```
import.meta.env.VITE_WEATHER_API_KEY
```
.gitignoreには.envファイルを記述しておく。
```
*.env
```
