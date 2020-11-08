---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzJitNetworkAccessPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzJitNetworkAccessPolicy.md
ms.openlocfilehash: a40fba16bd7d361544ca10867d2c575965447c12
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066052"
---
# <span data-ttu-id="b587d-101">Set-AzJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b587d-101">Set-AzJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="b587d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b587d-102">SYNOPSIS</span></span>
<span data-ttu-id="b587d-103">Обновляет политику JIT-доступа к сети.</span><span class="sxs-lookup"><span data-stu-id="b587d-103">Updates JIT network access policy.</span></span>

## <span data-ttu-id="b587d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b587d-104">SYNTAX</span></span>

```
Set-AzJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String>
 -VirtualMachine <PSSecurityJitNetworkAccessPolicyVirtualMachine[]> -Kind <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b587d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b587d-105">DESCRIPTION</span></span>
<span data-ttu-id="b587d-106">Обновляет политику JIT-доступа к сети.</span><span class="sxs-lookup"><span data-stu-id="b587d-106">Updates JIT network access policy.</span></span>

## <span data-ttu-id="b587d-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b587d-107">EXAMPLES</span></span>

### <span data-ttu-id="b587d-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b587d-108">Example 1</span></span>
```powershell
PS C:\> Set-AzJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default" -VirtualMachine $vmRules -Kind "Basic"

Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/testService}
Requests          : {}
ProvisioningState : Succeeded
```

<span data-ttu-id="b587d-109">Обновляет политику JIT-доступа к сети с помощью новых правил виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="b587d-109">Updates a JIT network access policy with new VM rules.</span></span>

## <span data-ttu-id="b587d-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b587d-110">PARAMETERS</span></span>

### <span data-ttu-id="b587d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b587d-111">-DefaultProfile</span></span>
<span data-ttu-id="b587d-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b587d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b587d-113">-Видах</span><span class="sxs-lookup"><span data-stu-id="b587d-113">-Kind</span></span>
<span data-ttu-id="b587d-114">Любые.</span><span class="sxs-lookup"><span data-stu-id="b587d-114">Kind.</span></span>

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

### <span data-ttu-id="b587d-115">-Location</span><span class="sxs-lookup"><span data-stu-id="b587d-115">-Location</span></span>
<span data-ttu-id="b587d-116">Поиска.</span><span class="sxs-lookup"><span data-stu-id="b587d-116">Location.</span></span>

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

### <span data-ttu-id="b587d-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b587d-117">-Name</span></span>
<span data-ttu-id="b587d-118">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="b587d-118">Resource name.</span></span>

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

### <span data-ttu-id="b587d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b587d-119">-ResourceGroupName</span></span>
<span data-ttu-id="b587d-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b587d-120">Resource group name.</span></span>

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

### <span data-ttu-id="b587d-121">-VirtualMachine</span><span class="sxs-lookup"><span data-stu-id="b587d-121">-VirtualMachine</span></span>
<span data-ttu-id="b587d-122">Виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="b587d-122">Virtual Machines.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyVirtualMachine[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b587d-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b587d-123">-Confirm</span></span>
<span data-ttu-id="b587d-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b587d-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b587d-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b587d-125">-WhatIf</span></span>
<span data-ttu-id="b587d-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b587d-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b587d-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b587d-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b587d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b587d-128">CommonParameters</span></span>
<span data-ttu-id="b587d-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b587d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b587d-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b587d-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b587d-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b587d-131">INPUTS</span></span>

### <span data-ttu-id="b587d-132">Ничего</span><span class="sxs-lookup"><span data-stu-id="b587d-132">None</span></span>

## <span data-ttu-id="b587d-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b587d-133">OUTPUTS</span></span>

### <span data-ttu-id="b587d-134">Microsoft. Azure. Commands. Security. Models. JitNetworkAccessPolicies. PSSecurityJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b587d-134">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="b587d-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="b587d-135">NOTES</span></span>

## <span data-ttu-id="b587d-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b587d-136">RELATED LINKS</span></span>
