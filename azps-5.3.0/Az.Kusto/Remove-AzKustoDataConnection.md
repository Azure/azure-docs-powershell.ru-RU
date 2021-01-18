---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/remove-azkustodataconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDataConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDataConnection.md
ms.openlocfilehash: c04cbc2a92e6fa80c718cb32d95cc4059e4e3a6d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98508306"
---
# <span data-ttu-id="14561-101">Remove-AzKustoDataConnection</span><span class="sxs-lookup"><span data-stu-id="14561-101">Remove-AzKustoDataConnection</span></span>

## <span data-ttu-id="14561-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14561-102">SYNOPSIS</span></span>
<span data-ttu-id="14561-103">Удаляет подключение к данным с заданным именем.</span><span class="sxs-lookup"><span data-stu-id="14561-103">Deletes the data connection with the given name.</span></span>

## <span data-ttu-id="14561-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="14561-104">SYNTAX</span></span>

### <span data-ttu-id="14561-105">Delete (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="14561-105">Delete (Default)</span></span>
```
Remove-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="14561-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="14561-106">DeleteViaIdentity</span></span>
```
Remove-AzKustoDataConnection -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="14561-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="14561-107">DESCRIPTION</span></span>
<span data-ttu-id="14561-108">Удаляет подключение к данным с заданным именем.</span><span class="sxs-lookup"><span data-stu-id="14561-108">Deletes the data connection with the given name.</span></span>

## <span data-ttu-id="14561-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="14561-109">EXAMPLES</span></span>

### <span data-ttu-id="14561-110">Пример 1. Удаление существующего подключения к данным по имени</span><span class="sxs-lookup"><span data-stu-id="14561-110">Example 1: Delete an existing data connection by name</span></span>
```powershell
PS C:\> Remove-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "mykustodataconnection"
```

<span data-ttu-id="14561-111">Команда выше удаляет подключение к данным с именем "mykustodataconnection" в базе данных "mykustodatabase" существующего кластера testnewkustocluster, найденное в группе ресурсов testrg</span><span class="sxs-lookup"><span data-stu-id="14561-111">The above command deletes the data connection named "mykustodataconnection" in database "mykustodatabase" of the existing cluster "testnewkustocluster" found in the resource group "testrg"</span></span>

## <span data-ttu-id="14561-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="14561-112">PARAMETERS</span></span>

### <span data-ttu-id="14561-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="14561-113">-AsJob</span></span>
<span data-ttu-id="14561-114">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="14561-114">Run the command as a job</span></span>

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

### <span data-ttu-id="14561-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="14561-115">-ClusterName</span></span>
<span data-ttu-id="14561-116">Название кластера "Кусто".</span><span class="sxs-lookup"><span data-stu-id="14561-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="14561-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="14561-117">-DatabaseName</span></span>
<span data-ttu-id="14561-118">Имя базы данных в кластере Кусто.</span><span class="sxs-lookup"><span data-stu-id="14561-118">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="14561-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14561-119">-DefaultProfile</span></span>
<span data-ttu-id="14561-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="14561-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14561-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="14561-121">-InputObject</span></span>
<span data-ttu-id="14561-122">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="14561-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="14561-123">-Name</span><span class="sxs-lookup"><span data-stu-id="14561-123">-Name</span></span>
<span data-ttu-id="14561-124">Имя подключения к данным.</span><span class="sxs-lookup"><span data-stu-id="14561-124">The name of the data connection.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: DataConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14561-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="14561-125">-NoWait</span></span>
<span data-ttu-id="14561-126">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="14561-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="14561-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="14561-127">-PassThru</span></span>
<span data-ttu-id="14561-128">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="14561-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="14561-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14561-129">-ResourceGroupName</span></span>
<span data-ttu-id="14561-130">Имя группы ресурсов, содержащей кластер Кусто.</span><span class="sxs-lookup"><span data-stu-id="14561-130">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="14561-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="14561-131">-SubscriptionId</span></span>
<span data-ttu-id="14561-132">Получает учетные данные подписки, которые однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="14561-132">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="14561-133">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="14561-133">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="14561-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="14561-134">-Confirm</span></span>
<span data-ttu-id="14561-135">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="14561-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14561-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14561-136">-WhatIf</span></span>
<span data-ttu-id="14561-137">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="14561-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14561-138">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="14561-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14561-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14561-139">CommonParameters</span></span>
<span data-ttu-id="14561-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14561-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14561-141">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="14561-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14561-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="14561-142">INPUTS</span></span>

### <span data-ttu-id="14561-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="14561-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="14561-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="14561-144">OUTPUTS</span></span>

### <span data-ttu-id="14561-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="14561-145">System.Boolean</span></span>

## <span data-ttu-id="14561-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="14561-146">NOTES</span></span>

<span data-ttu-id="14561-147">ALIASES</span><span class="sxs-lookup"><span data-stu-id="14561-147">ALIASES</span></span>

<span data-ttu-id="14561-148">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="14561-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="14561-149">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="14561-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="14561-150">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="14561-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="14561-151">INPUTOBJECT <IKustoIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="14561-151">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="14561-152">`[AttachedDatabaseConfigurationName <String>]`: имя конфигурации вложенной базы данных.</span><span class="sxs-lookup"><span data-stu-id="14561-152">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="14561-153">`[ClusterName <String>]`Название кластера "Кусто".</span><span class="sxs-lookup"><span data-stu-id="14561-153">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="14561-154">`[DataConnectionName <String>]`: имя подключения к данным.</span><span class="sxs-lookup"><span data-stu-id="14561-154">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="14561-155">`[DatabaseName <String>]`Имя базы данных в кластере Кусто.</span><span class="sxs-lookup"><span data-stu-id="14561-155">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="14561-156">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="14561-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="14561-157">`[Location <String>]`: расположение в Azure.</span><span class="sxs-lookup"><span data-stu-id="14561-157">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="14561-158">`[PrincipalAssignmentName <String>]`: Имя «Кусто principalAssignment».</span><span class="sxs-lookup"><span data-stu-id="14561-158">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="14561-159">`[ResourceGroupName <String>]`Название группы ресурсов, содержащей кластер Кусто.</span><span class="sxs-lookup"><span data-stu-id="14561-159">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="14561-160">`[SubscriptionId <String>]`: получает учетные данные подписки, которые однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="14561-160">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="14561-161">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="14561-161">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="14561-162">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="14561-162">RELATED LINKS</span></span>

