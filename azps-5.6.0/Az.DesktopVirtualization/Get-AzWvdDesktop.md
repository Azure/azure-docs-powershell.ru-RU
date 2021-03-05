---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/get-azwvddesktop
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdDesktop.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdDesktop.md
ms.openlocfilehash: 2c276ab6b791d041000adf872bf2bfb807032ff2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101980584"
---
# <span data-ttu-id="b5f3c-101">Get-AzWvdDesktop</span><span class="sxs-lookup"><span data-stu-id="b5f3c-101">Get-AzWvdDesktop</span></span>

## <span data-ttu-id="b5f3c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5f3c-102">SYNOPSIS</span></span>
<span data-ttu-id="b5f3c-103">Получите рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="b5f3c-103">Get a desktop.</span></span>

## <span data-ttu-id="b5f3c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b5f3c-104">SYNTAX</span></span>

### <span data-ttu-id="b5f3c-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b5f3c-105">List (Default)</span></span>
```
Get-AzWvdDesktop -ApplicationGroupName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b5f3c-106">Получить</span><span class="sxs-lookup"><span data-stu-id="b5f3c-106">Get</span></span>
```
Get-AzWvdDesktop -ApplicationGroupName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b5f3c-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b5f3c-107">GetViaIdentity</span></span>
```
Get-AzWvdDesktop -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="b5f3c-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b5f3c-108">DESCRIPTION</span></span>
<span data-ttu-id="b5f3c-109">Получите рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="b5f3c-109">Get a desktop.</span></span>

## <span data-ttu-id="b5f3c-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b5f3c-110">EXAMPLES</span></span>

### <span data-ttu-id="b5f3c-111">Пример 1. Получить виртуальный рабочий стол Windows по имени</span><span class="sxs-lookup"><span data-stu-id="b5f3c-111">Example 1: Get a Windows Virtual Desktop Desktop by name</span></span>
```powershell
PS C:\> Get-AzWvdDesktop -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName -Name DesktopName

Name                             Type
----                             ----
ApplicationGroupName/DesktopName Microsoft.DesktopVirtualization/applicationgroups/desktops
```

<span data-ttu-id="b5f3c-112">Эта команда возвращает виртуальный рабочий стол Windows в соответствующей группе.</span><span class="sxs-lookup"><span data-stu-id="b5f3c-112">This command gets a Windows Virtual Desktop Desktop in an applicaton Group.</span></span>

### <span data-ttu-id="b5f3c-113">Пример 2. Список виртуальных рабочих столов Windows</span><span class="sxs-lookup"><span data-stu-id="b5f3c-113">Example 2: List Windows Virtual Desktop Desktops</span></span>
```powershell
PS C:\> Get-AzWvdDesktop -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName

Name                             Type
----                             ----
ApplicationGroupName/DesktopName Microsoft.DesktopVirtualization/applicationgroups/desktops
```

<span data-ttu-id="b5f3c-114">Эта команда содержит список виртуальных рабочих столаWindows в соответствующей группе.</span><span class="sxs-lookup"><span data-stu-id="b5f3c-114">This command listsWindows Virtual Desktop Desktops in an applicaton Group.</span></span>

## <span data-ttu-id="b5f3c-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b5f3c-115">PARAMETERS</span></span>

### <span data-ttu-id="b5f3c-116">-ApplicationGroupName</span><span class="sxs-lookup"><span data-stu-id="b5f3c-116">-ApplicationGroupName</span></span>
<span data-ttu-id="b5f3c-117">Имя группы приложений</span><span class="sxs-lookup"><span data-stu-id="b5f3c-117">The name of the application group</span></span>

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

### <span data-ttu-id="b5f3c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5f3c-118">-DefaultProfile</span></span>
<span data-ttu-id="b5f3c-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b5f3c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b5f3c-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b5f3c-120">-InputObject</span></span>
<span data-ttu-id="b5f3c-121">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="b5f3c-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b5f3c-122">-Name</span><span class="sxs-lookup"><span data-stu-id="b5f3c-122">-Name</span></span>
<span data-ttu-id="b5f3c-123">Имя рабочего стола в указанной группе рабочего стола</span><span class="sxs-lookup"><span data-stu-id="b5f3c-123">The name of the desktop within the specified desktop group</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: DesktopName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5f3c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5f3c-124">-ResourceGroupName</span></span>
<span data-ttu-id="b5f3c-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b5f3c-125">The name of the resource group.</span></span>
<span data-ttu-id="b5f3c-126">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="b5f3c-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="b5f3c-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b5f3c-127">-SubscriptionId</span></span>
<span data-ttu-id="b5f3c-128">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="b5f3c-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="b5f3c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5f3c-129">CommonParameters</span></span>
<span data-ttu-id="b5f3c-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5f3c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5f3c-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b5f3c-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5f3c-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b5f3c-132">INPUTS</span></span>

### <span data-ttu-id="b5f3c-133">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="b5f3c-133">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="b5f3c-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b5f3c-134">OUTPUTS</span></span>

### <span data-ttu-id="b5f3c-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IDesktop</span><span class="sxs-lookup"><span data-stu-id="b5f3c-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IDesktop</span></span>

### <span data-ttu-id="b5f3c-136">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IDesktopList</span><span class="sxs-lookup"><span data-stu-id="b5f3c-136">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IDesktopList</span></span>

## <span data-ttu-id="b5f3c-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b5f3c-137">NOTES</span></span>

<span data-ttu-id="b5f3c-138">ALIASES</span><span class="sxs-lookup"><span data-stu-id="b5f3c-138">ALIASES</span></span>

<span data-ttu-id="b5f3c-139">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="b5f3c-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b5f3c-140">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="b5f3c-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b5f3c-141">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b5f3c-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b5f3c-142">INPUTOBJECT <IDesktopVirtualizationIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="b5f3c-142">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b5f3c-143">`[ApplicationGroupName <String>]`: имя группы приложений</span><span class="sxs-lookup"><span data-stu-id="b5f3c-143">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="b5f3c-144">`[ApplicationName <String>]`: имя приложения в указанной группе приложений</span><span class="sxs-lookup"><span data-stu-id="b5f3c-144">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="b5f3c-145">`[DesktopName <String>]`: имя рабочего стола в указанной группе рабочего стола</span><span class="sxs-lookup"><span data-stu-id="b5f3c-145">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="b5f3c-146">`[HostPoolName <String>]`: имя пула хостов в указанной группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="b5f3c-146">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="b5f3c-147">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="b5f3c-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b5f3c-148">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span><span class="sxs-lookup"><span data-stu-id="b5f3c-148">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="b5f3c-149">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b5f3c-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="b5f3c-150">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="b5f3c-150">The name is case insensitive.</span></span>
  - <span data-ttu-id="b5f3c-151">`[SessionHostName <String>]`: имя сеанса в указанном пуле хостов</span><span class="sxs-lookup"><span data-stu-id="b5f3c-151">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="b5f3c-152">`[SubscriptionId <String>]`: ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="b5f3c-152">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="b5f3c-153">`[UserSessionId <String>]`: имя сеанса пользователя в указанном хосте сеанса</span><span class="sxs-lookup"><span data-stu-id="b5f3c-153">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="b5f3c-154">`[WorkspaceName <String>]`: имя рабочей области</span><span class="sxs-lookup"><span data-stu-id="b5f3c-154">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="b5f3c-155">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b5f3c-155">RELATED LINKS</span></span>

