---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Start-AzureRmDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Start-AzureRmDataFactoryV2Trigger.md
ms.openlocfilehash: d49e04f4a791f6cbf5d609d6553fddcc26dc34e3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733388"
---
# <span data-ttu-id="adf04-101">Start-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="adf04-101">Start-AzureRmDataFactoryV2Trigger</span></span>

## <span data-ttu-id="adf04-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="adf04-102">SYNOPSIS</span></span>
<span data-ttu-id="adf04-103">Запускает триггер в фабрике данных.</span><span class="sxs-lookup"><span data-stu-id="adf04-103">Starts a trigger in a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="adf04-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="adf04-104">SYNTAX</span></span>

### <span data-ttu-id="adf04-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="adf04-105">ByFactoryName (Default)</span></span>
```
Start-AzureRmDataFactoryV2Trigger [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="adf04-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="adf04-106">ByInputObject</span></span>
```
Start-AzureRmDataFactoryV2Trigger [-InputObject] <PSTrigger> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="adf04-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="adf04-107">ByResourceId</span></span>
```
Start-AzureRmDataFactoryV2Trigger [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="adf04-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="adf04-108">DESCRIPTION</span></span>
<span data-ttu-id="adf04-109">Командлет **Start-AzureRmDataFactoryV2Trigger** запускает триггер в фабрике данных.</span><span class="sxs-lookup"><span data-stu-id="adf04-109">The **Start-AzureRmDataFactoryV2Trigger** cmdlet starts a trigger in a data factory.</span></span> <span data-ttu-id="adf04-110">Если триггер находится в состоянии "остановлено", командлет запускает триггер и в конечном итоге вызывает конвейеры на основе его определения.</span><span class="sxs-lookup"><span data-stu-id="adf04-110">If the trigger is in the 'Stopped' state, the cmdlet starts the trigger and it eventually invokes pipelines based on its definition.</span></span> <span data-ttu-id="adf04-111">Если триггер уже находится в состоянии "начато", этот командлет не действует.</span><span class="sxs-lookup"><span data-stu-id="adf04-111">If the trigger is already in the 'Started' state, this cmdlet has no effect.</span></span> <span data-ttu-id="adf04-112">Если указан параметр Force, командлет не выдает запрос перед запуском триггера.</span><span class="sxs-lookup"><span data-stu-id="adf04-112">If the Force parameter is specified, the cmdlet doesn't prompt before starting the trigger.</span></span>

## <span data-ttu-id="adf04-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="adf04-113">EXAMPLES</span></span>

### <span data-ttu-id="adf04-114">Пример 1: запуск триггера</span><span class="sxs-lookup"><span data-stu-id="adf04-114">Example 1: Start a trigger</span></span>
```
Start-AzureRmDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

Confirm
Are you sure you want to start trigger 'ScheduledTrigger' in data factory 'WikiADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="adf04-115">Запускает триггер с именем "ScheduledTrigger" в фабрике данных "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="adf04-115">Starts a trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span>

## <span data-ttu-id="adf04-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="adf04-116">PARAMETERS</span></span>

### <span data-ttu-id="adf04-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="adf04-117">-Confirm</span></span>
<span data-ttu-id="adf04-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="adf04-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="adf04-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="adf04-119">-DataFactoryName</span></span>
<span data-ttu-id="adf04-120">Имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="adf04-120">The data factory name.</span></span>

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

### <span data-ttu-id="adf04-121">-Force</span><span class="sxs-lookup"><span data-stu-id="adf04-121">-Force</span></span>
<span data-ttu-id="adf04-122">Запускает командлет без запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="adf04-122">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="adf04-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="adf04-123">-Name</span></span>
<span data-ttu-id="adf04-124">Имя триггера.</span><span class="sxs-lookup"><span data-stu-id="adf04-124">The trigger name.</span></span>

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

### <span data-ttu-id="adf04-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="adf04-125">-ResourceGroupName</span></span>
<span data-ttu-id="adf04-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="adf04-126">The resource group name.</span></span>

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

### <span data-ttu-id="adf04-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="adf04-127">-ResourceId</span></span>
<span data-ttu-id="adf04-128">Идентификатор ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="adf04-128">The Azure resource ID.</span></span>

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

### <span data-ttu-id="adf04-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="adf04-129">-InputObject</span></span>
<span data-ttu-id="adf04-130">Запускаемый объект.</span><span class="sxs-lookup"><span data-stu-id="adf04-130">Trigger object to start.</span></span>

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

### <span data-ttu-id="adf04-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="adf04-131">-WhatIf</span></span>
<span data-ttu-id="adf04-132">Показано, что происходит при запуске командлета, но не запускает командлет.</span><span class="sxs-lookup"><span data-stu-id="adf04-132">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="adf04-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="adf04-133">-DefaultProfile</span></span>
<span data-ttu-id="adf04-134">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="adf04-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="adf04-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adf04-135">CommonParameters</span></span>
<span data-ttu-id="adf04-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="adf04-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adf04-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="adf04-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adf04-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="adf04-138">INPUTS</span></span>

### <span data-ttu-id="adf04-139">System. String</span><span class="sxs-lookup"><span data-stu-id="adf04-139">System.String</span></span>
<span data-ttu-id="adf04-140">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="adf04-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="adf04-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="adf04-141">OUTPUTS</span></span>

### <span data-ttu-id="adf04-142">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. DataFactoryV2. Models. PSTrigger, Microsoft. Azure. Commands. DataFactoryV2, Version = 0.1.9.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="adf04-142">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="adf04-143">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="adf04-143">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="adf04-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="adf04-144">NOTES</span></span>

## <span data-ttu-id="adf04-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="adf04-145">RELATED LINKS</span></span>

[<span data-ttu-id="adf04-146">Get-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="adf04-146">Get-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="adf04-147">Set-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="adf04-147">Set-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="adf04-148">Остановить-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="adf04-148">Stop-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="adf04-149">Remove-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="adf04-149">Remove-AzureRmDataFactoryV2Trigger</span></span>]()
