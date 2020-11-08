---
external help file: ''
Module Name: Az.Portal
online version: https://docs.microsoft.com/en-us/powershell/module/az.portal/update-azportaldashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Update-AzPortalDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Update-AzPortalDashboard.md
ms.openlocfilehash: 42c5d90a24e671c47245ace0046c6f5987dbcd94
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244272"
---
# <span data-ttu-id="c7813-101">Update-AzPortalDashboard</span><span class="sxs-lookup"><span data-stu-id="c7813-101">Update-AzPortalDashboard</span></span>

## <span data-ttu-id="c7813-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c7813-102">SYNOPSIS</span></span>
<span data-ttu-id="c7813-103">Обновляет существующую панель мониторинга.</span><span class="sxs-lookup"><span data-stu-id="c7813-103">Updates an existing Dashboard.</span></span>

## <span data-ttu-id="c7813-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c7813-104">SYNTAX</span></span>

### <span data-ttu-id="c7813-105">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c7813-105">UpdateExpanded (Default)</span></span>
```
Update-AzPortalDashboard -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Lens <Hashtable>] [-Metadata <Hashtable>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c7813-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="c7813-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzPortalDashboard -InputObject <IPortalIdentity> [-Lens <Hashtable>] [-Metadata <Hashtable>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c7813-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c7813-107">DESCRIPTION</span></span>
<span data-ttu-id="c7813-108">Обновляет существующую панель мониторинга.</span><span class="sxs-lookup"><span data-stu-id="c7813-108">Updates an existing Dashboard.</span></span>

## <span data-ttu-id="c7813-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c7813-109">EXAMPLES</span></span>

### <span data-ttu-id="c7813-110">Пример 1: обновление тегов на панели мониторинга</span><span class="sxs-lookup"><span data-stu-id="c7813-110">Example 1: Update the Tags of a Dashboard</span></span>
```powershell
PS C:\> Update-AzPortalDashboard -ResourceGroupName my-rg -Name dashbase03 -Tag @{'hidden-title'="My Dashboard Title"; NewTag="NewValue"}

Location Name       Type
-------- ----       ----
eastasia dashbase03 Microsoft.Portal/dashboards
```

<span data-ttu-id="c7813-111">Обновите Теги на панели мониторинга.</span><span class="sxs-lookup"><span data-stu-id="c7813-111">Update the tags in a dashboard.</span></span>
<span data-ttu-id="c7813-112">Теги представлены в виде встроенной Hashtable.</span><span class="sxs-lookup"><span data-stu-id="c7813-112">Tags are represented as an inline hashtable.</span></span>

### <span data-ttu-id="c7813-113">Пример 2: обновление тегов панели мониторинга с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="c7813-113">Example 2: Update Dashboard tags using the pipeline</span></span>
```powershell
PS C:\> Get-AzPortalDashboard -ResourceGroupName my-rg -Name dashbase03 | Update-AzPortalDashboard -Tag @{'hidden-title'="My Dashboard Title"; NewTag="NewValue"}

