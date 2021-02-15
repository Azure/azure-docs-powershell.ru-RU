---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnprofileresourceusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileResourceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileResourceUsage.md
ms.openlocfilehash: 8395fc4d90eb4e6d38eda18753761a1bf2598479
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100239126"
---
# <span data-ttu-id="bbcfa-101">Get-AzCdnProfileResourceUsage</span><span class="sxs-lookup"><span data-stu-id="bbcfa-101">Get-AzCdnProfileResourceUsage</span></span>

## <span data-ttu-id="bbcfa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bbcfa-102">SYNOPSIS</span></span>
<span data-ttu-id="bbcfa-103">Возвращает использование ресурсов профиля CDN.</span><span class="sxs-lookup"><span data-stu-id="bbcfa-103">Gets the resource usage of a CDN profile.</span></span>

## <span data-ttu-id="bbcfa-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="bbcfa-104">SYNTAX</span></span>

### <span data-ttu-id="bbcfa-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="bbcfa-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnProfileResourceUsage -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bbcfa-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bbcfa-106">ByObjectParameterSet</span></span>
```
Get-AzCdnProfileResourceUsage -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bbcfa-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bbcfa-107">DESCRIPTION</span></span>
<span data-ttu-id="bbcfa-108">{{Fill in the Description}}</span><span class="sxs-lookup"><span data-stu-id="bbcfa-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="bbcfa-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="bbcfa-109">EXAMPLES</span></span>

### <span data-ttu-id="bbcfa-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="bbcfa-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="bbcfa-111">{{ Добавьте здесь описание примера }}</span><span class="sxs-lookup"><span data-stu-id="bbcfa-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="bbcfa-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bbcfa-112">PARAMETERS</span></span>

### <span data-ttu-id="bbcfa-113">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="bbcfa-113">-CdnProfile</span></span>
<span data-ttu-id="bbcfa-114">Объект профиля CDN Azure.</span><span class="sxs-lookup"><span data-stu-id="bbcfa-114">The Azure CDN profile object.</span></span>

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

### <span data-ttu-id="bbcfa-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbcfa-115">-DefaultProfile</span></span>
<span data-ttu-id="bbcfa-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="bbcfa-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bbcfa-117">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="bbcfa-117">-ProfileName</span></span>
<span data-ttu-id="bbcfa-118">Имя профиля.</span><span class="sxs-lookup"><span data-stu-id="bbcfa-118">The name of the profile.</span></span>

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

### <span data-ttu-id="bbcfa-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bbcfa-119">-ResourceGroupName</span></span>
<span data-ttu-id="bbcfa-120">Группа ресурсов, к которой принадлежит профиль.</span><span class="sxs-lookup"><span data-stu-id="bbcfa-120">The resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="bbcfa-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbcfa-121">CommonParameters</span></span>
<span data-ttu-id="bbcfa-122">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bbcfa-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbcfa-123">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bbcfa-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbcfa-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bbcfa-124">INPUTS</span></span>

### <span data-ttu-id="bbcfa-125">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span><span class="sxs-lookup"><span data-stu-id="bbcfa-125">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="bbcfa-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="bbcfa-126">OUTPUTS</span></span>

### <span data-ttu-id="bbcfa-127">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span><span class="sxs-lookup"><span data-stu-id="bbcfa-127">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span></span>

## <span data-ttu-id="bbcfa-128">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="bbcfa-128">NOTES</span></span>

## <span data-ttu-id="bbcfa-129">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bbcfa-129">RELATED LINKS</span></span>
