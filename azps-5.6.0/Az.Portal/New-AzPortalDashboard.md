---
external help file: ''
Module Name: Az.Portal
online version: https://docs.microsoft.com/powershell/module/az.portal/new-azportaldashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/New-AzPortalDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/New-AzPortalDashboard.md
ms.openlocfilehash: 05627146c0b9984ea5222f70f85f801b374e1321
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988994"
---
# <span data-ttu-id="3f364-101">New-AzPortalDashboard</span><span class="sxs-lookup"><span data-stu-id="3f364-101">New-AzPortalDashboard</span></span>

## <span data-ttu-id="3f364-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3f364-102">SYNOPSIS</span></span>
<span data-ttu-id="3f364-103">Создает или обновляет информационную панель.</span><span class="sxs-lookup"><span data-stu-id="3f364-103">Creates or updates a Dashboard.</span></span>

## <span data-ttu-id="3f364-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3f364-104">SYNTAX</span></span>

### <span data-ttu-id="3f364-105">CreateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3f364-105">CreateExpanded (Default)</span></span>
```
New-AzPortalDashboard -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-Lens <Hashtable>] [-Metadata <Hashtable>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3f364-106">"Создать"</span><span class="sxs-lookup"><span data-stu-id="3f364-106">Create</span></span>
```
New-AzPortalDashboard -Name <String> -ResourceGroupName <String> -Dashboard <IDashboard>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3f364-107">CreateByFile</span><span class="sxs-lookup"><span data-stu-id="3f364-107">CreateByFile</span></span>
```
New-AzPortalDashboard -Name <String> -ResourceGroupName <String> -DashboardPath <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3f364-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3f364-108">DESCRIPTION</span></span>
<span data-ttu-id="3f364-109">Создает или обновляет информационную панель.</span><span class="sxs-lookup"><span data-stu-id="3f364-109">Creates or updates a Dashboard.</span></span>

## <span data-ttu-id="3f364-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3f364-110">EXAMPLES</span></span>

### <span data-ttu-id="3f364-111">Пример 1. Создание панели мониторинга с помощью файла шаблона панели мониторинга</span><span class="sxs-lookup"><span data-stu-id="3f364-111">Example 1: Create a dashboard using a dashboard template file</span></span>
```powershell
PS C:\> New-AzPortalDashboard -DashboardPath .\resources\dash1.json -ResourceGroupName mydash-rg -DashboardName my-dashboard03

