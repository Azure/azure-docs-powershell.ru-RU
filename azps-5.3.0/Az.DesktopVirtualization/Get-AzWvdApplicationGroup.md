---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdApplicationGroup.md
ms.openlocfilehash: 5f2ccffd0b0ba82b215db018ee15f4e495704f15
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98516874"
---
# <span data-ttu-id="f0806-101">Get-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="f0806-101">Get-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="f0806-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f0806-102">SYNOPSIS</span></span>
<span data-ttu-id="f0806-103">Получите группу приложений.</span><span class="sxs-lookup"><span data-stu-id="f0806-103">Get an application group.</span></span>

## <span data-ttu-id="f0806-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f0806-104">SYNTAX</span></span>

### <span data-ttu-id="f0806-105">Список1 (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f0806-105">List1 (Default)</span></span>
```
Get-AzWvdApplicationGroup [-SubscriptionId <String[]>] [-Filter <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="f0806-106">Получить</span><span class="sxs-lookup"><span data-stu-id="f0806-106">Get</span></span>
```
Get-AzWvdApplicationGroup -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f0806-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f0806-107">GetViaIdentity</span></span>
```
Get-AzWvdApplicationGroup -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="f0806-108">Список</span><span class="sxs-lookup"><span data-stu-id="f0806-108">List</span></span>
```
Get-AzWvdApplicationGroup -ResourceGroupName <String> [-SubscriptionId <String[]>] [-Filter <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="f0806-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f0806-109">DESCRIPTION</span></span>
<span data-ttu-id="f0806-110">Получите группу приложений.</span><span class="sxs-lookup"><span data-stu-id="f0806-110">Get an application group.</span></span>

## <span data-ttu-id="f0806-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f0806-111">EXAMPLES</span></span>

### <span data-ttu-id="f0806-112">Пример 1. Получение группы приложений Virtual Desktop для Windows по имени</span><span class="sxs-lookup"><span data-stu-id="f0806-112">Example 1: Get a Windows Virtual Desktop ApplicationGroup by name</span></span>
```powershell
PS C:\> Get-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName -Name ApplicationGroupName

Location   Name                 Type
--------   ----                 ----
eastus     ApplicationGroupName Microsoft.DesktopVirtualization/applicationgroups
```

<span data-ttu-id="f0806-113">Эта команда получает группу приложений Виртуального рабочего стола Windows в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f0806-113">This command gets a Windows Virtual Desktop ApplicationGroup in a Resource Group.</span></span>

### <span data-ttu-id="f0806-114">Пример 2. Список групп приложений виртуального рабочего стола Windows</span><span class="sxs-lookup"><span data-stu-id="f0806-114">Example 2: List Windows Virtual Desktop ApplicationGroups</span></span>
```powershell
PS C:\> Get-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName

Location   Name                  Type
--------   ----                  ----
eastus     ApplicationGroupName1 Microsoft.DesktopVirtualization/applicationgroups
eastus     ApplicationGroupName2 Microsoft.DesktopVirtualization/applicationgroups
```

<span data-ttu-id="f0806-115">Эта команда содержит список групп приложений Виртуального рабочего стола Windows в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f0806-115">This command lists a Windows Virtual Desktop ApplicationGroups in a Resource Group.</span></span>

## <span data-ttu-id="f0806-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f0806-116">PARAMETERS</span></span>

### <span data-ttu-id="f0806-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0806-117">-DefaultProfile</span></span>
<span data-ttu-id="f0806-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f0806-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f0806-119">-Filter</span><span class="sxs-lookup"><span data-stu-id="f0806-119">-Filter</span></span>
<span data-ttu-id="f0806-120">Выражение фильтра OData.</span><span class="sxs-lookup"><span data-stu-id="f0806-120">OData filter expression.</span></span>
<span data-ttu-id="f0806-121">Допустимые свойства фильтрации — applicationGroupType.</span><span class="sxs-lookup"><span data-stu-id="f0806-121">Valid properties for filtering are applicationGroupType.</span></span>

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

### <span data-ttu-id="f0806-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f0806-122">-InputObject</span></span>
<span data-ttu-id="f0806-123">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="f0806-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f0806-124">-Name</span><span class="sxs-lookup"><span data-stu-id="f0806-124">-Name</span></span>
<span data-ttu-id="f0806-125">Имя группы приложений</span><span class="sxs-lookup"><span data-stu-id="f0806-125">The name of the application group</span></span>

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

### <span data-ttu-id="f0806-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0806-126">-ResourceGroupName</span></span>
<span data-ttu-id="f0806-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f0806-127">The name of the resource group.</span></span>
<span data-ttu-id="f0806-128">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="f0806-128">The name is case insensitive.</span></span>

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

### <span data-ttu-id="f0806-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f0806-129">-SubscriptionId</span></span>
<span data-ttu-id="f0806-130">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="f0806-130">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="f0806-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0806-131">CommonParameters</span></span>
<span data-ttu-id="f0806-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0806-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0806-133">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f0806-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0806-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f0806-134">INPUTS</span></span>

### <span data-ttu-id="f0806-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="f0806-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="f0806-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f0806-136">OUTPUTS</span></span>

### <span data-ttu-id="f0806-137">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="f0806-137">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IApplicationGroup</span></span>

## <span data-ttu-id="f0806-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f0806-138">NOTES</span></span>

<span data-ttu-id="f0806-139">ALIASES</span><span class="sxs-lookup"><span data-stu-id="f0806-139">ALIASES</span></span>

<span data-ttu-id="f0806-140">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="f0806-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f0806-141">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="f0806-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f0806-142">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f0806-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f0806-143">INPUTOBJECT <IDesktopVirtualizationIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="f0806-143">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f0806-144">`[ApplicationGroupName <String>]`: имя группы приложений</span><span class="sxs-lookup"><span data-stu-id="f0806-144">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="f0806-145">`[ApplicationName <String>]`: имя приложения в указанной группе приложений</span><span class="sxs-lookup"><span data-stu-id="f0806-145">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="f0806-146">`[DesktopName <String>]`: имя рабочего стола в указанной группе рабочего стола</span><span class="sxs-lookup"><span data-stu-id="f0806-146">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="f0806-147">`[HostPoolName <String>]`: имя пула хостов в указанной группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="f0806-147">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="f0806-148">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="f0806-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f0806-149">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span><span class="sxs-lookup"><span data-stu-id="f0806-149">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="f0806-150">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f0806-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="f0806-151">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="f0806-151">The name is case insensitive.</span></span>
  - <span data-ttu-id="f0806-152">`[SessionHostName <String>]`: имя сеанса в указанном пуле хостов</span><span class="sxs-lookup"><span data-stu-id="f0806-152">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="f0806-153">`[SubscriptionId <String>]`: ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="f0806-153">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="f0806-154">`[UserSessionId <String>]`: имя сеанса пользователя в указанном хосте сеанса</span><span class="sxs-lookup"><span data-stu-id="f0806-154">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="f0806-155">`[WorkspaceName <String>]`: имя рабочей области</span><span class="sxs-lookup"><span data-stu-id="f0806-155">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="f0806-156">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f0806-156">RELATED LINKS</span></span>

