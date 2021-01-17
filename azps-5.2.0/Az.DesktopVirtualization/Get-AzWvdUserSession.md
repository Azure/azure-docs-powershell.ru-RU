---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdusersession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdUserSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdUserSession.md
ms.openlocfilehash: 0b0a044b9521236c3a29e7deffa15840b6d039ef
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98416183"
---
# <span data-ttu-id="a2456-101">Get-AzWvdUserSession</span><span class="sxs-lookup"><span data-stu-id="a2456-101">Get-AzWvdUserSession</span></span>

## <span data-ttu-id="a2456-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a2456-102">SYNOPSIS</span></span>
<span data-ttu-id="a2456-103">Получить userSession.</span><span class="sxs-lookup"><span data-stu-id="a2456-103">Get a userSession.</span></span>

## <span data-ttu-id="a2456-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a2456-104">SYNTAX</span></span>

### <span data-ttu-id="a2456-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a2456-105">List (Default)</span></span>
```
Get-AzWvdUserSession -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a2456-106">Получить</span><span class="sxs-lookup"><span data-stu-id="a2456-106">Get</span></span>
```
Get-AzWvdUserSession -HostPoolName <String> -Id <String> -ResourceGroupName <String> -SessionHostName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a2456-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a2456-107">GetViaIdentity</span></span>
```
Get-AzWvdUserSession -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="a2456-108">List1</span><span class="sxs-lookup"><span data-stu-id="a2456-108">List1</span></span>
```
Get-AzWvdUserSession -HostPoolName <String> -ResourceGroupName <String> -SessionHostName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="a2456-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a2456-109">DESCRIPTION</span></span>
<span data-ttu-id="a2456-110">Получить userSession.</span><span class="sxs-lookup"><span data-stu-id="a2456-110">Get a userSession.</span></span>

## <span data-ttu-id="a2456-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a2456-111">EXAMPLES</span></span>

### <span data-ttu-id="a2456-112">Пример 1. Get a Windows Virtual Desktop UserSession by name</span><span class="sxs-lookup"><span data-stu-id="a2456-112">Example 1: Get a Windows Virtual Desktop UserSession by name</span></span>
```powershell
PS C:\> Get-AzWvdUserSession -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -SessionHostName SessionHostName -Id 2

Name                           Type
----                           ----
HostPoolName/SessionHostName/2 Microsoft.DesktopVirtualization/hostpools/sessionhosts/usersessions
```

<span data-ttu-id="a2456-113">Эта команда получает окно userSession виртуального рабочего стола Windows на рабочем столе.</span><span class="sxs-lookup"><span data-stu-id="a2456-113">This command gets a Windows Virtual Desktop UserSession in a Session Host.</span></span>

### <span data-ttu-id="a2456-114">Пример 2. List Windows Virtual Desktop UserSessions</span><span class="sxs-lookup"><span data-stu-id="a2456-114">Example 2: List Windows Virtual Desktop UserSessions</span></span>
```powershell
PS C:\> Get-AzWvdUserSession -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -SessionHostName SessionHostName

Name                           Type
----                           ----
HostPoolName/SessionHostName/2 Microsoft.DesktopVirtualization/hostpools/sessionhosts/usersessions
HostPoolName/SessionHostName/3 Microsoft.DesktopVirtualization/hostpools/sessionhosts/usersessions
```

<span data-ttu-id="a2456-115">Эта команда содержит список userSessions виртуального рабочего стола Windows на рабочем столе.</span><span class="sxs-lookup"><span data-stu-id="a2456-115">This command lists a Windows Virtual Desktop UserSessions in a Session Host.</span></span>

### <span data-ttu-id="a2456-116">Пример 3. List Windows Virtual Desktop UserSessions in host pool</span><span class="sxs-lookup"><span data-stu-id="a2456-116">Example 3: List Windows Virtual Desktop UserSessions in host pool</span></span>
```powershell
PS C:\> Get-AzWvdUserSession -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName

Name                           Type
----                           ----
HostPoolName/SessionHostName/2 Microsoft.DesktopVirtualization/hostpools/sessionhosts/usersessions
HostPoolName/SessionHostName/3 Microsoft.DesktopVirtualization/hostpools/sessionhosts/usersessions
```

<span data-ttu-id="a2456-117">Эта команда содержит список userSessions виртуального рабочего стола Windows в хост-сеансе в пуле хостов.</span><span class="sxs-lookup"><span data-stu-id="a2456-117">This command lists a Windows Virtual Desktop UserSessions in a Session Host in a host pool.</span></span>

