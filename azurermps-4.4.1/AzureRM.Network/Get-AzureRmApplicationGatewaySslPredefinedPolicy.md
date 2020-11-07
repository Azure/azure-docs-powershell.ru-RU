---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewaySslPredefinedPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewaySslPredefinedPolicy.md
ms.openlocfilehash: 03d47278681cbba23895c00b124cc3a2fc2cc6e7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93735158"
---
# <span data-ttu-id="3c705-101">Get-AzureRmApplicationGatewaySslPredefinedPolicy</span><span class="sxs-lookup"><span data-stu-id="3c705-101">Get-AzureRmApplicationGatewaySslPredefinedPolicy</span></span>

## <span data-ttu-id="3c705-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3c705-102">SYNOPSIS</span></span>
<span data-ttu-id="3c705-103">Получает предопределенные политики SSL, предоставляемые шлюзом приложений.</span><span class="sxs-lookup"><span data-stu-id="3c705-103">Gets Predefined SSL Policies provided by Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3c705-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3c705-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewaySslPredefinedPolicy [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3c705-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3c705-105">DESCRIPTION</span></span>
<span data-ttu-id="3c705-106">Командлет **Get-AzureRmApplicationGatewaySslPredefinedPolicy** получает предопределенные политики SSL, предоставляемые шлюзом приложений.</span><span class="sxs-lookup"><span data-stu-id="3c705-106">The **Get-AzureRmApplicationGatewaySslPredefinedPolicy** cmdlet gets Predefined SSL Policies provided by Application Gateway.</span></span>

## <span data-ttu-id="3c705-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3c705-107">EXAMPLES</span></span>

### <span data-ttu-id="3c705-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3c705-108">Example 1</span></span>
```
PS C:\>$policies = Get-AzureRmApplicationGatewaySslPredefinedPolicy
```

<span data-ttu-id="3c705-109">Эти команды возвращают все предопределенные политики SSL.</span><span class="sxs-lookup"><span data-stu-id="3c705-109">This commands returns all the predefined SSL policies.</span></span>

### <span data-ttu-id="3c705-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="3c705-110">Example 2</span></span>
```
PS C:\>$policy = Get-AzureRmApplicationGatewaySslPredefinedPolicy -Name AppGwSslPolicy20170401
```

<span data-ttu-id="3c705-111">Эти команды возвращают предопределенную политику с именем AppGwSslPolicy20170401.</span><span class="sxs-lookup"><span data-stu-id="3c705-111">This commands returns predefined policy with name AppGwSslPolicy20170401.</span></span>

## <span data-ttu-id="3c705-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3c705-112">PARAMETERS</span></span>

### <span data-ttu-id="3c705-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3c705-113">-Name</span></span>
<span data-ttu-id="3c705-114">Имя предопределенной политики SSL</span><span class="sxs-lookup"><span data-stu-id="3c705-114">Name of the ssl predefined policy</span></span>

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

### <span data-ttu-id="3c705-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c705-115">-DefaultProfile</span></span>
<span data-ttu-id="3c705-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3c705-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3c705-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c705-117">CommonParameters</span></span>
<span data-ttu-id="3c705-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3c705-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c705-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c705-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c705-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3c705-120">INPUTS</span></span>

### <span data-ttu-id="3c705-121">Ничего</span><span class="sxs-lookup"><span data-stu-id="3c705-121">None</span></span>

## <span data-ttu-id="3c705-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3c705-122">OUTPUTS</span></span>

### <span data-ttu-id="3c705-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySslPredefinedPolicy</span><span class="sxs-lookup"><span data-stu-id="3c705-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPredefinedPolicy</span></span>
<span data-ttu-id="3c705-124">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. Network. rePSApplicationGatewaySslPredefinedPolicy, Microsoft. Azure. Commands. Network, Version = 4.1.0.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="3c705-124">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPredefinedPolicy, Microsoft.Azure.Commands.Network, Version=4.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="3c705-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="3c705-125">NOTES</span></span>

## <span data-ttu-id="3c705-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3c705-126">RELATED LINKS</span></span>

