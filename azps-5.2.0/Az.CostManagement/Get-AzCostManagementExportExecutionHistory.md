---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.costmanagement/get-azcostmanagementexportexecutionhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Get-AzCostManagementExportExecutionHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Get-AzCostManagementExportExecutionHistory.md
ms.openlocfilehash: 7bb337837f9bd2be532c4eead8d8379b7cf04fe9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98395575"
---
# <span data-ttu-id="3c8fe-101">Get-AzCostManagementExportExecutionHistory</span><span class="sxs-lookup"><span data-stu-id="3c8fe-101">Get-AzCostManagementExportExecutionHistory</span></span>

## <span data-ttu-id="3c8fe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3c8fe-102">SYNOPSIS</span></span>
<span data-ttu-id="3c8fe-103">Операция получения истории выполнения экспорта для определенной области и имени экспорта.</span><span class="sxs-lookup"><span data-stu-id="3c8fe-103">The operation to get the execution history of an export for the defined scope and export name.</span></span>

## <span data-ttu-id="3c8fe-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3c8fe-104">SYNTAX</span></span>

### <span data-ttu-id="3c8fe-105">Получить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3c8fe-105">Get (Default)</span></span>
```
Get-AzCostManagementExportExecutionHistory -ExportName <String> -Scope <String> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="3c8fe-106">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="3c8fe-106">GetViaIdentity</span></span>
```
Get-AzCostManagementExportExecutionHistory -InputObject <ICostManagementIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="3c8fe-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3c8fe-107">DESCRIPTION</span></span>
<span data-ttu-id="3c8fe-108">Операция получения истории выполнения экспорта для определенной области и имени экспорта.</span><span class="sxs-lookup"><span data-stu-id="3c8fe-108">The operation to get the execution history of an export for the defined scope and export name.</span></span>

## <span data-ttu-id="3c8fe-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3c8fe-109">EXAMPLES</span></span>

### <span data-ttu-id="3c8fe-110">Пример 1. Получить AzCostManagementExportExecutionHistory</span><span class="sxs-lookup"><span data-stu-id="3c8fe-110">Example 1: Get AzCostManagementExportExecutionHistory</span></span>
```powershell
PS C:\> Get-AzCostManagementExportExecutionHistory -ExportName 'TestExport' -Scope 'subscriptions/**********'

ExecutionType ProcessingStartTime ProcessingEndTime  Status    FileName
------------- ------------------- -----------------  ------    --------
Scheduled     2020/6/11 12:03:20  2020/6/11 12:03:43 Completed ad-hoc/TestExport/20200601-20200630/TestExport_00000000-0000-0000-0000-000000000000.csv
Scheduled     2020/6/12 12:03:37  2020/6/12 12:03:48 Completed ad-hoc/TestExport/20200601-20200630/TestExport_00000000-0000-0000-0000-000000000000.csv
```

<span data-ttu-id="3c8fe-111">Получить AzCostManagementExportExecutionHistory By ExportName и Scope</span><span class="sxs-lookup"><span data-stu-id="3c8fe-111">Get AzCostManagementExportExecutionHistory By ExportName and Scope</span></span>

### <span data-ttu-id="3c8fe-112">Пример 2. Получить AzCostManagementExportExecutionHistory by InputObject</span><span class="sxs-lookup"><span data-stu-id="3c8fe-112">Example 2: Get AzCostManagementExportExecutionHistory by InputObject</span></span>
```powershell
PS C:\> $getExport = Get-AzCostManagementExport -Name 'TestExport' -Scope 'subscriptions/**********'
Get-AzCostManagementExportExecutionHistory -InputObject $getExport

ExecutionType ProcessingStartTime ProcessingEndTime  Status    FileName
------------- ------------------- -----------------  ------    --------
Scheduled     2020/6/11 12:03:20  2020/6/11 12:03:43 Completed ad-hoc/TestExport/20200601-20200630/TestExport_00000000-0000-0000-0000-000000000000.csv
Scheduled     2020/6/12 12:03:37  2020/6/12 12:03:48 Completed ad-hoc/TestExport/20200601-20200630/
```

<span data-ttu-id="3c8fe-113">Получить AzCostManagementExportExecutionHistory By InputObject</span><span class="sxs-lookup"><span data-stu-id="3c8fe-113">Get AzCostManagementExportExecutionHistory By InputObject</span></span>

## <span data-ttu-id="3c8fe-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3c8fe-114">PARAMETERS</span></span>

