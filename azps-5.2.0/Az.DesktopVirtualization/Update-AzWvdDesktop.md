---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvddesktop
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdDesktop.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdDesktop.md
ms.openlocfilehash: 3d1a822bf545cd111ef3fef19ba380f426a831c1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98328933"
---
# <span data-ttu-id="32805-101">Update-AzWvdDesktop</span><span class="sxs-lookup"><span data-stu-id="32805-101">Update-AzWvdDesktop</span></span>

## <span data-ttu-id="32805-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="32805-102">SYNOPSIS</span></span>
<span data-ttu-id="32805-103">Обновив рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="32805-103">Update a desktop.</span></span>

## <span data-ttu-id="32805-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="32805-104">SYNTAX</span></span>

### <span data-ttu-id="32805-105">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="32805-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdDesktop -ApplicationGroupName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="32805-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="32805-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdDesktop -InputObject <IDesktopVirtualizationIdentity> [-Description <String>]
 [-FriendlyName <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="32805-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="32805-107">DESCRIPTION</span></span>
<span data-ttu-id="32805-108">Обновив рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="32805-108">Update a desktop.</span></span>

## <span data-ttu-id="32805-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="32805-109">EXAMPLES</span></span>

### <span data-ttu-id="32805-110">Пример 1. Обновление виртуального рабочего стола Windows</span><span class="sxs-lookup"><span data-stu-id="32805-110">Example 1: Update a Windows Virtual Desktop Desktop</span></span>
```powershell
PS C:\> Update-AzWvdDesktop -ResourceGroupName ResourceGroupName `
                             -GroupName ApplicationGroupName `
                             -Name DesktopName `
                             -FriendlyName 'Friendly name' `
                             -Description 'Description' `

Name                             Type
----                             ----
ApplicationGroupName/DesktopName Microsoft.DesktopVirtualization/applicationgroups/desktops
```

<span data-ttu-id="32805-111">Эта команда обновляет виртуальный рабочий стол Windows в соответствующей группе.</span><span class="sxs-lookup"><span data-stu-id="32805-111">This command updates a Windows Virtual Desktop Desktop in an applicaton Group.</span></span>

## <span data-ttu-id="32805-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="32805-112">PARAMETERS</span></span>

### <span data-ttu-id="32805-113">-ApplicationGroupName</span><span class="sxs-lookup"><span data-stu-id="32805-113">-ApplicationGroupName</span></span>
<span data-ttu-id="32805-114">Имя группы приложений</span><span class="sxs-lookup"><span data-stu-id="32805-114">The name of the application group</span></span>

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

### <span data-ttu-id="32805-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32805-115">-DefaultProfile</span></span>
<span data-ttu-id="32805-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="32805-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="32805-117">-Description</span><span class="sxs-lookup"><span data-stu-id="32805-117">-Description</span></span>
<span data-ttu-id="32805-118">Описание рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="32805-118">Description of Desktop.</span></span>

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

### <span data-ttu-id="32805-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="32805-119">-FriendlyName</span></span>
<span data-ttu-id="32805-120">Удобное имя рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="32805-120">Friendly name of Desktop.</span></span>

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

### <span data-ttu-id="32805-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="32805-121">-InputObject</span></span>
<span data-ttu-id="32805-122">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="32805-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="32805-123">-Name</span><span class="sxs-lookup"><span data-stu-id="32805-123">-Name</span></span>
<span data-ttu-id="32805-124">Имя рабочего стола в указанной группе рабочего стола</span><span class="sxs-lookup"><span data-stu-id="32805-124">The name of the desktop within the specified desktop group</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: DesktopName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32805-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32805-125">-ResourceGroupName</span></span>
<span data-ttu-id="32805-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="32805-126">The name of the resource group.</span></span>
<span data-ttu-id="32805-127">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="32805-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="32805-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="32805-128">-SubscriptionId</span></span>
<span data-ttu-id="32805-129">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="32805-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="32805-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="32805-130">-Tag</span></span>
<span data-ttu-id="32805-131">теги для обновления</span><span class="sxs-lookup"><span data-stu-id="32805-131">tags to be updated</span></span>

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

### <span data-ttu-id="32805-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="32805-132">-Confirm</span></span>
<span data-ttu-id="32805-133">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="32805-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32805-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32805-134">-WhatIf</span></span>
<span data-ttu-id="32805-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="32805-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="32805-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="32805-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32805-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32805-137">CommonParameters</span></span>
<span data-ttu-id="32805-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32805-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32805-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="32805-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32805-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="32805-140">INPUTS</span></span>

### <span data-ttu-id="32805-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="32805-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="32805-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="32805-142">OUTPUTS</span></span>

### <span data-ttu-id="32805-143">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IDesktop</span><span class="sxs-lookup"><span data-stu-id="32805-143">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IDesktop</span></span>

## <span data-ttu-id="32805-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="32805-144">NOTES</span></span>

<span data-ttu-id="32805-145">ALIASES</span><span class="sxs-lookup"><span data-stu-id="32805-145">ALIASES</span></span>

<span data-ttu-id="32805-146">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="32805-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="32805-147">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="32805-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="32805-148">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="32805-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="32805-149">INPUTOBJECT <IDesktopVirtualizationIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="32805-149">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="32805-150">`[ApplicationGroupName <String>]`: имя группы приложений</span><span class="sxs-lookup"><span data-stu-id="32805-150">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="32805-151">`[ApplicationName <String>]`: имя приложения в указанной группе приложений</span><span class="sxs-lookup"><span data-stu-id="32805-151">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="32805-152">`[DesktopName <String>]`: имя рабочего стола в указанной группе рабочего стола</span><span class="sxs-lookup"><span data-stu-id="32805-152">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="32805-153">`[HostPoolName <String>]`: имя пула хостов в указанной группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="32805-153">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="32805-154">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="32805-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="32805-155">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span><span class="sxs-lookup"><span data-stu-id="32805-155">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="32805-156">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="32805-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="32805-157">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="32805-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="32805-158">`[SessionHostName <String>]`: имя сеанса в указанном пуле хостов</span><span class="sxs-lookup"><span data-stu-id="32805-158">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="32805-159">`[SubscriptionId <String>]`: ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="32805-159">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="32805-160">`[UserSessionId <String>]`: имя сеанса пользователя в указанном хосте сеанса</span><span class="sxs-lookup"><span data-stu-id="32805-160">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="32805-161">`[WorkspaceName <String>]`: имя рабочей области</span><span class="sxs-lookup"><span data-stu-id="32805-161">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="32805-162">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="32805-162">RELATED LINKS</span></span>

