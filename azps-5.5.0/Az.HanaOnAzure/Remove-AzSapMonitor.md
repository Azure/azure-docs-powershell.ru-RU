---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/en-us/powershell/module/az.hanaonazure/remove-azsapmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Remove-AzSapMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Remove-AzSapMonitor.md
ms.openlocfilehash: bcba06d87bce2f9ccc8016afc9f08dff75e29b1c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100219892"
---
# <span data-ttu-id="ce253-101">Remove-AzSapMonitor</span><span class="sxs-lookup"><span data-stu-id="ce253-101">Remove-AzSapMonitor</span></span>

## <span data-ttu-id="ce253-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ce253-102">SYNOPSIS</span></span>
<span data-ttu-id="ce253-103">Удаляет монитор SAP с указанной подпиской, группой ресурсов и именем монитора.</span><span class="sxs-lookup"><span data-stu-id="ce253-103">Deletes a SAP monitor with the specified subscription, resource group, and monitor name.</span></span>

## <span data-ttu-id="ce253-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ce253-104">SYNTAX</span></span>

### <span data-ttu-id="ce253-105">Delete (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ce253-105">Delete (Default)</span></span>
```
Remove-AzSapMonitor -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ce253-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ce253-106">DeleteViaIdentity</span></span>
```
Remove-AzSapMonitor -InputObject <IHanaOnAzureIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ce253-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ce253-107">DESCRIPTION</span></span>
<span data-ttu-id="ce253-108">Удаляет монитор SAP с указанной подпиской, группой ресурсов и именем монитора.</span><span class="sxs-lookup"><span data-stu-id="ce253-108">Deletes a SAP monitor with the specified subscription, resource group, and monitor name.</span></span>

## <span data-ttu-id="ce253-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ce253-109">EXAMPLES</span></span>

### <span data-ttu-id="ce253-110">Пример 1. Удаление монитора SAP по имени</span><span class="sxs-lookup"><span data-stu-id="ce253-110">Example 1: Remove a SAP monitor by name</span></span>
```powershell
PS C:\> Remove-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-sapmonitor-t02

```

<span data-ttu-id="ce253-111">Эта команда удаляет монитор SAP по имени.</span><span class="sxs-lookup"><span data-stu-id="ce253-111">This command removes a SAP monitor by name.</span></span>

### <span data-ttu-id="ce253-112">Пример 2. Удаление монитора SAP по объектам</span><span class="sxs-lookup"><span data-stu-id="ce253-112">Example 2: Remove a SAP monitor by object</span></span>
```powershell
PS C:\> $sap = Get-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-sapmonitor-t01
PS C:\> Remove-AzSapMonitor -InputObject $sap

```

<span data-ttu-id="ce253-113">Эта команда удаляет монитор SAP по объектам.</span><span class="sxs-lookup"><span data-stu-id="ce253-113">This command removes a SAP monitor by object.</span></span>

## <span data-ttu-id="ce253-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ce253-114">PARAMETERS</span></span>

### <span data-ttu-id="ce253-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ce253-115">-AsJob</span></span>
<span data-ttu-id="ce253-116">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="ce253-116">Run the command as a job</span></span>

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

### <span data-ttu-id="ce253-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce253-117">-DefaultProfile</span></span>
<span data-ttu-id="ce253-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ce253-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ce253-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ce253-119">-InputObject</span></span>
<span data-ttu-id="ce253-120">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="ce253-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ce253-121">-Name</span><span class="sxs-lookup"><span data-stu-id="ce253-121">-Name</span></span>
<span data-ttu-id="ce253-122">Имя ресурса sap monitor.</span><span class="sxs-lookup"><span data-stu-id="ce253-122">Name of the SAP monitor resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: SapMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce253-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="ce253-123">-NoWait</span></span>
<span data-ttu-id="ce253-124">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="ce253-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ce253-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ce253-125">-PassThru</span></span>
<span data-ttu-id="ce253-126">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="ce253-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="ce253-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce253-127">-ResourceGroupName</span></span>
<span data-ttu-id="ce253-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ce253-128">Name of the resource group.</span></span>

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

