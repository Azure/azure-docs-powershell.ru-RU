---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnprofilesupportedoptimizationtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileSupportedOptimizationType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileSupportedOptimizationType.md
ms.openlocfilehash: db6520ae16d114fdcad85daf3e0742589fa0fbbe
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98509385"
---
# <span data-ttu-id="7288b-101">Get-AzCdnProfileSupportedOptimizationType</span><span class="sxs-lookup"><span data-stu-id="7288b-101">Get-AzCdnProfileSupportedOptimizationType</span></span>

## <span data-ttu-id="7288b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7288b-102">SYNOPSIS</span></span>
<span data-ttu-id="7288b-103">Возвращает поддерживаемые типы оптимизации для профиля CDN.</span><span class="sxs-lookup"><span data-stu-id="7288b-103">Gets the supported optimization types for a CDN profile.</span></span>

## <span data-ttu-id="7288b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7288b-104">SYNTAX</span></span>

### <span data-ttu-id="7288b-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7288b-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnProfileSupportedOptimizationType -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7288b-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7288b-106">ByObjectParameterSet</span></span>
```
Get-AzCdnProfileSupportedOptimizationType -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7288b-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7288b-107">DESCRIPTION</span></span>
<span data-ttu-id="7288b-108">Для текущего профиля поддерживаются типы оптимизации для **get-AzCdnProfileSupportedOptimizationType.**</span><span class="sxs-lookup"><span data-stu-id="7288b-108">The **Get-AzCdnProfileSupportedOptimizationType** cmdlet gets the supported optimization types for the current profile.</span></span> <span data-ttu-id="7288b-109">Пользователь может создать конечную точку с типом оптимизации из перечисленных значений.</span><span class="sxs-lookup"><span data-stu-id="7288b-109">A user can create an endpoint with an optimization type from the listed values.</span></span>

## <span data-ttu-id="7288b-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7288b-110">EXAMPLES</span></span>

### <span data-ttu-id="7288b-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7288b-111">Example 1</span></span>
```powershell
PS C:\> Get-AzCdnProfileSupportedOptimizationType -ProfileName $profileName -ResourceGroupName $resourceGroupName
OptimizationType: GeneralWebDelivery
OptimizationType: DynamicSiteAcceleration
```

<span data-ttu-id="7288b-112">Получите поддерживаемые типы оптимизации для профиля CDN.</span><span class="sxs-lookup"><span data-stu-id="7288b-112">Get the supported optimization types for a CDN profile.</span></span>

## <span data-ttu-id="7288b-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7288b-113">PARAMETERS</span></span>

### <span data-ttu-id="7288b-114">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="7288b-114">-CdnProfile</span></span>
<span data-ttu-id="7288b-115">Объект профиля CDN Azure.</span><span class="sxs-lookup"><span data-stu-id="7288b-115">The Azure CDN profile object.</span></span>

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

### <span data-ttu-id="7288b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7288b-116">-DefaultProfile</span></span>
<span data-ttu-id="7288b-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7288b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7288b-118">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="7288b-118">-ProfileName</span></span>
<span data-ttu-id="7288b-119">Имя профиля.</span><span class="sxs-lookup"><span data-stu-id="7288b-119">The name of the profile.</span></span>

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

### <span data-ttu-id="7288b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7288b-120">-ResourceGroupName</span></span>
<span data-ttu-id="7288b-121">Группа ресурсов, к которой принадлежит профиль.</span><span class="sxs-lookup"><span data-stu-id="7288b-121">The resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="7288b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7288b-122">CommonParameters</span></span>
<span data-ttu-id="7288b-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7288b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7288b-124">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7288b-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7288b-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7288b-125">INPUTS</span></span>

### <span data-ttu-id="7288b-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span><span class="sxs-lookup"><span data-stu-id="7288b-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="7288b-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7288b-127">OUTPUTS</span></span>

### <span data-ttu-id="7288b-128">Microsoft.Azure.Commands.Cdn.Models.Profile.PSOptimizationType</span><span class="sxs-lookup"><span data-stu-id="7288b-128">Microsoft.Azure.Commands.Cdn.Models.Profile.PSOptimizationType</span></span>

## <span data-ttu-id="7288b-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7288b-129">NOTES</span></span>

## <span data-ttu-id="7288b-130">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7288b-130">RELATED LINKS</span></span>
