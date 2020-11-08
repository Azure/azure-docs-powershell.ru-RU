---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/new-azvmwareauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/New-AzVMWareAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/New-AzVMWareAuthorization.md
ms.openlocfilehash: b1e8ca1e5140470524ec83656ef0042bafa494b7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243443"
---
# <span data-ttu-id="38260-101">New-AzVMWareAuthorization</span><span class="sxs-lookup"><span data-stu-id="38260-101">New-AzVMWareAuthorization</span></span>

## <span data-ttu-id="38260-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="38260-102">SYNOPSIS</span></span>
<span data-ttu-id="38260-103">Создание и обновление авторизации канала ExpressRoute в частном облаке</span><span class="sxs-lookup"><span data-stu-id="38260-103">Create or update an ExpressRoute Circuit Authorization in a private cloud</span></span>

## <span data-ttu-id="38260-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="38260-104">SYNTAX</span></span>

```
New-AzVMWareAuthorization -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="38260-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="38260-105">DESCRIPTION</span></span>
<span data-ttu-id="38260-106">Создание и обновление авторизации канала ExpressRoute в частном облаке</span><span class="sxs-lookup"><span data-stu-id="38260-106">Create or update an ExpressRoute Circuit Authorization in a private cloud</span></span>

## <span data-ttu-id="38260-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="38260-107">EXAMPLES</span></span>

### <span data-ttu-id="38260-108">Пример 1: создание autorization</span><span class="sxs-lookup"><span data-stu-id="38260-108">Example 1: Create autorization</span></span>
```powershell
PS C:\> New-AzVMWareAuthorization -Name azps-test-auth -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group



Name           Type
----           ----
azps-test-auth Microsoft.AVS/privateClouds/authorizations
```

<span data-ttu-id="38260-109">Этот командлет создает авторизацию `azps-test-auth` в частном облаке `azps-test-cloud`</span><span class="sxs-lookup"><span data-stu-id="38260-109">This cmdlet creates authorization `azps-test-auth` under private cloud `azps-test-cloud`</span></span>

## <span data-ttu-id="38260-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="38260-110">PARAMETERS</span></span>

### <span data-ttu-id="38260-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="38260-111">-AsJob</span></span>
<span data-ttu-id="38260-112">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="38260-112">Run the command as a job</span></span>

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

### <span data-ttu-id="38260-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38260-113">-DefaultProfile</span></span>
<span data-ttu-id="38260-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="38260-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38260-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="38260-115">-Name</span></span>
<span data-ttu-id="38260-116">Имя авторизации канала ExpressRoute в частном облаке</span><span class="sxs-lookup"><span data-stu-id="38260-116">Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>

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

### <span data-ttu-id="38260-117">-Wait</span><span class="sxs-lookup"><span data-stu-id="38260-117">-NoWait</span></span>
<span data-ttu-id="38260-118">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="38260-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="38260-119">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="38260-119">-PrivateCloudName</span></span>
<span data-ttu-id="38260-120">Имя частного облака.</span><span class="sxs-lookup"><span data-stu-id="38260-120">The name of the private cloud.</span></span>

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

### <span data-ttu-id="38260-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38260-121">-ResourceGroupName</span></span>
<span data-ttu-id="38260-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="38260-122">The name of the resource group.</span></span>
<span data-ttu-id="38260-123">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="38260-123">The name is case insensitive.</span></span>

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

### <span data-ttu-id="38260-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="38260-124">-SubscriptionId</span></span>
<span data-ttu-id="38260-125">Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="38260-125">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="38260-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="38260-126">-Confirm</span></span>
<span data-ttu-id="38260-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="38260-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38260-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38260-128">-WhatIf</span></span>
<span data-ttu-id="38260-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="38260-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38260-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="38260-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38260-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38260-131">CommonParameters</span></span>
<span data-ttu-id="38260-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="38260-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38260-133">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="38260-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38260-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="38260-134">INPUTS</span></span>

## <span data-ttu-id="38260-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="38260-135">OUTPUTS</span></span>

### <span data-ttu-id="38260-136">Microsoft. Azure. PowerShell. командлеты. VMWare. Models. Api20200320. IExpressRouteAuthorization</span><span class="sxs-lookup"><span data-stu-id="38260-136">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IExpressRouteAuthorization</span></span>

## <span data-ttu-id="38260-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="38260-137">NOTES</span></span>

<span data-ttu-id="38260-138">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="38260-138">ALIASES</span></span>

## <span data-ttu-id="38260-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="38260-139">RELATED LINKS</span></span>

