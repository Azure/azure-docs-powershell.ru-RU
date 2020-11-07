---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: E43C8D2A-A6B5-4259-94B9-353FBC15F5A8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayurlpathmapconfig
schema: 2.0.0
ms.openlocfilehash: a0885534311dfef4498c9fc71be7f82d16b05277
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913595"
---
# <span data-ttu-id="1165c-101">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="1165c-101">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="1165c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1165c-102">SYNOPSIS</span></span>
<span data-ttu-id="1165c-103">Удаление сопоставлений URL-путей с пулом серверов внутренней базы данных.</span><span class="sxs-lookup"><span data-stu-id="1165c-103">Removes URL path mappings to a backend server pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1165c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1165c-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayUrlPathMapConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1165c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1165c-105">DESCRIPTION</span></span>
<span data-ttu-id="1165c-106">Командлет **Remove-AzureRmApplicationGatewayUrlPathMapConfig** Удаляет сопоставления URL-путей с пулом серверов внутренней базы данных.</span><span class="sxs-lookup"><span data-stu-id="1165c-106">The **Remove-AzureRmApplicationGatewayUrlPathMapConfig** cmdlet removes URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="1165c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1165c-107">EXAMPLES</span></span>

### <span data-ttu-id="1165c-108">1:</span><span class="sxs-lookup"><span data-stu-id="1165c-108">1:</span></span>
```

```

## <span data-ttu-id="1165c-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1165c-109">PARAMETERS</span></span>

### <span data-ttu-id="1165c-110">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1165c-110">-ApplicationGateway</span></span>
<span data-ttu-id="1165c-111">Указывает шлюз приложений, для которого этот командлет удаляет конфигурацию карты URL-пути.</span><span class="sxs-lookup"><span data-stu-id="1165c-111">Specifies the application gateway to which this cmdlet removes URL path map configuration.</span></span>

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

### <span data-ttu-id="1165c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1165c-112">-DefaultProfile</span></span>
<span data-ttu-id="1165c-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1165c-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1165c-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1165c-114">-Name</span></span>
<span data-ttu-id="1165c-115">Указывает имя карты URL-пути, которое удаляется этим командлетом из внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="1165c-115">Specifies the URL path map name that this cmdlet removes from the backend server.</span></span>

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

### <span data-ttu-id="1165c-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1165c-116">CommonParameters</span></span>
<span data-ttu-id="1165c-117">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1165c-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1165c-118">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1165c-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1165c-119">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1165c-119">INPUTS</span></span>

### <span data-ttu-id="1165c-120">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1165c-120">PSApplicationGateway</span></span>
<span data-ttu-id="1165c-121">Параметр "ApplicationGateway" принимает значение типа "PSApplicationGateway" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="1165c-121">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="1165c-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1165c-122">OUTPUTS</span></span>

### <span data-ttu-id="1165c-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1165c-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1165c-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="1165c-124">NOTES</span></span>

## <span data-ttu-id="1165c-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1165c-125">RELATED LINKS</span></span>

[<span data-ttu-id="1165c-126">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="1165c-126">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="1165c-127">Get-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="1165c-127">Get-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="1165c-128">New-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="1165c-128">New-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./New-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="1165c-129">Set-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="1165c-129">Set-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzureRmApplicationGatewayUrlPathMapConfig.md)


