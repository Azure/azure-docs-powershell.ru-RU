---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzJitNetworkAccessPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzJitNetworkAccessPolicy.md
ms.openlocfilehash: a316a59492034f0effd2d233ce386cbd6a256c75
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98394748"
---
# <span data-ttu-id="eaa89-101">Set-AzJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="eaa89-101">Set-AzJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="eaa89-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eaa89-102">SYNOPSIS</span></span>
<span data-ttu-id="eaa89-103">Обновляет политику доступа к сети JIT.</span><span class="sxs-lookup"><span data-stu-id="eaa89-103">Updates JIT network access policy.</span></span>

## <span data-ttu-id="eaa89-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="eaa89-104">SYNTAX</span></span>

```
Set-AzJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String>
 -VirtualMachine <PSSecurityJitNetworkAccessPolicyVirtualMachine[]> -Kind <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eaa89-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="eaa89-105">DESCRIPTION</span></span>
<span data-ttu-id="eaa89-106">Обновляет политику доступа к сети JIT.</span><span class="sxs-lookup"><span data-stu-id="eaa89-106">Updates JIT network access policy.</span></span>

## <span data-ttu-id="eaa89-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="eaa89-107">EXAMPLES</span></span>

### <span data-ttu-id="eaa89-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="eaa89-108">Example 1</span></span>
```powershell
PS C:\> Set-AzJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default" -VirtualMachine $vmRules -Kind "Basic"

Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/testService}
Requests          : {}
ProvisioningState : Succeeded
```

<span data-ttu-id="eaa89-109">Обновляет политику доступа К СЕТИ JIT с помощью новых правил VM.</span><span class="sxs-lookup"><span data-stu-id="eaa89-109">Updates a JIT network access policy with new VM rules.</span></span>

## <span data-ttu-id="eaa89-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eaa89-110">PARAMETERS</span></span>

### <span data-ttu-id="eaa89-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eaa89-111">-DefaultProfile</span></span>
<span data-ttu-id="eaa89-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="eaa89-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eaa89-113">-Kind</span><span class="sxs-lookup"><span data-stu-id="eaa89-113">-Kind</span></span>
<span data-ttu-id="eaa89-114">"Тип".</span><span class="sxs-lookup"><span data-stu-id="eaa89-114">Kind.</span></span>

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

### <span data-ttu-id="eaa89-115">-Location</span><span class="sxs-lookup"><span data-stu-id="eaa89-115">-Location</span></span>
<span data-ttu-id="eaa89-116">"Расположение".</span><span class="sxs-lookup"><span data-stu-id="eaa89-116">Location.</span></span>

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

### <span data-ttu-id="eaa89-117">-Name</span><span class="sxs-lookup"><span data-stu-id="eaa89-117">-Name</span></span>
<span data-ttu-id="eaa89-118">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="eaa89-118">Resource name.</span></span>

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

### <span data-ttu-id="eaa89-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eaa89-119">-ResourceGroupName</span></span>
<span data-ttu-id="eaa89-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="eaa89-120">Resource group name.</span></span>

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

### <span data-ttu-id="eaa89-121">-VirtualMachine</span><span class="sxs-lookup"><span data-stu-id="eaa89-121">-VirtualMachine</span></span>
<span data-ttu-id="eaa89-122">Виртуальные машины.</span><span class="sxs-lookup"><span data-stu-id="eaa89-122">Virtual Machines.</span></span>

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

### <span data-ttu-id="eaa89-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="eaa89-123">-Confirm</span></span>
<span data-ttu-id="eaa89-124">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="eaa89-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eaa89-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eaa89-125">-WhatIf</span></span>
<span data-ttu-id="eaa89-126">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eaa89-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="eaa89-127">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="eaa89-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eaa89-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eaa89-128">CommonParameters</span></span>
<span data-ttu-id="eaa89-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eaa89-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eaa89-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="eaa89-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eaa89-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="eaa89-131">INPUTS</span></span>

### <span data-ttu-id="eaa89-132">Нет</span><span class="sxs-lookup"><span data-stu-id="eaa89-132">None</span></span>

## <span data-ttu-id="eaa89-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="eaa89-133">OUTPUTS</span></span>

### <span data-ttu-id="eaa89-134">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="eaa89-134">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="eaa89-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="eaa89-135">NOTES</span></span>

## <span data-ttu-id="eaa89-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="eaa89-136">RELATED LINKS</span></span>
