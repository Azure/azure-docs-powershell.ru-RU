---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmJitNetworkAccessPolicy.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmJitNetworkAccessPolicy.md
ms.openlocfilehash: 72e3cf48f112c5e9bb07a8f7eb57dfe3d4c9ee07
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562631"
---
# <span data-ttu-id="59d21-101">Set-AzureRmJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="59d21-101">Set-AzureRmJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="59d21-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="59d21-102">SYNOPSIS</span></span>
<span data-ttu-id="59d21-103">Обновляет политику JIT-доступа к сети.</span><span class="sxs-lookup"><span data-stu-id="59d21-103">Updates JIT network access policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="59d21-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="59d21-104">SYNTAX</span></span>

```
Set-AzureRmJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String>
 -VirtualMachine <PSSecurityJitNetworkAccessPolicyVirtualMachine[]> -Kind <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59d21-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="59d21-105">DESCRIPTION</span></span>
<span data-ttu-id="59d21-106">Обновляет политику JIT-доступа к сети.</span><span class="sxs-lookup"><span data-stu-id="59d21-106">Updates JIT network access policy.</span></span>

## <span data-ttu-id="59d21-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="59d21-107">EXAMPLES</span></span>

### <span data-ttu-id="59d21-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="59d21-108">Example 1</span></span>
```powershell
PS C:\> Set-AzureRmJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default" -VirtualMachine $vmRules -Kind "Basic"

Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/testService}
Requests          : {}
ProvisioningState : Succeeded
```

<span data-ttu-id="59d21-109">Обновляет политику JIT-доступа к сети с помощью новых правил виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="59d21-109">Updates a JIT network access policy with new VM rules.</span></span>

## <span data-ttu-id="59d21-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="59d21-110">PARAMETERS</span></span>

### <span data-ttu-id="59d21-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59d21-111">-DefaultProfile</span></span>
<span data-ttu-id="59d21-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="59d21-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59d21-113">-Видах</span><span class="sxs-lookup"><span data-stu-id="59d21-113">-Kind</span></span>
<span data-ttu-id="59d21-114">Любые.</span><span class="sxs-lookup"><span data-stu-id="59d21-114">Kind.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59d21-115">-Location</span><span class="sxs-lookup"><span data-stu-id="59d21-115">-Location</span></span>
<span data-ttu-id="59d21-116">Поиска.</span><span class="sxs-lookup"><span data-stu-id="59d21-116">Location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59d21-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="59d21-117">-Name</span></span>
<span data-ttu-id="59d21-118">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="59d21-118">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59d21-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59d21-119">-ResourceGroupName</span></span>
<span data-ttu-id="59d21-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="59d21-120">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59d21-121">-VirtualMachine</span><span class="sxs-lookup"><span data-stu-id="59d21-121">-VirtualMachine</span></span>
<span data-ttu-id="59d21-122">Virutal машины.</span><span class="sxs-lookup"><span data-stu-id="59d21-122">Virutal Machines.</span></span>

```yaml
Type: PSSecurityJitNetworkAccessPolicyVirtualMachine[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59d21-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="59d21-123">-Confirm</span></span>
<span data-ttu-id="59d21-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="59d21-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59d21-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59d21-125">-WhatIf</span></span>
<span data-ttu-id="59d21-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="59d21-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="59d21-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="59d21-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59d21-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59d21-128">CommonParameters</span></span>
<span data-ttu-id="59d21-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="59d21-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59d21-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59d21-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59d21-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="59d21-131">INPUTS</span></span>

### <span data-ttu-id="59d21-132">System. String</span><span class="sxs-lookup"><span data-stu-id="59d21-132">System.String</span></span>
<span data-ttu-id="59d21-133">Microsoft. Azure. Commands. Security. Models. JitNetworkAccessPolicies. PSSecurityJitNetworkAccessPolicyVirtualMachine []</span><span class="sxs-lookup"><span data-stu-id="59d21-133">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyVirtualMachine[]</span></span>

## <span data-ttu-id="59d21-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="59d21-134">OUTPUTS</span></span>

### <span data-ttu-id="59d21-135">Microsoft. Azure. Commands. Security. Models. JitNetworkAccessPolicies. PSSecurityJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="59d21-135">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="59d21-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="59d21-136">NOTES</span></span>

## <span data-ttu-id="59d21-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="59d21-137">RELATED LINKS</span></span>
