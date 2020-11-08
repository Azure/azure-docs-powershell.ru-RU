---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2Trigger.md
ms.openlocfilehash: cb0d548e1fcbc7acecf1ae1457eb762d4cf81645
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94077872"
---
# <span data-ttu-id="1f82a-101">Set-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="1f82a-101">Set-AzDataFactoryV2Trigger</span></span>

## <span data-ttu-id="1f82a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1f82a-102">SYNOPSIS</span></span>
<span data-ttu-id="1f82a-103">Создание триггера в фабрике данных.</span><span class="sxs-lookup"><span data-stu-id="1f82a-103">Creates a trigger in a data factory.</span></span>

## <span data-ttu-id="1f82a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1f82a-104">SYNTAX</span></span>

### <span data-ttu-id="1f82a-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1f82a-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2Trigger [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1f82a-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="1f82a-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2Trigger [-DefinitionFile] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f82a-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1f82a-107">DESCRIPTION</span></span>
<span data-ttu-id="1f82a-108">Командлет **Set-AzDataFactoryV2Trigger** создает триггер в фабрике данных.</span><span class="sxs-lookup"><span data-stu-id="1f82a-108">The **Set-AzDataFactoryV2Trigger** cmdlet creates a trigger in a data factory.</span></span> <span data-ttu-id="1f82a-109">Если вы укажете имя триггера, который уже существует, командлет запрашивает подтверждение перед заменой триггера.</span><span class="sxs-lookup"><span data-stu-id="1f82a-109">If you specify a name for a trigger that already exists, the cmdlet prompts for confirmation before replacing the trigger.</span></span> <span data-ttu-id="1f82a-110">Если указан параметр _Force_ , командлет заменяет существующий триггер без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="1f82a-110">If you specify the _Force_ parameter, the cmdlet replaces the existing trigger without prompting for confirmation.</span></span> <span data-ttu-id="1f82a-111">Триггеры создаются в состоянии "остановлено", что означает, что они сразу же не начинают вызывать конвейеры, на которые они ссылаются.</span><span class="sxs-lookup"><span data-stu-id="1f82a-111">Triggers are created in the 'Stopped' state, meaning that they don't immediately begin invoking pipelines that they reference.</span></span>

## <span data-ttu-id="1f82a-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1f82a-112">EXAMPLES</span></span>

### <span data-ttu-id="1f82a-113">Пример 1: Создание триггера</span><span class="sxs-lookup"><span data-stu-id="1f82a-113">Example 1: Create a trigger</span></span>
```
PS C:\> Set-AzDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "ScheduledTrigger" -DefinitionFile ".\scheduledTrigger.json"

    TriggerName       : ScheduledTrigger
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.ScheduleTrigger
    RuntimeState      : Stopped
```

<span data-ttu-id="1f82a-114">Создание нового триггера с именем "ScheduledTrigger" в фабрике данных "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="1f82a-114">Create a new trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span> <span data-ttu-id="1f82a-115">Триггер создается в состоянии "остановлено", что означает, что оно не запускается сразу.</span><span class="sxs-lookup"><span data-stu-id="1f82a-115">The trigger is created in the 'Stopped' state, meaning that it doesn't immediately start.</span></span> <span data-ttu-id="1f82a-116">Триггер может быть запущен с помощью `Start-AzDataFactoryV2Trigger` командлета.</span><span class="sxs-lookup"><span data-stu-id="1f82a-116">A trigger can be started using the `Start-AzDataFactoryV2Trigger` cmdlet.</span></span>

## <span data-ttu-id="1f82a-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1f82a-117">PARAMETERS</span></span>

### <span data-ttu-id="1f82a-118">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="1f82a-118">-DataFactoryName</span></span>
<span data-ttu-id="1f82a-119">Имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="1f82a-119">The data factory name.</span></span>

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

### <span data-ttu-id="1f82a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f82a-120">-DefaultProfile</span></span>
<span data-ttu-id="1f82a-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1f82a-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1f82a-122">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="1f82a-122">-DefinitionFile</span></span>
<span data-ttu-id="1f82a-123">Путь к файлу JSON.</span><span class="sxs-lookup"><span data-stu-id="1f82a-123">The JSON file path.</span></span>

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

### <span data-ttu-id="1f82a-124">-Force</span><span class="sxs-lookup"><span data-stu-id="1f82a-124">-Force</span></span>
<span data-ttu-id="1f82a-125">Запускает командлет без запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="1f82a-125">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="1f82a-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1f82a-126">-Name</span></span>
<span data-ttu-id="1f82a-127">Имя триггера.</span><span class="sxs-lookup"><span data-stu-id="1f82a-127">The trigger name.</span></span>

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

### <span data-ttu-id="1f82a-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f82a-128">-ResourceGroupName</span></span>
<span data-ttu-id="1f82a-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1f82a-129">The resource group name.</span></span>

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

### <span data-ttu-id="1f82a-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1f82a-130">-ResourceId</span></span>
<span data-ttu-id="1f82a-131">Идентификатор ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="1f82a-131">The Azure resource ID.</span></span>

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

### <span data-ttu-id="1f82a-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1f82a-132">-Confirm</span></span>
<span data-ttu-id="1f82a-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1f82a-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f82a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f82a-134">-WhatIf</span></span>
<span data-ttu-id="1f82a-135">Показано, что происходит при запуске командлета, но не запускает командлет.</span><span class="sxs-lookup"><span data-stu-id="1f82a-135">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="1f82a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f82a-136">CommonParameters</span></span>
<span data-ttu-id="1f82a-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1f82a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f82a-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f82a-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f82a-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1f82a-139">INPUTS</span></span>

### <span data-ttu-id="1f82a-140">System. String</span><span class="sxs-lookup"><span data-stu-id="1f82a-140">System.String</span></span>

## <span data-ttu-id="1f82a-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1f82a-141">OUTPUTS</span></span>

### <span data-ttu-id="1f82a-142">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="1f82a-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="1f82a-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="1f82a-143">NOTES</span></span>

## <span data-ttu-id="1f82a-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1f82a-144">RELATED LINKS</span></span>

[<span data-ttu-id="1f82a-145">Get-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="1f82a-145">Get-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="1f82a-146">Start-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="1f82a-146">Start-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="1f82a-147">Остановить-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="1f82a-147">Stop-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="1f82a-148">Remove-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="1f82a-148">Remove-AzDataFactoryV2Trigger</span></span>]()
