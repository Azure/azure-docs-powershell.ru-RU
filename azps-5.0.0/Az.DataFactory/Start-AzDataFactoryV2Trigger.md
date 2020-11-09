---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/start-azdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Start-AzDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Start-AzDataFactoryV2Trigger.md
ms.openlocfilehash: 2a47676324f2955d02c2d50ff83d564ea150d818
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94313718"
---
# <span data-ttu-id="7cb32-101">Start-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="7cb32-101">Start-AzDataFactoryV2Trigger</span></span>

## <span data-ttu-id="7cb32-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7cb32-102">SYNOPSIS</span></span>
<span data-ttu-id="7cb32-103">Запускает триггер в фабрике данных.</span><span class="sxs-lookup"><span data-stu-id="7cb32-103">Starts a trigger in a data factory.</span></span>

## <span data-ttu-id="7cb32-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7cb32-104">SYNTAX</span></span>

### <span data-ttu-id="7cb32-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7cb32-105">ByFactoryName (Default)</span></span>
```
Start-AzDataFactoryV2Trigger [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7cb32-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="7cb32-106">ByInputObject</span></span>
```
Start-AzDataFactoryV2Trigger [-InputObject] <PSTrigger> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7cb32-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="7cb32-107">ByResourceId</span></span>
```
Start-AzDataFactoryV2Trigger [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7cb32-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7cb32-108">DESCRIPTION</span></span>
<span data-ttu-id="7cb32-109">Командлет **Start-AzDataFactoryV2Trigger** запускает триггер в фабрике данных.</span><span class="sxs-lookup"><span data-stu-id="7cb32-109">The **Start-AzDataFactoryV2Trigger** cmdlet starts a trigger in a data factory.</span></span> <span data-ttu-id="7cb32-110">Если триггер находится в состоянии "остановлено", командлет запускает триггер и в конечном итоге вызывает конвейеры на основе его определения.</span><span class="sxs-lookup"><span data-stu-id="7cb32-110">If the trigger is in the 'Stopped' state, the cmdlet starts the trigger and it eventually invokes pipelines based on its definition.</span></span> <span data-ttu-id="7cb32-111">Если триггер уже находится в состоянии "начато", этот командлет не действует.</span><span class="sxs-lookup"><span data-stu-id="7cb32-111">If the trigger is already in the 'Started' state, this cmdlet has no effect.</span></span> <span data-ttu-id="7cb32-112">Если указан параметр Force, командлет не выдает запрос перед запуском триггера.</span><span class="sxs-lookup"><span data-stu-id="7cb32-112">If the Force parameter is specified, the cmdlet doesn't prompt before starting the trigger.</span></span>

## <span data-ttu-id="7cb32-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7cb32-113">EXAMPLES</span></span>

### <span data-ttu-id="7cb32-114">Пример 1: запуск триггера</span><span class="sxs-lookup"><span data-stu-id="7cb32-114">Example 1: Start a trigger</span></span>
```
Start-AzDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

Confirm
Are you sure you want to start trigger 'ScheduledTrigger' in data factory 'WikiADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="7cb32-115">Запускает триггер с именем "ScheduledTrigger" в фабрике данных "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="7cb32-115">Starts a trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span>

## <span data-ttu-id="7cb32-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7cb32-116">PARAMETERS</span></span>

### <span data-ttu-id="7cb32-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="7cb32-117">-DataFactoryName</span></span>
<span data-ttu-id="7cb32-118">Имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="7cb32-118">The data factory name.</span></span>

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

### <span data-ttu-id="7cb32-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cb32-119">-DefaultProfile</span></span>
<span data-ttu-id="7cb32-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7cb32-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7cb32-121">-Force</span><span class="sxs-lookup"><span data-stu-id="7cb32-121">-Force</span></span>
<span data-ttu-id="7cb32-122">Запускает командлет без запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="7cb32-122">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="7cb32-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7cb32-123">-InputObject</span></span>
<span data-ttu-id="7cb32-124">Запускаемый объект.</span><span class="sxs-lookup"><span data-stu-id="7cb32-124">Trigger object to start.</span></span>

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

### <span data-ttu-id="7cb32-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7cb32-125">-Name</span></span>
<span data-ttu-id="7cb32-126">Имя триггера.</span><span class="sxs-lookup"><span data-stu-id="7cb32-126">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7cb32-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7cb32-127">-ResourceGroupName</span></span>
<span data-ttu-id="7cb32-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7cb32-128">The resource group name.</span></span>

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

### <span data-ttu-id="7cb32-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7cb32-129">-ResourceId</span></span>
<span data-ttu-id="7cb32-130">Идентификатор ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="7cb32-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="7cb32-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7cb32-131">-Confirm</span></span>
<span data-ttu-id="7cb32-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7cb32-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7cb32-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7cb32-133">-WhatIf</span></span>
<span data-ttu-id="7cb32-134">Показано, что происходит при запуске командлета, но не запускает командлет.</span><span class="sxs-lookup"><span data-stu-id="7cb32-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="7cb32-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cb32-135">CommonParameters</span></span>
<span data-ttu-id="7cb32-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7cb32-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cb32-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7cb32-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cb32-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7cb32-138">INPUTS</span></span>

### <span data-ttu-id="7cb32-139">System. String</span><span class="sxs-lookup"><span data-stu-id="7cb32-139">System.String</span></span>

### <span data-ttu-id="7cb32-140">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="7cb32-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="7cb32-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7cb32-141">OUTPUTS</span></span>

### <span data-ttu-id="7cb32-142">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="7cb32-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="7cb32-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="7cb32-143">NOTES</span></span>

## <span data-ttu-id="7cb32-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7cb32-144">RELATED LINKS</span></span>

[<span data-ttu-id="7cb32-145">Get-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="7cb32-145">Get-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="7cb32-146">Set-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="7cb32-146">Set-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="7cb32-147">Остановить-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="7cb32-147">Stop-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="7cb32-148">Remove-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="7cb32-148">Remove-AzDataFactoryV2Trigger</span></span>]()
