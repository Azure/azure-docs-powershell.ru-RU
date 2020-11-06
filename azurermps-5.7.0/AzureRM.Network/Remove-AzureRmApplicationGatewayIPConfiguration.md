---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6943BB5C-D709-4A80-AF5E-DC9501C20680
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 823b4ce458e4308965b4c5bea1ad5739708f7aff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568999"
---
# <span data-ttu-id="9d347-101">Remove-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="9d347-101">Remove-AzureRmApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="9d347-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9d347-102">SYNOPSIS</span></span>
<span data-ttu-id="9d347-103">Удаление IP-конфигурации с шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="9d347-103">Removes an IP configuration from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9d347-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9d347-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayIPConfiguration -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9d347-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9d347-105">DESCRIPTION</span></span>
<span data-ttu-id="9d347-106">Командлет **Remove-AzureRmApplicationGatewayIPConfiguration** УДАЛЯЕТ конфигурацию IP из шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="9d347-106">The **Remove-AzureRmApplicationGatewayIPConfiguration** cmdlet removes an IP configuration from an Azure application gateway.</span></span>

## <span data-ttu-id="9d347-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9d347-107">EXAMPLES</span></span>

### <span data-ttu-id="9d347-108">Пример 1: Удаление конфигурации IP из шлюза приложений Azure</span><span class="sxs-lookup"><span data-stu-id="9d347-108">Example 1: Remove an IP configuration from an Azure application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "Subnet02"
```

<span data-ttu-id="9d347-109">Первая команда получает шлюз приложения и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="9d347-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="9d347-110">Вторая команда удаляет IP-конфигурацию с именем Subnet02 из шлюза приложений, хранящегося в $AppGw.</span><span class="sxs-lookup"><span data-stu-id="9d347-110">The second command removes the IP configuration named Subnet02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="9d347-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9d347-111">PARAMETERS</span></span>

### <span data-ttu-id="9d347-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9d347-112">-ApplicationGateway</span></span>
<span data-ttu-id="9d347-113">Указывает шлюз приложений, из которого нужно удалить конфигурацию IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="9d347-113">Specifies the application gateway from which to remove an IP configuration.</span></span>

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

### <span data-ttu-id="9d347-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d347-114">-DefaultProfile</span></span>
<span data-ttu-id="9d347-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9d347-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9d347-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9d347-116">-Name</span></span>
<span data-ttu-id="9d347-117">Указывает имя удаляемой IP-конфигурации.</span><span class="sxs-lookup"><span data-stu-id="9d347-117">Specifies the name of the IP configuration to remove.</span></span>

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

### <span data-ttu-id="9d347-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d347-118">CommonParameters</span></span>
<span data-ttu-id="9d347-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9d347-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d347-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d347-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d347-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9d347-121">INPUTS</span></span>

### <span data-ttu-id="9d347-122">System. String</span><span class="sxs-lookup"><span data-stu-id="9d347-122">System.String</span></span>

## <span data-ttu-id="9d347-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9d347-123">OUTPUTS</span></span>

### <span data-ttu-id="9d347-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9d347-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9d347-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="9d347-125">NOTES</span></span>

## <span data-ttu-id="9d347-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9d347-126">RELATED LINKS</span></span>

[<span data-ttu-id="9d347-127">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="9d347-127">Add-AzureRmApplicationGatewayIPConfiguration</span></span>](./Add-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="9d347-128">Get-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="9d347-128">Get-AzureRmApplicationGatewayIPConfiguration</span></span>](./Get-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="9d347-129">New-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="9d347-129">New-AzureRmApplicationGatewayIPConfiguration</span></span>](./New-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="9d347-130">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="9d347-130">Set-AzureRmApplicationGatewayIPConfiguration</span></span>](./Set-AzureRmApplicationGatewayIPConfiguration.md)


