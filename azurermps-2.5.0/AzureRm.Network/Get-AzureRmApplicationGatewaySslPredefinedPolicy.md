---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewaysslpredefinedpolicy
schema: 2.0.0
ms.openlocfilehash: a977de2b4a60f0fc5ae93e175d521d398d40f850
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93915198"
---
# <span data-ttu-id="44102-101">Get-AzureRmApplicationGatewaySslPredefinedPolicy</span><span class="sxs-lookup"><span data-stu-id="44102-101">Get-AzureRmApplicationGatewaySslPredefinedPolicy</span></span>

## <span data-ttu-id="44102-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="44102-102">SYNOPSIS</span></span>
<span data-ttu-id="44102-103">Получает предопределенные политики SSL, предоставляемые шлюзом приложений.</span><span class="sxs-lookup"><span data-stu-id="44102-103">Gets Predefined SSL Policies provided by Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="44102-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="44102-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewaySslPredefinedPolicy [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="44102-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="44102-105">DESCRIPTION</span></span>
<span data-ttu-id="44102-106">Командлет **Get-AzureRmApplicationGatewaySslPredefinedPolicy** получает предопределенные политики SSL, предоставляемые шлюзом приложений.</span><span class="sxs-lookup"><span data-stu-id="44102-106">The **Get-AzureRmApplicationGatewaySslPredefinedPolicy** cmdlet gets Predefined SSL Policies provided by Application Gateway.</span></span>

## <span data-ttu-id="44102-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="44102-107">EXAMPLES</span></span>

### <span data-ttu-id="44102-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="44102-108">Example 1</span></span>
```
PS C:\>$policies = Get-AzureRmApplicationGatewaySslPredefinedPolicy
```

<span data-ttu-id="44102-109">Эти команды возвращают все предопределенные политики SSL.</span><span class="sxs-lookup"><span data-stu-id="44102-109">This commands returns all the predefined SSL policies.</span></span>

### <span data-ttu-id="44102-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="44102-110">Example 2</span></span>
```
PS C:\>$policy = Get-AzureRmApplicationGatewaySslPredefinedPolicy -Name AppGwSslPolicy20170401
```

<span data-ttu-id="44102-111">Эти команды возвращают предопределенную политику с именем AppGwSslPolicy20170401.</span><span class="sxs-lookup"><span data-stu-id="44102-111">This commands returns predefined policy with name AppGwSslPolicy20170401.</span></span>

## <span data-ttu-id="44102-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="44102-112">PARAMETERS</span></span>

### <span data-ttu-id="44102-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44102-113">-DefaultProfile</span></span>
<span data-ttu-id="44102-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="44102-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="44102-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="44102-115">-Name</span></span>
<span data-ttu-id="44102-116">Имя предопределенной политики SSL</span><span class="sxs-lookup"><span data-stu-id="44102-116">Name of the ssl predefined policy</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44102-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44102-117">CommonParameters</span></span>
<span data-ttu-id="44102-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="44102-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44102-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44102-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44102-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="44102-120">INPUTS</span></span>

### <span data-ttu-id="44102-121">Ничего</span><span class="sxs-lookup"><span data-stu-id="44102-121">None</span></span>

## <span data-ttu-id="44102-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="44102-122">OUTPUTS</span></span>

### <span data-ttu-id="44102-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySslPredefinedPolicy</span><span class="sxs-lookup"><span data-stu-id="44102-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPredefinedPolicy</span></span>
<span data-ttu-id="44102-124">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. Network. rePSApplicationGatewaySslPredefinedPolicy, Microsoft. Azure. Commands. Network, Version = 4.1.0.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="44102-124">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPredefinedPolicy, Microsoft.Azure.Commands.Network, Version=4.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="44102-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="44102-125">NOTES</span></span>

## <span data-ttu-id="44102-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="44102-126">RELATED LINKS</span></span>

