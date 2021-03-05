---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/powershell/module/az.costmanagement/remove-azcostmanagementexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Remove-AzCostManagementExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Remove-AzCostManagementExport.md
ms.openlocfilehash: e3c464ee8a2ae038a9e6d8d7578c3e4862c16460
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101962408"
---
# <span data-ttu-id="6db7f-101">Remove-AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="6db7f-101">Remove-AzCostManagementExport</span></span>

## <span data-ttu-id="6db7f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6db7f-102">SYNOPSIS</span></span>
<span data-ttu-id="6db7f-103">Операция удаления экспорта.</span><span class="sxs-lookup"><span data-stu-id="6db7f-103">The operation to delete a export.</span></span>

## <span data-ttu-id="6db7f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6db7f-104">SYNTAX</span></span>

### <span data-ttu-id="6db7f-105">Delete (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6db7f-105">Delete (Default)</span></span>
```
Remove-AzCostManagementExport -Name <String> -Scope <String> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6db7f-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="6db7f-106">DeleteViaIdentity</span></span>
```
Remove-AzCostManagementExport -InputObject <ICostManagementIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6db7f-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6db7f-107">DESCRIPTION</span></span>
<span data-ttu-id="6db7f-108">Операция удаления экспорта.</span><span class="sxs-lookup"><span data-stu-id="6db7f-108">The operation to delete a export.</span></span>

## <span data-ttu-id="6db7f-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6db7f-109">EXAMPLES</span></span>

### <span data-ttu-id="6db7f-110">Пример 1. Удаление AzCostManagementExport по области и имени</span><span class="sxs-lookup"><span data-stu-id="6db7f-110">Example 1: Delete the AzCostManagementExport by Scope and Name</span></span>
```powershell
PS C:\> Remove-AzCostManagementExport -Scope 'subscriptions/********' -name 'TestExportDatasetAggregationInfoYouri'


```

<span data-ttu-id="6db7f-111">Delete the AzCostManagementExport By Scope and ExportName</span><span class="sxs-lookup"><span data-stu-id="6db7f-111">Delete the AzCostManagementExport By Scope and ExportName</span></span>

### <span data-ttu-id="6db7f-112">Пример 2. Удаление AzCostManagementExport с помощью экспорта объекта</span><span class="sxs-lookup"><span data-stu-id="6db7f-112">Example 2: Delete the AzCostManagementExport by Export Object</span></span>
```powershell
PS C:\> $getExport = Get-AzCostManagementExport -Scope 'subscriptions/*********' -name 'TestExportDatasetAggregationYouori'
Remove-AzCostManagementExport -InputObject $getExport


```

<span data-ttu-id="6db7f-113">Удаление AzCostManagementExport by InputObject</span><span class="sxs-lookup"><span data-stu-id="6db7f-113">Delete the AzCostManagementExport By InputObject</span></span>

## <span data-ttu-id="6db7f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6db7f-114">PARAMETERS</span></span>

### <span data-ttu-id="6db7f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6db7f-115">-DefaultProfile</span></span>
<span data-ttu-id="6db7f-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6db7f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6db7f-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6db7f-117">-InputObject</span></span>
<span data-ttu-id="6db7f-118">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="6db7f-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6db7f-119">-Name</span><span class="sxs-lookup"><span data-stu-id="6db7f-119">-Name</span></span>
<span data-ttu-id="6db7f-120">Имя экспорта.</span><span class="sxs-lookup"><span data-stu-id="6db7f-120">Export Name.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ExportName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6db7f-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6db7f-121">-PassThru</span></span>
<span data-ttu-id="6db7f-122">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="6db7f-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="6db7f-123">-Scope</span><span class="sxs-lookup"><span data-stu-id="6db7f-123">-Scope</span></span>
<span data-ttu-id="6db7f-124">Этот параметр определяет область затрат по стоимости с различных точек зрения : "Подписка", "Группа ресурсов" и "Предоставление службы".</span><span class="sxs-lookup"><span data-stu-id="6db7f-124">This parameter defines the scope of costmanagement from different perspectives 'Subscription','ResourceGroup' and 'Provide Service'.</span></span>

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

