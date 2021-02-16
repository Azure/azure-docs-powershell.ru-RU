---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/register-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Register-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Register-AzWvdApplicationGroup.md
ms.openlocfilehash: 874cc587bff418bf0d6846fe39bdf7d10c42d7dd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100238046"
---
# <span data-ttu-id="125bb-101">Register-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="125bb-101">Register-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="125bb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="125bb-102">SYNOPSIS</span></span>
<span data-ttu-id="125bb-103">Зарегистрируйте группу виртуальных классических приложений Windows.</span><span class="sxs-lookup"><span data-stu-id="125bb-103">Register a Windows virtual desktop application group.</span></span>

## <span data-ttu-id="125bb-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="125bb-104">SYNTAX</span></span>

```
Register-AzWvdApplicationGroup -ApplicationGroupPath <String> -ResourceGroupName <String>
 -WorkspaceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="125bb-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="125bb-105">DESCRIPTION</span></span>
<span data-ttu-id="125bb-106">Зарегистрируйте группу виртуальных классических приложений Windows.</span><span class="sxs-lookup"><span data-stu-id="125bb-106">Register a Windows virtual desktop application group.</span></span>

## <span data-ttu-id="125bb-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="125bb-107">EXAMPLES</span></span>

### <span data-ttu-id="125bb-108">Пример 1. Регистрация группы виртуальных классических приложений Windows</span><span class="sxs-lookup"><span data-stu-id="125bb-108">Example 1: Register a Windows Virtual Desktop Application Group</span></span>
```powershell
PS C:\> Register-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName `
                                    -WorkspaceName WorkspaceName `
                                    -ApplicationGroupPath '/subscriptions/SubscriptionId/resourceGroups/ResourceGroupName/providers/Microsoft.DesktopVirtualization/applicationGroups/ApplicationGroupName'

Location   Name                 Type
--------   ----                 ----
eastus     WorkspaceName Microsoft.DesktopVirtualization/workspaces
```

<span data-ttu-id="125bb-109">Эта команда регистрирует группу приложений виртуального рабочего стола Windows в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="125bb-109">This command registers a Windows Virtual Desktop Application Group to a Workspace.</span></span>

## <span data-ttu-id="125bb-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="125bb-110">PARAMETERS</span></span>

### <span data-ttu-id="125bb-111">-ApplicationGroupPath</span><span class="sxs-lookup"><span data-stu-id="125bb-111">-ApplicationGroupPath</span></span>
<span data-ttu-id="125bb-112">ApplicationGroupPath Path</span><span class="sxs-lookup"><span data-stu-id="125bb-112">ApplicationGroupPath Path</span></span>

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

### <span data-ttu-id="125bb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="125bb-113">-DefaultProfile</span></span>
<span data-ttu-id="125bb-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="125bb-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="125bb-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="125bb-115">-ResourceGroupName</span></span>
<span data-ttu-id="125bb-116">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="125bb-116">Resource Group Name</span></span>

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

### <span data-ttu-id="125bb-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="125bb-117">-SubscriptionId</span></span>
<span data-ttu-id="125bb-118">ИД подписки</span><span class="sxs-lookup"><span data-stu-id="125bb-118">Subscription Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="125bb-119">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="125bb-119">-WorkspaceName</span></span>
<span data-ttu-id="125bb-120">Имя рабочей области</span><span class="sxs-lookup"><span data-stu-id="125bb-120">Workspace Name</span></span>

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

### <span data-ttu-id="125bb-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="125bb-121">-Confirm</span></span>
<span data-ttu-id="125bb-122">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="125bb-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="125bb-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="125bb-123">-WhatIf</span></span>
<span data-ttu-id="125bb-124">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="125bb-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="125bb-125">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="125bb-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="125bb-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="125bb-126">CommonParameters</span></span>
<span data-ttu-id="125bb-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="125bb-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="125bb-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="125bb-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="125bb-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="125bb-129">INPUTS</span></span>

## <span data-ttu-id="125bb-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="125bb-130">OUTPUTS</span></span>

### <span data-ttu-id="125bb-131">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IWorkspace</span><span class="sxs-lookup"><span data-stu-id="125bb-131">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IWorkspace</span></span>

## <span data-ttu-id="125bb-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="125bb-132">NOTES</span></span>

<span data-ttu-id="125bb-133">ALIASES</span><span class="sxs-lookup"><span data-stu-id="125bb-133">ALIASES</span></span>

## <span data-ttu-id="125bb-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="125bb-134">RELATED LINKS</span></span>

