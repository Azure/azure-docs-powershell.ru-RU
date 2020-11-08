---
external help file: ''
Module Name: Az.Portal
online version: https://docs.microsoft.com/en-us/powershell/module/az.portal/new-azportaldashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/New-AzPortalDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/New-AzPortalDashboard.md
ms.openlocfilehash: 80b2289b4f481fff126d9cd5dfc98ca94536cfa0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244280"
---
# <span data-ttu-id="59692-101">New-AzPortalDashboard</span><span class="sxs-lookup"><span data-stu-id="59692-101">New-AzPortalDashboard</span></span>

## <span data-ttu-id="59692-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="59692-102">SYNOPSIS</span></span>
<span data-ttu-id="59692-103">Создание или обновление информационной панели.</span><span class="sxs-lookup"><span data-stu-id="59692-103">Creates or updates a Dashboard.</span></span>

## <span data-ttu-id="59692-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="59692-104">SYNTAX</span></span>

### <span data-ttu-id="59692-105">CreateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="59692-105">CreateExpanded (Default)</span></span>
```
New-AzPortalDashboard -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-Lens <Hashtable>] [-Metadata <Hashtable>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="59692-106">Заново</span><span class="sxs-lookup"><span data-stu-id="59692-106">Create</span></span>
```
New-AzPortalDashboard -Name <String> -ResourceGroupName <String> -Dashboard <IDashboard>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="59692-107">CreateByFile</span><span class="sxs-lookup"><span data-stu-id="59692-107">CreateByFile</span></span>
```
New-AzPortalDashboard -Name <String> -ResourceGroupName <String> -DashboardPath <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="59692-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="59692-108">DESCRIPTION</span></span>
<span data-ttu-id="59692-109">Создание или обновление информационной панели.</span><span class="sxs-lookup"><span data-stu-id="59692-109">Creates or updates a Dashboard.</span></span>

## <span data-ttu-id="59692-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="59692-110">EXAMPLES</span></span>

### <span data-ttu-id="59692-111">Пример 1: Создание панели мониторинга с помощью файла шаблона панели мониторинга</span><span class="sxs-lookup"><span data-stu-id="59692-111">Example 1: Create a dashboard using a dashboard template file</span></span>
```powershell
PS C:\> New-AzPortalDashboard -DashboardPath .\resources\dash1.json -ResourceGroupName mydash-rg -DashboardName my-dashboard03

