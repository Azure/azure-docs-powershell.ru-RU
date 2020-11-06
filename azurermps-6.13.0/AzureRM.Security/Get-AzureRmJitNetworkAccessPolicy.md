---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmJitNetworkAccessPolicy.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmJitNetworkAccessPolicy.md
ms.openlocfilehash: bd366b636a29a08bea9124b3c3f4b9b423dc4deb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558284"
---
# <span data-ttu-id="89b08-101">Get-AzureRmJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="89b08-101">Get-AzureRmJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="89b08-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="89b08-102">SYNOPSIS</span></span>
<span data-ttu-id="89b08-103">Получает политики доступа к сети JIT</span><span class="sxs-lookup"><span data-stu-id="89b08-103">Gets the JIT network access policies</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="89b08-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="89b08-104">SYNTAX</span></span>

### <span data-ttu-id="89b08-105">SubscriptionScope (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="89b08-105">SubscriptionScope (Default)</span></span>
```
Get-AzureRmJitNetworkAccessPolicy [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="89b08-106">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="89b08-106">ResourceGroupScope</span></span>
```
Get-AzureRmJitNetworkAccessPolicy -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="89b08-107">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="89b08-107">ResourceGroupLevelResource</span></span>
```
Get-AzureRmJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="89b08-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="89b08-108">ResourceId</span></span>
```
Get-AzureRmJitNetworkAccessPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="89b08-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="89b08-109">DESCRIPTION</span></span>
<span data-ttu-id="89b08-110">Политики доступа к сети по времени (JIT) позволяют определять политику, благодаря которой пользователи смогут создавать временное сетевое подключение к виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="89b08-110">Just In Time (JIT) network access policies let you define a policy the will allow simple users to create a temporary network connection to a VM.</span></span>
<span data-ttu-id="89b08-111">Политика определяет, какие порты, протоколы и IP-адреса источника могут запрашивать подключение к виртуальной машине и максимальную продолжительность до автоматического закрытия подключения.</span><span class="sxs-lookup"><span data-stu-id="89b08-111">The policy defines what ports, protocol and source IP addresses can request a connection to a VM and the max duration before the connection will be closed automatically.</span></span>
<span data-ttu-id="89b08-112">В политике также можно увидеть запрос на подключение, созданный с помощью этой политики.</span><span class="sxs-lookup"><span data-stu-id="89b08-112">In the policy you can also see the connection request that were made with this policy.</span></span> 

## <span data-ttu-id="89b08-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="89b08-113">EXAMPLES</span></span>

### <span data-ttu-id="89b08-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="89b08-114">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmJitNetworkAccessPolicy
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

<span data-ttu-id="89b08-115">Получение всех политик доступа к сети JIT для подписки</span><span class="sxs-lookup"><span data-stu-id="89b08-115">Get all the JIT network access polices on a subscription</span></span>

### <span data-ttu-id="89b08-116">Пример 2</span><span class="sxs-lookup"><span data-stu-id="89b08-116">Example 2</span></span>
```powershell
PS C:\> Get-AzureRmJitNetworkAccessPolicy -ResourceGroupName "myService1"
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

<span data-ttu-id="89b08-117">Получение всех политик доступа к сети по JIT для группы ресурсов "myService1"</span><span class="sxs-lookup"><span data-stu-id="89b08-117">Get all the JIT network access polices on the "myService1" resource group</span></span>

### <span data-ttu-id="89b08-118">Пример 3</span><span class="sxs-lookup"><span data-stu-id="89b08-118">Example 3</span></span>
```powershell
PS C:\> Get-AzureRmJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default"
Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/testService}
Requests          : {Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyRequest}
ProvisioningState : Succeeded
```

<span data-ttu-id="89b08-119">Возвращает определенную политику JIT-доступа к сети.</span><span class="sxs-lookup"><span data-stu-id="89b08-119">Gets a specific JIT network access policy</span></span>

## <span data-ttu-id="89b08-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="89b08-120">PARAMETERS</span></span>

### <span data-ttu-id="89b08-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89b08-121">-DefaultProfile</span></span>
<span data-ttu-id="89b08-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="89b08-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89b08-123">-Location</span><span class="sxs-lookup"><span data-stu-id="89b08-123">-Location</span></span>
<span data-ttu-id="89b08-124">Поиска.</span><span class="sxs-lookup"><span data-stu-id="89b08-124">Location.</span></span>

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

### <span data-ttu-id="89b08-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="89b08-125">-Name</span></span>
<span data-ttu-id="89b08-126">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="89b08-126">Resource name.</span></span>

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

### <span data-ttu-id="89b08-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89b08-127">-ResourceGroupName</span></span>
<span data-ttu-id="89b08-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="89b08-128">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupScope, ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89b08-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="89b08-129">-ResourceId</span></span>
<span data-ttu-id="89b08-130">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="89b08-130">Resource ID.</span></span>

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

### <span data-ttu-id="89b08-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89b08-131">CommonParameters</span></span>
<span data-ttu-id="89b08-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="89b08-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89b08-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89b08-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89b08-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="89b08-134">INPUTS</span></span>

### <span data-ttu-id="89b08-135">System. String</span><span class="sxs-lookup"><span data-stu-id="89b08-135">System.String</span></span>

## <span data-ttu-id="89b08-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="89b08-136">OUTPUTS</span></span>

### <span data-ttu-id="89b08-137">Microsoft. Azure. Commands. Security. Models. JitNetworkAccessPolicies. PSSecurityJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="89b08-137">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="89b08-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="89b08-138">NOTES</span></span>

## <span data-ttu-id="89b08-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="89b08-139">RELATED LINKS</span></span>
