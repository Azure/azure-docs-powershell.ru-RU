---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnorigingroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnOriginGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnOriginGroup.md
ms.openlocfilehash: 98c41f8e9e1592cf0405f42701fc19f3badd9553
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98413391"
---
# <span data-ttu-id="6beb5-101">Get-AzCdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="6beb5-101">Get-AzCdnOriginGroup</span></span>

## <span data-ttu-id="6beb5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6beb5-102">SYNOPSIS</span></span>
<span data-ttu-id="6beb5-103">Возвращает группу источников CDN</span><span class="sxs-lookup"><span data-stu-id="6beb5-103">Gets a CDN origin group</span></span>

## <span data-ttu-id="6beb5-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6beb5-104">SYNTAX</span></span>

### <span data-ttu-id="6beb5-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6beb5-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnOriginGroup -EndpointName <String> -OriginGroupName <String> -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6beb5-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6beb5-106">ByResourceIdParameterSet</span></span>
```
Get-AzCdnOriginGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6beb5-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6beb5-107">DESCRIPTION</span></span>
<span data-ttu-id="6beb5-108">Новый Get-AzCdnOriginGroup извлекает группу источников CDN.</span><span class="sxs-lookup"><span data-stu-id="6beb5-108">The Get-AzCdnOriginGroup cmdlet retrieves a CDN origin group.</span></span>

## <span data-ttu-id="6beb5-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6beb5-109">EXAMPLES</span></span>

### <span data-ttu-id="6beb5-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6beb5-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCdnOriginGroup -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginGroupName $originGroupName
```

<span data-ttu-id="6beb5-111">Эта команда будет получать группу источника в указанной конечной точке.</span><span class="sxs-lookup"><span data-stu-id="6beb5-111">This command will get the origin group within the specified endpoint.</span></span>

## <span data-ttu-id="6beb5-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6beb5-112">PARAMETERS</span></span>

### <span data-ttu-id="6beb5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6beb5-113">-DefaultProfile</span></span>
<span data-ttu-id="6beb5-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6beb5-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6beb5-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="6beb5-115">-EndpointName</span></span>
<span data-ttu-id="6beb5-116">Имя конечной точки CDN Azure.</span><span class="sxs-lookup"><span data-stu-id="6beb5-116">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="6beb5-117">-OriginGroupName</span><span class="sxs-lookup"><span data-stu-id="6beb5-117">-OriginGroupName</span></span>
<span data-ttu-id="6beb5-118">Имя группы "Источник" в CDN Azure.</span><span class="sxs-lookup"><span data-stu-id="6beb5-118">Azure CDN origin group name.</span></span>

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

### <span data-ttu-id="6beb5-119">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="6beb5-119">-ProfileName</span></span>
<span data-ttu-id="6beb5-120">Имя профиля CDN Azure.</span><span class="sxs-lookup"><span data-stu-id="6beb5-120">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="6beb5-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6beb5-121">-ResourceGroupName</span></span>
<span data-ttu-id="6beb5-122">Группа ресурсов профиля Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="6beb5-122">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="6beb5-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6beb5-123">-ResourceId</span></span>
<span data-ttu-id="6beb5-124">ИД ресурса для группы источника</span><span class="sxs-lookup"><span data-stu-id="6beb5-124">Resource Id for the the origin group</span></span>

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

### <span data-ttu-id="6beb5-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6beb5-125">CommonParameters</span></span>
<span data-ttu-id="6beb5-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6beb5-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6beb5-127">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6beb5-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6beb5-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6beb5-128">INPUTS</span></span>

### <span data-ttu-id="6beb5-129">Нет</span><span class="sxs-lookup"><span data-stu-id="6beb5-129">None</span></span>

## <span data-ttu-id="6beb5-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6beb5-130">OUTPUTS</span></span>

### <span data-ttu-id="6beb5-131">System.Object</span><span class="sxs-lookup"><span data-stu-id="6beb5-131">System.Object</span></span>

## <span data-ttu-id="6beb5-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6beb5-132">NOTES</span></span>

## <span data-ttu-id="6beb5-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6beb5-133">RELATED LINKS</span></span>
