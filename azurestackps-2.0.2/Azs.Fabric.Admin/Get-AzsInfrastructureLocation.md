---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsinfrastructurelocation
schema: 2.0.0
ms.openlocfilehash: 0d0f2856503943d19653dd09a8cb1c125fec9517
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94076771"
---
# Get-AzsInfrastructureLocation

## КРАТКИй обзор
Возвращает указанное расположение структуры.

## Максимальное

### Список (по умолчанию)
```
Get-AzsInfrastructureLocation [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-Filter <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### Получить
```
Get-AzsInfrastructureLocation -FabricLocation <String> [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### GetViaIdentity
```
Get-AzsInfrastructureLocation -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## NОПИСАНИЕ
Возвращает указанное расположение структуры.

## ИЛЛЮСТРИРУЮТ

### Пример 1: 
```powershell
PS C:\> Get-AzsInfrastructureLocation

Return a list of all fabric locations.
```

Получение списка всех структурных местоположений.

### Пример 2: 
```powershell
PS C:\> Get-AzsInfrastructureLocation -Location "local"

Return a location based on the name.
```

Получение расположения на основе имени.

## ПАРАМЕТРЫ

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -FabricLocation
Расположение структуры.

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -Фильтр
Параметр фильтра OData.

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -InputObject
Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### -PassThru
Возвращает значение истина, если команда выполнена успешно.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Get, GetViaIdentity
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -ResourceGroupName
Имя группы ресурсов.

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### -SubscriptionId
Учетные данные подписки, однозначно определяющие подписку Microsoft Azure.
Идентификатор подписки образует часть URI для каждого вызова службы.

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## ВХОДНЫЕ данные

### Microsoft. Azure. PowerShell. командлеты. FabricAdmin. Models. IFabricAdminIdentity

## НАПРЯЖЕНИЕ

### Microsoft. Azure. PowerShell. командлеты. FabricAdmin. Models. Api20160501. IFabricLocation



## Пуск

Свойства сложных параметров для создания описанных ниже параметров создайте хэш-таблицу, содержащую соответствующие свойства. Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.

INPUTOBJECT <IFabricAdminIdentity> : параметр Identity
  - `[Drive <String>]`: Имя диска хранилища.
  - `[EdgeGateway <String>]`: Имя шлюза Edge.
  - `[EdgeGatewayPool <String>]`: Имя пула шлюзов Edge.
  - `[FabricLocation <String>]`: Расположение в структуре.
  - `[FileShare <String>]`: Имя общего файлового файла структуры.
  - `[IPPool <String>]`: Имя пула IP-адресов.
  - `[Id <String>]`: Путь к удостоверению ресурса
  - `[InfraRole <String>]`: Имя роли инфраструктуры.
  - `[InfraRoleInstance <String>]`: Имя экземпляра роли инфраструктуры.
  - `[Location <String>]`: Расположение ресурса.
  - `[LogicalNetwork <String>]`: Имя логической сети.
  - `[LogicalSubnet <String>]`: Имя логической подсети.
  - `[MacAddressPool <String>]`: Имя пула MAC-адресов.
  - `[Operation <String>]`: Идентификатор операции.
  - `[ResourceGroupName <String>]`: Имя группы ресурсов.
  - `[ScaleUnit <String>]`: Название единиц измерения шкалы.
  - `[ScaleUnitNode <String>]`: Имя узла единица масштабирования.
  - `[SlbMuxInstance <String>]`: Имя экземпляра МУЛЬТИПЛЕКСОРа SLB.
  - `[StorageSubSystem <String>]`: Имя системы хранения.
  - `[SubscriptionId <String>]`: Учетные данные подписки, которые однозначно определяют подписку Microsoft Azure. Идентификатор подписки образует часть URI для каждого вызова службы.
  - `[Volume <String>]`: Имя тома хранилища.

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

