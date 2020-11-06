---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 7C8B47B4-2F6A-45EF-A351-88C8C3F9D0D3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGateway.md
ms.openlocfilehash: f755c08b880a9ec97315931843d6dca6f5fc3229
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93570348"
---
# <span data-ttu-id="14284-101">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="14284-101">Set-AzureRmApplicationGateway</span></span>

## <span data-ttu-id="14284-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="14284-102">SYNOPSIS</span></span>
<span data-ttu-id="14284-103">Обновляет шлюз приложения.</span><span class="sxs-lookup"><span data-stu-id="14284-103">Updates an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="14284-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="14284-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGateway -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="14284-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="14284-105">DESCRIPTION</span></span>
<span data-ttu-id="14284-106">Командлет **Set-AzureRmApplicationGateway** обновляет шлюз приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="14284-106">The **Set-AzureRmApplicationGateway** cmdlet updates an Azure application gateway.</span></span>

## <span data-ttu-id="14284-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="14284-107">EXAMPLES</span></span>

### <span data-ttu-id="14284-108">Пример 1: обновление шлюза приложения</span><span class="sxs-lookup"><span data-stu-id="14284-108">Example 1: Update an application gateway</span></span>
```
PS C:\>$UpdatedAppGw = Set-AzureRmApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="14284-109">Эта команда обновляет шлюз приложения параметрами $AppGw переменной и сохраняет обновленный шлюз в переменной $UpdatedAppGw.</span><span class="sxs-lookup"><span data-stu-id="14284-109">This command updates the application gateway with settings in the $AppGw variable and stores the updated gateway in the $UpdatedAppGw variable.</span></span>

## <span data-ttu-id="14284-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="14284-110">PARAMETERS</span></span>

### <span data-ttu-id="14284-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="14284-111">-ApplicationGateway</span></span>
<span data-ttu-id="14284-112">Указывает объект Application Gateway, представляющий состояние, в котором должен быть установлен шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="14284-112">Specifies an application gateway object representing the state to which the application gateway should be set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="14284-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14284-113">-DefaultProfile</span></span>
<span data-ttu-id="14284-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="14284-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="14284-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14284-115">CommonParameters</span></span>
<span data-ttu-id="14284-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="14284-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14284-117">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14284-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14284-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="14284-118">INPUTS</span></span>

### <span data-ttu-id="14284-119">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="14284-119">PSApplicationGateway</span></span>
<span data-ttu-id="14284-120">Параметр "ApplicationGateway" принимает значение типа "PSApplicationGateway" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="14284-120">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="14284-121">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="14284-121">OUTPUTS</span></span>

### <span data-ttu-id="14284-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="14284-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="14284-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="14284-123">NOTES</span></span>

## <span data-ttu-id="14284-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="14284-124">RELATED LINKS</span></span>

[<span data-ttu-id="14284-125">Start-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="14284-125">Start-AzureRmApplicationGateway</span></span>](./Start-AzureRmApplicationGateway.md)


