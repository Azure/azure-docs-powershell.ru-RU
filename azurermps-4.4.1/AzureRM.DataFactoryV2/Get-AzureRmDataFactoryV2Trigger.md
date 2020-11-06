---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Trigger.md
gitcommit: https://github.com/Azure/azure-powershell/blob/c396953644d237789e0f4e1f726b553913186d34
ms.openlocfilehash: bc60bbb5b48c4022e7db6a95e26a1f43ef891ae2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569551"
---
# <span data-ttu-id="a5017-101">Get-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="a5017-101">Get-AzureRmDataFactoryV2Trigger</span></span>

## <span data-ttu-id="a5017-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a5017-102">SYNOPSIS</span></span>
<span data-ttu-id="a5017-103">Получение сведений о триггерах в фабрике данных.</span><span class="sxs-lookup"><span data-stu-id="a5017-103">Gets information about triggers in a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a5017-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a5017-104">SYNTAX</span></span>

### <span data-ttu-id="a5017-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a5017-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryV2Trigger [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
```

### <span data-ttu-id="a5017-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="a5017-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryV2Trigger [[-Name] <String>] [-DataFactory] <PSDataFactory>
```

## <span data-ttu-id="a5017-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a5017-107">DESCRIPTION</span></span>
<span data-ttu-id="a5017-108">Командлет **Get-AzureRmDataFactoryV2Trigger** получает сведения о триггерах в фабрике данных.</span><span class="sxs-lookup"><span data-stu-id="a5017-108">The **Get-AzureRmDataFactoryV2Trigger** cmdlet gets information about triggers in a data factory.</span></span> <span data-ttu-id="a5017-109">Если вы задаете имя триггера, командлет получает сведения об этом триггере.</span><span class="sxs-lookup"><span data-stu-id="a5017-109">If you specify the name of a trigger, the cmdlet gets information about that trigger.</span></span> <span data-ttu-id="a5017-110">Если имя не задано, командлет получает сведения обо всех триггерах в фабрике данных.</span><span class="sxs-lookup"><span data-stu-id="a5017-110">If you do not specify a name, the cmdlet gets information about all triggers in the data factory.</span></span>


## <span data-ttu-id="a5017-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a5017-111">EXAMPLES</span></span>

### <span data-ttu-id="a5017-112">Пример 1: получение сведений об определенном триггере</span><span class="sxs-lookup"><span data-stu-id="a5017-112">Example 1: Get information about a specific trigger</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF"

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

<span data-ttu-id="a5017-113">Получает список всех триггеров, созданных в фабрике данных "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="a5017-113">Gets a list of all triggers that have been created in the data factory "WikiADF".</span></span>

### <span data-ttu-id="a5017-114">Пример 2: получение сведений обо всех триггерах</span><span class="sxs-lookup"><span data-stu-id="a5017-114">Example 2: Get information about all triggers</span></span>

```
Get-AzureRmDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

    TriggerName       : ScheduledTrigger
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.ScheduleTrigger
    RuntimeState      : Stopped
```

<span data-ttu-id="a5017-115">Получает один триггер с именем "ScheduledTrigger" в фабрике данных "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="a5017-115">Gets a single trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span>

## <span data-ttu-id="a5017-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a5017-116">PARAMETERS</span></span>

### <span data-ttu-id="a5017-117">— Фактическое.</span><span class="sxs-lookup"><span data-stu-id="a5017-117">-DataFactory</span></span>
<span data-ttu-id="a5017-118">Объект фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="a5017-118">The data factory object.</span></span>

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

### <span data-ttu-id="a5017-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="a5017-119">-DataFactoryName</span></span>
<span data-ttu-id="a5017-120">Имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="a5017-120">The data factory name.</span></span>

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

### <span data-ttu-id="a5017-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a5017-121">-Name</span></span>
<span data-ttu-id="a5017-122">Имя триггера.</span><span class="sxs-lookup"><span data-stu-id="a5017-122">The trigger name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: TriggerName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5017-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5017-123">-ResourceGroupName</span></span>
<span data-ttu-id="a5017-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a5017-124">The resource group name.</span></span>

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

## <span data-ttu-id="a5017-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a5017-125">INPUTS</span></span>

### <span data-ttu-id="a5017-126">System. String</span><span class="sxs-lookup"><span data-stu-id="a5017-126">System.String</span></span>
<span data-ttu-id="a5017-127">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="a5017-127">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>


## <span data-ttu-id="a5017-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a5017-128">OUTPUTS</span></span>

### <span data-ttu-id="a5017-129">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. DataFactoryV2. Models. PSTrigger, Microsoft. Azure. Commands. DataFactoryV2, Version = 0.1.9.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="a5017-129">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="a5017-130">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="a5017-130">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>


## <span data-ttu-id="a5017-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="a5017-131">NOTES</span></span>

## <span data-ttu-id="a5017-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a5017-132">RELATED LINKS</span></span>
[<span data-ttu-id="a5017-133">Set-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="a5017-133">Set-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="a5017-134">Start-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="a5017-134">Start-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="a5017-135">Остановить-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="a5017-135">Stop-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="a5017-136">Remove-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="a5017-136">Remove-AzureRmDataFactoryV2Trigger</span></span>]()
