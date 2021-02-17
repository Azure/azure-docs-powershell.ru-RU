---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/invoke-azkustodiagnoseclustervirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDiagnoseClusterVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDiagnoseClusterVirtualNetwork.md
ms.openlocfilehash: 682de416a4aba61e1f287661c88faee9e20d248c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100243333"
---
# <span data-ttu-id="d6607-101">Invoke-AzKustoDiagnoseClusterVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="d6607-101">Invoke-AzKustoDiagnoseClusterVirtualNetwork</span></span>

## <span data-ttu-id="d6607-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d6607-102">SYNOPSIS</span></span>
<span data-ttu-id="d6607-103">Диагностирует состояние сетевого подключения для внешних ресурсов, от которых зависит служба.</span><span class="sxs-lookup"><span data-stu-id="d6607-103">Diagnoses network connectivity status for external resources on which the service is dependent on.</span></span>

## <span data-ttu-id="d6607-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d6607-104">SYNTAX</span></span>

### <span data-ttu-id="d6607-105">Диагностика (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d6607-105">Diagnose (Default)</span></span>
```
Invoke-AzKustoDiagnoseClusterVirtualNetwork -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="d6607-106">DiagnoseViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d6607-106">DiagnoseViaIdentity</span></span>
```
Invoke-AzKustoDiagnoseClusterVirtualNetwork -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d6607-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d6607-107">DESCRIPTION</span></span>
<span data-ttu-id="d6607-108">Диагностирует состояние сетевого подключения для внешних ресурсов, от которых зависит служба.</span><span class="sxs-lookup"><span data-stu-id="d6607-108">Diagnoses network connectivity status for external resources on which the service is dependent on.</span></span>

## <span data-ttu-id="d6607-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d6607-109">EXAMPLES</span></span>

### <span data-ttu-id="d6607-110">Пример 1. Демонстрация диагностики сетевого подключения для внешних ресурсов</span><span class="sxs-lookup"><span data-stu-id="d6607-110">Example 1: Show network connectivity diagnosis for external resources</span></span> 
```powershell
PS C:\> Invoke-AzKustoDiagnoseClusterVirtualNetwork -ResourceGroupName "testrg" -ClusterName "testnewkustocluster"

```

<span data-ttu-id="d6607-111">Вышеупомяненная команда диагностирует состояние сетевого подключения для внешних ресурсов, от которых зависит кластер "testnewkustocluster"</span><span class="sxs-lookup"><span data-stu-id="d6607-111">The above command diagnoses network connectivity status for external resources on which the cluster "testnewkustocluster" is dependent on</span></span>

## <span data-ttu-id="d6607-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d6607-112">PARAMETERS</span></span>

### <span data-ttu-id="d6607-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d6607-113">-AsJob</span></span>
<span data-ttu-id="d6607-114">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="d6607-114">Run the command as a job</span></span>

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

### <span data-ttu-id="d6607-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="d6607-115">-ClusterName</span></span>
<span data-ttu-id="d6607-116">Название кластера Кусто.</span><span class="sxs-lookup"><span data-stu-id="d6607-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="d6607-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6607-117">-DefaultProfile</span></span>
<span data-ttu-id="d6607-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d6607-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6607-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d6607-119">-InputObject</span></span>
<span data-ttu-id="d6607-120">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="d6607-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d6607-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="d6607-121">-NoWait</span></span>
<span data-ttu-id="d6607-122">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="d6607-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="d6607-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6607-123">-ResourceGroupName</span></span>
<span data-ttu-id="d6607-124">Имя группы ресурсов, содержащей кластер Кусто.</span><span class="sxs-lookup"><span data-stu-id="d6607-124">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="d6607-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d6607-125">-SubscriptionId</span></span>
<span data-ttu-id="d6607-126">Получает учетные данные подписки, которые однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d6607-126">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="d6607-127">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="d6607-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="d6607-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d6607-128">-Confirm</span></span>
<span data-ttu-id="d6607-129">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="d6607-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6607-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6607-130">-WhatIf</span></span>
<span data-ttu-id="d6607-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d6607-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6607-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="d6607-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6607-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6607-133">CommonParameters</span></span>
<span data-ttu-id="d6607-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6607-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6607-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d6607-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6607-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d6607-136">INPUTS</span></span>

### <span data-ttu-id="d6607-137">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="d6607-137">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="d6607-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d6607-138">OUTPUTS</span></span>

### <span data-ttu-id="d6607-139">System.String</span><span class="sxs-lookup"><span data-stu-id="d6607-139">System.String</span></span>

## <span data-ttu-id="d6607-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d6607-140">NOTES</span></span>

<span data-ttu-id="d6607-141">ALIASES</span><span class="sxs-lookup"><span data-stu-id="d6607-141">ALIASES</span></span>

<span data-ttu-id="d6607-142">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="d6607-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d6607-143">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="d6607-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d6607-144">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d6607-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d6607-145">INPUTOBJECT <IKustoIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="d6607-145">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d6607-146">`[AttachedDatabaseConfigurationName <String>]`: имя конфигурации вложенной базы данных.</span><span class="sxs-lookup"><span data-stu-id="d6607-146">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="d6607-147">`[ClusterName <String>]`Название кластера "Кусто".</span><span class="sxs-lookup"><span data-stu-id="d6607-147">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="d6607-148">`[DataConnectionName <String>]`: имя подключения к данным.</span><span class="sxs-lookup"><span data-stu-id="d6607-148">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="d6607-149">`[DatabaseName <String>]`Имя базы данных в кластере Кусто.</span><span class="sxs-lookup"><span data-stu-id="d6607-149">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="d6607-150">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="d6607-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d6607-151">`[Location <String>]`: расположение в Azure.</span><span class="sxs-lookup"><span data-stu-id="d6607-151">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="d6607-152">`[PrincipalAssignmentName <String>]`: Имя «Кусто principalAssignment».</span><span class="sxs-lookup"><span data-stu-id="d6607-152">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="d6607-153">`[ResourceGroupName <String>]`Название группы ресурсов, содержащей кластер Кусто.</span><span class="sxs-lookup"><span data-stu-id="d6607-153">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="d6607-154">`[SubscriptionId <String>]`: получает учетные данные подписки, которые однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d6607-154">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="d6607-155">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="d6607-155">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="d6607-156">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d6607-156">RELATED LINKS</span></span>

