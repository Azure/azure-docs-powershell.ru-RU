---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: ECC5C079-C9A0-4159-A039-EE216897D686
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: c2a1a63abb18f5f47ed155f24e8ac73a7bae83ec
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732925"
---
# <span data-ttu-id="5b33e-101">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="5b33e-101">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="5b33e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5b33e-102">SYNOPSIS</span></span>
<span data-ttu-id="5b33e-103">Используется для отображения общего ключа, используемого для подключения.</span><span class="sxs-lookup"><span data-stu-id="5b33e-103">Displays the shared key used for the connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5b33e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5b33e-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkGatewayConnectionSharedKey [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5b33e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5b33e-105">DESCRIPTION</span></span>
<span data-ttu-id="5b33e-106">Используется для отображения общего ключа, используемого для подключения.</span><span class="sxs-lookup"><span data-stu-id="5b33e-106">Displays the shared key used for the connection.</span></span>

## <span data-ttu-id="5b33e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5b33e-107">EXAMPLES</span></span>

### <span data-ttu-id="5b33e-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5b33e-108">Example 1</span></span>
```
Get-AzureRmVirtualNetworkGatewayConnectionSharedKey -Name 1 -ResourceGroupName P2SVPNGateway
xxxxxx
```

## <span data-ttu-id="5b33e-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5b33e-109">PARAMETERS</span></span>

### <span data-ttu-id="5b33e-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b33e-110">-DefaultProfile</span></span>
<span data-ttu-id="5b33e-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5b33e-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5b33e-112">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5b33e-112">-Name</span></span>
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

### <span data-ttu-id="5b33e-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b33e-113">-ResourceGroupName</span></span>
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

### <span data-ttu-id="5b33e-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b33e-114">CommonParameters</span></span>
<span data-ttu-id="5b33e-115">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5b33e-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b33e-116">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b33e-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b33e-117">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5b33e-117">INPUTS</span></span>

### <span data-ttu-id="5b33e-118">System. String</span><span class="sxs-lookup"><span data-stu-id="5b33e-118">System.String</span></span>

## <span data-ttu-id="5b33e-119">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5b33e-119">OUTPUTS</span></span>

### <span data-ttu-id="5b33e-120">System. String</span><span class="sxs-lookup"><span data-stu-id="5b33e-120">System.String</span></span>

## <span data-ttu-id="5b33e-121">Пуск</span><span class="sxs-lookup"><span data-stu-id="5b33e-121">NOTES</span></span>

## <span data-ttu-id="5b33e-122">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5b33e-122">RELATED LINKS</span></span>
