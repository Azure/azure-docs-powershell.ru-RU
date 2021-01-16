---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvdmsixpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdMsixPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdMsixPackage.md
ms.openlocfilehash: 8fe887f754c5a5a9f45d38d646a1edd03d1cc006
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98426324"
---
# <span data-ttu-id="d6d2e-101">Update-AzWvdMsixPackage</span><span class="sxs-lookup"><span data-stu-id="d6d2e-101">Update-AzWvdMsixPackage</span></span>

## <span data-ttu-id="d6d2e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d6d2e-102">SYNOPSIS</span></span>
<span data-ttu-id="d6d2e-103">Обновление пакета MSIX.</span><span class="sxs-lookup"><span data-stu-id="d6d2e-103">Update an  MSIX Package.</span></span>

## <span data-ttu-id="d6d2e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d6d2e-104">SYNTAX</span></span>

### <span data-ttu-id="d6d2e-105">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d6d2e-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdMsixPackage -FullName <String> -HostPoolName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DisplayName <String>] [-IsActive] [-IsRegularRegistration]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d6d2e-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="d6d2e-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdMsixPackage -InputObject <IDesktopVirtualizationIdentity> [-DisplayName <String>] [-IsActive]
 [-IsRegularRegistration] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d6d2e-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d6d2e-107">DESCRIPTION</span></span>
<span data-ttu-id="d6d2e-108">Обновление пакета MSIX.</span><span class="sxs-lookup"><span data-stu-id="d6d2e-108">Update an  MSIX Package.</span></span>

## <span data-ttu-id="d6d2e-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d6d2e-109">EXAMPLES</span></span>

### <span data-ttu-id="d6d2e-110">Пример 1. Обновление пакета MSIX</span><span class="sxs-lookup"><span data-stu-id="d6d2e-110">Example 1: Update a MSIX Package</span></span> 
```powershell
PS C:\> Update-AzWvdMsixPackage -HostPoolName HostPoolName `
                -ResourceGroupName ResourceGroupName `
                -SubscriptionId SubscriptionId `
                -displayName 'Updated-display-Name' `
                    -IsRegularRegistration:$False `
                -IsActive:$True

