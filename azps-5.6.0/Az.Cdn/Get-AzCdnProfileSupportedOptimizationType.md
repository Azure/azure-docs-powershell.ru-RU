---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/powershell/module/az.cdn/get-azcdnprofilesupportedoptimizationtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileSupportedOptimizationType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileSupportedOptimizationType.md
ms.openlocfilehash: f26e1bd19b9856df7bf68de6c8afddefb3ee64a0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988487"
---
# <span data-ttu-id="75a24-101">Get-AzCdnProfileSupportedOptimizationType</span><span class="sxs-lookup"><span data-stu-id="75a24-101">Get-AzCdnProfileSupportedOptimizationType</span></span>

## <span data-ttu-id="75a24-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75a24-102">SYNOPSIS</span></span>
<span data-ttu-id="75a24-103">Возвращает поддерживаемые типы оптимизации для профиля CDN.</span><span class="sxs-lookup"><span data-stu-id="75a24-103">Gets the supported optimization types for a CDN profile.</span></span>

## <span data-ttu-id="75a24-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="75a24-104">SYNTAX</span></span>

### <span data-ttu-id="75a24-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="75a24-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnProfileSupportedOptimizationType -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75a24-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="75a24-106">ByObjectParameterSet</span></span>
```
Get-AzCdnProfileSupportedOptimizationType -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="75a24-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="75a24-107">DESCRIPTION</span></span>
<span data-ttu-id="75a24-108">Для текущего профиля поддерживаются типы оптимизации для **get-AzCdnProfileSupportedOptimizationType.**</span><span class="sxs-lookup"><span data-stu-id="75a24-108">The **Get-AzCdnProfileSupportedOptimizationType** cmdlet gets the supported optimization types for the current profile.</span></span> <span data-ttu-id="75a24-109">Пользователь может создать конечную точку с типом оптимизации из перечисленных значений.</span><span class="sxs-lookup"><span data-stu-id="75a24-109">A user can create an endpoint with an optimization type from the listed values.</span></span>

## <span data-ttu-id="75a24-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="75a24-110">EXAMPLES</span></span>

### <span data-ttu-id="75a24-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="75a24-111">Example 1</span></span>
```powershell
PS C:\> Get-AzCdnProfileSupportedOptimizationType -ProfileName $profileName -ResourceGroupName $resourceGroupName
OptimizationType: GeneralWebDelivery
OptimizationType: DynamicSiteAcceleration
```

<span data-ttu-id="75a24-112">Получите поддерживаемые типы оптимизации для профиля CDN.</span><span class="sxs-lookup"><span data-stu-id="75a24-112">Get the supported optimization types for a CDN profile.</span></span>

## <span data-ttu-id="75a24-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="75a24-113">PARAMETERS</span></span>

### <span data-ttu-id="75a24-114">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="75a24-114">-CdnProfile</span></span>
<span data-ttu-id="75a24-115">Объект профиля CDN Azure.</span><span class="sxs-lookup"><span data-stu-id="75a24-115">The Azure CDN profile object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="75a24-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75a24-116">-DefaultProfile</span></span>
<span data-ttu-id="75a24-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="75a24-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75a24-118">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="75a24-118">-ProfileName</span></span>
<span data-ttu-id="75a24-119">Имя профиля.</span><span class="sxs-lookup"><span data-stu-id="75a24-119">The name of the profile.</span></span>

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

### <span data-ttu-id="75a24-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75a24-120">-ResourceGroupName</span></span>
<span data-ttu-id="75a24-121">Группа ресурсов, к которой принадлежит профиль.</span><span class="sxs-lookup"><span data-stu-id="75a24-121">The resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="75a24-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75a24-122">CommonParameters</span></span>
<span data-ttu-id="75a24-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75a24-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75a24-124">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="75a24-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75a24-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="75a24-125">INPUTS</span></span>

### <span data-ttu-id="75a24-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span><span class="sxs-lookup"><span data-stu-id="75a24-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="75a24-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="75a24-127">OUTPUTS</span></span>

### <span data-ttu-id="75a24-128">Microsoft.Azure.Commands.Cdn.Models.Profile.PSOptimizationType</span><span class="sxs-lookup"><span data-stu-id="75a24-128">Microsoft.Azure.Commands.Cdn.Models.Profile.PSOptimizationType</span></span>

## <span data-ttu-id="75a24-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="75a24-129">NOTES</span></span>

## <span data-ttu-id="75a24-130">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="75a24-130">RELATED LINKS</span></span>
