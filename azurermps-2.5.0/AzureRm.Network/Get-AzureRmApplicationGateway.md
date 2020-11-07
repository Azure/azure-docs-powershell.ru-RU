---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 77CDEE77-FD5D-4C2D-B027-FF1F6FF6618E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgateway
schema: 2.0.0
ms.openlocfilehash: 2b6373944f8b7bbc741557629fad7c9f717e979e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93915230"
---
# <span data-ttu-id="aa808-101">Get-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="aa808-101">Get-AzureRmApplicationGateway</span></span>

## <span data-ttu-id="aa808-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="aa808-102">SYNOPSIS</span></span>
<span data-ttu-id="aa808-103">Получает шлюз приложения.</span><span class="sxs-lookup"><span data-stu-id="aa808-103">Gets an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aa808-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="aa808-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGateway [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aa808-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="aa808-105">DESCRIPTION</span></span>
<span data-ttu-id="aa808-106">Командлет **Get-AzureRmApplicationGateway** получает шлюз приложения.</span><span class="sxs-lookup"><span data-stu-id="aa808-106">The **Get-AzureRmApplicationGateway** cmdlet gets an application gateway.</span></span>

## <span data-ttu-id="aa808-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="aa808-107">EXAMPLES</span></span>

### <span data-ttu-id="aa808-108">Пример 1: получение указанного шлюза приложения</span><span class="sxs-lookup"><span data-stu-id="aa808-108">Example 1: Get a specified application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="aa808-109">Эта команда получает шлюз приложения с именем ApplicationGateway01, который принадлежит группе ресурсов с именем ResourceGroup01, и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="aa808-109">This command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>

### <span data-ttu-id="aa808-110">Пример 2: получение списка шлюзов приложений в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="aa808-110">Example 2: Get a list of application gateways in a resource group</span></span>
```
PS C:\>$AppGwList = Get-AzureRmApplicationGateway -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="aa808-111">Эта команда получает список всех шлюзов приложений в группе ресурсов с именем ResourceGroup01 и сохраняет их в переменной $AppGwList.</span><span class="sxs-lookup"><span data-stu-id="aa808-111">This command gets a list of all the application gateways in the resource group named ResourceGroup01 and stores it in the $AppGwList variable.</span></span>

### <span data-ttu-id="aa808-112">Пример 3: получение списка шлюзов приложений в подписке</span><span class="sxs-lookup"><span data-stu-id="aa808-112">Example 3: Get a list of application gateways in a subscription</span></span>
```
PS C:\>$AppGwList = Get-AzureRmApplicationGateway
```

<span data-ttu-id="aa808-113">Эта команда возвращает список всех шлюзов приложений в подписке и сохраняет их в переменной $AppGwList.</span><span class="sxs-lookup"><span data-stu-id="aa808-113">This command gets a list of all the application gateways in the subscription and stores it in the $AppGwList variable.</span></span>

## <span data-ttu-id="aa808-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="aa808-114">PARAMETERS</span></span>

### <span data-ttu-id="aa808-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa808-115">-DefaultProfile</span></span>
<span data-ttu-id="aa808-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="aa808-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aa808-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="aa808-117">-Name</span></span>
<span data-ttu-id="aa808-118">Указывает имя шлюза приложения, который получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="aa808-118">Specifies the name of the application gateway that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa808-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa808-119">-ResourceGroupName</span></span>
<span data-ttu-id="aa808-120">Указывает имя группы ресурсов, которая содержит шлюз приложения.</span><span class="sxs-lookup"><span data-stu-id="aa808-120">Specifies the name of the resource group that contains the application gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa808-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa808-121">CommonParameters</span></span>
<span data-ttu-id="aa808-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="aa808-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa808-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa808-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa808-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="aa808-124">INPUTS</span></span>

### <span data-ttu-id="aa808-125">System. String</span><span class="sxs-lookup"><span data-stu-id="aa808-125">System.String</span></span>

## <span data-ttu-id="aa808-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="aa808-126">OUTPUTS</span></span>

### <span data-ttu-id="aa808-127">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="aa808-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="aa808-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="aa808-128">NOTES</span></span>

## <span data-ttu-id="aa808-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="aa808-129">RELATED LINKS</span></span>

[<span data-ttu-id="aa808-130">Остановить-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="aa808-130">Stop-AzureRmApplicationGateway</span></span>](./Stop-AzureRmApplicationGateway.md)