Name                                                  Type
----                                                  ----
HostPoolName/MSIXPackage_FullName1                    Microsoft.DesktopVirtualization/hostpools/msixpackages
```

<span data-ttu-id="d6d2e-111">Эта команда обновляет пакет MSIX в hostPool.</span><span class="sxs-lookup"><span data-stu-id="d6d2e-111">This command updates a MSIX Package in a HostPool.</span></span>

## <span data-ttu-id="d6d2e-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d6d2e-112">PARAMETERS</span></span>

### <span data-ttu-id="d6d2e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6d2e-113">-DefaultProfile</span></span>
<span data-ttu-id="d6d2e-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d6d2e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6d2e-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="d6d2e-115">-DisplayName</span></span>
<span data-ttu-id="d6d2e-116">Отображаемая имя пакета MSIX.</span><span class="sxs-lookup"><span data-stu-id="d6d2e-116">Display name for MSIX Package.</span></span>

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

### <span data-ttu-id="d6d2e-117">-FullName</span><span class="sxs-lookup"><span data-stu-id="d6d2e-117">-FullName</span></span>
<span data-ttu-id="d6d2e-118">Название пакета MSIX для конкретной версии в указанном hostpool</span><span class="sxs-lookup"><span data-stu-id="d6d2e-118">The version specific package full name of the MSIX package within specified hostpool</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: MsixPackageFullName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6d2e-119">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="d6d2e-119">-HostPoolName</span></span>
<span data-ttu-id="d6d2e-120">Имя пула хостов в указанной группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="d6d2e-120">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="d6d2e-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d6d2e-121">-InputObject</span></span>
<span data-ttu-id="d6d2e-122">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="d6d2e-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d6d2e-123">-IsActive</span><span class="sxs-lookup"><span data-stu-id="d6d2e-123">-IsActive</span></span>
<span data-ttu-id="d6d2e-124">Установите версию пакета, которая будет активной для всего хостпака.</span><span class="sxs-lookup"><span data-stu-id="d6d2e-124">Set a version of the package to be active across hostpool.</span></span>

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

### <span data-ttu-id="d6d2e-125">-IsRegularRegistration</span><span class="sxs-lookup"><span data-stu-id="d6d2e-125">-IsRegularRegistration</span></span>
<span data-ttu-id="d6d2e-126">Настройка режима регистрации.</span><span class="sxs-lookup"><span data-stu-id="d6d2e-126">Set Registration mode.</span></span>
<span data-ttu-id="d6d2e-127">Обычный или с задержкой.</span><span class="sxs-lookup"><span data-stu-id="d6d2e-127">Regular or Delayed.</span></span>

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

### <span data-ttu-id="d6d2e-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6d2e-128">-ResourceGroupName</span></span>
<span data-ttu-id="d6d2e-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d6d2e-129">The name of the resource group.</span></span>
<span data-ttu-id="d6d2e-130">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="d6d2e-130">The name is case insensitive.</span></span>

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

### <span data-ttu-id="d6d2e-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d6d2e-131">-SubscriptionId</span></span>
<span data-ttu-id="d6d2e-132">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="d6d2e-132">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="d6d2e-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d6d2e-133">-Confirm</span></span>
<span data-ttu-id="d6d2e-134">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d6d2e-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6d2e-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6d2e-135">-WhatIf</span></span>
<span data-ttu-id="d6d2e-136">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d6d2e-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6d2e-137">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="d6d2e-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6d2e-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6d2e-138">CommonParameters</span></span>
<span data-ttu-id="d6d2e-139">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6d2e-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6d2e-140">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d6d2e-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6d2e-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d6d2e-141">INPUTS</span></span>

### <span data-ttu-id="d6d2e-142">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="d6d2e-142">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="d6d2e-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d6d2e-143">OUTPUTS</span></span>

### <span data-ttu-id="d6d2e-144">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IMsixPackage</span><span class="sxs-lookup"><span data-stu-id="d6d2e-144">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IMsixPackage</span></span>

## <span data-ttu-id="d6d2e-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d6d2e-145">NOTES</span></span>

<span data-ttu-id="d6d2e-146">ALIASES</span><span class="sxs-lookup"><span data-stu-id="d6d2e-146">ALIASES</span></span>

<span data-ttu-id="d6d2e-147">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="d6d2e-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d6d2e-148">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="d6d2e-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d6d2e-149">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d6d2e-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d6d2e-150">INPUTOBJECT <IDesktopVirtualizationIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="d6d2e-150">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d6d2e-151">`[ApplicationGroupName <String>]`: имя группы приложений</span><span class="sxs-lookup"><span data-stu-id="d6d2e-151">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="d6d2e-152">`[ApplicationName <String>]`: имя приложения в указанной группе приложений</span><span class="sxs-lookup"><span data-stu-id="d6d2e-152">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="d6d2e-153">`[DesktopName <String>]`: имя рабочего стола в указанной группе рабочего стола</span><span class="sxs-lookup"><span data-stu-id="d6d2e-153">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="d6d2e-154">`[HostPoolName <String>]`: имя пула хостов в указанной группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="d6d2e-154">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="d6d2e-155">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="d6d2e-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d6d2e-156">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span><span class="sxs-lookup"><span data-stu-id="d6d2e-156">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="d6d2e-157">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d6d2e-157">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="d6d2e-158">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="d6d2e-158">The name is case insensitive.</span></span>
  - <span data-ttu-id="d6d2e-159">`[SessionHostName <String>]`: имя сеанса в указанном пуле хостов</span><span class="sxs-lookup"><span data-stu-id="d6d2e-159">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="d6d2e-160">`[SubscriptionId <String>]`: ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="d6d2e-160">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="d6d2e-161">`[UserSessionId <String>]`: имя сеанса пользователя в указанном хосте сеанса</span><span class="sxs-lookup"><span data-stu-id="d6d2e-161">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="d6d2e-162">`[WorkspaceName <String>]`: имя рабочей области</span><span class="sxs-lookup"><span data-stu-id="d6d2e-162">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="d6d2e-163">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d6d2e-163">RELATED LINKS</span></span>

