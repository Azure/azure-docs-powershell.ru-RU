---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.costmanagement/get-azcostmanagementexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Get-AzCostManagementExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Get-AzCostManagementExport.md
ms.openlocfilehash: 269a58e57510f6b0945218645ec079b21b606e44
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98519162"
---
# <span data-ttu-id="a612e-101">Get-AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="a612e-101">Get-AzCostManagementExport</span></span>

## <span data-ttu-id="a612e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a612e-102">SYNOPSIS</span></span>
<span data-ttu-id="a612e-103">Операция получения экспорта для определенной области по имени экспорта.</span><span class="sxs-lookup"><span data-stu-id="a612e-103">The operation to get the export for the defined scope by export name.</span></span>

## <span data-ttu-id="a612e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a612e-104">SYNTAX</span></span>

### <span data-ttu-id="a612e-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a612e-105">List (Default)</span></span>
```
Get-AzCostManagementExport -Scope <String> [-Expand <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="a612e-106">Получить</span><span class="sxs-lookup"><span data-stu-id="a612e-106">Get</span></span>
```
Get-AzCostManagementExport -Name <String> -Scope <String> [-Expand <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="a612e-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a612e-107">GetViaIdentity</span></span>
```
Get-AzCostManagementExport -InputObject <ICostManagementIdentity> [-Expand <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="a612e-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a612e-108">DESCRIPTION</span></span>
<span data-ttu-id="a612e-109">Операция получения экспорта для определенной области по имени экспорта.</span><span class="sxs-lookup"><span data-stu-id="a612e-109">The operation to get the export for the defined scope by export name.</span></span>

## <span data-ttu-id="a612e-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a612e-110">EXAMPLES</span></span>

### <span data-ttu-id="a612e-111">Пример 1. Получить все AzCostManagementExports по области</span><span class="sxs-lookup"><span data-stu-id="a612e-111">Example 1: Get all AzCostManagementExports by scope</span></span>
```powershell
PS C:\> Get-AzCostManagementExport -Scope 'subscriptions/**********'

ETag              Name                               Type
----              ----                               ----
"************" TestExport                         Microsoft.CostManagement/exports
"************" TestExport1                        Microsoft.CostManagement/exports
"************" TestExport2                        Microsoft.CostManagement/exports
```

<span data-ttu-id="a612e-112">Получить все AzCostManagementExports по области</span><span class="sxs-lookup"><span data-stu-id="a612e-112">Get all AzCostManagementExports by Scope</span></span>

### <span data-ttu-id="a612e-113">Пример 2. Получить AzCostManagementExport по имени и области</span><span class="sxs-lookup"><span data-stu-id="a612e-113">Example 2: Get AzCostManagementExport by Name and scope</span></span>
```powershell
PS C:\> Get-AzCostManagementExport -Name 'TestExport' -Scope 'subscriptions/**********'

ETag              Name       Type
----              ----       ----
"************" TestExport Microsoft.CostManagement/exports
```

<span data-ttu-id="a612e-114">Получить AzCostManagementExport по имени и области</span><span class="sxs-lookup"><span data-stu-id="a612e-114">Get AzCostManagementExport by Name and scope</span></span>

## <span data-ttu-id="a612e-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a612e-115">PARAMETERS</span></span>

### <span data-ttu-id="a612e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a612e-116">-DefaultProfile</span></span>
<span data-ttu-id="a612e-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a612e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a612e-118">-Развернуть</span><span class="sxs-lookup"><span data-stu-id="a612e-118">-Expand</span></span>
<span data-ttu-id="a612e-119">Может использоваться для расширения свойств в экспорте.</span><span class="sxs-lookup"><span data-stu-id="a612e-119">May be used to expand the properties within an export.</span></span>
<span data-ttu-id="a612e-120">В настоящее время поддерживается только система runHistory, которая возвращает сведения о последних 10 выполнениях экспорта.</span><span class="sxs-lookup"><span data-stu-id="a612e-120">Currently only 'runHistory' is supported and will return information for the last 10 executions of the export.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a612e-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a612e-121">-InputObject</span></span>
<span data-ttu-id="a612e-122">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="a612e-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a612e-123">-Name</span><span class="sxs-lookup"><span data-stu-id="a612e-123">-Name</span></span>
<span data-ttu-id="a612e-124">Имя экспорта.</span><span class="sxs-lookup"><span data-stu-id="a612e-124">Export Name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ExportName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a612e-125">-Scope</span><span class="sxs-lookup"><span data-stu-id="a612e-125">-Scope</span></span>
<span data-ttu-id="a612e-126">Этот параметр определяет область затрат по стоимости с различных точек зрения : "Подписка", "Группа ресурсов" и "Предоставление службы".</span><span class="sxs-lookup"><span data-stu-id="a612e-126">This parameter defines the scope of costmanagement from different perspectives 'Subscription','ResourceGroup' and 'Provide Service'.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a612e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a612e-127">CommonParameters</span></span>
<span data-ttu-id="a612e-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a612e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a612e-129">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a612e-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a612e-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a612e-130">INPUTS</span></span>

### <span data-ttu-id="a612e-131">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity</span><span class="sxs-lookup"><span data-stu-id="a612e-131">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity</span></span>

## <span data-ttu-id="a612e-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a612e-132">OUTPUTS</span></span>

### <span data-ttu-id="a612e-133">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IExport</span><span class="sxs-lookup"><span data-stu-id="a612e-133">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IExport</span></span>

## <span data-ttu-id="a612e-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a612e-134">NOTES</span></span>

<span data-ttu-id="a612e-135">ALIASES</span><span class="sxs-lookup"><span data-stu-id="a612e-135">ALIASES</span></span>

<span data-ttu-id="a612e-136">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="a612e-136">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a612e-137">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="a612e-137">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a612e-138">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a612e-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a612e-139">INPUTOBJECT <ICostManagementIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="a612e-139">INPUTOBJECT <ICostManagementIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a612e-140">`[AlertId <String>]`: ИД оповещения</span><span class="sxs-lookup"><span data-stu-id="a612e-140">`[AlertId <String>]`: Alert ID</span></span>
  - <span data-ttu-id="a612e-141">`[ExportName <String>]`: имя экспорта.</span><span class="sxs-lookup"><span data-stu-id="a612e-141">`[ExportName <String>]`: Export Name.</span></span>
  - <span data-ttu-id="a612e-142">`[ExternalCloudProviderId <String>]`: {externalSubscriptionId}" для связанной учетной записи или {externalBillingAccountId}" для консолидированной учетной записи, которая используется для операций измерения или запроса.</span><span class="sxs-lookup"><span data-stu-id="a612e-142">`[ExternalCloudProviderId <String>]`: This can be '{externalSubscriptionId}' for linked account or '{externalBillingAccountId}' for consolidated account used with dimension/query operations.</span></span>
  - <span data-ttu-id="a612e-143">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`Внешний поставщик облачных услуг, связанный с операциями измерения или запроса.</span><span class="sxs-lookup"><span data-stu-id="a612e-143">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: The external cloud provider type associated with dimension/query operations.</span></span> <span data-ttu-id="a612e-144">К ним относятся 'externalSubscriptions' для связанных учетных записей и externalBillingAccounts для консолидированной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="a612e-144">This includes 'externalSubscriptions' for linked account and 'externalBillingAccounts' for consolidated account.</span></span>
  - <span data-ttu-id="a612e-145">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="a612e-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a612e-146">`[Scope <String>]`: область, связанная с действиями представления.</span><span class="sxs-lookup"><span data-stu-id="a612e-146">`[Scope <String>]`: The scope associated with view operations.</span></span> <span data-ttu-id="a612e-147">К ним относятся подписки/{subscriptionId}, для области действия подписки, "subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}" для области resourceGroup, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}" для области учетной записи вы выставления счетов, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}" для области Department, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}" для области EnrollmentAccountunt, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}" for BillingProfile Scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' для области InvoiceSection, "providers/Microsoft.Management/managementGroups/{managementGroupId}" for Management Group scope, 'providers/Microsoft.CostManagement/externalBillingAccounts/{externalBillingAccountName}" for External Billing Account scope and 'providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}" для внешней подписки.</span><span class="sxs-lookup"><span data-stu-id="a612e-147">This includes 'subscriptions/{subscriptionId}' for subscription scope, 'subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}' for resourceGroup scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' for Billing Account scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' for Department scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' for BillingProfile scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' for InvoiceSection scope, 'providers/Microsoft.Management/managementGroups/{managementGroupId}' for Management Group scope, 'providers/Microsoft.CostManagement/externalBillingAccounts/{externalBillingAccountName}' for External Billing Account scope and 'providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}' for External Subscription scope.</span></span>
  - <span data-ttu-id="a612e-148">`[ViewName <String>]`: имя представления</span><span class="sxs-lookup"><span data-stu-id="a612e-148">`[ViewName <String>]`: View name</span></span>

## <span data-ttu-id="a612e-149">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a612e-149">RELATED LINKS</span></span>

