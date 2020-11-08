---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnorigingroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnOriginGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnOriginGroup.md
ms.openlocfilehash: 98c41f8e9e1592cf0405f42701fc19f3badd9553
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249534"
---
# <span data-ttu-id="2b110-101">Get-AzCdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="2b110-101">Get-AzCdnOriginGroup</span></span>

## <span data-ttu-id="2b110-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2b110-102">SYNOPSIS</span></span>
<span data-ttu-id="2b110-103">Получает группу происхождения сети CDN</span><span class="sxs-lookup"><span data-stu-id="2b110-103">Gets a CDN origin group</span></span>

## <span data-ttu-id="2b110-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2b110-104">SYNTAX</span></span>

### <span data-ttu-id="2b110-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2b110-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnOriginGroup -EndpointName <String> -OriginGroupName <String> -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2b110-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2b110-106">ByResourceIdParameterSet</span></span>
```
Get-AzCdnOriginGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2b110-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2b110-107">DESCRIPTION</span></span>
<span data-ttu-id="2b110-108">Командлет Get-AzCdnOriginGroup извлекает группу источников сети CDN.</span><span class="sxs-lookup"><span data-stu-id="2b110-108">The Get-AzCdnOriginGroup cmdlet retrieves a CDN origin group.</span></span>

## <span data-ttu-id="2b110-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2b110-109">EXAMPLES</span></span>

### <span data-ttu-id="2b110-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2b110-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCdnOriginGroup -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginGroupName $originGroupName
```

<span data-ttu-id="2b110-111">Эта команда получит группу источника в указанной конечной точке.</span><span class="sxs-lookup"><span data-stu-id="2b110-111">This command will get the origin group within the specified endpoint.</span></span>

## <span data-ttu-id="2b110-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2b110-112">PARAMETERS</span></span>

### <span data-ttu-id="2b110-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b110-113">-DefaultProfile</span></span>
<span data-ttu-id="2b110-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2b110-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2b110-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="2b110-115">-EndpointName</span></span>
<span data-ttu-id="2b110-116">Имя конечной точки CDN Azure.</span><span class="sxs-lookup"><span data-stu-id="2b110-116">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="2b110-117">-OriginGroupName</span><span class="sxs-lookup"><span data-stu-id="2b110-117">-OriginGroupName</span></span>
<span data-ttu-id="2b110-118">Имя группы источника Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="2b110-118">Azure CDN origin group name.</span></span>

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

### <span data-ttu-id="2b110-119">-Имя_профиля</span><span class="sxs-lookup"><span data-stu-id="2b110-119">-ProfileName</span></span>
<span data-ttu-id="2b110-120">Имя профиля CDN в службе Azure.</span><span class="sxs-lookup"><span data-stu-id="2b110-120">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="2b110-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b110-121">-ResourceGroupName</span></span>
<span data-ttu-id="2b110-122">Группа ресурсов в профиле CDN для Azure.</span><span class="sxs-lookup"><span data-stu-id="2b110-122">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="2b110-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2b110-123">-ResourceId</span></span>
<span data-ttu-id="2b110-124">Идентификатор ресурса для начальной группы</span><span class="sxs-lookup"><span data-stu-id="2b110-124">Resource Id for the the origin group</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b110-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b110-125">CommonParameters</span></span>
<span data-ttu-id="2b110-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2b110-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b110-127">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2b110-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b110-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2b110-128">INPUTS</span></span>

### <span data-ttu-id="2b110-129">Ничего</span><span class="sxs-lookup"><span data-stu-id="2b110-129">None</span></span>

## <span data-ttu-id="2b110-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2b110-130">OUTPUTS</span></span>

### <span data-ttu-id="2b110-131">System. Object</span><span class="sxs-lookup"><span data-stu-id="2b110-131">System.Object</span></span>

## <span data-ttu-id="2b110-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="2b110-132">NOTES</span></span>

## <span data-ttu-id="2b110-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2b110-133">RELATED LINKS</span></span>
