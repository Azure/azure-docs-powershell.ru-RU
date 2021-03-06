---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewaybackendhttpsettings
schema: 2.0.0
ms.openlocfilehash: f4c4ccdce719b3593968f0429d5e02936d052cc4
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914066"
---
# New-AzureRmApplicationGatewayBackendHttpSettings

## КРАТКИй обзор
Создает серверные параметры HTTP для шлюза приложения.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
New-AzureRmApplicationGatewayBackendHttpSettings -Name <String> -Port <Int32> -Protocol <String>
 -CookieBasedAffinity <String> [-RequestTimeout <Int32>]
 [-ConnectionDraining <PSApplicationGatewayConnectionDraining>] [-ProbeId <String>]
 [-Probe <PSApplicationGatewayProbe>]
 [-AuthenticationCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate]>]
 [-PickHostNameFromBackendAddress] [-HostName <String>] [-AffinityCookieName <String>] [-ProbeEnabled]
 [-Path <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет New-AzureRmApplicationGatewayBackendHttpSettings создает серверные параметры HTTP для шлюза приложения.
Серверные параметры HTTP применяются ко всем внутренним серверам в пуле.

## ИЛЛЮСТРИРУЮТ

### Пример 1: Создание HTTP-параметров для серверной части
```
PS C:\>$Setting = New-AzureRmApplicationGatewayBackendHttpSettings -Name "Setting01" -Port 80 -Protocol Http -CookieBasedAffinity Disabled
```

Эта команда создает серверные параметры HTTP с именем Setting01 на порте 80, используя HTTP-протокол с отключенным сходством на основе файлов cookie.
Параметры хранятся в переменной $Setting.

## ПАРАМЕТРЫ

### -AffinityCookieName
Имя cookie-файла, используемое для файла cookie схожести

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AuthenticationCertificates
Определяет сертификаты проверки подлинности для шлюза приложений.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ConnectionDraining
Сток подключений для ресурса внутренних HTTP-параметров.

```yaml
Type: PSApplicationGatewayConnectionDraining
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CookieBasedAffinity
Указывает, следует ли включить или отключить сходство на основе файлов cookie для серверного пула.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HostName
Задает заголовок hosts, который будет отправляться внутренним серверам.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (имя)
Задает имена серверных параметров HTTP, создаваемых этим командлетом.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Path
Путь, который должен использоваться в качестве префикса для всех HTTP-запросов.
Если для этого параметра не задано значение, путь не будет иметь префикса.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PickHostNameFromBackendAddress
Флаг, если заголовок узла должен быть выбран из имени узла внутреннего сервера.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Port (порт)
Указывает порт пула серверов с внутренними интерфейсами.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Зонд
Указывает зонд для связи с серверным пулом.

```yaml
Type: PSApplicationGatewayProbe
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProbeEnabled
Флажок, если зонд должен быть включен.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProbeId
Указывает идентификатор зонда для связи с серверным пулом.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Protocol (протокол)
Указывает протокол для обмена данными между шлюзом приложения и внутренними серверами.
Допустимые значения этого параметра: HTTP и HTTPS.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Http, Https

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RequestTimeout
Указывает значение времени ожидания запроса.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### System. String

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendHttpSettings

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Add-AzureRmApplicationGatewayBackendHttpSettings]()

[Get-AzureRmApplicationGatewayBackendHttpSettings]()

[Remove-AzureRmApplicationGatewayBackendHttpSettings]()

[Set-AzureRmApplicationGatewayBackendHttpSettings]()

