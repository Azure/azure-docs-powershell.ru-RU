---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/remove-azkustoattacheddatabaseconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoAttachedDatabaseConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoAttachedDatabaseConfiguration.md
ms.openlocfilehash: 065cb2177eec7bd94439d52f3a4157d9ef043779
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995473"
---
# <span data-ttu-id="245f2-101">Remove-AzKustoAttachedDatabaseConfiguration</span><span class="sxs-lookup"><span data-stu-id="245f2-101">Remove-AzKustoAttachedDatabaseConfiguration</span></span>

## <span data-ttu-id="245f2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="245f2-102">SYNOPSIS</span></span>
<span data-ttu-id="245f2-103">Удаляет конфигурацию вложенной базы данных с заданным именем.</span><span class="sxs-lookup"><span data-stu-id="245f2-103">Deletes the attached database configuration with the given name.</span></span>

## <span data-ttu-id="245f2-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="245f2-104">SYNTAX</span></span>

### <span data-ttu-id="245f2-105">Delete (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="245f2-105">Delete (Default)</span></span>
```
Remove-AzKustoAttachedDatabaseConfiguration -ClusterName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="245f2-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="245f2-106">DeleteViaIdentity</span></span>
```
Remove-AzKustoAttachedDatabaseConfiguration -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="245f2-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="245f2-107">DESCRIPTION</span></span>
<span data-ttu-id="245f2-108">Удаляет конфигурацию вложенной базы данных с заданным именем.</span><span class="sxs-lookup"><span data-stu-id="245f2-108">Deletes the attached database configuration with the given name.</span></span>

## <span data-ttu-id="245f2-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="245f2-109">EXAMPLES</span></span>

### <span data-ttu-id="245f2-110">Пример 1. Удаление существующей структуры AttachedDatabaseConfiguration по имени</span><span class="sxs-lookup"><span data-stu-id="245f2-110">Example 1: Delete an existing AttachedDatabaseConfiguration by name</span></span>
```powershell
PS C:\> Remove-AzKustoAttachedDatabaseConfiguration -ResourceGroupName "testrg" -ClusterName "testnewkustoclusterf" -Name "myfollowerconfiguration"
```

<span data-ttu-id="245f2-111">При наложении этой команды удаляется база данных, заданная в AttachedDatabaseConfiguration "myfollowerconfiguration" из кластера "testnewkustoclusterf".</span><span class="sxs-lookup"><span data-stu-id="245f2-111">The above command deletes the follower database defined in the AttachedDatabaseConfiguration "myfollowerconfiguration" from cluster "testnewkustoclusterf".</span></span>

## <span data-ttu-id="245f2-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="245f2-112">PARAMETERS</span></span>

### <span data-ttu-id="245f2-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="245f2-113">-AsJob</span></span>
<span data-ttu-id="245f2-114">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="245f2-114">Run the command as a job</span></span>

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

### <span data-ttu-id="245f2-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="245f2-115">-ClusterName</span></span>
<span data-ttu-id="245f2-116">Название кластера Кусто.</span><span class="sxs-lookup"><span data-stu-id="245f2-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="245f2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="245f2-117">-DefaultProfile</span></span>
<span data-ttu-id="245f2-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="245f2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="245f2-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="245f2-119">-InputObject</span></span>
<span data-ttu-id="245f2-120">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="245f2-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="245f2-121">-Name</span><span class="sxs-lookup"><span data-stu-id="245f2-121">-Name</span></span>
<span data-ttu-id="245f2-122">Имя конфигурации вложенной базы данных.</span><span class="sxs-lookup"><span data-stu-id="245f2-122">The name of the attached database configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: AttachedDatabaseConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="245f2-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="245f2-123">-NoWait</span></span>
<span data-ttu-id="245f2-124">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="245f2-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="245f2-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="245f2-125">-PassThru</span></span>
<span data-ttu-id="245f2-126">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="245f2-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="245f2-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="245f2-127">-ResourceGroupName</span></span>
<span data-ttu-id="245f2-128">Имя группы ресурсов, содержащей кластер Кусто.</span><span class="sxs-lookup"><span data-stu-id="245f2-128">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="245f2-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="245f2-129">-SubscriptionId</span></span>
<span data-ttu-id="245f2-130">Получает учетные данные подписки, которые однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="245f2-130">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="245f2-131">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="245f2-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="245f2-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="245f2-132">-Confirm</span></span>
<span data-ttu-id="245f2-133">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="245f2-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="245f2-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="245f2-134">-WhatIf</span></span>
<span data-ttu-id="245f2-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="245f2-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="245f2-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="245f2-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="245f2-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="245f2-137">CommonParameters</span></span>
<span data-ttu-id="245f2-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="245f2-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="245f2-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="245f2-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="245f2-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="245f2-140">INPUTS</span></span>

### <span data-ttu-id="245f2-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="245f2-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="245f2-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="245f2-142">OUTPUTS</span></span>

### <span data-ttu-id="245f2-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="245f2-143">System.Boolean</span></span>

## <span data-ttu-id="245f2-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="245f2-144">NOTES</span></span>

<span data-ttu-id="245f2-145">ALIASES</span><span class="sxs-lookup"><span data-stu-id="245f2-145">ALIASES</span></span>

<span data-ttu-id="245f2-146">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="245f2-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="245f2-147">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="245f2-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="245f2-148">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="245f2-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="245f2-149">INPUTOBJECT <IKustoIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="245f2-149">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="245f2-150">`[AttachedDatabaseConfigurationName <String>]`: имя конфигурации вложенной базы данных.</span><span class="sxs-lookup"><span data-stu-id="245f2-150">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="245f2-151">`[ClusterName <String>]`Название кластера "Кусто".</span><span class="sxs-lookup"><span data-stu-id="245f2-151">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="245f2-152">`[DataConnectionName <String>]`: имя подключения к данным.</span><span class="sxs-lookup"><span data-stu-id="245f2-152">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="245f2-153">`[DatabaseName <String>]`Имя базы данных в кластере Кусто.</span><span class="sxs-lookup"><span data-stu-id="245f2-153">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="245f2-154">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="245f2-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="245f2-155">`[Location <String>]`: расположение в Azure.</span><span class="sxs-lookup"><span data-stu-id="245f2-155">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="245f2-156">`[PrincipalAssignmentName <String>]`: Имя «Кусто principalAssignment».</span><span class="sxs-lookup"><span data-stu-id="245f2-156">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="245f2-157">`[ResourceGroupName <String>]`Название группы ресурсов, содержащей кластер Кусто.</span><span class="sxs-lookup"><span data-stu-id="245f2-157">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="245f2-158">`[SubscriptionId <String>]`. Получает учетные данные подписки, которые однозначно определяют подписку microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="245f2-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="245f2-159">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="245f2-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="245f2-160">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="245f2-160">RELATED LINKS</span></span>

