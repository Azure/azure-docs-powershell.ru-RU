---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdusersession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdUserSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdUserSession.md
ms.openlocfilehash: eedf639ebf5c25ff9153072a337ea659b41a9e92
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236731"
---
# <span data-ttu-id="a8712-101">Get-AzWvdUserSession</span><span class="sxs-lookup"><span data-stu-id="a8712-101">Get-AzWvdUserSession</span></span>

## <span data-ttu-id="a8712-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a8712-102">SYNOPSIS</span></span>
<span data-ttu-id="a8712-103">Получить userSession.</span><span class="sxs-lookup"><span data-stu-id="a8712-103">Get a userSession.</span></span>

## <span data-ttu-id="a8712-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a8712-104">SYNTAX</span></span>

### <span data-ttu-id="a8712-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a8712-105">List (Default)</span></span>
```
Get-AzWvdUserSession -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a8712-106">Получить</span><span class="sxs-lookup"><span data-stu-id="a8712-106">Get</span></span>
```
Get-AzWvdUserSession -HostPoolName <String> -Id <String> -ResourceGroupName <String> -SessionHostName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a8712-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a8712-107">GetViaIdentity</span></span>
```
Get-AzWvdUserSession -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="a8712-108">List1</span><span class="sxs-lookup"><span data-stu-id="a8712-108">List1</span></span>
```
Get-AzWvdUserSession -HostPoolName <String> -ResourceGroupName <String> -SessionHostName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="a8712-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a8712-109">DESCRIPTION</span></span>
<span data-ttu-id="a8712-110">Получить userSession.</span><span class="sxs-lookup"><span data-stu-id="a8712-110">Get a userSession.</span></span>

## <span data-ttu-id="a8712-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a8712-111">EXAMPLES</span></span>

### <span data-ttu-id="a8712-112">Пример 1: получение виртуального рабочего стола Windows UserSession по имени</span><span class="sxs-lookup"><span data-stu-id="a8712-112">Example 1: Get a Windows Virtual Desktop UserSession by name</span></span>
```powershell
PS C:\> Get-AzWvdUserSession -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -SessionHostName SessionHostName -Id 2

Name                           Type
----                           ----
HostPoolName/SessionHostName/2 Microsoft.DesktopVirtualization/hostpools/sessionhosts/usersessions
```

<span data-ttu-id="a8712-113">Эта команда получает UserSession виртуальных рабочих столов Windows на узле сеансов.</span><span class="sxs-lookup"><span data-stu-id="a8712-113">This command gets a Windows Virtual Desktop UserSession in a Session Host.</span></span>

### <span data-ttu-id="a8712-114">Пример 2: список виртуальных рабочих столов Windows UserSessions</span><span class="sxs-lookup"><span data-stu-id="a8712-114">Example 2: List Windows Virtual Desktop UserSessions</span></span>
```powershell
PS C:\> Get-AzWvdUserSession -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -SessionHostName SessionHostName

Name                           Type
----                           ----
HostPoolName/SessionHostName/2 Microsoft.DesktopVirtualization/hostpools/sessionhosts/usersessions
HostPoolName/SessionHostName/3 Microsoft.DesktopVirtualization/hostpools/sessionhosts/usersessions
```

<span data-ttu-id="a8712-115">Эта команда перечисляет UserSessions виртуальных рабочих столов Windows на узле сеансов.</span><span class="sxs-lookup"><span data-stu-id="a8712-115">This command lists a Windows Virtual Desktop UserSessions in a Session Host.</span></span>

### <span data-ttu-id="a8712-116">Пример 3: список виртуальных рабочих столов Windows UserSessions в пуле узлов</span><span class="sxs-lookup"><span data-stu-id="a8712-116">Example 3: List Windows Virtual Desktop UserSessions in host pool</span></span>
```powershell
PS C:\> Get-AzWvdUserSession -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName

Name                           Type
----                           ----
HostPoolName/SessionHostName/2 Microsoft.DesktopVirtualization/hostpools/sessionhosts/usersessions
HostPoolName/SessionHostName/3 Microsoft.DesktopVirtualization/hostpools/sessionhosts/usersessions
```

<span data-ttu-id="a8712-117">Эта команда перечисляет UserSessions виртуальных рабочих столов Windows на узле сеансов в пуле узлов.</span><span class="sxs-lookup"><span data-stu-id="a8712-117">This command lists a Windows Virtual Desktop UserSessions in a Session Host in a host pool.</span></span>

