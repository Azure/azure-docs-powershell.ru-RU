---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnorigingroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnOriginGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnOriginGroup.md
ms.openlocfilehash: 98c41f8e9e1592cf0405f42701fc19f3badd9553
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98509381"
---
# <span data-ttu-id="c02ea-101">Get-AzCdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="c02ea-101">Get-AzCdnOriginGroup</span></span>

## <span data-ttu-id="c02ea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c02ea-102">SYNOPSIS</span></span>
<span data-ttu-id="c02ea-103">Возвращает группу источников CDN</span><span class="sxs-lookup"><span data-stu-id="c02ea-103">Gets a CDN origin group</span></span>

## <span data-ttu-id="c02ea-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c02ea-104">SYNTAX</span></span>

### <span data-ttu-id="c02ea-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c02ea-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnOriginGroup -EndpointName <String> -OriginGroupName <String> -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c02ea-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c02ea-106">ByResourceIdParameterSet</span></span>
```
Get-AzCdnOriginGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c02ea-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c02ea-107">DESCRIPTION</span></span>
<span data-ttu-id="c02ea-108">Новый Get-AzCdnOriginGroup извлекает группу источников CDN.</span><span class="sxs-lookup"><span data-stu-id="c02ea-108">The Get-AzCdnOriginGroup cmdlet retrieves a CDN origin group.</span></span>

## <span data-ttu-id="c02ea-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c02ea-109">EXAMPLES</span></span>

### <span data-ttu-id="c02ea-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c02ea-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCdnOriginGroup -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginGroupName $originGroupName
```

<span data-ttu-id="c02ea-111">Эта команда будет получать группу источника в указанной конечной точке.</span><span class="sxs-lookup"><span data-stu-id="c02ea-111">This command will get the origin group within the specified endpoint.</span></span>

## <span data-ttu-id="c02ea-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c02ea-112">PARAMETERS</span></span>

### <span data-ttu-id="c02ea-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c02ea-113">-DefaultProfile</span></span>
<span data-ttu-id="c02ea-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c02ea-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c02ea-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="c02ea-115">-EndpointName</span></span>
<span data-ttu-id="c02ea-116">Имя конечной точки CDN Azure.</span><span class="sxs-lookup"><span data-stu-id="c02ea-116">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="c02ea-117">-OriginGroupName</span><span class="sxs-lookup"><span data-stu-id="c02ea-117">-OriginGroupName</span></span>
<span data-ttu-id="c02ea-118">Имя группы источников Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="c02ea-118">Azure CDN origin group name.</span></span>

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

### <span data-ttu-id="c02ea-119">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="c02ea-119">-ProfileName</span></span>
<span data-ttu-id="c02ea-120">Имя профиля CDN Azure.</span><span class="sxs-lookup"><span data-stu-id="c02ea-120">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="c02ea-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c02ea-121">-ResourceGroupName</span></span>
<span data-ttu-id="c02ea-122">Группа ресурсов профиля AZURE CDN.</span><span class="sxs-lookup"><span data-stu-id="c02ea-122">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="c02ea-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c02ea-123">-ResourceId</span></span>
<span data-ttu-id="c02ea-124">ИД ресурса для группы источника</span><span class="sxs-lookup"><span data-stu-id="c02ea-124">Resource Id for the the origin group</span></span>

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

### <span data-ttu-id="c02ea-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c02ea-125">CommonParameters</span></span>
<span data-ttu-id="c02ea-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c02ea-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c02ea-127">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c02ea-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c02ea-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c02ea-128">INPUTS</span></span>

### <span data-ttu-id="c02ea-129">Нет</span><span class="sxs-lookup"><span data-stu-id="c02ea-129">None</span></span>

## <span data-ttu-id="c02ea-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c02ea-130">OUTPUTS</span></span>

### <span data-ttu-id="c02ea-131">System.Object</span><span class="sxs-lookup"><span data-stu-id="c02ea-131">System.Object</span></span>

## <span data-ttu-id="c02ea-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c02ea-132">NOTES</span></span>

## <span data-ttu-id="c02ea-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c02ea-133">RELATED LINKS</span></span>
