---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewaybackendhttpsettings
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayBackendHttpSettings.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayBackendHttpSettings.md
ms.openlocfilehash: d7dc38e25ffda43eae3c29bc0e3db83f1a27c9f8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562968"
---
# <span data-ttu-id="d3dcb-101">Get-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="d3dcb-101">Get-AzureRmApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="d3dcb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d3dcb-102">SYNOPSIS</span></span>
<span data-ttu-id="d3dcb-103">Получает серверные параметры HTTP для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="d3dcb-103">Gets the back-end HTTP settings of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d3dcb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d3dcb-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayBackendHttpSettings [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d3dcb-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d3dcb-105">DESCRIPTION</span></span>
<span data-ttu-id="d3dcb-106">Командлет Get-AzureRmApplicationGatewayBackendHttpSettings получает серверные параметры HTTP для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="d3dcb-106">The Get-AzureRmApplicationGatewayBackendHttpSettings cmdlet gets the back-end HTTP settings of an application gateway.</span></span>

## <span data-ttu-id="d3dcb-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d3dcb-107">EXAMPLES</span></span>

### <span data-ttu-id="d3dcb-108">Пример 1: получение HTTP-параметров "на сервер" по имени</span><span class="sxs-lookup"><span data-stu-id="d3dcb-108">Example 1: Get back-end HTTP settings by name</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzureRmApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
```

<span data-ttu-id="d3dcb-109">Первая команда получает шлюз приложения с именем ApplicationGateway01 в группе ресурсов с именем ResourceGroup01 и сохраняет ее в переменной $AppGw. Вторая команда получает параметры HTTP с именем Settings01 для $AppGw и сохраняет параметры в переменной $Settings.</span><span class="sxs-lookup"><span data-stu-id="d3dcb-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>

### <span data-ttu-id="d3dcb-110">Пример 2: получение коллекции параметров HTTP для веб-части</span><span class="sxs-lookup"><span data-stu-id="d3dcb-110">Example 2: Get a collection of back-end HTTP settings</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $SettingsList  = Get-AzureRmApplicationGatewayBackendHttpSettings -ApplicationGateway $AppGw
```

<span data-ttu-id="d3dcb-111">Первая команда получает шлюз приложения с именем ApplicationGateway01 в группе ресурсов с именем ResourceGroup01 и сохраняет ее в переменной $AppGw. Вторая команда получает коллекцию параметров HTTP для $AppGw и сохраняет параметры в переменной $SettingsList.</span><span class="sxs-lookup"><span data-stu-id="d3dcb-111">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the collection of HTTP settings for $AppGw and stores the settings in the $SettingsList variable.</span></span>

## <span data-ttu-id="d3dcb-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d3dcb-112">PARAMETERS</span></span>

### <span data-ttu-id="d3dcb-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d3dcb-113">-ApplicationGateway</span></span>
<span data-ttu-id="d3dcb-114">Указывает объект шлюза приложения, который содержит параметры HTTP для внутренней стороны.</span><span class="sxs-lookup"><span data-stu-id="d3dcb-114">Specifies an application gateway object that contains back-end HTTP settings.</span></span>

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

### <span data-ttu-id="d3dcb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3dcb-115">-DefaultProfile</span></span>
<span data-ttu-id="d3dcb-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d3dcb-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d3dcb-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d3dcb-117">-Name</span></span>
<span data-ttu-id="d3dcb-118">Указывает имя HTTP-параметров серверной части, которые получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="d3dcb-118">Specifies the name of the backend HTTP settings that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3dcb-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3dcb-119">CommonParameters</span></span>
<span data-ttu-id="d3dcb-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d3dcb-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3dcb-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3dcb-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3dcb-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d3dcb-122">INPUTS</span></span>

### <span data-ttu-id="d3dcb-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d3dcb-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="d3dcb-124">Параметры: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d3dcb-124">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="d3dcb-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d3dcb-125">OUTPUTS</span></span>

### <span data-ttu-id="d3dcb-126">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="d3dcb-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="d3dcb-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="d3dcb-127">NOTES</span></span>

## <span data-ttu-id="d3dcb-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d3dcb-128">RELATED LINKS</span></span>

[<span data-ttu-id="d3dcb-129">Add-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="d3dcb-129">Add-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="d3dcb-130">New-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="d3dcb-130">New-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="d3dcb-131">Remove-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="d3dcb-131">Remove-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="d3dcb-132">Set-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="d3dcb-132">Set-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

