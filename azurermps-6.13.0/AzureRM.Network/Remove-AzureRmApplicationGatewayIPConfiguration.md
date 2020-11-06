---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6943BB5C-D709-4A80-AF5E-DC9501C20680
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 884ff52132af34dad7c4498653233f0b122555ee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568474"
---
# <span data-ttu-id="47789-101">Remove-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="47789-101">Remove-AzureRmApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="47789-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="47789-102">SYNOPSIS</span></span>
<span data-ttu-id="47789-103">Удаление IP-конфигурации с шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="47789-103">Removes an IP configuration from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="47789-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="47789-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayIPConfiguration -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="47789-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="47789-105">DESCRIPTION</span></span>
<span data-ttu-id="47789-106">Командлет **Remove-AzureRmApplicationGatewayIPConfiguration** УДАЛЯЕТ конфигурацию IP из шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="47789-106">The **Remove-AzureRmApplicationGatewayIPConfiguration** cmdlet removes an IP configuration from an Azure application gateway.</span></span>

## <span data-ttu-id="47789-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="47789-107">EXAMPLES</span></span>

### <span data-ttu-id="47789-108">Пример 1: Удаление конфигурации IP из шлюза приложений Azure</span><span class="sxs-lookup"><span data-stu-id="47789-108">Example 1: Remove an IP configuration from an Azure application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "Subnet02"
```

<span data-ttu-id="47789-109">Первая команда получает шлюз приложения и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="47789-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="47789-110">Вторая команда удаляет IP-конфигурацию с именем Subnet02 из шлюза приложений, хранящегося в $AppGw.</span><span class="sxs-lookup"><span data-stu-id="47789-110">The second command removes the IP configuration named Subnet02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="47789-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="47789-111">PARAMETERS</span></span>

### <span data-ttu-id="47789-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="47789-112">-ApplicationGateway</span></span>
<span data-ttu-id="47789-113">Указывает шлюз приложений, из которого нужно удалить конфигурацию IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="47789-113">Specifies the application gateway from which to remove an IP configuration.</span></span>

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

### <span data-ttu-id="47789-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47789-114">-DefaultProfile</span></span>
<span data-ttu-id="47789-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="47789-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="47789-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="47789-116">-Name</span></span>
<span data-ttu-id="47789-117">Указывает имя удаляемой IP-конфигурации.</span><span class="sxs-lookup"><span data-stu-id="47789-117">Specifies the name of the IP configuration to remove.</span></span>

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

### <span data-ttu-id="47789-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47789-118">CommonParameters</span></span>
<span data-ttu-id="47789-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="47789-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47789-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47789-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47789-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="47789-121">INPUTS</span></span>

### <span data-ttu-id="47789-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="47789-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="47789-123">Параметры: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="47789-123">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="47789-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="47789-124">OUTPUTS</span></span>

### <span data-ttu-id="47789-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="47789-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="47789-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="47789-126">NOTES</span></span>

## <span data-ttu-id="47789-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="47789-127">RELATED LINKS</span></span>

[<span data-ttu-id="47789-128">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="47789-128">Add-AzureRmApplicationGatewayIPConfiguration</span></span>](./Add-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="47789-129">Get-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="47789-129">Get-AzureRmApplicationGatewayIPConfiguration</span></span>](./Get-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="47789-130">New-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="47789-130">New-AzureRmApplicationGatewayIPConfiguration</span></span>](./New-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="47789-131">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="47789-131">Set-AzureRmApplicationGatewayIPConfiguration</span></span>](./Set-AzureRmApplicationGatewayIPConfiguration.md)


