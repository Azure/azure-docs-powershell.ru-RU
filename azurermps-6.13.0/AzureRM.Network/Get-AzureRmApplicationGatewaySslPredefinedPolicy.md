---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewaysslpredefinedpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewaySslPredefinedPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewaySslPredefinedPolicy.md
ms.openlocfilehash: 82713c41d6f2e3882c50ffbd5ab6b276a90dc2e1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567274"
---
# <span data-ttu-id="5e69b-101">Get-AzureRmApplicationGatewaySslPredefinedPolicy</span><span class="sxs-lookup"><span data-stu-id="5e69b-101">Get-AzureRmApplicationGatewaySslPredefinedPolicy</span></span>

## <span data-ttu-id="5e69b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5e69b-102">SYNOPSIS</span></span>
<span data-ttu-id="5e69b-103">Получает предопределенные политики SSL, предоставляемые шлюзом приложений.</span><span class="sxs-lookup"><span data-stu-id="5e69b-103">Gets Predefined SSL Policies provided by Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5e69b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5e69b-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewaySslPredefinedPolicy [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5e69b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5e69b-105">DESCRIPTION</span></span>
<span data-ttu-id="5e69b-106">Командлет **Get-AzureRmApplicationGatewaySslPredefinedPolicy** получает предопределенные политики SSL, предоставляемые шлюзом приложений.</span><span class="sxs-lookup"><span data-stu-id="5e69b-106">The **Get-AzureRmApplicationGatewaySslPredefinedPolicy** cmdlet gets Predefined SSL Policies provided by Application Gateway.</span></span>

## <span data-ttu-id="5e69b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5e69b-107">EXAMPLES</span></span>

### <span data-ttu-id="5e69b-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5e69b-108">Example 1</span></span>
```
PS C:\>$policies = Get-AzureRmApplicationGatewaySslPredefinedPolicy
```

<span data-ttu-id="5e69b-109">Эти команды возвращают все предопределенные политики SSL.</span><span class="sxs-lookup"><span data-stu-id="5e69b-109">This commands returns all the predefined SSL policies.</span></span>

### <span data-ttu-id="5e69b-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="5e69b-110">Example 2</span></span>
```
PS C:\>$policy = Get-AzureRmApplicationGatewaySslPredefinedPolicy -Name AppGwSslPolicy20170401
```

<span data-ttu-id="5e69b-111">Эти команды возвращают предопределенную политику с именем AppGwSslPolicy20170401.</span><span class="sxs-lookup"><span data-stu-id="5e69b-111">This commands returns predefined policy with name AppGwSslPolicy20170401.</span></span>

## <span data-ttu-id="5e69b-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5e69b-112">PARAMETERS</span></span>

### <span data-ttu-id="5e69b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e69b-113">-DefaultProfile</span></span>
<span data-ttu-id="5e69b-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5e69b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5e69b-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5e69b-115">-Name</span></span>
<span data-ttu-id="5e69b-116">Имя предопределенной политики SSL</span><span class="sxs-lookup"><span data-stu-id="5e69b-116">Name of the ssl predefined policy</span></span>

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

### <span data-ttu-id="5e69b-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e69b-117">CommonParameters</span></span>
<span data-ttu-id="5e69b-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5e69b-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e69b-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e69b-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e69b-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5e69b-120">INPUTS</span></span>

### <span data-ttu-id="5e69b-121">Ничего</span><span class="sxs-lookup"><span data-stu-id="5e69b-121">None</span></span>

## <span data-ttu-id="5e69b-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5e69b-122">OUTPUTS</span></span>

### <span data-ttu-id="5e69b-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySslPredefinedPolicy</span><span class="sxs-lookup"><span data-stu-id="5e69b-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPredefinedPolicy</span></span>

## <span data-ttu-id="5e69b-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="5e69b-124">NOTES</span></span>

## <span data-ttu-id="5e69b-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5e69b-125">RELATED LINKS</span></span>
