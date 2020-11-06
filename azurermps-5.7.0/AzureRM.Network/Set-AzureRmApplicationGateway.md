---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 7C8B47B4-2F6A-45EF-A351-88C8C3F9D0D3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGateway.md
ms.openlocfilehash: ff836268c92b575db05e05b1843c57af2bc6dca7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568560"
---
# <span data-ttu-id="b9e2e-101">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b9e2e-101">Set-AzureRmApplicationGateway</span></span>

## <span data-ttu-id="b9e2e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b9e2e-102">SYNOPSIS</span></span>
<span data-ttu-id="b9e2e-103">Обновляет шлюз приложения.</span><span class="sxs-lookup"><span data-stu-id="b9e2e-103">Updates an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b9e2e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b9e2e-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGateway -ApplicationGateway <PSApplicationGateway> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b9e2e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b9e2e-105">DESCRIPTION</span></span>
<span data-ttu-id="b9e2e-106">Командлет **Set-AzureRmApplicationGateway** обновляет шлюз приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="b9e2e-106">The **Set-AzureRmApplicationGateway** cmdlet updates an Azure application gateway.</span></span>

## <span data-ttu-id="b9e2e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b9e2e-107">EXAMPLES</span></span>

### <span data-ttu-id="b9e2e-108">Пример 1: обновление шлюза приложения</span><span class="sxs-lookup"><span data-stu-id="b9e2e-108">Example 1: Update an application gateway</span></span>
```
PS C:\>$UpdatedAppGw = Set-AzureRmApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="b9e2e-109">Эта команда обновляет шлюз приложения параметрами $AppGw переменной и сохраняет обновленный шлюз в переменной $UpdatedAppGw.</span><span class="sxs-lookup"><span data-stu-id="b9e2e-109">This command updates the application gateway with settings in the $AppGw variable and stores the updated gateway in the $UpdatedAppGw variable.</span></span>

## <span data-ttu-id="b9e2e-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b9e2e-110">PARAMETERS</span></span>

### <span data-ttu-id="b9e2e-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b9e2e-111">-ApplicationGateway</span></span>
<span data-ttu-id="b9e2e-112">Указывает объект Application Gateway, представляющий состояние, в котором должен быть установлен шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="b9e2e-112">Specifies an application gateway object representing the state to which the application gateway should be set.</span></span>

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

### <span data-ttu-id="b9e2e-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b9e2e-113">-AsJob</span></span>
<span data-ttu-id="b9e2e-114">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="b9e2e-114">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9e2e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9e2e-115">-DefaultProfile</span></span>
<span data-ttu-id="b9e2e-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b9e2e-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b9e2e-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9e2e-117">CommonParameters</span></span>
<span data-ttu-id="b9e2e-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b9e2e-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9e2e-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9e2e-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9e2e-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b9e2e-120">INPUTS</span></span>

### <span data-ttu-id="b9e2e-121">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b9e2e-121">PSApplicationGateway</span></span>
<span data-ttu-id="b9e2e-122">Параметр "ApplicationGateway" принимает значение типа "PSApplicationGateway" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="b9e2e-122">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="b9e2e-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b9e2e-123">OUTPUTS</span></span>

### <span data-ttu-id="b9e2e-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b9e2e-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b9e2e-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="b9e2e-125">NOTES</span></span>

## <span data-ttu-id="b9e2e-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b9e2e-126">RELATED LINKS</span></span>

[<span data-ttu-id="b9e2e-127">Start-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b9e2e-127">Start-AzureRmApplicationGateway</span></span>](./Start-AzureRmApplicationGateway.md)


