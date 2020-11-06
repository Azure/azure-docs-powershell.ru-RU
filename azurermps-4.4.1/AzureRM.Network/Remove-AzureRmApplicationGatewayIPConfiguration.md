---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6943BB5C-D709-4A80-AF5E-DC9501C20680
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 4ef644fb92bf3f872a9e80aef2674a3ffb56747b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565239"
---
# <span data-ttu-id="e7729-101">Remove-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="e7729-101">Remove-AzureRmApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="e7729-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e7729-102">SYNOPSIS</span></span>
<span data-ttu-id="e7729-103">Удаление IP-конфигурации с шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="e7729-103">Removes an IP configuration from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e7729-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e7729-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayIPConfiguration -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e7729-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e7729-105">DESCRIPTION</span></span>
<span data-ttu-id="e7729-106">Командлет **Remove-AzureRmApplicationGatewayIPConfiguration** УДАЛЯЕТ конфигурацию IP из шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="e7729-106">The **Remove-AzureRmApplicationGatewayIPConfiguration** cmdlet removes an IP configuration from an Azure application gateway.</span></span>

## <span data-ttu-id="e7729-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e7729-107">EXAMPLES</span></span>

### <span data-ttu-id="e7729-108">Пример 1: Удаление конфигурации IP из шлюза приложений Azure</span><span class="sxs-lookup"><span data-stu-id="e7729-108">Example 1: Remove an IP configuration from an Azure application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "Subnet02"
```

<span data-ttu-id="e7729-109">Первая команда получает шлюз приложения и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="e7729-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="e7729-110">Вторая команда удаляет IP-конфигурацию с именем Subnet02 из шлюза приложений, хранящегося в $AppGw.</span><span class="sxs-lookup"><span data-stu-id="e7729-110">The second command removes the IP configuration named Subnet02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="e7729-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e7729-111">PARAMETERS</span></span>

### <span data-ttu-id="e7729-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e7729-112">-ApplicationGateway</span></span>
<span data-ttu-id="e7729-113">Указывает шлюз приложений, из которого нужно удалить конфигурацию IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="e7729-113">Specifies the application gateway from which to remove an IP configuration.</span></span>

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

### <span data-ttu-id="e7729-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e7729-114">-Name</span></span>
<span data-ttu-id="e7729-115">Указывает имя удаляемой IP-конфигурации.</span><span class="sxs-lookup"><span data-stu-id="e7729-115">Specifies the name of the IP configuration to remove.</span></span>

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

### <span data-ttu-id="e7729-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7729-116">-DefaultProfile</span></span>
<span data-ttu-id="e7729-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e7729-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e7729-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7729-118">CommonParameters</span></span>
<span data-ttu-id="e7729-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e7729-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7729-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7729-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7729-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e7729-121">INPUTS</span></span>

### <span data-ttu-id="e7729-122">System. String</span><span class="sxs-lookup"><span data-stu-id="e7729-122">System.String</span></span>

## <span data-ttu-id="e7729-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e7729-123">OUTPUTS</span></span>

### <span data-ttu-id="e7729-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e7729-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e7729-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="e7729-125">NOTES</span></span>

## <span data-ttu-id="e7729-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e7729-126">RELATED LINKS</span></span>

[<span data-ttu-id="e7729-127">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="e7729-127">Add-AzureRmApplicationGatewayIPConfiguration</span></span>](./Add-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="e7729-128">Get-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="e7729-128">Get-AzureRmApplicationGatewayIPConfiguration</span></span>](./Get-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="e7729-129">New-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="e7729-129">New-AzureRmApplicationGatewayIPConfiguration</span></span>](./New-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="e7729-130">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="e7729-130">Set-AzureRmApplicationGatewayIPConfiguration</span></span>](./Set-AzureRmApplicationGatewayIPConfiguration.md)


