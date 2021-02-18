---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/expand-azwvdmsiximage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Expand-AzWvdMsixImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Expand-AzWvdMsixImage.md
ms.openlocfilehash: 56122e8d1ae94b6a898c073f2b2f2fb891504789
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100220140"
---
# <span data-ttu-id="35349-101">Expand-AzWvdMsixImage</span><span class="sxs-lookup"><span data-stu-id="35349-101">Expand-AzWvdMsixImage</span></span>

## <span data-ttu-id="35349-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35349-102">SYNOPSIS</span></span>
<span data-ttu-id="35349-103">Расширение и списки пакетов MSIX в изображении с учетом пути к изображению.</span><span class="sxs-lookup"><span data-stu-id="35349-103">Expands and Lists MSIX packages in an Image, given the Image Path.</span></span>

## <span data-ttu-id="35349-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="35349-104">SYNTAX</span></span>

### <span data-ttu-id="35349-105">ExpandExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="35349-105">ExpandExpanded (Default)</span></span>
```
Expand-AzWvdMsixImage -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Uri <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="35349-106">Развернуть</span><span class="sxs-lookup"><span data-stu-id="35349-106">Expand</span></span>
```
Expand-AzWvdMsixImage -HostPoolName <String> -ResourceGroupName <String> -MsixImageUri <IMsixImageUri>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="35349-107">ExpandViaIdentity</span><span class="sxs-lookup"><span data-stu-id="35349-107">ExpandViaIdentity</span></span>
```
Expand-AzWvdMsixImage -InputObject <IDesktopVirtualizationIdentity> -MsixImageUri <IMsixImageUri>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="35349-108">ExpandViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="35349-108">ExpandViaIdentityExpanded</span></span>
```
Expand-AzWvdMsixImage -InputObject <IDesktopVirtualizationIdentity> [-Uri <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="35349-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="35349-109">DESCRIPTION</span></span>
<span data-ttu-id="35349-110">Расширение и списки пакетов MSIX в изображении с учетом пути к изображению.</span><span class="sxs-lookup"><span data-stu-id="35349-110">Expands and Lists MSIX packages in an Image, given the Image Path.</span></span>

## <span data-ttu-id="35349-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="35349-111">EXAMPLES</span></span>

### <span data-ttu-id="35349-112">Пример 1. Расширяет указанный путь к изображению и извлекает метаданные пакета, найденные в AppxManifest.xml</span><span class="sxs-lookup"><span data-stu-id="35349-112">Example 1: Expands specified Image Path and retrieves Package metadata found in AppxManifest.xml</span></span>
```powershell
PS C:\> Expand-AzWvdMsixImage -HostPoolName HostPoolName `
          -ResourceGroupName resourceGroupName `
          -SubscriptionId SubscriptionId `
          -Uri ImagePathURI

Name                          Type
----                          ----
HostPoolName/extractmsiximage Microsoft.DesktopVirtualization/hostpools/extractmsiximage
```

<span data-ttu-id="35349-113">Эта команда возвращает метаданные пакета MSIX, найденные в заданном пути изображения.</span><span class="sxs-lookup"><span data-stu-id="35349-113">This command returns Metadata of MSIX Package found in the given Image Path.</span></span>

## <span data-ttu-id="35349-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="35349-114">PARAMETERS</span></span>

### <span data-ttu-id="35349-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35349-115">-DefaultProfile</span></span>
<span data-ttu-id="35349-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="35349-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35349-117">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="35349-117">-HostPoolName</span></span>
<span data-ttu-id="35349-118">Имя пула хостов в указанной группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="35349-118">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="35349-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="35349-119">-InputObject</span></span>
<span data-ttu-id="35349-120">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="35349-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="35349-121">-MsixImageUri</span><span class="sxs-lookup"><span data-stu-id="35349-121">-MsixImageUri</span></span>
<span data-ttu-id="35349-122">Представляет URI, ссылающийся на изображение MSIX. Чтобы построить, см. раздел "ПРИМЕЧАНИЯ" для свойств MSIXIMAGEURI и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="35349-122">Represents URI referring to MSIX Image To construct, see NOTES section for MSIXIMAGEURI properties and create a hash table.</span></span>

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

### <span data-ttu-id="35349-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35349-123">-ResourceGroupName</span></span>
<span data-ttu-id="35349-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="35349-124">The name of the resource group.</span></span>
<span data-ttu-id="35349-125">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="35349-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="35349-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="35349-126">-SubscriptionId</span></span>
<span data-ttu-id="35349-127">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="35349-127">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="35349-128">-Uri</span><span class="sxs-lookup"><span data-stu-id="35349-128">-Uri</span></span>
<span data-ttu-id="35349-129">URI для изображения</span><span class="sxs-lookup"><span data-stu-id="35349-129">URI to Image</span></span>

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

### <span data-ttu-id="35349-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="35349-130">-Confirm</span></span>
<span data-ttu-id="35349-131">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="35349-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35349-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35349-132">-WhatIf</span></span>
<span data-ttu-id="35349-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="35349-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35349-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="35349-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35349-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35349-135">CommonParameters</span></span>
<span data-ttu-id="35349-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35349-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35349-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="35349-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35349-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="35349-138">INPUTS</span></span>

### <span data-ttu-id="35349-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IMsixImageUri</span><span class="sxs-lookup"><span data-stu-id="35349-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IMsixImageUri</span></span>

### <span data-ttu-id="35349-140">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="35349-140">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="35349-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="35349-141">OUTPUTS</span></span>

### <span data-ttu-id="35349-142">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IExpandMsixImage</span><span class="sxs-lookup"><span data-stu-id="35349-142">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IExpandMsixImage</span></span>

## <span data-ttu-id="35349-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="35349-143">NOTES</span></span>

<span data-ttu-id="35349-144">ALIASES</span><span class="sxs-lookup"><span data-stu-id="35349-144">ALIASES</span></span>

<span data-ttu-id="35349-145">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="35349-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="35349-146">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="35349-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="35349-147">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="35349-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="35349-148">INPUTOBJECT <IDesktopVirtualizationIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="35349-148">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="35349-149">`[ApplicationGroupName <String>]`: имя группы приложений</span><span class="sxs-lookup"><span data-stu-id="35349-149">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="35349-150">`[ApplicationName <String>]`: имя приложения в указанной группе приложений</span><span class="sxs-lookup"><span data-stu-id="35349-150">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="35349-151">`[DesktopName <String>]`: имя рабочего стола в указанной группе рабочего стола</span><span class="sxs-lookup"><span data-stu-id="35349-151">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="35349-152">`[HostPoolName <String>]`: имя пула хостов в указанной группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="35349-152">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="35349-153">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="35349-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="35349-154">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span><span class="sxs-lookup"><span data-stu-id="35349-154">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="35349-155">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="35349-155">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="35349-156">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="35349-156">The name is case insensitive.</span></span>
  - <span data-ttu-id="35349-157">`[SessionHostName <String>]`: имя сеанса в указанном пуле хостов</span><span class="sxs-lookup"><span data-stu-id="35349-157">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="35349-158">`[SubscriptionId <String>]`: ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="35349-158">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="35349-159">`[UserSessionId <String>]`: имя сеанса пользователя в указанном хосте сеанса</span><span class="sxs-lookup"><span data-stu-id="35349-159">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="35349-160">`[WorkspaceName <String>]`: имя рабочей области</span><span class="sxs-lookup"><span data-stu-id="35349-160">`[WorkspaceName <String>]`: The name of the workspace</span></span>

<span data-ttu-id="35349-161">MSIXIMAGEURI: <IMsixImageUri> представляет URI, ссылаясь на изображение MSIX</span><span class="sxs-lookup"><span data-stu-id="35349-161">MSIXIMAGEURI <IMsixImageUri>: Represents URI referring to MSIX Image</span></span>
  - <span data-ttu-id="35349-162">`[Uri <String>]`: URI для изображения</span><span class="sxs-lookup"><span data-stu-id="35349-162">`[Uri <String>]`: URI to Image</span></span>

## <span data-ttu-id="35349-163">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="35349-163">RELATED LINKS</span></span>

