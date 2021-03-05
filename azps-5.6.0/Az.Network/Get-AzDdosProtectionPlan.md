---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azddosprotectionplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzDdosProtectionPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzDdosProtectionPlan.md
ms.openlocfilehash: 2b5cc008e96d12828d5f834fd5fa4a30f83ea70f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967955"
---
# <span data-ttu-id="9ea5f-101">Get-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="9ea5f-101">Get-AzDdosProtectionPlan</span></span>

## <span data-ttu-id="9ea5f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ea5f-102">SYNOPSIS</span></span>
<span data-ttu-id="9ea5f-103">Получает план защиты DDoS.</span><span class="sxs-lookup"><span data-stu-id="9ea5f-103">Gets a DDoS protection plan.</span></span>

## <span data-ttu-id="9ea5f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9ea5f-104">SYNTAX</span></span>

```
Get-AzDdosProtectionPlan [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9ea5f-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9ea5f-105">DESCRIPTION</span></span>
<span data-ttu-id="9ea5f-106">Этот Get-AzDdosProtectionPlan получает план защиты DDoS.</span><span class="sxs-lookup"><span data-stu-id="9ea5f-106">The Get-AzDdosProtectionPlan cmdlet gets a DDoS protection plan.</span></span>

## <span data-ttu-id="9ea5f-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9ea5f-107">EXAMPLES</span></span>

### <span data-ttu-id="9ea5f-108">Пример 1. Получите определенный план защиты DDoS</span><span class="sxs-lookup"><span data-stu-id="9ea5f-108">Example 1: Get a specific DDoS protection plan</span></span>
```
D:\> Get-AzDdosProtectionPlan -ResourceGroupName ResourceGroupName -Name DdosProtectionPlanName


Name              : DdosProtectionPlanName
Id                : /subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/ddosProtectionPlans/DdosProtectionPlanName
Etag              : W/"a20e5592-9b51-423b-9758-b00cd322f744"
ProvisioningState : Succeeded
VirtualNetworks   : [
                      {
                        "Id": "/subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/virtualNetworks/VnetName"
                      }
                    ]
```

<span data-ttu-id="9ea5f-109">В этом случае нам нужно указать атрибуты **ResourceGroupName** и **Name,** соответствующие группе ресурсов и названию плана защиты DDoS соответственно.</span><span class="sxs-lookup"><span data-stu-id="9ea5f-109">In this case, we need to specify both **ResourceGroupName** and **Name** attributes, which correspond to the resource group and the name of the DDoS protection plan, respectively.</span></span>

### <span data-ttu-id="9ea5f-110">Пример 2. Все планы защиты DDoS в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="9ea5f-110">Example 2: Get all DDoS protection plans in a resource group</span></span>
```
D:\> Get-AzDdosProtectionPlan -ResourceGroupName ResourceGroupName


Name              : DdosProtectionPlanName
Id                : /subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/ddosProtectionPlans/DdosProtectionPlanName
Etag              : W/"a20e5592-9b51-423b-9758-b00cd322f744"
ProvisioningState : Succeeded
VirtualNetworks   : [
                      {
                        "Id": "/subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/virtualNetworks/VnetName"
                      }
                    ]
```

<span data-ttu-id="9ea5f-111">В этом сценарии для получения списка планов защиты DDoS указывается только параметр **ResourceGroupName.**</span><span class="sxs-lookup"><span data-stu-id="9ea5f-111">In this scenario, we only specify the parameter **ResourceGroupName** to get a list of DDoS protection plans.</span></span>

### <span data-ttu-id="9ea5f-112">Пример 3. Все планы защиты DDoS в подписке</span><span class="sxs-lookup"><span data-stu-id="9ea5f-112">Example 3: Get all DDoS protection plans in a subscription</span></span>
```
D:\> Get-AzDdosProtectionPlan


Name              : DdosProtectionPlanName
Id                : /subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/ddosProtectionPlans/DdosProtectionPlanName
Etag              : W/"a20e5592-9b51-423b-9758-b00cd322f744"
ProvisioningState : Succeeded
VirtualNetworks   : [
                      {
                        "Id": "/subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/virtualNetworks/VnetName"
                      }
                    ]