Location Name       Type
-------- ----       ----
eastasia dashbase03 Microsoft.Portal/dashboards
```

<span data-ttu-id="c7813-114">Обновление тегов на панели мониторинга повторно выполнялось с помощью Get-AzPortalDashboard.</span><span class="sxs-lookup"><span data-stu-id="c7813-114">Update the Tags in a Dashboard retried using Get-AzPortalDashboard.</span></span>
<span data-ttu-id="c7813-115">Это можно использовать для обновления тегов на одной информационной панели или нескольких dashboardfs.</span><span class="sxs-lookup"><span data-stu-id="c7813-115">This can be used to update the tags over a single dashboard, or multiple dashboardfs.</span></span>

## <span data-ttu-id="c7813-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c7813-116">PARAMETERS</span></span>

### <span data-ttu-id="c7813-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7813-117">-DefaultProfile</span></span>
<span data-ttu-id="c7813-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c7813-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c7813-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c7813-119">-InputObject</span></span>
<span data-ttu-id="c7813-120">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="c7813-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="c7813-121">-Линза</span><span class="sxs-lookup"><span data-stu-id="c7813-121">-Lens</span></span>
<span data-ttu-id="c7813-122">Линзы панели мониторинга.</span><span class="sxs-lookup"><span data-stu-id="c7813-122">The dashboard lenses.</span></span>

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

### <span data-ttu-id="c7813-123">-Metadata</span><span class="sxs-lookup"><span data-stu-id="c7813-123">-Metadata</span></span>
<span data-ttu-id="c7813-124">Метаданные информационной панели.</span><span class="sxs-lookup"><span data-stu-id="c7813-124">The dashboard metadata.</span></span>

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

### <span data-ttu-id="c7813-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c7813-125">-Name</span></span>
<span data-ttu-id="c7813-126">Имя панели мониторинга.</span><span class="sxs-lookup"><span data-stu-id="c7813-126">The name of the dashboard.</span></span>

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

### <span data-ttu-id="c7813-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7813-127">-ResourceGroupName</span></span>
<span data-ttu-id="c7813-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c7813-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="c7813-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c7813-129">-SubscriptionId</span></span>
<span data-ttu-id="c7813-130">Идентификатор подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="c7813-130">The Azure subscription ID.</span></span>
<span data-ttu-id="c7813-131">Это строка в формате GUID (например, 00000000-0000-0000-0000-000000000000).</span><span class="sxs-lookup"><span data-stu-id="c7813-131">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="c7813-132">-Тег</span><span class="sxs-lookup"><span data-stu-id="c7813-132">-Tag</span></span>
<span data-ttu-id="c7813-133">Теги ресурсов</span><span class="sxs-lookup"><span data-stu-id="c7813-133">Resource tags</span></span>

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

### <span data-ttu-id="c7813-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c7813-134">-Confirm</span></span>
<span data-ttu-id="c7813-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c7813-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7813-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7813-136">-WhatIf</span></span>
<span data-ttu-id="c7813-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c7813-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c7813-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c7813-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7813-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7813-139">CommonParameters</span></span>
<span data-ttu-id="c7813-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c7813-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7813-141">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c7813-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7813-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c7813-142">INPUTS</span></span>

### <span data-ttu-id="c7813-143">Microsoft. Azure. PowerShell. командлеты. Portal. Models. IPortalIdentity</span><span class="sxs-lookup"><span data-stu-id="c7813-143">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity</span></span>

## <span data-ttu-id="c7813-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c7813-144">OUTPUTS</span></span>

### <span data-ttu-id="c7813-145">Microsoft. Azure. PowerShell. командлеты. Portal. Models. Api201901Preview. IDashboard</span><span class="sxs-lookup"><span data-stu-id="c7813-145">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span></span>

## <span data-ttu-id="c7813-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="c7813-146">NOTES</span></span>

<span data-ttu-id="c7813-147">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="c7813-147">ALIASES</span></span>

<span data-ttu-id="c7813-148">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="c7813-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c7813-149">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="c7813-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c7813-150">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c7813-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c7813-151">INPUTOBJECT <IPortalIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="c7813-151">INPUTOBJECT <IPortalIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c7813-152">`[DashboardName <String>]`: Имя панели мониторинга.</span><span class="sxs-lookup"><span data-stu-id="c7813-152">`[DashboardName <String>]`: The name of the dashboard.</span></span>
  - <span data-ttu-id="c7813-153">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="c7813-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c7813-154">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c7813-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="c7813-155">`[SubscriptionId <String>]`: Идентификатор подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="c7813-155">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="c7813-156">Это строка в формате GUID (например, 00000000-0000-0000-0000-000000000000).</span><span class="sxs-lookup"><span data-stu-id="c7813-156">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="c7813-157">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c7813-157">RELATED LINKS</span></span>

