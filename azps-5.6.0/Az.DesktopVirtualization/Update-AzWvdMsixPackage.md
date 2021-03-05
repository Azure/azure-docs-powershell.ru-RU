---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/update-azwvdmsixpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdMsixPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdMsixPackage.md
ms.openlocfilehash: f552c8e21703d64efa2ac65f47461daa963fc1f1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983576"
---
# <span data-ttu-id="fa4e8-101">Update-AzWvdMsixPackage</span><span class="sxs-lookup"><span data-stu-id="fa4e8-101">Update-AzWvdMsixPackage</span></span>

## <span data-ttu-id="fa4e8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa4e8-102">SYNOPSIS</span></span>
<span data-ttu-id="fa4e8-103">Обновление пакета MSIX.</span><span class="sxs-lookup"><span data-stu-id="fa4e8-103">Update an  MSIX Package.</span></span>

## <span data-ttu-id="fa4e8-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="fa4e8-104">SYNTAX</span></span>

### <span data-ttu-id="fa4e8-105">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fa4e8-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdMsixPackage -FullName <String> -HostPoolName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DisplayName <String>] [-IsActive] [-IsRegularRegistration]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="fa4e8-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="fa4e8-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdMsixPackage -InputObject <IDesktopVirtualizationIdentity> [-DisplayName <String>] [-IsActive]
 [-IsRegularRegistration] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="fa4e8-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fa4e8-107">DESCRIPTION</span></span>
<span data-ttu-id="fa4e8-108">Обновление пакета MSIX.</span><span class="sxs-lookup"><span data-stu-id="fa4e8-108">Update an  MSIX Package.</span></span>

## <span data-ttu-id="fa4e8-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="fa4e8-109">EXAMPLES</span></span>

### <span data-ttu-id="fa4e8-110">Пример 1. Обновление пакета MSIX</span><span class="sxs-lookup"><span data-stu-id="fa4e8-110">Example 1: Update a MSIX Package</span></span> 
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

<span data-ttu-id="fa4e8-111">Эта команда обновляет пакет MSIX в hostPool.</span><span class="sxs-lookup"><span data-stu-id="fa4e8-111">This command updates a MSIX Package in a HostPool.</span></span>

## <span data-ttu-id="fa4e8-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fa4e8-112">PARAMETERS</span></span>

### <span data-ttu-id="fa4e8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa4e8-113">-DefaultProfile</span></span>
<span data-ttu-id="fa4e8-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fa4e8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fa4e8-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="fa4e8-115">-DisplayName</span></span>
<span data-ttu-id="fa4e8-116">Отображаемая имя пакета MSIX.</span><span class="sxs-lookup"><span data-stu-id="fa4e8-116">Display name for MSIX Package.</span></span>

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

### <span data-ttu-id="fa4e8-117">-FullName</span><span class="sxs-lookup"><span data-stu-id="fa4e8-117">-FullName</span></span>
<span data-ttu-id="fa4e8-118">Название пакета MSIX для конкретной версии в указанном hostpool</span><span class="sxs-lookup"><span data-stu-id="fa4e8-118">The version specific package full name of the MSIX package within specified hostpool</span></span>

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

### <span data-ttu-id="fa4e8-119">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="fa4e8-119">-HostPoolName</span></span>
<span data-ttu-id="fa4e8-120">Имя пула хостов в указанной группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="fa4e8-120">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="fa4e8-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fa4e8-121">-InputObject</span></span>
<span data-ttu-id="fa4e8-122">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="fa4e8-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="fa4e8-123">-IsActive</span><span class="sxs-lookup"><span data-stu-id="fa4e8-123">-IsActive</span></span>
<span data-ttu-id="fa4e8-124">Установите версию пакета, которая будет активной для всего хостпака.</span><span class="sxs-lookup"><span data-stu-id="fa4e8-124">Set a version of the package to be active across hostpool.</span></span>

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

