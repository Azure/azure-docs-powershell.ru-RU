---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/set-azdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2Trigger.md
ms.openlocfilehash: b0058f21f472f14e97898ea81636fa000034bed5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006931"
---
# <span data-ttu-id="79594-101">Set-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="79594-101">Set-AzDataFactoryV2Trigger</span></span>

## <span data-ttu-id="79594-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79594-102">SYNOPSIS</span></span>
<span data-ttu-id="79594-103">Создает триггер в фабрике данных.</span><span class="sxs-lookup"><span data-stu-id="79594-103">Creates a trigger in a data factory.</span></span>

## <span data-ttu-id="79594-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="79594-104">SYNTAX</span></span>

### <span data-ttu-id="79594-105">ByFactoryName (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="79594-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2Trigger [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="79594-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="79594-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2Trigger [-DefinitionFile] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79594-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="79594-107">DESCRIPTION</span></span>
<span data-ttu-id="79594-108">Для этого в фабрике данных создается триггер **Set-AzDataFactoryV2Trigger.**</span><span class="sxs-lookup"><span data-stu-id="79594-108">The **Set-AzDataFactoryV2Trigger** cmdlet creates a trigger in a data factory.</span></span> <span data-ttu-id="79594-109">Если указать имя для триггера, который уже существует, перед заменой триггера будет предложено подтвердить действие.</span><span class="sxs-lookup"><span data-stu-id="79594-109">If you specify a name for a trigger that already exists, the cmdlet prompts for confirmation before replacing the trigger.</span></span> <span data-ttu-id="79594-110">При указании _параметра Force_ существующий триггер заменяется этим триггером без запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="79594-110">If you specify the _Force_ parameter, the cmdlet replaces the existing trigger without prompting for confirmation.</span></span> <span data-ttu-id="79594-111">Триггеры создаются в состоянии "Остановлено", то есть они не начинают прямо сейчас вызывать конвейеры, на которые они ссылаются.</span><span class="sxs-lookup"><span data-stu-id="79594-111">Triggers are created in the 'Stopped' state, meaning that they don't immediately begin invoking pipelines that they reference.</span></span>

## <span data-ttu-id="79594-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="79594-112">EXAMPLES</span></span>

### <span data-ttu-id="79594-113">Пример 1. Создание триггера</span><span class="sxs-lookup"><span data-stu-id="79594-113">Example 1: Create a trigger</span></span>
```
PS C:\> Set-AzDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "ScheduledTrigger" -DefinitionFile ".\scheduledTrigger.json"

    TriggerName       : ScheduledTrigger
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.ScheduleTrigger
    RuntimeState      : Stopped
```

<span data-ttu-id="79594-114">Создайте новый триггер под названием "ScheduledTrigger" в фабрике данных "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="79594-114">Create a new trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span> <span data-ttu-id="79594-115">Триггер создается в состоянии "Остановлено", то есть он не запускается сразу.</span><span class="sxs-lookup"><span data-stu-id="79594-115">The trigger is created in the 'Stopped' state, meaning that it doesn't immediately start.</span></span> <span data-ttu-id="79594-116">С помощью этого триггера можно запускать `Start-AzDataFactoryV2Trigger` триггеры.</span><span class="sxs-lookup"><span data-stu-id="79594-116">A trigger can be started using the `Start-AzDataFactoryV2Trigger` cmdlet.</span></span>

## <span data-ttu-id="79594-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="79594-117">PARAMETERS</span></span>

### <span data-ttu-id="79594-118">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="79594-118">-DataFactoryName</span></span>
<span data-ttu-id="79594-119">Название фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="79594-119">The data factory name.</span></span>

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

### <span data-ttu-id="79594-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79594-120">-DefaultProfile</span></span>
<span data-ttu-id="79594-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="79594-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="79594-122">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="79594-122">-DefinitionFile</span></span>
<span data-ttu-id="79594-123">Путь к файлу JSON.</span><span class="sxs-lookup"><span data-stu-id="79594-123">The JSON file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79594-124">-Force</span><span class="sxs-lookup"><span data-stu-id="79594-124">-Force</span></span>
<span data-ttu-id="79594-125">Выполняется cmdlet без запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="79594-125">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="79594-126">-Name</span><span class="sxs-lookup"><span data-stu-id="79594-126">-Name</span></span>
<span data-ttu-id="79594-127">Имя триггера.</span><span class="sxs-lookup"><span data-stu-id="79594-127">The trigger name.</span></span>

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

### <span data-ttu-id="79594-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79594-128">-ResourceGroupName</span></span>
<span data-ttu-id="79594-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="79594-129">The resource group name.</span></span>

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

### <span data-ttu-id="79594-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="79594-130">-ResourceId</span></span>
<span data-ttu-id="79594-131">ИД ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="79594-131">The Azure resource ID.</span></span>

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

### <span data-ttu-id="79594-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="79594-132">-Confirm</span></span>
<span data-ttu-id="79594-133">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="79594-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79594-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79594-134">-WhatIf</span></span>
<span data-ttu-id="79594-135">Показывает, что происходит, если выполняется только запуск, но не выполняется.</span><span class="sxs-lookup"><span data-stu-id="79594-135">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="79594-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79594-136">CommonParameters</span></span>
<span data-ttu-id="79594-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79594-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79594-138">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79594-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79594-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="79594-139">INPUTS</span></span>

### <span data-ttu-id="79594-140">System.String</span><span class="sxs-lookup"><span data-stu-id="79594-140">System.String</span></span>

## <span data-ttu-id="79594-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="79594-141">OUTPUTS</span></span>

### <span data-ttu-id="79594-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span><span class="sxs-lookup"><span data-stu-id="79594-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="79594-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="79594-143">NOTES</span></span>

## <span data-ttu-id="79594-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="79594-144">RELATED LINKS</span></span>

[<span data-ttu-id="79594-145">Get-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="79594-145">Get-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="79594-146">Start-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="79594-146">Start-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="79594-147">Stop-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="79594-147">Stop-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="79594-148">Remove-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="79594-148">Remove-AzDataFactoryV2Trigger</span></span>]()
