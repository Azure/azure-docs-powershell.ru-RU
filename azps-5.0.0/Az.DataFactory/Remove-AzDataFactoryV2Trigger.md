---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Trigger.md
ms.openlocfilehash: d5426decba60df0e18e331c01481ae4f99d5c27c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94313808"
---
# <span data-ttu-id="0244a-101">Remove-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="0244a-101">Remove-AzDataFactoryV2Trigger</span></span>

## <span data-ttu-id="0244a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0244a-102">SYNOPSIS</span></span>
<span data-ttu-id="0244a-103">Удаляет триггер из фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="0244a-103">Removes a trigger from a data factory.</span></span>

## <span data-ttu-id="0244a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0244a-104">SYNTAX</span></span>

### <span data-ttu-id="0244a-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0244a-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2Trigger [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0244a-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="0244a-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2Trigger [-InputObject] <PSTrigger> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0244a-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="0244a-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2Trigger [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0244a-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0244a-108">DESCRIPTION</span></span>
<span data-ttu-id="0244a-109">Командлет **Remove-AzDataFactoryV2Trigger** удаляет триггер из фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="0244a-109">The **Remove-AzDataFactoryV2Trigger** cmdlet removes a trigger from a data factory.</span></span> <span data-ttu-id="0244a-110">Если указан параметр _Force_ , командлет не выдает запрос перед удалением триггера.</span><span class="sxs-lookup"><span data-stu-id="0244a-110">If the _Force_ parameter is specified, the cmdlet doesn't prompt before removing the trigger.</span></span>

## <span data-ttu-id="0244a-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0244a-111">EXAMPLES</span></span>

### <span data-ttu-id="0244a-112">Пример 1: удаление триггера</span><span class="sxs-lookup"><span data-stu-id="0244a-112">Example 1: Remove a trigger</span></span>
```
Remove-AzDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "ScheduledTrigger"

Confirm
Are you sure you want to remove trigger 'ScheduledTrigger' in data factory 'TestFactory'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="0244a-113">Удаление триггера с именем "ScheduledTrigger" из фабрики данных "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="0244a-113">Remove a trigger called "ScheduledTrigger" from the data factory "WikiADF".</span></span>

## <span data-ttu-id="0244a-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0244a-114">PARAMETERS</span></span>

### <span data-ttu-id="0244a-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="0244a-115">-DataFactoryName</span></span>
<span data-ttu-id="0244a-116">Имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="0244a-116">The data factory name.</span></span>

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

### <span data-ttu-id="0244a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0244a-117">-DefaultProfile</span></span>
<span data-ttu-id="0244a-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0244a-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0244a-119">-Force</span><span class="sxs-lookup"><span data-stu-id="0244a-119">-Force</span></span>
<span data-ttu-id="0244a-120">Запускает командлет без запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="0244a-120">Runs the cmdlet without prompting for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0244a-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0244a-121">-InputObject</span></span>
<span data-ttu-id="0244a-122">Удаляемый объект триггера.</span><span class="sxs-lookup"><span data-stu-id="0244a-122">The Trigger object to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0244a-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0244a-123">-Name</span></span>
<span data-ttu-id="0244a-124">Имя триггера.</span><span class="sxs-lookup"><span data-stu-id="0244a-124">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0244a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0244a-125">-ResourceGroupName</span></span>
<span data-ttu-id="0244a-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0244a-126">The resource group name.</span></span>

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

### <span data-ttu-id="0244a-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0244a-127">-ResourceId</span></span>
<span data-ttu-id="0244a-128">Идентификатор ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="0244a-128">The Azure resource ID.</span></span>

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

### <span data-ttu-id="0244a-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0244a-129">-Confirm</span></span>
<span data-ttu-id="0244a-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0244a-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0244a-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0244a-131">-WhatIf</span></span>
<span data-ttu-id="0244a-132">Показано, что происходит при запуске командлета, но не запускает командлет.</span><span class="sxs-lookup"><span data-stu-id="0244a-132">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0244a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0244a-133">CommonParameters</span></span>
<span data-ttu-id="0244a-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0244a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0244a-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0244a-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0244a-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0244a-136">INPUTS</span></span>

### <span data-ttu-id="0244a-137">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="0244a-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

### <span data-ttu-id="0244a-138">System. String</span><span class="sxs-lookup"><span data-stu-id="0244a-138">System.String</span></span>

## <span data-ttu-id="0244a-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0244a-139">OUTPUTS</span></span>

### <span data-ttu-id="0244a-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0244a-140">System.Boolean</span></span>

## <span data-ttu-id="0244a-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="0244a-141">NOTES</span></span>

## <span data-ttu-id="0244a-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0244a-142">RELATED LINKS</span></span>

[<span data-ttu-id="0244a-143">Get-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="0244a-143">Get-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="0244a-144">Set-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="0244a-144">Set-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="0244a-145">Start-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="0244a-145">Start-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="0244a-146">Остановить-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="0244a-146">Stop-AzDataFactoryV2Trigger</span></span>]()
