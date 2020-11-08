---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/remove-azkustoclusterprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoClusterPrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoClusterPrincipalAssignment.md
ms.openlocfilehash: 92d6855753bdf56941d6f6ca85ec021228894a2d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248981"
---
# <span data-ttu-id="fa0a5-101">Remove-AzKustoClusterPrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="fa0a5-101">Remove-AzKustoClusterPrincipalAssignment</span></span>

## <span data-ttu-id="fa0a5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fa0a5-102">SYNOPSIS</span></span>
<span data-ttu-id="fa0a5-103">Удаление Kusto кластера principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="fa0a5-103">Deletes a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="fa0a5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fa0a5-104">SYNTAX</span></span>

### <span data-ttu-id="fa0a5-105">Удалить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fa0a5-105">Delete (Default)</span></span>
```
Remove-AzKustoClusterPrincipalAssignment -ClusterName <String> -PrincipalAssignmentName <String>
 -ResourceGroupName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="fa0a5-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="fa0a5-106">DeleteViaIdentity</span></span>
```
Remove-AzKustoClusterPrincipalAssignment -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="fa0a5-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fa0a5-107">DESCRIPTION</span></span>
<span data-ttu-id="fa0a5-108">Удаление Kusto кластера principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="fa0a5-108">Deletes a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="fa0a5-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fa0a5-109">EXAMPLES</span></span>

### <span data-ttu-id="fa0a5-110">Пример 1: удаление существующей PrincipalAssignment кластера Kusto по имени</span><span class="sxs-lookup"><span data-stu-id="fa0a5-110">Example 1: Delete an existing Kusto cluster PrincipalAssignment by name</span></span>
```powershell
PS C:\> Remove-AzKustoClusterPrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -PrincipalAssignmentName kustoprincipal1
```

<span data-ttu-id="fa0a5-111">В приведенной выше команде удаляется PrincipalAssignment с именем "kustoprincipal1" в Kusto кластере "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="fa0a5-111">The above command deletes the PrincipalAssignment named "kustoprincipal1" in the Kusto cluster  "testnewkustocluster".</span></span>

## <span data-ttu-id="fa0a5-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fa0a5-112">PARAMETERS</span></span>

### <span data-ttu-id="fa0a5-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fa0a5-113">-AsJob</span></span>
<span data-ttu-id="fa0a5-114">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="fa0a5-114">Run the command as a job</span></span>

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

### <span data-ttu-id="fa0a5-115">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="fa0a5-115">-ClusterName</span></span>
<span data-ttu-id="fa0a5-116">Имя кластера Kusto.</span><span class="sxs-lookup"><span data-stu-id="fa0a5-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="fa0a5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa0a5-117">-DefaultProfile</span></span>
<span data-ttu-id="fa0a5-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fa0a5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fa0a5-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fa0a5-119">-InputObject</span></span>
<span data-ttu-id="fa0a5-120">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="fa0a5-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fa0a5-121">-Wait</span><span class="sxs-lookup"><span data-stu-id="fa0a5-121">-NoWait</span></span>
<span data-ttu-id="fa0a5-122">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="fa0a5-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="fa0a5-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fa0a5-123">-PassThru</span></span>
<span data-ttu-id="fa0a5-124">Возвращает значение истина, если команда выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="fa0a5-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="fa0a5-125">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="fa0a5-125">-PrincipalAssignmentName</span></span>
<span data-ttu-id="fa0a5-126">Имя Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="fa0a5-126">The name of the Kusto principalAssignment.</span></span>

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

### <span data-ttu-id="fa0a5-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa0a5-127">-ResourceGroupName</span></span>
<span data-ttu-id="fa0a5-128">Имя группы ресурсов, содержащей кластер Kusto.</span><span class="sxs-lookup"><span data-stu-id="fa0a5-128">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="fa0a5-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fa0a5-129">-SubscriptionId</span></span>
<span data-ttu-id="fa0a5-130">Получение учетных данных подписки, однозначно идентифицирующей подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="fa0a5-130">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="fa0a5-131">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="fa0a5-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="fa0a5-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fa0a5-132">-Confirm</span></span>
<span data-ttu-id="fa0a5-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="fa0a5-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa0a5-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa0a5-134">-WhatIf</span></span>
<span data-ttu-id="fa0a5-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="fa0a5-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa0a5-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="fa0a5-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa0a5-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa0a5-137">CommonParameters</span></span>
<span data-ttu-id="fa0a5-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fa0a5-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa0a5-139">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fa0a5-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa0a5-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fa0a5-140">INPUTS</span></span>

### <span data-ttu-id="fa0a5-141">Microsoft. Azure. PowerShell. командлеты. Kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="fa0a5-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="fa0a5-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fa0a5-142">OUTPUTS</span></span>

### <span data-ttu-id="fa0a5-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fa0a5-143">System.Boolean</span></span>

## <span data-ttu-id="fa0a5-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="fa0a5-144">NOTES</span></span>

<span data-ttu-id="fa0a5-145">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="fa0a5-145">ALIASES</span></span>

<span data-ttu-id="fa0a5-146">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="fa0a5-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="fa0a5-147">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="fa0a5-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="fa0a5-148">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="fa0a5-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="fa0a5-149">INPUTOBJECT <IKustoIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="fa0a5-149">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="fa0a5-150">`[AttachedDatabaseConfigurationName <String>]`: Имя конфигурации присоединенной базы данных.</span><span class="sxs-lookup"><span data-stu-id="fa0a5-150">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="fa0a5-151">`[ClusterName <String>]`: Имя кластера Kusto.</span><span class="sxs-lookup"><span data-stu-id="fa0a5-151">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="fa0a5-152">`[DataConnectionName <String>]`: Имя подключения к данным.</span><span class="sxs-lookup"><span data-stu-id="fa0a5-152">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="fa0a5-153">`[DatabaseName <String>]`: Имя базы данных в кластере Kusto.</span><span class="sxs-lookup"><span data-stu-id="fa0a5-153">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="fa0a5-154">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="fa0a5-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="fa0a5-155">`[Location <String>]`: Расположение Azure.</span><span class="sxs-lookup"><span data-stu-id="fa0a5-155">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="fa0a5-156">`[PrincipalAssignmentName <String>]`: Имя Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="fa0a5-156">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="fa0a5-157">`[ResourceGroupName <String>]`: Имя группы ресурсов, содержащей кластер Kusto.</span><span class="sxs-lookup"><span data-stu-id="fa0a5-157">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="fa0a5-158">`[SubscriptionId <String>]`: Получение учетных данных подписки, которые уникально определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="fa0a5-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="fa0a5-159">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="fa0a5-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="fa0a5-160">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fa0a5-160">RELATED LINKS</span></span>

