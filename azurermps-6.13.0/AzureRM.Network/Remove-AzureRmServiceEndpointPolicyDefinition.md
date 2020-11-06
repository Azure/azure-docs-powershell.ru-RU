---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 3d406bf0dffb0ee250e1494fc05727d0a4c983ab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568457"
---
# <span data-ttu-id="32064-101">Remove-AzureRmServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="32064-101">Remove-AzureRmServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="32064-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="32064-102">SYNOPSIS</span></span>
<span data-ttu-id="32064-103">{Заполнение кратких описаний}</span><span class="sxs-lookup"><span data-stu-id="32064-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="32064-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="32064-104">SYNTAX</span></span>

```
Remove-AzureRmServiceEndpointPolicyDefinition [-Name <String>] -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="32064-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="32064-105">DESCRIPTION</span></span>
<span data-ttu-id="32064-106">Командлет **Remove-AzureRmServiceEndpointPolicy** удаляет политику конечной точки службы.</span><span class="sxs-lookup"><span data-stu-id="32064-106">The **Remove-AzureRmServiceEndpointPolicy** cmdlet removes a service endpoint policy.</span></span>

## <span data-ttu-id="32064-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="32064-107">EXAMPLES</span></span>

### <span data-ttu-id="32064-108">Пример 1: Удаление политики конечной точки службы с помощью имени</span><span class="sxs-lookup"><span data-stu-id="32064-108">Example 1: Removes a service endpoint policy using name</span></span>
```
Remove-AzureRmServiceEndpointPolicyDefinition -Name "PolicyDef1"
```

<span data-ttu-id="32064-109">Эта команда удаляет политику конечной точки службы с именем PolicyDef1</span><span class="sxs-lookup"><span data-stu-id="32064-109">This command removes a service endpoint policy with name PolicyDef1</span></span>

## <span data-ttu-id="32064-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="32064-110">PARAMETERS</span></span>

### <span data-ttu-id="32064-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32064-111">-DefaultProfile</span></span>
<span data-ttu-id="32064-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="32064-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="32064-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="32064-113">-Name</span></span>
<span data-ttu-id="32064-114">Имя определения конечной точки службы.</span><span class="sxs-lookup"><span data-stu-id="32064-114">The name of the service endpoint definition</span></span>

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

### <span data-ttu-id="32064-115">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="32064-115">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="32064-116">ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="32064-116">The ServiceEndpointPolicy</span></span>

```yaml
Type: PSServiceEndpointPolicy
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="32064-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32064-117">CommonParameters</span></span>
<span data-ttu-id="32064-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="32064-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="32064-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32064-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32064-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="32064-120">INPUTS</span></span>

### <span data-ttu-id="32064-121">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="32064-121">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>


## <span data-ttu-id="32064-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="32064-122">OUTPUTS</span></span>

### <span data-ttu-id="32064-123">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="32064-123">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>


## <span data-ttu-id="32064-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="32064-124">NOTES</span></span>

## <span data-ttu-id="32064-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="32064-125">RELATED LINKS</span></span>
