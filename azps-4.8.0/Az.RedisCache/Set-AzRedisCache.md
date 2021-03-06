---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 6234F211-6ED4-443F-9B83-DEB9AC51B763
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/set-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Set-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Set-AzRedisCache.md
ms.openlocfilehash: 5cb3723e95acbc05b5fffce55a1f768c8a3b7fba
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235926"
---
# Set-AzRedisCache

## КРАТКИй обзор
Изменяет кэш Redis.

## Максимальное

```
Set-AzRedisCache [-ResourceGroupName <String>] -Name <String> [-Size <String>] [-Sku <String>]
 [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>]
 [-ShardCount <Int32>] [-MinimumTlsVersion <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Set-AzRedisCache** изменяет кэш Azure Redis.

## ИЛЛЮСТРИРУЮТ

### Пример 1: изменение кэша Redis
```
PS C:\>Set-AzRedisCache -ResourceGroupName "MyGroup" -Name "MyCache" -RedisConfiguration @{"maxmemory-policy" = "allkeys-random"}

          PrimaryKey         : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
          SecondaryKey       : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
          ResourceGroupName  : mygroup
          Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/mygroup/providers/Microsoft.Cache/Redis/myCache
          Location           : North Central US
          Name               : MyCache
          Type               : Microsoft.Cache/Redis
          HostName           : mycache.redis.cache.windows.net
          Port               : 6379
          ProvisioningState  : creating
          SslPort            : 6380
          RedisConfiguration : {[maxmemory-policy, allkeys-random]}
          EnableNonSslPort   : False
          RedisVersion       : 2.8
          Size               : 250MB
          Sku                : Standard
          Tag                : {}
          Zone               : []
```

Эта команда обновляет MaxMemory-политику для кэша Redis с именем MyCache.

## ПАРАМЕТРЫ

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableNonSslPort
Указывает, включен ли порт без SSL.
Значение по умолчанию — $False (порт без SSL отключен).

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -MinimumTlsVersion
Укажите версию TLS, необходимую клиентам для подключения к кэшу.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name (имя)
Указывает имя кэша Redis, который нужно обновить.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RedisConfiguration
Задает параметры конфигурации Redis.
Для этого параметра допустимы следующие значения:
- RDB — включена резервная копия.
Указывает на то, что сохраняемость данных Redis включена.
Только уровень Premium.
- RDB — строка подключения к хранилищу.
Задает строку подключения к учетной записи хранения для Redis сохраняемости данных.
Только уровень Premium.
- RDB — периодичность резервного копирования.
Указывает периодичность резервного копирования для сохраняемости данных Redis.
Только уровень Premium. 
- MaxMemory — зарезервирован.
Настраивает память, зарезервированную для процессов без кэширования.
Уровни Standard и Premium. 
- MaxMemory — политика.
Настройка политики вытеснения для кэша.
Все ценовые категории. 
- Notify-keyspace-Events.
Настраивает уведомления keyspace.
Уровни Standard и Premium. 
- хэш-максимум-ziplist-записи.
Настройка оптимизации памяти для небольших типов данных агрегатов.
Уровни Standard и Premium. 
- hash-Max-ziplist-value.
Настройка оптимизации памяти для небольших типов данных агрегатов.
Уровни Standard и Premium. 
- Set-Max-intset-"записи".
Настройка оптимизации памяти для небольших типов данных агрегатов.
Уровни Standard и Premium. 
- zset-Max-ziplist-(записи).
Настройка оптимизации памяти для небольших типов данных агрегатов.
Уровни Standard и Premium. 
- zset-Max-ziplist-value.
Настройка оптимизации памяти для небольших типов данных агрегатов.
Уровни Standard и Premium. 
- баз данных.
Настраивает количество баз данных.
Это свойство можно настроить только при создании кэша.
Уровни Standard и Premium.
Дополнительные сведения можно найти в разделе Управление кэшем Redis Azure с помощью Azure PowerShell http://go.microsoft.com/fwlink/?LinkId=800051 ( http://go.microsoft.com/fwlink/?LinkId=800051) .

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Указывает имя группы ресурсов, которая содержит кэш Redis.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ShardCount
Задает количество сегментов для создания в кэше высококачественных кластеров.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Size
Задает размер кэша Redis.
Допустимые значения: 
- P1
- –
- –
- P4
- P5
- C0
- C1
- Режим
- Ячейку
- C4
- C5
- C6
- 250MB
- Гбайт
- 2,5 ГБ
- 6GB
- 13GB
- 26GB
- 53GB
- 120 ГБ значение по умолчанию — 1 ГБ или C1.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SKU
Указывает SKU кэша Redis для создания.
Допустимые значения: 
- Базового
- Стандартная
- Premium по умолчанию используется значение Standard.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Тег
Хэш-таблица, представляющая Теги.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TenantSettings
Этот параметр устарел.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Confirm
Запрашивает подтверждение перед запуском командлета.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Показывает, что произойдет при запуске командлета. Командлет не выполняется.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## ВХОДНЫЕ данные

### System. String

### System. Collections. Hashtable

### System. Nullable "1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, культура = Neutral, PublicKeyToken = 7cec85d7bea7798e]]

### System. Nullable "1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = 7cec85d7bea7798e]]

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. RedisCache. Models. RedisCacheAttributesWithAccessKeys

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzRedisCache](./Get-AzRedisCache.md)

[New-AzRedisCache](./New-AzRedisCache.md)

[Remove-AzRedisCache](./Remove-AzRedisCache.md)


