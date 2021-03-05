---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/update-azwvdsessionhost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdSessionHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdSessionHost.md
ms.openlocfilehash: 9e8599edaa1a1c19d5b0629d290402c792cf2563
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983571"
---
# <span data-ttu-id="339f6-101">Update-AzWvdSessionHost</span><span class="sxs-lookup"><span data-stu-id="339f6-101">Update-AzWvdSessionHost</span></span>

## <span data-ttu-id="339f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="339f6-102">SYNOPSIS</span></span>
<span data-ttu-id="339f6-103">Обновив хост сеанса.</span><span class="sxs-lookup"><span data-stu-id="339f6-103">Update a session host.</span></span>

## <span data-ttu-id="339f6-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="339f6-104">SYNTAX</span></span>

### <span data-ttu-id="339f6-105">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="339f6-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdSessionHost -HostPoolName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-AllowNewSession] [-AssignedUser <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="339f6-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="339f6-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdSessionHost -InputObject <IDesktopVirtualizationIdentity> [-AllowNewSession]
 [-AssignedUser <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="339f6-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="339f6-107">DESCRIPTION</span></span>
<span data-ttu-id="339f6-108">Обновив хост сеанса.</span><span class="sxs-lookup"><span data-stu-id="339f6-108">Update a session host.</span></span>

## <span data-ttu-id="339f6-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="339f6-109">EXAMPLES</span></span>

### <span data-ttu-id="339f6-110">Пример 1. Обновление имени виртуального рабочего стола Windows</span><span class="sxs-lookup"><span data-stu-id="339f6-110">Example 1: Update a Windows Virtual Desktop SessionHost by name</span></span>
```powershell
PS C:\> Update-AzWvdSessionHost -ResourceGroupName ResourceGroupName `
                            -HostPoolName HostPoolName `
                            -Name SessionHostName `
                            -AllowNewSession:$false

Name                                               Type
----                                               ----
HostPoolName/SessionHostName Microsoft.DesktopVirtualization/hostpools/sessionhosts
```

<span data-ttu-id="339f6-111">Эта команда обновляет сеанс Виртуального рабочего стола Windows в пуле хостов.</span><span class="sxs-lookup"><span data-stu-id="339f6-111">This command updates a Windows Virtual Desktop SessionHost in a Host Pool.</span></span>

## <span data-ttu-id="339f6-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="339f6-112">PARAMETERS</span></span>

### <span data-ttu-id="339f6-113">-AllowNewSession</span><span class="sxs-lookup"><span data-stu-id="339f6-113">-AllowNewSession</span></span>
<span data-ttu-id="339f6-114">Разрешить новый сеанс.</span><span class="sxs-lookup"><span data-stu-id="339f6-114">Allow a new session.</span></span>

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

### <span data-ttu-id="339f6-115">-AssignedUser</span><span class="sxs-lookup"><span data-stu-id="339f6-115">-AssignedUser</span></span>
<span data-ttu-id="339f6-116">Пользователь, назначенный sessionHost.</span><span class="sxs-lookup"><span data-stu-id="339f6-116">User assigned to SessionHost.</span></span>

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

### <span data-ttu-id="339f6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="339f6-117">-DefaultProfile</span></span>
<span data-ttu-id="339f6-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="339f6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="339f6-119">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="339f6-119">-HostPoolName</span></span>
<span data-ttu-id="339f6-120">Имя пула хостов в указанной группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="339f6-120">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="339f6-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="339f6-121">-InputObject</span></span>
<span data-ttu-id="339f6-122">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="339f6-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="339f6-123">-Name</span><span class="sxs-lookup"><span data-stu-id="339f6-123">-Name</span></span>
<span data-ttu-id="339f6-124">Имя сеанса в указанном пуле хостов</span><span class="sxs-lookup"><span data-stu-id="339f6-124">The name of the session host within the specified host pool</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: SessionHostName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="339f6-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="339f6-125">-ResourceGroupName</span></span>
<span data-ttu-id="339f6-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="339f6-126">The name of the resource group.</span></span>
<span data-ttu-id="339f6-127">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="339f6-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="339f6-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="339f6-128">-SubscriptionId</span></span>
<span data-ttu-id="339f6-129">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="339f6-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="339f6-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="339f6-130">-Confirm</span></span>
<span data-ttu-id="339f6-131">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="339f6-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="339f6-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="339f6-132">-WhatIf</span></span>
<span data-ttu-id="339f6-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="339f6-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="339f6-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="339f6-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="339f6-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="339f6-135">CommonParameters</span></span>
<span data-ttu-id="339f6-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="339f6-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="339f6-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="339f6-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="339f6-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="339f6-138">INPUTS</span></span>

### <span data-ttu-id="339f6-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="339f6-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="339f6-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="339f6-140">OUTPUTS</span></span>

### <span data-ttu-id="339f6-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.ISessionHost</span><span class="sxs-lookup"><span data-stu-id="339f6-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.ISessionHost</span></span>

## <span data-ttu-id="339f6-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="339f6-142">NOTES</span></span>

<span data-ttu-id="339f6-143">ALIASES</span><span class="sxs-lookup"><span data-stu-id="339f6-143">ALIASES</span></span>

<span data-ttu-id="339f6-144">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="339f6-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="339f6-145">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="339f6-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="339f6-146">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="339f6-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="339f6-147">INPUTOBJECT <IDesktopVirtualizationIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="339f6-147">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="339f6-148">`[ApplicationGroupName <String>]`: имя группы приложений</span><span class="sxs-lookup"><span data-stu-id="339f6-148">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="339f6-149">`[ApplicationName <String>]`: имя приложения в указанной группе приложений</span><span class="sxs-lookup"><span data-stu-id="339f6-149">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="339f6-150">`[DesktopName <String>]`: имя рабочего стола в указанной группе рабочего стола</span><span class="sxs-lookup"><span data-stu-id="339f6-150">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="339f6-151">`[HostPoolName <String>]`: имя пула хостов в указанной группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="339f6-151">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="339f6-152">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="339f6-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="339f6-153">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span><span class="sxs-lookup"><span data-stu-id="339f6-153">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="339f6-154">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="339f6-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="339f6-155">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="339f6-155">The name is case insensitive.</span></span>
  - <span data-ttu-id="339f6-156">`[SessionHostName <String>]`: имя сеанса в указанном пуле хостов</span><span class="sxs-lookup"><span data-stu-id="339f6-156">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="339f6-157">`[SubscriptionId <String>]`: ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="339f6-157">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="339f6-158">`[UserSessionId <String>]`: имя сеанса пользователя в указанном хосте сеанса</span><span class="sxs-lookup"><span data-stu-id="339f6-158">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="339f6-159">`[WorkspaceName <String>]`: имя рабочей области</span><span class="sxs-lookup"><span data-stu-id="339f6-159">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="339f6-160">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="339f6-160">RELATED LINKS</span></span>

