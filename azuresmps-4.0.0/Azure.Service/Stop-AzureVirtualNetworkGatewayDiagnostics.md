---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 9E7A170D-512A-4117-85C3-3AA4D6341C6B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 97fe847fd183caa7de281b358da579e8df4d5831
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075740"
---
# <span data-ttu-id="0e4b0-101">Stop-AzureVirtualNetworkGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="0e4b0-101">Stop-AzureVirtualNetworkGatewayDiagnostics</span></span>

## <span data-ttu-id="0e4b0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0e4b0-102">SYNOPSIS</span></span>
<span data-ttu-id="0e4b0-103">Прекращение запущенного сеанса диагностики шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="0e4b0-103">Stops a running virtual network gateway diagnostics session.</span></span>

## <span data-ttu-id="0e4b0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0e4b0-104">SYNTAX</span></span>

```
Stop-AzureVirtualNetworkGatewayDiagnostics -GatewayId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="0e4b0-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0e4b0-105">DESCRIPTION</span></span>
<span data-ttu-id="0e4b0-106">Командлет **Stop-AzureVirtualNetworkGatewayDiagnostics** останавливает запущенный сеанс диагностики шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="0e4b0-106">The **Stop-AzureVirtualNetworkGatewayDiagnostics** cmdlet stops a running virtual network gateway diagnostics session.</span></span>
<span data-ttu-id="0e4b0-107">Эта команда сохраняет результаты сеанса диагностики в учетной записи хранения, которую указывает командлет Start-AzureVirtualNetworkGatewayDiagnostics.</span><span class="sxs-lookup"><span data-stu-id="0e4b0-107">This command saves the results of the diagnostics session to the storage account that the Start-AzureVirtualNetworkGatewayDiagnostics cmdlet specifies.</span></span>

## <span data-ttu-id="0e4b0-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0e4b0-108">EXAMPLES</span></span>

## <span data-ttu-id="0e4b0-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0e4b0-109">PARAMETERS</span></span>

### <span data-ttu-id="0e4b0-110">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="0e4b0-110">-GatewayId</span></span>
<span data-ttu-id="0e4b0-111">Указывает идентификатор шлюза.</span><span class="sxs-lookup"><span data-stu-id="0e4b0-111">Specifies the ID of a gateway.</span></span>

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

### <span data-ttu-id="0e4b0-112">-Profile</span><span class="sxs-lookup"><span data-stu-id="0e4b0-112">-Profile</span></span>
<span data-ttu-id="0e4b0-113">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="0e4b0-113">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="0e4b0-114">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0e4b0-114">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0e4b0-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e4b0-115">CommonParameters</span></span>
<span data-ttu-id="0e4b0-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0e4b0-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e4b0-117">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e4b0-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e4b0-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0e4b0-118">INPUTS</span></span>

## <span data-ttu-id="0e4b0-119">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0e4b0-119">OUTPUTS</span></span>

## <span data-ttu-id="0e4b0-120">Пуск</span><span class="sxs-lookup"><span data-stu-id="0e4b0-120">NOTES</span></span>

## <span data-ttu-id="0e4b0-121">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0e4b0-121">RELATED LINKS</span></span>

[<span data-ttu-id="0e4b0-122">Get-AzureVirtualNetworkGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="0e4b0-122">Get-AzureVirtualNetworkGatewayDiagnostics</span></span>](./Get-AzureVirtualNetworkGatewayDiagnostics.md)

[<span data-ttu-id="0e4b0-123">Start-AzureVirtualNetworkGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="0e4b0-123">Start-AzureVirtualNetworkGatewayDiagnostics</span></span>](./Start-AzureVirtualNetworkGatewayDiagnostics.md)


