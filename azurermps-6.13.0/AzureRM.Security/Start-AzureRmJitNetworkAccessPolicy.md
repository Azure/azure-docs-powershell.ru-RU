---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Start-AzureRmJitNetworkAccessPolicy.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Start-AzureRmJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Start-AzureRmJitNetworkAccessPolicy.md
ms.openlocfilehash: 62dccdc3b55caa5d63036ed3298caa5a01514342
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567238"
---
# <span data-ttu-id="da3a2-101">Start-AzureRmJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="da3a2-101">Start-AzureRmJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="da3a2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="da3a2-102">SYNOPSIS</span></span>
<span data-ttu-id="da3a2-103">Вызывает временный запрос на доступ к сети.</span><span class="sxs-lookup"><span data-stu-id="da3a2-103">Invokes a temporary network access request.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="da3a2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="da3a2-104">SYNTAX</span></span>

### <span data-ttu-id="da3a2-105">ResourceGroupLevelResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="da3a2-105">ResourceGroupLevelResource (Default)</span></span>
```
Start-AzureRmJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String>
 -VirtualMachine <PSSecurityJitNetworkAccessPolicyInitiateVirtualMachine[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da3a2-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="da3a2-106">ResourceId</span></span>
```
Start-AzureRmJitNetworkAccessPolicy -VirtualMachine <PSSecurityJitNetworkAccessPolicyInitiateVirtualMachine[]>
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da3a2-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="da3a2-107">InputObject</span></span>
```
Start-AzureRmJitNetworkAccessPolicy -InputObject <PSSecurityJitNetworkAccessPolicyInitiateInputObject>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da3a2-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="da3a2-108">DESCRIPTION</span></span>
<span data-ttu-id="da3a2-109">Вызывает временный запрос на доступ к сети.</span><span class="sxs-lookup"><span data-stu-id="da3a2-109">Invokes a temporary network access request.</span></span>
<span data-ttu-id="da3a2-110">Запрос проверяются на соответствие настроенной политике доступа к сети JIT и, если permittet, открывает сетевое подключение в соответствии с запросом пользователя.</span><span class="sxs-lookup"><span data-stu-id="da3a2-110">The request is validated against the configured JIT network access policy and if permittet, opens up a network connection according to the user's request.</span></span>
<span data-ttu-id="da3a2-111">Запрос будет loged в политике для более поздней проверки и будет прекращен, когда будет превышена Указанная длительность.</span><span class="sxs-lookup"><span data-stu-id="da3a2-111">The request will be loged in the policy for later review and will be terminated when the specified duration will be exceeded.</span></span>

## <span data-ttu-id="da3a2-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="da3a2-112">EXAMPLES</span></span>

### <span data-ttu-id="da3a2-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="da3a2-113">Example 1</span></span>
```powershell
PS C:\> Set-AzureRmJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default" -Kind "Basic" -VirtualMachine $vms

Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.S
                    ecurity/locations/centralus/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.
                    Compute/virtualMachines/testService}
Requests          : {}
ProvisioningState : Succeeded
```

<span data-ttu-id="da3a2-114">Открывает сетевое подключение в соответствии с указанными данными запроса на подключение.</span><span class="sxs-lookup"><span data-stu-id="da3a2-114">Opens up a network connection according to the specified connection request data.</span></span>

## <span data-ttu-id="da3a2-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="da3a2-115">PARAMETERS</span></span>

### <span data-ttu-id="da3a2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da3a2-116">-DefaultProfile</span></span>
<span data-ttu-id="da3a2-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="da3a2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da3a2-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="da3a2-118">-InputObject</span></span>
<span data-ttu-id="da3a2-119">Объект input.</span><span class="sxs-lookup"><span data-stu-id="da3a2-119">Input Object.</span></span>

```yaml
Type: PSSecurityJitNetworkAccessPolicyInitiateInputObject
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="da3a2-120">-Location</span><span class="sxs-lookup"><span data-stu-id="da3a2-120">-Location</span></span>
<span data-ttu-id="da3a2-121">Поиска.</span><span class="sxs-lookup"><span data-stu-id="da3a2-121">Location.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da3a2-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="da3a2-122">-Name</span></span>
<span data-ttu-id="da3a2-123">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="da3a2-123">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da3a2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da3a2-124">-ResourceGroupName</span></span>
<span data-ttu-id="da3a2-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="da3a2-125">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da3a2-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="da3a2-126">-ResourceId</span></span>
<span data-ttu-id="da3a2-127">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="da3a2-127">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da3a2-128">-VirtualMachine</span><span class="sxs-lookup"><span data-stu-id="da3a2-128">-VirtualMachine</span></span>
<span data-ttu-id="da3a2-129">Автоматическая подготовка.</span><span class="sxs-lookup"><span data-stu-id="da3a2-129">Automatic Provisioning.</span></span>

```yaml
Type: PSSecurityJitNetworkAccessPolicyInitiateVirtualMachine[]
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da3a2-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="da3a2-130">-Confirm</span></span>
<span data-ttu-id="da3a2-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="da3a2-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da3a2-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da3a2-132">-WhatIf</span></span>
<span data-ttu-id="da3a2-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="da3a2-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="da3a2-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="da3a2-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da3a2-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da3a2-135">CommonParameters</span></span>
<span data-ttu-id="da3a2-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="da3a2-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da3a2-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da3a2-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da3a2-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="da3a2-138">INPUTS</span></span>

### <span data-ttu-id="da3a2-139">System. String</span><span class="sxs-lookup"><span data-stu-id="da3a2-139">System.String</span></span>
<span data-ttu-id="da3a2-140">Microsoft. Azure. Commands. Security. Models. JitNetworkAccessPolicies. PSSecurityJitNetworkAccessPolicyInitiateVirtualMachine []</span><span class="sxs-lookup"><span data-stu-id="da3a2-140">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyInitiateVirtualMachine[]</span></span>

## <span data-ttu-id="da3a2-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="da3a2-141">OUTPUTS</span></span>

### <span data-ttu-id="da3a2-142">Microsoft. Azure. Commands. Security. Models. JitNetworkAccessPolicies. PSSecurityJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="da3a2-142">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="da3a2-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="da3a2-143">NOTES</span></span>

## <span data-ttu-id="da3a2-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="da3a2-144">RELATED LINKS</span></span>
