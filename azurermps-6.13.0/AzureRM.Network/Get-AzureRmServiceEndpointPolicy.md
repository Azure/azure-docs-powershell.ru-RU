---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmServiceEndpointPolicy.md
ms.openlocfilehash: 989b6aa91c0dabec1b72425f214c4097df374041
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560900"
---
# <span data-ttu-id="60f16-101">Get-AzureRmServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="60f16-101">Get-AzureRmServiceEndpointPolicy</span></span>

## <span data-ttu-id="60f16-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="60f16-102">SYNOPSIS</span></span>
<span data-ttu-id="60f16-103">{Заполнение кратких описаний}</span><span class="sxs-lookup"><span data-stu-id="60f16-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="60f16-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="60f16-104">SYNTAX</span></span>

```
Get-AzureRmServiceEndpointPolicy -Name <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="60f16-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="60f16-105">DESCRIPTION</span></span>
<span data-ttu-id="60f16-106">Командлет **Get-AzureRmServiceEndpointPolicy** получает политику конечной точки службы.</span><span class="sxs-lookup"><span data-stu-id="60f16-106">The **Get-AzureRmServiceEndpointPolicy** cmdlet gets a service endpoint policy.</span></span>

## <span data-ttu-id="60f16-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="60f16-107">EXAMPLES</span></span>

### <span data-ttu-id="60f16-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="60f16-108">Example 1</span></span>
```
$policy = Get-AzureRmServiceEndpointPolicy -Name "ServiceEndpointPolicy1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="60f16-109">Эта команда получает политику конечной точки службы с именем ServiceEndpointPolicy1, которая относится к группе ресурсов с именем ResourceGroup01, и сохраняет ее в переменной $policy.</span><span class="sxs-lookup"><span data-stu-id="60f16-109">This command gets the service endpoint policy named ServiceEndpointPolicy1 that belongs to the resource group named ResourceGroup01 and stores it in the $policy variable.</span></span>

### <span data-ttu-id="60f16-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="60f16-110">Example 2</span></span>
```
$policyList = Get-AzureRmServiceEndpointPolicy -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="60f16-111">Эта команда получает список всех политик конечной точки службы в группе ресурсов с именем ResourceGroup01 и сохраняет его в переменной $policyList.</span><span class="sxs-lookup"><span data-stu-id="60f16-111">This command gets a list of all the service endpoint policies in the resource group named ResourceGroup01 and stores it in the $policyList variable.</span></span>

## <span data-ttu-id="60f16-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="60f16-112">PARAMETERS</span></span>

### <span data-ttu-id="60f16-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60f16-113">-DefaultProfile</span></span>
<span data-ttu-id="60f16-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="60f16-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="60f16-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="60f16-115">-Name</span></span>
<span data-ttu-id="60f16-116">Имя политики конечной точки службы.</span><span class="sxs-lookup"><span data-stu-id="60f16-116">The name of the service endpoint policy</span></span>

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

### <span data-ttu-id="60f16-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60f16-117">-ResourceGroupName</span></span>
<span data-ttu-id="60f16-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="60f16-118">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60f16-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60f16-119">CommonParameters</span></span>
<span data-ttu-id="60f16-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="60f16-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="60f16-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60f16-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60f16-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="60f16-122">INPUTS</span></span>

### <span data-ttu-id="60f16-123">System. String</span><span class="sxs-lookup"><span data-stu-id="60f16-123">System.String</span></span>


## <span data-ttu-id="60f16-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="60f16-124">OUTPUTS</span></span>

### <span data-ttu-id="60f16-125">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="60f16-125">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>


## <span data-ttu-id="60f16-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="60f16-126">NOTES</span></span>

## <span data-ttu-id="60f16-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="60f16-127">RELATED LINKS</span></span>
