---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdsessionhost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdSessionHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdSessionHost.md
ms.openlocfilehash: 806bd45ca4a9c3332388214ef146772c19282355
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98391716"
---
# <span data-ttu-id="49628-101">Get-AzWvdSessionHost</span><span class="sxs-lookup"><span data-stu-id="49628-101">Get-AzWvdSessionHost</span></span>

## <span data-ttu-id="49628-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49628-102">SYNOPSIS</span></span>
<span data-ttu-id="49628-103">Получите хост сеанса.</span><span class="sxs-lookup"><span data-stu-id="49628-103">Get a session host.</span></span>

## <span data-ttu-id="49628-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="49628-104">SYNTAX</span></span>

### <span data-ttu-id="49628-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="49628-105">List (Default)</span></span>
```
Get-AzWvdSessionHost -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="49628-106">Получить</span><span class="sxs-lookup"><span data-stu-id="49628-106">Get</span></span>
```
Get-AzWvdSessionHost -HostPoolName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="49628-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="49628-107">GetViaIdentity</span></span>
```
Get-AzWvdSessionHost -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="49628-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="49628-108">DESCRIPTION</span></span>
<span data-ttu-id="49628-109">Получите хост сеанса.</span><span class="sxs-lookup"><span data-stu-id="49628-109">Get a session host.</span></span>

## <span data-ttu-id="49628-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="49628-110">EXAMPLES</span></span>

### <span data-ttu-id="49628-111">Пример 1. Получить виртуальный рабочий стол Windows SessionHost по имени</span><span class="sxs-lookup"><span data-stu-id="49628-111">Example 1: Get a Windows Virtual Desktop SessionHost by name</span></span>
```powershell
PS C:\> Get-AzWvdSessionHost -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -Name SessionHostName

Name                                               Type
----                                               ----
HostPoolName/SessionHostName Microsoft.DesktopVirtualization/hostpools/sessionhosts
```

<span data-ttu-id="49628-112">Эта команда получает виртуальный рабочий стол SessionHost Windows в пуле хостов.</span><span class="sxs-lookup"><span data-stu-id="49628-112">This command gets a Windows Virtual Desktop SessionHost in a Host Pool.</span></span>

### <span data-ttu-id="49628-113">Пример 2. Список виртуальных рабочих столов Windows SessionHosts</span><span class="sxs-lookup"><span data-stu-id="49628-113">Example 2: List Windows Virtual Desktop SessionHosts</span></span>
```powershell
PS C:\> Get-AzWvdSessionHost -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName

Name                                               Type
----                                               ----
HostPoolName/SessionHostName1 Microsoft.DesktopVirtualization/hostpools/sessionhosts
HostPoolName/SessionHostName2 Microsoft.DesktopVirtualization/hostpools/sessionhosts
```

<span data-ttu-id="49628-114">Эта команда содержит список виртуальных рабочих окон SessionHosts в пуле хостов.</span><span class="sxs-lookup"><span data-stu-id="49628-114">This command lists a Windows Virtual Desktop SessionHosts in a Host Pool.</span></span>

## <span data-ttu-id="49628-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="49628-115">PARAMETERS</span></span>

### <span data-ttu-id="49628-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49628-116">-DefaultProfile</span></span>
<span data-ttu-id="49628-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="49628-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49628-118">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="49628-118">-HostPoolName</span></span>
<span data-ttu-id="49628-119">Имя пула хостов в указанной группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="49628-119">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="49628-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="49628-120">-InputObject</span></span>
<span data-ttu-id="49628-121">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="49628-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="49628-122">-Name</span><span class="sxs-lookup"><span data-stu-id="49628-122">-Name</span></span>
<span data-ttu-id="49628-123">Имя сеанса в указанном пуле хостов</span><span class="sxs-lookup"><span data-stu-id="49628-123">The name of the session host within the specified host pool</span></span>

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

### <span data-ttu-id="49628-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49628-124">-ResourceGroupName</span></span>
<span data-ttu-id="49628-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="49628-125">The name of the resource group.</span></span>
<span data-ttu-id="49628-126">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="49628-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="49628-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="49628-127">-SubscriptionId</span></span>
<span data-ttu-id="49628-128">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="49628-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="49628-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49628-129">CommonParameters</span></span>
<span data-ttu-id="49628-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49628-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49628-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="49628-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49628-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="49628-132">INPUTS</span></span>

### <span data-ttu-id="49628-133">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="49628-133">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="49628-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="49628-134">OUTPUTS</span></span>

### <span data-ttu-id="49628-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.ISessionHost</span><span class="sxs-lookup"><span data-stu-id="49628-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.ISessionHost</span></span>

## <span data-ttu-id="49628-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="49628-136">NOTES</span></span>

<span data-ttu-id="49628-137">ALIASES</span><span class="sxs-lookup"><span data-stu-id="49628-137">ALIASES</span></span>

<span data-ttu-id="49628-138">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="49628-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="49628-139">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="49628-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="49628-140">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="49628-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="49628-141">INPUTOBJECT <IDesktopVirtualizationIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="49628-141">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="49628-142">`[ApplicationGroupName <String>]`: имя группы приложений</span><span class="sxs-lookup"><span data-stu-id="49628-142">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="49628-143">`[ApplicationName <String>]`: имя приложения в указанной группе приложений</span><span class="sxs-lookup"><span data-stu-id="49628-143">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="49628-144">`[DesktopName <String>]`: имя рабочего стола в указанной группе рабочего стола</span><span class="sxs-lookup"><span data-stu-id="49628-144">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="49628-145">`[HostPoolName <String>]`: имя пула хостов в указанной группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="49628-145">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="49628-146">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="49628-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="49628-147">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span><span class="sxs-lookup"><span data-stu-id="49628-147">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="49628-148">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="49628-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="49628-149">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="49628-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="49628-150">`[SessionHostName <String>]`: имя сеанса в указанном пуле хостов</span><span class="sxs-lookup"><span data-stu-id="49628-150">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="49628-151">`[SubscriptionId <String>]`: ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="49628-151">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="49628-152">`[UserSessionId <String>]`: имя сеанса пользователя в указанном хосте сеанса</span><span class="sxs-lookup"><span data-stu-id="49628-152">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="49628-153">`[WorkspaceName <String>]`: имя рабочей области</span><span class="sxs-lookup"><span data-stu-id="49628-153">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="49628-154">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="49628-154">RELATED LINKS</span></span>

