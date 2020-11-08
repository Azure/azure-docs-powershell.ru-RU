---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnprofilesupportedoptimizationtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileSupportedOptimizationType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileSupportedOptimizationType.md
ms.openlocfilehash: db6520ae16d114fdcad85daf3e0742589fa0fbbe
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94064956"
---
# <span data-ttu-id="1f70a-101">Get-AzCdnProfileSupportedOptimizationType</span><span class="sxs-lookup"><span data-stu-id="1f70a-101">Get-AzCdnProfileSupportedOptimizationType</span></span>

## <span data-ttu-id="1f70a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1f70a-102">SYNOPSIS</span></span>
<span data-ttu-id="1f70a-103">Возвращает поддерживаемые типы оптимизации для профиля CDN.</span><span class="sxs-lookup"><span data-stu-id="1f70a-103">Gets the supported optimization types for a CDN profile.</span></span>

## <span data-ttu-id="1f70a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1f70a-104">SYNTAX</span></span>

### <span data-ttu-id="1f70a-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1f70a-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnProfileSupportedOptimizationType -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1f70a-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1f70a-106">ByObjectParameterSet</span></span>
```
Get-AzCdnProfileSupportedOptimizationType -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1f70a-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1f70a-107">DESCRIPTION</span></span>
<span data-ttu-id="1f70a-108">Командлет **Get-AzCdnProfileSupportedOptimizationType** получает Поддерживаемые типы оптимизации для текущего профиля.</span><span class="sxs-lookup"><span data-stu-id="1f70a-108">The **Get-AzCdnProfileSupportedOptimizationType** cmdlet gets the supported optimization types for the current profile.</span></span> <span data-ttu-id="1f70a-109">Пользователь может создать конечную точку с типом оптимизации из указанных значений.</span><span class="sxs-lookup"><span data-stu-id="1f70a-109">A user can create an endpoint with an optimization type from the listed values.</span></span>

## <span data-ttu-id="1f70a-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1f70a-110">EXAMPLES</span></span>

### <span data-ttu-id="1f70a-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1f70a-111">Example 1</span></span>
```powershell
PS C:\> Get-AzCdnProfileSupportedOptimizationType -ProfileName $profileName -ResourceGroupName $resourceGroupName
OptimizationType: GeneralWebDelivery
OptimizationType: DynamicSiteAcceleration
```

<span data-ttu-id="1f70a-112">Получите Поддерживаемые типы оптимизации для профиля CDN.</span><span class="sxs-lookup"><span data-stu-id="1f70a-112">Get the supported optimization types for a CDN profile.</span></span>

## <span data-ttu-id="1f70a-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1f70a-113">PARAMETERS</span></span>

### <span data-ttu-id="1f70a-114">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="1f70a-114">-CdnProfile</span></span>
<span data-ttu-id="1f70a-115">Объект профиля CDN в службе Azure.</span><span class="sxs-lookup"><span data-stu-id="1f70a-115">The Azure CDN profile object.</span></span>

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

### <span data-ttu-id="1f70a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f70a-116">-DefaultProfile</span></span>
<span data-ttu-id="1f70a-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1f70a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f70a-118">-Имя_профиля</span><span class="sxs-lookup"><span data-stu-id="1f70a-118">-ProfileName</span></span>
<span data-ttu-id="1f70a-119">Имя профиля.</span><span class="sxs-lookup"><span data-stu-id="1f70a-119">The name of the profile.</span></span>

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

### <span data-ttu-id="1f70a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f70a-120">-ResourceGroupName</span></span>
<span data-ttu-id="1f70a-121">Группа ресурсов, к которой относится профиль.</span><span class="sxs-lookup"><span data-stu-id="1f70a-121">The resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="1f70a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f70a-122">CommonParameters</span></span>
<span data-ttu-id="1f70a-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1f70a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f70a-124">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1f70a-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f70a-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1f70a-125">INPUTS</span></span>

### <span data-ttu-id="1f70a-126">Microsoft. Azure. Commands. CDN. Models. Profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="1f70a-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="1f70a-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1f70a-127">OUTPUTS</span></span>

### <span data-ttu-id="1f70a-128">Microsoft. Azure. Commands. CDN. Models. Profile. PSOptimizationType</span><span class="sxs-lookup"><span data-stu-id="1f70a-128">Microsoft.Azure.Commands.Cdn.Models.Profile.PSOptimizationType</span></span>

## <span data-ttu-id="1f70a-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="1f70a-129">NOTES</span></span>

## <span data-ttu-id="1f70a-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1f70a-130">RELATED LINKS</span></span>
