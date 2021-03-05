---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/powershell/module/az.resourcemover/invoke-azresourcemoverbulkremove
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverBulkRemove.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverBulkRemove.md
ms.openlocfilehash: f9815c32526a5ce462a50ec167771d30bc840b1e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999987"
---
# <span data-ttu-id="8b572-101">Invoke-AzResourceMoverBulkRemove</span><span class="sxs-lookup"><span data-stu-id="8b572-101">Invoke-AzResourceMoverBulkRemove</span></span>

## <span data-ttu-id="8b572-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b572-102">SYNOPSIS</span></span>
<span data-ttu-id="8b572-103">Удаляет из коллекции ресурсов перемещения набор ресурсов, включенных в запрос.</span><span class="sxs-lookup"><span data-stu-id="8b572-103">Removes the set of move resources included in the request body from move collection.</span></span>
<span data-ttu-id="8b572-104">Развяжение будет сделано службой.</span><span class="sxs-lookup"><span data-stu-id="8b572-104">The orchestration is done by service.</span></span>
<span data-ttu-id="8b572-105">Чтобы помочь пользователю в предварительной проверке операции, клиент может позвонить, если для свойства validateOnly за установлено истинное имя.</span><span class="sxs-lookup"><span data-stu-id="8b572-105">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="8b572-106">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8b572-106">SYNTAX</span></span>

```
Invoke-AzResourceMoverBulkRemove -MoveCollectionName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-MoveResource <String[]>] [-MoveResourceInputType <MoveResourceInputType>]
 [-ValidateOnly] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8b572-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8b572-107">DESCRIPTION</span></span>
<span data-ttu-id="8b572-108">Удаляет из коллекции ресурсов перемещения набор ресурсов, включенных в запрос.</span><span class="sxs-lookup"><span data-stu-id="8b572-108">Removes the set of move resources included in the request body from move collection.</span></span>
<span data-ttu-id="8b572-109">Развяжение будет сделано службой.</span><span class="sxs-lookup"><span data-stu-id="8b572-109">The orchestration is done by service.</span></span>
<span data-ttu-id="8b572-110">Чтобы помочь пользователю в предварительной проверке операции, клиент может позвонить, если для свойства validateOnly за установлено истинное имя.</span><span class="sxs-lookup"><span data-stu-id="8b572-110">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="8b572-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8b572-111">EXAMPLES</span></span>

### <span data-ttu-id="8b572-112">Пример 1. Проверка зависимовлений перед удалением ресурсов из коллекции перемещения</span><span class="sxs-lookup"><span data-stu-id="8b572-112">Example 1: Validate the dependecies before remove of the Move Resources from Move Collection</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverBulkRemove -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS"  -MoveResource $('PSDemoVM') -MoveResourceInputType "MoveResourceId" -ValidateOnly

AdditionalInfo : 
Code           : 
Detail         : 
EndTime        : 2/10/2021 12:52:28 PM
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveCollections/PS-centralus-westcentralu
                 s-demoRMS/operations/b4e3f140-b36b-4fd5-a507-b1e663ecf7a3
Message        : 
Name           : b4e3f140-b36b-4fd5-a507-b1e663ecf7a3
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/10/2021 12:52:28 PM
Status         : Succeeded

```

<span data-ttu-id="8b572-113">Прежде чем удалять ресурсы из перемещаемого сбора, проверьте их зависимость.</span><span class="sxs-lookup"><span data-stu-id="8b572-113">Validate the dependecies before remove of the move resources from Move Collection.</span></span>

### <span data-ttu-id="8b572-114">Пример 2. Удаление ресурса из коллекции перемещения с использованием имени MoveResource в качестве входных данных</span><span class="sxs-lookup"><span data-stu-id="8b572-114">Example 2: Remove the Move Resource from Move Collection using "MoveResource Name" as input</span></span>
```powershell
Invoke-AzResourceMoverBulkRemove -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS"  -MoveResource $('PSDemoVM') -MoveResourceInputType "MoveResourceId"

AdditionalInfo : 
Code           : 
Detail         : 
EndTime        : 2/10/2021 12:58:10 PM
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveCollections/PS-centralus-westcentralu
                 s-demoRMS/operations/d4827071-b797-45c5-b88c-00ddd7818d42
Message        : 
Name           : d4827071-b797-45c5-b88c-00ddd7818d42
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/10/2021 12:57:08 PM
Status         : Succeeded
```

<span data-ttu-id="8b572-115">Удаление ресурса из перемещаемой коллекции с использованием в качестве входных данных MoveResource Name</span><span class="sxs-lookup"><span data-stu-id="8b572-115">Remove the Move Resource from Move Collection using "MoveResource Name" as input</span></span>

