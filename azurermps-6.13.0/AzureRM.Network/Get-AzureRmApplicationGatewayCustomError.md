---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayCustomError.md
ms.openlocfilehash: b2f748bca68bff772026237f3bb6205ca6bc1923
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734344"
---
# <span data-ttu-id="eedea-101">Get-AzureRmApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="eedea-101">Get-AzureRmApplicationGatewayCustomError</span></span>

## <span data-ttu-id="eedea-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="eedea-102">SYNOPSIS</span></span>
<span data-ttu-id="eedea-103">Получает пользовательские ошибки из шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="eedea-103">Gets custom error(s) from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eedea-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="eedea-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayCustomError [-StatusCode <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eedea-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="eedea-105">DESCRIPTION</span></span>
<span data-ttu-id="eedea-106">Командлет **Get-AzureRmApplicationGatewayCustomError** получает пользовательские ошибки из шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="eedea-106">The **Get-AzureRmApplicationGatewayCustomError** cmdlet gets custom error(s) from an application gateway.</span></span>

## <span data-ttu-id="eedea-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="eedea-107">EXAMPLES</span></span>

### <span data-ttu-id="eedea-108">Пример 1: получение настраиваемой ошибки в шлюзе приложений</span><span class="sxs-lookup"><span data-stu-id="eedea-108">Example 1: Gets a custom error in an application gateway</span></span>
```powershell
PS C:\> $ce = Get-AzureRmApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502
```

<span data-ttu-id="eedea-109">Эта команда возвращает и возвращает ошибку 502 кода состояния HTTP из $appgw шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="eedea-109">This command gets and returns the custom error of http status code 502 from the application gateway $appgw.</span></span>

### <span data-ttu-id="eedea-110">Пример 2: получение списка всех настраиваемых ошибок в шлюзе приложений</span><span class="sxs-lookup"><span data-stu-id="eedea-110">Example 2: Gets the list of all custom errors in an application gateway</span></span>
```powershell
PS C:\> $ces = Get-AzureRmApplicationGatewayCustomError -ApplicationGateway $appgw
```

<span data-ttu-id="eedea-111">Эта команда возвращает список всех настраиваемых ошибок из $appgw шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="eedea-111">This command gets and returns the list of all custom errors from the application gateway $appgw.</span></span>

## <span data-ttu-id="eedea-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="eedea-112">PARAMETERS</span></span>

### <span data-ttu-id="eedea-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="eedea-113">-ApplicationGateway</span></span>
<span data-ttu-id="eedea-114">Шлюз приложений</span><span class="sxs-lookup"><span data-stu-id="eedea-114">The Application Gateway</span></span>

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

### <span data-ttu-id="eedea-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eedea-115">-DefaultProfile</span></span>
<span data-ttu-id="eedea-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="eedea-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eedea-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="eedea-117">-StatusCode</span></span>
<span data-ttu-id="eedea-118">Код состояния ошибки клиента шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="eedea-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="eedea-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eedea-119">CommonParameters</span></span>
<span data-ttu-id="eedea-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="eedea-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eedea-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eedea-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eedea-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="eedea-122">INPUTS</span></span>

### <span data-ttu-id="eedea-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="eedea-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="eedea-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="eedea-124">OUTPUTS</span></span>

### <span data-ttu-id="eedea-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="eedea-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="eedea-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="eedea-126">NOTES</span></span>

## <span data-ttu-id="eedea-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="eedea-127">RELATED LINKS</span></span>
