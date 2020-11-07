---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 3C046A0A-A2B6-413C-8D3B-8991A1FC4926
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayfrontendport
schema: 2.0.0
ms.openlocfilehash: f8b9d6b981300c32badbe69ec153865c04814dd6
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914425"
---
# <span data-ttu-id="27da3-101">New-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="27da3-101">New-AzureRmApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="27da3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="27da3-102">SYNOPSIS</span></span>
<span data-ttu-id="27da3-103">Создает интерфейсный порт для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="27da3-103">Creates a front-end port for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="27da3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="27da3-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayFrontendPort -Name <String> -Port <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="27da3-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="27da3-105">DESCRIPTION</span></span>
<span data-ttu-id="27da3-106">Командлет **New-AzureRmApplicationGatewayFrontendPort** создает интерфейсный порт для шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="27da3-106">The **New-AzureRmApplicationGatewayFrontendPort** cmdlet creates a front-end port for an Azure application gateway.</span></span>

## <span data-ttu-id="27da3-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="27da3-107">EXAMPLES</span></span>

### <span data-ttu-id="27da3-108">Example1: создание внешнего порта</span><span class="sxs-lookup"><span data-stu-id="27da3-108">Example1: Create a front-end port</span></span>
```
PS C:\>$FrontEndPort = New-AzureRmApplicationGatewayFrontendPort -Name "FrontEndPort01" -Port 80
```

<span data-ttu-id="27da3-109">Эта команда создает интерфейсный порт с именем FrontEndPort01 на порту 80 и сохраняет результат в переменной с именем $FrontEndPort.</span><span class="sxs-lookup"><span data-stu-id="27da3-109">This command creates a front-end port named FrontEndPort01 on port 80 and stores the result in the variable named $FrontEndPort.</span></span>

## <span data-ttu-id="27da3-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="27da3-110">PARAMETERS</span></span>

### <span data-ttu-id="27da3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27da3-111">-DefaultProfile</span></span>
<span data-ttu-id="27da3-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="27da3-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="27da3-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="27da3-113">-Name</span></span>
<span data-ttu-id="27da3-114">Указывает имя порта переднего плана, созданного этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="27da3-114">Specifies the name of the front-end port that this cmdlet creates.</span></span>

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

### <span data-ttu-id="27da3-115">-Port (порт)</span><span class="sxs-lookup"><span data-stu-id="27da3-115">-Port</span></span>
<span data-ttu-id="27da3-116">Задает номер порта переднего порта.</span><span class="sxs-lookup"><span data-stu-id="27da3-116">Specifies the port number of the front-end port.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27da3-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27da3-117">CommonParameters</span></span>
<span data-ttu-id="27da3-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="27da3-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27da3-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27da3-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27da3-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="27da3-120">INPUTS</span></span>

### <span data-ttu-id="27da3-121">System. String</span><span class="sxs-lookup"><span data-stu-id="27da3-121">System.String</span></span>

## <span data-ttu-id="27da3-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="27da3-122">OUTPUTS</span></span>

### <span data-ttu-id="27da3-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="27da3-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="27da3-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="27da3-124">NOTES</span></span>

## <span data-ttu-id="27da3-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="27da3-125">RELATED LINKS</span></span>

[<span data-ttu-id="27da3-126">Add-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="27da3-126">Add-AzureRmApplicationGatewayFrontendPort</span></span>](./Add-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="27da3-127">Get-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="27da3-127">Get-AzureRmApplicationGatewayFrontendPort</span></span>](./Get-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="27da3-128">Remove-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="27da3-128">Remove-AzureRmApplicationGatewayFrontendPort</span></span>](./Remove-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="27da3-129">Set-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="27da3-129">Set-AzureRmApplicationGatewayFrontendPort</span></span>](./Set-AzureRmApplicationGatewayFrontendPort.md)


