---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Trigger.md
ms.openlocfilehash: 5004b50cf5bb5b22a95ef00bf19f0e783fd04cb2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568602"
---
# <span data-ttu-id="1737c-101">Get-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="1737c-101">Get-AzureRmDataFactoryV2Trigger</span></span>

## <span data-ttu-id="1737c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1737c-102">SYNOPSIS</span></span>
<span data-ttu-id="1737c-103">Получение сведений о триггерах в фабрике данных.</span><span class="sxs-lookup"><span data-stu-id="1737c-103">Gets information about triggers in a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1737c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1737c-104">SYNTAX</span></span>

### <span data-ttu-id="1737c-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1737c-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryV2Trigger [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1737c-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="1737c-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryV2Trigger [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1737c-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="1737c-107">ByResourceId</span></span>
```
Get-AzureRmDataFactoryV2Trigger -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1737c-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1737c-108">DESCRIPTION</span></span>
<span data-ttu-id="1737c-109">Командлет **Get-AzureRmDataFactoryV2Trigger** получает сведения о триггерах в фабрике данных.</span><span class="sxs-lookup"><span data-stu-id="1737c-109">The **Get-AzureRmDataFactoryV2Trigger** cmdlet gets information about triggers in a data factory.</span></span> <span data-ttu-id="1737c-110">Если вы задаете имя триггера, командлет получает сведения об этом триггере.</span><span class="sxs-lookup"><span data-stu-id="1737c-110">If you specify the name of a trigger, the cmdlet gets information about that trigger.</span></span> <span data-ttu-id="1737c-111">Если имя не задано, командлет получает сведения обо всех триггерах в фабрике данных.</span><span class="sxs-lookup"><span data-stu-id="1737c-111">If you do not specify a name, the cmdlet gets information about all triggers in the data factory.</span></span>

## <span data-ttu-id="1737c-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1737c-112">EXAMPLES</span></span>

### <span data-ttu-id="1737c-113">Пример 1: получение сведений об определенном триггере</span><span class="sxs-lookup"><span data-stu-id="1737c-113">Example 1: Get information about a specific trigger</span></span>
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

<span data-ttu-id="1737c-114">Получает список всех триггеров, созданных в фабрике данных "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="1737c-114">Gets a list of all triggers that have been created in the data factory "WikiADF".</span></span>

### <span data-ttu-id="1737c-115">Пример 2: получение сведений обо всех триггерах</span><span class="sxs-lookup"><span data-stu-id="1737c-115">Example 2: Get information about all triggers</span></span>
```
Get-AzureRmDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

    TriggerName       : ScheduledTrigger
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.ScheduleTrigger
    RuntimeState      : Stopped
```

<span data-ttu-id="1737c-116">Получает один триггер с именем "ScheduledTrigger" в фабрике данных "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="1737c-116">Gets a single trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span>

## <span data-ttu-id="1737c-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1737c-117">PARAMETERS</span></span>

### <span data-ttu-id="1737c-118">— Фактическое.</span><span class="sxs-lookup"><span data-stu-id="1737c-118">-DataFactory</span></span>
<span data-ttu-id="1737c-119">Объект фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="1737c-119">The data factory object.</span></span>

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

### <span data-ttu-id="1737c-120">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="1737c-120">-DataFactoryName</span></span>
<span data-ttu-id="1737c-121">Имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="1737c-121">The data factory name.</span></span>

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

### <span data-ttu-id="1737c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1737c-122">-DefaultProfile</span></span>
<span data-ttu-id="1737c-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1737c-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1737c-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1737c-124">-Name</span></span>
<span data-ttu-id="1737c-125">Имя триггера.</span><span class="sxs-lookup"><span data-stu-id="1737c-125">The trigger name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName, ByFactoryObject
Aliases: TriggerName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1737c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1737c-126">-ResourceGroupName</span></span>
<span data-ttu-id="1737c-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1737c-127">The resource group name.</span></span>

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

### <span data-ttu-id="1737c-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1737c-128">-ResourceId</span></span>
<span data-ttu-id="1737c-129">Идентификатор ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="1737c-129">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1737c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1737c-130">CommonParameters</span></span>
<span data-ttu-id="1737c-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1737c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1737c-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1737c-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1737c-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1737c-133">INPUTS</span></span>

### <span data-ttu-id="1737c-134">System. String</span><span class="sxs-lookup"><span data-stu-id="1737c-134">System.String</span></span>
<span data-ttu-id="1737c-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="1737c-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="1737c-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1737c-136">OUTPUTS</span></span>

### <span data-ttu-id="1737c-137">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. DataFactoryV2. Models. PSTrigger, Microsoft. Azure. Commands. DataFactoryV2, Version = 0.1.9.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="1737c-137">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="1737c-138">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="1737c-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="1737c-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="1737c-139">NOTES</span></span>

## <span data-ttu-id="1737c-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1737c-140">RELATED LINKS</span></span>

[<span data-ttu-id="1737c-141">Set-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="1737c-141">Set-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="1737c-142">Start-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="1737c-142">Start-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="1737c-143">Остановить-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="1737c-143">Stop-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="1737c-144">Remove-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="1737c-144">Remove-AzureRmDataFactoryV2Trigger</span></span>]()
