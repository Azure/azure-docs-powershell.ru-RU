---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/invoke-azkustodiagnoseclustervirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDiagnoseClusterVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDiagnoseClusterVirtualNetwork.md
ms.openlocfilehash: 682de416a4aba61e1f287661c88faee9e20d248c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248999"
---
# <span data-ttu-id="7dd92-101">Invoke-AzKustoDiagnoseClusterVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7dd92-101">Invoke-AzKustoDiagnoseClusterVirtualNetwork</span></span>

## <span data-ttu-id="7dd92-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7dd92-102">SYNOPSIS</span></span>
<span data-ttu-id="7dd92-103">Диагностика состояния сетевого подключения для внешних ресурсов, от которых зависит служба.</span><span class="sxs-lookup"><span data-stu-id="7dd92-103">Diagnoses network connectivity status for external resources on which the service is dependent on.</span></span>

## <span data-ttu-id="7dd92-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7dd92-104">SYNTAX</span></span>

### <span data-ttu-id="7dd92-105">Диагностика (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7dd92-105">Diagnose (Default)</span></span>
```
Invoke-AzKustoDiagnoseClusterVirtualNetwork -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="7dd92-106">DiagnoseViaIdentity</span><span class="sxs-lookup"><span data-stu-id="7dd92-106">DiagnoseViaIdentity</span></span>
```
Invoke-AzKustoDiagnoseClusterVirtualNetwork -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7dd92-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7dd92-107">DESCRIPTION</span></span>
<span data-ttu-id="7dd92-108">Диагностика состояния сетевого подключения для внешних ресурсов, от которых зависит служба.</span><span class="sxs-lookup"><span data-stu-id="7dd92-108">Diagnoses network connectivity status for external resources on which the service is dependent on.</span></span>

## <span data-ttu-id="7dd92-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7dd92-109">EXAMPLES</span></span>

### <span data-ttu-id="7dd92-110">Пример 1: Отображение диагностики сетевого подключения для внешних ресурсов</span><span class="sxs-lookup"><span data-stu-id="7dd92-110">Example 1: Show network connectivity diagnosis for external resources</span></span> 
```powershell
PS C:\> Invoke-AzKustoDiagnoseClusterVirtualNetwork -ResourceGroupName "testrg" -ClusterName "testnewkustocluster"

```

<span data-ttu-id="7dd92-111">В приведенной выше команде выполняется диагностика состояния сетевого подключения для внешних ресурсов, от которых зависит кластер "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="7dd92-111">The above command diagnoses network connectivity status for external resources on which the cluster "testnewkustocluster" is dependent on</span></span>

## <span data-ttu-id="7dd92-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7dd92-112">PARAMETERS</span></span>

### <span data-ttu-id="7dd92-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7dd92-113">-AsJob</span></span>
<span data-ttu-id="7dd92-114">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="7dd92-114">Run the command as a job</span></span>

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

### <span data-ttu-id="7dd92-115">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="7dd92-115">-ClusterName</span></span>
<span data-ttu-id="7dd92-116">Имя кластера Kusto.</span><span class="sxs-lookup"><span data-stu-id="7dd92-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="7dd92-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7dd92-117">-DefaultProfile</span></span>
<span data-ttu-id="7dd92-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7dd92-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7dd92-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7dd92-119">-InputObject</span></span>
<span data-ttu-id="7dd92-120">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="7dd92-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="7dd92-121">-Wait</span><span class="sxs-lookup"><span data-stu-id="7dd92-121">-NoWait</span></span>
<span data-ttu-id="7dd92-122">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="7dd92-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="7dd92-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7dd92-123">-ResourceGroupName</span></span>
<span data-ttu-id="7dd92-124">Имя группы ресурсов, содержащей кластер Kusto.</span><span class="sxs-lookup"><span data-stu-id="7dd92-124">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="7dd92-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7dd92-125">-SubscriptionId</span></span>
<span data-ttu-id="7dd92-126">Получение учетных данных подписки, однозначно идентифицирующей подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="7dd92-126">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="7dd92-127">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="7dd92-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="7dd92-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7dd92-128">-Confirm</span></span>
<span data-ttu-id="7dd92-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7dd92-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7dd92-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7dd92-130">-WhatIf</span></span>
<span data-ttu-id="7dd92-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7dd92-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7dd92-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7dd92-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7dd92-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7dd92-133">CommonParameters</span></span>
<span data-ttu-id="7dd92-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7dd92-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7dd92-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7dd92-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7dd92-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7dd92-136">INPUTS</span></span>

### <span data-ttu-id="7dd92-137">Microsoft. Azure. PowerShell. командлеты. Kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="7dd92-137">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="7dd92-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7dd92-138">OUTPUTS</span></span>

### <span data-ttu-id="7dd92-139">System. String</span><span class="sxs-lookup"><span data-stu-id="7dd92-139">System.String</span></span>

## <span data-ttu-id="7dd92-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="7dd92-140">NOTES</span></span>

<span data-ttu-id="7dd92-141">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="7dd92-141">ALIASES</span></span>

<span data-ttu-id="7dd92-142">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="7dd92-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7dd92-143">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="7dd92-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7dd92-144">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7dd92-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7dd92-145">INPUTOBJECT <IKustoIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="7dd92-145">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7dd92-146">`[AttachedDatabaseConfigurationName <String>]`: Имя конфигурации присоединенной базы данных.</span><span class="sxs-lookup"><span data-stu-id="7dd92-146">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="7dd92-147">`[ClusterName <String>]`: Имя кластера Kusto.</span><span class="sxs-lookup"><span data-stu-id="7dd92-147">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="7dd92-148">`[DataConnectionName <String>]`: Имя подключения к данным.</span><span class="sxs-lookup"><span data-stu-id="7dd92-148">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="7dd92-149">`[DatabaseName <String>]`: Имя базы данных в кластере Kusto.</span><span class="sxs-lookup"><span data-stu-id="7dd92-149">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="7dd92-150">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="7dd92-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7dd92-151">`[Location <String>]`: Расположение Azure.</span><span class="sxs-lookup"><span data-stu-id="7dd92-151">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="7dd92-152">`[PrincipalAssignmentName <String>]`: Имя Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="7dd92-152">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="7dd92-153">`[ResourceGroupName <String>]`: Имя группы ресурсов, содержащей кластер Kusto.</span><span class="sxs-lookup"><span data-stu-id="7dd92-153">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="7dd92-154">`[SubscriptionId <String>]`: Получение учетных данных подписки, которые уникально определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="7dd92-154">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="7dd92-155">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="7dd92-155">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="7dd92-156">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7dd92-156">RELATED LINKS</span></span>