### <span data-ttu-id="3c8fe-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c8fe-115">-DefaultProfile</span></span>
<span data-ttu-id="3c8fe-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3c8fe-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3c8fe-117">-ExportName</span><span class="sxs-lookup"><span data-stu-id="3c8fe-117">-ExportName</span></span>
<span data-ttu-id="3c8fe-118">Имя экспорта.</span><span class="sxs-lookup"><span data-stu-id="3c8fe-118">Export Name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c8fe-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3c8fe-119">-InputObject</span></span>
<span data-ttu-id="3c8fe-120">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="3c8fe-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="3c8fe-121">-Scope</span><span class="sxs-lookup"><span data-stu-id="3c8fe-121">-Scope</span></span>
<span data-ttu-id="3c8fe-122">Этот параметр определяет область затрат по стоимости с различных точек зрения : "Подписка", "Группа ресурсов" и "Предоставление службы".</span><span class="sxs-lookup"><span data-stu-id="3c8fe-122">This parameter defines the scope of costmanagement from different perspectives 'Subscription','ResourceGroup' and 'Provide Service'.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c8fe-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c8fe-123">CommonParameters</span></span>
<span data-ttu-id="3c8fe-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c8fe-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c8fe-125">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3c8fe-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c8fe-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3c8fe-126">INPUTS</span></span>

### <span data-ttu-id="3c8fe-127">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity</span><span class="sxs-lookup"><span data-stu-id="3c8fe-127">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity</span></span>

## <span data-ttu-id="3c8fe-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3c8fe-128">OUTPUTS</span></span>

### <span data-ttu-id="3c8fe-129">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IExportExecution</span><span class="sxs-lookup"><span data-stu-id="3c8fe-129">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IExportExecution</span></span>

## <span data-ttu-id="3c8fe-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3c8fe-130">NOTES</span></span>

<span data-ttu-id="3c8fe-131">ALIASES</span><span class="sxs-lookup"><span data-stu-id="3c8fe-131">ALIASES</span></span>

<span data-ttu-id="3c8fe-132">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="3c8fe-132">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3c8fe-133">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="3c8fe-133">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3c8fe-134">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3c8fe-134">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3c8fe-135">INPUTOBJECT <ICostManagementIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="3c8fe-135">INPUTOBJECT <ICostManagementIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3c8fe-136">`[AlertId <String>]`: ИД оповещения</span><span class="sxs-lookup"><span data-stu-id="3c8fe-136">`[AlertId <String>]`: Alert ID</span></span>
  - <span data-ttu-id="3c8fe-137">`[ExportName <String>]`: имя экспорта.</span><span class="sxs-lookup"><span data-stu-id="3c8fe-137">`[ExportName <String>]`: Export Name.</span></span>
  - <span data-ttu-id="3c8fe-138">`[ExternalCloudProviderId <String>]`: {externalSubscriptionId}" для связанной учетной записи или {externalBillingAccountId}" для консолидированной учетной записи, которая используется для операций измерения или запроса.</span><span class="sxs-lookup"><span data-stu-id="3c8fe-138">`[ExternalCloudProviderId <String>]`: This can be '{externalSubscriptionId}' for linked account or '{externalBillingAccountId}' for consolidated account used with dimension/query operations.</span></span>
  - <span data-ttu-id="3c8fe-139">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`Внешний поставщик облачных услуг, связанный с операциями измерения или запроса.</span><span class="sxs-lookup"><span data-stu-id="3c8fe-139">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: The external cloud provider type associated with dimension/query operations.</span></span> <span data-ttu-id="3c8fe-140">К ним относятся 'externalSubscriptions' для связанных учетных записей и externalBillingAccounts для консолидированной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="3c8fe-140">This includes 'externalSubscriptions' for linked account and 'externalBillingAccounts' for consolidated account.</span></span>
  - <span data-ttu-id="3c8fe-141">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="3c8fe-141">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3c8fe-142">`[Scope <String>]`: область, связанная с действиями представления.</span><span class="sxs-lookup"><span data-stu-id="3c8fe-142">`[Scope <String>]`: The scope associated with view operations.</span></span> <span data-ttu-id="3c8fe-143">К ним относятся подписки/{subscriptionId}" для области подписки, "subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}" для области resourceGroup, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}" для области учетной записи вы выставления счетов, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}" для области Department, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}" для области EnrollmentAccountunt, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}" for BillingProfile Scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' для области InvoiceSection, "providers/Microsoft.Management/managementGroups/{managementGroupId}" for Management Group scope, 'providers/Microsoft.CostManagement/externalBillingAccounts/{externalBillingAccountName}" for External Billing Account scope and 'providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}" для внешней подписки.</span><span class="sxs-lookup"><span data-stu-id="3c8fe-143">This includes 'subscriptions/{subscriptionId}' for subscription scope, 'subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}' for resourceGroup scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' for Billing Account scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' for Department scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' for BillingProfile scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' for InvoiceSection scope, 'providers/Microsoft.Management/managementGroups/{managementGroupId}' for Management Group scope, 'providers/Microsoft.CostManagement/externalBillingAccounts/{externalBillingAccountName}' for External Billing Account scope and 'providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}' for External Subscription scope.</span></span>
  - <span data-ttu-id="3c8fe-144">`[ViewName <String>]`: имя представления</span><span class="sxs-lookup"><span data-stu-id="3c8fe-144">`[ViewName <String>]`: View name</span></span>

## <span data-ttu-id="3c8fe-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3c8fe-145">RELATED LINKS</span></span>

