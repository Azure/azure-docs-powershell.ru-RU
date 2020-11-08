---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnprofilesupportedoptimizationtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileSupportedOptimizationType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileSupportedOptimizationType.md
ms.openlocfilehash: db6520ae16d114fdcad85daf3e0742589fa0fbbe
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249524"
---
# <span data-ttu-id="c587c-101">Get-AzCdnProfileSupportedOptimizationType</span><span class="sxs-lookup"><span data-stu-id="c587c-101">Get-AzCdnProfileSupportedOptimizationType</span></span>

## <span data-ttu-id="c587c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c587c-102">SYNOPSIS</span></span>
<span data-ttu-id="c587c-103">Возвращает поддерживаемые типы оптимизации для профиля CDN.</span><span class="sxs-lookup"><span data-stu-id="c587c-103">Gets the supported optimization types for a CDN profile.</span></span>

## <span data-ttu-id="c587c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c587c-104">SYNTAX</span></span>

### <span data-ttu-id="c587c-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c587c-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnProfileSupportedOptimizationType -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c587c-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c587c-106">ByObjectParameterSet</span></span>
```
Get-AzCdnProfileSupportedOptimizationType -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c587c-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c587c-107">DESCRIPTION</span></span>
<span data-ttu-id="c587c-108">Командлет **Get-AzCdnProfileSupportedOptimizationType** получает Поддерживаемые типы оптимизации для текущего профиля.</span><span class="sxs-lookup"><span data-stu-id="c587c-108">The **Get-AzCdnProfileSupportedOptimizationType** cmdlet gets the supported optimization types for the current profile.</span></span> <span data-ttu-id="c587c-109">Пользователь может создать конечную точку с типом оптимизации из указанных значений.</span><span class="sxs-lookup"><span data-stu-id="c587c-109">A user can create an endpoint with an optimization type from the listed values.</span></span>

## <span data-ttu-id="c587c-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c587c-110">EXAMPLES</span></span>

### <span data-ttu-id="c587c-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c587c-111">Example 1</span></span>
```powershell
PS C:\> Get-AzCdnProfileSupportedOptimizationType -ProfileName $profileName -ResourceGroupName $resourceGroupName
OptimizationType: GeneralWebDelivery
OptimizationType: DynamicSiteAcceleration
```

<span data-ttu-id="c587c-112">Получите Поддерживаемые типы оптимизации для профиля CDN.</span><span class="sxs-lookup"><span data-stu-id="c587c-112">Get the supported optimization types for a CDN profile.</span></span>

## <span data-ttu-id="c587c-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c587c-113">PARAMETERS</span></span>

### <span data-ttu-id="c587c-114">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="c587c-114">-CdnProfile</span></span>
<span data-ttu-id="c587c-115">Объект профиля CDN в службе Azure.</span><span class="sxs-lookup"><span data-stu-id="c587c-115">The Azure CDN profile object.</span></span>

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

### <span data-ttu-id="c587c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c587c-116">-DefaultProfile</span></span>
<span data-ttu-id="c587c-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c587c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c587c-118">-Имя_профиля</span><span class="sxs-lookup"><span data-stu-id="c587c-118">-ProfileName</span></span>
<span data-ttu-id="c587c-119">Имя профиля.</span><span class="sxs-lookup"><span data-stu-id="c587c-119">The name of the profile.</span></span>

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

### <span data-ttu-id="c587c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c587c-120">-ResourceGroupName</span></span>
<span data-ttu-id="c587c-121">Группа ресурсов, к которой относится профиль.</span><span class="sxs-lookup"><span data-stu-id="c587c-121">The resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="c587c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c587c-122">CommonParameters</span></span>
<span data-ttu-id="c587c-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c587c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c587c-124">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c587c-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c587c-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c587c-125">INPUTS</span></span>

### <span data-ttu-id="c587c-126">Microsoft. Azure. Commands. CDN. Models. Profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="c587c-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="c587c-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c587c-127">OUTPUTS</span></span>

### <span data-ttu-id="c587c-128">Microsoft. Azure. Commands. CDN. Models. Profile. PSOptimizationType</span><span class="sxs-lookup"><span data-stu-id="c587c-128">Microsoft.Azure.Commands.Cdn.Models.Profile.PSOptimizationType</span></span>

## <span data-ttu-id="c587c-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="c587c-129">NOTES</span></span>

## <span data-ttu-id="c587c-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c587c-130">RELATED LINKS</span></span>
