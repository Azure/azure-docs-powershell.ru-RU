---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzJitNetworkAccessPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzJitNetworkAccessPolicy.md
ms.openlocfilehash: 83aca2353102b85fd138422f249464b59a8666ca
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98517653"
---
# <span data-ttu-id="96137-101">Set-AzJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="96137-101">Set-AzJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="96137-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="96137-102">SYNOPSIS</span></span>
<span data-ttu-id="96137-103">Обновляет политику доступа к сети JIT.</span><span class="sxs-lookup"><span data-stu-id="96137-103">Updates JIT network access policy.</span></span>

## <span data-ttu-id="96137-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="96137-104">SYNTAX</span></span>

```
Set-AzJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String>
 -VirtualMachine <PSSecurityJitNetworkAccessPolicyVirtualMachine[]> -Kind <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="96137-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="96137-105">DESCRIPTION</span></span>
<span data-ttu-id="96137-106">Обновляет политику доступа к сети JIT.</span><span class="sxs-lookup"><span data-stu-id="96137-106">Updates JIT network access policy.</span></span>

## <span data-ttu-id="96137-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="96137-107">EXAMPLES</span></span>

### <span data-ttu-id="96137-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="96137-108">Example 1</span></span>
```powershell
PS C:\> Set-AzJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default" -VirtualMachine $vmRules -Kind "Basic"

Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/testService}
Requests          : {}
ProvisioningState : Succeeded
```

<span data-ttu-id="96137-109">Обновляет политику доступа К СЕТИ JIT с помощью новых правил VM.</span><span class="sxs-lookup"><span data-stu-id="96137-109">Updates a JIT network access policy with new VM rules.</span></span>

## <span data-ttu-id="96137-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="96137-110">PARAMETERS</span></span>

### <span data-ttu-id="96137-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96137-111">-DefaultProfile</span></span>
<span data-ttu-id="96137-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="96137-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="96137-113">-Kind</span><span class="sxs-lookup"><span data-stu-id="96137-113">-Kind</span></span>
<span data-ttu-id="96137-114">политика доступа к сети Jit.</span><span class="sxs-lookup"><span data-stu-id="96137-114">Jit Network Access Policy Kind.</span></span>

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

### <span data-ttu-id="96137-115">-Location</span><span class="sxs-lookup"><span data-stu-id="96137-115">-Location</span></span>
<span data-ttu-id="96137-116">"Расположение".</span><span class="sxs-lookup"><span data-stu-id="96137-116">Location.</span></span>

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

### <span data-ttu-id="96137-117">-Name</span><span class="sxs-lookup"><span data-stu-id="96137-117">-Name</span></span>
<span data-ttu-id="96137-118">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="96137-118">Resource name.</span></span>

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

### <span data-ttu-id="96137-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96137-119">-ResourceGroupName</span></span>
<span data-ttu-id="96137-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="96137-120">Resource group name.</span></span>

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

### <span data-ttu-id="96137-121">-VirtualMachine</span><span class="sxs-lookup"><span data-stu-id="96137-121">-VirtualMachine</span></span>
<span data-ttu-id="96137-122">Виртуальные машины.</span><span class="sxs-lookup"><span data-stu-id="96137-122">Virtual Machines.</span></span>

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

### <span data-ttu-id="96137-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="96137-123">-Confirm</span></span>
<span data-ttu-id="96137-124">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="96137-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96137-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96137-125">-WhatIf</span></span>
<span data-ttu-id="96137-126">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="96137-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="96137-127">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="96137-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96137-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96137-128">CommonParameters</span></span>
<span data-ttu-id="96137-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96137-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96137-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="96137-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96137-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="96137-131">INPUTS</span></span>

### <span data-ttu-id="96137-132">Нет</span><span class="sxs-lookup"><span data-stu-id="96137-132">None</span></span>

## <span data-ttu-id="96137-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="96137-133">OUTPUTS</span></span>

### <span data-ttu-id="96137-134">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="96137-134">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="96137-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="96137-135">NOTES</span></span>

## <span data-ttu-id="96137-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="96137-136">RELATED LINKS</span></span>
