---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/remove-azdatabricksvnetpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Remove-AzDatabricksVNetPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Remove-AzDatabricksVNetPeering.md
ms.openlocfilehash: 1c75bb4e8f94fadfb3b56c2fbb44889c5eaff458
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244559"
---
# <span data-ttu-id="e71ba-101">Remove-AzDatabricksVNetPeering</span><span class="sxs-lookup"><span data-stu-id="e71ba-101">Remove-AzDatabricksVNetPeering</span></span>

## <span data-ttu-id="e71ba-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e71ba-102">SYNOPSIS</span></span>
<span data-ttu-id="e71ba-103">Удаление vNetPeering рабочей области.</span><span class="sxs-lookup"><span data-stu-id="e71ba-103">Deletes the workspace vNetPeering.</span></span>

## <span data-ttu-id="e71ba-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e71ba-104">SYNTAX</span></span>

### <span data-ttu-id="e71ba-105">Удалить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e71ba-105">Delete (Default)</span></span>
```
Remove-AzDatabricksVNetPeering -Name <String> -ResourceGroupName <String> -WorkspaceName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="e71ba-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e71ba-106">DeleteViaIdentity</span></span>
```
Remove-AzDatabricksVNetPeering -InputObject <IDatabricksIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e71ba-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e71ba-107">DESCRIPTION</span></span>
<span data-ttu-id="e71ba-108">Удаление vNetPeering рабочей области.</span><span class="sxs-lookup"><span data-stu-id="e71ba-108">Deletes the workspace vNetPeering.</span></span>

## <span data-ttu-id="e71ba-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e71ba-109">EXAMPLES</span></span>

### <span data-ttu-id="e71ba-110">Пример 1: удаление однорангового соединения vnet из модуля данных по имени</span><span class="sxs-lookup"><span data-stu-id="e71ba-110">Example 1: Remove a vnet peering of databricks by name</span></span>
```powershell
PS C:\> Remove-AzDatabricksVNetPeering -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test -Name vnetpeering-t01

```

<span data-ttu-id="e71ba-111">Эта команда удаляет пиринг сети vnet из модуля данных по имени.</span><span class="sxs-lookup"><span data-stu-id="e71ba-111">This command removes a vnet peering of databricks by name</span></span>

### <span data-ttu-id="e71ba-112">Пример 2: удаление однорангового соединения vnet из модуля данных с помощью объекта</span><span class="sxs-lookup"><span data-stu-id="e71ba-112">Example 2: Remove a vnet peering of databricks by object</span></span>
```powershell
PS C:\> Get-AzDatabricksVNetPeering -ResourceGroupName lucas-manual-test -WorkspaceName databricks-test01 -PeeringName MyPeering-test01 | Remove-AzDatabricksVNetPeering

```

<span data-ttu-id="e71ba-113">Эта команда удаляет одноранговый элемент vnet из модуля данных с помощью объекта</span><span class="sxs-lookup"><span data-stu-id="e71ba-113">This command removes a vnet peering of databricks by object</span></span>

## <span data-ttu-id="e71ba-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e71ba-114">PARAMETERS</span></span>

### <span data-ttu-id="e71ba-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e71ba-115">-AsJob</span></span>
<span data-ttu-id="e71ba-116">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="e71ba-116">Run the command as a job</span></span>

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

### <span data-ttu-id="e71ba-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e71ba-117">-DefaultProfile</span></span>
<span data-ttu-id="e71ba-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e71ba-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e71ba-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e71ba-119">-InputObject</span></span>
<span data-ttu-id="e71ba-120">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="e71ba-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="e71ba-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e71ba-121">-Name</span></span>
<span data-ttu-id="e71ba-122">Имя одноранговой сети виртуальной среды.</span><span class="sxs-lookup"><span data-stu-id="e71ba-122">The name of the workspace vNet peering.</span></span>

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

### <span data-ttu-id="e71ba-123">-Wait</span><span class="sxs-lookup"><span data-stu-id="e71ba-123">-NoWait</span></span>
<span data-ttu-id="e71ba-124">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="e71ba-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="e71ba-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e71ba-125">-PassThru</span></span>
<span data-ttu-id="e71ba-126">Возвращает значение истина, если команда выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="e71ba-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="e71ba-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e71ba-127">-ResourceGroupName</span></span>
<span data-ttu-id="e71ba-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e71ba-128">The name of the resource group.</span></span>
<span data-ttu-id="e71ba-129">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="e71ba-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="e71ba-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e71ba-130">-SubscriptionId</span></span>
<span data-ttu-id="e71ba-131">Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="e71ba-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="e71ba-132">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e71ba-132">-WorkspaceName</span></span>
<span data-ttu-id="e71ba-133">Имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="e71ba-133">The name of the workspace.</span></span>

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

### <span data-ttu-id="e71ba-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e71ba-134">-Confirm</span></span>
<span data-ttu-id="e71ba-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e71ba-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e71ba-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e71ba-136">-WhatIf</span></span>
<span data-ttu-id="e71ba-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e71ba-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e71ba-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e71ba-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e71ba-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e71ba-139">CommonParameters</span></span>
<span data-ttu-id="e71ba-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e71ba-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e71ba-141">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e71ba-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e71ba-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e71ba-142">INPUTS</span></span>

### <span data-ttu-id="e71ba-143">Microsoft. Azure. PowerShell. командлеты. кирпичи. Models. IDatabricksIdentity</span><span class="sxs-lookup"><span data-stu-id="e71ba-143">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="e71ba-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e71ba-144">OUTPUTS</span></span>

### <span data-ttu-id="e71ba-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e71ba-145">System.Boolean</span></span>

## <span data-ttu-id="e71ba-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="e71ba-146">NOTES</span></span>

<span data-ttu-id="e71ba-147">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="e71ba-147">ALIASES</span></span>

<span data-ttu-id="e71ba-148">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="e71ba-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e71ba-149">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="e71ba-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e71ba-150">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e71ba-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e71ba-151">INPUTOBJECT <IDatabricksIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="e71ba-151">INPUTOBJECT <IDatabricksIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e71ba-152">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="e71ba-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e71ba-153">`[PeeringName <String>]`: Имя одноранговой сети виртуальной среды.</span><span class="sxs-lookup"><span data-stu-id="e71ba-153">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="e71ba-154">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e71ba-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="e71ba-155">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="e71ba-155">The name is case insensitive.</span></span>
  - <span data-ttu-id="e71ba-156">`[SubscriptionId <String>]`: Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="e71ba-156">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="e71ba-157">`[WorkspaceName <String>]`: Имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="e71ba-157">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="e71ba-158">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e71ba-158">RELATED LINKS</span></span>

