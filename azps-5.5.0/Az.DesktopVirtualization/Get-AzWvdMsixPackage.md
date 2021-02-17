---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdmsixpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdMsixPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdMsixPackage.md
ms.openlocfilehash: 51b940df2ee26c3da53c34fd7f1ffa25d3a266a9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100234577"
---
# <span data-ttu-id="8d9cf-101">Get-AzWvdMsixPackage</span><span class="sxs-lookup"><span data-stu-id="8d9cf-101">Get-AzWvdMsixPackage</span></span>

## <span data-ttu-id="8d9cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d9cf-102">SYNOPSIS</span></span>
<span data-ttu-id="8d9cf-103">Получите msixpackage.</span><span class="sxs-lookup"><span data-stu-id="8d9cf-103">Get a msixpackage.</span></span>

## <span data-ttu-id="8d9cf-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8d9cf-104">SYNTAX</span></span>

### <span data-ttu-id="8d9cf-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8d9cf-105">List (Default)</span></span>
```
Get-AzWvdMsixPackage -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="8d9cf-106">Получить</span><span class="sxs-lookup"><span data-stu-id="8d9cf-106">Get</span></span>
```
Get-AzWvdMsixPackage -FullName <String> -HostPoolName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="8d9cf-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="8d9cf-107">GetViaIdentity</span></span>
```
Get-AzWvdMsixPackage -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="8d9cf-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8d9cf-108">DESCRIPTION</span></span>
<span data-ttu-id="8d9cf-109">Получите msixpackage.</span><span class="sxs-lookup"><span data-stu-id="8d9cf-109">Get a msixpackage.</span></span>

## <span data-ttu-id="8d9cf-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8d9cf-110">EXAMPLES</span></span>

### <span data-ttu-id="8d9cf-111">Пример 1. Получить пакет MSIX по имени</span><span class="sxs-lookup"><span data-stu-id="8d9cf-111">Example 1: Get a MSIX Package by Name</span></span>
```powershell
PS C:\> Get-AzWvdMsixPackage -HostPoolName HostPoolName -ResourceGroupName ResourceGroupName -SubscriptionId SubscriptionId -FullName PackageFullName

Name                                                  Type
----                                                  ----
HostPoolName/MSIXPackage_FullName                     Microsoft.DesktopVirtualization/hostpools/msixpackages
```

<span data-ttu-id="8d9cf-112">Эта команда получает пакет MSIX в hostPool.</span><span class="sxs-lookup"><span data-stu-id="8d9cf-112">This command gets a MSIX Package in a HostPool.</span></span>

### <span data-ttu-id="8d9cf-113">Пример 2. Список пакетов MSIX</span><span class="sxs-lookup"><span data-stu-id="8d9cf-113">Example 2: List MSIX Packages</span></span> 
```powershell
PS C:\> Get-AzWvdMsixPackage -HostPoolName HostPoolName -ResourceGroupName ResourceGroupName -SubscriptionId SubscriptionId

Name                                                  Type
----                                                  ----
HostPoolName/MSIXPackage_FullName1                    Microsoft.DesktopVirtualization/hostpools/msixpackages
HostPoolName/MSIXPackage_FullName2                    Microsoft.DesktopVirtualization/hostpools/msixpackages
HostPoolName/MSIXPackage_FullName3                    Microsoft.DesktopVirtualization/hostpools/msixpackages
```

<span data-ttu-id="8d9cf-114">Эта команда содержит список пакетов MSIX в hostPool.</span><span class="sxs-lookup"><span data-stu-id="8d9cf-114">This command Lists MSIX Packages in a HostPool.</span></span>

## <span data-ttu-id="8d9cf-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8d9cf-115">PARAMETERS</span></span>

### <span data-ttu-id="8d9cf-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d9cf-116">-DefaultProfile</span></span>
<span data-ttu-id="8d9cf-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8d9cf-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d9cf-118">-FullName</span><span class="sxs-lookup"><span data-stu-id="8d9cf-118">-FullName</span></span>
<span data-ttu-id="8d9cf-119">Полное имя пакета MSIX для версии в указанном хостпаке</span><span class="sxs-lookup"><span data-stu-id="8d9cf-119">The version specific package full name of the MSIX package within specified hostpool</span></span>

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

### <span data-ttu-id="8d9cf-120">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="8d9cf-120">-HostPoolName</span></span>
<span data-ttu-id="8d9cf-121">Имя пула хостов в указанной группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="8d9cf-121">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="8d9cf-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8d9cf-122">-InputObject</span></span>
<span data-ttu-id="8d9cf-123">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="8d9cf-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="8d9cf-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d9cf-124">-ResourceGroupName</span></span>
<span data-ttu-id="8d9cf-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8d9cf-125">The name of the resource group.</span></span>
<span data-ttu-id="8d9cf-126">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="8d9cf-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="8d9cf-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8d9cf-127">-SubscriptionId</span></span>
<span data-ttu-id="8d9cf-128">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="8d9cf-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="8d9cf-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d9cf-129">CommonParameters</span></span>
<span data-ttu-id="8d9cf-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d9cf-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d9cf-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8d9cf-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d9cf-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8d9cf-132">INPUTS</span></span>

### <span data-ttu-id="8d9cf-133">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="8d9cf-133">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="8d9cf-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8d9cf-134">OUTPUTS</span></span>

### <span data-ttu-id="8d9cf-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IMsixPackage</span><span class="sxs-lookup"><span data-stu-id="8d9cf-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IMsixPackage</span></span>

## <span data-ttu-id="8d9cf-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8d9cf-136">NOTES</span></span>

<span data-ttu-id="8d9cf-137">ALIASES</span><span class="sxs-lookup"><span data-stu-id="8d9cf-137">ALIASES</span></span>

<span data-ttu-id="8d9cf-138">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="8d9cf-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8d9cf-139">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="8d9cf-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8d9cf-140">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8d9cf-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8d9cf-141">INPUTOBJECT <IDesktopVirtualizationIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="8d9cf-141">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8d9cf-142">`[ApplicationGroupName <String>]`: имя группы приложений</span><span class="sxs-lookup"><span data-stu-id="8d9cf-142">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="8d9cf-143">`[ApplicationName <String>]`: имя приложения в указанной группе приложений</span><span class="sxs-lookup"><span data-stu-id="8d9cf-143">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="8d9cf-144">`[DesktopName <String>]`: имя рабочего стола в указанной группе рабочего стола</span><span class="sxs-lookup"><span data-stu-id="8d9cf-144">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="8d9cf-145">`[HostPoolName <String>]`: имя пула хостов в указанной группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="8d9cf-145">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="8d9cf-146">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="8d9cf-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8d9cf-147">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span><span class="sxs-lookup"><span data-stu-id="8d9cf-147">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="8d9cf-148">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8d9cf-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="8d9cf-149">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="8d9cf-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="8d9cf-150">`[SessionHostName <String>]`: имя сеанса в указанном пуле хостов</span><span class="sxs-lookup"><span data-stu-id="8d9cf-150">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="8d9cf-151">`[SubscriptionId <String>]`: ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="8d9cf-151">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="8d9cf-152">`[UserSessionId <String>]`: имя сеанса пользователя в указанном хосте сеанса</span><span class="sxs-lookup"><span data-stu-id="8d9cf-152">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="8d9cf-153">`[WorkspaceName <String>]`: имя рабочей области</span><span class="sxs-lookup"><span data-stu-id="8d9cf-153">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="8d9cf-154">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8d9cf-154">RELATED LINKS</span></span>

