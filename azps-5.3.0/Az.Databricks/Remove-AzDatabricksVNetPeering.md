---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/remove-azdatabricksvnetpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Remove-AzDatabricksVNetPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Remove-AzDatabricksVNetPeering.md
ms.openlocfilehash: 1c75bb4e8f94fadfb3b56c2fbb44889c5eaff458
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98516934"
---
# <span data-ttu-id="0c159-101">Remove-AzDatabricksVNetPeering</span><span class="sxs-lookup"><span data-stu-id="0c159-101">Remove-AzDatabricksVNetPeering</span></span>

## <span data-ttu-id="0c159-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c159-102">SYNOPSIS</span></span>
<span data-ttu-id="0c159-103">Удаляет рабочее пространство vNetPeering.</span><span class="sxs-lookup"><span data-stu-id="0c159-103">Deletes the workspace vNetPeering.</span></span>

## <span data-ttu-id="0c159-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="0c159-104">SYNTAX</span></span>

### <span data-ttu-id="0c159-105">Delete (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0c159-105">Delete (Default)</span></span>
```
Remove-AzDatabricksVNetPeering -Name <String> -ResourceGroupName <String> -WorkspaceName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="0c159-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="0c159-106">DeleteViaIdentity</span></span>
```
Remove-AzDatabricksVNetPeering -InputObject <IDatabricksIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0c159-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0c159-107">DESCRIPTION</span></span>
<span data-ttu-id="0c159-108">Удаляет рабочее пространство vNetPeering.</span><span class="sxs-lookup"><span data-stu-id="0c159-108">Deletes the workspace vNetPeering.</span></span>

## <span data-ttu-id="0c159-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="0c159-109">EXAMPLES</span></span>

### <span data-ttu-id="0c159-110">Пример 1. Удаление пиринга vnet по имени</span><span class="sxs-lookup"><span data-stu-id="0c159-110">Example 1: Remove a vnet peering of databricks by name</span></span>
```powershell
PS C:\> Remove-AzDatabricksVNetPeering -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test -Name vnetpeering-t01

```

<span data-ttu-id="0c159-111">Эта команда удаляет пиринг vnet по именам данных.</span><span class="sxs-lookup"><span data-stu-id="0c159-111">This command removes a vnet peering of databricks by name</span></span>

### <span data-ttu-id="0c159-112">Пример 2. Удаление пиринга vnet по объектам</span><span class="sxs-lookup"><span data-stu-id="0c159-112">Example 2: Remove a vnet peering of databricks by object</span></span>
```powershell
PS C:\> Get-AzDatabricksVNetPeering -ResourceGroupName lucas-manual-test -WorkspaceName databricks-test01 -PeeringName MyPeering-test01 | Remove-AzDatabricksVNetPeering

```

<span data-ttu-id="0c159-113">Эта команда удаляет пиринг vnet объектов-кубов данных.</span><span class="sxs-lookup"><span data-stu-id="0c159-113">This command removes a vnet peering of databricks by object</span></span>

## <span data-ttu-id="0c159-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0c159-114">PARAMETERS</span></span>

### <span data-ttu-id="0c159-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0c159-115">-AsJob</span></span>
<span data-ttu-id="0c159-116">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="0c159-116">Run the command as a job</span></span>

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

### <span data-ttu-id="0c159-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c159-117">-DefaultProfile</span></span>
<span data-ttu-id="0c159-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0c159-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c159-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0c159-119">-InputObject</span></span>
<span data-ttu-id="0c159-120">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="0c159-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0c159-121">-Name</span><span class="sxs-lookup"><span data-stu-id="0c159-121">-Name</span></span>
<span data-ttu-id="0c159-122">Имя пиринга vNet рабочей области.</span><span class="sxs-lookup"><span data-stu-id="0c159-122">The name of the workspace vNet peering.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c159-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="0c159-123">-NoWait</span></span>
<span data-ttu-id="0c159-124">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="0c159-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="0c159-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0c159-125">-PassThru</span></span>
<span data-ttu-id="0c159-126">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="0c159-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="0c159-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c159-127">-ResourceGroupName</span></span>
<span data-ttu-id="0c159-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0c159-128">The name of the resource group.</span></span>
<span data-ttu-id="0c159-129">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="0c159-129">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c159-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0c159-130">-SubscriptionId</span></span>
<span data-ttu-id="0c159-131">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="0c159-131">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c159-132">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="0c159-132">-WorkspaceName</span></span>
<span data-ttu-id="0c159-133">Имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="0c159-133">The name of the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c159-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0c159-134">-Confirm</span></span>
<span data-ttu-id="0c159-135">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="0c159-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c159-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c159-136">-WhatIf</span></span>
<span data-ttu-id="0c159-137">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c159-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c159-138">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="0c159-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c159-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c159-139">CommonParameters</span></span>
<span data-ttu-id="0c159-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c159-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c159-141">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0c159-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c159-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0c159-142">INPUTS</span></span>

### <span data-ttu-id="0c159-143">Microsoft.Azure.PowerShell.Cmdlets.Datab models.Models.IDatabоsIdentity</span><span class="sxs-lookup"><span data-stu-id="0c159-143">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="0c159-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0c159-144">OUTPUTS</span></span>

### <span data-ttu-id="0c159-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0c159-145">System.Boolean</span></span>

## <span data-ttu-id="0c159-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="0c159-146">NOTES</span></span>

<span data-ttu-id="0c159-147">ALIASES</span><span class="sxs-lookup"><span data-stu-id="0c159-147">ALIASES</span></span>

<span data-ttu-id="0c159-148">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="0c159-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0c159-149">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="0c159-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0c159-150">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0c159-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0c159-151">INPUTOBJECT <IDatabricksIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="0c159-151">INPUTOBJECT <IDatabricksIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0c159-152">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="0c159-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0c159-153">`[PeeringName <String>]`: имя пиринга vNet рабочей области.</span><span class="sxs-lookup"><span data-stu-id="0c159-153">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="0c159-154">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0c159-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="0c159-155">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="0c159-155">The name is case insensitive.</span></span>
  - <span data-ttu-id="0c159-156">`[SubscriptionId <String>]`: ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="0c159-156">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="0c159-157">`[WorkspaceName <String>]`: название рабочей области.</span><span class="sxs-lookup"><span data-stu-id="0c159-157">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="0c159-158">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0c159-158">RELATED LINKS</span></span>