## <span data-ttu-id="a8712-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a8712-118">PARAMETERS</span></span>

### <span data-ttu-id="a8712-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8712-119">-DefaultProfile</span></span>
<span data-ttu-id="a8712-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a8712-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a8712-121">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="a8712-121">-Filter</span></span>
<span data-ttu-id="a8712-122">Выражение фильтра OData.</span><span class="sxs-lookup"><span data-stu-id="a8712-122">OData filter expression.</span></span>
<span data-ttu-id="a8712-123">Допустимыми свойствами для фильтрации являются userPrincipalName и sessionState.</span><span class="sxs-lookup"><span data-stu-id="a8712-123">Valid properties for filtering are userprincipalname and sessionstate.</span></span>

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

### <span data-ttu-id="a8712-124">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="a8712-124">-HostPoolName</span></span>
<span data-ttu-id="a8712-125">Имя пула узлов в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a8712-125">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="a8712-126">-ID</span><span class="sxs-lookup"><span data-stu-id="a8712-126">-Id</span></span>
<span data-ttu-id="a8712-127">Имя сеанса пользователя на указанном узле сеанса</span><span class="sxs-lookup"><span data-stu-id="a8712-127">The name of the user session within the specified session host</span></span>

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

### <span data-ttu-id="a8712-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a8712-128">-InputObject</span></span>
<span data-ttu-id="a8712-129">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="a8712-129">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a8712-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8712-130">-ResourceGroupName</span></span>
<span data-ttu-id="a8712-131">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a8712-131">The name of the resource group.</span></span>
<span data-ttu-id="a8712-132">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="a8712-132">The name is case insensitive.</span></span>

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

### <span data-ttu-id="a8712-133">-SessionHostName</span><span class="sxs-lookup"><span data-stu-id="a8712-133">-SessionHostName</span></span>
<span data-ttu-id="a8712-134">Имя узла сеанса в указанном пуле узлов.</span><span class="sxs-lookup"><span data-stu-id="a8712-134">The name of the session host within the specified host pool</span></span>

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

### <span data-ttu-id="a8712-135">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a8712-135">-SubscriptionId</span></span>
<span data-ttu-id="a8712-136">Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="a8712-136">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="a8712-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8712-137">CommonParameters</span></span>
<span data-ttu-id="a8712-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a8712-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8712-139">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a8712-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8712-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a8712-140">INPUTS</span></span>

### <span data-ttu-id="a8712-141">Microsoft. Azure. PowerShell. командлеты. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="a8712-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="a8712-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a8712-142">OUTPUTS</span></span>

### <span data-ttu-id="a8712-143">Microsoft. Azure. PowerShell. командлеты. DesktopVirtualization. Models. Api20191210Preview. IUserSession</span><span class="sxs-lookup"><span data-stu-id="a8712-143">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IUserSession</span></span>

## <span data-ttu-id="a8712-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="a8712-144">NOTES</span></span>

<span data-ttu-id="a8712-145">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="a8712-145">ALIASES</span></span>

<span data-ttu-id="a8712-146">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="a8712-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a8712-147">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="a8712-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a8712-148">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a8712-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a8712-149">INPUTOBJECT <IDesktopVirtualizationIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="a8712-149">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a8712-150">`[ApplicationGroupName <String>]`: Имя группы приложения.</span><span class="sxs-lookup"><span data-stu-id="a8712-150">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="a8712-151">`[ApplicationName <String>]`: Имя приложения в указанной группе приложения.</span><span class="sxs-lookup"><span data-stu-id="a8712-151">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="a8712-152">`[DesktopName <String>]`: Имя рабочего стола в пределах указанной группы рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="a8712-152">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="a8712-153">`[HostPoolName <String>]`: Имя пула узлов в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a8712-153">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="a8712-154">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="a8712-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a8712-155">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a8712-155">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="a8712-156">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="a8712-156">The name is case insensitive.</span></span>
  - <span data-ttu-id="a8712-157">`[SessionHostName <String>]`: Имя узла сеанса в указанном пуле узлов.</span><span class="sxs-lookup"><span data-stu-id="a8712-157">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="a8712-158">`[SubscriptionId <String>]`: Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="a8712-158">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="a8712-159">`[UserSessionId <String>]`: Имя сеанса пользователя на указанном узле сеансов</span><span class="sxs-lookup"><span data-stu-id="a8712-159">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="a8712-160">`[WorkspaceName <String>]`: Имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="a8712-160">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="a8712-161">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a8712-161">RELATED LINKS</span></span>

