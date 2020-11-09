---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/unregister-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Unregister-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Unregister-AzWvdApplicationGroup.md
ms.openlocfilehash: 0533864f3fd16e9810e837629782b767fbdc0435
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94312458"
---
# <span data-ttu-id="4b453-101">Unregister-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="4b453-101">Unregister-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="4b453-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4b453-102">SYNOPSIS</span></span>
<span data-ttu-id="4b453-103">Отмените регистрацию группы приложений виртуальных рабочих столов Windows.</span><span class="sxs-lookup"><span data-stu-id="4b453-103">Unregister the Windows virtual desktop application group.</span></span>

## <span data-ttu-id="4b453-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4b453-104">SYNTAX</span></span>

```
Unregister-AzWvdApplicationGroup -ApplicationGroupPath <String> -ResourceGroupName <String>
 -WorkspaceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="4b453-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4b453-105">DESCRIPTION</span></span>
<span data-ttu-id="4b453-106">Отмените регистрацию группы приложений виртуальных рабочих столов Windows.</span><span class="sxs-lookup"><span data-stu-id="4b453-106">Unregister the Windows virtual desktop application group.</span></span>

## <span data-ttu-id="4b453-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4b453-107">EXAMPLES</span></span>

### <span data-ttu-id="4b453-108">Пример 1: Отмена регистрации группы приложений виртуальных рабочих столов Windows</span><span class="sxs-lookup"><span data-stu-id="4b453-108">Example 1: Unregister a Windows Virtual Desktop Application Group</span></span>
```powershell
PS C:\> Unregister-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName `
                                    -WorkspaceName WorkspaceName `
                                    -ApplicationGroupPath '/subscriptions/SubscriptionId/resourceGroups/ResourceGroupName/providers/Microsoft.DesktopVirtualization/applicationGroups/ApplicationGroupName'

Location   Name                 Type
--------   ----                 ----
eastus     WorkspaceName Microsoft.DesktopVirtualization/workspaces
```

<span data-ttu-id="4b453-109">Эта команда отменяет регистрацию группы приложений виртуальных рабочих столов Windows в рабочую область.</span><span class="sxs-lookup"><span data-stu-id="4b453-109">This command unregisters a Windows Virtual Desktop Application Group to a Workspace.</span></span>

## <span data-ttu-id="4b453-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4b453-110">PARAMETERS</span></span>

### <span data-ttu-id="4b453-111">-ApplicationGroupPath</span><span class="sxs-lookup"><span data-stu-id="4b453-111">-ApplicationGroupPath</span></span>
<span data-ttu-id="4b453-112">ResourceGroupName путь</span><span class="sxs-lookup"><span data-stu-id="4b453-112">ResourceGroupName Path</span></span>

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

### <span data-ttu-id="4b453-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b453-113">-DefaultProfile</span></span>
<span data-ttu-id="4b453-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4b453-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4b453-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b453-115">-ResourceGroupName</span></span>
<span data-ttu-id="4b453-116">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="4b453-116">Resource Group Name</span></span>

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

### <span data-ttu-id="4b453-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4b453-117">-SubscriptionId</span></span>
<span data-ttu-id="4b453-118">Идентификатор подписки</span><span class="sxs-lookup"><span data-stu-id="4b453-118">Subscription Id</span></span>

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

### <span data-ttu-id="4b453-119">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="4b453-119">-WorkspaceName</span></span>
<span data-ttu-id="4b453-120">Имя рабочей области</span><span class="sxs-lookup"><span data-stu-id="4b453-120">Workspace Name</span></span>

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

### <span data-ttu-id="4b453-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4b453-121">-Confirm</span></span>
<span data-ttu-id="4b453-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4b453-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b453-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b453-123">-WhatIf</span></span>
<span data-ttu-id="4b453-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4b453-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b453-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4b453-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b453-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b453-126">CommonParameters</span></span>
<span data-ttu-id="4b453-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4b453-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b453-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4b453-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b453-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4b453-129">INPUTS</span></span>

## <span data-ttu-id="4b453-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4b453-130">OUTPUTS</span></span>

### <span data-ttu-id="4b453-131">Microsoft. Azure. PowerShell. командлеты. DesktopVirtualization. Models. Api20191210Preview. IWorkspace</span><span class="sxs-lookup"><span data-stu-id="4b453-131">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IWorkspace</span></span>

## <span data-ttu-id="4b453-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="4b453-132">NOTES</span></span>

<span data-ttu-id="4b453-133">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="4b453-133">ALIASES</span></span>

## <span data-ttu-id="4b453-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4b453-134">RELATED LINKS</span></span>

