---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewaysslpredefinedpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewaySslPredefinedPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewaySslPredefinedPolicy.md
ms.openlocfilehash: 92c71163b922dacb7920fd842f3d662b18607a70
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566596"
---
# <span data-ttu-id="40ac2-101">Get-AzureRmApplicationGatewaySslPredefinedPolicy</span><span class="sxs-lookup"><span data-stu-id="40ac2-101">Get-AzureRmApplicationGatewaySslPredefinedPolicy</span></span>

## <span data-ttu-id="40ac2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="40ac2-102">SYNOPSIS</span></span>
<span data-ttu-id="40ac2-103">Получает предопределенные политики SSL, предоставляемые шлюзом приложений.</span><span class="sxs-lookup"><span data-stu-id="40ac2-103">Gets Predefined SSL Policies provided by Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="40ac2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="40ac2-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewaySslPredefinedPolicy [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="40ac2-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="40ac2-105">DESCRIPTION</span></span>
<span data-ttu-id="40ac2-106">Командлет **Get-AzureRmApplicationGatewaySslPredefinedPolicy** получает предопределенные политики SSL, предоставляемые шлюзом приложений.</span><span class="sxs-lookup"><span data-stu-id="40ac2-106">The **Get-AzureRmApplicationGatewaySslPredefinedPolicy** cmdlet gets Predefined SSL Policies provided by Application Gateway.</span></span>

## <span data-ttu-id="40ac2-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="40ac2-107">EXAMPLES</span></span>

### <span data-ttu-id="40ac2-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="40ac2-108">Example 1</span></span>
```
PS C:\>$policies = Get-AzureRmApplicationGatewaySslPredefinedPolicy
```

<span data-ttu-id="40ac2-109">Эти команды возвращают все предопределенные политики SSL.</span><span class="sxs-lookup"><span data-stu-id="40ac2-109">This commands returns all the predefined SSL policies.</span></span>

### <span data-ttu-id="40ac2-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="40ac2-110">Example 2</span></span>
```
PS C:\>$policy = Get-AzureRmApplicationGatewaySslPredefinedPolicy -Name AppGwSslPolicy20170401
```

<span data-ttu-id="40ac2-111">Эти команды возвращают предопределенную политику с именем AppGwSslPolicy20170401.</span><span class="sxs-lookup"><span data-stu-id="40ac2-111">This commands returns predefined policy with name AppGwSslPolicy20170401.</span></span>

## <span data-ttu-id="40ac2-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="40ac2-112">PARAMETERS</span></span>

### <span data-ttu-id="40ac2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40ac2-113">-DefaultProfile</span></span>
<span data-ttu-id="40ac2-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="40ac2-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="40ac2-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="40ac2-115">-Name</span></span>
<span data-ttu-id="40ac2-116">Имя предопределенной политики SSL</span><span class="sxs-lookup"><span data-stu-id="40ac2-116">Name of the ssl predefined policy</span></span>

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

### <span data-ttu-id="40ac2-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40ac2-117">CommonParameters</span></span>
<span data-ttu-id="40ac2-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="40ac2-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40ac2-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40ac2-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40ac2-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="40ac2-120">INPUTS</span></span>

### <span data-ttu-id="40ac2-121">Ничего</span><span class="sxs-lookup"><span data-stu-id="40ac2-121">None</span></span>

## <span data-ttu-id="40ac2-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="40ac2-122">OUTPUTS</span></span>

### <span data-ttu-id="40ac2-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySslPredefinedPolicy</span><span class="sxs-lookup"><span data-stu-id="40ac2-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPredefinedPolicy</span></span>
<span data-ttu-id="40ac2-124">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. Network. rePSApplicationGatewaySslPredefinedPolicy, Microsoft. Azure. Commands. Network, Version = 4.1.0.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="40ac2-124">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPredefinedPolicy, Microsoft.Azure.Commands.Network, Version=4.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="40ac2-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="40ac2-125">NOTES</span></span>

## <span data-ttu-id="40ac2-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="40ac2-126">RELATED LINKS</span></span>