Location Name           Type
-------- ----           ----
eastasia my-dashboard03 Microsoft.Portal/dashboards
```

<span data-ttu-id="59692-112">Создание панели мониторинга с помощью указанного файла шаблона панели мониторинга.</span><span class="sxs-lookup"><span data-stu-id="59692-112">Create a new dashboard using the provided dashboard template file.</span></span>

## <span data-ttu-id="59692-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="59692-113">PARAMETERS</span></span>

### <span data-ttu-id="59692-114">-Панель мониторинга</span><span class="sxs-lookup"><span data-stu-id="59692-114">-Dashboard</span></span>
<span data-ttu-id="59692-115">Определение ресурса общей панели мониторинга.</span><span class="sxs-lookup"><span data-stu-id="59692-115">The shared dashboard resource definition.</span></span>
<span data-ttu-id="59692-116">Для конструирования просмотрите раздел "Заметки" для свойств панели мониторинга и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="59692-116">To construct, see NOTES section for DASHBOARD properties and create a hash table.</span></span>

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

### <span data-ttu-id="59692-117">-DashboardPath</span><span class="sxs-lookup"><span data-stu-id="59692-117">-DashboardPath</span></span>
<span data-ttu-id="59692-118">Путь к существующему шаблону панели мониторинга.</span><span class="sxs-lookup"><span data-stu-id="59692-118">The Path to an existing dashboard template.</span></span>
<span data-ttu-id="59692-119">Шаблоны панели мониторинга можно загрузить с портала.</span><span class="sxs-lookup"><span data-stu-id="59692-119">Dashboard templates may be downloaded from the portal.</span></span>

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

### <span data-ttu-id="59692-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59692-120">-DefaultProfile</span></span>
<span data-ttu-id="59692-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="59692-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59692-122">-Линза</span><span class="sxs-lookup"><span data-stu-id="59692-122">-Lens</span></span>
<span data-ttu-id="59692-123">Линзы панели мониторинга.</span><span class="sxs-lookup"><span data-stu-id="59692-123">The dashboard lenses.</span></span>

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

### <span data-ttu-id="59692-124">-Location</span><span class="sxs-lookup"><span data-stu-id="59692-124">-Location</span></span>
<span data-ttu-id="59692-125">Расположение ресурса</span><span class="sxs-lookup"><span data-stu-id="59692-125">Resource location</span></span>

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

### <span data-ttu-id="59692-126">-Metadata</span><span class="sxs-lookup"><span data-stu-id="59692-126">-Metadata</span></span>
<span data-ttu-id="59692-127">Метаданные информационной панели.</span><span class="sxs-lookup"><span data-stu-id="59692-127">The dashboard metadata.</span></span>

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

### <span data-ttu-id="59692-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="59692-128">-Name</span></span>
<span data-ttu-id="59692-129">Имя панели мониторинга.</span><span class="sxs-lookup"><span data-stu-id="59692-129">The name of the dashboard.</span></span>

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

### <span data-ttu-id="59692-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59692-130">-ResourceGroupName</span></span>
<span data-ttu-id="59692-131">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="59692-131">The name of the resource group.</span></span>

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

### <span data-ttu-id="59692-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="59692-132">-SubscriptionId</span></span>
<span data-ttu-id="59692-133">Идентификатор подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="59692-133">The Azure subscription ID.</span></span>
<span data-ttu-id="59692-134">Это строка в формате GUID (например, 00000000-0000-0000-0000-000000000000).</span><span class="sxs-lookup"><span data-stu-id="59692-134">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="59692-135">-Тег</span><span class="sxs-lookup"><span data-stu-id="59692-135">-Tag</span></span>
<span data-ttu-id="59692-136">Теги ресурсов</span><span class="sxs-lookup"><span data-stu-id="59692-136">Resource tags</span></span>

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

### <span data-ttu-id="59692-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="59692-137">-Confirm</span></span>
<span data-ttu-id="59692-138">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="59692-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59692-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59692-139">-WhatIf</span></span>
<span data-ttu-id="59692-140">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="59692-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59692-141">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="59692-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59692-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59692-142">CommonParameters</span></span>
<span data-ttu-id="59692-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="59692-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59692-144">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="59692-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59692-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="59692-145">INPUTS</span></span>

### <span data-ttu-id="59692-146">Microsoft. Azure. PowerShell. командлеты. Portal. Models. Api201901Preview. IDashboard</span><span class="sxs-lookup"><span data-stu-id="59692-146">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span></span>

## <span data-ttu-id="59692-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="59692-147">OUTPUTS</span></span>

### <span data-ttu-id="59692-148">Microsoft. Azure. PowerShell. командлеты. Portal. Models. Api201901Preview. IDashboard</span><span class="sxs-lookup"><span data-stu-id="59692-148">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span></span>

## <span data-ttu-id="59692-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="59692-149">NOTES</span></span>

<span data-ttu-id="59692-150">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="59692-150">ALIASES</span></span>

<span data-ttu-id="59692-151">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="59692-151">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="59692-152">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="59692-152">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="59692-153">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="59692-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="59692-154">ИНФОРМАЦИОНная панель <IDashboard> : определение ресурса общей панели мониторинга.</span><span class="sxs-lookup"><span data-stu-id="59692-154">DASHBOARD <IDashboard>: The shared dashboard resource definition.</span></span>
  - <span data-ttu-id="59692-155">`Location <String>`: Расположение ресурса</span><span class="sxs-lookup"><span data-stu-id="59692-155">`Location <String>`: Resource location</span></span>
  - <span data-ttu-id="59692-156">`[Lens <IDashboardPropertiesLenses>]`: Линзы панели мониторинга.</span><span class="sxs-lookup"><span data-stu-id="59692-156">`[Lens <IDashboardPropertiesLenses>]`: The dashboard lenses.</span></span>
    - <span data-ttu-id="59692-157">`[(Any) <IDashboardLens>]`: Это указывает на то, что в этот объект можно добавить любое свойство.</span><span class="sxs-lookup"><span data-stu-id="59692-157">`[(Any) <IDashboardLens>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="59692-158">`[Metadata <IDashboardPropertiesMetadata>]`: Метаданные информационной панели.</span><span class="sxs-lookup"><span data-stu-id="59692-158">`[Metadata <IDashboardPropertiesMetadata>]`: The dashboard metadata.</span></span>
    - <span data-ttu-id="59692-159">`[(Any) <Object>]`: Это указывает на то, что в этот объект можно добавить любое свойство.</span><span class="sxs-lookup"><span data-stu-id="59692-159">`[(Any) <Object>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="59692-160">`[Tag <IDashboardTags>]`: Теги ресурсов</span><span class="sxs-lookup"><span data-stu-id="59692-160">`[Tag <IDashboardTags>]`: Resource tags</span></span>
    - <span data-ttu-id="59692-161">`[(Any) <String>]`: Это указывает на то, что в этот объект можно добавить любое свойство.</span><span class="sxs-lookup"><span data-stu-id="59692-161">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>

## <span data-ttu-id="59692-162">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="59692-162">RELATED LINKS</span></span>

