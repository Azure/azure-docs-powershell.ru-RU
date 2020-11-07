---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azuredosprotectionplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmDdosProtectionPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmDdosProtectionPlan.md
ms.openlocfilehash: 2d1942dd5c069660d062922a069cc88b505748fa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733443"
---
# <span data-ttu-id="721da-101">Get-AzureRmDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="721da-101">Get-AzureRmDdosProtectionPlan</span></span>

## <span data-ttu-id="721da-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="721da-102">SYNOPSIS</span></span>
<span data-ttu-id="721da-103">Возвращает план защиты Distributed.</span><span class="sxs-lookup"><span data-stu-id="721da-103">Gets a DDoS protection plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="721da-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="721da-104">SYNTAX</span></span>

### <span data-ttu-id="721da-105">GetByNameAndGroup</span><span class="sxs-lookup"><span data-stu-id="721da-105">GetByNameAndGroup</span></span>
```
Get-AzureRmDdosProtectionPlan -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="721da-106">Список</span><span class="sxs-lookup"><span data-stu-id="721da-106">List</span></span>
```
Get-AzureRmDdosProtectionPlan [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="721da-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="721da-107">DESCRIPTION</span></span>
<span data-ttu-id="721da-108">Командлет Get-AzureRmDdosProtectionPlan получает план защиты Distributed.</span><span class="sxs-lookup"><span data-stu-id="721da-108">The Get-AzureRmDdosProtectionPlan cmdlet gets a DDoS protection plan.</span></span>

## <span data-ttu-id="721da-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="721da-109">EXAMPLES</span></span>

### <span data-ttu-id="721da-110">Пример 1: получение определенного плана защиты Distributed</span><span class="sxs-lookup"><span data-stu-id="721da-110">Example 1: Get a specific DDoS protection plan</span></span>
```
D:\> Get-AzureRmDdosProtectionPlan -ResourceGroupName ResourceGroupName -Name DdosProtectionPlanName


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

<span data-ttu-id="721da-111">В этом случае необходимо указать оба атрибута: **ResourceGroupName** и **Name** , соответствующие группе ресурсов и имя плана защиты Distributed соответственно.</span><span class="sxs-lookup"><span data-stu-id="721da-111">In this case, we need to specify both **ResourceGroupName** and **Name** attributes, which correspond to the resource group and the name of the DDoS protection plan, respectively.</span></span>

### <span data-ttu-id="721da-112">Пример 2: получение всех планов защиты Distributed в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="721da-112">Example 2: Get all DDoS protection plans in a resource group</span></span>
```
D:\> Get-AzureRmDdosProtectionPlan -ResourceGroupName ResourceGroupName


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

<span data-ttu-id="721da-113">В этом сценарии мы указываем параметр **ResourceGroupName** только для получения списка планов защиты Distributed.</span><span class="sxs-lookup"><span data-stu-id="721da-113">In this scenario, we only specify the parameter **ResourceGroupName** to get a list of DDoS protection plans.</span></span>

### <span data-ttu-id="721da-114">Пример 2: получение всех планов защиты Distributed в подписке</span><span class="sxs-lookup"><span data-stu-id="721da-114">Example 2: Get all DDoS protection plans in a subscription</span></span>
```
D:\> Get-AzureRmDdosProtectionPlan


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

<span data-ttu-id="721da-115">Здесь мы не указываем никакие параметры, чтобы получить список всех планов защиты Distributed в подписке.</span><span class="sxs-lookup"><span data-stu-id="721da-115">Here, we do not specify any parameters to get a list of all DDoS protection plans in a subscription.</span></span>

## <span data-ttu-id="721da-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="721da-116">PARAMETERS</span></span>

### <span data-ttu-id="721da-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="721da-117">-DefaultProfile</span></span>
<span data-ttu-id="721da-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="721da-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="721da-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="721da-119">-Name</span></span>
<span data-ttu-id="721da-120">Указывает имя плана защиты Distributed.</span><span class="sxs-lookup"><span data-stu-id="721da-120">Specifies the name of the DDoS protection plan.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndGroup
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="721da-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="721da-121">-ResourceGroupName</span></span>
<span data-ttu-id="721da-122">Указывает имя группы ресурсов для плана защиты Distributed.</span><span class="sxs-lookup"><span data-stu-id="721da-122">Specifies the name of the DDoS protection plan resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="721da-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="721da-123">CommonParameters</span></span>
<span data-ttu-id="721da-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="721da-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="721da-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="721da-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="721da-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="721da-126">INPUTS</span></span>

### <span data-ttu-id="721da-127">System. String</span><span class="sxs-lookup"><span data-stu-id="721da-127">System.String</span></span>

## <span data-ttu-id="721da-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="721da-128">OUTPUTS</span></span>

### <span data-ttu-id="721da-129">Microsoft.Azure.Commands.Network.Models.PSDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="721da-129">Microsoft.Azure.Commands.Network.Models.PSDdosProtectionPlan</span></span>

## <span data-ttu-id="721da-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="721da-130">NOTES</span></span>

## <span data-ttu-id="721da-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="721da-131">RELATED LINKS</span></span>

[<span data-ttu-id="721da-132">New-AzureRmDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="721da-132">New-AzureRmDdosProtectionPlan</span></span>](./New-AzureRmDdosProtectionPlan.md)

[<span data-ttu-id="721da-133">Remove-AzureRmDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="721da-133">Remove-AzureRmDdosProtectionPlan</span></span>](./Remove-AzureRmDdosProtectionPlan.md)

[<span data-ttu-id="721da-134">New-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="721da-134">New-AzureRmVirtualNetwork</span></span>](./New-AzureRmVirtualNetwork.md)

[<span data-ttu-id="721da-135">Set-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="721da-135">Set-AzureRmVirtualNetwork</span></span>](./Set-AzureRmVirtualNetwork.md)

[<span data-ttu-id="721da-136">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="721da-136">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)
