---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Start-AzJitNetworkAccessPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Start-AzJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Start-AzJitNetworkAccessPolicy.md
ms.openlocfilehash: 674f88a30ea036fc496cd6931b3d856a20a25c0a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986485"
---
# <span data-ttu-id="64dff-101">Start-AzJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="64dff-101">Start-AzJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="64dff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="64dff-102">SYNOPSIS</span></span>
<span data-ttu-id="64dff-103">Вызывает запрос на временный сетевой доступ.</span><span class="sxs-lookup"><span data-stu-id="64dff-103">Invokes a temporary network access request.</span></span>

## <span data-ttu-id="64dff-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="64dff-104">SYNTAX</span></span>

### <span data-ttu-id="64dff-105">ResourceGroupLevelResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="64dff-105">ResourceGroupLevelResource (Default)</span></span>
```
Start-AzJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String>
 -VirtualMachine <PSSecurityJitNetworkAccessPolicyInitiateVirtualMachine[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64dff-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="64dff-106">ResourceId</span></span>
```
Start-AzJitNetworkAccessPolicy -VirtualMachine <PSSecurityJitNetworkAccessPolicyInitiateVirtualMachine[]>
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64dff-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="64dff-107">InputObject</span></span>
```
Start-AzJitNetworkAccessPolicy -InputObject <PSSecurityJitNetworkAccessPolicyInitiateInputObject>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64dff-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="64dff-108">DESCRIPTION</span></span>
<span data-ttu-id="64dff-109">Вызывает запрос на временный доступ к сети.</span><span class="sxs-lookup"><span data-stu-id="64dff-109">Invokes a temporary network access request.</span></span>
<span data-ttu-id="64dff-110">Запрос проверяется в соответствии с настроенной политикой сетевого доступа JIT и, если разрешено, открывает сетевое подключение по запросу пользователя.</span><span class="sxs-lookup"><span data-stu-id="64dff-110">The request is validated against the configured JIT network access policy and if permitted, opens up a network connection according to the user's request.</span></span>
<span data-ttu-id="64dff-111">Запрос будет внесен в политику для более позднего просмотра и будет прерван при превышении указанной длительности.</span><span class="sxs-lookup"><span data-stu-id="64dff-111">The request will be logged in the policy for later review and will be terminated when the specified duration will be exceeded.</span></span>

## <span data-ttu-id="64dff-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="64dff-112">EXAMPLES</span></span>

### <span data-ttu-id="64dff-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="64dff-113">Example 1</span></span>
```powershell
$MyResource = Get-AzResource -Id /subscriptions/xxxxxxx-xxxxx-xxxxx-xxxxxxx/resourceGroups/PolicyDemo/providers/Microsoft.Compute/virtualMachines/PolicyDemoVM1
$JitPolicy = (@{
        id    = $MyResource.ResourceId; 
        ports = (@{
                number                     = 22
                endTimeUtc                 = Get-Date (Get-Date -AsUTC).AddHours(1) -Format O
                allowedSourceAddressPrefix = @($MyPublicIP) 
            })
    })
$ActivationVM = @($JitPolicy)
Start-AzJitNetworkAccessPolicy -ResourceGroupName $($MyResource.ResourceGroupName) -Location $MyResource.Location -Name "default" -VirtualMachine $ActivationVM

```

<span data-ttu-id="64dff-114">Открытие сетевого подключения на 1 час с моим общедоступным IP-адресом на 22 часа (не отображается).</span><span class="sxs-lookup"><span data-stu-id="64dff-114">Opens up a network connection for 1 hour over port 22 from my public IP (not shown).</span></span>

## <span data-ttu-id="64dff-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="64dff-115">PARAMETERS</span></span>

### <span data-ttu-id="64dff-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64dff-116">-DefaultProfile</span></span>
<span data-ttu-id="64dff-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="64dff-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="64dff-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="64dff-118">-InputObject</span></span>
<span data-ttu-id="64dff-119">Объект ввода.</span><span class="sxs-lookup"><span data-stu-id="64dff-119">Input Object.</span></span>

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

### <span data-ttu-id="64dff-120">-Location</span><span class="sxs-lookup"><span data-stu-id="64dff-120">-Location</span></span>
<span data-ttu-id="64dff-121">"Расположение".</span><span class="sxs-lookup"><span data-stu-id="64dff-121">Location.</span></span>

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

### <span data-ttu-id="64dff-122">-Name</span><span class="sxs-lookup"><span data-stu-id="64dff-122">-Name</span></span>
<span data-ttu-id="64dff-123">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="64dff-123">Resource name.</span></span>

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

### <span data-ttu-id="64dff-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64dff-124">-ResourceGroupName</span></span>
<span data-ttu-id="64dff-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="64dff-125">Resource group name.</span></span>

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

### <span data-ttu-id="64dff-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="64dff-126">-ResourceId</span></span>
<span data-ttu-id="64dff-127">ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="64dff-127">Resource ID.</span></span>

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

### <span data-ttu-id="64dff-128">-VirtualMachine</span><span class="sxs-lookup"><span data-stu-id="64dff-128">-VirtualMachine</span></span>
<span data-ttu-id="64dff-129">Автоматическая подготовка.</span><span class="sxs-lookup"><span data-stu-id="64dff-129">Automatic Provisioning.</span></span>

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

### <span data-ttu-id="64dff-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="64dff-130">-Confirm</span></span>
<span data-ttu-id="64dff-131">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="64dff-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64dff-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64dff-132">-WhatIf</span></span>
<span data-ttu-id="64dff-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="64dff-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="64dff-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="64dff-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64dff-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64dff-135">CommonParameters</span></span>
<span data-ttu-id="64dff-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64dff-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64dff-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="64dff-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64dff-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="64dff-138">INPUTS</span></span>

### <span data-ttu-id="64dff-139">System.String</span><span class="sxs-lookup"><span data-stu-id="64dff-139">System.String</span></span>

### <span data-ttu-id="64dff-140">Microsoft.Azure.Commands.Security.Cmdlets.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyInitiateInputObject</span><span class="sxs-lookup"><span data-stu-id="64dff-140">Microsoft.Azure.Commands.Security.Cmdlets.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyInitiateInputObject</span></span>

## <span data-ttu-id="64dff-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="64dff-141">OUTPUTS</span></span>

### <span data-ttu-id="64dff-142">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="64dff-142">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="64dff-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="64dff-143">NOTES</span></span>

## <span data-ttu-id="64dff-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="64dff-144">RELATED LINKS</span></span>
