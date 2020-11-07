---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Start-AzJitNetworkAccessPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Start-AzJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Start-AzJitNetworkAccessPolicy.md
ms.openlocfilehash: 188d653f58644a359f20886e96791efa53ab7b2a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93903885"
---
# <span data-ttu-id="d2d2a-101">Start-AzJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d2d2a-101">Start-AzJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="d2d2a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d2d2a-102">SYNOPSIS</span></span>
<span data-ttu-id="d2d2a-103">Вызывает временный запрос на доступ к сети.</span><span class="sxs-lookup"><span data-stu-id="d2d2a-103">Invokes a temporary network access request.</span></span>

## <span data-ttu-id="d2d2a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d2d2a-104">SYNTAX</span></span>

### <span data-ttu-id="d2d2a-105">ResourceGroupLevelResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d2d2a-105">ResourceGroupLevelResource (Default)</span></span>
```
Start-AzJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String>
 -VirtualMachine <PSSecurityJitNetworkAccessPolicyInitiateVirtualMachine[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2d2a-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="d2d2a-106">ResourceId</span></span>
```
Start-AzJitNetworkAccessPolicy -VirtualMachine <PSSecurityJitNetworkAccessPolicyInitiateVirtualMachine[]>
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2d2a-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="d2d2a-107">InputObject</span></span>
```
Start-AzJitNetworkAccessPolicy -InputObject <PSSecurityJitNetworkAccessPolicyInitiateInputObject>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2d2a-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d2d2a-108">DESCRIPTION</span></span>
<span data-ttu-id="d2d2a-109">Вызывает временный запрос на доступ к сети.</span><span class="sxs-lookup"><span data-stu-id="d2d2a-109">Invokes a temporary network access request.</span></span>
<span data-ttu-id="d2d2a-110">Запрос проверяются на соответствие настроенной политике доступа к сети JIT и, если разрешено, открывает сетевое подключение в соответствии с запросом пользователя.</span><span class="sxs-lookup"><span data-stu-id="d2d2a-110">The request is validated against the configured JIT network access policy and if permitted, opens up a network connection according to the user's request.</span></span>
<span data-ttu-id="d2d2a-111">Запрос будет зарегистрирован в политике для более поздней проверки и будет прекращен, когда будет превышена Указанная длительность.</span><span class="sxs-lookup"><span data-stu-id="d2d2a-111">The request will be logged in the policy for later review and will be terminated when the specified duration will be exceeded.</span></span>

## <span data-ttu-id="d2d2a-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d2d2a-112">EXAMPLES</span></span>

### <span data-ttu-id="d2d2a-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d2d2a-113">Example 1</span></span>
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

<span data-ttu-id="d2d2a-114">Открывает сетевое подключение в соответствии с указанными данными запроса на подключение.</span><span class="sxs-lookup"><span data-stu-id="d2d2a-114">Opens up a network connection according to the specified connection request data.</span></span>

## <span data-ttu-id="d2d2a-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d2d2a-115">PARAMETERS</span></span>

### <span data-ttu-id="d2d2a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2d2a-116">-DefaultProfile</span></span>
<span data-ttu-id="d2d2a-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d2d2a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2d2a-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d2d2a-118">-InputObject</span></span>
<span data-ttu-id="d2d2a-119">Объект input.</span><span class="sxs-lookup"><span data-stu-id="d2d2a-119">Input Object.</span></span>

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

### <span data-ttu-id="d2d2a-120">-Location</span><span class="sxs-lookup"><span data-stu-id="d2d2a-120">-Location</span></span>
<span data-ttu-id="d2d2a-121">Поиска.</span><span class="sxs-lookup"><span data-stu-id="d2d2a-121">Location.</span></span>

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

### <span data-ttu-id="d2d2a-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d2d2a-122">-Name</span></span>
<span data-ttu-id="d2d2a-123">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="d2d2a-123">Resource name.</span></span>

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

### <span data-ttu-id="d2d2a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2d2a-124">-ResourceGroupName</span></span>
<span data-ttu-id="d2d2a-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d2d2a-125">Resource group name.</span></span>

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

### <span data-ttu-id="d2d2a-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d2d2a-126">-ResourceId</span></span>
<span data-ttu-id="d2d2a-127">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="d2d2a-127">Resource ID.</span></span>

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

### <span data-ttu-id="d2d2a-128">-VirtualMachine</span><span class="sxs-lookup"><span data-stu-id="d2d2a-128">-VirtualMachine</span></span>
<span data-ttu-id="d2d2a-129">Автоматическая подготовка.</span><span class="sxs-lookup"><span data-stu-id="d2d2a-129">Automatic Provisioning.</span></span>

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

### <span data-ttu-id="d2d2a-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d2d2a-130">-Confirm</span></span>
<span data-ttu-id="d2d2a-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d2d2a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2d2a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2d2a-132">-WhatIf</span></span>
<span data-ttu-id="d2d2a-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d2d2a-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d2d2a-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d2d2a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2d2a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2d2a-135">CommonParameters</span></span>
<span data-ttu-id="d2d2a-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d2d2a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2d2a-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2d2a-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2d2a-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d2d2a-138">INPUTS</span></span>

### <span data-ttu-id="d2d2a-139">System. String</span><span class="sxs-lookup"><span data-stu-id="d2d2a-139">System.String</span></span>

### <span data-ttu-id="d2d2a-140">Microsoft. Azure. Commands. Security. командлеты. JitNetworkAccessPolicies. PSSecurityJitNetworkAccessPolicyInitiateInputObject</span><span class="sxs-lookup"><span data-stu-id="d2d2a-140">Microsoft.Azure.Commands.Security.Cmdlets.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyInitiateInputObject</span></span>

## <span data-ttu-id="d2d2a-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d2d2a-141">OUTPUTS</span></span>

### <span data-ttu-id="d2d2a-142">Microsoft. Azure. Commands. Security. Models. JitNetworkAccessPolicies. PSSecurityJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d2d2a-142">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="d2d2a-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="d2d2a-143">NOTES</span></span>

## <span data-ttu-id="d2d2a-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d2d2a-144">RELATED LINKS</span></span>
