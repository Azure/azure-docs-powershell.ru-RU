---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaybackendhttpsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayBackendHttpSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayBackendHttpSetting.md
ms.openlocfilehash: 6c5729ec4d450ad122e359b9bd009000212e3b0a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93730230"
---
# <span data-ttu-id="6df47-101">Remove-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="6df47-101">Remove-AzApplicationGatewayBackendHttpSetting</span></span>

## <span data-ttu-id="6df47-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6df47-102">SYNOPSIS</span></span>
<span data-ttu-id="6df47-103">Удаляет из шлюза приложений параметры HTTP с внутренним интерфейсом.</span><span class="sxs-lookup"><span data-stu-id="6df47-103">Removes back-end HTTP settings from an application gateway.</span></span>

## <span data-ttu-id="6df47-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6df47-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayBackendHttpSetting -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6df47-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6df47-105">DESCRIPTION</span></span>
<span data-ttu-id="6df47-106">Командлет Remove-AzApplicationGatewayBackendHttpSetting удаляет параметры HTTP-протокола обратной передачи с шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="6df47-106">The Remove-AzApplicationGatewayBackendHttpSetting cmdlet removes back-end Hypertext Transfer Protocol (HTTP) settings from an Azure application gateway.</span></span>

## <span data-ttu-id="6df47-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6df47-107">EXAMPLES</span></span>

### <span data-ttu-id="6df47-108">Пример 1: Удаление HTTP-параметров для серверных интерфейсов из шлюза приложений</span><span class="sxs-lookup"><span data-stu-id="6df47-108">Example 1: Remove back-end HTTP settings from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayBackendHttpSetting -ApplicationGateway $AppGw -Name "BackEndSetting02"
```

<span data-ttu-id="6df47-109">Первая команда получает шлюз приложения с именем ApplicationGateway01, который принадлежит группе ресурсов с именем ResourceGroup01, и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="6df47-109">The first command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="6df47-110">Вторая команда удаляет серверный параметр HTTP с именем BackEndSetting02 из шлюза приложения, который хранится в $AppGw.</span><span class="sxs-lookup"><span data-stu-id="6df47-110">The second command removes the back-end HTTP setting named BackEndSetting02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="6df47-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6df47-111">PARAMETERS</span></span>

### <span data-ttu-id="6df47-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6df47-112">-ApplicationGateway</span></span>
<span data-ttu-id="6df47-113">Указывает шлюз приложений, с помощью которого этот командлет удаляет параметры HTTP для серверного элемента.</span><span class="sxs-lookup"><span data-stu-id="6df47-113">Specifies the application gateway from which this cmdlet removes back-end HTTP settings.</span></span>

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

### <span data-ttu-id="6df47-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6df47-114">-DefaultProfile</span></span>
<span data-ttu-id="6df47-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6df47-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6df47-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6df47-116">-Name</span></span>
<span data-ttu-id="6df47-117">Указывает имя серверных параметров HTTP, которые удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="6df47-117">Specifies the name of the back-end HTTP settings that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6df47-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6df47-118">CommonParameters</span></span>
<span data-ttu-id="6df47-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6df47-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6df47-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6df47-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6df47-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6df47-121">INPUTS</span></span>

### <span data-ttu-id="6df47-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6df47-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6df47-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6df47-123">OUTPUTS</span></span>

### <span data-ttu-id="6df47-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6df47-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6df47-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="6df47-125">NOTES</span></span>

## <span data-ttu-id="6df47-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6df47-126">RELATED LINKS</span></span>

[<span data-ttu-id="6df47-127">Add-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="6df47-127">Add-AzApplicationGatewayBackendHttpSetting</span></span>](./Add-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="6df47-128">New-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="6df47-128">New-AzApplicationGatewayBackendHttpSetting</span></span>](./New-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="6df47-129">Get-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="6df47-129">Get-AzApplicationGatewayBackendHttpSetting</span></span>](./Get-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="6df47-130">Set-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="6df47-130">Set-AzApplicationGatewayBackendHttpSetting</span></span>](./Set-AzApplicationGatewayBackendHttpSetting.md)

