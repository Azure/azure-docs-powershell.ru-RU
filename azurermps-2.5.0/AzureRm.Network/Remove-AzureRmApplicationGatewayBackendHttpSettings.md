---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewaybackendhttpsettings
schema: 2.0.0
ms.openlocfilehash: 71ce0dd8d4c5988dfc5cd4226ee76dcec46042ff
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913785"
---
# <span data-ttu-id="b9c22-101">Remove-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="b9c22-101">Remove-AzureRmApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="b9c22-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b9c22-102">SYNOPSIS</span></span>
<span data-ttu-id="b9c22-103">Удаляет из шлюза приложений параметры HTTP с внутренним интерфейсом.</span><span class="sxs-lookup"><span data-stu-id="b9c22-103">Removes back-end HTTP settings from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b9c22-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b9c22-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayBackendHttpSettings -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b9c22-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b9c22-105">DESCRIPTION</span></span>
<span data-ttu-id="b9c22-106">Командлет Remove-AzureRmApplicationGatewayBackendHttpSettings удаляет параметры HTTP-протокола обратной передачи с шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="b9c22-106">The Remove-AzureRmApplicationGatewayBackendHttpSettings cmdlet removes back-end Hypertext Transfer Protocol (HTTP) settings from an Azure application gateway.</span></span>

## <span data-ttu-id="b9c22-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b9c22-107">EXAMPLES</span></span>

### <span data-ttu-id="b9c22-108">Пример 1: Удаление HTTP-параметров для серверных интерфейсов из шлюза приложений</span><span class="sxs-lookup"><span data-stu-id="b9c22-108">Example 1: Remove back-end HTTP settings from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewayBackendHttpSettings -ApplicationGateway $AppGw -Name "BackEndSetting02"
```

<span data-ttu-id="b9c22-109">Первая команда получает шлюз приложения с именем ApplicationGateway01, который принадлежит группе ресурсов с именем ResourceGroup01, и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="b9c22-109">The first command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="b9c22-110">Вторая команда удаляет серверный параметр HTTP с именем BackEndSetting02 из шлюза приложения, который хранится в $AppGw.</span><span class="sxs-lookup"><span data-stu-id="b9c22-110">The second command removes the back-end HTTP setting named BackEndSetting02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="b9c22-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b9c22-111">PARAMETERS</span></span>

### <span data-ttu-id="b9c22-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b9c22-112">-ApplicationGateway</span></span>
<span data-ttu-id="b9c22-113">Указывает шлюз приложений, с помощью которого этот командлет удаляет параметры HTTP для серверного элемента.</span><span class="sxs-lookup"><span data-stu-id="b9c22-113">Specifies the application gateway from which this cmdlet removes back-end HTTP settings.</span></span>

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

### <span data-ttu-id="b9c22-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9c22-114">-DefaultProfile</span></span>
<span data-ttu-id="b9c22-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b9c22-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b9c22-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b9c22-116">-Name</span></span>
<span data-ttu-id="b9c22-117">Указывает имя серверных параметров HTTP, которые удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="b9c22-117">Specifies the name of the back-end HTTP settings that this cmdlet removes.</span></span>

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

### <span data-ttu-id="b9c22-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9c22-118">CommonParameters</span></span>
<span data-ttu-id="b9c22-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b9c22-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9c22-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9c22-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9c22-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b9c22-121">INPUTS</span></span>

### <span data-ttu-id="b9c22-122">System. String</span><span class="sxs-lookup"><span data-stu-id="b9c22-122">System.String</span></span>

## <span data-ttu-id="b9c22-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b9c22-123">OUTPUTS</span></span>

### <span data-ttu-id="b9c22-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b9c22-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b9c22-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="b9c22-125">NOTES</span></span>

## <span data-ttu-id="b9c22-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b9c22-126">RELATED LINKS</span></span>

[<span data-ttu-id="b9c22-127">Add-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="b9c22-127">Add-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="b9c22-128">New-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="b9c22-128">New-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="b9c22-129">Get-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="b9c22-129">Get-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="b9c22-130">Set-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="b9c22-130">Set-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

