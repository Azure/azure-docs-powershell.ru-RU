---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/powershell/module/az.vmware/new-azvmwareauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/New-AzVMwareAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/New-AzVMwareAuthorization.md
ms.openlocfilehash: 7c532f6aca8c959367d4e67725f36b44e4978840
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991819"
---
# <span data-ttu-id="e73ca-101">New-AzVMWareAuthorization</span><span class="sxs-lookup"><span data-stu-id="e73ca-101">New-AzVMWareAuthorization</span></span>

## <span data-ttu-id="e73ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e73ca-102">SYNOPSIS</span></span>
<span data-ttu-id="e73ca-103">Создание или обновление авторизации каналов ExpressRoute в частном облаке</span><span class="sxs-lookup"><span data-stu-id="e73ca-103">Create or update an ExpressRoute Circuit Authorization in a private cloud</span></span>

## <span data-ttu-id="e73ca-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e73ca-104">SYNTAX</span></span>

```
New-AzVMWareAuthorization -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="e73ca-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e73ca-105">DESCRIPTION</span></span>
<span data-ttu-id="e73ca-106">Создание или обновление авторизации каналов ExpressRoute в частном облаке</span><span class="sxs-lookup"><span data-stu-id="e73ca-106">Create or update an ExpressRoute Circuit Authorization in a private cloud</span></span>

## <span data-ttu-id="e73ca-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e73ca-107">EXAMPLES</span></span>

### <span data-ttu-id="e73ca-108">Пример 1. Создание автозаверх</span><span class="sxs-lookup"><span data-stu-id="e73ca-108">Example 1: Create autorization</span></span>
```powershell
PS C:\> New-AzVMWareAuthorization -Name azps-test-auth -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group



Name           Type
----           ----
azps-test-auth Microsoft.AVS/privateClouds/authorizations
```

<span data-ttu-id="e73ca-109">Этот cmdlet создает авторизацию в `azps-test-auth` закрытом облаке `azps-test-cloud`</span><span class="sxs-lookup"><span data-stu-id="e73ca-109">This cmdlet creates authorization `azps-test-auth` under private cloud `azps-test-cloud`</span></span>

## <span data-ttu-id="e73ca-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e73ca-110">PARAMETERS</span></span>

### <span data-ttu-id="e73ca-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e73ca-111">-AsJob</span></span>
<span data-ttu-id="e73ca-112">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="e73ca-112">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e73ca-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e73ca-113">-DefaultProfile</span></span>
<span data-ttu-id="e73ca-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e73ca-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e73ca-115">-Name</span><span class="sxs-lookup"><span data-stu-id="e73ca-115">-Name</span></span>
<span data-ttu-id="e73ca-116">Имя авторизации каналов ExpressRoute в частном облаке</span><span class="sxs-lookup"><span data-stu-id="e73ca-116">Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e73ca-117">-NoWait</span><span class="sxs-lookup"><span data-stu-id="e73ca-117">-NoWait</span></span>
<span data-ttu-id="e73ca-118">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="e73ca-118">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e73ca-119">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="e73ca-119">-PrivateCloudName</span></span>
<span data-ttu-id="e73ca-120">Имя закрытого облака.</span><span class="sxs-lookup"><span data-stu-id="e73ca-120">The name of the private cloud.</span></span>

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

### <span data-ttu-id="e73ca-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e73ca-121">-ResourceGroupName</span></span>
<span data-ttu-id="e73ca-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e73ca-122">The name of the resource group.</span></span>
<span data-ttu-id="e73ca-123">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="e73ca-123">The name is case insensitive.</span></span>

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

### <span data-ttu-id="e73ca-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e73ca-124">-SubscriptionId</span></span>
<span data-ttu-id="e73ca-125">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="e73ca-125">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="e73ca-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e73ca-126">-Confirm</span></span>
<span data-ttu-id="e73ca-127">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="e73ca-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e73ca-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e73ca-128">-WhatIf</span></span>
<span data-ttu-id="e73ca-129">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e73ca-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e73ca-130">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="e73ca-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e73ca-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e73ca-131">CommonParameters</span></span>
<span data-ttu-id="e73ca-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e73ca-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e73ca-133">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e73ca-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e73ca-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e73ca-134">INPUTS</span></span>

## <span data-ttu-id="e73ca-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e73ca-135">OUTPUTS</span></span>

### <span data-ttu-id="e73ca-136">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IExpressRouteAuthorization</span><span class="sxs-lookup"><span data-stu-id="e73ca-136">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IExpressRouteAuthorization</span></span>

## <span data-ttu-id="e73ca-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e73ca-137">NOTES</span></span>

<span data-ttu-id="e73ca-138">ALIASES</span><span class="sxs-lookup"><span data-stu-id="e73ca-138">ALIASES</span></span>

## <span data-ttu-id="e73ca-139">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e73ca-139">RELATED LINKS</span></span>

