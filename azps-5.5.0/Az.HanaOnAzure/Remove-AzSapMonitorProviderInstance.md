---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/en-us/powershell/module/az.hanaonazure/remove-azsapmonitorproviderinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Remove-AzSapMonitorProviderInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Remove-AzSapMonitorProviderInstance.md
ms.openlocfilehash: 53f251b001b4e2f6319840079e9db3111c00b006
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100219865"
---
# <span data-ttu-id="90a24-101">Remove-AzSapMonitorProviderInstance</span><span class="sxs-lookup"><span data-stu-id="90a24-101">Remove-AzSapMonitorProviderInstance</span></span>

## <span data-ttu-id="90a24-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="90a24-102">SYNOPSIS</span></span>
<span data-ttu-id="90a24-103">Удаляет экземпляр поставщика для указанной подписки, группы ресурсов, имени sapMonitor и имени ресурса.</span><span class="sxs-lookup"><span data-stu-id="90a24-103">Deletes a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="90a24-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="90a24-104">SYNTAX</span></span>

### <span data-ttu-id="90a24-105">Delete (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="90a24-105">Delete (Default)</span></span>
```
Remove-AzSapMonitorProviderInstance -Name <String> -ResourceGroupName <String> -SapMonitorName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="90a24-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="90a24-106">DeleteViaIdentity</span></span>
```
Remove-AzSapMonitorProviderInstance -InputObject <IHanaOnAzureIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="90a24-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="90a24-107">DESCRIPTION</span></span>
<span data-ttu-id="90a24-108">Удаляет экземпляр поставщика для указанной подписки, группы ресурсов, имени SapMonitor и имени ресурса.</span><span class="sxs-lookup"><span data-stu-id="90a24-108">Deletes a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="90a24-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="90a24-109">EXAMPLES</span></span>

### <span data-ttu-id="90a24-110">Пример 1. Удаление экземпляра монитора SAP по имени</span><span class="sxs-lookup"><span data-stu-id="90a24-110">Example 1: Remove instance of SAP monitor by name</span></span>
```powershell
PS C:\> Remove-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -SapMonitorName ps-spamonitor-t01 -Name ps-sapmonitorins-t02

```

<span data-ttu-id="90a24-111">Эта команда удаляет экземпляр монитора SAP по имени.</span><span class="sxs-lookup"><span data-stu-id="90a24-111">This command removes instance of SAP monitor by name.</span></span>

### <span data-ttu-id="90a24-112">Пример 2. Удаление экземпляра монитора SAP для объекта</span><span class="sxs-lookup"><span data-stu-id="90a24-112">Example 2: Remove instance of SAP monitor by object</span></span>
```powershell
PS C:\> $sapIns = Get-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -SapMonitorName ps-spamonitor-t01 -Name ps-sapmonitorins-t01
PS C:\> Remove-AzSapMonitorProviderInstance -InputObject $sapIns

```

<span data-ttu-id="90a24-113">Эта команда удаляет экземпляр монитора SAP для объекта.</span><span class="sxs-lookup"><span data-stu-id="90a24-113">This command removes instance of SAP monitor by object.</span></span>

## <span data-ttu-id="90a24-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="90a24-114">PARAMETERS</span></span>

### <span data-ttu-id="90a24-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="90a24-115">-AsJob</span></span>
<span data-ttu-id="90a24-116">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="90a24-116">Run the command as a job</span></span>

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

### <span data-ttu-id="90a24-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90a24-117">-DefaultProfile</span></span>
<span data-ttu-id="90a24-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="90a24-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="90a24-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="90a24-119">-InputObject</span></span>
<span data-ttu-id="90a24-120">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="90a24-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="90a24-121">-Name</span><span class="sxs-lookup"><span data-stu-id="90a24-121">-Name</span></span>
<span data-ttu-id="90a24-122">Имя экземпляра поставщика.</span><span class="sxs-lookup"><span data-stu-id="90a24-122">Name of the provider instance.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ProviderInstanceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90a24-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="90a24-123">-NoWait</span></span>
<span data-ttu-id="90a24-124">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="90a24-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="90a24-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="90a24-125">-PassThru</span></span>
<span data-ttu-id="90a24-126">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="90a24-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="90a24-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90a24-127">-ResourceGroupName</span></span>
<span data-ttu-id="90a24-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="90a24-128">Name of the resource group.</span></span>

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

