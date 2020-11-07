---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F8756DA1-7BB9-4CD5-9D81-E11FF7A26125
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLocalNetworkGateway.md
ms.openlocfilehash: 522516df5d4500f55a17e769140149f021501210
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93735097"
---
# <span data-ttu-id="bff4f-101">Get-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="bff4f-101">Get-AzureRmLocalNetworkGateway</span></span>

## <span data-ttu-id="bff4f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bff4f-102">SYNOPSIS</span></span>
<span data-ttu-id="bff4f-103">Получение шлюза локальной сети</span><span class="sxs-lookup"><span data-stu-id="bff4f-103">Gets a Local Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bff4f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bff4f-104">SYNTAX</span></span>

```
Get-AzureRmLocalNetworkGateway [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bff4f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bff4f-105">DESCRIPTION</span></span>
<span data-ttu-id="bff4f-106">Шлюз локальной сети — это объект, представляющий локальное устройство VPN.</span><span class="sxs-lookup"><span data-stu-id="bff4f-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>
<span data-ttu-id="bff4f-107">Командлет **Get-AzureRmLocalNetworkGateway** возвращает объект, представляющий локальный шлюз на основе имени и имени группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bff4f-107">The **Get-AzureRmLocalNetworkGateway** cmdlet returns the object representing your on-prem gateway based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="bff4f-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bff4f-108">EXAMPLES</span></span>

### <span data-ttu-id="bff4f-109">1: получение шлюза локальной сети</span><span class="sxs-lookup"><span data-stu-id="bff4f-109">1: Get a Local Network Gateway</span></span>
```
Get-AzureRmLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG
```

<span data-ttu-id="bff4f-110">Возвращает объект шлюза локальной сети с именем "myLocalGW" в группе ресурсов "myRG".</span><span class="sxs-lookup"><span data-stu-id="bff4f-110">Returns the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG"</span></span>

## <span data-ttu-id="bff4f-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bff4f-111">PARAMETERS</span></span>

### <span data-ttu-id="bff4f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bff4f-112">-DefaultProfile</span></span>
<span data-ttu-id="bff4f-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bff4f-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bff4f-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="bff4f-114">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bff4f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bff4f-115">-ResourceGroupName</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bff4f-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bff4f-116">CommonParameters</span></span>
<span data-ttu-id="bff4f-117">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bff4f-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bff4f-118">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bff4f-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bff4f-119">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bff4f-119">INPUTS</span></span>

### <span data-ttu-id="bff4f-120">System. String</span><span class="sxs-lookup"><span data-stu-id="bff4f-120">System.String</span></span>

## <span data-ttu-id="bff4f-121">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bff4f-121">OUTPUTS</span></span>

### <span data-ttu-id="bff4f-122">Microsoft. Azure. Commands. Network. Models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="bff4f-122">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="bff4f-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="bff4f-123">NOTES</span></span>

## <span data-ttu-id="bff4f-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bff4f-124">RELATED LINKS</span></span>
