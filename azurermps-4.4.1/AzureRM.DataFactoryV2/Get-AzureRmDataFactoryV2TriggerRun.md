---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2TriggerRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2TriggerRun.md
gitcommit: https://github.com/Azure/azure-powershell/blob/7fe7039e96038b4a91513dfda26026ad8e0a352b
ms.openlocfilehash: d5ea2dee1f6023b9505c38a58d364b7aa92591db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734075"
---
# <span data-ttu-id="e1489-101">Get-AzureRmDataFactoryV2TriggerRun</span><span class="sxs-lookup"><span data-stu-id="e1489-101">Get-AzureRmDataFactoryV2TriggerRun</span></span>

## <span data-ttu-id="e1489-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e1489-102">SYNOPSIS</span></span>
<span data-ttu-id="e1489-103">Возвращает сведения о запусках триггеров.</span><span class="sxs-lookup"><span data-stu-id="e1489-103">Returns information about trigger runs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e1489-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e1489-104">SYNTAX</span></span>

### <span data-ttu-id="e1489-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e1489-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryV2TriggerRun [-Name] <String> [-TriggerRunStartedAfter] <DateTime>
 [-TriggerRunStartedBefore] <DateTime> [-ResourceGroupName] <String> [-DataFactoryName] <String>
```

### <span data-ttu-id="e1489-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="e1489-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryV2TriggerRun [-Name] <String> [-TriggerRunStartedAfter] <DateTime>
 [-TriggerRunStartedBefore] <DateTime> [-DataFactory] <PSDataFactory>
```

## <span data-ttu-id="e1489-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e1489-107">DESCRIPTION</span></span>
<span data-ttu-id="e1489-108">Команда **Get-AzureRmDataFactoryV2TriggerRun** возвращает подробные сведения о выполнении триггеров для определенного триггера в течение заданного периода.</span><span class="sxs-lookup"><span data-stu-id="e1489-108">The **Get-AzureRmDataFactoryV2TriggerRun** command returns detailed information about trigger runs for the specified trigger in the given timeframe.</span></span>

## <span data-ttu-id="e1489-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e1489-109">EXAMPLES</span></span>

### <span data-ttu-id="e1489-110">Пример 1: получение сведений о запуске триггеров</span><span class="sxs-lookup"><span data-stu-id="e1489-110">Example 1: Get information about trigger run</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2TriggerRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "WikiTrigger" -TriggerRunStartedAfter "2017-09-01" -TriggerRunStartedBefore "2019-09-30"

    ResourceGroupName   : ADF
    DataFactoryName     : WikiADF
    TriggerName         : WikiTrigger
    TriggerRunId        : 08586958400454144995526033731
    TriggerType         : ScheduleTrigger
    TriggerRunTimestamp : 9/18/2017 8:34:00 PM
    Status              : Succeeded

```

<span data-ttu-id="e1489-111">Эта команда отображает сведения о запусках для "WikiTrigger" в фабрике "WikiADF", которая начинается между "2017-09-01" и "2019-09-30".</span><span class="sxs-lookup"><span data-stu-id="e1489-111">This command shows information about runs for "WikiTrigger" in the factory "WikiADF" that started between "2017-09-01" and "2019-09-30".</span></span>

## <span data-ttu-id="e1489-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e1489-112">PARAMETERS</span></span>

### <span data-ttu-id="e1489-113">— Фактическое.</span><span class="sxs-lookup"><span data-stu-id="e1489-113">-DataFactory</span></span>
<span data-ttu-id="e1489-114">Объект фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="e1489-114">The data factory object.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e1489-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="e1489-115">-DataFactoryName</span></span>
<span data-ttu-id="e1489-116">Имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="e1489-116">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1489-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e1489-117">-Name</span></span>
<span data-ttu-id="e1489-118">Имя триггера.</span><span class="sxs-lookup"><span data-stu-id="e1489-118">The trigger name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1489-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1489-119">-ResourceGroupName</span></span>
<span data-ttu-id="e1489-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e1489-120">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1489-121">-TriggerRunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="e1489-121">-TriggerRunStartedAfter</span></span>
<span data-ttu-id="e1489-122">Время, по истечении которого началось выполнение триггера в формате ISO8601 или назад.</span><span class="sxs-lookup"><span data-stu-id="e1489-122">The time at or after which the trigger run started to execute in ISO8601 format.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1489-123">-TriggerRunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="e1489-123">-TriggerRunStartedBefore</span></span>
<span data-ttu-id="e1489-124">Время, до которого началось выполнение триггера в формате ISO8601 или до него.</span><span class="sxs-lookup"><span data-stu-id="e1489-124">The time at or before which the trigger run started to execute in ISO8601 format.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="e1489-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e1489-125">INPUTS</span></span>

### <span data-ttu-id="e1489-126">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="e1489-126">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>
<span data-ttu-id="e1489-127">System. String</span><span class="sxs-lookup"><span data-stu-id="e1489-127">System.String</span></span>


## <span data-ttu-id="e1489-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e1489-128">OUTPUTS</span></span>

### <span data-ttu-id="e1489-129">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. DataFactoryV2. Models. PSTriggerRun, Microsoft. Azure. Commands. DataFactoryV2, Version = 0.1.9.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="e1489-129">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="e1489-130">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTriggerRun</span><span class="sxs-lookup"><span data-stu-id="e1489-130">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun</span></span>


## <span data-ttu-id="e1489-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="e1489-131">NOTES</span></span>

## <span data-ttu-id="e1489-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e1489-132">RELATED LINKS</span></span>
[<span data-ttu-id="e1489-133">Start-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="e1489-133">Start-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="e1489-134">Остановить-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="e1489-134">Stop-AzureRmDataFactoryV2Trigger</span></span>]()

