---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/remove-azurermdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Trigger.md
ms.openlocfilehash: 82af1131e2730cf1f78c0c04ff8540e2ef371d2c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557391"
---
# <span data-ttu-id="9390e-101">Remove-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="9390e-101">Remove-AzureRmDataFactoryV2Trigger</span></span>

## <span data-ttu-id="9390e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9390e-102">SYNOPSIS</span></span>
<span data-ttu-id="9390e-103">Удаляет триггер из фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="9390e-103">Removes a trigger from a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9390e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9390e-104">SYNTAX</span></span>

### <span data-ttu-id="9390e-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9390e-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2Trigger [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9390e-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="9390e-106">ByInputObject</span></span>
```
Remove-AzureRmDataFactoryV2Trigger [-InputObject] <PSTrigger> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9390e-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="9390e-107">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2Trigger [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9390e-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9390e-108">DESCRIPTION</span></span>
<span data-ttu-id="9390e-109">Командлет **Remove-AzureRmDataFactoryV2Trigger** удаляет триггер из фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="9390e-109">The **Remove-AzureRmDataFactoryV2Trigger** cmdlet removes a trigger from a data factory.</span></span> <span data-ttu-id="9390e-110">Если указан параметр _Force_ , командлет не выдает запрос перед удалением триггера.</span><span class="sxs-lookup"><span data-stu-id="9390e-110">If the _Force_ parameter is specified, the cmdlet doesn't prompt before removing the trigger.</span></span>

## <span data-ttu-id="9390e-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9390e-111">EXAMPLES</span></span>

### <span data-ttu-id="9390e-112">Пример 1: удаление триггера</span><span class="sxs-lookup"><span data-stu-id="9390e-112">Example 1: Remove a trigger</span></span>
```
Remove-AzureRmDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "ScheduledTrigger"

Confirm
Are you sure you want to remove trigger 'ScheduledTrigger' in data factory 'TestFactory'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="9390e-113">Удаление триггера с именем "ScheduledTrigger" из фабрики данных "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="9390e-113">Remove a trigger called "ScheduledTrigger" from the data factory "WikiADF".</span></span>

## <span data-ttu-id="9390e-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9390e-114">PARAMETERS</span></span>

### <span data-ttu-id="9390e-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="9390e-115">-DataFactoryName</span></span>
<span data-ttu-id="9390e-116">Имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="9390e-116">The data factory name.</span></span>

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

### <span data-ttu-id="9390e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9390e-117">-DefaultProfile</span></span>
<span data-ttu-id="9390e-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9390e-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9390e-119">-Force</span><span class="sxs-lookup"><span data-stu-id="9390e-119">-Force</span></span>
<span data-ttu-id="9390e-120">Запускает командлет без запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="9390e-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="9390e-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9390e-121">-InputObject</span></span>
<span data-ttu-id="9390e-122">Удаляемый объект триггера.</span><span class="sxs-lookup"><span data-stu-id="9390e-122">The Trigger object to remove.</span></span>

```yaml
Type: PSTrigger
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9390e-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9390e-123">-Name</span></span>
<span data-ttu-id="9390e-124">Имя триггера.</span><span class="sxs-lookup"><span data-stu-id="9390e-124">The trigger name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9390e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9390e-125">-ResourceGroupName</span></span>
<span data-ttu-id="9390e-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9390e-126">The resource group name.</span></span>

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

### <span data-ttu-id="9390e-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9390e-127">-ResourceId</span></span>
<span data-ttu-id="9390e-128">Идентификатор ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="9390e-128">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9390e-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9390e-129">-Confirm</span></span>
<span data-ttu-id="9390e-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9390e-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9390e-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9390e-131">-WhatIf</span></span>
<span data-ttu-id="9390e-132">Показано, что происходит при запуске командлета, но не запускает командлет.</span><span class="sxs-lookup"><span data-stu-id="9390e-132">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="9390e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9390e-133">CommonParameters</span></span>
<span data-ttu-id="9390e-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9390e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9390e-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9390e-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9390e-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9390e-136">INPUTS</span></span>

### <span data-ttu-id="9390e-137">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="9390e-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>
<span data-ttu-id="9390e-138">System. String</span><span class="sxs-lookup"><span data-stu-id="9390e-138">System.String</span></span>

## <span data-ttu-id="9390e-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9390e-139">OUTPUTS</span></span>

### <span data-ttu-id="9390e-140">System. Object</span><span class="sxs-lookup"><span data-stu-id="9390e-140">System.Object</span></span>

## <span data-ttu-id="9390e-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="9390e-141">NOTES</span></span>

## <span data-ttu-id="9390e-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9390e-142">RELATED LINKS</span></span>

[<span data-ttu-id="9390e-143">Get-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="9390e-143">Get-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="9390e-144">Set-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="9390e-144">Set-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="9390e-145">Start-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="9390e-145">Start-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="9390e-146">Остановить-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="9390e-146">Stop-AzureRmDataFactoryV2Trigger</span></span>]()

