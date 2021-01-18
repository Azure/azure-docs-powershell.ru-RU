---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/invoke-azkustodiagnoseclustervirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDiagnoseClusterVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDiagnoseClusterVirtualNetwork.md
ms.openlocfilehash: 682de416a4aba61e1f287661c88faee9e20d248c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98518322"
---
# <span data-ttu-id="db920-101">Invoke-AzKustoDiagnoseClusterVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="db920-101">Invoke-AzKustoDiagnoseClusterVirtualNetwork</span></span>

## <span data-ttu-id="db920-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="db920-102">SYNOPSIS</span></span>
<span data-ttu-id="db920-103">Диагностирует состояние сетевого подключения для внешних ресурсов, от которых зависит служба.</span><span class="sxs-lookup"><span data-stu-id="db920-103">Diagnoses network connectivity status for external resources on which the service is dependent on.</span></span>

## <span data-ttu-id="db920-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="db920-104">SYNTAX</span></span>

### <span data-ttu-id="db920-105">Диагностика (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="db920-105">Diagnose (Default)</span></span>
```
Invoke-AzKustoDiagnoseClusterVirtualNetwork -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="db920-106">DiagnoseViaIdentity</span><span class="sxs-lookup"><span data-stu-id="db920-106">DiagnoseViaIdentity</span></span>
```
Invoke-AzKustoDiagnoseClusterVirtualNetwork -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="db920-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="db920-107">DESCRIPTION</span></span>
<span data-ttu-id="db920-108">Диагностирует состояние сетевого подключения для внешних ресурсов, от которых зависит служба.</span><span class="sxs-lookup"><span data-stu-id="db920-108">Diagnoses network connectivity status for external resources on which the service is dependent on.</span></span>

## <span data-ttu-id="db920-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="db920-109">EXAMPLES</span></span>

### <span data-ttu-id="db920-110">Пример 1. Демонстрация диагностики сетевого подключения для внешних ресурсов</span><span class="sxs-lookup"><span data-stu-id="db920-110">Example 1: Show network connectivity diagnosis for external resources</span></span> 
```powershell
PS C:\> Invoke-AzKustoDiagnoseClusterVirtualNetwork -ResourceGroupName "testrg" -ClusterName "testnewkustocluster"

```

<span data-ttu-id="db920-111">Команда выше диагностирует состояние сетевого подключения для внешних ресурсов, от которых зависит кластер testnewkustocluster.</span><span class="sxs-lookup"><span data-stu-id="db920-111">The above command diagnoses network connectivity status for external resources on which the cluster "testnewkustocluster" is dependent on</span></span>

## <span data-ttu-id="db920-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="db920-112">PARAMETERS</span></span>

### <span data-ttu-id="db920-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="db920-113">-AsJob</span></span>
<span data-ttu-id="db920-114">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="db920-114">Run the command as a job</span></span>

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

### <span data-ttu-id="db920-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="db920-115">-ClusterName</span></span>
<span data-ttu-id="db920-116">Название кластера Кусто.</span><span class="sxs-lookup"><span data-stu-id="db920-116">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Diagnose
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db920-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db920-117">-DefaultProfile</span></span>
<span data-ttu-id="db920-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="db920-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db920-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="db920-119">-InputObject</span></span>
<span data-ttu-id="db920-120">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="db920-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: DiagnoseViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="db920-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="db920-121">-NoWait</span></span>
<span data-ttu-id="db920-122">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="db920-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="db920-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db920-123">-ResourceGroupName</span></span>
<span data-ttu-id="db920-124">Имя группы ресурсов, содержащей кластер Кусто.</span><span class="sxs-lookup"><span data-stu-id="db920-124">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Diagnose
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db920-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="db920-125">-SubscriptionId</span></span>
<span data-ttu-id="db920-126">Получает учетные данные подписки, которые однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="db920-126">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="db920-127">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="db920-127">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Diagnose
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db920-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="db920-128">-Confirm</span></span>
<span data-ttu-id="db920-129">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="db920-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db920-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db920-130">-WhatIf</span></span>
<span data-ttu-id="db920-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="db920-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db920-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="db920-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db920-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db920-133">CommonParameters</span></span>
<span data-ttu-id="db920-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db920-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db920-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="db920-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db920-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="db920-136">INPUTS</span></span>

### <span data-ttu-id="db920-137">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="db920-137">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="db920-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="db920-138">OUTPUTS</span></span>

### <span data-ttu-id="db920-139">System.String</span><span class="sxs-lookup"><span data-stu-id="db920-139">System.String</span></span>

## <span data-ttu-id="db920-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="db920-140">NOTES</span></span>

<span data-ttu-id="db920-141">ALIASES</span><span class="sxs-lookup"><span data-stu-id="db920-141">ALIASES</span></span>

<span data-ttu-id="db920-142">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="db920-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="db920-143">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="db920-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="db920-144">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="db920-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="db920-145">INPUTOBJECT <IKustoIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="db920-145">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="db920-146">`[AttachedDatabaseConfigurationName <String>]`: имя конфигурации вложенной базы данных.</span><span class="sxs-lookup"><span data-stu-id="db920-146">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="db920-147">`[ClusterName <String>]`Название кластера "Кусто".</span><span class="sxs-lookup"><span data-stu-id="db920-147">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="db920-148">`[DataConnectionName <String>]`: имя подключения к данным.</span><span class="sxs-lookup"><span data-stu-id="db920-148">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="db920-149">`[DatabaseName <String>]`Имя базы данных в кластере Кусто.</span><span class="sxs-lookup"><span data-stu-id="db920-149">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="db920-150">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="db920-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="db920-151">`[Location <String>]`: расположение в Azure.</span><span class="sxs-lookup"><span data-stu-id="db920-151">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="db920-152">`[PrincipalAssignmentName <String>]`: Имя «Кусто principalAssignment».</span><span class="sxs-lookup"><span data-stu-id="db920-152">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="db920-153">`[ResourceGroupName <String>]`Название группы ресурсов, содержащей кластер Кусто.</span><span class="sxs-lookup"><span data-stu-id="db920-153">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="db920-154">`[SubscriptionId <String>]`. Получает учетные данные подписки, которые однозначно определяют подписку microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="db920-154">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="db920-155">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="db920-155">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="db920-156">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="db920-156">RELATED LINKS</span></span>

