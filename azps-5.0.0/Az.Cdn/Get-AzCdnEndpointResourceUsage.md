---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnendpointresourceusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpointResourceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpointResourceUsage.md
ms.openlocfilehash: 7b8773f4e8e0f63404d81c56703181124f6f8ad0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249538"
---
# <span data-ttu-id="41b70-101">Get-AzCdnEndpointResourceUsage</span><span class="sxs-lookup"><span data-stu-id="41b70-101">Get-AzCdnEndpointResourceUsage</span></span>

## <span data-ttu-id="41b70-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="41b70-102">SYNOPSIS</span></span>
<span data-ttu-id="41b70-103">Получает использование ресурсов конечной точки CDN.</span><span class="sxs-lookup"><span data-stu-id="41b70-103">Gets the resource usage of a CDN endpoint.</span></span>

## <span data-ttu-id="41b70-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="41b70-104">SYNTAX</span></span>

### <span data-ttu-id="41b70-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="41b70-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnEndpointResourceUsage [-EndpointName <String>] -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="41b70-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="41b70-106">ByObjectParameterSet</span></span>
```
Get-AzCdnEndpointResourceUsage [-EndpointName <String>] -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="41b70-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="41b70-107">DESCRIPTION</span></span>
<span data-ttu-id="41b70-108">{Заполнение в описании}}</span><span class="sxs-lookup"><span data-stu-id="41b70-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="41b70-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="41b70-109">EXAMPLES</span></span>

### <span data-ttu-id="41b70-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="41b70-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="41b70-111">{{Добавить пример описания}}</span><span class="sxs-lookup"><span data-stu-id="41b70-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="41b70-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="41b70-112">PARAMETERS</span></span>

### <span data-ttu-id="41b70-113">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="41b70-113">-CdnEndpoint</span></span>
<span data-ttu-id="41b70-114">Объект конечной точки CDN.</span><span class="sxs-lookup"><span data-stu-id="41b70-114">The CDN endpoint object.</span></span>

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

### <span data-ttu-id="41b70-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41b70-115">-DefaultProfile</span></span>
<span data-ttu-id="41b70-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="41b70-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="41b70-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="41b70-117">-EndpointName</span></span>
<span data-ttu-id="41b70-118">Имя конечной точки CDN Azure.</span><span class="sxs-lookup"><span data-stu-id="41b70-118">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="41b70-119">-Имя_профиля</span><span class="sxs-lookup"><span data-stu-id="41b70-119">-ProfileName</span></span>
<span data-ttu-id="41b70-120">Имя профиля CDN в службе Azure.</span><span class="sxs-lookup"><span data-stu-id="41b70-120">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="41b70-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41b70-121">-ResourceGroupName</span></span>
<span data-ttu-id="41b70-122">Группа ресурсов в профиле CDN для Azure.</span><span class="sxs-lookup"><span data-stu-id="41b70-122">The resource group of the Azure CDN Profile.</span></span>

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

### <span data-ttu-id="41b70-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41b70-123">CommonParameters</span></span>
<span data-ttu-id="41b70-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="41b70-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41b70-125">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="41b70-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41b70-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="41b70-126">INPUTS</span></span>

### <span data-ttu-id="41b70-127">Microsoft. Azure. Commands. CDN. Models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="41b70-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="41b70-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="41b70-128">OUTPUTS</span></span>

### <span data-ttu-id="41b70-129">Microsoft. Azure. Commands. CDN. Models. PSResourceUsage</span><span class="sxs-lookup"><span data-stu-id="41b70-129">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span></span>

## <span data-ttu-id="41b70-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="41b70-130">NOTES</span></span>

## <span data-ttu-id="41b70-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="41b70-131">RELATED LINKS</span></span>