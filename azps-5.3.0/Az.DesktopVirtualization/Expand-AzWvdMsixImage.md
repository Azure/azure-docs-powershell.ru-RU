---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/expand-azwvdmsiximage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Expand-AzWvdMsixImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Expand-AzWvdMsixImage.md
ms.openlocfilehash: 56122e8d1ae94b6a898c073f2b2f2fb891504789
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98426383"
---
# <span data-ttu-id="978f3-101">Expand-AzWvdMsixImage</span><span class="sxs-lookup"><span data-stu-id="978f3-101">Expand-AzWvdMsixImage</span></span>

## <span data-ttu-id="978f3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="978f3-102">SYNOPSIS</span></span>
<span data-ttu-id="978f3-103">Расширение и списки пакетов MSIX в изображении с учетом пути к изображению.</span><span class="sxs-lookup"><span data-stu-id="978f3-103">Expands and Lists MSIX packages in an Image, given the Image Path.</span></span>

## <span data-ttu-id="978f3-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="978f3-104">SYNTAX</span></span>

### <span data-ttu-id="978f3-105">ExpandExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="978f3-105">ExpandExpanded (Default)</span></span>
```
Expand-AzWvdMsixImage -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Uri <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="978f3-106">Развернуть</span><span class="sxs-lookup"><span data-stu-id="978f3-106">Expand</span></span>
```
Expand-AzWvdMsixImage -HostPoolName <String> -ResourceGroupName <String> -MsixImageUri <IMsixImageUri>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="978f3-107">ExpandViaIdentity</span><span class="sxs-lookup"><span data-stu-id="978f3-107">ExpandViaIdentity</span></span>
```
Expand-AzWvdMsixImage -InputObject <IDesktopVirtualizationIdentity> -MsixImageUri <IMsixImageUri>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="978f3-108">ExpandViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="978f3-108">ExpandViaIdentityExpanded</span></span>
```
Expand-AzWvdMsixImage -InputObject <IDesktopVirtualizationIdentity> [-Uri <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="978f3-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="978f3-109">DESCRIPTION</span></span>
<span data-ttu-id="978f3-110">Расширение и списки пакетов MSIX в изображении с учетом пути к изображению.</span><span class="sxs-lookup"><span data-stu-id="978f3-110">Expands and Lists MSIX packages in an Image, given the Image Path.</span></span>

## <span data-ttu-id="978f3-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="978f3-111">EXAMPLES</span></span>

### <span data-ttu-id="978f3-112">Пример 1. Расширяет указанный путь к изображению и извлекает метаданные пакета, найденные в AppxManifest.xml</span><span class="sxs-lookup"><span data-stu-id="978f3-112">Example 1: Expands specified Image Path and retrieves Package metadata found in AppxManifest.xml</span></span>
```powershell
PS C:\> Expand-AzWvdMsixImage -HostPoolName HostPoolName `
          -ResourceGroupName resourceGroupName `
          -SubscriptionId SubscriptionId `
          -Uri ImagePathURI

Name                          Type
----                          ----
HostPoolName/extractmsiximage Microsoft.DesktopVirtualization/hostpools/extractmsiximage
```

<span data-ttu-id="978f3-113">Эта команда возвращает метаданные пакета MSIX, найденные в заданном пути изображения.</span><span class="sxs-lookup"><span data-stu-id="978f3-113">This command returns Metadata of MSIX Package found in the given Image Path.</span></span>

## <span data-ttu-id="978f3-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="978f3-114">PARAMETERS</span></span>

### <span data-ttu-id="978f3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="978f3-115">-DefaultProfile</span></span>
<span data-ttu-id="978f3-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="978f3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="978f3-117">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="978f3-117">-HostPoolName</span></span>
<span data-ttu-id="978f3-118">Имя пула хостов в указанной группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="978f3-118">The name of the host pool within the specified resource group</span></span>

```yaml
Type: System.String
Parameter Sets: Expand, ExpandExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="978f3-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="978f3-119">-InputObject</span></span>
<span data-ttu-id="978f3-120">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="978f3-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: ExpandViaIdentity, ExpandViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="978f3-121">-MsixImageUri</span><span class="sxs-lookup"><span data-stu-id="978f3-121">-MsixImageUri</span></span>
<span data-ttu-id="978f3-122">Представляет URI, ссылающийся на изображение MSIX. См. раздел "Заметки" для свойств MSIXIMAGEURI и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="978f3-122">Represents URI referring to MSIX Image To construct, see NOTES section for MSIXIMAGEURI properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IMsixImageUri
Parameter Sets: Expand, ExpandViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="978f3-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="978f3-123">-ResourceGroupName</span></span>
<span data-ttu-id="978f3-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="978f3-124">The name of the resource group.</span></span>
<span data-ttu-id="978f3-125">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="978f3-125">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Expand, ExpandExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="978f3-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="978f3-126">-SubscriptionId</span></span>
<span data-ttu-id="978f3-127">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="978f3-127">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Expand, ExpandExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="978f3-128">-Uri</span><span class="sxs-lookup"><span data-stu-id="978f3-128">-Uri</span></span>
<span data-ttu-id="978f3-129">URI для изображения</span><span class="sxs-lookup"><span data-stu-id="978f3-129">URI to Image</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandExpanded, ExpandViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="978f3-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="978f3-130">-Confirm</span></span>
<span data-ttu-id="978f3-131">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="978f3-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="978f3-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="978f3-132">-WhatIf</span></span>
<span data-ttu-id="978f3-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="978f3-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="978f3-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="978f3-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="978f3-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="978f3-135">CommonParameters</span></span>
<span data-ttu-id="978f3-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="978f3-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="978f3-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="978f3-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="978f3-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="978f3-138">INPUTS</span></span>

### <span data-ttu-id="978f3-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IMsixImageUri</span><span class="sxs-lookup"><span data-stu-id="978f3-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IMsixImageUri</span></span>

### <span data-ttu-id="978f3-140">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="978f3-140">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="978f3-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="978f3-141">OUTPUTS</span></span>

### <span data-ttu-id="978f3-142">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IExpandMsixImage</span><span class="sxs-lookup"><span data-stu-id="978f3-142">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IExpandMsixImage</span></span>

## <span data-ttu-id="978f3-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="978f3-143">NOTES</span></span>

<span data-ttu-id="978f3-144">ALIASES</span><span class="sxs-lookup"><span data-stu-id="978f3-144">ALIASES</span></span>

<span data-ttu-id="978f3-145">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="978f3-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="978f3-146">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="978f3-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="978f3-147">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="978f3-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="978f3-148">INPUTOBJECT <IDesktopVirtualizationIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="978f3-148">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="978f3-149">`[ApplicationGroupName <String>]`: имя группы приложений</span><span class="sxs-lookup"><span data-stu-id="978f3-149">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="978f3-150">`[ApplicationName <String>]`: имя приложения в указанной группе приложений</span><span class="sxs-lookup"><span data-stu-id="978f3-150">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="978f3-151">`[DesktopName <String>]`: имя рабочего стола в указанной группе рабочего стола</span><span class="sxs-lookup"><span data-stu-id="978f3-151">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="978f3-152">`[HostPoolName <String>]`: имя пула хостов в указанной группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="978f3-152">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="978f3-153">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="978f3-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="978f3-154">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span><span class="sxs-lookup"><span data-stu-id="978f3-154">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="978f3-155">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="978f3-155">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="978f3-156">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="978f3-156">The name is case insensitive.</span></span>
  - <span data-ttu-id="978f3-157">`[SessionHostName <String>]`: имя сеанса в указанном пуле хостов</span><span class="sxs-lookup"><span data-stu-id="978f3-157">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="978f3-158">`[SubscriptionId <String>]`: ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="978f3-158">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="978f3-159">`[UserSessionId <String>]`: имя сеанса пользователя в указанном хосте сеанса</span><span class="sxs-lookup"><span data-stu-id="978f3-159">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="978f3-160">`[WorkspaceName <String>]`: имя рабочей области</span><span class="sxs-lookup"><span data-stu-id="978f3-160">`[WorkspaceName <String>]`: The name of the workspace</span></span>

<span data-ttu-id="978f3-161">MSIXIMAGEURI: <IMsixImageUri> представляет URI, ссылаясь на изображение MSIX</span><span class="sxs-lookup"><span data-stu-id="978f3-161">MSIXIMAGEURI <IMsixImageUri>: Represents URI referring to MSIX Image</span></span>
  - <span data-ttu-id="978f3-162">`[Uri <String>]`: URI для изображения</span><span class="sxs-lookup"><span data-stu-id="978f3-162">`[Uri <String>]`: URI to Image</span></span>

## <span data-ttu-id="978f3-163">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="978f3-163">RELATED LINKS</span></span>

