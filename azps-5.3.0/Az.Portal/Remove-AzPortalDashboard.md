---
external help file: ''
Module Name: Az.Portal
online version: https://docs.microsoft.com/en-us/powershell/module/az.portal/remove-azportaldashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Remove-AzPortalDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Remove-AzPortalDashboard.md
ms.openlocfilehash: f0ef681f09caf43ac2f2100d1a30af19b1b3c364
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506033"
---
# <span data-ttu-id="db293-101">Remove-AzPortalDashboard</span><span class="sxs-lookup"><span data-stu-id="db293-101">Remove-AzPortalDashboard</span></span>

## <span data-ttu-id="db293-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="db293-102">SYNOPSIS</span></span>
<span data-ttu-id="db293-103">Удаляет информационную панель.</span><span class="sxs-lookup"><span data-stu-id="db293-103">Deletes the Dashboard.</span></span>

## <span data-ttu-id="db293-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="db293-104">SYNTAX</span></span>

### <span data-ttu-id="db293-105">Delete (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="db293-105">Delete (Default)</span></span>
```
Remove-AzPortalDashboard -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="db293-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="db293-106">DeleteViaIdentity</span></span>
```
Remove-AzPortalDashboard -InputObject <IPortalIdentity> [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="db293-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="db293-107">DESCRIPTION</span></span>
<span data-ttu-id="db293-108">Удаляет информационную панель.</span><span class="sxs-lookup"><span data-stu-id="db293-108">Deletes the Dashboard.</span></span>

## <span data-ttu-id="db293-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="db293-109">EXAMPLES</span></span>

### <span data-ttu-id="db293-110">Пример 1. Удаление панели мониторинга</span><span class="sxs-lookup"><span data-stu-id="db293-110">Example 1: Remove a Dashboard</span></span>
```powershell
PS C:\td\> Remove-AzPortalDashboard -ResourceGroupName my-rg -DashboardName dashbase02
```

<span data-ttu-id="db293-111">Удалите штриховую панель с помощью имени группы ресурсов и имени панели мониторинга.</span><span class="sxs-lookup"><span data-stu-id="db293-111">Remove a Dashbaord using resource group name and dashboard name.</span></span>

### <span data-ttu-id="db293-112">Пример 2. Удаление панели мониторинга с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="db293-112">Example 2: Remove a Dashboard using the pipeline</span></span>
```powershell
PS C:\> Get-AzPortalDashboard -ResourceGroupName my-rg -DashboardName dashbase02 | Remove-AzPortalDashboard
```

<span data-ttu-id="db293-113">Удалите панель мониторинга, возвращенную из Get-AzDashboard звонка.</span><span class="sxs-lookup"><span data-stu-id="db293-113">Remove the dashboard returned from a Get-AzDashboard call.</span></span>

## <span data-ttu-id="db293-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="db293-114">PARAMETERS</span></span>

### <span data-ttu-id="db293-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db293-115">-DefaultProfile</span></span>
<span data-ttu-id="db293-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="db293-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db293-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="db293-117">-InputObject</span></span>
<span data-ttu-id="db293-118">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="db293-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="db293-119">-Name</span><span class="sxs-lookup"><span data-stu-id="db293-119">-Name</span></span>
<span data-ttu-id="db293-120">Имя панели мониторинга.</span><span class="sxs-lookup"><span data-stu-id="db293-120">The name of the dashboard.</span></span>

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

### <span data-ttu-id="db293-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="db293-121">-PassThru</span></span>
<span data-ttu-id="db293-122">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="db293-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="db293-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db293-123">-ResourceGroupName</span></span>
<span data-ttu-id="db293-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="db293-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="db293-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="db293-125">-SubscriptionId</span></span>
<span data-ttu-id="db293-126">ИД подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="db293-126">The Azure subscription ID.</span></span>
<span data-ttu-id="db293-127">Строка в формате GUID (например, 00000000-0000-0000-0000-0000-00000000000000)</span><span class="sxs-lookup"><span data-stu-id="db293-127">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="db293-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="db293-128">-Confirm</span></span>
<span data-ttu-id="db293-129">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="db293-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db293-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db293-130">-WhatIf</span></span>
<span data-ttu-id="db293-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="db293-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db293-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="db293-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db293-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db293-133">CommonParameters</span></span>
<span data-ttu-id="db293-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db293-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db293-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="db293-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db293-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="db293-136">INPUTS</span></span>

### <span data-ttu-id="db293-137">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity</span><span class="sxs-lookup"><span data-stu-id="db293-137">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity</span></span>

## <span data-ttu-id="db293-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="db293-138">OUTPUTS</span></span>

### <span data-ttu-id="db293-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="db293-139">System.Boolean</span></span>

## <span data-ttu-id="db293-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="db293-140">NOTES</span></span>

<span data-ttu-id="db293-141">ALIASES</span><span class="sxs-lookup"><span data-stu-id="db293-141">ALIASES</span></span>

<span data-ttu-id="db293-142">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="db293-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="db293-143">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="db293-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="db293-144">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="db293-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="db293-145">INPUTOBJECT <IPortalIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="db293-145">INPUTOBJECT <IPortalIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="db293-146">`[DashboardName <String>]`: имя панели мониторинга.</span><span class="sxs-lookup"><span data-stu-id="db293-146">`[DashboardName <String>]`: The name of the dashboard.</span></span>
  - <span data-ttu-id="db293-147">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="db293-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="db293-148">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="db293-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="db293-149">`[SubscriptionId <String>]`: ИД подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="db293-149">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="db293-150">Строка в формате GUID (например, 00000000-0000-0000-0000-0000-00000000000000)</span><span class="sxs-lookup"><span data-stu-id="db293-150">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="db293-151">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="db293-151">RELATED LINKS</span></span>

