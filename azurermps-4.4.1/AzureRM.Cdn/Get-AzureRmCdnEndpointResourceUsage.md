---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnEndpointResourceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnEndpointResourceUsage.md
ms.openlocfilehash: f9d9d307959d53748afe7219ccb4cbce631c5b1e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93570100"
---
# <span data-ttu-id="98ae2-101">Get-AzureRmCdnEndpointResourceUsage</span><span class="sxs-lookup"><span data-stu-id="98ae2-101">Get-AzureRmCdnEndpointResourceUsage</span></span>

## <span data-ttu-id="98ae2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="98ae2-102">SYNOPSIS</span></span>
<span data-ttu-id="98ae2-103">{Заполнение кратких описаний}</span><span class="sxs-lookup"><span data-stu-id="98ae2-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="98ae2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="98ae2-104">SYNTAX</span></span>

### <span data-ttu-id="98ae2-105">Параметры, заданные для параметров полей (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="98ae2-105">Parameter Set for fields parameters (Default)</span></span>
```
Get-AzureRmCdnEndpointResourceUsage [-EndpointName <String>] -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="98ae2-106">Параметр, заданный для параметров объекта</span><span class="sxs-lookup"><span data-stu-id="98ae2-106">Parameter Set for object parameters</span></span>
```
Get-AzureRmCdnEndpointResourceUsage [-EndpointName <String>] -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="98ae2-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="98ae2-107">DESCRIPTION</span></span>
<span data-ttu-id="98ae2-108">{Заполнение в описании}}</span><span class="sxs-lookup"><span data-stu-id="98ae2-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="98ae2-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="98ae2-109">EXAMPLES</span></span>

### <span data-ttu-id="98ae2-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="98ae2-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="98ae2-111">{{Добавить пример описания}}</span><span class="sxs-lookup"><span data-stu-id="98ae2-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="98ae2-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="98ae2-112">PARAMETERS</span></span>

### <span data-ttu-id="98ae2-113">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="98ae2-113">-CdnEndpoint</span></span>
<span data-ttu-id="98ae2-114">Объект конечной точки CDN.</span><span class="sxs-lookup"><span data-stu-id="98ae2-114">The CDN endpoint object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint
Parameter Sets: Parameter Set for object parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="98ae2-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="98ae2-115">-EndpointName</span></span>
<span data-ttu-id="98ae2-116">Имя конечной точки CDN Azure.</span><span class="sxs-lookup"><span data-stu-id="98ae2-116">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="98ae2-117">-Имя_профиля</span><span class="sxs-lookup"><span data-stu-id="98ae2-117">-ProfileName</span></span>
<span data-ttu-id="98ae2-118">Имя профиля CDN в службе Azure.</span><span class="sxs-lookup"><span data-stu-id="98ae2-118">Azure CDN profile name.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98ae2-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98ae2-119">-ResourceGroupName</span></span>
<span data-ttu-id="98ae2-120">Группа ресурсов в профиле CDN для Azure.</span><span class="sxs-lookup"><span data-stu-id="98ae2-120">The resource group of the Azure CDN Profile.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98ae2-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98ae2-121">-DefaultProfile</span></span>
<span data-ttu-id="98ae2-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="98ae2-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="98ae2-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98ae2-123">CommonParameters</span></span>
<span data-ttu-id="98ae2-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="98ae2-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98ae2-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98ae2-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98ae2-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="98ae2-126">INPUTS</span></span>

### <span data-ttu-id="98ae2-127">Microsoft. Azure. Commands. CDN. Models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="98ae2-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="98ae2-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="98ae2-128">OUTPUTS</span></span>

### <span data-ttu-id="98ae2-129">Microsoft. Azure. Commands. CDN. Models. PSResourceUsage</span><span class="sxs-lookup"><span data-stu-id="98ae2-129">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span></span>

## <span data-ttu-id="98ae2-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="98ae2-130">NOTES</span></span>

## <span data-ttu-id="98ae2-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="98ae2-131">RELATED LINKS</span></span>

