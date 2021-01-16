---
external help file: ''
Module Name: Az.Portal
online version: https://docs.microsoft.com/en-us/powershell/module/az.portal/update-azportaldashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Update-AzPortalDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Update-AzPortalDashboard.md
ms.openlocfilehash: 42c5d90a24e671c47245ace0046c6f5987dbcd94
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98421367"
---
# <span data-ttu-id="ade45-101">Update-AzPortalDashboard</span><span class="sxs-lookup"><span data-stu-id="ade45-101">Update-AzPortalDashboard</span></span>

## <span data-ttu-id="ade45-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ade45-102">SYNOPSIS</span></span>
<span data-ttu-id="ade45-103">Обновляет существующую информационную панель.</span><span class="sxs-lookup"><span data-stu-id="ade45-103">Updates an existing Dashboard.</span></span>

## <span data-ttu-id="ade45-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ade45-104">SYNTAX</span></span>

### <span data-ttu-id="ade45-105">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ade45-105">UpdateExpanded (Default)</span></span>
```
Update-AzPortalDashboard -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Lens <Hashtable>] [-Metadata <Hashtable>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ade45-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="ade45-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzPortalDashboard -InputObject <IPortalIdentity> [-Lens <Hashtable>] [-Metadata <Hashtable>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ade45-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ade45-107">DESCRIPTION</span></span>
<span data-ttu-id="ade45-108">Обновляет существующую информационную панель.</span><span class="sxs-lookup"><span data-stu-id="ade45-108">Updates an existing Dashboard.</span></span>

## <span data-ttu-id="ade45-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ade45-109">EXAMPLES</span></span>

### <span data-ttu-id="ade45-110">Пример 1. Обновление тегов панели мониторинга</span><span class="sxs-lookup"><span data-stu-id="ade45-110">Example 1: Update the Tags of a Dashboard</span></span>
```powershell
PS C:\> Update-AzPortalDashboard -ResourceGroupName my-rg -Name dashbase03 -Tag @{'hidden-title'="My Dashboard Title"; NewTag="NewValue"}

Location Name       Type
-------- ----       ----
eastasia dashbase03 Microsoft.Portal/dashboards
```

<span data-ttu-id="ade45-111">Обновив теги на панели мониторинга.</span><span class="sxs-lookup"><span data-stu-id="ade45-111">Update the tags in a dashboard.</span></span>
<span data-ttu-id="ade45-112">Теги представлены как вмещаемые.</span><span class="sxs-lookup"><span data-stu-id="ade45-112">Tags are represented as an inline hashtable.</span></span>

### <span data-ttu-id="ade45-113">Пример 2. Обновление тегов панели мониторинга с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="ade45-113">Example 2: Update Dashboard tags using the pipeline</span></span>
```powershell
PS C:\> Get-AzPortalDashboard -ResourceGroupName my-rg -Name dashbase03 | Update-AzPortalDashboard -Tag @{'hidden-title'="My Dashboard Title"; NewTag="NewValue"}

Location Name       Type
-------- ----       ----
eastasia dashbase03 Microsoft.Portal/dashboards
```

<span data-ttu-id="ade45-114">Обновите теги на панели мониторинга, искомые с помощью Get-AzPortalDashboard.</span><span class="sxs-lookup"><span data-stu-id="ade45-114">Update the Tags in a Dashboard retried using Get-AzPortalDashboard.</span></span>
<span data-ttu-id="ade45-115">Это может использоваться для обновления тегов на одной панели мониторинга или нескольких панелях мониторинга.</span><span class="sxs-lookup"><span data-stu-id="ade45-115">This can be used to update the tags over a single dashboard, or multiple dashboardfs.</span></span>

## <span data-ttu-id="ade45-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ade45-116">PARAMETERS</span></span>

### <span data-ttu-id="ade45-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ade45-117">-DefaultProfile</span></span>
<span data-ttu-id="ade45-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ade45-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ade45-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ade45-119">-InputObject</span></span>
<span data-ttu-id="ade45-120">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="ade45-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ade45-121">-Lens</span><span class="sxs-lookup"><span data-stu-id="ade45-121">-Lens</span></span>
<span data-ttu-id="ade45-122">Панели мониторинга.</span><span class="sxs-lookup"><span data-stu-id="ade45-122">The dashboard lenses.</span></span>

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

### <span data-ttu-id="ade45-123">-Метаданные</span><span class="sxs-lookup"><span data-stu-id="ade45-123">-Metadata</span></span>
<span data-ttu-id="ade45-124">Метаданные панели мониторинга.</span><span class="sxs-lookup"><span data-stu-id="ade45-124">The dashboard metadata.</span></span>

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

### <span data-ttu-id="ade45-125">-Name</span><span class="sxs-lookup"><span data-stu-id="ade45-125">-Name</span></span>
<span data-ttu-id="ade45-126">Имя панели мониторинга.</span><span class="sxs-lookup"><span data-stu-id="ade45-126">The name of the dashboard.</span></span>

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

### <span data-ttu-id="ade45-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ade45-127">-ResourceGroupName</span></span>
<span data-ttu-id="ade45-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ade45-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="ade45-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ade45-129">-SubscriptionId</span></span>
<span data-ttu-id="ade45-130">ИД подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="ade45-130">The Azure subscription ID.</span></span>
<span data-ttu-id="ade45-131">Строка в формате GUID (например, 00000000-0000-0000-0000-0000-00000000000000)</span><span class="sxs-lookup"><span data-stu-id="ade45-131">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="ade45-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="ade45-132">-Tag</span></span>
<span data-ttu-id="ade45-133">Теги ресурсов</span><span class="sxs-lookup"><span data-stu-id="ade45-133">Resource tags</span></span>

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

### <span data-ttu-id="ade45-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ade45-134">-Confirm</span></span>
<span data-ttu-id="ade45-135">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ade45-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ade45-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ade45-136">-WhatIf</span></span>
<span data-ttu-id="ade45-137">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ade45-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ade45-138">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="ade45-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ade45-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ade45-139">CommonParameters</span></span>
<span data-ttu-id="ade45-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ade45-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ade45-141">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ade45-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ade45-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ade45-142">INPUTS</span></span>

### <span data-ttu-id="ade45-143">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity</span><span class="sxs-lookup"><span data-stu-id="ade45-143">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity</span></span>

## <span data-ttu-id="ade45-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ade45-144">OUTPUTS</span></span>

### <span data-ttu-id="ade45-145">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span><span class="sxs-lookup"><span data-stu-id="ade45-145">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span></span>

## <span data-ttu-id="ade45-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ade45-146">NOTES</span></span>

<span data-ttu-id="ade45-147">ALIASES</span><span class="sxs-lookup"><span data-stu-id="ade45-147">ALIASES</span></span>

<span data-ttu-id="ade45-148">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="ade45-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ade45-149">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="ade45-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ade45-150">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ade45-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ade45-151">INPUTOBJECT <IPortalIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="ade45-151">INPUTOBJECT <IPortalIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ade45-152">`[DashboardName <String>]`: название панели мониторинга.</span><span class="sxs-lookup"><span data-stu-id="ade45-152">`[DashboardName <String>]`: The name of the dashboard.</span></span>
  - <span data-ttu-id="ade45-153">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="ade45-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ade45-154">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ade45-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="ade45-155">`[SubscriptionId <String>]`: ИД подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="ade45-155">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="ade45-156">Строка в формате GUID (например, 00000000-0000-0000-0000-0000-00000000000000)</span><span class="sxs-lookup"><span data-stu-id="ade45-156">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="ade45-157">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ade45-157">RELATED LINKS</span></span>

