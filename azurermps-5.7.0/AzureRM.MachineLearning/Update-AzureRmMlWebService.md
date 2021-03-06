---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/update-azurermmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Update-AzureRmMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Update-AzureRmMlWebService.md
ms.openlocfilehash: 5fb8c8f71366dd9fd0a2c6b12fc023c1ce3ccf9b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567983"
---
# Update-AzureRmMlWebService

## КРАТКИй обзор
Обновляет свойства существующего ресурса веб-службы.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

### UpdateFromParameters
```
Update-AzureRmMlWebService -ResourceGroupName <String> -Name <String> [-Title <String>] [-Description <String>]
 [-IsReadOnly] [-Keys <WebServiceKeys>] [-StorageAccountKey <String>] [-Diagnostics <DiagnosticsConfiguration>]
 [-RealtimeConfiguration <RealtimeConfiguration>] [-Assets <Hashtable>]
 [-Input <ServiceInputOutputSpecification>] [-Output <ServiceInputOutputSpecification>]
 [-Parameters <Hashtable>] [-Package <GraphPackage>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### UpdateFromObject
```
Update-AzureRmMlWebService -ResourceGroupName <String> -Name <String> -ServiceUpdates <WebService> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет Update-AzureRmMlWebService позволяет обновлять нестатические свойства веб-службы.
Командлет работает как операция исправления.
Передача только тех свойств, которые вы хотите изменить.

## ИЛЛЮСТРИРУЮТ

### --------------------------Пример 1: аргументы выборочного обновления--------------------------
```
Update-AzureRmMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Description "new update to description" -Keys @{Primary='changed primary key'} -Diagnostics @{Level='All'}
```

Здесь мы изменим описание, основной ключ доступа и Активируй сбор диагностических сведений для всех трассировок во время выполнения для веб-службы.

### --------------------------Пример 2: обновление на основе экземпляра веб-службы--------------------------
```
$updates = @{ Properties = @{ Title="New Title"; RealtimeConfiguration = @{ MaxConcurrentCalls=25 }}}

Update-AzureRmMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -ServiceUpdates $updates
```

В примере сначала создается определение веб-службы, которое включает только поля, которые нужно обновить, а затем вызывает Update-AzureRmMlWebService, чтобы применить их с помощью параметра ServiceUpdates.

## ПАРАМЕТРЫ

### -Активы
Набор ресурсов (например, модулей, наборов данных), образующих веб-службу.

```yaml
Type: Hashtable
Parameter Sets: UpdateFromParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure

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

### -Описание
Новое значение для описания веб-службы.
Это видно в схеме API службы Swagger.

```yaml
Type: String
Parameter Sets: UpdateFromParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Диагностика
Параметры, управляющие сбором трассировок диагностики для веб-службы.

```yaml
Type: DiagnosticsConfiguration
Parameter Sets: UpdateFromParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Не запрашивать подтверждение.

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

### -Input
Определение входных данных веб-службы, предоставленных в качестве конструкции схемы Swagger.

```yaml
Type: ServiceInputOutputSpecification
Parameter Sets: UpdateFromParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReadOnly
Указывает, что эта веб-служба предназначена только для чтения.
После того как вы задали этот параметр, веб-службу можно будет обновлять, в том числе изменить значение этого свойства, и удалить ее.

```yaml
Type: SwitchParameter
Parameter Sets: UpdateFromParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Keys
Обновляет один или оба клавиши доступа, используемые для проверки подлинности вызовов API среды выполнения службы.

```yaml
Type: WebServiceKeys
Parameter Sets: UpdateFromParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (имя)
Имя ресурса веб-службы, который нужно обновить.

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

### -Output
Определение выходных данных веб-службы, которые представлены в виде конструкции схемы Swagger.

```yaml
Type: ServiceInputOutputSpecification
Parameter Sets: UpdateFromParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Package
Определение пакета графа, определяющего эту веб-службу.

```yaml
Type: GraphPackage
Parameter Sets: UpdateFromParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Parameters
Набор значений глобальных параметров, определенных для веб-службы, заданный в качестве имени глобального параметра — \> коллекция значений по умолчанию.
Если значение по умолчанию не задано, параметр считается обязательным.

```yaml
Type: Hashtable
Parameter Sets: UpdateFromParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RealtimeConfiguration
Обновляет конфигурацию конечной точки реального времени службы.

```yaml
Type: RealtimeConfiguration
Parameter Sets: UpdateFromParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Группа ресурсов, содержащая веб-службу, которую нужно обновить.

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

### -ServiceUpdates
Набор обновлений, которые необходимо применить к веб-службе, указанной в качестве экземпляра определения веб-службы.
Изменяются только поля, не являющиеся статическими.

```yaml
Type: WebService
Parameter Sets: UpdateFromObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -StorageAccountKey
Поворачивает клавишу доступа для учетной записи хранения, связанной с веб-службой.

```yaml
Type: String
Parameter Sets: UpdateFromParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Title
Новое значение заголовка веб-службы.
Это видно в схеме API службы Swagger.

```yaml
Type: String
Parameter Sets: UpdateFromParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm
Запрашивает подтверждение перед запуском командлета.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Показывает, что произойдет при запуске командлета.
Командлет не выполняется.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### Вебслужба
Параметр "ServiceUpdates" принимает значение типа WebService из конвейера.

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Management. MachineLearning. WebService. Models.
Сводное описание веб-службы машинного обучения Azure.
Аналогично описанию, возвращаемому вызовом командлета Get-AzureRmMlWebService для существующей веб-службы.
Это описание не содержит конфиденциальные свойства, такие как учетные данные учетной записи хранения и клавиши доступа службы.

## Пуск
Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Machine, Machine Learning, azureml

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

