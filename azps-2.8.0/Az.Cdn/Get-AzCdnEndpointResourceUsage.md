---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnendpointresourceusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpointResourceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpointResourceUsage.md
ms.openlocfilehash: 28f285ef55acbca3c4226f198f69fb9a70b62364
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93727608"
---
# <span data-ttu-id="62709-101">Get-AzCdnEndpointResourceUsage</span><span class="sxs-lookup"><span data-stu-id="62709-101">Get-AzCdnEndpointResourceUsage</span></span>

## <span data-ttu-id="62709-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="62709-102">SYNOPSIS</span></span>
<span data-ttu-id="62709-103">Получает использование ресурсов конечной точки CDN.</span><span class="sxs-lookup"><span data-stu-id="62709-103">Gets the resource usage of a CDN endpoint.</span></span>

## <span data-ttu-id="62709-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="62709-104">SYNTAX</span></span>

### <span data-ttu-id="62709-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="62709-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnEndpointResourceUsage [-EndpointName <String>] -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="62709-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="62709-106">ByObjectParameterSet</span></span>
```
Get-AzCdnEndpointResourceUsage [-EndpointName <String>] -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="62709-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="62709-107">DESCRIPTION</span></span>
<span data-ttu-id="62709-108">{Заполнение в описании}}</span><span class="sxs-lookup"><span data-stu-id="62709-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="62709-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="62709-109">EXAMPLES</span></span>

### <span data-ttu-id="62709-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="62709-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="62709-111">{{Добавить пример описания}}</span><span class="sxs-lookup"><span data-stu-id="62709-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="62709-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="62709-112">PARAMETERS</span></span>

### <span data-ttu-id="62709-113">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="62709-113">-CdnEndpoint</span></span>
<span data-ttu-id="62709-114">Объект конечной точки CDN.</span><span class="sxs-lookup"><span data-stu-id="62709-114">The CDN endpoint object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="62709-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62709-115">-DefaultProfile</span></span>
<span data-ttu-id="62709-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="62709-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62709-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="62709-117">-EndpointName</span></span>
<span data-ttu-id="62709-118">Имя конечной точки CDN Azure.</span><span class="sxs-lookup"><span data-stu-id="62709-118">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="62709-119">-Имя_профиля</span><span class="sxs-lookup"><span data-stu-id="62709-119">-ProfileName</span></span>
<span data-ttu-id="62709-120">Имя профиля CDN в службе Azure.</span><span class="sxs-lookup"><span data-stu-id="62709-120">Azure CDN profile name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62709-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62709-121">-ResourceGroupName</span></span>
<span data-ttu-id="62709-122">Группа ресурсов в профиле CDN для Azure.</span><span class="sxs-lookup"><span data-stu-id="62709-122">The resource group of the Azure CDN Profile.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62709-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62709-123">CommonParameters</span></span>
<span data-ttu-id="62709-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="62709-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62709-125">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="62709-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62709-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="62709-126">INPUTS</span></span>

### <span data-ttu-id="62709-127">Microsoft. Azure. Commands. CDN. Models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="62709-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="62709-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="62709-128">OUTPUTS</span></span>

### <span data-ttu-id="62709-129">Microsoft. Azure. Commands. CDN. Models. PSResourceUsage</span><span class="sxs-lookup"><span data-stu-id="62709-129">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span></span>

## <span data-ttu-id="62709-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="62709-130">NOTES</span></span>

## <span data-ttu-id="62709-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="62709-131">RELATED LINKS</span></span>
