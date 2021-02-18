---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/remove-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDatabase.md
ms.openlocfilehash: cfb5eb3c65434f0f62af03bcca57174010041e58
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100228353"
---
# <span data-ttu-id="36e9c-101">Remove-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="36e9c-101">Remove-AzKustoDatabase</span></span>

## <span data-ttu-id="36e9c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36e9c-102">SYNOPSIS</span></span>
<span data-ttu-id="36e9c-103">Удаляет базу данных с заданным именем.</span><span class="sxs-lookup"><span data-stu-id="36e9c-103">Deletes the database with the given name.</span></span>

## <span data-ttu-id="36e9c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="36e9c-104">SYNTAX</span></span>

### <span data-ttu-id="36e9c-105">Delete (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="36e9c-105">Delete (Default)</span></span>
```
Remove-AzKustoDatabase -ClusterName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="36e9c-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="36e9c-106">DeleteViaIdentity</span></span>
```
Remove-AzKustoDatabase -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="36e9c-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="36e9c-107">DESCRIPTION</span></span>
<span data-ttu-id="36e9c-108">Удаляет базу данных с заданным именем.</span><span class="sxs-lookup"><span data-stu-id="36e9c-108">Deletes the database with the given name.</span></span>

## <span data-ttu-id="36e9c-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="36e9c-109">EXAMPLES</span></span>

### <span data-ttu-id="36e9c-110">Пример 1. Удаление базы данных "Кузто" по имени</span><span class="sxs-lookup"><span data-stu-id="36e9c-110">Example 1: Delete an existing Kusto database by name</span></span>
```powershell
PS C:\> Remove-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase
```

<span data-ttu-id="36e9c-111">При этом база данных "Кузто" с именем "mykustodatabase" в кластере testnewkustocluster, найденная в группе ресурсов testrg.</span><span class="sxs-lookup"><span data-stu-id="36e9c-111">The above command deletes the Kusto database named "mykustodatabase" in the cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

## <span data-ttu-id="36e9c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="36e9c-112">PARAMETERS</span></span>

### <span data-ttu-id="36e9c-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="36e9c-113">-AsJob</span></span>
<span data-ttu-id="36e9c-114">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="36e9c-114">Run the command as a job</span></span>

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

### <span data-ttu-id="36e9c-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="36e9c-115">-ClusterName</span></span>
<span data-ttu-id="36e9c-116">Название кластера "Кусто".</span><span class="sxs-lookup"><span data-stu-id="36e9c-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="36e9c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36e9c-117">-DefaultProfile</span></span>
<span data-ttu-id="36e9c-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="36e9c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36e9c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="36e9c-119">-InputObject</span></span>
<span data-ttu-id="36e9c-120">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="36e9c-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="36e9c-121">-Name</span><span class="sxs-lookup"><span data-stu-id="36e9c-121">-Name</span></span>
<span data-ttu-id="36e9c-122">Имя базы данных в кластере Кусто.</span><span class="sxs-lookup"><span data-stu-id="36e9c-122">The name of the database in the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: DatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36e9c-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="36e9c-123">-NoWait</span></span>
<span data-ttu-id="36e9c-124">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="36e9c-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="36e9c-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="36e9c-125">-PassThru</span></span>
<span data-ttu-id="36e9c-126">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="36e9c-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="36e9c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36e9c-127">-ResourceGroupName</span></span>
<span data-ttu-id="36e9c-128">Имя группы ресурсов, содержащей кластер Кусто.</span><span class="sxs-lookup"><span data-stu-id="36e9c-128">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="36e9c-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="36e9c-129">-SubscriptionId</span></span>
<span data-ttu-id="36e9c-130">Получает учетные данные подписки, которые однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="36e9c-130">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="36e9c-131">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="36e9c-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="36e9c-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="36e9c-132">-Confirm</span></span>
<span data-ttu-id="36e9c-133">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="36e9c-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36e9c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36e9c-134">-WhatIf</span></span>
<span data-ttu-id="36e9c-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="36e9c-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36e9c-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="36e9c-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36e9c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36e9c-137">CommonParameters</span></span>
<span data-ttu-id="36e9c-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36e9c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36e9c-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="36e9c-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36e9c-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="36e9c-140">INPUTS</span></span>

### <span data-ttu-id="36e9c-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="36e9c-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="36e9c-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="36e9c-142">OUTPUTS</span></span>

### <span data-ttu-id="36e9c-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="36e9c-143">System.Boolean</span></span>

## <span data-ttu-id="36e9c-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="36e9c-144">NOTES</span></span>

<span data-ttu-id="36e9c-145">ALIASES</span><span class="sxs-lookup"><span data-stu-id="36e9c-145">ALIASES</span></span>

<span data-ttu-id="36e9c-146">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="36e9c-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="36e9c-147">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="36e9c-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="36e9c-148">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="36e9c-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="36e9c-149">INPUTOBJECT <IKustoIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="36e9c-149">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="36e9c-150">`[AttachedDatabaseConfigurationName <String>]`: имя конфигурации вложенной базы данных.</span><span class="sxs-lookup"><span data-stu-id="36e9c-150">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="36e9c-151">`[ClusterName <String>]`Название кластера "Кусто".</span><span class="sxs-lookup"><span data-stu-id="36e9c-151">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="36e9c-152">`[DataConnectionName <String>]`: имя подключения к данным.</span><span class="sxs-lookup"><span data-stu-id="36e9c-152">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="36e9c-153">`[DatabaseName <String>]`Имя базы данных в кластере Кусто.</span><span class="sxs-lookup"><span data-stu-id="36e9c-153">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="36e9c-154">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="36e9c-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="36e9c-155">`[Location <String>]`: расположение в Azure.</span><span class="sxs-lookup"><span data-stu-id="36e9c-155">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="36e9c-156">`[PrincipalAssignmentName <String>]`: Имя «Кусто principalAssignment».</span><span class="sxs-lookup"><span data-stu-id="36e9c-156">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="36e9c-157">`[ResourceGroupName <String>]`Название группы ресурсов, содержащей кластер Кусто.</span><span class="sxs-lookup"><span data-stu-id="36e9c-157">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="36e9c-158">`[SubscriptionId <String>]`: получает учетные данные подписки, которые однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="36e9c-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="36e9c-159">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="36e9c-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="36e9c-160">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="36e9c-160">RELATED LINKS</span></span>

