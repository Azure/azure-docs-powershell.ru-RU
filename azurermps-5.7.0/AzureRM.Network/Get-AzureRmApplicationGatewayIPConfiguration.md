---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 35562212-283C-4BB2-8B12-C3617A6760D0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 3ebe90d5f28adf0e7e4a9de66b04a1ea000cc69e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564796"
---
# <span data-ttu-id="99b22-101">Get-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="99b22-101">Get-AzureRmApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="99b22-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="99b22-102">SYNOPSIS</span></span>
<span data-ttu-id="99b22-103">Возвращает конфигурацию IP для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="99b22-103">Gets the IP configuration of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="99b22-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="99b22-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayIPConfiguration [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="99b22-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="99b22-105">DESCRIPTION</span></span>
<span data-ttu-id="99b22-106">Командлет **Get-AzureRmApplicationGatewayIPConfiguration** получает IP-конфигурацию шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="99b22-106">The **Get-AzureRmApplicationGatewayIPConfiguration** cmdlet gets the IP configuration of an application gateway.</span></span>
<span data-ttu-id="99b22-107">Конфигурация IP содержит подсеть, в которой развернут шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="99b22-107">The IP configuration contains the subnet in which the application gateway is deployed.</span></span>

## <span data-ttu-id="99b22-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="99b22-108">EXAMPLES</span></span>

### <span data-ttu-id="99b22-109">Пример 1: получение определенной конфигурации IP</span><span class="sxs-lookup"><span data-stu-id="99b22-109">Example 1: Get a specific IP configuration</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $GatewaySubnet = Get-AzureRmApplicationGatewayIPConfiguration -Name "GatewaySubnet01" -ApplicationGateway $AppGw
```

<span data-ttu-id="99b22-110">Первая команда получает шлюз приложения и сохраняет его в переменной $AppGw. Вторая команда получает IP-конфигурацию с именем GateSubnet01 из шлюза, хранящегося в $AppGw.</span><span class="sxs-lookup"><span data-stu-id="99b22-110">The first command gets an application gateway and stores it in the $AppGw variable.The second command gets an IP configuration named GateSubnet01 from the gateway stored in $AppGw.</span></span>

### <span data-ttu-id="99b22-111">Пример 2: получение списка конфигураций IP</span><span class="sxs-lookup"><span data-stu-id="99b22-111">Example 2: Get a list of IP configurations</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $GatewaySubnets = Get-AzureRmApplicationGatewayIPConfiguration -ApplicationGateway $AppGw
```

<span data-ttu-id="99b22-112">Первая команда получает шлюз приложения и сохраняет его в переменной $AppGw. Вторая команда возвращает список всех конфигураций IP.</span><span class="sxs-lookup"><span data-stu-id="99b22-112">The first command gets an application gateway and stores it in the $AppGw variable.The second command gets a list of all IP configurations.</span></span>

## <span data-ttu-id="99b22-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="99b22-113">PARAMETERS</span></span>

### <span data-ttu-id="99b22-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="99b22-114">-ApplicationGateway</span></span>
<span data-ttu-id="99b22-115">Указывает объект шлюза приложения, который содержит IP-конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="99b22-115">Specifies the application gateway object that contains IP configuration.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="99b22-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99b22-116">-DefaultProfile</span></span>
<span data-ttu-id="99b22-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="99b22-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="99b22-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="99b22-118">-Name</span></span>
<span data-ttu-id="99b22-119">Указывает имя конфигурации IP, которую этот командлет получает.</span><span class="sxs-lookup"><span data-stu-id="99b22-119">Specifies the name of the IP configuration which this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99b22-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99b22-120">CommonParameters</span></span>
<span data-ttu-id="99b22-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="99b22-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99b22-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99b22-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99b22-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="99b22-123">INPUTS</span></span>

### <span data-ttu-id="99b22-124">System. String</span><span class="sxs-lookup"><span data-stu-id="99b22-124">System.String</span></span>

## <span data-ttu-id="99b22-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="99b22-125">OUTPUTS</span></span>

### <span data-ttu-id="99b22-126">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="99b22-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="99b22-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="99b22-127">NOTES</span></span>

## <span data-ttu-id="99b22-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="99b22-128">RELATED LINKS</span></span>

[<span data-ttu-id="99b22-129">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="99b22-129">Add-AzureRmApplicationGatewayIPConfiguration</span></span>](./Add-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="99b22-130">New-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="99b22-130">New-AzureRmApplicationGatewayIPConfiguration</span></span>](./New-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="99b22-131">Remove-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="99b22-131">Remove-AzureRmApplicationGatewayIPConfiguration</span></span>](./Remove-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="99b22-132">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="99b22-132">Set-AzureRmApplicationGatewayIPConfiguration</span></span>](./Set-AzureRmApplicationGatewayIPConfiguration.md)


