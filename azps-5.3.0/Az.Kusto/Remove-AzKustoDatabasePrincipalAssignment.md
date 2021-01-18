---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/remove-azkustodatabaseprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDatabasePrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDatabasePrincipalAssignment.md
ms.openlocfilehash: cd29af9ac8569683e6447a51f4d4f6784139f735
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98508298"
---
# <span data-ttu-id="d657d-101">Remove-AzKustoDatabasePrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="d657d-101">Remove-AzKustoDatabasePrincipalAssignment</span></span>

## <span data-ttu-id="d657d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d657d-102">SYNOPSIS</span></span>
<span data-ttu-id="d657d-103">Удаляет "Кузto principalAssignment".</span><span class="sxs-lookup"><span data-stu-id="d657d-103">Deletes a Kusto principalAssignment.</span></span>

## <span data-ttu-id="d657d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d657d-104">SYNTAX</span></span>

### <span data-ttu-id="d657d-105">Delete (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d657d-105">Delete (Default)</span></span>
```
Remove-AzKustoDatabasePrincipalAssignment -ClusterName <String> -DatabaseName <String>
 -PrincipalAssignmentName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d657d-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d657d-106">DeleteViaIdentity</span></span>
```
Remove-AzKustoDatabasePrincipalAssignment -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d657d-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d657d-107">DESCRIPTION</span></span>
<span data-ttu-id="d657d-108">Удаляет "Кузto principalAssignment".</span><span class="sxs-lookup"><span data-stu-id="d657d-108">Deletes a Kusto principalAssignment.</span></span>

## <span data-ttu-id="d657d-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d657d-109">EXAMPLES</span></span>

### <span data-ttu-id="d657d-110">Пример 1. Удаление существующей базы данных "Кузто" PrincipalAssignment по имени</span><span class="sxs-lookup"><span data-stu-id="d657d-110">Example 1: Delete an existing Kusto database PrincipalAssignment by name</span></span>
```powershell
PS C:\> Remove-AzKustoDatabasePrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase -PrincipalAssignmentName kustoprincipal1
```

<span data-ttu-id="d657d-111">С этой командой удаляется principalAssignment kustoprincipal1 из базы данных Кузто "mykustodatabase".</span><span class="sxs-lookup"><span data-stu-id="d657d-111">The above command deletes the PrincipalAssignment named "kustoprincipal1" in the Kusto database  "mykustodatabase".</span></span>

## <span data-ttu-id="d657d-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d657d-112">PARAMETERS</span></span>

### <span data-ttu-id="d657d-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d657d-113">-AsJob</span></span>
<span data-ttu-id="d657d-114">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="d657d-114">Run the command as a job</span></span>

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

### <span data-ttu-id="d657d-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="d657d-115">-ClusterName</span></span>
<span data-ttu-id="d657d-116">Название кластера Кусто.</span><span class="sxs-lookup"><span data-stu-id="d657d-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="d657d-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d657d-117">-DatabaseName</span></span>
<span data-ttu-id="d657d-118">Имя базы данных в кластере Кусто.</span><span class="sxs-lookup"><span data-stu-id="d657d-118">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="d657d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d657d-119">-DefaultProfile</span></span>
<span data-ttu-id="d657d-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d657d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d657d-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d657d-121">-InputObject</span></span>
<span data-ttu-id="d657d-122">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="d657d-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d657d-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="d657d-123">-NoWait</span></span>
<span data-ttu-id="d657d-124">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="d657d-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="d657d-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d657d-125">-PassThru</span></span>
<span data-ttu-id="d657d-126">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="d657d-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="d657d-127">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="d657d-127">-PrincipalAssignmentName</span></span>
<span data-ttu-id="d657d-128">Имя «Кусто principalAssignment».</span><span class="sxs-lookup"><span data-stu-id="d657d-128">The name of the Kusto principalAssignment.</span></span>

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

### <span data-ttu-id="d657d-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d657d-129">-ResourceGroupName</span></span>
<span data-ttu-id="d657d-130">Имя группы ресурсов, содержащей кластер Кусто.</span><span class="sxs-lookup"><span data-stu-id="d657d-130">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="d657d-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d657d-131">-SubscriptionId</span></span>
<span data-ttu-id="d657d-132">Получает учетные данные подписки, которые однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d657d-132">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="d657d-133">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="d657d-133">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="d657d-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d657d-134">-Confirm</span></span>
<span data-ttu-id="d657d-135">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="d657d-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d657d-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d657d-136">-WhatIf</span></span>
<span data-ttu-id="d657d-137">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d657d-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d657d-138">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="d657d-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d657d-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d657d-139">CommonParameters</span></span>
<span data-ttu-id="d657d-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d657d-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d657d-141">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d657d-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d657d-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d657d-142">INPUTS</span></span>

### <span data-ttu-id="d657d-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="d657d-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="d657d-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d657d-144">OUTPUTS</span></span>

### <span data-ttu-id="d657d-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d657d-145">System.Boolean</span></span>

## <span data-ttu-id="d657d-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d657d-146">NOTES</span></span>

<span data-ttu-id="d657d-147">ALIASES</span><span class="sxs-lookup"><span data-stu-id="d657d-147">ALIASES</span></span>

<span data-ttu-id="d657d-148">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="d657d-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d657d-149">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="d657d-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d657d-150">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d657d-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d657d-151">INPUTOBJECT <IKustoIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="d657d-151">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d657d-152">`[AttachedDatabaseConfigurationName <String>]`: имя конфигурации вложенной базы данных.</span><span class="sxs-lookup"><span data-stu-id="d657d-152">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="d657d-153">`[ClusterName <String>]`Название кластера "Кусто".</span><span class="sxs-lookup"><span data-stu-id="d657d-153">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="d657d-154">`[DataConnectionName <String>]`: имя подключения к данным.</span><span class="sxs-lookup"><span data-stu-id="d657d-154">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="d657d-155">`[DatabaseName <String>]`Имя базы данных в кластере Кусто.</span><span class="sxs-lookup"><span data-stu-id="d657d-155">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="d657d-156">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="d657d-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d657d-157">`[Location <String>]`: расположение в Azure.</span><span class="sxs-lookup"><span data-stu-id="d657d-157">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="d657d-158">`[PrincipalAssignmentName <String>]`: Имя «Кусто principalAssignment».</span><span class="sxs-lookup"><span data-stu-id="d657d-158">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="d657d-159">`[ResourceGroupName <String>]`Название группы ресурсов, содержащей кластер Кусто.</span><span class="sxs-lookup"><span data-stu-id="d657d-159">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="d657d-160">`[SubscriptionId <String>]`: получает учетные данные подписки, которые однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d657d-160">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="d657d-161">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="d657d-161">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="d657d-162">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d657d-162">RELATED LINKS</span></span>

