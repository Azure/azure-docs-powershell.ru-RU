---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/new-azwvdworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdWorkspace.md
ms.openlocfilehash: fbd71d03c6f82bcb785105d9d75e155e9f7ef498
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94312527"
---
# <span data-ttu-id="2742d-101">New-AzWvdWorkspace</span><span class="sxs-lookup"><span data-stu-id="2742d-101">New-AzWvdWorkspace</span></span>

## <span data-ttu-id="2742d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2742d-102">SYNOPSIS</span></span>
<span data-ttu-id="2742d-103">Создание или обновление рабочей области.</span><span class="sxs-lookup"><span data-stu-id="2742d-103">Create or update a workspace.</span></span>

## <span data-ttu-id="2742d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2742d-104">SYNTAX</span></span>

```
New-AzWvdWorkspace -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-ApplicationGroupReference <String[]>] [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2742d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2742d-105">DESCRIPTION</span></span>
<span data-ttu-id="2742d-106">Создание или обновление рабочей области.</span><span class="sxs-lookup"><span data-stu-id="2742d-106">Create or update a workspace.</span></span>

## <span data-ttu-id="2742d-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2742d-107">EXAMPLES</span></span>

### <span data-ttu-id="2742d-108">Пример 1: создание виртуального рабочего стола Windows Worksapce по имени</span><span class="sxs-lookup"><span data-stu-id="2742d-108">Example 1: Create a Windows Virtual Desktop Worksapce by name</span></span>
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

<span data-ttu-id="2742d-109">Эта команда создает рабочую область виртуальных рабочих столов Windows в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2742d-109">This command creates a Windows Virtual Desktop Workspace in a Resource Group.</span></span>

### <span data-ttu-id="2742d-110">Пример 2: создание виртуального рабочего стола Windows Worksapce по имени</span><span class="sxs-lookup"><span data-stu-id="2742d-110">Example 2: Create a Windows Virtual Desktop Worksapce by name</span></span>
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

<span data-ttu-id="2742d-111">Эта команда создает рабочую область виртуальных рабочих столов Windows в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2742d-111">This command creates a Windows Virtual Desktop Workspace in a Resource Group.</span></span>

## <span data-ttu-id="2742d-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2742d-112">PARAMETERS</span></span>

### <span data-ttu-id="2742d-113">-ApplicationGroupReference</span><span class="sxs-lookup"><span data-stu-id="2742d-113">-ApplicationGroupReference</span></span>
<span data-ttu-id="2742d-114">Список идентификаторов ресурсов applicationGroup.</span><span class="sxs-lookup"><span data-stu-id="2742d-114">List of applicationGroup resource Ids.</span></span>

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

### <span data-ttu-id="2742d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2742d-115">-DefaultProfile</span></span>
<span data-ttu-id="2742d-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2742d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2742d-117">-Описание</span><span class="sxs-lookup"><span data-stu-id="2742d-117">-Description</span></span>
<span data-ttu-id="2742d-118">Описание рабочей области.</span><span class="sxs-lookup"><span data-stu-id="2742d-118">Description of Workspace.</span></span>

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

### <span data-ttu-id="2742d-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="2742d-119">-FriendlyName</span></span>
<span data-ttu-id="2742d-120">Понятное имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="2742d-120">Friendly name of Workspace.</span></span>

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

### <span data-ttu-id="2742d-121">-Location</span><span class="sxs-lookup"><span data-stu-id="2742d-121">-Location</span></span>
<span data-ttu-id="2742d-122">Географическое расположение, в котором находится ресурс</span><span class="sxs-lookup"><span data-stu-id="2742d-122">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="2742d-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2742d-123">-Name</span></span>
<span data-ttu-id="2742d-124">Имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="2742d-124">The name of the workspace</span></span>

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

### <span data-ttu-id="2742d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2742d-125">-ResourceGroupName</span></span>
<span data-ttu-id="2742d-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2742d-126">The name of the resource group.</span></span>
<span data-ttu-id="2742d-127">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="2742d-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="2742d-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2742d-128">-SubscriptionId</span></span>
<span data-ttu-id="2742d-129">Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="2742d-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="2742d-130">-Тег</span><span class="sxs-lookup"><span data-stu-id="2742d-130">-Tag</span></span>
<span data-ttu-id="2742d-131">Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2742d-131">Resource tags.</span></span>

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

### <span data-ttu-id="2742d-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2742d-132">-Confirm</span></span>
<span data-ttu-id="2742d-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2742d-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2742d-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2742d-134">-WhatIf</span></span>
<span data-ttu-id="2742d-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2742d-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2742d-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2742d-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2742d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2742d-137">CommonParameters</span></span>
<span data-ttu-id="2742d-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2742d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2742d-139">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2742d-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2742d-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2742d-140">INPUTS</span></span>

## <span data-ttu-id="2742d-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2742d-141">OUTPUTS</span></span>

### <span data-ttu-id="2742d-142">Microsoft. Azure. PowerShell. командлеты. DesktopVirtualization. Models. Api20191210Preview. IWorkspace</span><span class="sxs-lookup"><span data-stu-id="2742d-142">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IWorkspace</span></span>

## <span data-ttu-id="2742d-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="2742d-143">NOTES</span></span>

<span data-ttu-id="2742d-144">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="2742d-144">ALIASES</span></span>

## <span data-ttu-id="2742d-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2742d-145">RELATED LINKS</span></span>