### <span data-ttu-id="90a24-129">-SapMonitorName</span><span class="sxs-lookup"><span data-stu-id="90a24-129">-SapMonitorName</span></span>
<span data-ttu-id="90a24-130">Имя ресурса sap monitor.</span><span class="sxs-lookup"><span data-stu-id="90a24-130">Name of the SAP monitor resource.</span></span>

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

### <span data-ttu-id="90a24-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="90a24-131">-SubscriptionId</span></span>
<span data-ttu-id="90a24-132">ИД подписки, однозначно определяемой подпиской Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="90a24-132">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="90a24-133">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="90a24-133">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="90a24-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="90a24-134">-Confirm</span></span>
<span data-ttu-id="90a24-135">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="90a24-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90a24-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90a24-136">-WhatIf</span></span>
<span data-ttu-id="90a24-137">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="90a24-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90a24-138">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="90a24-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90a24-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90a24-139">CommonParameters</span></span>
<span data-ttu-id="90a24-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90a24-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90a24-141">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="90a24-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90a24-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="90a24-142">INPUTS</span></span>

### <span data-ttu-id="90a24-143">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span><span class="sxs-lookup"><span data-stu-id="90a24-143">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span></span>

## <span data-ttu-id="90a24-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="90a24-144">OUTPUTS</span></span>

### <span data-ttu-id="90a24-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="90a24-145">System.Boolean</span></span>

## <span data-ttu-id="90a24-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="90a24-146">NOTES</span></span>

<span data-ttu-id="90a24-147">ALIASES</span><span class="sxs-lookup"><span data-stu-id="90a24-147">ALIASES</span></span>

<span data-ttu-id="90a24-148">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="90a24-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="90a24-149">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="90a24-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="90a24-150">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="90a24-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="90a24-151">INPUTOBJECT <IHanaOnAzureIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="90a24-151">INPUTOBJECT <IHanaOnAzureIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="90a24-152">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="90a24-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="90a24-153">`[Location <String>]`: расположение удаленного сейфа.</span><span class="sxs-lookup"><span data-stu-id="90a24-153">`[Location <String>]`: The location of the deleted vault.</span></span>
  - <span data-ttu-id="90a24-154">`[OperationKind <AccessPolicyUpdateKind?>]`: название операции</span><span class="sxs-lookup"><span data-stu-id="90a24-154">`[OperationKind <AccessPolicyUpdateKind?>]`: Name of the operation</span></span>
  - <span data-ttu-id="90a24-155">`[ProviderInstanceName <String>]`: имя экземпляра поставщика.</span><span class="sxs-lookup"><span data-stu-id="90a24-155">`[ProviderInstanceName <String>]`: Name of the provider instance.</span></span>
  - <span data-ttu-id="90a24-156">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="90a24-156">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="90a24-157">`[ResourceName <String>]`: Имя ресурса удостоверения.</span><span class="sxs-lookup"><span data-stu-id="90a24-157">`[ResourceName <String>]`: The name of the identity resource.</span></span>
  - <span data-ttu-id="90a24-158">`[SapMonitorName <String>]`. Имя ресурса sap monitor.</span><span class="sxs-lookup"><span data-stu-id="90a24-158">`[SapMonitorName <String>]`: Name of the SAP monitor resource.</span></span>
  - <span data-ttu-id="90a24-159">`[Scope <String>]`Область поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="90a24-159">`[Scope <String>]`: The resource provider scope of the resource.</span></span> <span data-ttu-id="90a24-160">Родительский ресурс, который расширяется с помощью управляемых удостоверений.</span><span class="sxs-lookup"><span data-stu-id="90a24-160">Parent resource being extended by Managed Identities.</span></span>
  - <span data-ttu-id="90a24-161">`[SubscriptionId <String>]`: ИД подписки, однозначно определяемой подпиской Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="90a24-161">`[SubscriptionId <String>]`: Subscription ID which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="90a24-162">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="90a24-162">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="90a24-163">`[VaultName <String>]`: имя сейфа</span><span class="sxs-lookup"><span data-stu-id="90a24-163">`[VaultName <String>]`: Name of the vault</span></span>

## <span data-ttu-id="90a24-164">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="90a24-164">RELATED LINKS</span></span>

