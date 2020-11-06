---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Trigger.md
ms.openlocfilehash: 3d5db6b7aa1b7c2ffdd63292696230e2d12bd4c0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560451"
---
# <span data-ttu-id="063e5-101">Get-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="063e5-101">Get-AzureRmDataFactoryV2Trigger</span></span>

## <span data-ttu-id="063e5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="063e5-102">SYNOPSIS</span></span>
<span data-ttu-id="063e5-103">Получение сведений о триггерах в фабрике данных.</span><span class="sxs-lookup"><span data-stu-id="063e5-103">Gets information about triggers in a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="063e5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="063e5-104">SYNTAX</span></span>

### <span data-ttu-id="063e5-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="063e5-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryV2Trigger [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="063e5-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="063e5-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryV2Trigger [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="063e5-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="063e5-107">DESCRIPTION</span></span>
<span data-ttu-id="063e5-108">Командлет **Get-AzureRmDataFactoryV2Trigger** получает сведения о триггерах в фабрике данных.</span><span class="sxs-lookup"><span data-stu-id="063e5-108">The **Get-AzureRmDataFactoryV2Trigger** cmdlet gets information about triggers in a data factory.</span></span> <span data-ttu-id="063e5-109">Если вы задаете имя триггера, командлет получает сведения об этом триггере.</span><span class="sxs-lookup"><span data-stu-id="063e5-109">If you specify the name of a trigger, the cmdlet gets information about that trigger.</span></span> <span data-ttu-id="063e5-110">Если имя не задано, командлет получает сведения обо всех триггерах в фабрике данных.</span><span class="sxs-lookup"><span data-stu-id="063e5-110">If you do not specify a name, the cmdlet gets information about all triggers in the data factory.</span></span>

## <span data-ttu-id="063e5-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="063e5-111">EXAMPLES</span></span>

### <span data-ttu-id="063e5-112">Пример 1: получение сведений об определенном триггере</span><span class="sxs-lookup"><span data-stu-id="063e5-112">Example 1: Get information about a specific trigger</span></span>
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

<span data-ttu-id="063e5-113">Получает список всех триггеров, созданных в фабрике данных "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="063e5-113">Gets a list of all triggers that have been created in the data factory "WikiADF".</span></span>

### <span data-ttu-id="063e5-114">Пример 2: получение сведений обо всех триггерах</span><span class="sxs-lookup"><span data-stu-id="063e5-114">Example 2: Get information about all triggers</span></span>
```
Get-AzureRmDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

    TriggerName       : ScheduledTrigger
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.ScheduleTrigger
    RuntimeState      : Stopped
```

<span data-ttu-id="063e5-115">Получает один триггер с именем "ScheduledTrigger" в фабрике данных "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="063e5-115">Gets a single trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span>

## <span data-ttu-id="063e5-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="063e5-116">PARAMETERS</span></span>

### <span data-ttu-id="063e5-117">— Фактическое.</span><span class="sxs-lookup"><span data-stu-id="063e5-117">-DataFactory</span></span>
<span data-ttu-id="063e5-118">Объект фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="063e5-118">The data factory object.</span></span>

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

### <span data-ttu-id="063e5-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="063e5-119">-DataFactoryName</span></span>
<span data-ttu-id="063e5-120">Имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="063e5-120">The data factory name.</span></span>

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

### <span data-ttu-id="063e5-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="063e5-121">-Name</span></span>
<span data-ttu-id="063e5-122">Имя триггера.</span><span class="sxs-lookup"><span data-stu-id="063e5-122">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TriggerName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="063e5-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="063e5-123">-ResourceGroupName</span></span>
<span data-ttu-id="063e5-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="063e5-124">The resource group name.</span></span>

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

### <span data-ttu-id="063e5-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="063e5-125">-DefaultProfile</span></span>
<span data-ttu-id="063e5-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="063e5-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="063e5-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="063e5-127">CommonParameters</span></span>
<span data-ttu-id="063e5-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="063e5-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="063e5-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="063e5-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="063e5-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="063e5-130">INPUTS</span></span>

### <span data-ttu-id="063e5-131">System. String</span><span class="sxs-lookup"><span data-stu-id="063e5-131">System.String</span></span>
<span data-ttu-id="063e5-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="063e5-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="063e5-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="063e5-133">OUTPUTS</span></span>

### <span data-ttu-id="063e5-134">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. DataFactoryV2. Models. PSTrigger, Microsoft. Azure. Commands. DataFactoryV2, Version = 0.1.9.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="063e5-134">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="063e5-135">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="063e5-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="063e5-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="063e5-136">NOTES</span></span>

## <span data-ttu-id="063e5-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="063e5-137">RELATED LINKS</span></span>

[<span data-ttu-id="063e5-138">Set-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="063e5-138">Set-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="063e5-139">Start-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="063e5-139">Start-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="063e5-140">Остановить-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="063e5-140">Stop-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="063e5-141">Remove-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="063e5-141">Remove-AzureRmDataFactoryV2Trigger</span></span>]()
