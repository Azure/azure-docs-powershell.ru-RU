---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/remove-azdatabricksworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Remove-AzDatabricksWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Remove-AzDatabricksWorkspace.md
ms.openlocfilehash: 629b12a7db506b0a96633396b97e0df3d66e1760
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98412076"
---
# <span data-ttu-id="e6df4-101">Remove-AzDatabricksWorkspace</span><span class="sxs-lookup"><span data-stu-id="e6df4-101">Remove-AzDatabricksWorkspace</span></span>

## <span data-ttu-id="e6df4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e6df4-102">SYNOPSIS</span></span>
<span data-ttu-id="e6df4-103">Удаляет рабочее пространство.</span><span class="sxs-lookup"><span data-stu-id="e6df4-103">Deletes the workspace.</span></span>

## <span data-ttu-id="e6df4-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e6df4-104">SYNTAX</span></span>

### <span data-ttu-id="e6df4-105">Delete (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e6df4-105">Delete (Default)</span></span>
```
Remove-AzDatabricksWorkspace -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e6df4-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e6df4-106">DeleteViaIdentity</span></span>
```
Remove-AzDatabricksWorkspace -InputObject <IDatabricksIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e6df4-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e6df4-107">DESCRIPTION</span></span>
<span data-ttu-id="e6df4-108">Удаляет рабочее пространство.</span><span class="sxs-lookup"><span data-stu-id="e6df4-108">Deletes the workspace.</span></span>

## <span data-ttu-id="e6df4-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e6df4-109">EXAMPLES</span></span>

### <span data-ttu-id="e6df4-110">Пример 1. Удаление рабочей области Datab ветвей</span><span class="sxs-lookup"><span data-stu-id="e6df4-110">Example 1: Remove a Databricks workspace</span></span>
```powershell
PS C:\> Remove-AzDatabricksWorkspace -ResourceGroupName testgroup -Name databricks-test
```

<span data-ttu-id="e6df4-111">Эта команда удаляет из группы ресурсов рабочее пространство Datab ветвей.</span><span class="sxs-lookup"><span data-stu-id="e6df4-111">This command removes a Databricks workspace from a resource group.</span></span>

### <span data-ttu-id="e6df4-112">Пример 2. Удаление рабочей области datab у объектов</span><span class="sxs-lookup"><span data-stu-id="e6df4-112">Example 2: Remove a Databricks workspace by object</span></span>
```powershell
PS C:\> $dbr = Get-AzDatabricksWorkspace -ResourceGroupName testgroup -Name databricks-test02
PS C:\> Remove-AzDatabricksWorkspace -InputObject $dbr
```

<span data-ttu-id="e6df4-113">Эта команда удаляет из группы ресурсов рабочее пространство Datab ветвей.</span><span class="sxs-lookup"><span data-stu-id="e6df4-113">This command removes a Databricks workspace from a resource group.</span></span>

## <span data-ttu-id="e6df4-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e6df4-114">PARAMETERS</span></span>

### <span data-ttu-id="e6df4-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e6df4-115">-AsJob</span></span>
<span data-ttu-id="e6df4-116">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="e6df4-116">Run the command as a job</span></span>

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

### <span data-ttu-id="e6df4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6df4-117">-DefaultProfile</span></span>
<span data-ttu-id="e6df4-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e6df4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6df4-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e6df4-119">-InputObject</span></span>
<span data-ttu-id="e6df4-120">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="e6df4-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="e6df4-121">-Name</span><span class="sxs-lookup"><span data-stu-id="e6df4-121">-Name</span></span>
<span data-ttu-id="e6df4-122">Имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="e6df4-122">The name of the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: WorkspaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6df4-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="e6df4-123">-NoWait</span></span>
<span data-ttu-id="e6df4-124">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="e6df4-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="e6df4-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e6df4-125">-PassThru</span></span>
<span data-ttu-id="e6df4-126">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="e6df4-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="e6df4-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6df4-127">-ResourceGroupName</span></span>
<span data-ttu-id="e6df4-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e6df4-128">The name of the resource group.</span></span>
<span data-ttu-id="e6df4-129">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="e6df4-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="e6df4-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e6df4-130">-SubscriptionId</span></span>
<span data-ttu-id="e6df4-131">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="e6df4-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="e6df4-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e6df4-132">-Confirm</span></span>
<span data-ttu-id="e6df4-133">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="e6df4-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6df4-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6df4-134">-WhatIf</span></span>
<span data-ttu-id="e6df4-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e6df4-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e6df4-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="e6df4-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6df4-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6df4-137">CommonParameters</span></span>
<span data-ttu-id="e6df4-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6df4-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6df4-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e6df4-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6df4-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e6df4-140">INPUTS</span></span>

### <span data-ttu-id="e6df4-141">Microsoft.Azure.PowerShell.Cmdlets.Datab models.Models.IDatabоsIdentity</span><span class="sxs-lookup"><span data-stu-id="e6df4-141">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="e6df4-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e6df4-142">OUTPUTS</span></span>

### <span data-ttu-id="e6df4-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e6df4-143">System.Boolean</span></span>

## <span data-ttu-id="e6df4-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e6df4-144">NOTES</span></span>

<span data-ttu-id="e6df4-145">ALIASES</span><span class="sxs-lookup"><span data-stu-id="e6df4-145">ALIASES</span></span>

<span data-ttu-id="e6df4-146">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="e6df4-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e6df4-147">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="e6df4-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e6df4-148">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e6df4-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e6df4-149">INPUTOBJECT <IDatabricksIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="e6df4-149">INPUTOBJECT <IDatabricksIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e6df4-150">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="e6df4-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e6df4-151">`[PeeringName <String>]`: имя пиринга vNet рабочей области.</span><span class="sxs-lookup"><span data-stu-id="e6df4-151">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="e6df4-152">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e6df4-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="e6df4-153">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="e6df4-153">The name is case insensitive.</span></span>
  - <span data-ttu-id="e6df4-154">`[SubscriptionId <String>]`: ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="e6df4-154">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="e6df4-155">`[WorkspaceName <String>]`: имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="e6df4-155">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="e6df4-156">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e6df4-156">RELATED LINKS</span></span>

