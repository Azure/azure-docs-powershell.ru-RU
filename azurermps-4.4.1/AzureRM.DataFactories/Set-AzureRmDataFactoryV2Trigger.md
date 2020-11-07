---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2Trigger.md
ms.openlocfilehash: 490965bf1edf39942272b9ef6caeb598b4e2d296
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734873"
---
# <span data-ttu-id="9d0ed-101">Set-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="9d0ed-101">Set-AzureRmDataFactoryV2Trigger</span></span>

## <span data-ttu-id="9d0ed-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9d0ed-102">SYNOPSIS</span></span>
<span data-ttu-id="9d0ed-103">Создание триггера в фабрике данных.</span><span class="sxs-lookup"><span data-stu-id="9d0ed-103">Creates a trigger in a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9d0ed-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9d0ed-104">SYNTAX</span></span>

### <span data-ttu-id="9d0ed-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9d0ed-105">ByFactoryName (Default)</span></span>
```
Set-AzureRmDataFactoryV2Trigger [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9d0ed-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="9d0ed-106">ByResourceId</span></span>
```
Set-AzureRmDataFactoryV2Trigger [-DefinitionFile] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9d0ed-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9d0ed-107">DESCRIPTION</span></span>
<span data-ttu-id="9d0ed-108">Командлет **Set-AzureRmDataFactoryV2Trigger** создает триггер в фабрике данных.</span><span class="sxs-lookup"><span data-stu-id="9d0ed-108">The **Set-AzureRmDataFactoryV2Trigger** cmdlet creates a trigger in a data factory.</span></span> <span data-ttu-id="9d0ed-109">Если вы укажете имя триггера, который уже существует, командлет запрашивает подтверждение перед заменой триггера.</span><span class="sxs-lookup"><span data-stu-id="9d0ed-109">If you specify a name for a trigger that already exists, the cmdlet prompts for confirmation before replacing the trigger.</span></span> <span data-ttu-id="9d0ed-110">Если указан параметр _Force_ , командлет заменяет существующий триггер без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="9d0ed-110">If you specify the _Force_ parameter, the cmdlet replaces the existing trigger without prompting for confirmation.</span></span> <span data-ttu-id="9d0ed-111">Триггеры создаются в состоянии "остановлено", что означает, что они сразу же не начинают вызывать конвейеры, на которые они ссылаются.</span><span class="sxs-lookup"><span data-stu-id="9d0ed-111">Triggers are created in the 'Stopped' state, meaning that they don't immediately begin invoking pipelines that they reference.</span></span>

## <span data-ttu-id="9d0ed-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9d0ed-112">EXAMPLES</span></span>

### <span data-ttu-id="9d0ed-113">Пример 1: Создание триггера</span><span class="sxs-lookup"><span data-stu-id="9d0ed-113">Example 1: Create a trigger</span></span>
```
PS C:\> Set-AzureRmDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "ScheduledTrigger" -DefinitionFile ".\scheduledTrigger.json"

    TriggerName       : ScheduledTrigger
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.ScheduleTrigger
    RuntimeState      : Stopped
```

<span data-ttu-id="9d0ed-114">Создание нового триггера с именем "ScheduledTrigger" в фабрике данных "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="9d0ed-114">Create a new trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span> <span data-ttu-id="9d0ed-115">Триггер создается в состоянии "остановлено", что означает, что оно не запускается сразу.</span><span class="sxs-lookup"><span data-stu-id="9d0ed-115">The trigger is created in the 'Stopped' state, meaning that it doesn't immediately start.</span></span> <span data-ttu-id="9d0ed-116">Триггер может быть запущен с помощью `Start-AzureRmDataFactoryV2Trigger` командлета.</span><span class="sxs-lookup"><span data-stu-id="9d0ed-116">A trigger can be started using the `Start-AzureRmDataFactoryV2Trigger` cmdlet.</span></span>

## <span data-ttu-id="9d0ed-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9d0ed-117">PARAMETERS</span></span>

### <span data-ttu-id="9d0ed-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9d0ed-118">-Confirm</span></span>
<span data-ttu-id="9d0ed-119">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9d0ed-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9d0ed-120">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="9d0ed-120">-DataFactoryName</span></span>
<span data-ttu-id="9d0ed-121">Имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="9d0ed-121">The data factory name.</span></span>

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

### <span data-ttu-id="9d0ed-122">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="9d0ed-122">-DefinitionFile</span></span>
<span data-ttu-id="9d0ed-123">Путь к файлу JSON.</span><span class="sxs-lookup"><span data-stu-id="9d0ed-123">The JSON file path.</span></span>

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

### <span data-ttu-id="9d0ed-124">-Force</span><span class="sxs-lookup"><span data-stu-id="9d0ed-124">-Force</span></span>
<span data-ttu-id="9d0ed-125">Запускает командлет без запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="9d0ed-125">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="9d0ed-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9d0ed-126">-Name</span></span>
<span data-ttu-id="9d0ed-127">Имя триггера.</span><span class="sxs-lookup"><span data-stu-id="9d0ed-127">The trigger name.</span></span>

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

### <span data-ttu-id="9d0ed-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d0ed-128">-ResourceGroupName</span></span>
<span data-ttu-id="9d0ed-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9d0ed-129">The resource group name.</span></span>

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

### <span data-ttu-id="9d0ed-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9d0ed-130">-ResourceId</span></span>
<span data-ttu-id="9d0ed-131">Идентификатор ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="9d0ed-131">The Azure resource ID.</span></span>

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

### <span data-ttu-id="9d0ed-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d0ed-132">-WhatIf</span></span>
<span data-ttu-id="9d0ed-133">Показано, что происходит при запуске командлета, но не запускает командлет.</span><span class="sxs-lookup"><span data-stu-id="9d0ed-133">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="9d0ed-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d0ed-134">-DefaultProfile</span></span>
<span data-ttu-id="9d0ed-135">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9d0ed-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9d0ed-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d0ed-136">CommonParameters</span></span>
<span data-ttu-id="9d0ed-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9d0ed-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d0ed-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d0ed-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d0ed-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9d0ed-139">INPUTS</span></span>

### <span data-ttu-id="9d0ed-140">System. String</span><span class="sxs-lookup"><span data-stu-id="9d0ed-140">System.String</span></span>

## <span data-ttu-id="9d0ed-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9d0ed-141">OUTPUTS</span></span>

### <span data-ttu-id="9d0ed-142">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="9d0ed-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="9d0ed-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="9d0ed-143">NOTES</span></span>

## <span data-ttu-id="9d0ed-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9d0ed-144">RELATED LINKS</span></span>

[<span data-ttu-id="9d0ed-145">Get-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="9d0ed-145">Get-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="9d0ed-146">Start-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="9d0ed-146">Start-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="9d0ed-147">Остановить-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="9d0ed-147">Stop-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="9d0ed-148">Remove-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="9d0ed-148">Remove-AzureRmDataFactoryV2Trigger</span></span>]()
