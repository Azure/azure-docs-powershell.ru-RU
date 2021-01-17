---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/unregister-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Unregister-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Unregister-AzWvdApplicationGroup.md
ms.openlocfilehash: 0533864f3fd16e9810e837629782b767fbdc0435
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98426335"
---
# <span data-ttu-id="8ffc5-101">Unregister-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="8ffc5-101">Unregister-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="8ffc5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8ffc5-102">SYNOPSIS</span></span>
<span data-ttu-id="8ffc5-103">Отоблести регистрацию группы виртуальных классических приложений Windows.</span><span class="sxs-lookup"><span data-stu-id="8ffc5-103">Unregister the Windows virtual desktop application group.</span></span>

## <span data-ttu-id="8ffc5-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8ffc5-104">SYNTAX</span></span>

```
Unregister-AzWvdApplicationGroup -ApplicationGroupPath <String> -ResourceGroupName <String>
 -WorkspaceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="8ffc5-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8ffc5-105">DESCRIPTION</span></span>
<span data-ttu-id="8ffc5-106">Отоблести регистрацию группы виртуальных классических приложений Windows.</span><span class="sxs-lookup"><span data-stu-id="8ffc5-106">Unregister the Windows virtual desktop application group.</span></span>

## <span data-ttu-id="8ffc5-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8ffc5-107">EXAMPLES</span></span>

### <span data-ttu-id="8ffc5-108">Пример 1. Unregister a Windows Virtual Desktop Application Group</span><span class="sxs-lookup"><span data-stu-id="8ffc5-108">Example 1: Unregister a Windows Virtual Desktop Application Group</span></span>
```powershell
PS C:\> Unregister-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName `
                                    -WorkspaceName WorkspaceName `
                                    -ApplicationGroupPath '/subscriptions/SubscriptionId/resourceGroups/ResourceGroupName/providers/Microsoft.DesktopVirtualization/applicationGroups/ApplicationGroupName'

Location   Name                 Type
--------   ----                 ----
eastus     WorkspaceName Microsoft.DesktopVirtualization/workspaces
```

<span data-ttu-id="8ffc5-109">Эта команда unregisters a Windows Virtual Desktop Application Group to a Workspace.</span><span class="sxs-lookup"><span data-stu-id="8ffc5-109">This command unregisters a Windows Virtual Desktop Application Group to a Workspace.</span></span>

## <span data-ttu-id="8ffc5-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8ffc5-110">PARAMETERS</span></span>

### <span data-ttu-id="8ffc5-111">-ApplicationGroupPath</span><span class="sxs-lookup"><span data-stu-id="8ffc5-111">-ApplicationGroupPath</span></span>
<span data-ttu-id="8ffc5-112">Путь к resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ffc5-112">ResourceGroupName Path</span></span>

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

### <span data-ttu-id="8ffc5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ffc5-113">-DefaultProfile</span></span>
<span data-ttu-id="8ffc5-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8ffc5-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8ffc5-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ffc5-115">-ResourceGroupName</span></span>
<span data-ttu-id="8ffc5-116">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="8ffc5-116">Resource Group Name</span></span>

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

### <span data-ttu-id="8ffc5-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8ffc5-117">-SubscriptionId</span></span>
<span data-ttu-id="8ffc5-118">ИД подписки</span><span class="sxs-lookup"><span data-stu-id="8ffc5-118">Subscription Id</span></span>

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

### <span data-ttu-id="8ffc5-119">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="8ffc5-119">-WorkspaceName</span></span>
<span data-ttu-id="8ffc5-120">Имя рабочей области</span><span class="sxs-lookup"><span data-stu-id="8ffc5-120">Workspace Name</span></span>

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

### <span data-ttu-id="8ffc5-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8ffc5-121">-Confirm</span></span>
<span data-ttu-id="8ffc5-122">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8ffc5-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ffc5-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ffc5-123">-WhatIf</span></span>
<span data-ttu-id="8ffc5-124">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8ffc5-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8ffc5-125">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="8ffc5-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ffc5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ffc5-126">CommonParameters</span></span>
<span data-ttu-id="8ffc5-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ffc5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ffc5-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8ffc5-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ffc5-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8ffc5-129">INPUTS</span></span>

## <span data-ttu-id="8ffc5-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8ffc5-130">OUTPUTS</span></span>

### <span data-ttu-id="8ffc5-131">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IWorkspace</span><span class="sxs-lookup"><span data-stu-id="8ffc5-131">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IWorkspace</span></span>

## <span data-ttu-id="8ffc5-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8ffc5-132">NOTES</span></span>

<span data-ttu-id="8ffc5-133">ALIASES</span><span class="sxs-lookup"><span data-stu-id="8ffc5-133">ALIASES</span></span>

## <span data-ttu-id="8ffc5-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8ffc5-134">RELATED LINKS</span></span>

