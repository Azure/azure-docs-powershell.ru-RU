---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2triggerrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2TriggerRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2TriggerRun.md
ms.openlocfilehash: 5844863cf56008d5d73fae7eef644dfd8e27c239
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100232908"
---
# <span data-ttu-id="96cc5-101">Get-AzDataFactoryV2TriggerRun</span><span class="sxs-lookup"><span data-stu-id="96cc5-101">Get-AzDataFactoryV2TriggerRun</span></span>

## <span data-ttu-id="96cc5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="96cc5-102">SYNOPSIS</span></span>
<span data-ttu-id="96cc5-103">Возвращает сведения о запусках триггера.</span><span class="sxs-lookup"><span data-stu-id="96cc5-103">Returns information about trigger runs.</span></span>

## <span data-ttu-id="96cc5-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="96cc5-104">SYNTAX</span></span>

### <span data-ttu-id="96cc5-105">ByFactoryName (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="96cc5-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2TriggerRun [-Name] <String> [-TriggerRunStartedAfter] <DateTime>
 [-TriggerRunStartedBefore] <DateTime> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="96cc5-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="96cc5-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2TriggerRun [-Name] <String> [-TriggerRunStartedAfter] <DateTime>
 [-TriggerRunStartedBefore] <DateTime> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="96cc5-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="96cc5-107">DESCRIPTION</span></span>
<span data-ttu-id="96cc5-108">Команда **Get-AzDataFactoryV2TriggerRun** возвращает подробные сведения о запусках триггера для указанного триггера на заданный период времени.</span><span class="sxs-lookup"><span data-stu-id="96cc5-108">The **Get-AzDataFactoryV2TriggerRun** command returns detailed information about trigger runs for the specified trigger in the given timeframe.</span></span>

## <span data-ttu-id="96cc5-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="96cc5-109">EXAMPLES</span></span>

### <span data-ttu-id="96cc5-110">Пример 1. Просмотр сведений о запуске триггера</span><span class="sxs-lookup"><span data-stu-id="96cc5-110">Example 1: Get information about trigger run</span></span>
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

<span data-ttu-id="96cc5-111">Эта команда отображает сведения о запуске вики-сайта WikiTrigger на заводском сайте WikiADF, который начался с "2017-09-01" и "2019-09-30".</span><span class="sxs-lookup"><span data-stu-id="96cc5-111">This command shows information about runs for "WikiTrigger" in the factory "WikiADF" that started between "2017-09-01" and "2019-09-30".</span></span>

## <span data-ttu-id="96cc5-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="96cc5-112">PARAMETERS</span></span>

### <span data-ttu-id="96cc5-113">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="96cc5-113">-DataFactory</span></span>
<span data-ttu-id="96cc5-114">Объект фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="96cc5-114">The data factory object.</span></span>

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

### <span data-ttu-id="96cc5-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="96cc5-115">-DataFactoryName</span></span>
<span data-ttu-id="96cc5-116">Название фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="96cc5-116">The data factory name.</span></span>

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

### <span data-ttu-id="96cc5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96cc5-117">-DefaultProfile</span></span>
<span data-ttu-id="96cc5-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="96cc5-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="96cc5-119">-Name</span><span class="sxs-lookup"><span data-stu-id="96cc5-119">-Name</span></span>
<span data-ttu-id="96cc5-120">Имя триггера.</span><span class="sxs-lookup"><span data-stu-id="96cc5-120">The trigger name.</span></span>

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

### <span data-ttu-id="96cc5-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96cc5-121">-ResourceGroupName</span></span>
<span data-ttu-id="96cc5-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="96cc5-122">The resource group name.</span></span>

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

### <span data-ttu-id="96cc5-123">-TriggerRunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="96cc5-123">-TriggerRunStartedAfter</span></span>
<span data-ttu-id="96cc5-124">Время запуска триггера или после его запуска в формате ISO8601.</span><span class="sxs-lookup"><span data-stu-id="96cc5-124">The time at or after which the trigger run started to execute in ISO8601 format.</span></span>

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

### <span data-ttu-id="96cc5-125">-TriggerRunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="96cc5-125">-TriggerRunStartedBefore</span></span>
<span data-ttu-id="96cc5-126">Время запуска триггера или до этого запуска в формате ISO8601.</span><span class="sxs-lookup"><span data-stu-id="96cc5-126">The time at or before which the trigger run started to execute in ISO8601 format.</span></span>

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

### <span data-ttu-id="96cc5-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96cc5-127">CommonParameters</span></span>
<span data-ttu-id="96cc5-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96cc5-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96cc5-129">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96cc5-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96cc5-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="96cc5-130">INPUTS</span></span>

### <span data-ttu-id="96cc5-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="96cc5-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

### <span data-ttu-id="96cc5-132">System.String</span><span class="sxs-lookup"><span data-stu-id="96cc5-132">System.String</span></span>

## <span data-ttu-id="96cc5-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="96cc5-133">OUTPUTS</span></span>

### <span data-ttu-id="96cc5-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun</span><span class="sxs-lookup"><span data-stu-id="96cc5-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun</span></span>

## <span data-ttu-id="96cc5-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="96cc5-135">NOTES</span></span>

## <span data-ttu-id="96cc5-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="96cc5-136">RELATED LINKS</span></span>

[<span data-ttu-id="96cc5-137">Start-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="96cc5-137">Start-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="96cc5-138">Stop-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="96cc5-138">Stop-AzDataFactoryV2Trigger</span></span>]()

