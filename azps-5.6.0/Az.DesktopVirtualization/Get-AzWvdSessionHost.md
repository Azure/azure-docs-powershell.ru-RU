---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/get-azwvdsessionhost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdSessionHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdSessionHost.md
ms.openlocfilehash: 1e7727933f01f1b2fa3196e3c195c25dda5c247b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101962019"
---
# <span data-ttu-id="23b12-101">Get-AzWvdSessionHost</span><span class="sxs-lookup"><span data-stu-id="23b12-101">Get-AzWvdSessionHost</span></span>

## <span data-ttu-id="23b12-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="23b12-102">SYNOPSIS</span></span>
<span data-ttu-id="23b12-103">Получите хост сеанса.</span><span class="sxs-lookup"><span data-stu-id="23b12-103">Get a session host.</span></span>

## <span data-ttu-id="23b12-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="23b12-104">SYNTAX</span></span>

### <span data-ttu-id="23b12-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="23b12-105">List (Default)</span></span>
```
Get-AzWvdSessionHost -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="23b12-106">Получить</span><span class="sxs-lookup"><span data-stu-id="23b12-106">Get</span></span>
```
Get-AzWvdSessionHost -HostPoolName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="23b12-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="23b12-107">GetViaIdentity</span></span>
```
Get-AzWvdSessionHost -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="23b12-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="23b12-108">DESCRIPTION</span></span>
<span data-ttu-id="23b12-109">Получите хост сеанса.</span><span class="sxs-lookup"><span data-stu-id="23b12-109">Get a session host.</span></span>

## <span data-ttu-id="23b12-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="23b12-110">EXAMPLES</span></span>

### <span data-ttu-id="23b12-111">Пример 1. Получить виртуальный рабочий стол Windows SessionHost по имени</span><span class="sxs-lookup"><span data-stu-id="23b12-111">Example 1: Get a Windows Virtual Desktop SessionHost by name</span></span>
```powershell
PS C:\> Get-AzWvdSessionHost -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -Name SessionHostName

Name                                               Type
----                                               ----
HostPoolName/SessionHostName Microsoft.DesktopVirtualization/hostpools/sessionhosts
```

<span data-ttu-id="23b12-112">Эта команда получает виртуальный рабочий стол SessionHost Windows в пуле хостов.</span><span class="sxs-lookup"><span data-stu-id="23b12-112">This command gets a Windows Virtual Desktop SessionHost in a Host Pool.</span></span>

### <span data-ttu-id="23b12-113">Пример 2. Список виртуальных рабочих столов Windows SessionHosts</span><span class="sxs-lookup"><span data-stu-id="23b12-113">Example 2: List Windows Virtual Desktop SessionHosts</span></span>
```powershell
PS C:\> Get-AzWvdSessionHost -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName

Name                                               Type
----                                               ----
HostPoolName/SessionHostName1 Microsoft.DesktopVirtualization/hostpools/sessionhosts
HostPoolName/SessionHostName2 Microsoft.DesktopVirtualization/hostpools/sessionhosts
```

<span data-ttu-id="23b12-114">Эта команда содержит список виртуальных рабочих окон SessionHosts в пуле хостов.</span><span class="sxs-lookup"><span data-stu-id="23b12-114">This command lists a Windows Virtual Desktop SessionHosts in a Host Pool.</span></span>

## <span data-ttu-id="23b12-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="23b12-115">PARAMETERS</span></span>

### <span data-ttu-id="23b12-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23b12-116">-DefaultProfile</span></span>
<span data-ttu-id="23b12-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="23b12-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23b12-118">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="23b12-118">-HostPoolName</span></span>
<span data-ttu-id="23b12-119">Имя пула хостов в указанной группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="23b12-119">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="23b12-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="23b12-120">-InputObject</span></span>
<span data-ttu-id="23b12-121">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="23b12-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="23b12-122">-Name</span><span class="sxs-lookup"><span data-stu-id="23b12-122">-Name</span></span>
<span data-ttu-id="23b12-123">Имя сеанса в указанном пуле хостов</span><span class="sxs-lookup"><span data-stu-id="23b12-123">The name of the session host within the specified host pool</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: SessionHostName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23b12-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23b12-124">-ResourceGroupName</span></span>
<span data-ttu-id="23b12-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="23b12-125">The name of the resource group.</span></span>
<span data-ttu-id="23b12-126">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="23b12-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="23b12-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="23b12-127">-SubscriptionId</span></span>
<span data-ttu-id="23b12-128">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="23b12-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="23b12-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23b12-129">CommonParameters</span></span>
<span data-ttu-id="23b12-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23b12-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23b12-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="23b12-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23b12-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="23b12-132">INPUTS</span></span>

### <span data-ttu-id="23b12-133">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="23b12-133">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="23b12-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="23b12-134">OUTPUTS</span></span>

### <span data-ttu-id="23b12-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.ISessionHost</span><span class="sxs-lookup"><span data-stu-id="23b12-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.ISessionHost</span></span>

## <span data-ttu-id="23b12-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="23b12-136">NOTES</span></span>

<span data-ttu-id="23b12-137">ALIASES</span><span class="sxs-lookup"><span data-stu-id="23b12-137">ALIASES</span></span>

<span data-ttu-id="23b12-138">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="23b12-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="23b12-139">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="23b12-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="23b12-140">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="23b12-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="23b12-141">INPUTOBJECT <IDesktopVirtualizationIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="23b12-141">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="23b12-142">`[ApplicationGroupName <String>]`: имя группы приложений</span><span class="sxs-lookup"><span data-stu-id="23b12-142">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="23b12-143">`[ApplicationName <String>]`: имя приложения в указанной группе приложений</span><span class="sxs-lookup"><span data-stu-id="23b12-143">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="23b12-144">`[DesktopName <String>]`: имя рабочего стола в указанной группе рабочего стола</span><span class="sxs-lookup"><span data-stu-id="23b12-144">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="23b12-145">`[HostPoolName <String>]`: имя пула хостов в указанной группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="23b12-145">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="23b12-146">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="23b12-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="23b12-147">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span><span class="sxs-lookup"><span data-stu-id="23b12-147">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="23b12-148">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="23b12-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="23b12-149">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="23b12-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="23b12-150">`[SessionHostName <String>]`: имя сеанса в указанном пуле хостов</span><span class="sxs-lookup"><span data-stu-id="23b12-150">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="23b12-151">`[SubscriptionId <String>]`: ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="23b12-151">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="23b12-152">`[UserSessionId <String>]`: имя сеанса пользователя в указанном хосте сеанса</span><span class="sxs-lookup"><span data-stu-id="23b12-152">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="23b12-153">`[WorkspaceName <String>]`: имя рабочей области</span><span class="sxs-lookup"><span data-stu-id="23b12-153">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="23b12-154">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="23b12-154">RELATED LINKS</span></span>

