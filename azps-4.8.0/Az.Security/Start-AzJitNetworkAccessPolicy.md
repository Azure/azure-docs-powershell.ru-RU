---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Start-AzJitNetworkAccessPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Start-AzJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Start-AzJitNetworkAccessPolicy.md
ms.openlocfilehash: b992f3a41278ba66c54eeefc0b548eef76b50980
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235341"
---
# <span data-ttu-id="cb16e-101">Start-AzJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="cb16e-101">Start-AzJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="cb16e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cb16e-102">SYNOPSIS</span></span>
<span data-ttu-id="cb16e-103">Вызывает временный запрос на доступ к сети.</span><span class="sxs-lookup"><span data-stu-id="cb16e-103">Invokes a temporary network access request.</span></span>

## <span data-ttu-id="cb16e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cb16e-104">SYNTAX</span></span>

### <span data-ttu-id="cb16e-105">ResourceGroupLevelResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cb16e-105">ResourceGroupLevelResource (Default)</span></span>
```
Start-AzJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String>
 -VirtualMachine <PSSecurityJitNetworkAccessPolicyInitiateVirtualMachine[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb16e-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="cb16e-106">ResourceId</span></span>
```
Start-AzJitNetworkAccessPolicy -VirtualMachine <PSSecurityJitNetworkAccessPolicyInitiateVirtualMachine[]>
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb16e-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="cb16e-107">InputObject</span></span>
```
Start-AzJitNetworkAccessPolicy -InputObject <PSSecurityJitNetworkAccessPolicyInitiateInputObject>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb16e-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cb16e-108">DESCRIPTION</span></span>
<span data-ttu-id="cb16e-109">Вызывает временный запрос на доступ к сети.</span><span class="sxs-lookup"><span data-stu-id="cb16e-109">Invokes a temporary network access request.</span></span>
<span data-ttu-id="cb16e-110">Запрос проверяются на соответствие настроенной политике доступа к сети JIT и, если разрешено, открывает сетевое подключение в соответствии с запросом пользователя.</span><span class="sxs-lookup"><span data-stu-id="cb16e-110">The request is validated against the configured JIT network access policy and if permitted, opens up a network connection according to the user's request.</span></span>
<span data-ttu-id="cb16e-111">Запрос будет зарегистрирован в политике для более поздней проверки и будет прекращен, когда будет превышена Указанная длительность.</span><span class="sxs-lookup"><span data-stu-id="cb16e-111">The request will be logged in the policy for later review and will be terminated when the specified duration will be exceeded.</span></span>

## <span data-ttu-id="cb16e-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cb16e-112">EXAMPLES</span></span>

### <span data-ttu-id="cb16e-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="cb16e-113">Example 1</span></span>
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

<span data-ttu-id="cb16e-114">Открывает сетевое подключение в соответствии с указанными данными запроса на подключение.</span><span class="sxs-lookup"><span data-stu-id="cb16e-114">Opens up a network connection according to the specified connection request data.</span></span>

## <span data-ttu-id="cb16e-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cb16e-115">PARAMETERS</span></span>

### <span data-ttu-id="cb16e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb16e-116">-DefaultProfile</span></span>
<span data-ttu-id="cb16e-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cb16e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb16e-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cb16e-118">-InputObject</span></span>
<span data-ttu-id="cb16e-119">Объект input.</span><span class="sxs-lookup"><span data-stu-id="cb16e-119">Input Object.</span></span>

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

### <span data-ttu-id="cb16e-120">-Location</span><span class="sxs-lookup"><span data-stu-id="cb16e-120">-Location</span></span>
<span data-ttu-id="cb16e-121">Поиска.</span><span class="sxs-lookup"><span data-stu-id="cb16e-121">Location.</span></span>

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

### <span data-ttu-id="cb16e-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="cb16e-122">-Name</span></span>
<span data-ttu-id="cb16e-123">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="cb16e-123">Resource name.</span></span>

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

### <span data-ttu-id="cb16e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb16e-124">-ResourceGroupName</span></span>
<span data-ttu-id="cb16e-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cb16e-125">Resource group name.</span></span>

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

### <span data-ttu-id="cb16e-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cb16e-126">-ResourceId</span></span>
<span data-ttu-id="cb16e-127">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="cb16e-127">Resource ID.</span></span>

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

### <span data-ttu-id="cb16e-128">-VirtualMachine</span><span class="sxs-lookup"><span data-stu-id="cb16e-128">-VirtualMachine</span></span>
<span data-ttu-id="cb16e-129">Автоматическая подготовка.</span><span class="sxs-lookup"><span data-stu-id="cb16e-129">Automatic Provisioning.</span></span>

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

### <span data-ttu-id="cb16e-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cb16e-130">-Confirm</span></span>
<span data-ttu-id="cb16e-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="cb16e-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb16e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb16e-132">-WhatIf</span></span>
<span data-ttu-id="cb16e-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="cb16e-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cb16e-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="cb16e-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb16e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb16e-135">CommonParameters</span></span>
<span data-ttu-id="cb16e-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cb16e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb16e-137">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cb16e-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb16e-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cb16e-138">INPUTS</span></span>

### <span data-ttu-id="cb16e-139">System. String</span><span class="sxs-lookup"><span data-stu-id="cb16e-139">System.String</span></span>

### <span data-ttu-id="cb16e-140">Microsoft. Azure. Commands. Security. командлеты. JitNetworkAccessPolicies. PSSecurityJitNetworkAccessPolicyInitiateInputObject</span><span class="sxs-lookup"><span data-stu-id="cb16e-140">Microsoft.Azure.Commands.Security.Cmdlets.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyInitiateInputObject</span></span>

## <span data-ttu-id="cb16e-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cb16e-141">OUTPUTS</span></span>

### <span data-ttu-id="cb16e-142">Microsoft. Azure. Commands. Security. Models. JitNetworkAccessPolicies. PSSecurityJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="cb16e-142">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="cb16e-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="cb16e-143">NOTES</span></span>

## <span data-ttu-id="cb16e-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cb16e-144">RELATED LINKS</span></span>
