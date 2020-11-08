---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/add-azresourcemovermoveresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Add-AzResourceMoverMoveResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Add-AzResourceMoverMoveResource.md
ms.openlocfilehash: bafba030de13cdee2c4b7026f498c07cf4231fdd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248220"
---
# <span data-ttu-id="4e67e-101">Add-AzResourceMoverMoveResource</span><span class="sxs-lookup"><span data-stu-id="4e67e-101">Add-AzResourceMoverMoveResource</span></span>

## <span data-ttu-id="4e67e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4e67e-102">SYNOPSIS</span></span>
<span data-ttu-id="4e67e-103">Создает или обновляет ресурс перемещения в коллекции Move.</span><span class="sxs-lookup"><span data-stu-id="4e67e-103">Creates or updates a Move Resource in the move collection.</span></span>

## <span data-ttu-id="4e67e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4e67e-104">SYNTAX</span></span>

```
Add-AzResourceMoverMoveResource -MoveCollectionName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DependsOnOverride <IMoveResourceDependencyOverride[]>]
 [-ExistingTargetId <String>] [-ResourceSettingResourceType <String>]
 [-ResourceSettingTargetResourceName <String>] [-SourceId <String>]
 [-SourceResourceSettingResourceType <String>] [-SourceResourceSettingTargetResourceName <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4e67e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4e67e-105">DESCRIPTION</span></span>
<span data-ttu-id="4e67e-106">Создает или обновляет ресурс перемещения в коллекции Move.</span><span class="sxs-lookup"><span data-stu-id="4e67e-106">Creates or updates a Move Resource in the move collection.</span></span>

## <span data-ttu-id="4e67e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4e67e-107">EXAMPLES</span></span>

### <span data-ttu-id="4e67e-108">Пример 1: Добавление ресурса в коллекцию Move.</span><span class="sxs-lookup"><span data-stu-id="4e67e-108">Example 1: Adding a resource to the move collection.</span></span>
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

<span data-ttu-id="4e67e-109">Добавление ресурса в коллекцию для перемещения в рамках указанной подписки.</span><span class="sxs-lookup"><span data-stu-id="4e67e-109">Adding a resource to the move collection within the specified subscription.</span></span>

## <span data-ttu-id="4e67e-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4e67e-110">PARAMETERS</span></span>

### <span data-ttu-id="4e67e-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4e67e-111">-AsJob</span></span>
<span data-ttu-id="4e67e-112">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="4e67e-112">Run the command as a job</span></span>

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

### <span data-ttu-id="4e67e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e67e-113">-DefaultProfile</span></span>
<span data-ttu-id="4e67e-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4e67e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e67e-115">-DependsOnOverride</span><span class="sxs-lookup"><span data-stu-id="4e67e-115">-DependsOnOverride</span></span>
<span data-ttu-id="4e67e-116">Возвращает или задает переопределения зависимостей ресурсов Move.</span><span class="sxs-lookup"><span data-stu-id="4e67e-116">Gets or sets the move resource dependencies overrides.</span></span>
<span data-ttu-id="4e67e-117">Для конструирования ознакомьтесь с разделом "Заметки" для свойств DEPENDSONOVERRIDE и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="4e67e-117">To construct, see NOTES section for DEPENDSONOVERRIDE properties and create a hash table.</span></span>

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

### <span data-ttu-id="4e67e-118">-ExistingTargetId</span><span class="sxs-lookup"><span data-stu-id="4e67e-118">-ExistingTargetId</span></span>
<span data-ttu-id="4e67e-119">Возвращает или задает существующий целевой идентификатор для ресурса.</span><span class="sxs-lookup"><span data-stu-id="4e67e-119">Gets or sets the existing target ARM Id of the resource.</span></span>

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

### <span data-ttu-id="4e67e-120">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="4e67e-120">-MoveCollectionName</span></span>
<span data-ttu-id="4e67e-121">Имя перемещения коллекции.</span><span class="sxs-lookup"><span data-stu-id="4e67e-121">The Move Collection Name.</span></span>

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

### <span data-ttu-id="4e67e-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4e67e-122">-Name</span></span>
<span data-ttu-id="4e67e-123">Имя ресурса для перемещения.</span><span class="sxs-lookup"><span data-stu-id="4e67e-123">The Move Resource Name.</span></span>

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

### <span data-ttu-id="4e67e-124">-Wait</span><span class="sxs-lookup"><span data-stu-id="4e67e-124">-NoWait</span></span>
<span data-ttu-id="4e67e-125">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="4e67e-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="4e67e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e67e-126">-ResourceGroupName</span></span>
<span data-ttu-id="4e67e-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4e67e-127">The Resource Group Name.</span></span>

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

### <span data-ttu-id="4e67e-128">-ResourceSettingResourceType</span><span class="sxs-lookup"><span data-stu-id="4e67e-128">-ResourceSettingResourceType</span></span>
<span data-ttu-id="4e67e-129">Тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="4e67e-129">The resource type.</span></span>
<span data-ttu-id="4e67e-130">Например, значение может быть Microsoft. COMPUTE/virtualMachines.</span><span class="sxs-lookup"><span data-stu-id="4e67e-130">For example, the value can be Microsoft.Compute/virtualMachines.</span></span>

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

### <span data-ttu-id="4e67e-131">-ResourceSettingTargetResourceName</span><span class="sxs-lookup"><span data-stu-id="4e67e-131">-ResourceSettingTargetResourceName</span></span>
<span data-ttu-id="4e67e-132">Возвращает или задает имя целевого ресурса.</span><span class="sxs-lookup"><span data-stu-id="4e67e-132">Gets or sets the target Resource name.</span></span>

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

### <span data-ttu-id="4e67e-133">-SourceId</span><span class="sxs-lookup"><span data-stu-id="4e67e-133">-SourceId</span></span>
<span data-ttu-id="4e67e-134">Возвращает или задает код ARM источника ресурса.</span><span class="sxs-lookup"><span data-stu-id="4e67e-134">Gets or sets the Source ARM Id of the resource.</span></span>

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

### <span data-ttu-id="4e67e-135">-SourceResourceSettingResourceType</span><span class="sxs-lookup"><span data-stu-id="4e67e-135">-SourceResourceSettingResourceType</span></span>
<span data-ttu-id="4e67e-136">Тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="4e67e-136">The resource type.</span></span>
<span data-ttu-id="4e67e-137">Например, значение может быть Microsoft. COMPUTE/virtualMachines.</span><span class="sxs-lookup"><span data-stu-id="4e67e-137">For example, the value can be Microsoft.Compute/virtualMachines.</span></span>

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

### <span data-ttu-id="4e67e-138">-SourceResourceSettingTargetResourceName</span><span class="sxs-lookup"><span data-stu-id="4e67e-138">-SourceResourceSettingTargetResourceName</span></span>
<span data-ttu-id="4e67e-139">Возвращает или задает имя целевого ресурса.</span><span class="sxs-lookup"><span data-stu-id="4e67e-139">Gets or sets the target Resource name.</span></span>

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

### <span data-ttu-id="4e67e-140">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4e67e-140">-SubscriptionId</span></span>
<span data-ttu-id="4e67e-141">Идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="4e67e-141">The Subscription ID.</span></span>

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

### <span data-ttu-id="4e67e-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4e67e-142">-Confirm</span></span>
<span data-ttu-id="4e67e-143">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4e67e-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e67e-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e67e-144">-WhatIf</span></span>
<span data-ttu-id="4e67e-145">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4e67e-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e67e-146">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4e67e-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e67e-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e67e-147">CommonParameters</span></span>
<span data-ttu-id="4e67e-148">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4e67e-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e67e-149">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4e67e-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e67e-150">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4e67e-150">INPUTS</span></span>

## <span data-ttu-id="4e67e-151">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4e67e-151">OUTPUTS</span></span>

### <span data-ttu-id="4e67e-152">Microsoft. Azure. PowerShell. командлеты. ResourceMover. Models. Api20191001Preview. IMoveResource</span><span class="sxs-lookup"><span data-stu-id="4e67e-152">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IMoveResource</span></span>

## <span data-ttu-id="4e67e-153">Пуск</span><span class="sxs-lookup"><span data-stu-id="4e67e-153">NOTES</span></span>

<span data-ttu-id="4e67e-154">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="4e67e-154">ALIASES</span></span>

<span data-ttu-id="4e67e-155">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="4e67e-155">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4e67e-156">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="4e67e-156">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4e67e-157">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4e67e-157">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4e67e-158">DEPENDSONOVERRIDE <IMoveResourceDependencyOverride [] >: Получает или задает изменения зависимостей ресурсов Move.</span><span class="sxs-lookup"><span data-stu-id="4e67e-158">DEPENDSONOVERRIDE <IMoveResourceDependencyOverride[]>: Gets or sets the move resource dependencies overrides.</span></span>
  - <span data-ttu-id="4e67e-159">`[Id <String>]`: Получает или задает идентификатор ARM зависимого ресурса.</span><span class="sxs-lookup"><span data-stu-id="4e67e-159">`[Id <String>]`: Gets or sets the ARM ID of the dependent resource.</span></span>
  - <span data-ttu-id="4e67e-160">`[TargetId <String>]`. Возвращает или задает идентификатор ARM ресурса либо MoveResource, либо идентификатор ARM ресурса зависимого ресурса.</span><span class="sxs-lookup"><span data-stu-id="4e67e-160">`[TargetId <String>]`: Gets or sets the resource ARM id of either the MoveResource or the resource ARM ID of         the dependent resource.</span></span>

## <span data-ttu-id="4e67e-161">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4e67e-161">RELATED LINKS</span></span>

