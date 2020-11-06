---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F8756DA1-7BB9-4CD5-9D81-E11FF7A26125
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLocalNetworkGateway.md
ms.openlocfilehash: ca23e58b173ee67917099f2743dac7dbd3d1bc4c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569935"
---
# <span data-ttu-id="ac642-101">Get-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ac642-101">Get-AzureRmLocalNetworkGateway</span></span>

## <span data-ttu-id="ac642-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ac642-102">SYNOPSIS</span></span>
<span data-ttu-id="ac642-103">Получение шлюза локальной сети</span><span class="sxs-lookup"><span data-stu-id="ac642-103">Gets a Local Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ac642-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ac642-104">SYNTAX</span></span>

```
Get-AzureRmLocalNetworkGateway [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ac642-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ac642-105">DESCRIPTION</span></span>
<span data-ttu-id="ac642-106">Шлюз локальной сети — это объект, представляющий локальное устройство VPN.</span><span class="sxs-lookup"><span data-stu-id="ac642-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>

<span data-ttu-id="ac642-107">Командлет **Get-AzureRmLocalNetworkGateway** возвращает объект, представляющий локальный шлюз на основе имени и имени группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ac642-107">The **Get-AzureRmLocalNetworkGateway** cmdlet returns the object representing your on-prem gateway based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="ac642-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ac642-108">EXAMPLES</span></span>

### <span data-ttu-id="ac642-109">1: получение шлюза локальной сети</span><span class="sxs-lookup"><span data-stu-id="ac642-109">1: Get a Local Network Gateway</span></span>
```
Get-AzureRmLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG
```

<span data-ttu-id="ac642-110">Возвращает объект шлюза локальной сети с именем "myLocalGW" в группе ресурсов "myRG".</span><span class="sxs-lookup"><span data-stu-id="ac642-110">Returns the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG"</span></span>

## <span data-ttu-id="ac642-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ac642-111">PARAMETERS</span></span>

### <span data-ttu-id="ac642-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac642-112">-DefaultProfile</span></span>
<span data-ttu-id="ac642-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ac642-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ac642-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ac642-114">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac642-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac642-115">-ResourceGroupName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac642-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac642-116">CommonParameters</span></span>
<span data-ttu-id="ac642-117">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ac642-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac642-118">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac642-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac642-119">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ac642-119">INPUTS</span></span>

### <span data-ttu-id="ac642-120">Ничего</span><span class="sxs-lookup"><span data-stu-id="ac642-120">None</span></span>
<span data-ttu-id="ac642-121">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="ac642-121">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ac642-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ac642-122">OUTPUTS</span></span>

### <span data-ttu-id="ac642-123">Microsoft. Azure. Commands. Network. Models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ac642-123">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="ac642-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="ac642-124">NOTES</span></span>

## <span data-ttu-id="ac642-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ac642-125">RELATED LINKS</span></span>

