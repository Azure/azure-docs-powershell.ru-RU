---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2Trigger.md
ms.openlocfilehash: 989a898605488fc7cfaa828bfd8c5b9b61378a27
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078349"
---
# <span data-ttu-id="0ada1-101">Get-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="0ada1-101">Get-AzDataFactoryV2Trigger</span></span>

## <span data-ttu-id="0ada1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0ada1-102">SYNOPSIS</span></span>
<span data-ttu-id="0ada1-103">Получение сведений о триггерах в фабрике данных.</span><span class="sxs-lookup"><span data-stu-id="0ada1-103">Gets information about triggers in a data factory.</span></span>

## <span data-ttu-id="0ada1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0ada1-104">SYNTAX</span></span>

### <span data-ttu-id="0ada1-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0ada1-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2Trigger [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0ada1-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="0ada1-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2Trigger [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0ada1-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="0ada1-107">ByResourceId</span></span>
```
Get-AzDataFactoryV2Trigger [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0ada1-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0ada1-108">DESCRIPTION</span></span>
<span data-ttu-id="0ada1-109">Командлет **Get-AzDataFactoryV2Trigger** получает сведения о триггерах в фабрике данных.</span><span class="sxs-lookup"><span data-stu-id="0ada1-109">The **Get-AzDataFactoryV2Trigger** cmdlet gets information about triggers in a data factory.</span></span> <span data-ttu-id="0ada1-110">Если вы задаете имя триггера, командлет получает сведения об этом триггере.</span><span class="sxs-lookup"><span data-stu-id="0ada1-110">If you specify the name of a trigger, the cmdlet gets information about that trigger.</span></span> <span data-ttu-id="0ada1-111">Если имя не задано, командлет получает сведения обо всех триггерах в фабрике данных.</span><span class="sxs-lookup"><span data-stu-id="0ada1-111">If you do not specify a name, the cmdlet gets information about all triggers in the data factory.</span></span>

## <span data-ttu-id="0ada1-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0ada1-112">EXAMPLES</span></span>

### <span data-ttu-id="0ada1-113">Пример 1: получение сведений об определенном триггере</span><span class="sxs-lookup"><span data-stu-id="0ada1-113">Example 1: Get information about a specific trigger</span></span>
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

<span data-ttu-id="0ada1-114">Получает список всех триггеров, созданных в фабрике данных "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="0ada1-114">Gets a list of all triggers that have been created in the data factory "WikiADF".</span></span>

### <span data-ttu-id="0ada1-115">Пример 2: получение сведений обо всех триггерах</span><span class="sxs-lookup"><span data-stu-id="0ada1-115">Example 2: Get information about all triggers</span></span>
```
Get-AzDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

    TriggerName       : ScheduledTrigger
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.ScheduleTrigger
    RuntimeState      : Stopped
```

<span data-ttu-id="0ada1-116">Получает один триггер с именем "ScheduledTrigger" в фабрике данных "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="0ada1-116">Gets a single trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span>

## <span data-ttu-id="0ada1-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0ada1-117">PARAMETERS</span></span>

### <span data-ttu-id="0ada1-118">— Фактическое.</span><span class="sxs-lookup"><span data-stu-id="0ada1-118">-DataFactory</span></span>
<span data-ttu-id="0ada1-119">Объект фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="0ada1-119">The data factory object.</span></span>

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

### <span data-ttu-id="0ada1-120">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="0ada1-120">-DataFactoryName</span></span>
<span data-ttu-id="0ada1-121">Имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="0ada1-121">The data factory name.</span></span>

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

### <span data-ttu-id="0ada1-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ada1-122">-DefaultProfile</span></span>
<span data-ttu-id="0ada1-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0ada1-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0ada1-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0ada1-124">-Name</span></span>
<span data-ttu-id="0ada1-125">Имя триггера.</span><span class="sxs-lookup"><span data-stu-id="0ada1-125">The trigger name.</span></span>

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

### <span data-ttu-id="0ada1-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ada1-126">-ResourceGroupName</span></span>
<span data-ttu-id="0ada1-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0ada1-127">The resource group name.</span></span>

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

### <span data-ttu-id="0ada1-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0ada1-128">-ResourceId</span></span>
<span data-ttu-id="0ada1-129">Идентификатор ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="0ada1-129">The Azure resource ID.</span></span>

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

### <span data-ttu-id="0ada1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ada1-130">CommonParameters</span></span>
<span data-ttu-id="0ada1-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0ada1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ada1-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ada1-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ada1-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0ada1-133">INPUTS</span></span>

### <span data-ttu-id="0ada1-134">System. String</span><span class="sxs-lookup"><span data-stu-id="0ada1-134">System.String</span></span>

### <span data-ttu-id="0ada1-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="0ada1-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="0ada1-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0ada1-136">OUTPUTS</span></span>

### <span data-ttu-id="0ada1-137">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="0ada1-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="0ada1-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="0ada1-138">NOTES</span></span>

## <span data-ttu-id="0ada1-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0ada1-139">RELATED LINKS</span></span>

[<span data-ttu-id="0ada1-140">Set-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="0ada1-140">Set-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="0ada1-141">Start-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="0ada1-141">Start-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="0ada1-142">Остановить-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="0ada1-142">Stop-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="0ada1-143">Remove-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="0ada1-143">Remove-AzDataFactoryV2Trigger</span></span>]()
