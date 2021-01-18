---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/add-azresourcemovermoveresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Add-AzResourceMoverMoveResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Add-AzResourceMoverMoveResource.md
ms.openlocfilehash: bafba030de13cdee2c4b7026f498c07cf4231fdd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505972"
---
# <span data-ttu-id="c63cb-101">Add-AzResourceMoverMoveResource</span><span class="sxs-lookup"><span data-stu-id="c63cb-101">Add-AzResourceMoverMoveResource</span></span>

## <span data-ttu-id="c63cb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c63cb-102">SYNOPSIS</span></span>
<span data-ttu-id="c63cb-103">Создает или обновляет перемещение ресурса в коллекции перемещения.</span><span class="sxs-lookup"><span data-stu-id="c63cb-103">Creates or updates a Move Resource in the move collection.</span></span>

## <span data-ttu-id="c63cb-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c63cb-104">SYNTAX</span></span>

```
Add-AzResourceMoverMoveResource -MoveCollectionName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DependsOnOverride <IMoveResourceDependencyOverride[]>]
 [-ExistingTargetId <String>] [-ResourceSettingResourceType <String>]
 [-ResourceSettingTargetResourceName <String>] [-SourceId <String>]
 [-SourceResourceSettingResourceType <String>] [-SourceResourceSettingTargetResourceName <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c63cb-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c63cb-105">DESCRIPTION</span></span>
<span data-ttu-id="c63cb-106">Создает или обновляет перемещение ресурса в коллекции перемещения.</span><span class="sxs-lookup"><span data-stu-id="c63cb-106">Creates or updates a Move Resource in the move collection.</span></span>

## <span data-ttu-id="c63cb-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c63cb-107">EXAMPLES</span></span>

### <span data-ttu-id="c63cb-108">Пример 1. Добавление ресурса в коллекцию перемещения.</span><span class="sxs-lookup"><span data-stu-id="c63cb-108">Example 1: Adding a resource to the move collection.</span></span>
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

<span data-ttu-id="c63cb-109">Добавление ресурса в коллекцию перемещения в пределах указанной подписки.</span><span class="sxs-lookup"><span data-stu-id="c63cb-109">Adding a resource to the move collection within the specified subscription.</span></span>

## <span data-ttu-id="c63cb-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c63cb-110">PARAMETERS</span></span>

### <span data-ttu-id="c63cb-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c63cb-111">-AsJob</span></span>
<span data-ttu-id="c63cb-112">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="c63cb-112">Run the command as a job</span></span>

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

### <span data-ttu-id="c63cb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c63cb-113">-DefaultProfile</span></span>
<span data-ttu-id="c63cb-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c63cb-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c63cb-115">-DependsOnOverride</span><span class="sxs-lookup"><span data-stu-id="c63cb-115">-DependsOnOverride</span></span>
<span data-ttu-id="c63cb-116">Переопределения зависимостей перемещения ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c63cb-116">Gets or sets the move resource dependencies overrides.</span></span>
<span data-ttu-id="c63cb-117">Чтобы создать новую таблицу, см. раздел "ЗАМЕТКИ" для свойств DEPENDSONOVERRIDE и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="c63cb-117">To construct, see NOTES section for DEPENDSONOVERRIDE properties and create a hash table.</span></span>

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

### <span data-ttu-id="c63cb-118">-ExistingTargetId</span><span class="sxs-lookup"><span data-stu-id="c63cb-118">-ExistingTargetId</span></span>
<span data-ttu-id="c63cb-119">Возвращает или задает существующий ARM ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="c63cb-119">Gets or sets the existing target ARM Id of the resource.</span></span>

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

### <span data-ttu-id="c63cb-120">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="c63cb-120">-MoveCollectionName</span></span>
<span data-ttu-id="c63cb-121">Имя коллекции для перемещения.</span><span class="sxs-lookup"><span data-stu-id="c63cb-121">The Move Collection Name.</span></span>

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

### <span data-ttu-id="c63cb-122">-Name</span><span class="sxs-lookup"><span data-stu-id="c63cb-122">-Name</span></span>
<span data-ttu-id="c63cb-123">Имя перемещение ресурса.</span><span class="sxs-lookup"><span data-stu-id="c63cb-123">The Move Resource Name.</span></span>

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

### <span data-ttu-id="c63cb-124">-NoWait</span><span class="sxs-lookup"><span data-stu-id="c63cb-124">-NoWait</span></span>
<span data-ttu-id="c63cb-125">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="c63cb-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="c63cb-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c63cb-126">-ResourceGroupName</span></span>
<span data-ttu-id="c63cb-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c63cb-127">The Resource Group Name.</span></span>

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

### <span data-ttu-id="c63cb-128">-ResourceSettingResourceType</span><span class="sxs-lookup"><span data-stu-id="c63cb-128">-ResourceSettingResourceType</span></span>
<span data-ttu-id="c63cb-129">Тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="c63cb-129">The resource type.</span></span>
<span data-ttu-id="c63cb-130">Например, это может быть Microsoft.Compute/virtualMaиes.</span><span class="sxs-lookup"><span data-stu-id="c63cb-130">For example, the value can be Microsoft.Compute/virtualMachines.</span></span>

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

### <span data-ttu-id="c63cb-131">-ResourceSettingTargetResourceName</span><span class="sxs-lookup"><span data-stu-id="c63cb-131">-ResourceSettingTargetResourceName</span></span>
<span data-ttu-id="c63cb-132">Возвращает или задает имя целевого ресурса.</span><span class="sxs-lookup"><span data-stu-id="c63cb-132">Gets or sets the target Resource name.</span></span>

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

### <span data-ttu-id="c63cb-133">-SourceId</span><span class="sxs-lookup"><span data-stu-id="c63cb-133">-SourceId</span></span>
<span data-ttu-id="c63cb-134">Получает или задает исходный ARM ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="c63cb-134">Gets or sets the Source ARM Id of the resource.</span></span>

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

### <span data-ttu-id="c63cb-135">-SourceResourceSettingResourceType</span><span class="sxs-lookup"><span data-stu-id="c63cb-135">-SourceResourceSettingResourceType</span></span>
<span data-ttu-id="c63cb-136">Тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="c63cb-136">The resource type.</span></span>
<span data-ttu-id="c63cb-137">Например, это может быть Microsoft.Compute/virtualMaиes.</span><span class="sxs-lookup"><span data-stu-id="c63cb-137">For example, the value can be Microsoft.Compute/virtualMachines.</span></span>

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

### <span data-ttu-id="c63cb-138">-SourceResourceSettingTargetResourceName</span><span class="sxs-lookup"><span data-stu-id="c63cb-138">-SourceResourceSettingTargetResourceName</span></span>
<span data-ttu-id="c63cb-139">Возвращает или задает имя целевого ресурса.</span><span class="sxs-lookup"><span data-stu-id="c63cb-139">Gets or sets the target Resource name.</span></span>

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

### <span data-ttu-id="c63cb-140">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c63cb-140">-SubscriptionId</span></span>
<span data-ttu-id="c63cb-141">ИД подписки.</span><span class="sxs-lookup"><span data-stu-id="c63cb-141">The Subscription ID.</span></span>

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

### <span data-ttu-id="c63cb-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c63cb-142">-Confirm</span></span>
<span data-ttu-id="c63cb-143">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c63cb-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c63cb-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c63cb-144">-WhatIf</span></span>
<span data-ttu-id="c63cb-145">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c63cb-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c63cb-146">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="c63cb-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c63cb-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c63cb-147">CommonParameters</span></span>
<span data-ttu-id="c63cb-148">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c63cb-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c63cb-149">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c63cb-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c63cb-150">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c63cb-150">INPUTS</span></span>

## <span data-ttu-id="c63cb-151">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c63cb-151">OUTPUTS</span></span>

### <span data-ttu-id="c63cb-152">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IMoveResource</span><span class="sxs-lookup"><span data-stu-id="c63cb-152">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IMoveResource</span></span>

## <span data-ttu-id="c63cb-153">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c63cb-153">NOTES</span></span>

<span data-ttu-id="c63cb-154">ALIASES</span><span class="sxs-lookup"><span data-stu-id="c63cb-154">ALIASES</span></span>

<span data-ttu-id="c63cb-155">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="c63cb-155">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c63cb-156">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="c63cb-156">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c63cb-157">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c63cb-157">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c63cb-158">DEPENDSONOVERRIDE <IMoveResourceDependencyOverride[]>: получает или устанавливает переопределения зависимостей перемещения ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c63cb-158">DEPENDSONOVERRIDE <IMoveResourceDependencyOverride[]>: Gets or sets the move resource dependencies overrides.</span></span>
  - <span data-ttu-id="c63cb-159">`[Id <String>]`: получает или задает ARM зависимый ресурс.</span><span class="sxs-lookup"><span data-stu-id="c63cb-159">`[Id <String>]`: Gets or sets the ARM ID of the dependent resource.</span></span>
  - <span data-ttu-id="c63cb-160">`[TargetId <String>]`: возвращает или задает ARM ресурса как ресурса MoveResource, так и ARM для зависимого ресурса.</span><span class="sxs-lookup"><span data-stu-id="c63cb-160">`[TargetId <String>]`: Gets or sets the resource ARM id of either the MoveResource or the resource ARM ID of         the dependent resource.</span></span>

## <span data-ttu-id="c63cb-161">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c63cb-161">RELATED LINKS</span></span>

