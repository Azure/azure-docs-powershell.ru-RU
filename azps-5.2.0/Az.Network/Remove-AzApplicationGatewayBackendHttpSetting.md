---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaybackendhttpsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayBackendHttpSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayBackendHttpSetting.md
ms.openlocfilehash: 9db92f11a7401eec1643156490079da8ff2b00d6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98326216"
---
# <span data-ttu-id="bee47-101">Remove-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="bee47-101">Remove-AzApplicationGatewayBackendHttpSetting</span></span>

## <span data-ttu-id="bee47-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bee47-102">SYNOPSIS</span></span>
<span data-ttu-id="bee47-103">Удаление конечных параметров HTTP из шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="bee47-103">Removes back-end HTTP settings from an application gateway.</span></span>

## <span data-ttu-id="bee47-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="bee47-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayBackendHttpSetting -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bee47-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bee47-105">DESCRIPTION</span></span>
<span data-ttu-id="bee47-106">Этот Remove-AzApplicationGatewayBackendHttpSetting удаляет из шлюза приложения Azure параметры протокола передачи гипертекста (HTTP).</span><span class="sxs-lookup"><span data-stu-id="bee47-106">The Remove-AzApplicationGatewayBackendHttpSetting cmdlet removes back-end Hypertext Transfer Protocol (HTTP) settings from an Azure application gateway.</span></span>

## <span data-ttu-id="bee47-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="bee47-107">EXAMPLES</span></span>

### <span data-ttu-id="bee47-108">Пример 1. Удаление back-end HTTP-параметров из шлюза приложения</span><span class="sxs-lookup"><span data-stu-id="bee47-108">Example 1: Remove back-end HTTP settings from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayBackendHttpSetting -ApplicationGateway $AppGw -Name "BackEndSetting02"
```

<span data-ttu-id="bee47-109">Первая команда получает шлюз приложения ApplicationGateway01, который принадлежит группе ресурсов ResourceGroup01, и сохраняет его в переменной $AppGw ресурса.</span><span class="sxs-lookup"><span data-stu-id="bee47-109">The first command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="bee47-110">Вторая команда удаляет end HTTP-параметр BackEndSetting02 из шлюза приложения, $AppGw.</span><span class="sxs-lookup"><span data-stu-id="bee47-110">The second command removes the back-end HTTP setting named BackEndSetting02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="bee47-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bee47-111">PARAMETERS</span></span>

### <span data-ttu-id="bee47-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bee47-112">-ApplicationGateway</span></span>
<span data-ttu-id="bee47-113">Указывает шлюз приложения, из которого этот cmdlet удаляет back-end HTTP-параметры.</span><span class="sxs-lookup"><span data-stu-id="bee47-113">Specifies the application gateway from which this cmdlet removes back-end HTTP settings.</span></span>

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

### <span data-ttu-id="bee47-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bee47-114">-DefaultProfile</span></span>
<span data-ttu-id="bee47-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bee47-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bee47-116">-Name</span><span class="sxs-lookup"><span data-stu-id="bee47-116">-Name</span></span>
<span data-ttu-id="bee47-117">Имя конечных параметров HTTP, которые удаляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bee47-117">Specifies the name of the back-end HTTP settings that this cmdlet removes.</span></span>

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

### <span data-ttu-id="bee47-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bee47-118">CommonParameters</span></span>
<span data-ttu-id="bee47-119">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bee47-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bee47-120">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bee47-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bee47-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bee47-121">INPUTS</span></span>

### <span data-ttu-id="bee47-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bee47-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="bee47-123">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="bee47-123">OUTPUTS</span></span>

### <span data-ttu-id="bee47-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bee47-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="bee47-125">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="bee47-125">NOTES</span></span>

## <span data-ttu-id="bee47-126">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bee47-126">RELATED LINKS</span></span>

[<span data-ttu-id="bee47-127">Add-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="bee47-127">Add-AzApplicationGatewayBackendHttpSetting</span></span>](./Add-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="bee47-128">New-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="bee47-128">New-AzApplicationGatewayBackendHttpSetting</span></span>](./New-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="bee47-129">Get-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="bee47-129">Get-AzApplicationGatewayBackendHttpSetting</span></span>](./Get-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="bee47-130">Set-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="bee47-130">Set-AzApplicationGatewayBackendHttpSetting</span></span>](./Set-AzApplicationGatewayBackendHttpSetting.md)

