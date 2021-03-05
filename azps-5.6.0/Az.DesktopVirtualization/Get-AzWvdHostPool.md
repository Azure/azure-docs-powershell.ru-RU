---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/get-azwvdhostpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdHostPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdHostPool.md
ms.openlocfilehash: 1ba4b3141b2254de9e1988fbd2b76f03a06ceb99
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101980579"
---
# <span data-ttu-id="c26fb-101">Get-AzWvdHostPool</span><span class="sxs-lookup"><span data-stu-id="c26fb-101">Get-AzWvdHostPool</span></span>

## <span data-ttu-id="c26fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c26fb-102">SYNOPSIS</span></span>
<span data-ttu-id="c26fb-103">Получить пул хостов.</span><span class="sxs-lookup"><span data-stu-id="c26fb-103">Get a host pool.</span></span>

## <span data-ttu-id="c26fb-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c26fb-104">SYNTAX</span></span>

### <span data-ttu-id="c26fb-105">Список1 (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c26fb-105">List1 (Default)</span></span>
```
Get-AzWvdHostPool [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c26fb-106">Получить</span><span class="sxs-lookup"><span data-stu-id="c26fb-106">Get</span></span>
```
Get-AzWvdHostPool -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c26fb-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="c26fb-107">GetViaIdentity</span></span>
```
Get-AzWvdHostPool -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="c26fb-108">Список</span><span class="sxs-lookup"><span data-stu-id="c26fb-108">List</span></span>
```
Get-AzWvdHostPool -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="c26fb-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c26fb-109">DESCRIPTION</span></span>
<span data-ttu-id="c26fb-110">Получить пул хостов.</span><span class="sxs-lookup"><span data-stu-id="c26fb-110">Get a host pool.</span></span>

## <span data-ttu-id="c26fb-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c26fb-111">EXAMPLES</span></span>

### <span data-ttu-id="c26fb-112">Пример 1. Получить виртуальный настольныйpool Windows по имени</span><span class="sxs-lookup"><span data-stu-id="c26fb-112">Example 1: Get a Windows Virtual Desktop HostPool by name</span></span>
```powershell
PS C:\> Get-AzWvdHostPool -ResourceGroupName ResourceGroupName -Name HostPoolName

Location   Name                 Type
--------   ----                 ----
eastus     HostPoolName Microsoft.DesktopVirtualization/hostpools
```

<span data-ttu-id="c26fb-113">Эта команда возвращает виртуальный рабочий стол Windows HostPool в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c26fb-113">This command gets a Windows Virtual Desktop HostPool in a Resource Group.</span></span>

### <span data-ttu-id="c26fb-114">Пример 2. Список виртуальных настольных систем (HostPools) Windows</span><span class="sxs-lookup"><span data-stu-id="c26fb-114">Example 2: List Windows Virtual Desktop HostPools</span></span>
```powershell
PS C:\> Get-AzWvdHostPool -ResourceGroupName ResourceGroupName

Location   Name          Type
--------   ----          ----
eastus     HostPoolName1 Microsoft.DesktopVirtualization/hostpools
eastus     HostPoolName2 Microsoft.DesktopVirtualization/hostpools
```

<span data-ttu-id="c26fb-115">Эта команда содержит список виртуальных настольных систем (HostPools) Windows в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c26fb-115">This command lists a Windows Virtual Desktop HostPools in a Resource Group.</span></span>

## <span data-ttu-id="c26fb-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c26fb-116">PARAMETERS</span></span>

### <span data-ttu-id="c26fb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c26fb-117">-DefaultProfile</span></span>
<span data-ttu-id="c26fb-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c26fb-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c26fb-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c26fb-119">-InputObject</span></span>
<span data-ttu-id="c26fb-120">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="c26fb-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="c26fb-121">-Name</span><span class="sxs-lookup"><span data-stu-id="c26fb-121">-Name</span></span>
<span data-ttu-id="c26fb-122">Имя пула хостов в указанной группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="c26fb-122">The name of the host pool within the specified resource group</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: HostPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c26fb-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c26fb-123">-ResourceGroupName</span></span>
<span data-ttu-id="c26fb-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c26fb-124">The name of the resource group.</span></span>
<span data-ttu-id="c26fb-125">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="c26fb-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="c26fb-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c26fb-126">-SubscriptionId</span></span>
<span data-ttu-id="c26fb-127">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="c26fb-127">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c26fb-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c26fb-128">CommonParameters</span></span>
<span data-ttu-id="c26fb-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c26fb-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c26fb-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c26fb-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c26fb-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c26fb-131">INPUTS</span></span>

### <span data-ttu-id="c26fb-132">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="c26fb-132">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="c26fb-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c26fb-133">OUTPUTS</span></span>

### <span data-ttu-id="c26fb-134">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IHostPool</span><span class="sxs-lookup"><span data-stu-id="c26fb-134">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IHostPool</span></span>

## <span data-ttu-id="c26fb-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c26fb-135">NOTES</span></span>

<span data-ttu-id="c26fb-136">ALIASES</span><span class="sxs-lookup"><span data-stu-id="c26fb-136">ALIASES</span></span>

<span data-ttu-id="c26fb-137">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="c26fb-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c26fb-138">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="c26fb-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c26fb-139">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c26fb-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c26fb-140">INPUTOBJECT <IDesktopVirtualizationIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="c26fb-140">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c26fb-141">`[ApplicationGroupName <String>]`: имя группы приложений</span><span class="sxs-lookup"><span data-stu-id="c26fb-141">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="c26fb-142">`[ApplicationName <String>]`: имя приложения в указанной группе приложений</span><span class="sxs-lookup"><span data-stu-id="c26fb-142">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="c26fb-143">`[DesktopName <String>]`: имя рабочего стола в указанной группе рабочего стола</span><span class="sxs-lookup"><span data-stu-id="c26fb-143">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="c26fb-144">`[HostPoolName <String>]`: имя пула хостов в указанной группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="c26fb-144">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="c26fb-145">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="c26fb-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c26fb-146">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span><span class="sxs-lookup"><span data-stu-id="c26fb-146">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="c26fb-147">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c26fb-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="c26fb-148">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="c26fb-148">The name is case insensitive.</span></span>
  - <span data-ttu-id="c26fb-149">`[SessionHostName <String>]`: имя сеанса в указанном пуле хостов</span><span class="sxs-lookup"><span data-stu-id="c26fb-149">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="c26fb-150">`[SubscriptionId <String>]`: ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="c26fb-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="c26fb-151">`[UserSessionId <String>]`: имя сеанса пользователя в указанном хосте сеанса</span><span class="sxs-lookup"><span data-stu-id="c26fb-151">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="c26fb-152">`[WorkspaceName <String>]`: имя рабочей области</span><span class="sxs-lookup"><span data-stu-id="c26fb-152">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="c26fb-153">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c26fb-153">RELATED LINKS</span></span>