### <span data-ttu-id="ce253-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ce253-129">-SubscriptionId</span></span>
<span data-ttu-id="ce253-130">ИД подписки, однозначно определяемой подпиской Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ce253-130">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="ce253-131">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="ce253-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="ce253-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ce253-132">-Confirm</span></span>
<span data-ttu-id="ce253-133">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="ce253-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce253-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce253-134">-WhatIf</span></span>
<span data-ttu-id="ce253-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ce253-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce253-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="ce253-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce253-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce253-137">CommonParameters</span></span>
<span data-ttu-id="ce253-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce253-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce253-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ce253-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce253-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ce253-140">INPUTS</span></span>

### <span data-ttu-id="ce253-141">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span><span class="sxs-lookup"><span data-stu-id="ce253-141">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span></span>

## <span data-ttu-id="ce253-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ce253-142">OUTPUTS</span></span>

### <span data-ttu-id="ce253-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ce253-143">System.Boolean</span></span>

## <span data-ttu-id="ce253-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ce253-144">NOTES</span></span>

<span data-ttu-id="ce253-145">ALIASES</span><span class="sxs-lookup"><span data-stu-id="ce253-145">ALIASES</span></span>

<span data-ttu-id="ce253-146">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="ce253-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ce253-147">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="ce253-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ce253-148">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ce253-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ce253-149">INPUTOBJECT <IHanaOnAzureIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="ce253-149">INPUTOBJECT <IHanaOnAzureIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ce253-150">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="ce253-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ce253-151">`[Location <String>]`: расположение удаленного сейфа.</span><span class="sxs-lookup"><span data-stu-id="ce253-151">`[Location <String>]`: The location of the deleted vault.</span></span>
  - <span data-ttu-id="ce253-152">`[OperationKind <AccessPolicyUpdateKind?>]`: название операции</span><span class="sxs-lookup"><span data-stu-id="ce253-152">`[OperationKind <AccessPolicyUpdateKind?>]`: Name of the operation</span></span>
  - <span data-ttu-id="ce253-153">`[ProviderInstanceName <String>]`: имя экземпляра поставщика.</span><span class="sxs-lookup"><span data-stu-id="ce253-153">`[ProviderInstanceName <String>]`: Name of the provider instance.</span></span>
  - <span data-ttu-id="ce253-154">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ce253-154">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="ce253-155">`[ResourceName <String>]`: Имя ресурса удостоверения.</span><span class="sxs-lookup"><span data-stu-id="ce253-155">`[ResourceName <String>]`: The name of the identity resource.</span></span>
  - <span data-ttu-id="ce253-156">`[SapMonitorName <String>]`. Имя ресурса sap monitor.</span><span class="sxs-lookup"><span data-stu-id="ce253-156">`[SapMonitorName <String>]`: Name of the SAP monitor resource.</span></span>
  - <span data-ttu-id="ce253-157">`[Scope <String>]`Область поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ce253-157">`[Scope <String>]`: The resource provider scope of the resource.</span></span> <span data-ttu-id="ce253-158">Родительский ресурс, который расширяется с помощью управляемых удостоверений.</span><span class="sxs-lookup"><span data-stu-id="ce253-158">Parent resource being extended by Managed Identities.</span></span>
  - <span data-ttu-id="ce253-159">`[SubscriptionId <String>]`: ИД подписки, однозначно определяемой подпиской Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ce253-159">`[SubscriptionId <String>]`: Subscription ID which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="ce253-160">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="ce253-160">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="ce253-161">`[VaultName <String>]`: имя сейфа</span><span class="sxs-lookup"><span data-stu-id="ce253-161">`[VaultName <String>]`: Name of the vault</span></span>

## <span data-ttu-id="ce253-162">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ce253-162">RELATED LINKS</span></span>

