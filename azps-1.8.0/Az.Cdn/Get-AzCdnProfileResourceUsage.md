---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnprofileresourceusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileResourceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileResourceUsage.md
ms.openlocfilehash: d33cc54102d06b3bd57784880280b6e035fce18f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93731411"
---
# <span data-ttu-id="af0e5-101">Get-AzCdnProfileResourceUsage</span><span class="sxs-lookup"><span data-stu-id="af0e5-101">Get-AzCdnProfileResourceUsage</span></span>

## <span data-ttu-id="af0e5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="af0e5-102">SYNOPSIS</span></span>
<span data-ttu-id="af0e5-103">Возвращает данные об использовании ресурсов в профиле CDN.</span><span class="sxs-lookup"><span data-stu-id="af0e5-103">Gets the resource usage of a CDN profile.</span></span>

## <span data-ttu-id="af0e5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="af0e5-104">SYNTAX</span></span>

### <span data-ttu-id="af0e5-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="af0e5-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnProfileResourceUsage -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="af0e5-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="af0e5-106">ByObjectParameterSet</span></span>
```
Get-AzCdnProfileResourceUsage -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="af0e5-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="af0e5-107">DESCRIPTION</span></span>
<span data-ttu-id="af0e5-108">{Заполнение в описании}}</span><span class="sxs-lookup"><span data-stu-id="af0e5-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="af0e5-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="af0e5-109">EXAMPLES</span></span>

### <span data-ttu-id="af0e5-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="af0e5-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="af0e5-111">{{Добавить пример описания}}</span><span class="sxs-lookup"><span data-stu-id="af0e5-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="af0e5-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="af0e5-112">PARAMETERS</span></span>

### <span data-ttu-id="af0e5-113">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="af0e5-113">-CdnProfile</span></span>
<span data-ttu-id="af0e5-114">Объект профиля CDN в службе Azure.</span><span class="sxs-lookup"><span data-stu-id="af0e5-114">The Azure CDN profile object.</span></span>

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

### <span data-ttu-id="af0e5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af0e5-115">-DefaultProfile</span></span>
<span data-ttu-id="af0e5-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="af0e5-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="af0e5-117">-Имя_профиля</span><span class="sxs-lookup"><span data-stu-id="af0e5-117">-ProfileName</span></span>
<span data-ttu-id="af0e5-118">Имя профиля.</span><span class="sxs-lookup"><span data-stu-id="af0e5-118">The name of the profile.</span></span>

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

### <span data-ttu-id="af0e5-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af0e5-119">-ResourceGroupName</span></span>
<span data-ttu-id="af0e5-120">Группа ресурсов, к которой относится профиль.</span><span class="sxs-lookup"><span data-stu-id="af0e5-120">The resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="af0e5-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af0e5-121">CommonParameters</span></span>
<span data-ttu-id="af0e5-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="af0e5-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af0e5-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af0e5-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af0e5-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="af0e5-124">INPUTS</span></span>

### <span data-ttu-id="af0e5-125">Microsoft. Azure. Commands. CDN. Models. Profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="af0e5-125">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="af0e5-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="af0e5-126">OUTPUTS</span></span>

### <span data-ttu-id="af0e5-127">Microsoft. Azure. Commands. CDN. Models. PSResourceUsage</span><span class="sxs-lookup"><span data-stu-id="af0e5-127">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span></span>

## <span data-ttu-id="af0e5-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="af0e5-128">NOTES</span></span>

## <span data-ttu-id="af0e5-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="af0e5-129">RELATED LINKS</span></span>
