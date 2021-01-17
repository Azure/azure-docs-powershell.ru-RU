---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Start-AzJitNetworkAccessPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Start-AzJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Start-AzJitNetworkAccessPolicy.md
ms.openlocfilehash: b992f3a41278ba66c54eeefc0b548eef76b50980
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98415367"
---
# <span data-ttu-id="9073c-101">Start-AzJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="9073c-101">Start-AzJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="9073c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9073c-102">SYNOPSIS</span></span>
<span data-ttu-id="9073c-103">Вызывает запрос на временный доступ к сети.</span><span class="sxs-lookup"><span data-stu-id="9073c-103">Invokes a temporary network access request.</span></span>

## <span data-ttu-id="9073c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9073c-104">SYNTAX</span></span>

### <span data-ttu-id="9073c-105">ResourceGroupLevelResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9073c-105">ResourceGroupLevelResource (Default)</span></span>
```
Start-AzJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String>
 -VirtualMachine <PSSecurityJitNetworkAccessPolicyInitiateVirtualMachine[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9073c-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="9073c-106">ResourceId</span></span>
```
Start-AzJitNetworkAccessPolicy -VirtualMachine <PSSecurityJitNetworkAccessPolicyInitiateVirtualMachine[]>
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9073c-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="9073c-107">InputObject</span></span>
```
Start-AzJitNetworkAccessPolicy -InputObject <PSSecurityJitNetworkAccessPolicyInitiateInputObject>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9073c-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9073c-108">DESCRIPTION</span></span>
<span data-ttu-id="9073c-109">Вызывает запрос на временный доступ к сети.</span><span class="sxs-lookup"><span data-stu-id="9073c-109">Invokes a temporary network access request.</span></span>
<span data-ttu-id="9073c-110">Запрос проверяется в соответствии с настроенной политикой сетевого доступа JIT и, если разрешено, открывает сетевое подключение по запросу пользователя.</span><span class="sxs-lookup"><span data-stu-id="9073c-110">The request is validated against the configured JIT network access policy and if permitted, opens up a network connection according to the user's request.</span></span>
<span data-ttu-id="9073c-111">Запрос будет внесен в политику для более позднего просмотра и будет прерван при превышении указанной длительности.</span><span class="sxs-lookup"><span data-stu-id="9073c-111">The request will be logged in the policy for later review and will be terminated when the specified duration will be exceeded.</span></span>

## <span data-ttu-id="9073c-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9073c-112">EXAMPLES</span></span>

### <span data-ttu-id="9073c-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9073c-113">Example 1</span></span>
```powershell
PS C:\> Set-AzJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default" -Kind "Basic" -VirtualMachine $vms

Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.S
                    ecurity/locations/centralus/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.
                    Compute/virtualMachines/testService}
Requests          : {}
ProvisioningState : Succeeded
```

<span data-ttu-id="9073c-114">Открывает сетевое подключение согласно указанным данным запроса на подключение.</span><span class="sxs-lookup"><span data-stu-id="9073c-114">Opens up a network connection according to the specified connection request data.</span></span>

## <span data-ttu-id="9073c-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9073c-115">PARAMETERS</span></span>

### <span data-ttu-id="9073c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9073c-116">-DefaultProfile</span></span>
<span data-ttu-id="9073c-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9073c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9073c-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9073c-118">-InputObject</span></span>
<span data-ttu-id="9073c-119">Объект ввода.</span><span class="sxs-lookup"><span data-stu-id="9073c-119">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Cmdlets.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyInitiateInputObject
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9073c-120">-Location</span><span class="sxs-lookup"><span data-stu-id="9073c-120">-Location</span></span>
<span data-ttu-id="9073c-121">"Расположение".</span><span class="sxs-lookup"><span data-stu-id="9073c-121">Location.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9073c-122">-Name</span><span class="sxs-lookup"><span data-stu-id="9073c-122">-Name</span></span>
<span data-ttu-id="9073c-123">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="9073c-123">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9073c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9073c-124">-ResourceGroupName</span></span>
<span data-ttu-id="9073c-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9073c-125">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9073c-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9073c-126">-ResourceId</span></span>
<span data-ttu-id="9073c-127">ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="9073c-127">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9073c-128">-VirtualMachine</span><span class="sxs-lookup"><span data-stu-id="9073c-128">-VirtualMachine</span></span>
<span data-ttu-id="9073c-129">Автоматическая подготовка.</span><span class="sxs-lookup"><span data-stu-id="9073c-129">Automatic Provisioning.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyInitiateVirtualMachine[]
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9073c-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9073c-130">-Confirm</span></span>
<span data-ttu-id="9073c-131">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9073c-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9073c-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9073c-132">-WhatIf</span></span>
<span data-ttu-id="9073c-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9073c-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9073c-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="9073c-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9073c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9073c-135">CommonParameters</span></span>
<span data-ttu-id="9073c-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9073c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9073c-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9073c-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9073c-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9073c-138">INPUTS</span></span>

### <span data-ttu-id="9073c-139">System.String</span><span class="sxs-lookup"><span data-stu-id="9073c-139">System.String</span></span>

### <span data-ttu-id="9073c-140">Microsoft.Azure.Commands.Security.Cmdlets.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyInitiateInputObject</span><span class="sxs-lookup"><span data-stu-id="9073c-140">Microsoft.Azure.Commands.Security.Cmdlets.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyInitiateInputObject</span></span>

## <span data-ttu-id="9073c-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9073c-141">OUTPUTS</span></span>

### <span data-ttu-id="9073c-142">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="9073c-142">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="9073c-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9073c-143">NOTES</span></span>

## <span data-ttu-id="9073c-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9073c-144">RELATED LINKS</span></span>
