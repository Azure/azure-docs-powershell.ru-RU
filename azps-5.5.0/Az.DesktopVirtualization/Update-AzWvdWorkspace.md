---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvdworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdWorkspace.md
ms.openlocfilehash: 8a20777cfd6e28c3edc127117687b7aef801d94e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100243776"
---
# <span data-ttu-id="1925c-101">Update-AzWvdWorkspace</span><span class="sxs-lookup"><span data-stu-id="1925c-101">Update-AzWvdWorkspace</span></span>

## <span data-ttu-id="1925c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1925c-102">SYNOPSIS</span></span>
<span data-ttu-id="1925c-103">Обновление рабочей области.</span><span class="sxs-lookup"><span data-stu-id="1925c-103">Update a workspace.</span></span>

## <span data-ttu-id="1925c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1925c-104">SYNTAX</span></span>

### <span data-ttu-id="1925c-105">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1925c-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdWorkspace -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-ApplicationGroupReference <String[]>] [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="1925c-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="1925c-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdWorkspace -InputObject <IDesktopVirtualizationIdentity> [-ApplicationGroupReference <String[]>]
 [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1925c-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1925c-107">DESCRIPTION</span></span>
<span data-ttu-id="1925c-108">Обновление рабочей области.</span><span class="sxs-lookup"><span data-stu-id="1925c-108">Update a workspace.</span></span>

## <span data-ttu-id="1925c-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1925c-109">EXAMPLES</span></span>

### <span data-ttu-id="1925c-110">Пример 1. Обновление по имени виртуальной рабочей области рабочего стола Windows</span><span class="sxs-lookup"><span data-stu-id="1925c-110">Example 1: Update a Windows Virtual Desktop Workspace by name</span></span>
```powershell
PS C:\> Update-AzWvdWorkspace -ResourceGroupName ResourceGroupName `
                        -Name WorkspaceName `
                        -FriendlyName 'Friendly Name' `
                        -ApplicationGroupReference "/subscriptions/SubscriptionId/resourceGroups/ResourceGroupName/providers/Microsoft.DesktopVirtualization/applicationGroups/ApplicationGroupName1","/subscriptions/SubscriptionId/resourceGroups/ResourceGroupName/providers/Microsoft.DesktopVirtualization/applicationGroups/ApplicationGroupName2" `
                        -Description 'Description'

Location   Name                 Type
--------   ----                 ----
eastus     WorkspaceName Microsoft.DesktopVirtualization/workspaces
```

<span data-ttu-id="1925c-111">Эта команда обновляет рабочее пространство Виртуального рабочего стола Windows в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1925c-111">This command updates a Windows Virtual Desktop Workspace in a Resource Group.</span></span>

## <span data-ttu-id="1925c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1925c-112">PARAMETERS</span></span>

### <span data-ttu-id="1925c-113">-ApplicationGroupReference</span><span class="sxs-lookup"><span data-stu-id="1925c-113">-ApplicationGroupReference</span></span>
<span data-ttu-id="1925c-114">Список ссылок applicationGroup.</span><span class="sxs-lookup"><span data-stu-id="1925c-114">List of applicationGroup links.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1925c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1925c-115">-DefaultProfile</span></span>
<span data-ttu-id="1925c-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1925c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1925c-117">-Description</span><span class="sxs-lookup"><span data-stu-id="1925c-117">-Description</span></span>
<span data-ttu-id="1925c-118">Описание рабочей области.</span><span class="sxs-lookup"><span data-stu-id="1925c-118">Description of Workspace.</span></span>

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

### <span data-ttu-id="1925c-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="1925c-119">-FriendlyName</span></span>
<span data-ttu-id="1925c-120">Имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="1925c-120">Friendly name of Workspace.</span></span>

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

### <span data-ttu-id="1925c-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1925c-121">-InputObject</span></span>
<span data-ttu-id="1925c-122">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="1925c-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1925c-123">-Name</span><span class="sxs-lookup"><span data-stu-id="1925c-123">-Name</span></span>
<span data-ttu-id="1925c-124">Имя рабочей области</span><span class="sxs-lookup"><span data-stu-id="1925c-124">The name of the workspace</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: WorkspaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1925c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1925c-125">-ResourceGroupName</span></span>
<span data-ttu-id="1925c-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1925c-126">The name of the resource group.</span></span>
<span data-ttu-id="1925c-127">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="1925c-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="1925c-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1925c-128">-SubscriptionId</span></span>
<span data-ttu-id="1925c-129">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="1925c-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="1925c-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="1925c-130">-Tag</span></span>
<span data-ttu-id="1925c-131">теги для обновления</span><span class="sxs-lookup"><span data-stu-id="1925c-131">tags to be updated</span></span>

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

### <span data-ttu-id="1925c-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1925c-132">-Confirm</span></span>
<span data-ttu-id="1925c-133">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1925c-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1925c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1925c-134">-WhatIf</span></span>
<span data-ttu-id="1925c-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1925c-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1925c-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="1925c-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1925c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1925c-137">CommonParameters</span></span>
<span data-ttu-id="1925c-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1925c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1925c-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1925c-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1925c-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1925c-140">INPUTS</span></span>

### <span data-ttu-id="1925c-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="1925c-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="1925c-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1925c-142">OUTPUTS</span></span>

### <span data-ttu-id="1925c-143">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IWorkspace</span><span class="sxs-lookup"><span data-stu-id="1925c-143">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IWorkspace</span></span>

## <span data-ttu-id="1925c-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1925c-144">NOTES</span></span>

<span data-ttu-id="1925c-145">ALIASES</span><span class="sxs-lookup"><span data-stu-id="1925c-145">ALIASES</span></span>

<span data-ttu-id="1925c-146">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="1925c-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1925c-147">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="1925c-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1925c-148">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="1925c-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1925c-149">INPUTOBJECT <IDesktopVirtualizationIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="1925c-149">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1925c-150">`[ApplicationGroupName <String>]`: имя группы приложений</span><span class="sxs-lookup"><span data-stu-id="1925c-150">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="1925c-151">`[ApplicationName <String>]`: имя приложения в указанной группе приложений</span><span class="sxs-lookup"><span data-stu-id="1925c-151">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="1925c-152">`[DesktopName <String>]`: имя рабочего стола в указанной группе рабочего стола</span><span class="sxs-lookup"><span data-stu-id="1925c-152">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="1925c-153">`[HostPoolName <String>]`: имя пула хостов в указанной группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="1925c-153">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="1925c-154">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="1925c-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1925c-155">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span><span class="sxs-lookup"><span data-stu-id="1925c-155">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="1925c-156">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1925c-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="1925c-157">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="1925c-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="1925c-158">`[SessionHostName <String>]`: имя сеанса в указанном пуле хостов</span><span class="sxs-lookup"><span data-stu-id="1925c-158">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="1925c-159">`[SubscriptionId <String>]`: ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="1925c-159">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="1925c-160">`[UserSessionId <String>]`: имя сеанса пользователя в указанном хосте сеанса</span><span class="sxs-lookup"><span data-stu-id="1925c-160">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="1925c-161">`[WorkspaceName <String>]`: имя рабочей области</span><span class="sxs-lookup"><span data-stu-id="1925c-161">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="1925c-162">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1925c-162">RELATED LINKS</span></span>

