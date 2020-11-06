---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 85C0A1C3-FC6D-496A-B6B5-8DC2A73B8032
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayFrontendPort.md
ms.openlocfilehash: 1c6a5ffee2f4a8b358f483fee2904fe1a7a970da
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557711"
---
# <span data-ttu-id="1af37-101">Set-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="1af37-101">Set-AzureRmApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="1af37-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1af37-102">SYNOPSIS</span></span>
<span data-ttu-id="1af37-103">Изменяет интерфейсный порт для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="1af37-103">Modifies a front-end port for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1af37-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1af37-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayFrontendPort -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Port <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1af37-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1af37-105">DESCRIPTION</span></span>
<span data-ttu-id="1af37-106">Командлет **Set-AzureRmApplicationGatewayFrontendPort** изменяет интерфейсный порт для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="1af37-106">The **Set-AzureRmApplicationGatewayFrontendPort** cmdlet modifies a front-end port for an application gateway.</span></span>

## <span data-ttu-id="1af37-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1af37-107">EXAMPLES</span></span>

### <span data-ttu-id="1af37-108">Пример 1: Установка внешнего порта шлюза приложения в 80</span><span class="sxs-lookup"><span data-stu-id="1af37-108">Example 1: Set an application gateway front-end port to 80</span></span>
```
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayFrontendPort -ApplicationGateway $AppGw -Name "FrontEndPort01" -Port 80
```

<span data-ttu-id="1af37-109">Первая команда получает шлюз приложения с именем ApplicationGateway01, который принадлежит группе ресурсов с именем ResourceGroup01, и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="1af37-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="1af37-110">Вторая команда изменяет шлюз в $AppGw для использования порта 80 для клиентского порта с именем FrontEndPort01.</span><span class="sxs-lookup"><span data-stu-id="1af37-110">The second command modifies the gateway in $AppGw to use port 80 for the front-end port named FrontEndPort01.</span></span>

## <span data-ttu-id="1af37-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1af37-111">PARAMETERS</span></span>

### <span data-ttu-id="1af37-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1af37-112">-ApplicationGateway</span></span>
<span data-ttu-id="1af37-113">Указывает объект шлюза приложения, с которым этот командлет связывает интерфейсный порт.</span><span class="sxs-lookup"><span data-stu-id="1af37-113">Specifies the application gateway object with which this cmdlet associates the front-end port.</span></span>

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

### <span data-ttu-id="1af37-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1af37-114">-Name</span></span>
<span data-ttu-id="1af37-115">Указывает имя переднего порта, который нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="1af37-115">Specifies the name of the front-end port to modify.</span></span>

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

### <span data-ttu-id="1af37-116">-Port (порт)</span><span class="sxs-lookup"><span data-stu-id="1af37-116">-Port</span></span>
<span data-ttu-id="1af37-117">Задает номер порта, который будет использоваться для интерфейса переднего порта.</span><span class="sxs-lookup"><span data-stu-id="1af37-117">Specifies the port number to use for the front-end port.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1af37-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1af37-118">-DefaultProfile</span></span>
<span data-ttu-id="1af37-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1af37-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1af37-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1af37-120">CommonParameters</span></span>
<span data-ttu-id="1af37-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1af37-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1af37-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1af37-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1af37-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1af37-123">INPUTS</span></span>

### <span data-ttu-id="1af37-124">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1af37-124">PSApplicationGateway</span></span>
<span data-ttu-id="1af37-125">Параметр "ApplicationGateway" принимает значение типа "PSApplicationGateway" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="1af37-125">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="1af37-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1af37-126">OUTPUTS</span></span>

### <span data-ttu-id="1af37-127">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1af37-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1af37-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="1af37-128">NOTES</span></span>

## <span data-ttu-id="1af37-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1af37-129">RELATED LINKS</span></span>

[<span data-ttu-id="1af37-130">Add-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="1af37-130">Add-AzureRmApplicationGatewayFrontendPort</span></span>](./Add-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="1af37-131">Get-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="1af37-131">Get-AzureRmApplicationGatewayFrontendPort</span></span>](./Get-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="1af37-132">New-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="1af37-132">New-AzureRmApplicationGatewayFrontendPort</span></span>](./New-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="1af37-133">Remove-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="1af37-133">Remove-AzureRmApplicationGatewayFrontendPort</span></span>](./Remove-AzureRmApplicationGatewayFrontendPort.md)
