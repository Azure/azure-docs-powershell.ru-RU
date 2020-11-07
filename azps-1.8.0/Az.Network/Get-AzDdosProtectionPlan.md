---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azddosprotectionplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzDdosProtectionPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzDdosProtectionPlan.md
ms.openlocfilehash: 729f89742c7dd3249124f2d2404ab85f08db0e86
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93730616"
---
# <span data-ttu-id="457b7-101">Get-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="457b7-101">Get-AzDdosProtectionPlan</span></span>

## <span data-ttu-id="457b7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="457b7-102">SYNOPSIS</span></span>
<span data-ttu-id="457b7-103">Возвращает план защиты Distributed.</span><span class="sxs-lookup"><span data-stu-id="457b7-103">Gets a DDoS protection plan.</span></span>

## <span data-ttu-id="457b7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="457b7-104">SYNTAX</span></span>

```
Get-AzDdosProtectionPlan [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="457b7-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="457b7-105">DESCRIPTION</span></span>
<span data-ttu-id="457b7-106">Командлет Get-AzDdosProtectionPlan получает план защиты Distributed.</span><span class="sxs-lookup"><span data-stu-id="457b7-106">The Get-AzDdosProtectionPlan cmdlet gets a DDoS protection plan.</span></span>

## <span data-ttu-id="457b7-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="457b7-107">EXAMPLES</span></span>

### <span data-ttu-id="457b7-108">Пример 1: получение определенного плана защиты Distributed</span><span class="sxs-lookup"><span data-stu-id="457b7-108">Example 1: Get a specific DDoS protection plan</span></span>
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

<span data-ttu-id="457b7-109">В этом случае необходимо указать оба атрибута: **ResourceGroupName** и **Name** , соответствующие группе ресурсов и имя плана защиты Distributed соответственно.</span><span class="sxs-lookup"><span data-stu-id="457b7-109">In this case, we need to specify both **ResourceGroupName** and **Name** attributes, which correspond to the resource group and the name of the DDoS protection plan, respectively.</span></span>

### <span data-ttu-id="457b7-110">Пример 2: получение всех планов защиты Distributed в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="457b7-110">Example 2: Get all DDoS protection plans in a resource group</span></span>
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

<span data-ttu-id="457b7-111">В этом сценарии мы указываем параметр **ResourceGroupName** только для получения списка планов защиты Distributed.</span><span class="sxs-lookup"><span data-stu-id="457b7-111">In this scenario, we only specify the parameter **ResourceGroupName** to get a list of DDoS protection plans.</span></span>

### <span data-ttu-id="457b7-112">Пример 3: получение всех планов защиты Distributed в подписке</span><span class="sxs-lookup"><span data-stu-id="457b7-112">Example 3: Get all DDoS protection plans in a subscription</span></span>
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

<span data-ttu-id="457b7-113">Здесь мы не указываем никакие параметры, чтобы получить список всех планов защиты Distributed в подписке.</span><span class="sxs-lookup"><span data-stu-id="457b7-113">Here, we do not specify any parameters to get a list of all DDoS protection plans in a subscription.</span></span>

### <span data-ttu-id="457b7-114">Пример 4: получение всех планов защиты Distributed в подписке</span><span class="sxs-lookup"><span data-stu-id="457b7-114">Example 4: Get all DDoS protection plans in a subscription</span></span>
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

<span data-ttu-id="457b7-115">Этот командлет возвращает все DdosProtectionPlans, которые начинаются с "Test".</span><span class="sxs-lookup"><span data-stu-id="457b7-115">This cmdlet returns all DdosProtectionPlans that start with "test".</span></span>

## <span data-ttu-id="457b7-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="457b7-116">PARAMETERS</span></span>

### <span data-ttu-id="457b7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="457b7-117">-DefaultProfile</span></span>
<span data-ttu-id="457b7-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="457b7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="457b7-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="457b7-119">-Name</span></span>
<span data-ttu-id="457b7-120">Указывает имя плана защиты Distributed.</span><span class="sxs-lookup"><span data-stu-id="457b7-120">Specifies the name of the DDoS protection plan.</span></span>

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

### <span data-ttu-id="457b7-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="457b7-121">-ResourceGroupName</span></span>
<span data-ttu-id="457b7-122">Указывает имя группы ресурсов для плана защиты Distributed.</span><span class="sxs-lookup"><span data-stu-id="457b7-122">Specifies the name of the DDoS protection plan resource group.</span></span>

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

### <span data-ttu-id="457b7-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="457b7-123">CommonParameters</span></span>
<span data-ttu-id="457b7-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="457b7-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="457b7-125">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="457b7-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="457b7-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="457b7-126">INPUTS</span></span>

### <span data-ttu-id="457b7-127">System. String</span><span class="sxs-lookup"><span data-stu-id="457b7-127">System.String</span></span>

## <span data-ttu-id="457b7-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="457b7-128">OUTPUTS</span></span>

### <span data-ttu-id="457b7-129">Microsoft.Azure.Commands.Network.Models.PSDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="457b7-129">Microsoft.Azure.Commands.Network.Models.PSDdosProtectionPlan</span></span>

## <span data-ttu-id="457b7-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="457b7-130">NOTES</span></span>

## <span data-ttu-id="457b7-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="457b7-131">RELATED LINKS</span></span>

[<span data-ttu-id="457b7-132">New-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="457b7-132">New-AzDdosProtectionPlan</span></span>](./New-AzDdosProtectionPlan.md)

[<span data-ttu-id="457b7-133">Remove-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="457b7-133">Remove-AzDdosProtectionPlan</span></span>](./Remove-AzDdosProtectionPlan.md)

[<span data-ttu-id="457b7-134">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="457b7-134">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="457b7-135">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="457b7-135">Set-AzVirtualNetwork</span></span>](./Set-AzVirtualNetwork.md)

[<span data-ttu-id="457b7-136">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="457b7-136">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)