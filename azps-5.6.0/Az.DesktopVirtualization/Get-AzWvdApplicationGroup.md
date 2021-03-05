---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/get-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdApplicationGroup.md
ms.openlocfilehash: e5cef84d4ae45e4ce55b1f377ab16edc2449c72c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101962051"
---
# <span data-ttu-id="95ac2-101">Get-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="95ac2-101">Get-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="95ac2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95ac2-102">SYNOPSIS</span></span>
<span data-ttu-id="95ac2-103">Получите группу приложений.</span><span class="sxs-lookup"><span data-stu-id="95ac2-103">Get an application group.</span></span>

## <span data-ttu-id="95ac2-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="95ac2-104">SYNTAX</span></span>

### <span data-ttu-id="95ac2-105">Список1 (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="95ac2-105">List1 (Default)</span></span>
```
Get-AzWvdApplicationGroup [-SubscriptionId <String[]>] [-Filter <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="95ac2-106">Получить</span><span class="sxs-lookup"><span data-stu-id="95ac2-106">Get</span></span>
```
Get-AzWvdApplicationGroup -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="95ac2-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="95ac2-107">GetViaIdentity</span></span>
```
Get-AzWvdApplicationGroup -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="95ac2-108">Список</span><span class="sxs-lookup"><span data-stu-id="95ac2-108">List</span></span>
```
Get-AzWvdApplicationGroup -ResourceGroupName <String> [-SubscriptionId <String[]>] [-Filter <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="95ac2-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="95ac2-109">DESCRIPTION</span></span>
<span data-ttu-id="95ac2-110">Получите группу приложений.</span><span class="sxs-lookup"><span data-stu-id="95ac2-110">Get an application group.</span></span>

## <span data-ttu-id="95ac2-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="95ac2-111">EXAMPLES</span></span>

### <span data-ttu-id="95ac2-112">Пример 1. Получение группы приложений Virtual Desktop для Windows по имени</span><span class="sxs-lookup"><span data-stu-id="95ac2-112">Example 1: Get a Windows Virtual Desktop ApplicationGroup by name</span></span>
```powershell
PS C:\> Get-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName -Name ApplicationGroupName

Location   Name                 Type
--------   ----                 ----
eastus     ApplicationGroupName Microsoft.DesktopVirtualization/applicationgroups
```

<span data-ttu-id="95ac2-113">Эта команда получает группу приложений Виртуального рабочего стола Windows в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="95ac2-113">This command gets a Windows Virtual Desktop ApplicationGroup in a Resource Group.</span></span>

### <span data-ttu-id="95ac2-114">Пример 2. List Windows Virtual Desktop ApplicationGroups</span><span class="sxs-lookup"><span data-stu-id="95ac2-114">Example 2: List Windows Virtual Desktop ApplicationGroups</span></span>
```powershell
PS C:\> Get-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName

Location   Name                  Type
--------   ----                  ----
eastus     ApplicationGroupName1 Microsoft.DesktopVirtualization/applicationgroups
eastus     ApplicationGroupName2 Microsoft.DesktopVirtualization/applicationgroups
```

<span data-ttu-id="95ac2-115">Эта команда содержит список групп приложений Виртуального рабочего стола Windows в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="95ac2-115">This command lists a Windows Virtual Desktop ApplicationGroups in a Resource Group.</span></span>

## <span data-ttu-id="95ac2-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="95ac2-116">PARAMETERS</span></span>

### <span data-ttu-id="95ac2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95ac2-117">-DefaultProfile</span></span>
<span data-ttu-id="95ac2-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="95ac2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="95ac2-119">-Filter</span><span class="sxs-lookup"><span data-stu-id="95ac2-119">-Filter</span></span>
<span data-ttu-id="95ac2-120">Выражение фильтра OData.</span><span class="sxs-lookup"><span data-stu-id="95ac2-120">OData filter expression.</span></span>
<span data-ttu-id="95ac2-121">Допустимые свойства фильтрации — applicationGroupType.</span><span class="sxs-lookup"><span data-stu-id="95ac2-121">Valid properties for filtering are applicationGroupType.</span></span>

```yaml
Type: System.String
Parameter Sets: List, List1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95ac2-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="95ac2-122">-InputObject</span></span>
<span data-ttu-id="95ac2-123">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="95ac2-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="95ac2-124">-Name</span><span class="sxs-lookup"><span data-stu-id="95ac2-124">-Name</span></span>
<span data-ttu-id="95ac2-125">Имя группы приложений</span><span class="sxs-lookup"><span data-stu-id="95ac2-125">The name of the application group</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ApplicationGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95ac2-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95ac2-126">-ResourceGroupName</span></span>
<span data-ttu-id="95ac2-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="95ac2-127">The name of the resource group.</span></span>
<span data-ttu-id="95ac2-128">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="95ac2-128">The name is case insensitive.</span></span>

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

### <span data-ttu-id="95ac2-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="95ac2-129">-SubscriptionId</span></span>
<span data-ttu-id="95ac2-130">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="95ac2-130">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="95ac2-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95ac2-131">CommonParameters</span></span>
<span data-ttu-id="95ac2-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95ac2-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95ac2-133">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="95ac2-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95ac2-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="95ac2-134">INPUTS</span></span>

### <span data-ttu-id="95ac2-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="95ac2-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="95ac2-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="95ac2-136">OUTPUTS</span></span>

### <span data-ttu-id="95ac2-137">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="95ac2-137">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IApplicationGroup</span></span>

## <span data-ttu-id="95ac2-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="95ac2-138">NOTES</span></span>

<span data-ttu-id="95ac2-139">ALIASES</span><span class="sxs-lookup"><span data-stu-id="95ac2-139">ALIASES</span></span>

<span data-ttu-id="95ac2-140">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="95ac2-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="95ac2-141">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="95ac2-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="95ac2-142">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="95ac2-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="95ac2-143">INPUTOBJECT <IDesktopVirtualizationIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="95ac2-143">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="95ac2-144">`[ApplicationGroupName <String>]`: имя группы приложений</span><span class="sxs-lookup"><span data-stu-id="95ac2-144">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="95ac2-145">`[ApplicationName <String>]`: имя приложения в указанной группе приложений</span><span class="sxs-lookup"><span data-stu-id="95ac2-145">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="95ac2-146">`[DesktopName <String>]`: имя рабочего стола в указанной группе рабочего стола</span><span class="sxs-lookup"><span data-stu-id="95ac2-146">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="95ac2-147">`[HostPoolName <String>]`: имя пула хостов в указанной группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="95ac2-147">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="95ac2-148">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="95ac2-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="95ac2-149">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span><span class="sxs-lookup"><span data-stu-id="95ac2-149">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="95ac2-150">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="95ac2-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="95ac2-151">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="95ac2-151">The name is case insensitive.</span></span>
  - <span data-ttu-id="95ac2-152">`[SessionHostName <String>]`: имя сеанса в указанном пуле хостов</span><span class="sxs-lookup"><span data-stu-id="95ac2-152">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="95ac2-153">`[SubscriptionId <String>]`: ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="95ac2-153">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="95ac2-154">`[UserSessionId <String>]`: имя сеанса пользователя в указанном хосте сеанса</span><span class="sxs-lookup"><span data-stu-id="95ac2-154">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="95ac2-155">`[WorkspaceName <String>]`: имя рабочей области</span><span class="sxs-lookup"><span data-stu-id="95ac2-155">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="95ac2-156">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="95ac2-156">RELATED LINKS</span></span>

