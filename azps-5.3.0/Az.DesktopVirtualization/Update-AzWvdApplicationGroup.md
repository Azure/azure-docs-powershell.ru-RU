---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdApplicationGroup.md
ms.openlocfilehash: b03fe0c62a446c9ed54c9330708f29737e18bd59
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98507541"
---
# <span data-ttu-id="fe1fe-101">Update-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="fe1fe-101">Update-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="fe1fe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe1fe-102">SYNOPSIS</span></span>
<span data-ttu-id="fe1fe-103">Обновив applicationGroup.</span><span class="sxs-lookup"><span data-stu-id="fe1fe-103">Update an applicationGroup.</span></span>

## <span data-ttu-id="fe1fe-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="fe1fe-104">SYNTAX</span></span>

### <span data-ttu-id="fe1fe-105">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fe1fe-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdApplicationGroup -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="fe1fe-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="fe1fe-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdApplicationGroup -InputObject <IDesktopVirtualizationIdentity> [-Description <String>]
 [-FriendlyName <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="fe1fe-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fe1fe-107">DESCRIPTION</span></span>
<span data-ttu-id="fe1fe-108">Обновив приложениеGroup.</span><span class="sxs-lookup"><span data-stu-id="fe1fe-108">Update an applicationGroup.</span></span>

## <span data-ttu-id="fe1fe-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="fe1fe-109">EXAMPLES</span></span>

### <span data-ttu-id="fe1fe-110">Пример 1. Создание группы приложений виртуального рабочего стола Windows по имени</span><span class="sxs-lookup"><span data-stu-id="fe1fe-110">Example 1: Create a Windows Virtual Desktop ApplicationGroup by name</span></span>
```powershell
PS C:\> New-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName `
                            -Name ApplicationGroupName `
                            -FriendlyName 'Friendly Name' `
                            -Description 'Description' `

Location   Name                 Type
--------   ----                 ----
eastus     ApplicationGroupName Microsoft.DesktopVirtualization/applicationgroups
```

<span data-ttu-id="fe1fe-111">Эта команда создает группу приложений Виртуального рабочего стола Windows в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fe1fe-111">This command creates a Windows Virtual Desktop ApplicationGroup in a Resource Group.</span></span>

## <span data-ttu-id="fe1fe-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fe1fe-112">PARAMETERS</span></span>

### <span data-ttu-id="fe1fe-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe1fe-113">-DefaultProfile</span></span>
<span data-ttu-id="fe1fe-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fe1fe-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe1fe-115">-Description</span><span class="sxs-lookup"><span data-stu-id="fe1fe-115">-Description</span></span>
<span data-ttu-id="fe1fe-116">Описание ApplicationGroup.</span><span class="sxs-lookup"><span data-stu-id="fe1fe-116">Description of ApplicationGroup.</span></span>

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

### <span data-ttu-id="fe1fe-117">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="fe1fe-117">-FriendlyName</span></span>
<span data-ttu-id="fe1fe-118">Имя ApplicationGroup.</span><span class="sxs-lookup"><span data-stu-id="fe1fe-118">Friendly name of ApplicationGroup.</span></span>

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

### <span data-ttu-id="fe1fe-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fe1fe-119">-InputObject</span></span>
<span data-ttu-id="fe1fe-120">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="fe1fe-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="fe1fe-121">-Name</span><span class="sxs-lookup"><span data-stu-id="fe1fe-121">-Name</span></span>
<span data-ttu-id="fe1fe-122">Имя группы приложений</span><span class="sxs-lookup"><span data-stu-id="fe1fe-122">The name of the application group</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ApplicationGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe1fe-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe1fe-123">-ResourceGroupName</span></span>
<span data-ttu-id="fe1fe-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fe1fe-124">The name of the resource group.</span></span>
<span data-ttu-id="fe1fe-125">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="fe1fe-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="fe1fe-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fe1fe-126">-SubscriptionId</span></span>
<span data-ttu-id="fe1fe-127">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="fe1fe-127">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="fe1fe-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="fe1fe-128">-Tag</span></span>
<span data-ttu-id="fe1fe-129">теги для обновления</span><span class="sxs-lookup"><span data-stu-id="fe1fe-129">tags to be updated</span></span>

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

### <span data-ttu-id="fe1fe-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fe1fe-130">-Confirm</span></span>
<span data-ttu-id="fe1fe-131">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fe1fe-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe1fe-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe1fe-132">-WhatIf</span></span>
<span data-ttu-id="fe1fe-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fe1fe-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe1fe-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="fe1fe-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe1fe-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe1fe-135">CommonParameters</span></span>
<span data-ttu-id="fe1fe-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe1fe-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe1fe-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fe1fe-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe1fe-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fe1fe-138">INPUTS</span></span>

### <span data-ttu-id="fe1fe-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="fe1fe-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="fe1fe-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="fe1fe-140">OUTPUTS</span></span>

### <span data-ttu-id="fe1fe-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="fe1fe-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IApplicationGroup</span></span>

## <span data-ttu-id="fe1fe-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="fe1fe-142">NOTES</span></span>

<span data-ttu-id="fe1fe-143">ALIASES</span><span class="sxs-lookup"><span data-stu-id="fe1fe-143">ALIASES</span></span>

<span data-ttu-id="fe1fe-144">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="fe1fe-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="fe1fe-145">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="fe1fe-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="fe1fe-146">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="fe1fe-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="fe1fe-147">INPUTOBJECT <IDesktopVirtualizationIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="fe1fe-147">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="fe1fe-148">`[ApplicationGroupName <String>]`: имя группы приложений</span><span class="sxs-lookup"><span data-stu-id="fe1fe-148">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="fe1fe-149">`[ApplicationName <String>]`: имя приложения в указанной группе приложений</span><span class="sxs-lookup"><span data-stu-id="fe1fe-149">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="fe1fe-150">`[DesktopName <String>]`: имя рабочего стола в указанной группе рабочего стола</span><span class="sxs-lookup"><span data-stu-id="fe1fe-150">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="fe1fe-151">`[HostPoolName <String>]`: имя пула хостов в указанной группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="fe1fe-151">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="fe1fe-152">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="fe1fe-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="fe1fe-153">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span><span class="sxs-lookup"><span data-stu-id="fe1fe-153">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="fe1fe-154">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fe1fe-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="fe1fe-155">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="fe1fe-155">The name is case insensitive.</span></span>
  - <span data-ttu-id="fe1fe-156">`[SessionHostName <String>]`: имя сеанса в указанном пуле хостов</span><span class="sxs-lookup"><span data-stu-id="fe1fe-156">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="fe1fe-157">`[SubscriptionId <String>]`: ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="fe1fe-157">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="fe1fe-158">`[UserSessionId <String>]`: имя сеанса пользователя в указанном хосте сеанса</span><span class="sxs-lookup"><span data-stu-id="fe1fe-158">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="fe1fe-159">`[WorkspaceName <String>]`: имя рабочей области</span><span class="sxs-lookup"><span data-stu-id="fe1fe-159">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="fe1fe-160">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fe1fe-160">RELATED LINKS</span></span>