Location Name           Type
-------- ----           ----
eastasia my-dashboard03 Microsoft.Portal/dashboards
```

<span data-ttu-id="3f364-112">Создайте панель мониторинга, используя предоставленный файл шаблона панели мониторинга.</span><span class="sxs-lookup"><span data-stu-id="3f364-112">Create a new dashboard using the provided dashboard template file.</span></span>

## <span data-ttu-id="3f364-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3f364-113">PARAMETERS</span></span>

### <span data-ttu-id="3f364-114">-Dashboard</span><span class="sxs-lookup"><span data-stu-id="3f364-114">-Dashboard</span></span>
<span data-ttu-id="3f364-115">Определение ресурса общей панели мониторинга.</span><span class="sxs-lookup"><span data-stu-id="3f364-115">The shared dashboard resource definition.</span></span>
<span data-ttu-id="3f364-116">Чтобы построить новую таблицу, см. раздел "ЗАМЕТКИ" для свойств панели мониторинга и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="3f364-116">To construct, see NOTES section for DASHBOARD properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard
Parameter Sets: Create
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3f364-117">-DashboardPath</span><span class="sxs-lookup"><span data-stu-id="3f364-117">-DashboardPath</span></span>
<span data-ttu-id="3f364-118">Путь к существующему шаблону панели мониторинга.</span><span class="sxs-lookup"><span data-stu-id="3f364-118">The Path to an existing dashboard template.</span></span>
<span data-ttu-id="3f364-119">Шаблоны панелей мониторинга можно скачать с портала.</span><span class="sxs-lookup"><span data-stu-id="3f364-119">Dashboard templates may be downloaded from the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f364-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f364-120">-DefaultProfile</span></span>
<span data-ttu-id="3f364-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3f364-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f364-122">-Lens</span><span class="sxs-lookup"><span data-stu-id="3f364-122">-Lens</span></span>
<span data-ttu-id="3f364-123">Панели мониторинга.</span><span class="sxs-lookup"><span data-stu-id="3f364-123">The dashboard lenses.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f364-124">-Location</span><span class="sxs-lookup"><span data-stu-id="3f364-124">-Location</span></span>
<span data-ttu-id="3f364-125">Расположение ресурса</span><span class="sxs-lookup"><span data-stu-id="3f364-125">Resource location</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f364-126">-Метаданные</span><span class="sxs-lookup"><span data-stu-id="3f364-126">-Metadata</span></span>
<span data-ttu-id="3f364-127">Метаданные панели мониторинга.</span><span class="sxs-lookup"><span data-stu-id="3f364-127">The dashboard metadata.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f364-128">-Name</span><span class="sxs-lookup"><span data-stu-id="3f364-128">-Name</span></span>
<span data-ttu-id="3f364-129">Имя панели мониторинга.</span><span class="sxs-lookup"><span data-stu-id="3f364-129">The name of the dashboard.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DashboardName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f364-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f364-130">-ResourceGroupName</span></span>
<span data-ttu-id="3f364-131">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3f364-131">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f364-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3f364-132">-SubscriptionId</span></span>
<span data-ttu-id="3f364-133">ИД подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="3f364-133">The Azure subscription ID.</span></span>
<span data-ttu-id="3f364-134">Строка в формате GUID (например, 00000000-0000-0000-0000-0000-00000000000000)</span><span class="sxs-lookup"><span data-stu-id="3f364-134">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f364-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="3f364-135">-Tag</span></span>
<span data-ttu-id="3f364-136">Теги ресурсов</span><span class="sxs-lookup"><span data-stu-id="3f364-136">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f364-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3f364-137">-Confirm</span></span>
<span data-ttu-id="3f364-138">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="3f364-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f364-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f364-139">-WhatIf</span></span>
<span data-ttu-id="3f364-140">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3f364-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3f364-141">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="3f364-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f364-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f364-142">CommonParameters</span></span>
<span data-ttu-id="3f364-143">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f364-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f364-144">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3f364-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f364-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3f364-145">INPUTS</span></span>

### <span data-ttu-id="3f364-146">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span><span class="sxs-lookup"><span data-stu-id="3f364-146">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span></span>

## <span data-ttu-id="3f364-147">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3f364-147">OUTPUTS</span></span>

### <span data-ttu-id="3f364-148">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span><span class="sxs-lookup"><span data-stu-id="3f364-148">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span></span>

## <span data-ttu-id="3f364-149">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3f364-149">NOTES</span></span>

<span data-ttu-id="3f364-150">ALIASES</span><span class="sxs-lookup"><span data-stu-id="3f364-150">ALIASES</span></span>

<span data-ttu-id="3f364-151">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="3f364-151">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3f364-152">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="3f364-152">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3f364-153">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3f364-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3f364-154">ИНФОРМАЦИОННАЯ <IDashboard> ПАНЕЛЬ: определение ресурса общей панели мониторинга.</span><span class="sxs-lookup"><span data-stu-id="3f364-154">DASHBOARD <IDashboard>: The shared dashboard resource definition.</span></span>
  - <span data-ttu-id="3f364-155">`Location <String>`: расположение ресурса</span><span class="sxs-lookup"><span data-stu-id="3f364-155">`Location <String>`: Resource location</span></span>
  - <span data-ttu-id="3f364-156">`[Lens <IDashboardPropertiesLenses>]`. Панели мониторинга.</span><span class="sxs-lookup"><span data-stu-id="3f364-156">`[Lens <IDashboardPropertiesLenses>]`: The dashboard lenses.</span></span>
    - <span data-ttu-id="3f364-157">`[(Any) <IDashboardLens>]`— это означает, что к этому объекту можно добавить любое свойство.</span><span class="sxs-lookup"><span data-stu-id="3f364-157">`[(Any) <IDashboardLens>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="3f364-158">`[Metadata <IDashboardPropertiesMetadata>]`. Метаданные панели мониторинга.</span><span class="sxs-lookup"><span data-stu-id="3f364-158">`[Metadata <IDashboardPropertiesMetadata>]`: The dashboard metadata.</span></span>
    - <span data-ttu-id="3f364-159">`[(Any) <Object>]`— это означает, что к этому объекту можно добавить любое свойство.</span><span class="sxs-lookup"><span data-stu-id="3f364-159">`[(Any) <Object>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="3f364-160">`[Tag <IDashboardTags>]`: теги ресурсов</span><span class="sxs-lookup"><span data-stu-id="3f364-160">`[Tag <IDashboardTags>]`: Resource tags</span></span>
    - <span data-ttu-id="3f364-161">`[(Any) <String>]`— это означает, что к этому объекту можно добавить любое свойство.</span><span class="sxs-lookup"><span data-stu-id="3f364-161">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>

## <span data-ttu-id="3f364-162">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3f364-162">RELATED LINKS</span></span>

