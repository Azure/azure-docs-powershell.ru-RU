---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/remove-azkustoclusterprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoClusterPrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoClusterPrincipalAssignment.md
ms.openlocfilehash: b2dd7c125fbf2529e7dc214efdc9ef5fdef1ace0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001256"
---
# <span data-ttu-id="5d34f-101">Remove-AzKustoClusterPrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="5d34f-101">Remove-AzKustoClusterPrincipalAssignment</span></span>

## <span data-ttu-id="5d34f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5d34f-102">SYNOPSIS</span></span>
<span data-ttu-id="5d34f-103">Удаление principalAssignment кластера Кусто.</span><span class="sxs-lookup"><span data-stu-id="5d34f-103">Deletes a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="5d34f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5d34f-104">SYNTAX</span></span>

### <span data-ttu-id="5d34f-105">Delete (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5d34f-105">Delete (Default)</span></span>
```
Remove-AzKustoClusterPrincipalAssignment -ClusterName <String> -PrincipalAssignmentName <String>
 -ResourceGroupName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="5d34f-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="5d34f-106">DeleteViaIdentity</span></span>
```
Remove-AzKustoClusterPrincipalAssignment -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5d34f-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5d34f-107">DESCRIPTION</span></span>
<span data-ttu-id="5d34f-108">Удаление principalAssignment кластера Кусто.</span><span class="sxs-lookup"><span data-stu-id="5d34f-108">Deletes a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="5d34f-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5d34f-109">EXAMPLES</span></span>

### <span data-ttu-id="5d34f-110">Пример 1. Удаление существующего кластера "Кузто" principalAssignment по имени</span><span class="sxs-lookup"><span data-stu-id="5d34f-110">Example 1: Delete an existing Kusto cluster PrincipalAssignment by name</span></span>
```powershell
PS C:\> Remove-AzKustoClusterPrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -PrincipalAssignmentName kustoprincipal1
```

<span data-ttu-id="5d34f-111">С этой команды удаляется principalAssignment с именем "kustoprincipal1" в кластере Кузто "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="5d34f-111">The above command deletes the PrincipalAssignment named "kustoprincipal1" in the Kusto cluster  "testnewkustocluster".</span></span>

## <span data-ttu-id="5d34f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5d34f-112">PARAMETERS</span></span>

### <span data-ttu-id="5d34f-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5d34f-113">-AsJob</span></span>
<span data-ttu-id="5d34f-114">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="5d34f-114">Run the command as a job</span></span>

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

### <span data-ttu-id="5d34f-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="5d34f-115">-ClusterName</span></span>
<span data-ttu-id="5d34f-116">Название кластера Кусто.</span><span class="sxs-lookup"><span data-stu-id="5d34f-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="5d34f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d34f-117">-DefaultProfile</span></span>
<span data-ttu-id="5d34f-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5d34f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5d34f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5d34f-119">-InputObject</span></span>
<span data-ttu-id="5d34f-120">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="5d34f-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="5d34f-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="5d34f-121">-NoWait</span></span>
<span data-ttu-id="5d34f-122">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="5d34f-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="5d34f-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5d34f-123">-PassThru</span></span>
<span data-ttu-id="5d34f-124">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="5d34f-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="5d34f-125">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="5d34f-125">-PrincipalAssignmentName</span></span>
<span data-ttu-id="5d34f-126">Имя «Кусто principalAssignment».</span><span class="sxs-lookup"><span data-stu-id="5d34f-126">The name of the Kusto principalAssignment.</span></span>

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

### <span data-ttu-id="5d34f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d34f-127">-ResourceGroupName</span></span>
<span data-ttu-id="5d34f-128">Имя группы ресурсов, содержащей кластер Кусто.</span><span class="sxs-lookup"><span data-stu-id="5d34f-128">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="5d34f-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5d34f-129">-SubscriptionId</span></span>
<span data-ttu-id="5d34f-130">Получает учетные данные подписки, которые однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="5d34f-130">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="5d34f-131">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="5d34f-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="5d34f-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5d34f-132">-Confirm</span></span>
<span data-ttu-id="5d34f-133">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5d34f-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d34f-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d34f-134">-WhatIf</span></span>
<span data-ttu-id="5d34f-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5d34f-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5d34f-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="5d34f-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d34f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d34f-137">CommonParameters</span></span>
<span data-ttu-id="5d34f-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d34f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d34f-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5d34f-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d34f-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5d34f-140">INPUTS</span></span>

### <span data-ttu-id="5d34f-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="5d34f-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="5d34f-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5d34f-142">OUTPUTS</span></span>

### <span data-ttu-id="5d34f-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5d34f-143">System.Boolean</span></span>

## <span data-ttu-id="5d34f-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5d34f-144">NOTES</span></span>

<span data-ttu-id="5d34f-145">ALIASES</span><span class="sxs-lookup"><span data-stu-id="5d34f-145">ALIASES</span></span>

<span data-ttu-id="5d34f-146">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="5d34f-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5d34f-147">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="5d34f-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5d34f-148">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5d34f-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5d34f-149">INPUTOBJECT <IKustoIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="5d34f-149">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5d34f-150">`[AttachedDatabaseConfigurationName <String>]`: имя конфигурации вложенной базы данных.</span><span class="sxs-lookup"><span data-stu-id="5d34f-150">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="5d34f-151">`[ClusterName <String>]`Название кластера "Кусто".</span><span class="sxs-lookup"><span data-stu-id="5d34f-151">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="5d34f-152">`[DataConnectionName <String>]`: имя подключения к данным.</span><span class="sxs-lookup"><span data-stu-id="5d34f-152">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="5d34f-153">`[DatabaseName <String>]`Имя базы данных в кластере Кусто.</span><span class="sxs-lookup"><span data-stu-id="5d34f-153">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="5d34f-154">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="5d34f-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5d34f-155">`[Location <String>]`: расположение в Azure.</span><span class="sxs-lookup"><span data-stu-id="5d34f-155">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="5d34f-156">`[PrincipalAssignmentName <String>]`: Имя «Кусто principalAssignment».</span><span class="sxs-lookup"><span data-stu-id="5d34f-156">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="5d34f-157">`[ResourceGroupName <String>]`Название группы ресурсов, содержащей кластер Кусто.</span><span class="sxs-lookup"><span data-stu-id="5d34f-157">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="5d34f-158">`[SubscriptionId <String>]`: получает учетные данные подписки, которые однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="5d34f-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="5d34f-159">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="5d34f-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="5d34f-160">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5d34f-160">RELATED LINKS</span></span>

