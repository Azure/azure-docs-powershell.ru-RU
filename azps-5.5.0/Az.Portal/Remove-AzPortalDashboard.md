---
external help file: ''
Module Name: Az.Portal
online version: https://docs.microsoft.com/en-us/powershell/module/az.portal/remove-azportaldashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Remove-AzPortalDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Remove-AzPortalDashboard.md
ms.openlocfilehash: f0ef681f09caf43ac2f2100d1a30af19b1b3c364
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100213233"
---
# <span data-ttu-id="30f98-101">Remove-AzPortalDashboard</span><span class="sxs-lookup"><span data-stu-id="30f98-101">Remove-AzPortalDashboard</span></span>

## <span data-ttu-id="30f98-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30f98-102">SYNOPSIS</span></span>
<span data-ttu-id="30f98-103">Удаляет информационную панель.</span><span class="sxs-lookup"><span data-stu-id="30f98-103">Deletes the Dashboard.</span></span>

## <span data-ttu-id="30f98-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="30f98-104">SYNTAX</span></span>

### <span data-ttu-id="30f98-105">Delete (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="30f98-105">Delete (Default)</span></span>
```
Remove-AzPortalDashboard -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="30f98-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="30f98-106">DeleteViaIdentity</span></span>
```
Remove-AzPortalDashboard -InputObject <IPortalIdentity> [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="30f98-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="30f98-107">DESCRIPTION</span></span>
<span data-ttu-id="30f98-108">Удаляет информационную панель.</span><span class="sxs-lookup"><span data-stu-id="30f98-108">Deletes the Dashboard.</span></span>

## <span data-ttu-id="30f98-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="30f98-109">EXAMPLES</span></span>

### <span data-ttu-id="30f98-110">Пример 1. Удаление панели мониторинга</span><span class="sxs-lookup"><span data-stu-id="30f98-110">Example 1: Remove a Dashboard</span></span>
```powershell
PS C:\td\> Remove-AzPortalDashboard -ResourceGroupName my-rg -DashboardName dashbase02
```

<span data-ttu-id="30f98-111">Удалите штриховую панель с помощью имени группы ресурсов и имени панели мониторинга.</span><span class="sxs-lookup"><span data-stu-id="30f98-111">Remove a Dashbaord using resource group name and dashboard name.</span></span>

### <span data-ttu-id="30f98-112">Пример 2. Удаление панели мониторинга с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="30f98-112">Example 2: Remove a Dashboard using the pipeline</span></span>
```powershell
PS C:\> Get-AzPortalDashboard -ResourceGroupName my-rg -DashboardName dashbase02 | Remove-AzPortalDashboard
```

<span data-ttu-id="30f98-113">Удалите панель мониторинга, возвращенную из Get-AzDashboard звонка.</span><span class="sxs-lookup"><span data-stu-id="30f98-113">Remove the dashboard returned from a Get-AzDashboard call.</span></span>

## <span data-ttu-id="30f98-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="30f98-114">PARAMETERS</span></span>

### <span data-ttu-id="30f98-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30f98-115">-DefaultProfile</span></span>
<span data-ttu-id="30f98-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="30f98-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="30f98-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="30f98-117">-InputObject</span></span>
<span data-ttu-id="30f98-118">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="30f98-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="30f98-119">-Name</span><span class="sxs-lookup"><span data-stu-id="30f98-119">-Name</span></span>
<span data-ttu-id="30f98-120">Имя панели мониторинга.</span><span class="sxs-lookup"><span data-stu-id="30f98-120">The name of the dashboard.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: DashboardName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30f98-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="30f98-121">-PassThru</span></span>
<span data-ttu-id="30f98-122">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="30f98-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="30f98-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30f98-123">-ResourceGroupName</span></span>
<span data-ttu-id="30f98-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="30f98-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="30f98-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="30f98-125">-SubscriptionId</span></span>
<span data-ttu-id="30f98-126">ИД подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="30f98-126">The Azure subscription ID.</span></span>
<span data-ttu-id="30f98-127">Строка в формате GUID (например, 00000000-0000-0000-0000-0000-00000000000000)</span><span class="sxs-lookup"><span data-stu-id="30f98-127">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="30f98-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="30f98-128">-Confirm</span></span>
<span data-ttu-id="30f98-129">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="30f98-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30f98-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30f98-130">-WhatIf</span></span>
<span data-ttu-id="30f98-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="30f98-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="30f98-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="30f98-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30f98-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30f98-133">CommonParameters</span></span>
<span data-ttu-id="30f98-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30f98-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30f98-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="30f98-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30f98-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="30f98-136">INPUTS</span></span>

### <span data-ttu-id="30f98-137">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity</span><span class="sxs-lookup"><span data-stu-id="30f98-137">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity</span></span>

## <span data-ttu-id="30f98-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="30f98-138">OUTPUTS</span></span>

### <span data-ttu-id="30f98-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="30f98-139">System.Boolean</span></span>

## <span data-ttu-id="30f98-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="30f98-140">NOTES</span></span>

<span data-ttu-id="30f98-141">ALIASES</span><span class="sxs-lookup"><span data-stu-id="30f98-141">ALIASES</span></span>

<span data-ttu-id="30f98-142">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="30f98-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="30f98-143">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="30f98-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="30f98-144">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="30f98-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="30f98-145">INPUTOBJECT <IPortalIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="30f98-145">INPUTOBJECT <IPortalIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="30f98-146">`[DashboardName <String>]`: имя панели мониторинга.</span><span class="sxs-lookup"><span data-stu-id="30f98-146">`[DashboardName <String>]`: The name of the dashboard.</span></span>
  - <span data-ttu-id="30f98-147">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="30f98-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="30f98-148">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="30f98-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="30f98-149">`[SubscriptionId <String>]`: ИД подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="30f98-149">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="30f98-150">Строка в формате GUID (например, 00000000-0000-0000-0000-0000-00000000000000)</span><span class="sxs-lookup"><span data-stu-id="30f98-150">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="30f98-151">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="30f98-151">RELATED LINKS</span></span>

