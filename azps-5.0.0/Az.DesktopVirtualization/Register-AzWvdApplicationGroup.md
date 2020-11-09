---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/register-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Register-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Register-AzWvdApplicationGroup.md
ms.openlocfilehash: 874cc587bff418bf0d6846fe39bdf7d10c42d7dd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94312512"
---
# <span data-ttu-id="0c547-101">Register-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="0c547-101">Register-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="0c547-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0c547-102">SYNOPSIS</span></span>
<span data-ttu-id="0c547-103">Зарегистрируйте группу приложений виртуальных рабочих столов Windows.</span><span class="sxs-lookup"><span data-stu-id="0c547-103">Register a Windows virtual desktop application group.</span></span>

## <span data-ttu-id="0c547-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0c547-104">SYNTAX</span></span>

```
Register-AzWvdApplicationGroup -ApplicationGroupPath <String> -ResourceGroupName <String>
 -WorkspaceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="0c547-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0c547-105">DESCRIPTION</span></span>
<span data-ttu-id="0c547-106">Зарегистрируйте группу приложений виртуальных рабочих столов Windows.</span><span class="sxs-lookup"><span data-stu-id="0c547-106">Register a Windows virtual desktop application group.</span></span>

## <span data-ttu-id="0c547-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0c547-107">EXAMPLES</span></span>

### <span data-ttu-id="0c547-108">Пример 1: регистрация группы приложений виртуальных рабочих столов Windows</span><span class="sxs-lookup"><span data-stu-id="0c547-108">Example 1: Register a Windows Virtual Desktop Application Group</span></span>
```powershell
PS C:\> Register-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName `
                                    -WorkspaceName WorkspaceName `
                                    -ApplicationGroupPath '/subscriptions/SubscriptionId/resourceGroups/ResourceGroupName/providers/Microsoft.DesktopVirtualization/applicationGroups/ApplicationGroupName'

Location   Name                 Type
--------   ----                 ----
eastus     WorkspaceName Microsoft.DesktopVirtualization/workspaces
```

<span data-ttu-id="0c547-109">Эта команда регистрирует группу приложений виртуальных рабочих столов Windows в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="0c547-109">This command registers a Windows Virtual Desktop Application Group to a Workspace.</span></span>

## <span data-ttu-id="0c547-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0c547-110">PARAMETERS</span></span>

### <span data-ttu-id="0c547-111">-ApplicationGroupPath</span><span class="sxs-lookup"><span data-stu-id="0c547-111">-ApplicationGroupPath</span></span>
<span data-ttu-id="0c547-112">ApplicationGroupPath путь</span><span class="sxs-lookup"><span data-stu-id="0c547-112">ApplicationGroupPath Path</span></span>

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

### <span data-ttu-id="0c547-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c547-113">-DefaultProfile</span></span>
<span data-ttu-id="0c547-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0c547-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c547-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c547-115">-ResourceGroupName</span></span>
<span data-ttu-id="0c547-116">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="0c547-116">Resource Group Name</span></span>

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

### <span data-ttu-id="0c547-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0c547-117">-SubscriptionId</span></span>
<span data-ttu-id="0c547-118">Идентификатор подписки</span><span class="sxs-lookup"><span data-stu-id="0c547-118">Subscription Id</span></span>

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

### <span data-ttu-id="0c547-119">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="0c547-119">-WorkspaceName</span></span>
<span data-ttu-id="0c547-120">Имя рабочей области</span><span class="sxs-lookup"><span data-stu-id="0c547-120">Workspace Name</span></span>

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

### <span data-ttu-id="0c547-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0c547-121">-Confirm</span></span>
<span data-ttu-id="0c547-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0c547-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c547-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c547-123">-WhatIf</span></span>
<span data-ttu-id="0c547-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0c547-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c547-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0c547-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c547-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c547-126">CommonParameters</span></span>
<span data-ttu-id="0c547-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0c547-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c547-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0c547-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c547-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0c547-129">INPUTS</span></span>

## <span data-ttu-id="0c547-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0c547-130">OUTPUTS</span></span>

### <span data-ttu-id="0c547-131">Microsoft. Azure. PowerShell. командлеты. DesktopVirtualization. Models. Api20191210Preview. IWorkspace</span><span class="sxs-lookup"><span data-stu-id="0c547-131">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IWorkspace</span></span>

## <span data-ttu-id="0c547-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="0c547-132">NOTES</span></span>

<span data-ttu-id="0c547-133">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="0c547-133">ALIASES</span></span>

## <span data-ttu-id="0c547-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0c547-134">RELATED LINKS</span></span>

