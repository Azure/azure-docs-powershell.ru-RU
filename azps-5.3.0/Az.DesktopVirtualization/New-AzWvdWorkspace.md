---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/new-azwvdworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdWorkspace.md
ms.openlocfilehash: b97db1a21afab939e94b776b3da8d43f3d1468b2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98507566"
---
# <span data-ttu-id="62258-101">New-AzWvdWorkspace</span><span class="sxs-lookup"><span data-stu-id="62258-101">New-AzWvdWorkspace</span></span>

## <span data-ttu-id="62258-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="62258-102">SYNOPSIS</span></span>
<span data-ttu-id="62258-103">Создание или обновление рабочей области.</span><span class="sxs-lookup"><span data-stu-id="62258-103">Create or update a workspace.</span></span>

## <span data-ttu-id="62258-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="62258-104">SYNTAX</span></span>

```
New-AzWvdWorkspace -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-ApplicationGroupReference <String[]>] [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="62258-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="62258-105">DESCRIPTION</span></span>
<span data-ttu-id="62258-106">Создание или обновление рабочей области.</span><span class="sxs-lookup"><span data-stu-id="62258-106">Create or update a workspace.</span></span>

## <span data-ttu-id="62258-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="62258-107">EXAMPLES</span></span>

### <span data-ttu-id="62258-108">Пример 1. Создание виртуальной рабочей области рабочего стола Windows по имени</span><span class="sxs-lookup"><span data-stu-id="62258-108">Example 1: Create a Windows Virtual Desktop Workspace by name</span></span>
```powershell
PS C:\> New-AzWvdWorkspace -ResourceGroupName ResourceGroupName `
                        -Name WorkspaceName `
                        -Location 'eastus' `
                        -FriendlyName 'Friendly Name' `
                        -ApplicationGroupReference $null `
                        -Description 'Description'

Location   Name                 Type
--------   ----                 ----
eastus     WorkspaceName Microsoft.DesktopVirtualization/workspaces
```

<span data-ttu-id="62258-109">Эта команда создает в группе ресурсов рабочее пространство виртуального рабочего стола Windows.</span><span class="sxs-lookup"><span data-stu-id="62258-109">This command creates a Windows Virtual Desktop Workspace in a Resource Group.</span></span>

### <span data-ttu-id="62258-110">Пример 2. Создание рабочей области виртуального рабочего стола Windows по имени</span><span class="sxs-lookup"><span data-stu-id="62258-110">Example 2: Create a Windows Virtual Desktop Workspace by name</span></span>
```powershell
PS C:\> New-AzWvdWorkspace -ResourceGroupName ResourceGroupName `
                        -Name WorkspaceName `
                        -Location 'eastus' `
                        -FriendlyName 'Friendly Name' `
                        -ApplicationGroupReference "/subscriptions/SubscriptionId/resourceGroups/ResourceGroupName/providers/Microsoft.DesktopVirtualization/applicationGroups/ApplicationGroupName1","/subscriptions/SubscriptionId/resourceGroups/ResourceGroupName/providers/Microsoft.DesktopVirtualization/applicationGroups/ApplicationGroupName2" `
                        -Description 'Description'

Location   Name                 Type
--------   ----                 ----
eastus     WorkspaceName Microsoft.DesktopVirtualization/workspaces
```

<span data-ttu-id="62258-111">Эта команда создает в группе ресурсов рабочее пространство виртуального рабочего стола Windows.</span><span class="sxs-lookup"><span data-stu-id="62258-111">This command creates a Windows Virtual Desktop Workspace in a Resource Group.</span></span>

## <span data-ttu-id="62258-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="62258-112">PARAMETERS</span></span>

### <span data-ttu-id="62258-113">-ApplicationGroupReference</span><span class="sxs-lookup"><span data-stu-id="62258-113">-ApplicationGroupReference</span></span>
<span data-ttu-id="62258-114">Список ИД ресурсов applicationGroup.</span><span class="sxs-lookup"><span data-stu-id="62258-114">List of applicationGroup resource Ids.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62258-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62258-115">-DefaultProfile</span></span>
<span data-ttu-id="62258-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="62258-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62258-117">-Description</span><span class="sxs-lookup"><span data-stu-id="62258-117">-Description</span></span>
<span data-ttu-id="62258-118">Описание рабочей области.</span><span class="sxs-lookup"><span data-stu-id="62258-118">Description of Workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62258-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="62258-119">-FriendlyName</span></span>
<span data-ttu-id="62258-120">Имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="62258-120">Friendly name of Workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62258-121">-Location</span><span class="sxs-lookup"><span data-stu-id="62258-121">-Location</span></span>
<span data-ttu-id="62258-122">Географическое расположение ресурса</span><span class="sxs-lookup"><span data-stu-id="62258-122">The geo-location where the resource lives</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62258-123">-Name</span><span class="sxs-lookup"><span data-stu-id="62258-123">-Name</span></span>
<span data-ttu-id="62258-124">Имя рабочей области</span><span class="sxs-lookup"><span data-stu-id="62258-124">The name of the workspace</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: WorkspaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62258-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62258-125">-ResourceGroupName</span></span>
<span data-ttu-id="62258-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="62258-126">The name of the resource group.</span></span>
<span data-ttu-id="62258-127">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="62258-127">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62258-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="62258-128">-SubscriptionId</span></span>
<span data-ttu-id="62258-129">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="62258-129">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62258-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="62258-130">-Tag</span></span>
<span data-ttu-id="62258-131">Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="62258-131">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62258-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="62258-132">-Confirm</span></span>
<span data-ttu-id="62258-133">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="62258-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62258-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62258-134">-WhatIf</span></span>
<span data-ttu-id="62258-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="62258-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62258-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="62258-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62258-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62258-137">CommonParameters</span></span>
<span data-ttu-id="62258-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62258-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62258-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="62258-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62258-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="62258-140">INPUTS</span></span>

## <span data-ttu-id="62258-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="62258-141">OUTPUTS</span></span>

### <span data-ttu-id="62258-142">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IWorkspace</span><span class="sxs-lookup"><span data-stu-id="62258-142">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IWorkspace</span></span>

## <span data-ttu-id="62258-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="62258-143">NOTES</span></span>

<span data-ttu-id="62258-144">ALIASES</span><span class="sxs-lookup"><span data-stu-id="62258-144">ALIASES</span></span>

## <span data-ttu-id="62258-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="62258-145">RELATED LINKS</span></span>

