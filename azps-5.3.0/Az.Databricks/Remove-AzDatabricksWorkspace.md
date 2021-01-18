---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/remove-azdatabricksworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Remove-AzDatabricksWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Remove-AzDatabricksWorkspace.md
ms.openlocfilehash: 629b12a7db506b0a96633396b97e0df3d66e1760
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98516925"
---
# <span data-ttu-id="9eb28-101">Remove-AzDatabricksWorkspace</span><span class="sxs-lookup"><span data-stu-id="9eb28-101">Remove-AzDatabricksWorkspace</span></span>

## <span data-ttu-id="9eb28-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9eb28-102">SYNOPSIS</span></span>
<span data-ttu-id="9eb28-103">Удаляет рабочее пространство.</span><span class="sxs-lookup"><span data-stu-id="9eb28-103">Deletes the workspace.</span></span>

## <span data-ttu-id="9eb28-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9eb28-104">SYNTAX</span></span>

### <span data-ttu-id="9eb28-105">Delete (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9eb28-105">Delete (Default)</span></span>
```
Remove-AzDatabricksWorkspace -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="9eb28-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="9eb28-106">DeleteViaIdentity</span></span>
```
Remove-AzDatabricksWorkspace -InputObject <IDatabricksIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9eb28-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9eb28-107">DESCRIPTION</span></span>
<span data-ttu-id="9eb28-108">Удаляет рабочее пространство.</span><span class="sxs-lookup"><span data-stu-id="9eb28-108">Deletes the workspace.</span></span>

## <span data-ttu-id="9eb28-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9eb28-109">EXAMPLES</span></span>

### <span data-ttu-id="9eb28-110">Пример 1. Удаление рабочей области "Данные"</span><span class="sxs-lookup"><span data-stu-id="9eb28-110">Example 1: Remove a Databricks workspace</span></span>
```powershell
PS C:\> Remove-AzDatabricksWorkspace -ResourceGroupName testgroup -Name databricks-test
```

<span data-ttu-id="9eb28-111">Эта команда удаляет из группы ресурсов рабочее пространство Datab ветвей.</span><span class="sxs-lookup"><span data-stu-id="9eb28-111">This command removes a Databricks workspace from a resource group.</span></span>

### <span data-ttu-id="9eb28-112">Пример 2. Удаление рабочей области datab у объектов</span><span class="sxs-lookup"><span data-stu-id="9eb28-112">Example 2: Remove a Databricks workspace by object</span></span>
```powershell
PS C:\> $dbr = Get-AzDatabricksWorkspace -ResourceGroupName testgroup -Name databricks-test02
PS C:\> Remove-AzDatabricksWorkspace -InputObject $dbr
```

<span data-ttu-id="9eb28-113">Эта команда удаляет из группы ресурсов рабочее пространство Datab ветвей.</span><span class="sxs-lookup"><span data-stu-id="9eb28-113">This command removes a Databricks workspace from a resource group.</span></span>

## <span data-ttu-id="9eb28-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9eb28-114">PARAMETERS</span></span>

### <span data-ttu-id="9eb28-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9eb28-115">-AsJob</span></span>
<span data-ttu-id="9eb28-116">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="9eb28-116">Run the command as a job</span></span>

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

### <span data-ttu-id="9eb28-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9eb28-117">-DefaultProfile</span></span>
<span data-ttu-id="9eb28-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9eb28-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9eb28-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9eb28-119">-InputObject</span></span>
<span data-ttu-id="9eb28-120">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="9eb28-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="9eb28-121">-Name</span><span class="sxs-lookup"><span data-stu-id="9eb28-121">-Name</span></span>
<span data-ttu-id="9eb28-122">Имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="9eb28-122">The name of the workspace.</span></span>

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

### <span data-ttu-id="9eb28-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="9eb28-123">-NoWait</span></span>
<span data-ttu-id="9eb28-124">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="9eb28-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="9eb28-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9eb28-125">-PassThru</span></span>
<span data-ttu-id="9eb28-126">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="9eb28-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="9eb28-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9eb28-127">-ResourceGroupName</span></span>
<span data-ttu-id="9eb28-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9eb28-128">The name of the resource group.</span></span>
<span data-ttu-id="9eb28-129">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="9eb28-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="9eb28-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9eb28-130">-SubscriptionId</span></span>
<span data-ttu-id="9eb28-131">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="9eb28-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="9eb28-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9eb28-132">-Confirm</span></span>
<span data-ttu-id="9eb28-133">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="9eb28-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9eb28-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9eb28-134">-WhatIf</span></span>
<span data-ttu-id="9eb28-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9eb28-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9eb28-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="9eb28-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9eb28-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9eb28-137">CommonParameters</span></span>
<span data-ttu-id="9eb28-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9eb28-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9eb28-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9eb28-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9eb28-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9eb28-140">INPUTS</span></span>

### <span data-ttu-id="9eb28-141">Microsoft.Azure.PowerShell.Cmdlets.Datab models.Models.IDatabоsIdentity</span><span class="sxs-lookup"><span data-stu-id="9eb28-141">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="9eb28-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9eb28-142">OUTPUTS</span></span>

### <span data-ttu-id="9eb28-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9eb28-143">System.Boolean</span></span>

## <span data-ttu-id="9eb28-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9eb28-144">NOTES</span></span>

<span data-ttu-id="9eb28-145">ALIASES</span><span class="sxs-lookup"><span data-stu-id="9eb28-145">ALIASES</span></span>

<span data-ttu-id="9eb28-146">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="9eb28-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9eb28-147">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="9eb28-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9eb28-148">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="9eb28-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9eb28-149">INPUTOBJECT <IDatabricksIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="9eb28-149">INPUTOBJECT <IDatabricksIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9eb28-150">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="9eb28-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9eb28-151">`[PeeringName <String>]`: имя пиринга vNet рабочей области.</span><span class="sxs-lookup"><span data-stu-id="9eb28-151">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="9eb28-152">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9eb28-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="9eb28-153">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="9eb28-153">The name is case insensitive.</span></span>
  - <span data-ttu-id="9eb28-154">`[SubscriptionId <String>]`: ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="9eb28-154">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="9eb28-155">`[WorkspaceName <String>]`: название рабочей области.</span><span class="sxs-lookup"><span data-stu-id="9eb28-155">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="9eb28-156">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9eb28-156">RELATED LINKS</span></span>

