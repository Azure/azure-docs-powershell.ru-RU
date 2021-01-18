---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzJitNetworkAccessPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzJitNetworkAccessPolicy.md
ms.openlocfilehash: e82c540b946408671c424a1f86d3266a7e6d6906
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98517753"
---
# <span data-ttu-id="ed21e-101">Get-AzJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ed21e-101">Get-AzJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="ed21e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed21e-102">SYNOPSIS</span></span>
<span data-ttu-id="ed21e-103">Получает политики сетевого доступа JIT</span><span class="sxs-lookup"><span data-stu-id="ed21e-103">Gets the JIT network access policies</span></span>

## <span data-ttu-id="ed21e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ed21e-104">SYNTAX</span></span>

### <span data-ttu-id="ed21e-105">SubscriptionScope (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ed21e-105">SubscriptionScope (Default)</span></span>
```
Get-AzJitNetworkAccessPolicy [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ed21e-106">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="ed21e-106">ResourceGroupScope</span></span>
```
Get-AzJitNetworkAccessPolicy -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ed21e-107">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="ed21e-107">ResourceGroupLevelResource</span></span>
```
Get-AzJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ed21e-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="ed21e-108">ResourceId</span></span>
```
Get-AzJitNetworkAccessPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ed21e-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ed21e-109">DESCRIPTION</span></span>
<span data-ttu-id="ed21e-110">Политики сетевого доступа JIT позволяют определить политику, которая позволит простым пользователям создать временное сетевое подключение к VM.</span><span class="sxs-lookup"><span data-stu-id="ed21e-110">Just In Time (JIT) network access policies let you define a policy the will allow simple users to create a temporary network connection to a VM.</span></span>
<span data-ttu-id="ed21e-111">Политика определяет порты, IP-адреса протоколов и ip-адресов источника, которые могут запрашивать подключение к VM-порту, и максимальную продолжительность перед автоматическим закрытием подключения.</span><span class="sxs-lookup"><span data-stu-id="ed21e-111">The policy defines what ports, protocol and source IP addresses can request a connection to a VM and the max duration before the connection will be closed automatically.</span></span>
<span data-ttu-id="ed21e-112">В политике также можно увидеть запрос на подключение, сделанный с этой политикой.</span><span class="sxs-lookup"><span data-stu-id="ed21e-112">In the policy you can also see the connection request that were made with this policy.</span></span> 

## <span data-ttu-id="ed21e-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ed21e-113">EXAMPLES</span></span>

### <span data-ttu-id="ed21e-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ed21e-114">Example 1</span></span>
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

<span data-ttu-id="ed21e-115">Получить всеполядные действия по сетевому доступу JIT для подписки</span><span class="sxs-lookup"><span data-stu-id="ed21e-115">Get all the JIT network access polices on a subscription</span></span>

### <span data-ttu-id="ed21e-116">Пример 2</span><span class="sxs-lookup"><span data-stu-id="ed21e-116">Example 2</span></span>
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

<span data-ttu-id="ed21e-117">Получить все групповые дела о сетевом доступе JIT в группе ресурсов "МойСлужба1"</span><span class="sxs-lookup"><span data-stu-id="ed21e-117">Get all the JIT network access polices on the "myService1" resource group</span></span>

### <span data-ttu-id="ed21e-118">Пример 3</span><span class="sxs-lookup"><span data-stu-id="ed21e-118">Example 3</span></span>
```powershell
PS C:\> Get-AzJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default"
Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/testService}
Requests          : {Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyRequest}
ProvisioningState : Succeeded
```

<span data-ttu-id="ed21e-119">Получает определенную политику доступа к сети JIT</span><span class="sxs-lookup"><span data-stu-id="ed21e-119">Gets a specific JIT network access policy</span></span>

## <span data-ttu-id="ed21e-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ed21e-120">PARAMETERS</span></span>

### <span data-ttu-id="ed21e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed21e-121">-DefaultProfile</span></span>
<span data-ttu-id="ed21e-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ed21e-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed21e-123">-Location</span><span class="sxs-lookup"><span data-stu-id="ed21e-123">-Location</span></span>
<span data-ttu-id="ed21e-124">"Расположение".</span><span class="sxs-lookup"><span data-stu-id="ed21e-124">Location.</span></span>

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

### <span data-ttu-id="ed21e-125">-Name</span><span class="sxs-lookup"><span data-stu-id="ed21e-125">-Name</span></span>
<span data-ttu-id="ed21e-126">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="ed21e-126">Resource name.</span></span>

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

### <span data-ttu-id="ed21e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed21e-127">-ResourceGroupName</span></span>
<span data-ttu-id="ed21e-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ed21e-128">Resource group name.</span></span>

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

### <span data-ttu-id="ed21e-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ed21e-129">-ResourceId</span></span>
<span data-ttu-id="ed21e-130">ИД ресурса политики сетевого доступа jit.</span><span class="sxs-lookup"><span data-stu-id="ed21e-130">The resource id of the jit Network Access Policy resource.</span></span>

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

### <span data-ttu-id="ed21e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed21e-131">CommonParameters</span></span>
<span data-ttu-id="ed21e-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed21e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed21e-133">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ed21e-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed21e-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ed21e-134">INPUTS</span></span>

### <span data-ttu-id="ed21e-135">System.String</span><span class="sxs-lookup"><span data-stu-id="ed21e-135">System.String</span></span>

## <span data-ttu-id="ed21e-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ed21e-136">OUTPUTS</span></span>

### <span data-ttu-id="ed21e-137">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ed21e-137">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="ed21e-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ed21e-138">NOTES</span></span>

## <span data-ttu-id="ed21e-139">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ed21e-139">RELATED LINKS</span></span>
