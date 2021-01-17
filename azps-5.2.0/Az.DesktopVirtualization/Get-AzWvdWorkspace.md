---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdWorkspace.md
ms.openlocfilehash: b17fedefcac1acd260f9b3f0cf8834605a590ca9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98416180"
---
# <span data-ttu-id="67311-101">Get-AzWvdWorkspace</span><span class="sxs-lookup"><span data-stu-id="67311-101">Get-AzWvdWorkspace</span></span>

## <span data-ttu-id="67311-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67311-102">SYNOPSIS</span></span>
<span data-ttu-id="67311-103">Получите рабочее пространство.</span><span class="sxs-lookup"><span data-stu-id="67311-103">Get a workspace.</span></span>

## <span data-ttu-id="67311-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="67311-104">SYNTAX</span></span>

### <span data-ttu-id="67311-105">Список1 (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="67311-105">List1 (Default)</span></span>
```
Get-AzWvdWorkspace [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="67311-106">Получить</span><span class="sxs-lookup"><span data-stu-id="67311-106">Get</span></span>
```
Get-AzWvdWorkspace -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="67311-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="67311-107">GetViaIdentity</span></span>
```
Get-AzWvdWorkspace -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="67311-108">Список</span><span class="sxs-lookup"><span data-stu-id="67311-108">List</span></span>
```
Get-AzWvdWorkspace -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="67311-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="67311-109">DESCRIPTION</span></span>
<span data-ttu-id="67311-110">Получите рабочее пространство.</span><span class="sxs-lookup"><span data-stu-id="67311-110">Get a workspace.</span></span>

## <span data-ttu-id="67311-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="67311-111">EXAMPLES</span></span>

### <span data-ttu-id="67311-112">Пример 1. Получить рабочее пространство виртуального рабочего стола Windows по имени</span><span class="sxs-lookup"><span data-stu-id="67311-112">Example 1: Get a Windows Virtual Desktop Workspace by name</span></span>
```powershell
PS C:\> Get-AzWvdWorkspace -ResourceGroupName ResourceGroupName -Name WorkspaceName

Location   Name                 Type
--------   ----                 ----
eastus     WorkspaceName Microsoft.DesktopVirtualization/workspaces
```

<span data-ttu-id="67311-113">Эта команда получает в группе ресурсов рабочее пространство Виртуального рабочего стола Windows.</span><span class="sxs-lookup"><span data-stu-id="67311-113">This command gets a Windows Virtual Desktop Workspace in a Resource Group.</span></span>

### <span data-ttu-id="67311-114">Пример 2. Список рабочих области виртуального рабочего стола Windows</span><span class="sxs-lookup"><span data-stu-id="67311-114">Example 2: List Windows Virtual Desktop Workspaces</span></span>
```powershell
PS C:\> Get-AzWvdWorkspace -ResourceGroupName ResourceGroupName

Location   Name           Type
--------   ----           ----
eastus     WorkspaceName1 Microsoft.DesktopVirtualization/workspaces
eastus     WorkspaceName2 Microsoft.DesktopVirtualization/workspaces
```

<span data-ttu-id="67311-115">Эта команда содержит список рабочих пространство виртуального рабочего стола Windows в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="67311-115">This command lists a Windows Virtual Desktop Workspaces in a Resource Group.</span></span>

## <span data-ttu-id="67311-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="67311-116">PARAMETERS</span></span>

### <span data-ttu-id="67311-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67311-117">-DefaultProfile</span></span>
<span data-ttu-id="67311-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="67311-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67311-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="67311-119">-InputObject</span></span>
<span data-ttu-id="67311-120">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="67311-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="67311-121">-Name</span><span class="sxs-lookup"><span data-stu-id="67311-121">-Name</span></span>
<span data-ttu-id="67311-122">Имя рабочей области</span><span class="sxs-lookup"><span data-stu-id="67311-122">The name of the workspace</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: WorkspaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67311-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67311-123">-ResourceGroupName</span></span>
<span data-ttu-id="67311-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="67311-124">The name of the resource group.</span></span>
<span data-ttu-id="67311-125">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="67311-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="67311-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="67311-126">-SubscriptionId</span></span>
<span data-ttu-id="67311-127">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="67311-127">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="67311-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67311-128">CommonParameters</span></span>
<span data-ttu-id="67311-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67311-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67311-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="67311-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67311-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="67311-131">INPUTS</span></span>

### <span data-ttu-id="67311-132">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="67311-132">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="67311-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="67311-133">OUTPUTS</span></span>

### <span data-ttu-id="67311-134">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IWorkspace</span><span class="sxs-lookup"><span data-stu-id="67311-134">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IWorkspace</span></span>

## <span data-ttu-id="67311-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="67311-135">NOTES</span></span>

<span data-ttu-id="67311-136">ALIASES</span><span class="sxs-lookup"><span data-stu-id="67311-136">ALIASES</span></span>

<span data-ttu-id="67311-137">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="67311-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="67311-138">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="67311-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="67311-139">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="67311-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="67311-140">INPUTOBJECT <IDesktopVirtualizationIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="67311-140">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="67311-141">`[ApplicationGroupName <String>]`: имя группы приложений</span><span class="sxs-lookup"><span data-stu-id="67311-141">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="67311-142">`[ApplicationName <String>]`: имя приложения в указанной группе приложений</span><span class="sxs-lookup"><span data-stu-id="67311-142">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="67311-143">`[DesktopName <String>]`: имя рабочего стола в указанной группе рабочего стола</span><span class="sxs-lookup"><span data-stu-id="67311-143">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="67311-144">`[HostPoolName <String>]`: имя пула хостов в указанной группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="67311-144">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="67311-145">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="67311-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="67311-146">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span><span class="sxs-lookup"><span data-stu-id="67311-146">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="67311-147">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="67311-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="67311-148">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="67311-148">The name is case insensitive.</span></span>
  - <span data-ttu-id="67311-149">`[SessionHostName <String>]`: имя сеанса в указанном пуле хостов</span><span class="sxs-lookup"><span data-stu-id="67311-149">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="67311-150">`[SubscriptionId <String>]`: ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="67311-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="67311-151">`[UserSessionId <String>]`: имя сеанса пользователя в указанном хосте сеанса</span><span class="sxs-lookup"><span data-stu-id="67311-151">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="67311-152">`[WorkspaceName <String>]`: имя рабочей области</span><span class="sxs-lookup"><span data-stu-id="67311-152">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="67311-153">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="67311-153">RELATED LINKS</span></span>

