---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: F6A89D39-18AD-4087-823C-63FA0A3690E7
online version: ''
schema: 2.0.0
ms.openlocfilehash: 36c51d0ceae42aab50e2df9e0532c98dd6800747
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076520"
---
# <span data-ttu-id="1ee53-101">Get-AzureVirtualNetworkGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="1ee53-101">Get-AzureVirtualNetworkGatewayDiagnostics</span></span>

## <span data-ttu-id="1ee53-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1ee53-102">SYNOPSIS</span></span>
<span data-ttu-id="1ee53-103">Получает результаты диагностики шлюза виртуальной сети Azure.</span><span class="sxs-lookup"><span data-stu-id="1ee53-103">Gets the results of Azure virtual network gateway diagnostics.</span></span>

## <span data-ttu-id="1ee53-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1ee53-104">SYNTAX</span></span>

```
Get-AzureVirtualNetworkGatewayDiagnostics -GatewayId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="1ee53-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1ee53-105">DESCRIPTION</span></span>
<span data-ttu-id="1ee53-106">Командлет **Get-AzureVirtualNetworkGatewayDiagnostics** получает результаты диагностики шлюза виртуальной сети Azure.</span><span class="sxs-lookup"><span data-stu-id="1ee53-106">The **Get-AzureVirtualNetworkGatewayDiagnostics** cmdlet gets the results of Azure virtual network gateway diagnostics.</span></span>

## <span data-ttu-id="1ee53-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1ee53-107">EXAMPLES</span></span>

## <span data-ttu-id="1ee53-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1ee53-108">PARAMETERS</span></span>

### <span data-ttu-id="1ee53-109">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="1ee53-109">-GatewayId</span></span>
<span data-ttu-id="1ee53-110">Указывает идентификатор шлюза.</span><span class="sxs-lookup"><span data-stu-id="1ee53-110">Specifies the ID of a gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ee53-111">-Profile</span><span class="sxs-lookup"><span data-stu-id="1ee53-111">-Profile</span></span>
<span data-ttu-id="1ee53-112">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="1ee53-112">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="1ee53-113">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1ee53-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ee53-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ee53-114">CommonParameters</span></span>
<span data-ttu-id="1ee53-115">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1ee53-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ee53-116">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ee53-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ee53-117">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1ee53-117">INPUTS</span></span>

## <span data-ttu-id="1ee53-118">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1ee53-118">OUTPUTS</span></span>

## <span data-ttu-id="1ee53-119">Пуск</span><span class="sxs-lookup"><span data-stu-id="1ee53-119">NOTES</span></span>

## <span data-ttu-id="1ee53-120">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1ee53-120">RELATED LINKS</span></span>

[<span data-ttu-id="1ee53-121">Start-AzureVirtualNetworkGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="1ee53-121">Start-AzureVirtualNetworkGatewayDiagnostics</span></span>](./Start-AzureVirtualNetworkGatewayDiagnostics.md)

[<span data-ttu-id="1ee53-122">Остановить-AzureVirtualNetworkGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="1ee53-122">Stop-AzureVirtualNetworkGatewayDiagnostics</span></span>](./Stop-AzureVirtualNetworkGatewayDiagnostics.md)