### <span data-ttu-id="6db7f-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6db7f-125">-Confirm</span></span>
<span data-ttu-id="6db7f-126">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6db7f-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6db7f-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6db7f-127">-WhatIf</span></span>
<span data-ttu-id="6db7f-128">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6db7f-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6db7f-129">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="6db7f-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6db7f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6db7f-130">CommonParameters</span></span>
<span data-ttu-id="6db7f-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6db7f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6db7f-132">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6db7f-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6db7f-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6db7f-133">INPUTS</span></span>

### <span data-ttu-id="6db7f-134">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity</span><span class="sxs-lookup"><span data-stu-id="6db7f-134">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity</span></span>

## <span data-ttu-id="6db7f-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6db7f-135">OUTPUTS</span></span>

### <span data-ttu-id="6db7f-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6db7f-136">System.Boolean</span></span>

## <span data-ttu-id="6db7f-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6db7f-137">NOTES</span></span>

<span data-ttu-id="6db7f-138">ALIASES</span><span class="sxs-lookup"><span data-stu-id="6db7f-138">ALIASES</span></span>

<span data-ttu-id="6db7f-139">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="6db7f-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6db7f-140">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="6db7f-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6db7f-141">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6db7f-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6db7f-142">INPUTOBJECT <ICostManagementIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="6db7f-142">INPUTOBJECT <ICostManagementIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6db7f-143">`[AlertId <String>]`: ИД оповещения</span><span class="sxs-lookup"><span data-stu-id="6db7f-143">`[AlertId <String>]`: Alert ID</span></span>
  - <span data-ttu-id="6db7f-144">`[ExportName <String>]`: имя экспорта.</span><span class="sxs-lookup"><span data-stu-id="6db7f-144">`[ExportName <String>]`: Export Name.</span></span>
  - <span data-ttu-id="6db7f-145">`[ExternalCloudProviderId <String>]`: {externalSubscriptionId}" для связанной учетной записи или {externalBillingAccountId}" для консолидированной учетной записи, которая используется для операций измерения или запроса.</span><span class="sxs-lookup"><span data-stu-id="6db7f-145">`[ExternalCloudProviderId <String>]`: This can be '{externalSubscriptionId}' for linked account or '{externalBillingAccountId}' for consolidated account used with dimension/query operations.</span></span>
  - <span data-ttu-id="6db7f-146">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`Внешний поставщик облачных услуг, связанный с операциями измерения или запроса.</span><span class="sxs-lookup"><span data-stu-id="6db7f-146">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: The external cloud provider type associated with dimension/query operations.</span></span> <span data-ttu-id="6db7f-147">К ним относятся 'externalSubscriptions' для связанных учетных записей и externalBillingAccounts для консолидированной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="6db7f-147">This includes 'externalSubscriptions' for linked account and 'externalBillingAccounts' for consolidated account.</span></span>
  - <span data-ttu-id="6db7f-148">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="6db7f-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6db7f-149">`[Scope <String>]`: область, связанная с действиями представления.</span><span class="sxs-lookup"><span data-stu-id="6db7f-149">`[Scope <String>]`: The scope associated with view operations.</span></span> <span data-ttu-id="6db7f-150">К ним относятся подписки/{subscriptionId}" для области подписки, "subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}" для области resourceGroup, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}" для области учетной записи вы выставления счетов, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}" для области Department, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}" для области EnrollmentAccountunt, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}" for BillingProfile Scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' для области InvoiceSection, "providers/Microsoft.Management/managementGroups/{managementGroupId}" for Management Group scope, 'providers/Microsoft.CostManagement/externalBillingAccounts/{externalBillingAccountName}" for External Billing Account scope and 'providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}" для внешней подписки.</span><span class="sxs-lookup"><span data-stu-id="6db7f-150">This includes 'subscriptions/{subscriptionId}' for subscription scope, 'subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}' for resourceGroup scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' for Billing Account scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' for Department scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' for BillingProfile scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' for InvoiceSection scope, 'providers/Microsoft.Management/managementGroups/{managementGroupId}' for Management Group scope, 'providers/Microsoft.CostManagement/externalBillingAccounts/{externalBillingAccountName}' for External Billing Account scope and 'providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}' for External Subscription scope.</span></span>
  - <span data-ttu-id="6db7f-151">`[ViewName <String>]`: имя представления</span><span class="sxs-lookup"><span data-stu-id="6db7f-151">`[ViewName <String>]`: View name</span></span>

## <span data-ttu-id="6db7f-152">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6db7f-152">RELATED LINKS</span></span>

