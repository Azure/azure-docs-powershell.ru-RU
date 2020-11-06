---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewaybackendhttpsettings
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayBackendHttpSettings.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayBackendHttpSettings.md
ms.openlocfilehash: 036fef4e43d8d754bd0798e72159cba367a3e2f4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560867"
---
# <span data-ttu-id="3883e-101">Remove-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="3883e-101">Remove-AzureRmApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="3883e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3883e-102">SYNOPSIS</span></span>
<span data-ttu-id="3883e-103">Удаляет из шлюза приложений параметры HTTP с внутренним интерфейсом.</span><span class="sxs-lookup"><span data-stu-id="3883e-103">Removes back-end HTTP settings from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3883e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3883e-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayBackendHttpSettings -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3883e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3883e-105">DESCRIPTION</span></span>
<span data-ttu-id="3883e-106">Командлет Remove-AzureRmApplicationGatewayBackendHttpSettings удаляет параметры HTTP-протокола обратной передачи с шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="3883e-106">The Remove-AzureRmApplicationGatewayBackendHttpSettings cmdlet removes back-end Hypertext Transfer Protocol (HTTP) settings from an Azure application gateway.</span></span>

## <span data-ttu-id="3883e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3883e-107">EXAMPLES</span></span>

### <span data-ttu-id="3883e-108">Пример 1: Удаление HTTP-параметров для серверных интерфейсов из шлюза приложений</span><span class="sxs-lookup"><span data-stu-id="3883e-108">Example 1: Remove back-end HTTP settings from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewayBackendHttpSettings -ApplicationGateway $AppGw -Name "BackEndSetting02"
```

<span data-ttu-id="3883e-109">Первая команда получает шлюз приложения с именем ApplicationGateway01, который принадлежит группе ресурсов с именем ResourceGroup01, и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="3883e-109">The first command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="3883e-110">Вторая команда удаляет серверный параметр HTTP с именем BackEndSetting02 из шлюза приложения, который хранится в $AppGw.</span><span class="sxs-lookup"><span data-stu-id="3883e-110">The second command removes the back-end HTTP setting named BackEndSetting02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="3883e-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3883e-111">PARAMETERS</span></span>

### <span data-ttu-id="3883e-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3883e-112">-ApplicationGateway</span></span>
<span data-ttu-id="3883e-113">Указывает шлюз приложений, с помощью которого этот командлет удаляет параметры HTTP для серверного элемента.</span><span class="sxs-lookup"><span data-stu-id="3883e-113">Specifies the application gateway from which this cmdlet removes back-end HTTP settings.</span></span>

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

### <span data-ttu-id="3883e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3883e-114">-DefaultProfile</span></span>
<span data-ttu-id="3883e-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3883e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3883e-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3883e-116">-Name</span></span>
<span data-ttu-id="3883e-117">Указывает имя серверных параметров HTTP, которые удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="3883e-117">Specifies the name of the back-end HTTP settings that this cmdlet removes.</span></span>

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

### <span data-ttu-id="3883e-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3883e-118">CommonParameters</span></span>
<span data-ttu-id="3883e-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3883e-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3883e-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3883e-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3883e-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3883e-121">INPUTS</span></span>

### <span data-ttu-id="3883e-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3883e-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="3883e-123">Параметры: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="3883e-123">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="3883e-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3883e-124">OUTPUTS</span></span>

### <span data-ttu-id="3883e-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3883e-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="3883e-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="3883e-126">NOTES</span></span>

## <span data-ttu-id="3883e-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3883e-127">RELATED LINKS</span></span>

[<span data-ttu-id="3883e-128">Add-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="3883e-128">Add-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="3883e-129">New-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="3883e-129">New-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="3883e-130">Get-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="3883e-130">Get-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="3883e-131">Set-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="3883e-131">Set-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

