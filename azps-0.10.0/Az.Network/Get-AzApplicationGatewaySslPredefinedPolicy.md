---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaysslpredefinedpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewaySslPredefinedPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewaySslPredefinedPolicy.md
ms.openlocfilehash: 2c55da6b7193d02de51e273df4626152d6d088fb
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910037"
---
# <span data-ttu-id="50c86-101">Get-AzApplicationGatewaySslPredefinedPolicy</span><span class="sxs-lookup"><span data-stu-id="50c86-101">Get-AzApplicationGatewaySslPredefinedPolicy</span></span>

## <span data-ttu-id="50c86-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="50c86-102">SYNOPSIS</span></span>
<span data-ttu-id="50c86-103">Получает предопределенные политики SSL, предоставляемые шлюзом приложений.</span><span class="sxs-lookup"><span data-stu-id="50c86-103">Gets Predefined SSL Policies provided by Application Gateway.</span></span>

## <span data-ttu-id="50c86-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="50c86-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySslPredefinedPolicy [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="50c86-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="50c86-105">DESCRIPTION</span></span>
<span data-ttu-id="50c86-106">Командлет **Get-AzApplicationGatewaySslPredefinedPolicy** получает предопределенные политики SSL, предоставляемые шлюзом приложений.</span><span class="sxs-lookup"><span data-stu-id="50c86-106">The **Get-AzApplicationGatewaySslPredefinedPolicy** cmdlet gets Predefined SSL Policies provided by Application Gateway.</span></span>

## <span data-ttu-id="50c86-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="50c86-107">EXAMPLES</span></span>

### <span data-ttu-id="50c86-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="50c86-108">Example 1</span></span>
```
PS C:\>$policies = Get-AzApplicationGatewaySslPredefinedPolicy
```

<span data-ttu-id="50c86-109">Эти команды возвращают все предопределенные политики SSL.</span><span class="sxs-lookup"><span data-stu-id="50c86-109">This commands returns all the predefined SSL policies.</span></span>

### <span data-ttu-id="50c86-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="50c86-110">Example 2</span></span>
```
PS C:\>$policy = Get-AzApplicationGatewaySslPredefinedPolicy -Name AppGwSslPolicy20170401
```

<span data-ttu-id="50c86-111">Эти команды возвращают предопределенную политику с именем AppGwSslPolicy20170401.</span><span class="sxs-lookup"><span data-stu-id="50c86-111">This commands returns predefined policy with name AppGwSslPolicy20170401.</span></span>

## <span data-ttu-id="50c86-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="50c86-112">PARAMETERS</span></span>

### <span data-ttu-id="50c86-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50c86-113">-DefaultProfile</span></span>
<span data-ttu-id="50c86-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="50c86-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="50c86-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="50c86-115">-Name</span></span>
<span data-ttu-id="50c86-116">Имя предопределенной политики SSL</span><span class="sxs-lookup"><span data-stu-id="50c86-116">Name of the ssl predefined policy</span></span>

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

### <span data-ttu-id="50c86-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50c86-117">CommonParameters</span></span>
<span data-ttu-id="50c86-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="50c86-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50c86-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50c86-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50c86-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="50c86-120">INPUTS</span></span>

### <span data-ttu-id="50c86-121">Ничего</span><span class="sxs-lookup"><span data-stu-id="50c86-121">None</span></span>

## <span data-ttu-id="50c86-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="50c86-122">OUTPUTS</span></span>

### <span data-ttu-id="50c86-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySslPredefinedPolicy</span><span class="sxs-lookup"><span data-stu-id="50c86-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPredefinedPolicy</span></span>
<span data-ttu-id="50c86-124">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. Network. rePSApplicationGatewaySslPredefinedPolicy, Microsoft. Azure. Commands. Network, Version = 4.1.0.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="50c86-124">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPredefinedPolicy, Microsoft.Azure.Commands.Network, Version=4.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="50c86-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="50c86-125">NOTES</span></span>

## <span data-ttu-id="50c86-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="50c86-126">RELATED LINKS</span></span>

