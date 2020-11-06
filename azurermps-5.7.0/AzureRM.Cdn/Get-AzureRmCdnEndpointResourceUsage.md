---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/get-azurermcdnendpointresourceusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnEndpointResourceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnEndpointResourceUsage.md
ms.openlocfilehash: 82daa7f202dce698a84d17292a199fbd8f85bca5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568642"
---
# <span data-ttu-id="a0665-101">Get-AzureRmCdnEndpointResourceUsage</span><span class="sxs-lookup"><span data-stu-id="a0665-101">Get-AzureRmCdnEndpointResourceUsage</span></span>

## <span data-ttu-id="a0665-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a0665-102">SYNOPSIS</span></span>
<span data-ttu-id="a0665-103">{Заполнение кратких описаний}</span><span class="sxs-lookup"><span data-stu-id="a0665-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a0665-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a0665-104">SYNTAX</span></span>

### <span data-ttu-id="a0665-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a0665-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzureRmCdnEndpointResourceUsage [-EndpointName <String>] -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a0665-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a0665-106">ByObjectParameterSet</span></span>
```
Get-AzureRmCdnEndpointResourceUsage [-EndpointName <String>] -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a0665-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a0665-107">DESCRIPTION</span></span>
<span data-ttu-id="a0665-108">{Заполнение в описании}}</span><span class="sxs-lookup"><span data-stu-id="a0665-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="a0665-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a0665-109">EXAMPLES</span></span>

### <span data-ttu-id="a0665-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a0665-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="a0665-111">{{Добавить пример описания}}</span><span class="sxs-lookup"><span data-stu-id="a0665-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="a0665-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a0665-112">PARAMETERS</span></span>

### <span data-ttu-id="a0665-113">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="a0665-113">-CdnEndpoint</span></span>
<span data-ttu-id="a0665-114">Объект конечной точки CDN.</span><span class="sxs-lookup"><span data-stu-id="a0665-114">The CDN endpoint object.</span></span>

```yaml
Type: PSEndpoint
Parameter Sets: ByObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a0665-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0665-115">-DefaultProfile</span></span>
<span data-ttu-id="a0665-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="a0665-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a0665-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="a0665-117">-EndpointName</span></span>
<span data-ttu-id="a0665-118">Имя конечной точки CDN Azure.</span><span class="sxs-lookup"><span data-stu-id="a0665-118">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="a0665-119">-Имя_профиля</span><span class="sxs-lookup"><span data-stu-id="a0665-119">-ProfileName</span></span>
<span data-ttu-id="a0665-120">Имя профиля CDN в службе Azure.</span><span class="sxs-lookup"><span data-stu-id="a0665-120">Azure CDN profile name.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0665-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0665-121">-ResourceGroupName</span></span>
<span data-ttu-id="a0665-122">Группа ресурсов в профиле CDN для Azure.</span><span class="sxs-lookup"><span data-stu-id="a0665-122">The resource group of the Azure CDN Profile.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0665-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0665-123">CommonParameters</span></span>
<span data-ttu-id="a0665-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a0665-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0665-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0665-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0665-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a0665-126">INPUTS</span></span>

### <span data-ttu-id="a0665-127">Microsoft. Azure. Commands. CDN. Models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="a0665-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="a0665-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a0665-128">OUTPUTS</span></span>

### <span data-ttu-id="a0665-129">Microsoft. Azure. Commands. CDN. Models. PSResourceUsage</span><span class="sxs-lookup"><span data-stu-id="a0665-129">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span></span>

## <span data-ttu-id="a0665-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="a0665-130">NOTES</span></span>

## <span data-ttu-id="a0665-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a0665-131">RELATED LINKS</span></span>

