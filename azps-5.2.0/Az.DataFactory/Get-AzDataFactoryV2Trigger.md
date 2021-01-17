---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2Trigger.md
ms.openlocfilehash: 989a898605488fc7cfaa828bfd8c5b9b61378a27
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98396927"
---
# <span data-ttu-id="9a577-101">Get-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="9a577-101">Get-AzDataFactoryV2Trigger</span></span>

## <span data-ttu-id="9a577-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9a577-102">SYNOPSIS</span></span>
<span data-ttu-id="9a577-103">Получает сведения о триггерах в фабрике данных.</span><span class="sxs-lookup"><span data-stu-id="9a577-103">Gets information about triggers in a data factory.</span></span>

## <span data-ttu-id="9a577-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9a577-104">SYNTAX</span></span>

### <span data-ttu-id="9a577-105">ByFactoryName (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9a577-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2Trigger [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9a577-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="9a577-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2Trigger [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9a577-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="9a577-107">ByResourceId</span></span>
```
Get-AzDataFactoryV2Trigger [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9a577-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9a577-108">DESCRIPTION</span></span>
<span data-ttu-id="9a577-109">**Cmdlet Get-AzDataFactoryV2Trigger** получает сведения о триггерах в фабрике данных.</span><span class="sxs-lookup"><span data-stu-id="9a577-109">The **Get-AzDataFactoryV2Trigger** cmdlet gets information about triggers in a data factory.</span></span> <span data-ttu-id="9a577-110">Если указать имя триггера, он будет отсвещать сведения о нем.</span><span class="sxs-lookup"><span data-stu-id="9a577-110">If you specify the name of a trigger, the cmdlet gets information about that trigger.</span></span> <span data-ttu-id="9a577-111">Если имя не указано, он получает сведения обо всех триггерах в фабрике данных.</span><span class="sxs-lookup"><span data-stu-id="9a577-111">If you do not specify a name, the cmdlet gets information about all triggers in the data factory.</span></span>

## <span data-ttu-id="9a577-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9a577-112">EXAMPLES</span></span>

### <span data-ttu-id="9a577-113">Пример 1. Просмотр сведений об определенном триггере</span><span class="sxs-lookup"><span data-stu-id="9a577-113">Example 1: Get information about a specific trigger</span></span>
```
PS C:\> Get-AzDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF"

    TriggerName       : ScheduledTrigger
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.ScheduleTrigger
    RuntimeState      : Stopped

    TriggerName       : ScheduledTrigger2
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.ScheduleTrigger
    RuntimeState      : Stopped
```

<span data-ttu-id="9a577-114">Возвращает список всех триггеров, созданных на заводе данных "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="9a577-114">Gets a list of all triggers that have been created in the data factory "WikiADF".</span></span>

### <span data-ttu-id="9a577-115">Пример 2. Просмотр сведений обо всех триггерах</span><span class="sxs-lookup"><span data-stu-id="9a577-115">Example 2: Get information about all triggers</span></span>
```
Get-AzDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

    TriggerName       : ScheduledTrigger
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.ScheduleTrigger
    RuntimeState      : Stopped
```

<span data-ttu-id="9a577-116">Получает один триггер ScheduledTrigger в фабрике данных WikiADF.</span><span class="sxs-lookup"><span data-stu-id="9a577-116">Gets a single trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span>

## <span data-ttu-id="9a577-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9a577-117">PARAMETERS</span></span>

### <span data-ttu-id="9a577-118">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="9a577-118">-DataFactory</span></span>
<span data-ttu-id="9a577-119">Объект фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="9a577-119">The data factory object.</span></span>

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

### <span data-ttu-id="9a577-120">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="9a577-120">-DataFactoryName</span></span>
<span data-ttu-id="9a577-121">Название фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="9a577-121">The data factory name.</span></span>

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

### <span data-ttu-id="9a577-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a577-122">-DefaultProfile</span></span>
<span data-ttu-id="9a577-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9a577-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9a577-124">-Name</span><span class="sxs-lookup"><span data-stu-id="9a577-124">-Name</span></span>
<span data-ttu-id="9a577-125">Имя триггера.</span><span class="sxs-lookup"><span data-stu-id="9a577-125">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByFactoryObject
Aliases: TriggerName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a577-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a577-126">-ResourceGroupName</span></span>
<span data-ttu-id="9a577-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9a577-127">The resource group name.</span></span>

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

### <span data-ttu-id="9a577-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9a577-128">-ResourceId</span></span>
<span data-ttu-id="9a577-129">ИД ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="9a577-129">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a577-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a577-130">CommonParameters</span></span>
<span data-ttu-id="9a577-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a577-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a577-132">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a577-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a577-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9a577-133">INPUTS</span></span>

### <span data-ttu-id="9a577-134">System.String</span><span class="sxs-lookup"><span data-stu-id="9a577-134">System.String</span></span>

### <span data-ttu-id="9a577-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="9a577-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="9a577-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9a577-136">OUTPUTS</span></span>

### <span data-ttu-id="9a577-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span><span class="sxs-lookup"><span data-stu-id="9a577-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="9a577-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9a577-138">NOTES</span></span>

## <span data-ttu-id="9a577-139">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9a577-139">RELATED LINKS</span></span>

[<span data-ttu-id="9a577-140">Set-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="9a577-140">Set-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="9a577-141">Start-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="9a577-141">Start-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="9a577-142">Stop-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="9a577-142">Stop-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="9a577-143">Remove-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="9a577-143">Remove-AzDataFactoryV2Trigger</span></span>]()
