---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/get-azurermcdnprofilesupportedoptimizationtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnProfileSupportedOptimizationType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnProfileSupportedOptimizationType.md
ms.openlocfilehash: e6434b2b5b07cad811f245d72e1d6bd34da63bb4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567299"
---
# <span data-ttu-id="c2f18-101">Get-AzureRmCdnProfileSupportedOptimizationType</span><span class="sxs-lookup"><span data-stu-id="c2f18-101">Get-AzureRmCdnProfileSupportedOptimizationType</span></span>

## <span data-ttu-id="c2f18-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c2f18-102">SYNOPSIS</span></span>
<span data-ttu-id="c2f18-103">Возвращает поддерживаемые типы оптимизации для профиля CDN.</span><span class="sxs-lookup"><span data-stu-id="c2f18-103">Gets the supported optimization types for a CDN profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c2f18-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c2f18-104">SYNTAX</span></span>

### <span data-ttu-id="c2f18-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c2f18-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzureRmCdnProfileSupportedOptimizationType -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2f18-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2f18-106">ByObjectParameterSet</span></span>
```
Get-AzureRmCdnProfileSupportedOptimizationType -CdnProfile <PSProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c2f18-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c2f18-107">DESCRIPTION</span></span>
<span data-ttu-id="c2f18-108">Командлет **Get-AzureRmCdnProfileSupportedOptimizationType** получает Поддерживаемые типы оптимизации для текущего профиля.</span><span class="sxs-lookup"><span data-stu-id="c2f18-108">The **Get-AzureRmCdnProfileSupportedOptimizationType** cmdlet gets the supported optimization types for the current profile.</span></span> <span data-ttu-id="c2f18-109">Пользователь может создать конечную точку с типом оптимизации из указанных значений.</span><span class="sxs-lookup"><span data-stu-id="c2f18-109">A user can create an endpoint with an optimization type from the listed values.</span></span>

## <span data-ttu-id="c2f18-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c2f18-110">EXAMPLES</span></span>

### <span data-ttu-id="c2f18-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c2f18-111">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmCdnProfileSupportedOptimizationType -ProfileName $profileName -ResourceGroupName $resourceGroupName
OptimizationType: GeneralWebDelivery
OptimizationType: DynamicSiteAcceleration
```

<span data-ttu-id="c2f18-112">Получите Поддерживаемые типы оптимизации для профиля CDN.</span><span class="sxs-lookup"><span data-stu-id="c2f18-112">Get the supported optimization types for a CDN profile.</span></span>

## <span data-ttu-id="c2f18-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c2f18-113">PARAMETERS</span></span>

### <span data-ttu-id="c2f18-114">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="c2f18-114">-CdnProfile</span></span>
<span data-ttu-id="c2f18-115">Объект профиля CDN в службе Azure.</span><span class="sxs-lookup"><span data-stu-id="c2f18-115">The Azure CDN profile object.</span></span>

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

### <span data-ttu-id="c2f18-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2f18-116">-DefaultProfile</span></span>
<span data-ttu-id="c2f18-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c2f18-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2f18-118">-Имя_профиля</span><span class="sxs-lookup"><span data-stu-id="c2f18-118">-ProfileName</span></span>
<span data-ttu-id="c2f18-119">Имя профиля.</span><span class="sxs-lookup"><span data-stu-id="c2f18-119">The name of the profile.</span></span>

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

### <span data-ttu-id="c2f18-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2f18-120">-ResourceGroupName</span></span>
<span data-ttu-id="c2f18-121">Группа ресурсов, к которой относится профиль.</span><span class="sxs-lookup"><span data-stu-id="c2f18-121">The resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="c2f18-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2f18-122">CommonParameters</span></span>
<span data-ttu-id="c2f18-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c2f18-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2f18-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2f18-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2f18-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c2f18-125">INPUTS</span></span>

### <span data-ttu-id="c2f18-126">Microsoft. Azure. Commands. CDN. Models. Profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="c2f18-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>
<span data-ttu-id="c2f18-127">Параметры: CdnProfile (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c2f18-127">Parameters: CdnProfile (ByValue)</span></span>

## <span data-ttu-id="c2f18-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c2f18-128">OUTPUTS</span></span>

### <span data-ttu-id="c2f18-129">Microsoft. Azure. Commands. CDN. Models. Profile. PSOptimizationType</span><span class="sxs-lookup"><span data-stu-id="c2f18-129">Microsoft.Azure.Commands.Cdn.Models.Profile.PSOptimizationType</span></span>

## <span data-ttu-id="c2f18-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="c2f18-130">NOTES</span></span>

## <span data-ttu-id="c2f18-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c2f18-131">RELATED LINKS</span></span>
