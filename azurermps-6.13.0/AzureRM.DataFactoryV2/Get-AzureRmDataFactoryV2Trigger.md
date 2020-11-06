---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Trigger.md
ms.openlocfilehash: 7c14b5c53cdffa51671a64ad40fe18a400ae6803
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567782"
---
# <span data-ttu-id="b6427-101">Get-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="b6427-101">Get-AzureRmDataFactoryV2Trigger</span></span>

## <span data-ttu-id="b6427-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b6427-102">SYNOPSIS</span></span>
<span data-ttu-id="b6427-103">Получение сведений о триггерах в фабрике данных.</span><span class="sxs-lookup"><span data-stu-id="b6427-103">Gets information about triggers in a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b6427-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b6427-104">SYNTAX</span></span>

### <span data-ttu-id="b6427-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b6427-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryV2Trigger [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b6427-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="b6427-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryV2Trigger [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b6427-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b6427-107">ByResourceId</span></span>
```
Get-AzureRmDataFactoryV2Trigger [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b6427-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b6427-108">DESCRIPTION</span></span>
<span data-ttu-id="b6427-109">Командлет **Get-AzureRmDataFactoryV2Trigger** получает сведения о триггерах в фабрике данных.</span><span class="sxs-lookup"><span data-stu-id="b6427-109">The **Get-AzureRmDataFactoryV2Trigger** cmdlet gets information about triggers in a data factory.</span></span> <span data-ttu-id="b6427-110">Если вы задаете имя триггера, командлет получает сведения об этом триггере.</span><span class="sxs-lookup"><span data-stu-id="b6427-110">If you specify the name of a trigger, the cmdlet gets information about that trigger.</span></span> <span data-ttu-id="b6427-111">Если имя не задано, командлет получает сведения обо всех триггерах в фабрике данных.</span><span class="sxs-lookup"><span data-stu-id="b6427-111">If you do not specify a name, the cmdlet gets information about all triggers in the data factory.</span></span>

## <span data-ttu-id="b6427-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b6427-112">EXAMPLES</span></span>

### <span data-ttu-id="b6427-113">Пример 1: получение сведений об определенном триггере</span><span class="sxs-lookup"><span data-stu-id="b6427-113">Example 1: Get information about a specific trigger</span></span>
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

<span data-ttu-id="b6427-114">Получает список всех триггеров, созданных в фабрике данных "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="b6427-114">Gets a list of all triggers that have been created in the data factory "WikiADF".</span></span>

### <span data-ttu-id="b6427-115">Пример 2: получение сведений обо всех триггерах</span><span class="sxs-lookup"><span data-stu-id="b6427-115">Example 2: Get information about all triggers</span></span>
```
Get-AzureRmDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

    TriggerName       : ScheduledTrigger
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.ScheduleTrigger
    RuntimeState      : Stopped
```

<span data-ttu-id="b6427-116">Получает один триггер с именем "ScheduledTrigger" в фабрике данных "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="b6427-116">Gets a single trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span>

## <span data-ttu-id="b6427-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b6427-117">PARAMETERS</span></span>

### <span data-ttu-id="b6427-118">— Фактическое.</span><span class="sxs-lookup"><span data-stu-id="b6427-118">-DataFactory</span></span>
<span data-ttu-id="b6427-119">Объект фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="b6427-119">The data factory object.</span></span>

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

### <span data-ttu-id="b6427-120">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="b6427-120">-DataFactoryName</span></span>
<span data-ttu-id="b6427-121">Имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="b6427-121">The data factory name.</span></span>

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

### <span data-ttu-id="b6427-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6427-122">-DefaultProfile</span></span>
<span data-ttu-id="b6427-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b6427-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6427-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b6427-124">-Name</span></span>
<span data-ttu-id="b6427-125">Имя триггера.</span><span class="sxs-lookup"><span data-stu-id="b6427-125">The trigger name.</span></span>

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

### <span data-ttu-id="b6427-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6427-126">-ResourceGroupName</span></span>
<span data-ttu-id="b6427-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b6427-127">The resource group name.</span></span>

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

### <span data-ttu-id="b6427-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b6427-128">-ResourceId</span></span>
<span data-ttu-id="b6427-129">Идентификатор ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="b6427-129">The Azure resource ID.</span></span>

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

### <span data-ttu-id="b6427-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6427-130">CommonParameters</span></span>
<span data-ttu-id="b6427-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b6427-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6427-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6427-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6427-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b6427-133">INPUTS</span></span>

### <span data-ttu-id="b6427-134">System. String</span><span class="sxs-lookup"><span data-stu-id="b6427-134">System.String</span></span>

### <span data-ttu-id="b6427-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="b6427-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>
<span data-ttu-id="b6427-136">Параметры: фактическое (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b6427-136">Parameters: DataFactory (ByValue)</span></span>

## <span data-ttu-id="b6427-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b6427-137">OUTPUTS</span></span>

### <span data-ttu-id="b6427-138">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="b6427-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="b6427-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="b6427-139">NOTES</span></span>

## <span data-ttu-id="b6427-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b6427-140">RELATED LINKS</span></span>

[<span data-ttu-id="b6427-141">Set-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="b6427-141">Set-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="b6427-142">Start-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="b6427-142">Start-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="b6427-143">Остановить-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="b6427-143">Stop-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="b6427-144">Remove-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="b6427-144">Remove-AzureRmDataFactoryV2Trigger</span></span>]()