### <span data-ttu-id="8b572-116">Пример 3. Удаление ресурса из коллекции "Перемещение" с использованием входных данных SourceARMID</span><span class="sxs-lookup"><span data-stu-id="8b572-116">Example 3: Remove the Move Resource from Move Collection using "SourceARMID" as input</span></span>
```powershell
Invoke-AzResourceMoverBulkRemove -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS"  -MoveResource $('/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/PSDemoRM/providers/Microsoft.Network/networkSecurityGroups/PSDemoVM-nsg') -MoveResourceInputType "MoveResourceSourceId"

AdditionalInfo : 
Code           : 
Detail         : 
EndTime        : 2/10/2021 1:05:13 PM
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveCollections/PS-centralus-westcentralu
                 s-demoRMS/operations/7b6904e2-fc3f-400d-b248-8908fcb282fb
Message        : 
Name           : 7b6904e2-fc3f-400d-b248-8908fcb282fb
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/10/2021 1:05:00 PM
Status         : Succeeded
```

<span data-ttu-id="8b572-117">Удаление ресурса из коллекции "Перемещение" с использованием входных данных SourceARMID</span><span class="sxs-lookup"><span data-stu-id="8b572-117">Remove the Move Resource from Move Collection using "SourceARMID" as input</span></span>

## <span data-ttu-id="8b572-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8b572-118">PARAMETERS</span></span>

### <span data-ttu-id="8b572-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8b572-119">-AsJob</span></span>
<span data-ttu-id="8b572-120">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="8b572-120">Run the command as a job</span></span>

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

### <span data-ttu-id="8b572-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b572-121">-DefaultProfile</span></span>
<span data-ttu-id="8b572-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8b572-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b572-123">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="8b572-123">-MoveCollectionName</span></span>
<span data-ttu-id="8b572-124">.</span><span class="sxs-lookup"><span data-stu-id="8b572-124">.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b572-125">-MoveResource</span><span class="sxs-lookup"><span data-stu-id="8b572-125">-MoveResource</span></span>
<span data-ttu-id="8b572-126">Возвращает или задает список ИД ресурсов, по умолчанию он принимает перемещение ид ресурса, если тип ввода не был переключен с помощью свойства moveResourceInputType.</span><span class="sxs-lookup"><span data-stu-id="8b572-126">Gets or sets the list of resource Id's, by default it accepts move resource id's unless the input type is switched via moveResourceInputType property.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b572-127">-MoveResourceInputType</span><span class="sxs-lookup"><span data-stu-id="8b572-127">-MoveResourceInputType</span></span>
<span data-ttu-id="8b572-128">Определяет тип ввода для перемещения ресурса.</span><span class="sxs-lookup"><span data-stu-id="8b572-128">Defines the move resource input type.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Support.MoveResourceInputType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b572-129">-NoWait</span><span class="sxs-lookup"><span data-stu-id="8b572-129">-NoWait</span></span>
<span data-ttu-id="8b572-130">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="8b572-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="8b572-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b572-131">-ResourceGroupName</span></span>
<span data-ttu-id="8b572-132">.</span><span class="sxs-lookup"><span data-stu-id="8b572-132">.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b572-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8b572-133">-SubscriptionId</span></span>
<span data-ttu-id="8b572-134">ИД подписки.</span><span class="sxs-lookup"><span data-stu-id="8b572-134">The Subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b572-135">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="8b572-135">-ValidateOnly</span></span>
<span data-ttu-id="8b572-136">Возвращает или задает значение, указывающее, требуется ли выполнить только предварительные требования.</span><span class="sxs-lookup"><span data-stu-id="8b572-136">Gets or sets a value indicating whether the operation needs to only run pre-requisite.</span></span>

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

### <span data-ttu-id="8b572-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8b572-137">-Confirm</span></span>
<span data-ttu-id="8b572-138">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8b572-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b572-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b572-139">-WhatIf</span></span>
<span data-ttu-id="8b572-140">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8b572-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b572-141">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="8b572-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b572-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b572-142">CommonParameters</span></span>
<span data-ttu-id="8b572-143">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b572-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b572-144">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8b572-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b572-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8b572-145">INPUTS</span></span>

## <span data-ttu-id="8b572-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8b572-146">OUTPUTS</span></span>

### <span data-ttu-id="8b572-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="8b572-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IOperationStatus</span></span>

## <span data-ttu-id="8b572-148">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8b572-148">NOTES</span></span>

<span data-ttu-id="8b572-149">ALIASES</span><span class="sxs-lookup"><span data-stu-id="8b572-149">ALIASES</span></span>

## <span data-ttu-id="8b572-150">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8b572-150">RELATED LINKS</span></span>

