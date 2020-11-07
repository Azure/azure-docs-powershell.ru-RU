---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 289B761C-1A1D-46D2-8755-B6B6A4758EFC
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: 500d53810050dd539b57d2182a3b1aae9b4f358a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93909557"
---
# <span data-ttu-id="19937-101">Remove-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="19937-101">Remove-AzApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="19937-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="19937-102">SYNOPSIS</span></span>
<span data-ttu-id="19937-103">Удаляет интерфейсную конфигурацию IP из шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="19937-103">Removes a front-end IP configuration from an application gateway.</span></span>

## <span data-ttu-id="19937-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="19937-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayFrontendIPConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="19937-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="19937-105">DESCRIPTION</span></span>
<span data-ttu-id="19937-106">Командлет **Remove-AzApplicationGatewayFrontendIPConfig** удаляет IP-интерфейс из шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="19937-106">The **Remove-AzApplicationGatewayFrontendIPConfig** cmdlet removes frontend IP from an Azure application gateway.</span></span>

## <span data-ttu-id="19937-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="19937-107">EXAMPLES</span></span>

### <span data-ttu-id="19937-108">Пример 1: удаление интерфейсной конфигурации IP</span><span class="sxs-lookup"><span data-stu-id="19937-108">Example 1: Remove a front-end IP configuration</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontEndIP02"
```

<span data-ttu-id="19937-109">Первая команда получает шлюз приложения с именем ApplicationGateway01 и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="19937-109">The first command gets an application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="19937-110">Вторая команда удаляет IP-конфигурацию переднего плана с именем FrontEndIP02 из шлюза приложений, хранящегося в $AppGw.</span><span class="sxs-lookup"><span data-stu-id="19937-110">The second command removes the front-end IP configuration named FrontEndIP02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="19937-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="19937-111">PARAMETERS</span></span>

### <span data-ttu-id="19937-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="19937-112">-ApplicationGateway</span></span>
<span data-ttu-id="19937-113">Указывает шлюз приложений, из которого нужно удалить IP-конфигурацию интерфейсной части.</span><span class="sxs-lookup"><span data-stu-id="19937-113">Specifies an application gateway from which to remove a front-end IP configuration.</span></span>

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

### <span data-ttu-id="19937-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19937-114">-DefaultProfile</span></span>
<span data-ttu-id="19937-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="19937-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="19937-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="19937-116">-Name</span></span>
<span data-ttu-id="19937-117">Указывает имя удаляемой интерфейсной IP-конфигурации.</span><span class="sxs-lookup"><span data-stu-id="19937-117">Specifies the name of a front-end IP configuration to remove.</span></span>

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

### <span data-ttu-id="19937-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19937-118">CommonParameters</span></span>
<span data-ttu-id="19937-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="19937-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19937-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19937-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19937-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="19937-121">INPUTS</span></span>

### <span data-ttu-id="19937-122">System. String</span><span class="sxs-lookup"><span data-stu-id="19937-122">System.String</span></span>

## <span data-ttu-id="19937-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="19937-123">OUTPUTS</span></span>

### <span data-ttu-id="19937-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="19937-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="19937-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="19937-125">NOTES</span></span>

## <span data-ttu-id="19937-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="19937-126">RELATED LINKS</span></span>

[<span data-ttu-id="19937-127">Add-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="19937-127">Add-AzApplicationGatewayFrontendIPConfig</span></span>](./Add-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="19937-128">Get-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="19937-128">Get-AzApplicationGatewayFrontendIPConfig</span></span>](./Get-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="19937-129">New-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="19937-129">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="19937-130">Set-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="19937-130">Set-AzApplicationGatewayFrontendIPConfig</span></span>](./Set-AzApplicationGatewayFrontendIPConfig.md)


