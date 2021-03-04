---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/powershell/module/az.cdn/get-azcdnprofileresourceusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileResourceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileResourceUsage.md
ms.openlocfilehash: 1a4e3f08653f6c7bda799b55618caff4e77fe7bd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004584"
---
# <span data-ttu-id="880ec-101">Get-AzCdnProfileResourceUsage</span><span class="sxs-lookup"><span data-stu-id="880ec-101">Get-AzCdnProfileResourceUsage</span></span>

## <span data-ttu-id="880ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="880ec-102">SYNOPSIS</span></span>
<span data-ttu-id="880ec-103">Возвращает использование ресурсов профиля CDN.</span><span class="sxs-lookup"><span data-stu-id="880ec-103">Gets the resource usage of a CDN profile.</span></span>

## <span data-ttu-id="880ec-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="880ec-104">SYNTAX</span></span>

### <span data-ttu-id="880ec-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="880ec-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnProfileResourceUsage -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="880ec-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="880ec-106">ByObjectParameterSet</span></span>
```
Get-AzCdnProfileResourceUsage -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="880ec-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="880ec-107">DESCRIPTION</span></span>
<span data-ttu-id="880ec-108">{{Fill in the Description}}</span><span class="sxs-lookup"><span data-stu-id="880ec-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="880ec-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="880ec-109">EXAMPLES</span></span>

### <span data-ttu-id="880ec-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="880ec-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="880ec-111">{{ Добавьте здесь описание примера }}</span><span class="sxs-lookup"><span data-stu-id="880ec-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="880ec-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="880ec-112">PARAMETERS</span></span>

### <span data-ttu-id="880ec-113">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="880ec-113">-CdnProfile</span></span>
<span data-ttu-id="880ec-114">Объект профиля CDN Azure.</span><span class="sxs-lookup"><span data-stu-id="880ec-114">The Azure CDN profile object.</span></span>

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

### <span data-ttu-id="880ec-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="880ec-115">-DefaultProfile</span></span>
<span data-ttu-id="880ec-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="880ec-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="880ec-117">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="880ec-117">-ProfileName</span></span>
<span data-ttu-id="880ec-118">Имя профиля.</span><span class="sxs-lookup"><span data-stu-id="880ec-118">The name of the profile.</span></span>

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

### <span data-ttu-id="880ec-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="880ec-119">-ResourceGroupName</span></span>
<span data-ttu-id="880ec-120">Группа ресурсов, к которой принадлежит профиль.</span><span class="sxs-lookup"><span data-stu-id="880ec-120">The resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="880ec-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="880ec-121">CommonParameters</span></span>
<span data-ttu-id="880ec-122">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="880ec-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="880ec-123">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="880ec-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="880ec-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="880ec-124">INPUTS</span></span>

### <span data-ttu-id="880ec-125">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span><span class="sxs-lookup"><span data-stu-id="880ec-125">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="880ec-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="880ec-126">OUTPUTS</span></span>

### <span data-ttu-id="880ec-127">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span><span class="sxs-lookup"><span data-stu-id="880ec-127">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span></span>

## <span data-ttu-id="880ec-128">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="880ec-128">NOTES</span></span>

## <span data-ttu-id="880ec-129">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="880ec-129">RELATED LINKS</span></span>
