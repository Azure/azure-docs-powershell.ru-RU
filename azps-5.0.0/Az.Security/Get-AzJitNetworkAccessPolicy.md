---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzJitNetworkAccessPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzJitNetworkAccessPolicy.md
ms.openlocfilehash: c385ca902764d6bf9afa3808d718c2ceb5d1357c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94317600"
---
# <span data-ttu-id="e0c75-101">Get-AzJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e0c75-101">Get-AzJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="e0c75-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e0c75-102">SYNOPSIS</span></span>
<span data-ttu-id="e0c75-103">Получает политики доступа к сети JIT</span><span class="sxs-lookup"><span data-stu-id="e0c75-103">Gets the JIT network access policies</span></span>

## <span data-ttu-id="e0c75-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e0c75-104">SYNTAX</span></span>

### <span data-ttu-id="e0c75-105">SubscriptionScope (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e0c75-105">SubscriptionScope (Default)</span></span>
```
Get-AzJitNetworkAccessPolicy [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e0c75-106">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="e0c75-106">ResourceGroupScope</span></span>
```
Get-AzJitNetworkAccessPolicy -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e0c75-107">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="e0c75-107">ResourceGroupLevelResource</span></span>
```
Get-AzJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e0c75-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="e0c75-108">ResourceId</span></span>
```
Get-AzJitNetworkAccessPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e0c75-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e0c75-109">DESCRIPTION</span></span>
<span data-ttu-id="e0c75-110">Политики доступа к сети по времени (JIT) позволяют определять политику, благодаря которой пользователи смогут создавать временное сетевое подключение к виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="e0c75-110">Just In Time (JIT) network access policies let you define a policy the will allow simple users to create a temporary network connection to a VM.</span></span>
<span data-ttu-id="e0c75-111">Политика определяет, какие порты, протоколы и IP-адреса источника могут запрашивать подключение к виртуальной машине и максимальную продолжительность до автоматического закрытия подключения.</span><span class="sxs-lookup"><span data-stu-id="e0c75-111">The policy defines what ports, protocol and source IP addresses can request a connection to a VM and the max duration before the connection will be closed automatically.</span></span>
<span data-ttu-id="e0c75-112">В политике также можно увидеть запрос на подключение, созданный с помощью этой политики.</span><span class="sxs-lookup"><span data-stu-id="e0c75-112">In the policy you can also see the connection request that were made with this policy.</span></span> 

## <span data-ttu-id="e0c75-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e0c75-113">EXAMPLES</span></span>

### <span data-ttu-id="e0c75-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e0c75-114">Example 1</span></span>
```powershell
PS C:\> Get-AzJitNetworkAccessPolicy
Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/testService}
Requests          : {Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyRequest}
ProvisioningState : Succeeded

Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/northeurope/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/testService}
Requests          : {Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyRequest}
ProvisioningState : Succeeded
```

<span data-ttu-id="e0c75-115">Получение всех политик доступа к сети JIT для подписки</span><span class="sxs-lookup"><span data-stu-id="e0c75-115">Get all the JIT network access polices on a subscription</span></span>

### <span data-ttu-id="e0c75-116">Пример 2</span><span class="sxs-lookup"><span data-stu-id="e0c75-116">Example 2</span></span>
```powershell
PS C:\> Get-AzJitNetworkAccessPolicy -ResourceGroupName "myService1"
Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/testService}
Requests          : {Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyRequest}
ProvisioningState : Succeeded

Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/northeurope/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/testService}
Requests          : {Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyRequest}
ProvisioningState : Succeeded
```

<span data-ttu-id="e0c75-117">Получение всех политик доступа к сети по JIT для группы ресурсов "myService1"</span><span class="sxs-lookup"><span data-stu-id="e0c75-117">Get all the JIT network access polices on the "myService1" resource group</span></span>

### <span data-ttu-id="e0c75-118">Пример 3</span><span class="sxs-lookup"><span data-stu-id="e0c75-118">Example 3</span></span>
```powershell
PS C:\> Get-AzJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default"
Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/testService}
Requests          : {Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyRequest}
ProvisioningState : Succeeded
```

<span data-ttu-id="e0c75-119">Возвращает определенную политику JIT-доступа к сети.</span><span class="sxs-lookup"><span data-stu-id="e0c75-119">Gets a specific JIT network access policy</span></span>

## <span data-ttu-id="e0c75-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e0c75-120">PARAMETERS</span></span>

### <span data-ttu-id="e0c75-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0c75-121">-DefaultProfile</span></span>
<span data-ttu-id="e0c75-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e0c75-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0c75-123">-Location</span><span class="sxs-lookup"><span data-stu-id="e0c75-123">-Location</span></span>
<span data-ttu-id="e0c75-124">Поиска.</span><span class="sxs-lookup"><span data-stu-id="e0c75-124">Location.</span></span>

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

### <span data-ttu-id="e0c75-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e0c75-125">-Name</span></span>
<span data-ttu-id="e0c75-126">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="e0c75-126">Resource name.</span></span>

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

### <span data-ttu-id="e0c75-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0c75-127">-ResourceGroupName</span></span>
<span data-ttu-id="e0c75-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e0c75-128">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupScope, ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0c75-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e0c75-129">-ResourceId</span></span>
<span data-ttu-id="e0c75-130">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="e0c75-130">Resource ID.</span></span>

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

### <span data-ttu-id="e0c75-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0c75-131">CommonParameters</span></span>
<span data-ttu-id="e0c75-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e0c75-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0c75-133">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e0c75-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0c75-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e0c75-134">INPUTS</span></span>

### <span data-ttu-id="e0c75-135">System. String</span><span class="sxs-lookup"><span data-stu-id="e0c75-135">System.String</span></span>

## <span data-ttu-id="e0c75-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e0c75-136">OUTPUTS</span></span>

### <span data-ttu-id="e0c75-137">Microsoft. Azure. Commands. Security. Models. JitNetworkAccessPolicies. PSSecurityJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e0c75-137">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="e0c75-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="e0c75-138">NOTES</span></span>

## <span data-ttu-id="e0c75-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e0c75-139">RELATED LINKS</span></span>
