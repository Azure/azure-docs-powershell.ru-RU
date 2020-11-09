---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdWorkspace.md
ms.openlocfilehash: 4596900f336c10fe6c91bd62b7a14bde50efeef8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94312554"
---
# <span data-ttu-id="9ff47-101">Get-AzWvdWorkspace</span><span class="sxs-lookup"><span data-stu-id="9ff47-101">Get-AzWvdWorkspace</span></span>

## <span data-ttu-id="9ff47-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9ff47-102">SYNOPSIS</span></span>
<span data-ttu-id="9ff47-103">Получить рабочую область.</span><span class="sxs-lookup"><span data-stu-id="9ff47-103">Get a workspace.</span></span>

## <span data-ttu-id="9ff47-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9ff47-104">SYNTAX</span></span>

### <span data-ttu-id="9ff47-105">List1 (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9ff47-105">List1 (Default)</span></span>
```
Get-AzWvdWorkspace [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="9ff47-106">Получить</span><span class="sxs-lookup"><span data-stu-id="9ff47-106">Get</span></span>
```
Get-AzWvdWorkspace -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="9ff47-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="9ff47-107">GetViaIdentity</span></span>
```
Get-AzWvdWorkspace -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="9ff47-108">Список</span><span class="sxs-lookup"><span data-stu-id="9ff47-108">List</span></span>
```
Get-AzWvdWorkspace -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="9ff47-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9ff47-109">DESCRIPTION</span></span>
<span data-ttu-id="9ff47-110">Получить рабочую область.</span><span class="sxs-lookup"><span data-stu-id="9ff47-110">Get a workspace.</span></span>

## <span data-ttu-id="9ff47-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9ff47-111">EXAMPLES</span></span>

### <span data-ttu-id="9ff47-112">Пример 1: получение виртуального рабочего стола Windows Worksapce по имени</span><span class="sxs-lookup"><span data-stu-id="9ff47-112">Example 1: Get a Windows Virtual Desktop Worksapce by name</span></span>
```powershell
PS C:\> Get-AzWvdWorksapce -ResourceGroupName ResourceGroupName -Name WorkspaceName

Location   Name                 Type
--------   ----                 ----
eastus     WorkspaceName Microsoft.DesktopVirtualization/workspaces
```

<span data-ttu-id="9ff47-113">Эта команда получает рабочую область виртуальных рабочих столов Windows в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9ff47-113">This command gets a Windows Virtual Desktop Workspace in a Resource Group.</span></span>

### <span data-ttu-id="9ff47-114">Пример 2: список рабочих областей виртуальных рабочих столов Windows</span><span class="sxs-lookup"><span data-stu-id="9ff47-114">Example 2: List Windows Virtual Desktop Workspaces</span></span>
```powershell
PS C:\> Get-AzWvdWorksapce -ResourceGroupName ResourceGroupName

Location   Name           Type
--------   ----           ----
eastus     WorkspaceName1 Microsoft.DesktopVirtualization/workspaces
eastus     WorkspaceName2 Microsoft.DesktopVirtualization/workspaces
```

<span data-ttu-id="9ff47-115">Эта команда перечисляет рабочие области виртуальных рабочих столов Windows в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9ff47-115">This command lists a Windows Virtual Desktop Workspaces in a Resource Group.</span></span>

## <span data-ttu-id="9ff47-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9ff47-116">PARAMETERS</span></span>

### <span data-ttu-id="9ff47-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ff47-117">-DefaultProfile</span></span>
<span data-ttu-id="9ff47-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9ff47-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ff47-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9ff47-119">-InputObject</span></span>
<span data-ttu-id="9ff47-120">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="9ff47-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="9ff47-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9ff47-121">-Name</span></span>
<span data-ttu-id="9ff47-122">Имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="9ff47-122">The name of the workspace</span></span>

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

### <span data-ttu-id="9ff47-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ff47-123">-ResourceGroupName</span></span>
<span data-ttu-id="9ff47-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9ff47-124">The name of the resource group.</span></span>
<span data-ttu-id="9ff47-125">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="9ff47-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="9ff47-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9ff47-126">-SubscriptionId</span></span>
<span data-ttu-id="9ff47-127">Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="9ff47-127">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="9ff47-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ff47-128">CommonParameters</span></span>
<span data-ttu-id="9ff47-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9ff47-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ff47-130">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9ff47-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ff47-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9ff47-131">INPUTS</span></span>

### <span data-ttu-id="9ff47-132">Microsoft. Azure. PowerShell. командлеты. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="9ff47-132">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="9ff47-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9ff47-133">OUTPUTS</span></span>

### <span data-ttu-id="9ff47-134">Microsoft. Azure. PowerShell. командлеты. DesktopVirtualization. Models. Api20191210Preview. IWorkspace</span><span class="sxs-lookup"><span data-stu-id="9ff47-134">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IWorkspace</span></span>

## <span data-ttu-id="9ff47-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="9ff47-135">NOTES</span></span>

<span data-ttu-id="9ff47-136">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="9ff47-136">ALIASES</span></span>

<span data-ttu-id="9ff47-137">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="9ff47-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9ff47-138">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="9ff47-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9ff47-139">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="9ff47-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9ff47-140">INPUTOBJECT <IDesktopVirtualizationIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="9ff47-140">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9ff47-141">`[ApplicationGroupName <String>]`: Имя группы приложения.</span><span class="sxs-lookup"><span data-stu-id="9ff47-141">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="9ff47-142">`[ApplicationName <String>]`: Имя приложения в указанной группе приложения.</span><span class="sxs-lookup"><span data-stu-id="9ff47-142">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="9ff47-143">`[DesktopName <String>]`: Имя рабочего стола в пределах указанной группы рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="9ff47-143">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="9ff47-144">`[HostPoolName <String>]`: Имя пула узлов в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9ff47-144">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="9ff47-145">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="9ff47-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9ff47-146">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9ff47-146">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="9ff47-147">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="9ff47-147">The name is case insensitive.</span></span>
  - <span data-ttu-id="9ff47-148">`[SessionHostName <String>]`: Имя узла сеанса в указанном пуле узлов.</span><span class="sxs-lookup"><span data-stu-id="9ff47-148">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="9ff47-149">`[SubscriptionId <String>]`: Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="9ff47-149">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="9ff47-150">`[UserSessionId <String>]`: Имя сеанса пользователя на указанном узле сеансов</span><span class="sxs-lookup"><span data-stu-id="9ff47-150">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="9ff47-151">`[WorkspaceName <String>]`: Имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="9ff47-151">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="9ff47-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9ff47-152">RELATED LINKS</span></span>

