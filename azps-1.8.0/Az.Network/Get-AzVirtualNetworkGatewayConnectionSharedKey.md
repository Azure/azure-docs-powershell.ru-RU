---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: ECC5C079-C9A0-4159-A039-EE216897D686
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: 071843c47ea3a8f97125746aa80fdb90eb1cb566
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93730476"
---
# <span data-ttu-id="3e187-101">Get-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="3e187-101">Get-AzVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="3e187-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3e187-102">SYNOPSIS</span></span>
<span data-ttu-id="3e187-103">Используется для отображения общего ключа, используемого для подключения.</span><span class="sxs-lookup"><span data-stu-id="3e187-103">Displays the shared key used for the connection.</span></span>

## <span data-ttu-id="3e187-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3e187-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayConnectionSharedKey [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3e187-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3e187-105">DESCRIPTION</span></span>
<span data-ttu-id="3e187-106">Используется для отображения общего ключа, используемого для подключения.</span><span class="sxs-lookup"><span data-stu-id="3e187-106">Displays the shared key used for the connection.</span></span>

## <span data-ttu-id="3e187-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3e187-107">EXAMPLES</span></span>

### <span data-ttu-id="3e187-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3e187-108">Example 1</span></span>
```
Get-AzVirtualNetworkGatewayConnectionSharedKey -Name 1 -ResourceGroupName P2SVPNGateway
xxxxxx
```

## <span data-ttu-id="3e187-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3e187-109">PARAMETERS</span></span>

### <span data-ttu-id="3e187-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e187-110">-DefaultProfile</span></span>
<span data-ttu-id="3e187-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3e187-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3e187-112">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3e187-112">-Name</span></span>
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

### <span data-ttu-id="3e187-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e187-113">-ResourceGroupName</span></span>
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

### <span data-ttu-id="3e187-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e187-114">CommonParameters</span></span>
<span data-ttu-id="3e187-115">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3e187-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e187-116">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3e187-116">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e187-117">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3e187-117">INPUTS</span></span>

### <span data-ttu-id="3e187-118">System. String</span><span class="sxs-lookup"><span data-stu-id="3e187-118">System.String</span></span>

## <span data-ttu-id="3e187-119">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3e187-119">OUTPUTS</span></span>

### <span data-ttu-id="3e187-120">System. String</span><span class="sxs-lookup"><span data-stu-id="3e187-120">System.String</span></span>

## <span data-ttu-id="3e187-121">Пуск</span><span class="sxs-lookup"><span data-stu-id="3e187-121">NOTES</span></span>

## <span data-ttu-id="3e187-122">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3e187-122">RELATED LINKS</span></span>

[<span data-ttu-id="3e187-123">Сброс — AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="3e187-123">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Reset-AzVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="3e187-124">Set-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="3e187-124">Set-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Set-AzVirtualNetworkGatewayConnectionSharedKey.md)