```

<span data-ttu-id="9ea5f-113">Здесь не указаны параметры для получения списка всех планов защиты DDoS в подписке.</span><span class="sxs-lookup"><span data-stu-id="9ea5f-113">Here, we do not specify any parameters to get a list of all DDoS protection plans in a subscription.</span></span>

### <span data-ttu-id="9ea5f-114">Пример 4. Все планы защиты DDoS в подписке</span><span class="sxs-lookup"><span data-stu-id="9ea5f-114">Example 4: Get all DDoS protection plans in a subscription</span></span>
```
D:\> Get-AzDdosProtectionPlan -Name test*


Name              : test1
Id                : /subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/ddosProtectionPlans/test1
Etag              : W/"a20e5592-9b51-423b-9758-b00cd322f744"
ProvisioningState : Succeeded
VirtualNetworks   : [
                      {
                        "Id": "/subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/virtualNetworks/VnetName"
                      }
                    ]

Name              : test2
Id                : /subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/ddosProtectionPlans/test2
Etag              : W/"a20e5592-9b51-423b-9758-b00cd322f744"
ProvisioningState : Succeeded
VirtualNetworks   : [
                      {
                        "Id": "/subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/virtualNetworks/VnetName"
                      }
                    ]
```

<span data-ttu-id="9ea5f-115">Этот cmdlet возвращает все DdosProtectionPlans, которые начинаются с "test".</span><span class="sxs-lookup"><span data-stu-id="9ea5f-115">This cmdlet returns all DdosProtectionPlans that start with "test".</span></span>

## <span data-ttu-id="9ea5f-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9ea5f-116">PARAMETERS</span></span>

### <span data-ttu-id="9ea5f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ea5f-117">-DefaultProfile</span></span>
<span data-ttu-id="9ea5f-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9ea5f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ea5f-119">-Name</span><span class="sxs-lookup"><span data-stu-id="9ea5f-119">-Name</span></span>
<span data-ttu-id="9ea5f-120">Имя плана защиты DDoS.</span><span class="sxs-lookup"><span data-stu-id="9ea5f-120">Specifies the name of the DDoS protection plan.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="9ea5f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ea5f-121">-ResourceGroupName</span></span>
<span data-ttu-id="9ea5f-122">Имя группы ресурсов плана защиты DDoS.</span><span class="sxs-lookup"><span data-stu-id="9ea5f-122">Specifies the name of the DDoS protection plan resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="9ea5f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ea5f-123">CommonParameters</span></span>
<span data-ttu-id="9ea5f-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ea5f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ea5f-125">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9ea5f-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ea5f-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9ea5f-126">INPUTS</span></span>

### <span data-ttu-id="9ea5f-127">System.String</span><span class="sxs-lookup"><span data-stu-id="9ea5f-127">System.String</span></span>

## <span data-ttu-id="9ea5f-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9ea5f-128">OUTPUTS</span></span>

### <span data-ttu-id="9ea5f-129">Microsoft.Azure.Commands.Network.Models.PSDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="9ea5f-129">Microsoft.Azure.Commands.Network.Models.PSDdosProtectionPlan</span></span>

## <span data-ttu-id="9ea5f-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9ea5f-130">NOTES</span></span>

## <span data-ttu-id="9ea5f-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9ea5f-131">RELATED LINKS</span></span>

[<span data-ttu-id="9ea5f-132">New-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="9ea5f-132">New-AzDdosProtectionPlan</span></span>](./New-AzDdosProtectionPlan.md)

[<span data-ttu-id="9ea5f-133">Remove-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="9ea5f-133">Remove-AzDdosProtectionPlan</span></span>](./Remove-AzDdosProtectionPlan.md)

[<span data-ttu-id="9ea5f-134">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="9ea5f-134">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="9ea5f-135">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="9ea5f-135">Set-AzVirtualNetwork</span></span>](./Set-AzVirtualNetwork.md)

[<span data-ttu-id="9ea5f-136">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="9ea5f-136">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)