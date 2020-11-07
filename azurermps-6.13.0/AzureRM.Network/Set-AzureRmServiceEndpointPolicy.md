---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmServiceEndpointPolicy.md
ms.openlocfilehash: ecd5a8eafc70a88b4ebda17a83f2b40139f5463f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732915"
---
# <span data-ttu-id="4097c-101">Set-AzureRmServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="4097c-101">Set-AzureRmServiceEndpointPolicy</span></span>

## <span data-ttu-id="4097c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4097c-102">SYNOPSIS</span></span>
<span data-ttu-id="4097c-103">{Заполнение кратких описаний}</span><span class="sxs-lookup"><span data-stu-id="4097c-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4097c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4097c-104">SYNTAX</span></span>

```
Set-AzureRmServiceEndpointPolicy -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4097c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4097c-105">DESCRIPTION</span></span>
<span data-ttu-id="4097c-106">Командлет **Set-AzureRmServiceEndpointPolicy** , чтобы создать политику конечной точки службы.</span><span class="sxs-lookup"><span data-stu-id="4097c-106">The **Set-AzureRmServiceEndpointPolicy** cmdlet create a service endpoint policy.</span></span>

## <span data-ttu-id="4097c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4097c-107">EXAMPLES</span></span>

### <span data-ttu-id="4097c-108">Пример 1: Настройка политики конечной точки службы</span><span class="sxs-lookup"><span data-stu-id="4097c-108">Example 1: Sets a service endpoint policy</span></span>
```
$serviceEndpointPolicy = Set-AzureRmServiceEndpointPolicy -Name "Policy1" -ServiceEndpointPolicy $serviceEndpointPolicy -ResourceGroup "resourcegroup1"
```

<span data-ttu-id="4097c-109">Эта команда обновляет политику конечной точки службы с именем Policy1, определенную объектом, $serviceEndpointPolicy принадлежит к группе ресурсов "resourcegroup1".</span><span class="sxs-lookup"><span data-stu-id="4097c-109">This command updates a service endpoint policy named Policy1 defined by the object $serviceEndpointPolicy belong to the resourcegroup "resourcegroup1".</span></span>

## <span data-ttu-id="4097c-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4097c-110">PARAMETERS</span></span>

### <span data-ttu-id="4097c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4097c-111">-DefaultProfile</span></span>
<span data-ttu-id="4097c-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4097c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4097c-113">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="4097c-113">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="4097c-114">ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="4097c-114">The ServiceEndpointPolicy</span></span>

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

### <span data-ttu-id="4097c-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4097c-115">CommonParameters</span></span>
<span data-ttu-id="4097c-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4097c-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="4097c-117">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4097c-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4097c-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4097c-118">INPUTS</span></span>

### <span data-ttu-id="4097c-119">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="4097c-119">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>


## <span data-ttu-id="4097c-120">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4097c-120">OUTPUTS</span></span>

### <span data-ttu-id="4097c-121">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="4097c-121">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>


## <span data-ttu-id="4097c-122">Пуск</span><span class="sxs-lookup"><span data-stu-id="4097c-122">NOTES</span></span>

## <span data-ttu-id="4097c-123">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4097c-123">RELATED LINKS</span></span>
