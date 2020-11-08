---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7C8B47B4-2F6A-45EF-A351-88C8C3F9D0D3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGateway.md
ms.openlocfilehash: c7d8e147d227ac630709d28dca069955cb9dc512
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244331"
---
# <span data-ttu-id="9dc02-101">Set-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9dc02-101">Set-AzApplicationGateway</span></span>

## <span data-ttu-id="9dc02-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9dc02-102">SYNOPSIS</span></span>
<span data-ttu-id="9dc02-103">Обновляет шлюз приложения.</span><span class="sxs-lookup"><span data-stu-id="9dc02-103">Updates an application gateway.</span></span>

## <span data-ttu-id="9dc02-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9dc02-104">SYNTAX</span></span>

```
Set-AzApplicationGateway -ApplicationGateway <PSApplicationGateway> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9dc02-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9dc02-105">DESCRIPTION</span></span>
<span data-ttu-id="9dc02-106">Командлет **Set-AzApplicationGateway** обновляет шлюз приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="9dc02-106">The **Set-AzApplicationGateway** cmdlet updates an Azure application gateway.</span></span>

## <span data-ttu-id="9dc02-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9dc02-107">EXAMPLES</span></span>

### <span data-ttu-id="9dc02-108">Пример 1: обновление шлюза приложения</span><span class="sxs-lookup"><span data-stu-id="9dc02-108">Example 1: Update an application gateway</span></span>
```
PS C:\>$UpdatedAppGw = Set-AzApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="9dc02-109">Эта команда обновляет шлюз приложения параметрами $AppGw переменной и сохраняет обновленный шлюз в переменной $UpdatedAppGw.</span><span class="sxs-lookup"><span data-stu-id="9dc02-109">This command updates the application gateway with settings in the $AppGw variable and stores the updated gateway in the $UpdatedAppGw variable.</span></span>

## <span data-ttu-id="9dc02-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9dc02-110">PARAMETERS</span></span>

### <span data-ttu-id="9dc02-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9dc02-111">-ApplicationGateway</span></span>
<span data-ttu-id="9dc02-112">Указывает объект Application Gateway, представляющий состояние, в котором должен быть установлен шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="9dc02-112">Specifies an application gateway object representing the state to which the application gateway should be set.</span></span>

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

### <span data-ttu-id="9dc02-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9dc02-113">-AsJob</span></span>
<span data-ttu-id="9dc02-114">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="9dc02-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9dc02-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9dc02-115">-DefaultProfile</span></span>
<span data-ttu-id="9dc02-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9dc02-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dc02-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9dc02-117">CommonParameters</span></span>
<span data-ttu-id="9dc02-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9dc02-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9dc02-119">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9dc02-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9dc02-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9dc02-120">INPUTS</span></span>

### <span data-ttu-id="9dc02-121">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9dc02-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9dc02-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9dc02-122">OUTPUTS</span></span>

### <span data-ttu-id="9dc02-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9dc02-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9dc02-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="9dc02-124">NOTES</span></span>

## <span data-ttu-id="9dc02-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9dc02-125">RELATED LINKS</span></span>

[<span data-ttu-id="9dc02-126">Start-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9dc02-126">Start-AzApplicationGateway</span></span>](./Start-AzApplicationGateway.md)


