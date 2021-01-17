---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdmsixpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdMsixPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdMsixPackage.md
ms.openlocfilehash: 51b940df2ee26c3da53c34fd7f1ffa25d3a266a9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98426388"
---
# <span data-ttu-id="c4897-101">Get-AzWvdMsixPackage</span><span class="sxs-lookup"><span data-stu-id="c4897-101">Get-AzWvdMsixPackage</span></span>

## <span data-ttu-id="c4897-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c4897-102">SYNOPSIS</span></span>
<span data-ttu-id="c4897-103">Получите msixpackage.</span><span class="sxs-lookup"><span data-stu-id="c4897-103">Get a msixpackage.</span></span>

## <span data-ttu-id="c4897-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c4897-104">SYNTAX</span></span>

### <span data-ttu-id="c4897-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c4897-105">List (Default)</span></span>
```
Get-AzWvdMsixPackage -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c4897-106">Получить</span><span class="sxs-lookup"><span data-stu-id="c4897-106">Get</span></span>
```
Get-AzWvdMsixPackage -FullName <String> -HostPoolName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c4897-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="c4897-107">GetViaIdentity</span></span>
```
Get-AzWvdMsixPackage -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="c4897-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c4897-108">DESCRIPTION</span></span>
<span data-ttu-id="c4897-109">Получите msixpackage.</span><span class="sxs-lookup"><span data-stu-id="c4897-109">Get a msixpackage.</span></span>

## <span data-ttu-id="c4897-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c4897-110">EXAMPLES</span></span>

### <span data-ttu-id="c4897-111">Пример 1. Получить пакет MSIX по имени</span><span class="sxs-lookup"><span data-stu-id="c4897-111">Example 1: Get a MSIX Package by Name</span></span>
```powershell
PS C:\> Get-AzWvdMsixPackage -HostPoolName HostPoolName -ResourceGroupName ResourceGroupName -SubscriptionId SubscriptionId -FullName PackageFullName

Name                                                  Type
----                                                  ----
HostPoolName/MSIXPackage_FullName                     Microsoft.DesktopVirtualization/hostpools/msixpackages
```

<span data-ttu-id="c4897-112">Эта команда получает пакет MSIX в hostPool.</span><span class="sxs-lookup"><span data-stu-id="c4897-112">This command gets a MSIX Package in a HostPool.</span></span>

### <span data-ttu-id="c4897-113">Пример 2. Список пакетов MSIX</span><span class="sxs-lookup"><span data-stu-id="c4897-113">Example 2: List MSIX Packages</span></span> 
```powershell
PS C:\> Get-AzWvdMsixPackage -HostPoolName HostPoolName -ResourceGroupName ResourceGroupName -SubscriptionId SubscriptionId

Name                                                  Type
----                                                  ----
HostPoolName/MSIXPackage_FullName1                    Microsoft.DesktopVirtualization/hostpools/msixpackages
HostPoolName/MSIXPackage_FullName2                    Microsoft.DesktopVirtualization/hostpools/msixpackages
HostPoolName/MSIXPackage_FullName3                    Microsoft.DesktopVirtualization/hostpools/msixpackages
```

<span data-ttu-id="c4897-114">Эта команда содержит список пакетов MSIX в hostPool.</span><span class="sxs-lookup"><span data-stu-id="c4897-114">This command Lists MSIX Packages in a HostPool.</span></span>

## <span data-ttu-id="c4897-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c4897-115">PARAMETERS</span></span>

### <span data-ttu-id="c4897-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4897-116">-DefaultProfile</span></span>
<span data-ttu-id="c4897-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c4897-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4897-118">-FullName</span><span class="sxs-lookup"><span data-stu-id="c4897-118">-FullName</span></span>
<span data-ttu-id="c4897-119">Название пакета MSIX для конкретной версии в указанном hostpool</span><span class="sxs-lookup"><span data-stu-id="c4897-119">The version specific package full name of the MSIX package within specified hostpool</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: MsixPackageFullName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4897-120">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="c4897-120">-HostPoolName</span></span>
<span data-ttu-id="c4897-121">Имя пула хостов в указанной группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="c4897-121">The name of the host pool within the specified resource group</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4897-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c4897-122">-InputObject</span></span>
<span data-ttu-id="c4897-123">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="c4897-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c4897-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4897-124">-ResourceGroupName</span></span>
<span data-ttu-id="c4897-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c4897-125">The name of the resource group.</span></span>
<span data-ttu-id="c4897-126">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="c4897-126">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4897-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c4897-127">-SubscriptionId</span></span>
<span data-ttu-id="c4897-128">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="c4897-128">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4897-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4897-129">CommonParameters</span></span>
<span data-ttu-id="c4897-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4897-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4897-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c4897-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4897-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c4897-132">INPUTS</span></span>

### <span data-ttu-id="c4897-133">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="c4897-133">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="c4897-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c4897-134">OUTPUTS</span></span>

### <span data-ttu-id="c4897-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IMsixPackage</span><span class="sxs-lookup"><span data-stu-id="c4897-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IMsixPackage</span></span>

## <span data-ttu-id="c4897-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c4897-136">NOTES</span></span>

<span data-ttu-id="c4897-137">ALIASES</span><span class="sxs-lookup"><span data-stu-id="c4897-137">ALIASES</span></span>

<span data-ttu-id="c4897-138">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="c4897-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c4897-139">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="c4897-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c4897-140">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c4897-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c4897-141">INPUTOBJECT <IDesktopVirtualizationIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="c4897-141">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c4897-142">`[ApplicationGroupName <String>]`: имя группы приложений</span><span class="sxs-lookup"><span data-stu-id="c4897-142">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="c4897-143">`[ApplicationName <String>]`: имя приложения в указанной группе приложений</span><span class="sxs-lookup"><span data-stu-id="c4897-143">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="c4897-144">`[DesktopName <String>]`: имя рабочего стола в указанной группе рабочего стола</span><span class="sxs-lookup"><span data-stu-id="c4897-144">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="c4897-145">`[HostPoolName <String>]`: имя пула хостов в указанной группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="c4897-145">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="c4897-146">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="c4897-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c4897-147">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span><span class="sxs-lookup"><span data-stu-id="c4897-147">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="c4897-148">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c4897-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="c4897-149">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="c4897-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="c4897-150">`[SessionHostName <String>]`: имя сеанса в указанном пуле хостов</span><span class="sxs-lookup"><span data-stu-id="c4897-150">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="c4897-151">`[SubscriptionId <String>]`: ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="c4897-151">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="c4897-152">`[UserSessionId <String>]`: имя сеанса пользователя в указанном хосте сеанса</span><span class="sxs-lookup"><span data-stu-id="c4897-152">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="c4897-153">`[WorkspaceName <String>]`: имя рабочей области</span><span class="sxs-lookup"><span data-stu-id="c4897-153">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="c4897-154">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c4897-154">RELATED LINKS</span></span>

