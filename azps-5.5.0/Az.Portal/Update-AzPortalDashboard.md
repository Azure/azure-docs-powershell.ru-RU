---
external help file: ''
Module Name: Az.Portal
online version: https://docs.microsoft.com/en-us/powershell/module/az.portal/update-azportaldashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Update-AzPortalDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Update-AzPortalDashboard.md
ms.openlocfilehash: 42c5d90a24e671c47245ace0046c6f5987dbcd94
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100218089"
---
# <span data-ttu-id="52303-101">Update-AzPortalDashboard</span><span class="sxs-lookup"><span data-stu-id="52303-101">Update-AzPortalDashboard</span></span>

## <span data-ttu-id="52303-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="52303-102">SYNOPSIS</span></span>
<span data-ttu-id="52303-103">Обновляет существующую информационную панель.</span><span class="sxs-lookup"><span data-stu-id="52303-103">Updates an existing Dashboard.</span></span>

## <span data-ttu-id="52303-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="52303-104">SYNTAX</span></span>

### <span data-ttu-id="52303-105">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="52303-105">UpdateExpanded (Default)</span></span>
```
Update-AzPortalDashboard -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Lens <Hashtable>] [-Metadata <Hashtable>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="52303-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="52303-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzPortalDashboard -InputObject <IPortalIdentity> [-Lens <Hashtable>] [-Metadata <Hashtable>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="52303-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="52303-107">DESCRIPTION</span></span>
<span data-ttu-id="52303-108">Обновляет существующую информационную панель.</span><span class="sxs-lookup"><span data-stu-id="52303-108">Updates an existing Dashboard.</span></span>

## <span data-ttu-id="52303-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="52303-109">EXAMPLES</span></span>

### <span data-ttu-id="52303-110">Пример 1. Обновление тегов панели мониторинга</span><span class="sxs-lookup"><span data-stu-id="52303-110">Example 1: Update the Tags of a Dashboard</span></span>
```powershell
PS C:\> Update-AzPortalDashboard -ResourceGroupName my-rg -Name dashbase03 -Tag @{'hidden-title'="My Dashboard Title"; NewTag="NewValue"}

Location Name       Type
-------- ----       ----
eastasia dashbase03 Microsoft.Portal/dashboards
```

<span data-ttu-id="52303-111">Обновив теги на панели мониторинга.</span><span class="sxs-lookup"><span data-stu-id="52303-111">Update the tags in a dashboard.</span></span>
<span data-ttu-id="52303-112">Теги представлены как вмещаемый веха.</span><span class="sxs-lookup"><span data-stu-id="52303-112">Tags are represented as an inline hashtable.</span></span>

### <span data-ttu-id="52303-113">Пример 2. Обновление тегов панели мониторинга с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="52303-113">Example 2: Update Dashboard tags using the pipeline</span></span>
```powershell
PS C:\> Get-AzPortalDashboard -ResourceGroupName my-rg -Name dashbase03 | Update-AzPortalDashboard -Tag @{'hidden-title'="My Dashboard Title"; NewTag="NewValue"}

Location Name       Type
-------- ----       ----
eastasia dashbase03 Microsoft.Portal/dashboards
```

<span data-ttu-id="52303-114">Обновите теги на панели мониторинга, искомые с помощью Get-AzPortalDashboard.</span><span class="sxs-lookup"><span data-stu-id="52303-114">Update the Tags in a Dashboard retried using Get-AzPortalDashboard.</span></span>
<span data-ttu-id="52303-115">Это может использоваться для обновления тегов на одной панели мониторинга или нескольких панелях мониторинга.</span><span class="sxs-lookup"><span data-stu-id="52303-115">This can be used to update the tags over a single dashboard, or multiple dashboardfs.</span></span>

## <span data-ttu-id="52303-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="52303-116">PARAMETERS</span></span>

### <span data-ttu-id="52303-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52303-117">-DefaultProfile</span></span>
<span data-ttu-id="52303-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="52303-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52303-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="52303-119">-InputObject</span></span>
<span data-ttu-id="52303-120">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="52303-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="52303-121">-Lens</span><span class="sxs-lookup"><span data-stu-id="52303-121">-Lens</span></span>
<span data-ttu-id="52303-122">Панели мониторинга.</span><span class="sxs-lookup"><span data-stu-id="52303-122">The dashboard lenses.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52303-123">-Метаданные</span><span class="sxs-lookup"><span data-stu-id="52303-123">-Metadata</span></span>
<span data-ttu-id="52303-124">Метаданные панели мониторинга.</span><span class="sxs-lookup"><span data-stu-id="52303-124">The dashboard metadata.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52303-125">-Name</span><span class="sxs-lookup"><span data-stu-id="52303-125">-Name</span></span>
<span data-ttu-id="52303-126">Имя панели мониторинга.</span><span class="sxs-lookup"><span data-stu-id="52303-126">The name of the dashboard.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: DashboardName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52303-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52303-127">-ResourceGroupName</span></span>
<span data-ttu-id="52303-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="52303-128">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52303-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="52303-129">-SubscriptionId</span></span>
<span data-ttu-id="52303-130">ИД подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="52303-130">The Azure subscription ID.</span></span>
<span data-ttu-id="52303-131">Строка в формате GUID (например, 00000000-0000-0000-0000-0000-00000000000000)</span><span class="sxs-lookup"><span data-stu-id="52303-131">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52303-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="52303-132">-Tag</span></span>
<span data-ttu-id="52303-133">Теги ресурсов</span><span class="sxs-lookup"><span data-stu-id="52303-133">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52303-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="52303-134">-Confirm</span></span>
<span data-ttu-id="52303-135">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="52303-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52303-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52303-136">-WhatIf</span></span>
<span data-ttu-id="52303-137">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="52303-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52303-138">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="52303-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52303-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52303-139">CommonParameters</span></span>
<span data-ttu-id="52303-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52303-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52303-141">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="52303-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52303-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="52303-142">INPUTS</span></span>

### <span data-ttu-id="52303-143">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity</span><span class="sxs-lookup"><span data-stu-id="52303-143">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity</span></span>

## <span data-ttu-id="52303-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="52303-144">OUTPUTS</span></span>

### <span data-ttu-id="52303-145">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span><span class="sxs-lookup"><span data-stu-id="52303-145">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span></span>

## <span data-ttu-id="52303-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="52303-146">NOTES</span></span>

<span data-ttu-id="52303-147">ALIASES</span><span class="sxs-lookup"><span data-stu-id="52303-147">ALIASES</span></span>

<span data-ttu-id="52303-148">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="52303-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="52303-149">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="52303-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="52303-150">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="52303-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="52303-151">INPUTOBJECT <IPortalIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="52303-151">INPUTOBJECT <IPortalIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="52303-152">`[DashboardName <String>]`: название панели мониторинга.</span><span class="sxs-lookup"><span data-stu-id="52303-152">`[DashboardName <String>]`: The name of the dashboard.</span></span>
  - <span data-ttu-id="52303-153">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="52303-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="52303-154">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="52303-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="52303-155">`[SubscriptionId <String>]`: ИД подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="52303-155">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="52303-156">Строка в формате GUID (например, 00000000-0000-0000-0000-0000-00000000000000)</span><span class="sxs-lookup"><span data-stu-id="52303-156">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="52303-157">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="52303-157">RELATED LINKS</span></span>

