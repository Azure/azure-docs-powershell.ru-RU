---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/set-azurermdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2Trigger.md
ms.openlocfilehash: 17953aa02bf0242f358fd07b1173977db6318d05
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "93735214"
---
# <span data-ttu-id="6e8c1-101">Set-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="6e8c1-101">Set-AzureRmDataFactoryV2Trigger</span></span>

## <span data-ttu-id="6e8c1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6e8c1-102">SYNOPSIS</span></span>
<span data-ttu-id="6e8c1-103">Создание триггера в фабрике данных.</span><span class="sxs-lookup"><span data-stu-id="6e8c1-103">Creates a trigger in a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6e8c1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6e8c1-104">SYNTAX</span></span>

### <span data-ttu-id="6e8c1-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6e8c1-105">ByFactoryName (Default)</span></span>
```
Set-AzureRmDataFactoryV2Trigger [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6e8c1-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="6e8c1-106">ByResourceId</span></span>
```
Set-AzureRmDataFactoryV2Trigger [-DefinitionFile] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6e8c1-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6e8c1-107">DESCRIPTION</span></span>
<span data-ttu-id="6e8c1-108">Командлет **Set-AzureRmDataFactoryV2Trigger** создает триггер в фабрике данных.</span><span class="sxs-lookup"><span data-stu-id="6e8c1-108">The **Set-AzureRmDataFactoryV2Trigger** cmdlet creates a trigger in a data factory.</span></span> <span data-ttu-id="6e8c1-109">Если вы укажете имя триггера, который уже существует, командлет запрашивает подтверждение перед заменой триггера.</span><span class="sxs-lookup"><span data-stu-id="6e8c1-109">If you specify a name for a trigger that already exists, the cmdlet prompts for confirmation before replacing the trigger.</span></span> <span data-ttu-id="6e8c1-110">Если указан параметр _Force_ , командлет заменяет существующий триггер без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="6e8c1-110">If you specify the _Force_ parameter, the cmdlet replaces the existing trigger without prompting for confirmation.</span></span> <span data-ttu-id="6e8c1-111">Триггеры создаются в состоянии "остановлено", что означает, что они сразу же не начинают вызывать конвейеры, на которые они ссылаются.</span><span class="sxs-lookup"><span data-stu-id="6e8c1-111">Triggers are created in the 'Stopped' state, meaning that they don't immediately begin invoking pipelines that they reference.</span></span>

## <span data-ttu-id="6e8c1-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6e8c1-112">EXAMPLES</span></span>

### <span data-ttu-id="6e8c1-113">Пример 1: Создание триггера</span><span class="sxs-lookup"><span data-stu-id="6e8c1-113">Example 1: Create a trigger</span></span>
```
PS C:\> Set-AzureRmDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "ScheduledTrigger" -DefinitionFile ".\scheduledTrigger.json"

    TriggerName       : ScheduledTrigger
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.ScheduleTrigger
    RuntimeState      : Stopped
```

<span data-ttu-id="6e8c1-114">Создание нового триггера с именем "ScheduledTrigger" в фабрике данных "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="6e8c1-114">Create a new trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span> <span data-ttu-id="6e8c1-115">Триггер создается в состоянии "остановлено", что означает, что оно не запускается сразу.</span><span class="sxs-lookup"><span data-stu-id="6e8c1-115">The trigger is created in the 'Stopped' state, meaning that it doesn't immediately start.</span></span> <span data-ttu-id="6e8c1-116">Триггер может быть запущен с помощью `Start-AzureRmDataFactoryV2Trigger` командлета.</span><span class="sxs-lookup"><span data-stu-id="6e8c1-116">A trigger can be started using the `Start-AzureRmDataFactoryV2Trigger` cmdlet.</span></span>

## <span data-ttu-id="6e8c1-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6e8c1-117">PARAMETERS</span></span>

### <span data-ttu-id="6e8c1-118">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="6e8c1-118">-DataFactoryName</span></span>
<span data-ttu-id="6e8c1-119">Имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="6e8c1-119">The data factory name.</span></span>

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

### <span data-ttu-id="6e8c1-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e8c1-120">-DefaultProfile</span></span>
<span data-ttu-id="6e8c1-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6e8c1-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6e8c1-122">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="6e8c1-122">-DefinitionFile</span></span>
<span data-ttu-id="6e8c1-123">Путь к файлу JSON.</span><span class="sxs-lookup"><span data-stu-id="6e8c1-123">The JSON file path.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: File

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e8c1-124">-Force</span><span class="sxs-lookup"><span data-stu-id="6e8c1-124">-Force</span></span>
<span data-ttu-id="6e8c1-125">Запускает командлет без запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="6e8c1-125">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="6e8c1-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6e8c1-126">-Name</span></span>
<span data-ttu-id="6e8c1-127">Имя триггера.</span><span class="sxs-lookup"><span data-stu-id="6e8c1-127">The trigger name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e8c1-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e8c1-128">-ResourceGroupName</span></span>
<span data-ttu-id="6e8c1-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6e8c1-129">The resource group name.</span></span>

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

### <span data-ttu-id="6e8c1-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6e8c1-130">-ResourceId</span></span>
<span data-ttu-id="6e8c1-131">Идентификатор ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="6e8c1-131">The Azure resource ID.</span></span>

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

### <span data-ttu-id="6e8c1-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6e8c1-132">-Confirm</span></span>
<span data-ttu-id="6e8c1-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6e8c1-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6e8c1-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e8c1-134">-WhatIf</span></span>
<span data-ttu-id="6e8c1-135">Показано, что происходит при запуске командлета, но не запускает командлет.</span><span class="sxs-lookup"><span data-stu-id="6e8c1-135">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="6e8c1-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e8c1-136">CommonParameters</span></span>
<span data-ttu-id="6e8c1-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6e8c1-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e8c1-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e8c1-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e8c1-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6e8c1-139">INPUTS</span></span>

### <span data-ttu-id="6e8c1-140">System. String</span><span class="sxs-lookup"><span data-stu-id="6e8c1-140">System.String</span></span>

## <span data-ttu-id="6e8c1-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6e8c1-141">OUTPUTS</span></span>

### <span data-ttu-id="6e8c1-142">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="6e8c1-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="6e8c1-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="6e8c1-143">NOTES</span></span>

## <span data-ttu-id="6e8c1-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6e8c1-144">RELATED LINKS</span></span>

[<span data-ttu-id="6e8c1-145">Get-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="6e8c1-145">Get-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="6e8c1-146">Start-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="6e8c1-146">Start-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="6e8c1-147">Остановить-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="6e8c1-147">Stop-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="6e8c1-148">Remove-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="6e8c1-148">Remove-AzureRmDataFactoryV2Trigger</span></span>]()
