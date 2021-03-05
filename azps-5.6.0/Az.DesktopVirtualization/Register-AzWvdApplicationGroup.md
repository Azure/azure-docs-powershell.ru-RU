---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/register-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Register-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Register-AzWvdApplicationGroup.md
ms.openlocfilehash: ef1829dec7bdc1c3b41fa9e418246e1d9afcc1f8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101966056"
---
# <span data-ttu-id="d1792-101">Register-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="d1792-101">Register-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="d1792-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d1792-102">SYNOPSIS</span></span>
<span data-ttu-id="d1792-103">Зарегистрируйте группу виртуальных классических приложений Windows.</span><span class="sxs-lookup"><span data-stu-id="d1792-103">Register a Windows virtual desktop application group.</span></span>

## <span data-ttu-id="d1792-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d1792-104">SYNTAX</span></span>

```
Register-AzWvdApplicationGroup -ApplicationGroupPath <String> -ResourceGroupName <String>
 -WorkspaceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="d1792-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d1792-105">DESCRIPTION</span></span>
<span data-ttu-id="d1792-106">Зарегистрируйте группу виртуальных классических приложений Windows.</span><span class="sxs-lookup"><span data-stu-id="d1792-106">Register a Windows virtual desktop application group.</span></span>

## <span data-ttu-id="d1792-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d1792-107">EXAMPLES</span></span>

### <span data-ttu-id="d1792-108">Пример 1. Регистрация группы виртуальных классических приложений Windows</span><span class="sxs-lookup"><span data-stu-id="d1792-108">Example 1: Register a Windows Virtual Desktop Application Group</span></span>
```powershell
PS C:\> Register-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName `
                                    -WorkspaceName WorkspaceName `
                                    -ApplicationGroupPath '/subscriptions/SubscriptionId/resourceGroups/ResourceGroupName/providers/Microsoft.DesktopVirtualization/applicationGroups/ApplicationGroupName'

Location   Name                 Type
--------   ----                 ----
eastus     WorkspaceName Microsoft.DesktopVirtualization/workspaces
```

<span data-ttu-id="d1792-109">Эта команда регистрирует группу виртуальных классических приложений Windows в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="d1792-109">This command registers a Windows Virtual Desktop Application Group to a Workspace.</span></span>

## <span data-ttu-id="d1792-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d1792-110">PARAMETERS</span></span>

### <span data-ttu-id="d1792-111">-ApplicationGroupPath</span><span class="sxs-lookup"><span data-stu-id="d1792-111">-ApplicationGroupPath</span></span>
<span data-ttu-id="d1792-112">ApplicationGroupPath Path</span><span class="sxs-lookup"><span data-stu-id="d1792-112">ApplicationGroupPath Path</span></span>

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

### <span data-ttu-id="d1792-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1792-113">-DefaultProfile</span></span>
<span data-ttu-id="d1792-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d1792-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1792-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1792-115">-ResourceGroupName</span></span>
<span data-ttu-id="d1792-116">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="d1792-116">Resource Group Name</span></span>

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

### <span data-ttu-id="d1792-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d1792-117">-SubscriptionId</span></span>
<span data-ttu-id="d1792-118">ИД подписки</span><span class="sxs-lookup"><span data-stu-id="d1792-118">Subscription Id</span></span>

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

### <span data-ttu-id="d1792-119">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d1792-119">-WorkspaceName</span></span>
<span data-ttu-id="d1792-120">Имя рабочей области</span><span class="sxs-lookup"><span data-stu-id="d1792-120">Workspace Name</span></span>

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

### <span data-ttu-id="d1792-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d1792-121">-Confirm</span></span>
<span data-ttu-id="d1792-122">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d1792-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1792-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1792-123">-WhatIf</span></span>
<span data-ttu-id="d1792-124">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d1792-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1792-125">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="d1792-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1792-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1792-126">CommonParameters</span></span>
<span data-ttu-id="d1792-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1792-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1792-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d1792-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1792-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d1792-129">INPUTS</span></span>

## <span data-ttu-id="d1792-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d1792-130">OUTPUTS</span></span>

### <span data-ttu-id="d1792-131">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IWorkspace</span><span class="sxs-lookup"><span data-stu-id="d1792-131">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IWorkspace</span></span>

## <span data-ttu-id="d1792-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d1792-132">NOTES</span></span>

<span data-ttu-id="d1792-133">ALIASES</span><span class="sxs-lookup"><span data-stu-id="d1792-133">ALIASES</span></span>

## <span data-ttu-id="d1792-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d1792-134">RELATED LINKS</span></span>