### <span data-ttu-id="fa4e8-125">-IsRegularRegistration</span><span class="sxs-lookup"><span data-stu-id="fa4e8-125">-IsRegularRegistration</span></span>
<span data-ttu-id="fa4e8-126">Настройка режима регистрации.</span><span class="sxs-lookup"><span data-stu-id="fa4e8-126">Set Registration mode.</span></span>
<span data-ttu-id="fa4e8-127">Обычный или с задержкой.</span><span class="sxs-lookup"><span data-stu-id="fa4e8-127">Regular or Delayed.</span></span>

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

### <span data-ttu-id="fa4e8-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa4e8-128">-ResourceGroupName</span></span>
<span data-ttu-id="fa4e8-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fa4e8-129">The name of the resource group.</span></span>
<span data-ttu-id="fa4e8-130">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="fa4e8-130">The name is case insensitive.</span></span>

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

### <span data-ttu-id="fa4e8-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fa4e8-131">-SubscriptionId</span></span>
<span data-ttu-id="fa4e8-132">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="fa4e8-132">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="fa4e8-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fa4e8-133">-Confirm</span></span>
<span data-ttu-id="fa4e8-134">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="fa4e8-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa4e8-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa4e8-135">-WhatIf</span></span>
<span data-ttu-id="fa4e8-136">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fa4e8-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa4e8-137">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="fa4e8-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa4e8-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa4e8-138">CommonParameters</span></span>
<span data-ttu-id="fa4e8-139">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa4e8-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa4e8-140">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fa4e8-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa4e8-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fa4e8-141">INPUTS</span></span>

### <span data-ttu-id="fa4e8-142">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="fa4e8-142">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="fa4e8-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="fa4e8-143">OUTPUTS</span></span>

### <span data-ttu-id="fa4e8-144">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IMsixPackage</span><span class="sxs-lookup"><span data-stu-id="fa4e8-144">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IMsixPackage</span></span>

## <span data-ttu-id="fa4e8-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="fa4e8-145">NOTES</span></span>

<span data-ttu-id="fa4e8-146">ALIASES</span><span class="sxs-lookup"><span data-stu-id="fa4e8-146">ALIASES</span></span>

<span data-ttu-id="fa4e8-147">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="fa4e8-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="fa4e8-148">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="fa4e8-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="fa4e8-149">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="fa4e8-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="fa4e8-150">INPUTOBJECT <IDesktopVirtualizationIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="fa4e8-150">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="fa4e8-151">`[ApplicationGroupName <String>]`: имя группы приложений</span><span class="sxs-lookup"><span data-stu-id="fa4e8-151">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="fa4e8-152">`[ApplicationName <String>]`: имя приложения в указанной группе приложений</span><span class="sxs-lookup"><span data-stu-id="fa4e8-152">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="fa4e8-153">`[DesktopName <String>]`: имя рабочего стола в указанной группе рабочего стола</span><span class="sxs-lookup"><span data-stu-id="fa4e8-153">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="fa4e8-154">`[HostPoolName <String>]`: имя пула хостов в указанной группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="fa4e8-154">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="fa4e8-155">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="fa4e8-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="fa4e8-156">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span><span class="sxs-lookup"><span data-stu-id="fa4e8-156">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="fa4e8-157">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fa4e8-157">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="fa4e8-158">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="fa4e8-158">The name is case insensitive.</span></span>
  - <span data-ttu-id="fa4e8-159">`[SessionHostName <String>]`: имя сеанса в указанном пуле хостов</span><span class="sxs-lookup"><span data-stu-id="fa4e8-159">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="fa4e8-160">`[SubscriptionId <String>]`: ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="fa4e8-160">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="fa4e8-161">`[UserSessionId <String>]`: имя сеанса пользователя в указанном хосте сеанса</span><span class="sxs-lookup"><span data-stu-id="fa4e8-161">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="fa4e8-162">`[WorkspaceName <String>]`: имя рабочей области</span><span class="sxs-lookup"><span data-stu-id="fa4e8-162">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="fa4e8-163">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fa4e8-163">RELATED LINKS</span></span>

