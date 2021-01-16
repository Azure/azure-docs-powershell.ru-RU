---
external help file: ''
Module Name: Az.Portal
online version: https://docs.microsoft.com/en-us/powershell/module/az.portal/get-azportaldashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Get-AzPortalDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Get-AzPortalDashboard.md
ms.openlocfilehash: aa11a9828c422069823226b2d5df57efc84f8c7b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98424799"
---
# <span data-ttu-id="32bb5-101">Get-AzPortalDashboard</span><span class="sxs-lookup"><span data-stu-id="32bb5-101">Get-AzPortalDashboard</span></span>

## <span data-ttu-id="32bb5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="32bb5-102">SYNOPSIS</span></span>
<span data-ttu-id="32bb5-103">Получает панель мониторинга.</span><span class="sxs-lookup"><span data-stu-id="32bb5-103">Gets the Dashboard.</span></span>

## <span data-ttu-id="32bb5-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="32bb5-104">SYNTAX</span></span>

### <span data-ttu-id="32bb5-105">Список1 (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="32bb5-105">List1 (Default)</span></span>
```
Get-AzPortalDashboard [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="32bb5-106">Получить</span><span class="sxs-lookup"><span data-stu-id="32bb5-106">Get</span></span>
```
Get-AzPortalDashboard -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="32bb5-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="32bb5-107">GetViaIdentity</span></span>
```
Get-AzPortalDashboard -InputObject <IPortalIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="32bb5-108">Список</span><span class="sxs-lookup"><span data-stu-id="32bb5-108">List</span></span>
```
Get-AzPortalDashboard -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="32bb5-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="32bb5-109">DESCRIPTION</span></span>
<span data-ttu-id="32bb5-110">Получает панель мониторинга.</span><span class="sxs-lookup"><span data-stu-id="32bb5-110">Gets the Dashboard.</span></span>

## <span data-ttu-id="32bb5-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="32bb5-111">EXAMPLES</span></span>

### <span data-ttu-id="32bb5-112">Пример 1. Список всех панелей мониторинга в подписке</span><span class="sxs-lookup"><span data-stu-id="32bb5-112">Example 1: List all dashboards in a subscription</span></span>
```powershell
PS C:> Get-AzPortalDashboard                                                                                                                     
Location Name                                           Type
-------- ----                                           ----
eastasia my-custom-dashboard1                           Microsoft.Portal/dashboards
westus   my-second-custom-dashboard1                    Microsoft.Portal/dashboards

```

<span data-ttu-id="32bb5-113">Список всех панелей мониторинга в подписке</span><span class="sxs-lookup"><span data-stu-id="32bb5-113">List all dashboards in a subscription</span></span>

### <span data-ttu-id="32bb5-114">Пример 2. Сведения об одной информационной панели портала</span><span class="sxs-lookup"><span data-stu-id="32bb5-114">Example 2: Get details for a single Portal Dashboard</span></span>
```powershell
PS C:\> Get-AzPortalDashboard -ResourceGroupName my-rg -Name mydashboard

Location Name        Type
-------- ----        ----
eastus   mydashboard Microsoft.Portal/dashboards
```

<span data-ttu-id="32bb5-115">Сведения об одной панели мониторинга</span><span class="sxs-lookup"><span data-stu-id="32bb5-115">Get details for a single dashboard</span></span>

## <span data-ttu-id="32bb5-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="32bb5-116">PARAMETERS</span></span>

### <span data-ttu-id="32bb5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32bb5-117">-DefaultProfile</span></span>
<span data-ttu-id="32bb5-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="32bb5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="32bb5-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="32bb5-119">-InputObject</span></span>
<span data-ttu-id="32bb5-120">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="32bb5-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="32bb5-121">-Name</span><span class="sxs-lookup"><span data-stu-id="32bb5-121">-Name</span></span>
<span data-ttu-id="32bb5-122">Имя панели мониторинга.</span><span class="sxs-lookup"><span data-stu-id="32bb5-122">The name of the dashboard.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: DashboardName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32bb5-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32bb5-123">-ResourceGroupName</span></span>
<span data-ttu-id="32bb5-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="32bb5-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="32bb5-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="32bb5-125">-SubscriptionId</span></span>
<span data-ttu-id="32bb5-126">ИД подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="32bb5-126">The Azure subscription ID.</span></span>
<span data-ttu-id="32bb5-127">Строка в формате GUID (например, 00000000-0000-0000-0000-0000-00000000000000)</span><span class="sxs-lookup"><span data-stu-id="32bb5-127">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32bb5-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32bb5-128">CommonParameters</span></span>
<span data-ttu-id="32bb5-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32bb5-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32bb5-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="32bb5-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32bb5-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="32bb5-131">INPUTS</span></span>

### <span data-ttu-id="32bb5-132">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity</span><span class="sxs-lookup"><span data-stu-id="32bb5-132">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity</span></span>

## <span data-ttu-id="32bb5-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="32bb5-133">OUTPUTS</span></span>

### <span data-ttu-id="32bb5-134">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span><span class="sxs-lookup"><span data-stu-id="32bb5-134">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span></span>

## <span data-ttu-id="32bb5-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="32bb5-135">NOTES</span></span>

<span data-ttu-id="32bb5-136">ALIASES</span><span class="sxs-lookup"><span data-stu-id="32bb5-136">ALIASES</span></span>

<span data-ttu-id="32bb5-137">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="32bb5-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="32bb5-138">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="32bb5-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="32bb5-139">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="32bb5-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="32bb5-140">INPUTOBJECT <IPortalIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="32bb5-140">INPUTOBJECT <IPortalIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="32bb5-141">`[DashboardName <String>]`: название панели мониторинга.</span><span class="sxs-lookup"><span data-stu-id="32bb5-141">`[DashboardName <String>]`: The name of the dashboard.</span></span>
  - <span data-ttu-id="32bb5-142">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="32bb5-142">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="32bb5-143">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="32bb5-143">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="32bb5-144">`[SubscriptionId <String>]`: ИД подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="32bb5-144">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="32bb5-145">Строка в формате GUID (например, 00000000-0000-0000-0000-0000-00000000000000)</span><span class="sxs-lookup"><span data-stu-id="32bb5-145">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="32bb5-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="32bb5-146">RELATED LINKS</span></span>

