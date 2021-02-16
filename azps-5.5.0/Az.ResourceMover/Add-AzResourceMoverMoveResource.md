---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/add-azresourcemovermoveresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Add-AzResourceMoverMoveResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Add-AzResourceMoverMoveResource.md
ms.openlocfilehash: bafba030de13cdee2c4b7026f498c07cf4231fdd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100242624"
---
# <span data-ttu-id="c2e2d-101">Add-AzResourceMoverMoveResource</span><span class="sxs-lookup"><span data-stu-id="c2e2d-101">Add-AzResourceMoverMoveResource</span></span>

## <span data-ttu-id="c2e2d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2e2d-102">SYNOPSIS</span></span>
<span data-ttu-id="c2e2d-103">Создает или обновляет перемещение ресурса в коллекции перемещения.</span><span class="sxs-lookup"><span data-stu-id="c2e2d-103">Creates or updates a Move Resource in the move collection.</span></span>

## <span data-ttu-id="c2e2d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c2e2d-104">SYNTAX</span></span>

```
Add-AzResourceMoverMoveResource -MoveCollectionName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DependsOnOverride <IMoveResourceDependencyOverride[]>]
 [-ExistingTargetId <String>] [-ResourceSettingResourceType <String>]
 [-ResourceSettingTargetResourceName <String>] [-SourceId <String>]
 [-SourceResourceSettingResourceType <String>] [-SourceResourceSettingTargetResourceName <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c2e2d-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c2e2d-105">DESCRIPTION</span></span>
<span data-ttu-id="c2e2d-106">Создает или обновляет перемещение ресурса в коллекции перемещения.</span><span class="sxs-lookup"><span data-stu-id="c2e2d-106">Creates or updates a Move Resource in the move collection.</span></span>

## <span data-ttu-id="c2e2d-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c2e2d-107">EXAMPLES</span></span>

### <span data-ttu-id="c2e2d-108">Пример 1. Добавление ресурса в коллекцию перемещения.</span><span class="sxs-lookup"><span data-stu-id="c2e2d-108">Example 1: Adding a resource to the move collection.</span></span>
```powershell
PS C:\> Add-AzResourceMoverMoveResource -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName "PS-centralus-westcentralus-demoRM" -SourceId "/subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/PSDemoRM/providers/Microsoft.Compute/virtualMachines/PSDemoVM" -Name PSDemoVM -ResourceSettingResourceType "Microsoft.Compute/virtualMachines" -ResourceSettingTargetResourceName PSDemoVM

Output:

Code                                    :
DependsOn                               : {}
DependsOnOverride                       : {}
Detail                                  :
ExistingTargetId                        :
Id                                      : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migr
                                          ate/MoveCollections/PS-centralus-westcentralus-demoRM/MoveResources/PSDemoVM
Message                                 :
MoveStatusCode                          : DependencyComputationPending
MoveStatusDetail                        : {}
MoveStatusJobName                       :
MoveStatusJobProgress                   :
MoveStatusMessage                       : The dependency computation is not completed for resource - /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resou
                                          rceGroups/PSDemoRM/providers/Microsoft.Compute/virtualMachines/PSDemoVM.
                                              Possible Causes: Dependency computation is pending for resource.
                                              Recommended Action: Validate dependencies to compute the dependencies.

MoveStatusMoveState                     : PreparePending
MoveStatusTarget                        :
MoveStatusTargetId                      :
Name                                    : PSDemoVM
ProvisioningState                       : Succeeded
ResourceSettingResourceType             : Microsoft.Compute/virtualMachines
ResourceSettingTargetResourceName       : PSDemoVM
SourceId                                : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/PSDemoRM/providers/Microsoft.Compute/virtualMachi
                                          nes/PSDemoVM
SourceResourceSettingResourceType       : Microsoft.Compute/virtualMachines
SourceResourceSettingTargetResourceName : PSDemoVM
Target                                  :
TargetId                                :
Type          

