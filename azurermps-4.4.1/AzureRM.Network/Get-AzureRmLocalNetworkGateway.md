---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F8756DA1-7BB9-4CD5-9D81-E11FF7A26125
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLocalNetworkGateway.md
ms.openlocfilehash: c881232c065f8494b962a0e010865cbefe8bc0eb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566688"
---
# <span data-ttu-id="e13f6-101">Get-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e13f6-101">Get-AzureRmLocalNetworkGateway</span></span>

## <span data-ttu-id="e13f6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e13f6-102">SYNOPSIS</span></span>
<span data-ttu-id="e13f6-103">Получение шлюза локальной сети</span><span class="sxs-lookup"><span data-stu-id="e13f6-103">Gets a Local Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e13f6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e13f6-104">SYNTAX</span></span>

```
Get-AzureRmLocalNetworkGateway [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e13f6-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e13f6-105">DESCRIPTION</span></span>
<span data-ttu-id="e13f6-106">Шлюз локальной сети — это объект, представляющий локальное устройство VPN.</span><span class="sxs-lookup"><span data-stu-id="e13f6-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>

<span data-ttu-id="e13f6-107">Командлет **Get-AzureRmLocalNetworkGateway** возвращает объект, представляющий локальный шлюз на основе имени и имени группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e13f6-107">The **Get-AzureRmLocalNetworkGateway** cmdlet returns the object representing your on-prem gateway based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="e13f6-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e13f6-108">EXAMPLES</span></span>

### <span data-ttu-id="e13f6-109">1: получение шлюза локальной сети</span><span class="sxs-lookup"><span data-stu-id="e13f6-109">1: Get a Local Network Gateway</span></span>
```
Get-AzureRmLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG
```

<span data-ttu-id="e13f6-110">Возвращает объект шлюза локальной сети с именем "myLocalGW" в группе ресурсов "myRG".</span><span class="sxs-lookup"><span data-stu-id="e13f6-110">Returns the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG"</span></span>

## <span data-ttu-id="e13f6-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e13f6-111">PARAMETERS</span></span>

### <span data-ttu-id="e13f6-112">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e13f6-112">-Name</span></span>
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

### <span data-ttu-id="e13f6-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e13f6-113">-ResourceGroupName</span></span>
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

### <span data-ttu-id="e13f6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e13f6-114">-DefaultProfile</span></span>
<span data-ttu-id="e13f6-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e13f6-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e13f6-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e13f6-116">CommonParameters</span></span>
<span data-ttu-id="e13f6-117">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e13f6-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e13f6-118">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e13f6-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e13f6-119">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e13f6-119">INPUTS</span></span>

## <span data-ttu-id="e13f6-120">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e13f6-120">OUTPUTS</span></span>

### <span data-ttu-id="e13f6-121">Microsoft. Azure. Commands. Network. Models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e13f6-121">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="e13f6-122">Пуск</span><span class="sxs-lookup"><span data-stu-id="e13f6-122">NOTES</span></span>

## <span data-ttu-id="e13f6-123">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e13f6-123">RELATED LINKS</span></span>

