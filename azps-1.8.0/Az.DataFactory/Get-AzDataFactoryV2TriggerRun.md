---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2triggerrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2TriggerRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2TriggerRun.md
ms.openlocfilehash: 3f98ff38d5e74b7b167dc3a168a1cc05a42a7a23
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93731148"
---
# <span data-ttu-id="82179-101">Get-AzDataFactoryV2TriggerRun</span><span class="sxs-lookup"><span data-stu-id="82179-101">Get-AzDataFactoryV2TriggerRun</span></span>

## <span data-ttu-id="82179-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="82179-102">SYNOPSIS</span></span>
<span data-ttu-id="82179-103">Возвращает сведения о запусках триггеров.</span><span class="sxs-lookup"><span data-stu-id="82179-103">Returns information about trigger runs.</span></span>

## <span data-ttu-id="82179-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="82179-104">SYNTAX</span></span>

### <span data-ttu-id="82179-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="82179-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2TriggerRun [-Name] <String> [-TriggerRunStartedAfter] <DateTime>
 [-TriggerRunStartedBefore] <DateTime> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="82179-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="82179-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2TriggerRun [-Name] <String> [-TriggerRunStartedAfter] <DateTime>
 [-TriggerRunStartedBefore] <DateTime> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="82179-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="82179-107">DESCRIPTION</span></span>
<span data-ttu-id="82179-108">Команда **Get-AzDataFactoryV2TriggerRun** возвращает подробные сведения о выполнении триггеров для определенного триггера в течение заданного периода.</span><span class="sxs-lookup"><span data-stu-id="82179-108">The **Get-AzDataFactoryV2TriggerRun** command returns detailed information about trigger runs for the specified trigger in the given timeframe.</span></span>

## <span data-ttu-id="82179-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="82179-109">EXAMPLES</span></span>

### <span data-ttu-id="82179-110">Пример 1: получение сведений о запуске триггеров</span><span class="sxs-lookup"><span data-stu-id="82179-110">Example 1: Get information about trigger run</span></span>
```
PS C:\> Get-AzDataFactoryV2TriggerRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "WikiTrigger" -TriggerRunStartedAfter "2017-09-01" -TriggerRunStartedBefore "2019-09-30"

    ResourceGroupName   : ADF
    DataFactoryName     : WikiADF
    TriggerName         : WikiTrigger
    TriggerRunId        : 08586958400454144995526033731
    TriggerType         : ScheduleTrigger
    TriggerRunTimestamp : 9/18/2017 8:34:00 PM
    Status              : Succeeded
```

<span data-ttu-id="82179-111">Эта команда отображает сведения о запусках для "WikiTrigger" в фабрике "WikiADF", которая начинается между "2017-09-01" и "2019-09-30".</span><span class="sxs-lookup"><span data-stu-id="82179-111">This command shows information about runs for "WikiTrigger" in the factory "WikiADF" that started between "2017-09-01" and "2019-09-30".</span></span>

## <span data-ttu-id="82179-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="82179-112">PARAMETERS</span></span>

### <span data-ttu-id="82179-113">— Фактическое.</span><span class="sxs-lookup"><span data-stu-id="82179-113">-DataFactory</span></span>
<span data-ttu-id="82179-114">Объект фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="82179-114">The data factory object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="82179-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="82179-115">-DataFactoryName</span></span>
<span data-ttu-id="82179-116">Имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="82179-116">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82179-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82179-117">-DefaultProfile</span></span>
<span data-ttu-id="82179-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="82179-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="82179-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="82179-119">-Name</span></span>
<span data-ttu-id="82179-120">Имя триггера.</span><span class="sxs-lookup"><span data-stu-id="82179-120">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82179-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82179-121">-ResourceGroupName</span></span>
<span data-ttu-id="82179-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="82179-122">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82179-123">-TriggerRunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="82179-123">-TriggerRunStartedAfter</span></span>
<span data-ttu-id="82179-124">Время, по истечении которого началось выполнение триггера в формате ISO8601 или назад.</span><span class="sxs-lookup"><span data-stu-id="82179-124">The time at or after which the trigger run started to execute in ISO8601 format.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82179-125">-TriggerRunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="82179-125">-TriggerRunStartedBefore</span></span>
<span data-ttu-id="82179-126">Время, до которого началось выполнение триггера в формате ISO8601 или до него.</span><span class="sxs-lookup"><span data-stu-id="82179-126">The time at or before which the trigger run started to execute in ISO8601 format.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82179-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82179-127">CommonParameters</span></span>
<span data-ttu-id="82179-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="82179-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82179-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82179-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82179-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="82179-130">INPUTS</span></span>

### <span data-ttu-id="82179-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="82179-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

### <span data-ttu-id="82179-132">System. String</span><span class="sxs-lookup"><span data-stu-id="82179-132">System.String</span></span>

## <span data-ttu-id="82179-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="82179-133">OUTPUTS</span></span>

### <span data-ttu-id="82179-134">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTriggerRun</span><span class="sxs-lookup"><span data-stu-id="82179-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun</span></span>

## <span data-ttu-id="82179-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="82179-135">NOTES</span></span>

## <span data-ttu-id="82179-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="82179-136">RELATED LINKS</span></span>

[<span data-ttu-id="82179-137">Start-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="82179-137">Start-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="82179-138">Остановить-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="82179-138">Stop-AzDataFactoryV2Trigger</span></span>]()

