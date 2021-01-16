---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/remove-azkustodatabaseprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDatabasePrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDatabasePrincipalAssignment.md
ms.openlocfilehash: cd29af9ac8569683e6447a51f4d4f6784139f735
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98393868"
---
# <span data-ttu-id="0efee-101">Remove-AzKustoDatabasePrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="0efee-101">Remove-AzKustoDatabasePrincipalAssignment</span></span>

## <span data-ttu-id="0efee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0efee-102">SYNOPSIS</span></span>
<span data-ttu-id="0efee-103">Удаляет "Кузto principalAssignment".</span><span class="sxs-lookup"><span data-stu-id="0efee-103">Deletes a Kusto principalAssignment.</span></span>

## <span data-ttu-id="0efee-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="0efee-104">SYNTAX</span></span>

### <span data-ttu-id="0efee-105">Delete (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0efee-105">Delete (Default)</span></span>
```
Remove-AzKustoDatabasePrincipalAssignment -ClusterName <String> -DatabaseName <String>
 -PrincipalAssignmentName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="0efee-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="0efee-106">DeleteViaIdentity</span></span>
```
Remove-AzKustoDatabasePrincipalAssignment -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0efee-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0efee-107">DESCRIPTION</span></span>
<span data-ttu-id="0efee-108">Удаляет "Кузto principalAssignment".</span><span class="sxs-lookup"><span data-stu-id="0efee-108">Deletes a Kusto principalAssignment.</span></span>

## <span data-ttu-id="0efee-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="0efee-109">EXAMPLES</span></span>

### <span data-ttu-id="0efee-110">Пример 1. Удаление существующей базы данных "Кузто" PrincipalAssignment по имени</span><span class="sxs-lookup"><span data-stu-id="0efee-110">Example 1: Delete an existing Kusto database PrincipalAssignment by name</span></span>
```powershell
PS C:\> Remove-AzKustoDatabasePrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase -PrincipalAssignmentName kustoprincipal1
```

<span data-ttu-id="0efee-111">С этой командой удаляется principalAssignment kustoprincipal1 из базы данных Кузто "mykustodatabase".</span><span class="sxs-lookup"><span data-stu-id="0efee-111">The above command deletes the PrincipalAssignment named "kustoprincipal1" in the Kusto database  "mykustodatabase".</span></span>

## <span data-ttu-id="0efee-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0efee-112">PARAMETERS</span></span>

### <span data-ttu-id="0efee-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0efee-113">-AsJob</span></span>
<span data-ttu-id="0efee-114">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="0efee-114">Run the command as a job</span></span>

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

### <span data-ttu-id="0efee-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="0efee-115">-ClusterName</span></span>
<span data-ttu-id="0efee-116">Название кластера Кусто.</span><span class="sxs-lookup"><span data-stu-id="0efee-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="0efee-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="0efee-117">-DatabaseName</span></span>
<span data-ttu-id="0efee-118">Имя базы данных в кластере Кусто.</span><span class="sxs-lookup"><span data-stu-id="0efee-118">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="0efee-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0efee-119">-DefaultProfile</span></span>
<span data-ttu-id="0efee-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0efee-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0efee-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0efee-121">-InputObject</span></span>
<span data-ttu-id="0efee-122">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="0efee-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="0efee-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="0efee-123">-NoWait</span></span>
<span data-ttu-id="0efee-124">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="0efee-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="0efee-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0efee-125">-PassThru</span></span>
<span data-ttu-id="0efee-126">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="0efee-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="0efee-127">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="0efee-127">-PrincipalAssignmentName</span></span>
<span data-ttu-id="0efee-128">Имя «Кусто principalAssignment».</span><span class="sxs-lookup"><span data-stu-id="0efee-128">The name of the Kusto principalAssignment.</span></span>

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

### <span data-ttu-id="0efee-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0efee-129">-ResourceGroupName</span></span>
<span data-ttu-id="0efee-130">Имя группы ресурсов, содержащей кластер Кусто.</span><span class="sxs-lookup"><span data-stu-id="0efee-130">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="0efee-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0efee-131">-SubscriptionId</span></span>
<span data-ttu-id="0efee-132">Получает учетные данные подписки, которые однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="0efee-132">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="0efee-133">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="0efee-133">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="0efee-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0efee-134">-Confirm</span></span>
<span data-ttu-id="0efee-135">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="0efee-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0efee-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0efee-136">-WhatIf</span></span>
<span data-ttu-id="0efee-137">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0efee-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0efee-138">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="0efee-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0efee-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0efee-139">CommonParameters</span></span>
<span data-ttu-id="0efee-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0efee-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0efee-141">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0efee-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0efee-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0efee-142">INPUTS</span></span>

### <span data-ttu-id="0efee-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="0efee-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="0efee-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0efee-144">OUTPUTS</span></span>

### <span data-ttu-id="0efee-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0efee-145">System.Boolean</span></span>

## <span data-ttu-id="0efee-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="0efee-146">NOTES</span></span>

<span data-ttu-id="0efee-147">ALIASES</span><span class="sxs-lookup"><span data-stu-id="0efee-147">ALIASES</span></span>

<span data-ttu-id="0efee-148">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="0efee-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0efee-149">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="0efee-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0efee-150">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0efee-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0efee-151">INPUTOBJECT <IKustoIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="0efee-151">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0efee-152">`[AttachedDatabaseConfigurationName <String>]`: имя конфигурации вложенной базы данных.</span><span class="sxs-lookup"><span data-stu-id="0efee-152">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="0efee-153">`[ClusterName <String>]`Название кластера "Кусто".</span><span class="sxs-lookup"><span data-stu-id="0efee-153">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="0efee-154">`[DataConnectionName <String>]`: имя подключения к данным.</span><span class="sxs-lookup"><span data-stu-id="0efee-154">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="0efee-155">`[DatabaseName <String>]`Имя базы данных в кластере Кусто.</span><span class="sxs-lookup"><span data-stu-id="0efee-155">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="0efee-156">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="0efee-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0efee-157">`[Location <String>]`: расположение в Azure.</span><span class="sxs-lookup"><span data-stu-id="0efee-157">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="0efee-158">`[PrincipalAssignmentName <String>]`: Имя «Кусто principalAssignment».</span><span class="sxs-lookup"><span data-stu-id="0efee-158">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="0efee-159">`[ResourceGroupName <String>]`Название группы ресурсов, содержащей кластер Кусто.</span><span class="sxs-lookup"><span data-stu-id="0efee-159">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="0efee-160">`[SubscriptionId <String>]`. Получает учетные данные подписки, которые однозначно определяют подписку microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="0efee-160">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="0efee-161">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="0efee-161">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="0efee-162">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0efee-162">RELATED LINKS</span></span>

