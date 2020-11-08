---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/remove-azdatabricksworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Remove-AzDatabricksWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Remove-AzDatabricksWorkspace.md
ms.openlocfilehash: 629b12a7db506b0a96633396b97e0df3d66e1760
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94077809"
---
# <span data-ttu-id="a3d22-101">Remove-AzDatabricksWorkspace</span><span class="sxs-lookup"><span data-stu-id="a3d22-101">Remove-AzDatabricksWorkspace</span></span>

## <span data-ttu-id="a3d22-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a3d22-102">SYNOPSIS</span></span>
<span data-ttu-id="a3d22-103">Удаление рабочей области.</span><span class="sxs-lookup"><span data-stu-id="a3d22-103">Deletes the workspace.</span></span>

## <span data-ttu-id="a3d22-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a3d22-104">SYNTAX</span></span>

### <span data-ttu-id="a3d22-105">Удалить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a3d22-105">Delete (Default)</span></span>
```
Remove-AzDatabricksWorkspace -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a3d22-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a3d22-106">DeleteViaIdentity</span></span>
```
Remove-AzDatabricksWorkspace -InputObject <IDatabricksIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a3d22-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a3d22-107">DESCRIPTION</span></span>
<span data-ttu-id="a3d22-108">Удаление рабочей области.</span><span class="sxs-lookup"><span data-stu-id="a3d22-108">Deletes the workspace.</span></span>

## <span data-ttu-id="a3d22-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a3d22-109">EXAMPLES</span></span>

### <span data-ttu-id="a3d22-110">Пример 1: Удаление рабочей области "кирпичные"</span><span class="sxs-lookup"><span data-stu-id="a3d22-110">Example 1: Remove a Databricks workspace</span></span>
```powershell
PS C:\> Remove-AzDatabricksWorkspace -ResourceGroupName testgroup -Name databricks-test
```

<span data-ttu-id="a3d22-111">Эта команда удаляет рабочую область "модуль из группы ресурсов".</span><span class="sxs-lookup"><span data-stu-id="a3d22-111">This command removes a Databricks workspace from a resource group.</span></span>

### <span data-ttu-id="a3d22-112">Пример 2: Удаление модуля DataObjects по объекту</span><span class="sxs-lookup"><span data-stu-id="a3d22-112">Example 2: Remove a Databricks workspace by object</span></span>
```powershell
PS C:\> $dbr = Get-AzDatabricksWorkspace -ResourceGroupName testgroup -Name databricks-test02
PS C:\> Remove-AzDatabricksWorkspace -InputObject $dbr
```

<span data-ttu-id="a3d22-113">Эта команда удаляет рабочую область "модуль из группы ресурсов".</span><span class="sxs-lookup"><span data-stu-id="a3d22-113">This command removes a Databricks workspace from a resource group.</span></span>

## <span data-ttu-id="a3d22-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a3d22-114">PARAMETERS</span></span>

### <span data-ttu-id="a3d22-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a3d22-115">-AsJob</span></span>
<span data-ttu-id="a3d22-116">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="a3d22-116">Run the command as a job</span></span>

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

### <span data-ttu-id="a3d22-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3d22-117">-DefaultProfile</span></span>
<span data-ttu-id="a3d22-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a3d22-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3d22-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a3d22-119">-InputObject</span></span>
<span data-ttu-id="a3d22-120">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="a3d22-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a3d22-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a3d22-121">-Name</span></span>
<span data-ttu-id="a3d22-122">Имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="a3d22-122">The name of the workspace.</span></span>

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

### <span data-ttu-id="a3d22-123">-Wait</span><span class="sxs-lookup"><span data-stu-id="a3d22-123">-NoWait</span></span>
<span data-ttu-id="a3d22-124">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="a3d22-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="a3d22-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a3d22-125">-PassThru</span></span>
<span data-ttu-id="a3d22-126">Возвращает значение истина, если команда выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="a3d22-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="a3d22-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3d22-127">-ResourceGroupName</span></span>
<span data-ttu-id="a3d22-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a3d22-128">The name of the resource group.</span></span>
<span data-ttu-id="a3d22-129">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="a3d22-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="a3d22-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a3d22-130">-SubscriptionId</span></span>
<span data-ttu-id="a3d22-131">Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="a3d22-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="a3d22-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a3d22-132">-Confirm</span></span>
<span data-ttu-id="a3d22-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a3d22-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3d22-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3d22-134">-WhatIf</span></span>
<span data-ttu-id="a3d22-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a3d22-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3d22-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a3d22-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3d22-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3d22-137">CommonParameters</span></span>
<span data-ttu-id="a3d22-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a3d22-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3d22-139">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a3d22-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3d22-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a3d22-140">INPUTS</span></span>

### <span data-ttu-id="a3d22-141">Microsoft. Azure. PowerShell. командлеты. кирпичи. Models. IDatabricksIdentity</span><span class="sxs-lookup"><span data-stu-id="a3d22-141">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="a3d22-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a3d22-142">OUTPUTS</span></span>

### <span data-ttu-id="a3d22-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a3d22-143">System.Boolean</span></span>

## <span data-ttu-id="a3d22-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="a3d22-144">NOTES</span></span>

<span data-ttu-id="a3d22-145">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="a3d22-145">ALIASES</span></span>

<span data-ttu-id="a3d22-146">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="a3d22-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a3d22-147">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="a3d22-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a3d22-148">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a3d22-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a3d22-149">INPUTOBJECT <IDatabricksIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="a3d22-149">INPUTOBJECT <IDatabricksIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a3d22-150">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="a3d22-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a3d22-151">`[PeeringName <String>]`: Имя одноранговой сети виртуальной среды.</span><span class="sxs-lookup"><span data-stu-id="a3d22-151">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="a3d22-152">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a3d22-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="a3d22-153">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="a3d22-153">The name is case insensitive.</span></span>
  - <span data-ttu-id="a3d22-154">`[SubscriptionId <String>]`: Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="a3d22-154">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="a3d22-155">`[WorkspaceName <String>]`: Имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="a3d22-155">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="a3d22-156">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a3d22-156">RELATED LINKS</span></span>