```

<span data-ttu-id="c2e2d-109">Добавление ресурса в коллекцию перемещения в пределах указанной подписки.</span><span class="sxs-lookup"><span data-stu-id="c2e2d-109">Adding a resource to the move collection within the specified subscription.</span></span>

## <span data-ttu-id="c2e2d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c2e2d-110">PARAMETERS</span></span>

### <span data-ttu-id="c2e2d-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c2e2d-111">-AsJob</span></span>
<span data-ttu-id="c2e2d-112">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="c2e2d-112">Run the command as a job</span></span>

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

### <span data-ttu-id="c2e2d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2e2d-113">-DefaultProfile</span></span>
<span data-ttu-id="c2e2d-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c2e2d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2e2d-115">-DependsOnOverride</span><span class="sxs-lookup"><span data-stu-id="c2e2d-115">-DependsOnOverride</span></span>
<span data-ttu-id="c2e2d-116">Переопределения зависимостей перемещения ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c2e2d-116">Gets or sets the move resource dependencies overrides.</span></span>
<span data-ttu-id="c2e2d-117">Чтобы создать новую таблицу, см. раздел "ЗАМЕТКИ" для свойств DEPENDSONOVERRIDE и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="c2e2d-117">To construct, see NOTES section for DEPENDSONOVERRIDE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IMoveResourceDependencyOverride[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2e2d-118">-ExistingTargetId</span><span class="sxs-lookup"><span data-stu-id="c2e2d-118">-ExistingTargetId</span></span>
<span data-ttu-id="c2e2d-119">Возвращает или задает существующий ARM ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="c2e2d-119">Gets or sets the existing target ARM Id of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2e2d-120">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="c2e2d-120">-MoveCollectionName</span></span>
<span data-ttu-id="c2e2d-121">Имя коллекции для перемещения.</span><span class="sxs-lookup"><span data-stu-id="c2e2d-121">The Move Collection Name.</span></span>

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

### <span data-ttu-id="c2e2d-122">-Name</span><span class="sxs-lookup"><span data-stu-id="c2e2d-122">-Name</span></span>
<span data-ttu-id="c2e2d-123">Имя перемещения ресурса.</span><span class="sxs-lookup"><span data-stu-id="c2e2d-123">The Move Resource Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MoveResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2e2d-124">-NoWait</span><span class="sxs-lookup"><span data-stu-id="c2e2d-124">-NoWait</span></span>
<span data-ttu-id="c2e2d-125">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="c2e2d-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="c2e2d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2e2d-126">-ResourceGroupName</span></span>
<span data-ttu-id="c2e2d-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c2e2d-127">The Resource Group Name.</span></span>

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

### <span data-ttu-id="c2e2d-128">-ResourceSettingResourceType</span><span class="sxs-lookup"><span data-stu-id="c2e2d-128">-ResourceSettingResourceType</span></span>
<span data-ttu-id="c2e2d-129">Тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="c2e2d-129">The resource type.</span></span>
<span data-ttu-id="c2e2d-130">Например, это может быть Microsoft.Compute/virtualMaиes.</span><span class="sxs-lookup"><span data-stu-id="c2e2d-130">For example, the value can be Microsoft.Compute/virtualMachines.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2e2d-131">-ResourceSettingTargetResourceName</span><span class="sxs-lookup"><span data-stu-id="c2e2d-131">-ResourceSettingTargetResourceName</span></span>
<span data-ttu-id="c2e2d-132">Возвращает или задает имя целевого ресурса.</span><span class="sxs-lookup"><span data-stu-id="c2e2d-132">Gets or sets the target Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2e2d-133">-SourceId</span><span class="sxs-lookup"><span data-stu-id="c2e2d-133">-SourceId</span></span>
<span data-ttu-id="c2e2d-134">Получает или задает исходный ARM ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="c2e2d-134">Gets or sets the Source ARM Id of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2e2d-135">-SourceResourceSettingResourceType</span><span class="sxs-lookup"><span data-stu-id="c2e2d-135">-SourceResourceSettingResourceType</span></span>
<span data-ttu-id="c2e2d-136">Тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="c2e2d-136">The resource type.</span></span>
<span data-ttu-id="c2e2d-137">Например, это может быть Microsoft.Compute/virtualMaиes.</span><span class="sxs-lookup"><span data-stu-id="c2e2d-137">For example, the value can be Microsoft.Compute/virtualMachines.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2e2d-138">-SourceResourceSettingTargetResourceName</span><span class="sxs-lookup"><span data-stu-id="c2e2d-138">-SourceResourceSettingTargetResourceName</span></span>
<span data-ttu-id="c2e2d-139">Возвращает или задает имя целевого ресурса.</span><span class="sxs-lookup"><span data-stu-id="c2e2d-139">Gets or sets the target Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2e2d-140">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c2e2d-140">-SubscriptionId</span></span>
<span data-ttu-id="c2e2d-141">ИД подписки.</span><span class="sxs-lookup"><span data-stu-id="c2e2d-141">The Subscription ID.</span></span>

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

### <span data-ttu-id="c2e2d-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c2e2d-142">-Confirm</span></span>
<span data-ttu-id="c2e2d-143">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="c2e2d-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2e2d-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2e2d-144">-WhatIf</span></span>
<span data-ttu-id="c2e2d-145">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c2e2d-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2e2d-146">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="c2e2d-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2e2d-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2e2d-147">CommonParameters</span></span>
<span data-ttu-id="c2e2d-148">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2e2d-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2e2d-149">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c2e2d-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2e2d-150">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c2e2d-150">INPUTS</span></span>

## <span data-ttu-id="c2e2d-151">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c2e2d-151">OUTPUTS</span></span>

### <span data-ttu-id="c2e2d-152">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IMoveResource</span><span class="sxs-lookup"><span data-stu-id="c2e2d-152">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IMoveResource</span></span>

## <span data-ttu-id="c2e2d-153">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c2e2d-153">NOTES</span></span>

<span data-ttu-id="c2e2d-154">ALIASES</span><span class="sxs-lookup"><span data-stu-id="c2e2d-154">ALIASES</span></span>

<span data-ttu-id="c2e2d-155">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="c2e2d-155">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c2e2d-156">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="c2e2d-156">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c2e2d-157">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c2e2d-157">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c2e2d-158">DEPENDSONOVERRIDE <IMoveResourceDependencyOverride[]>: получает или устанавливает переопределения зависимостей перемещения ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c2e2d-158">DEPENDSONOVERRIDE <IMoveResourceDependencyOverride[]>: Gets or sets the move resource dependencies overrides.</span></span>
  - <span data-ttu-id="c2e2d-159">`[Id <String>]`: получает или задает ARM зависимый ресурс.</span><span class="sxs-lookup"><span data-stu-id="c2e2d-159">`[Id <String>]`: Gets or sets the ARM ID of the dependent resource.</span></span>
  - <span data-ttu-id="c2e2d-160">`[TargetId <String>]`: возвращает или задает ARM ресурса как ресурса MoveResource, так и ARM для зависимого ресурса.</span><span class="sxs-lookup"><span data-stu-id="c2e2d-160">`[TargetId <String>]`: Gets or sets the resource ARM id of either the MoveResource or the resource ARM ID of         the dependent resource.</span></span>

## <span data-ttu-id="c2e2d-161">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c2e2d-161">RELATED LINKS</span></span>