## <span data-ttu-id="a2456-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a2456-118">PARAMETERS</span></span>

### <span data-ttu-id="a2456-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2456-119">-DefaultProfile</span></span>
<span data-ttu-id="a2456-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a2456-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2456-121">-Filter</span><span class="sxs-lookup"><span data-stu-id="a2456-121">-Filter</span></span>
<span data-ttu-id="a2456-122">Выражение фильтра OData.</span><span class="sxs-lookup"><span data-stu-id="a2456-122">OData filter expression.</span></span>
<span data-ttu-id="a2456-123">Допустимые свойства фильтрации: userprincipalname и sessionstate.</span><span class="sxs-lookup"><span data-stu-id="a2456-123">Valid properties for filtering are userprincipalname and sessionstate.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2456-124">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="a2456-124">-HostPoolName</span></span>
<span data-ttu-id="a2456-125">Имя пула хостов в указанной группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="a2456-125">The name of the host pool within the specified resource group</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2456-126">-Id</span><span class="sxs-lookup"><span data-stu-id="a2456-126">-Id</span></span>
<span data-ttu-id="a2456-127">Имя сеанса пользователя в заданном хосте сеанса</span><span class="sxs-lookup"><span data-stu-id="a2456-127">The name of the user session within the specified session host</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: UserSessionId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2456-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a2456-128">-InputObject</span></span>
<span data-ttu-id="a2456-129">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="a2456-129">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a2456-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2456-130">-ResourceGroupName</span></span>
<span data-ttu-id="a2456-131">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a2456-131">The name of the resource group.</span></span>
<span data-ttu-id="a2456-132">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="a2456-132">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2456-133">-SessionHostName</span><span class="sxs-lookup"><span data-stu-id="a2456-133">-SessionHostName</span></span>
<span data-ttu-id="a2456-134">Имя сеанса в указанном пуле хостов</span><span class="sxs-lookup"><span data-stu-id="a2456-134">The name of the session host within the specified host pool</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2456-135">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a2456-135">-SubscriptionId</span></span>
<span data-ttu-id="a2456-136">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="a2456-136">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="a2456-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2456-137">CommonParameters</span></span>
<span data-ttu-id="a2456-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2456-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2456-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a2456-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2456-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a2456-140">INPUTS</span></span>

### <span data-ttu-id="a2456-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="a2456-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="a2456-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a2456-142">OUTPUTS</span></span>

### <span data-ttu-id="a2456-143">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IUserSession</span><span class="sxs-lookup"><span data-stu-id="a2456-143">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IUserSession</span></span>

## <span data-ttu-id="a2456-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a2456-144">NOTES</span></span>

<span data-ttu-id="a2456-145">ALIASES</span><span class="sxs-lookup"><span data-stu-id="a2456-145">ALIASES</span></span>

<span data-ttu-id="a2456-146">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="a2456-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a2456-147">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="a2456-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a2456-148">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a2456-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a2456-149">INPUTOBJECT <IDesktopVirtualizationIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="a2456-149">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a2456-150">`[ApplicationGroupName <String>]`: имя группы приложений</span><span class="sxs-lookup"><span data-stu-id="a2456-150">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="a2456-151">`[ApplicationName <String>]`: имя приложения в указанной группе приложений</span><span class="sxs-lookup"><span data-stu-id="a2456-151">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="a2456-152">`[DesktopName <String>]`: имя рабочего стола в указанной группе рабочего стола</span><span class="sxs-lookup"><span data-stu-id="a2456-152">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="a2456-153">`[HostPoolName <String>]`: имя пула хостов в указанной группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="a2456-153">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="a2456-154">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="a2456-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a2456-155">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span><span class="sxs-lookup"><span data-stu-id="a2456-155">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="a2456-156">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a2456-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="a2456-157">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="a2456-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="a2456-158">`[SessionHostName <String>]`: имя сеанса в указанном пуле хостов</span><span class="sxs-lookup"><span data-stu-id="a2456-158">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="a2456-159">`[SubscriptionId <String>]`: ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="a2456-159">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="a2456-160">`[UserSessionId <String>]`: имя сеанса пользователя в указанном хосте сеанса</span><span class="sxs-lookup"><span data-stu-id="a2456-160">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="a2456-161">`[WorkspaceName <String>]`: имя рабочей области</span><span class="sxs-lookup"><span data-stu-id="a2456-161">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="a2456-162">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a2456-162">RELATED LINKS</span></span>

