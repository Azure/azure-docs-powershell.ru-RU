---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: E43C8D2A-A6B5-4259-94B9-353FBC15F5A8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 612e6b0cb5438dbb37a2e9d1c77da151c852fac1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563455"
---
# <span data-ttu-id="15168-101">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="15168-101">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="15168-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="15168-102">SYNOPSIS</span></span>
<span data-ttu-id="15168-103">Удаление сопоставлений URL-путей с пулом серверов внутренней базы данных.</span><span class="sxs-lookup"><span data-stu-id="15168-103">Removes URL path mappings to a backend server pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="15168-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="15168-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayUrlPathMapConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="15168-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="15168-105">DESCRIPTION</span></span>
<span data-ttu-id="15168-106">Командлет **Remove-AzureRmApplicationGatewayUrlPathMapConfig** Удаляет сопоставления URL-путей с пулом серверов внутренней базы данных.</span><span class="sxs-lookup"><span data-stu-id="15168-106">The **Remove-AzureRmApplicationGatewayUrlPathMapConfig** cmdlet removes URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="15168-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="15168-107">EXAMPLES</span></span>

## <span data-ttu-id="15168-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="15168-108">PARAMETERS</span></span>

### <span data-ttu-id="15168-109">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="15168-109">-ApplicationGateway</span></span>
<span data-ttu-id="15168-110">Указывает шлюз приложений, для которого этот командлет удаляет конфигурацию карты URL-пути.</span><span class="sxs-lookup"><span data-stu-id="15168-110">Specifies the application gateway to which this cmdlet removes URL path map configuration.</span></span>

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

### <span data-ttu-id="15168-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15168-111">-DefaultProfile</span></span>
<span data-ttu-id="15168-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="15168-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="15168-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="15168-113">-Name</span></span>
<span data-ttu-id="15168-114">Указывает имя карты URL-пути, которое удаляется этим командлетом из внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="15168-114">Specifies the URL path map name that this cmdlet removes from the backend server.</span></span>

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

### <span data-ttu-id="15168-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15168-115">CommonParameters</span></span>
<span data-ttu-id="15168-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="15168-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15168-117">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15168-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15168-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="15168-118">INPUTS</span></span>

### <span data-ttu-id="15168-119">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="15168-119">PSApplicationGateway</span></span>
<span data-ttu-id="15168-120">Параметр "ApplicationGateway" принимает значение типа "PSApplicationGateway" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="15168-120">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="15168-121">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="15168-121">OUTPUTS</span></span>

### <span data-ttu-id="15168-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="15168-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="15168-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="15168-123">NOTES</span></span>

## <span data-ttu-id="15168-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="15168-124">RELATED LINKS</span></span>

[<span data-ttu-id="15168-125">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="15168-125">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="15168-126">Get-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="15168-126">Get-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="15168-127">New-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="15168-127">New-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./New-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="15168-128">Set-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="15168-128">Set-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzureRmApplicationGatewayUrlPathMapConfig.md)


