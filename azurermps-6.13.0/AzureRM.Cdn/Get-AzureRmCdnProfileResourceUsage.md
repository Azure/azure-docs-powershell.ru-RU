---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/get-azurermcdnprofileresourceusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnProfileResourceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnProfileResourceUsage.md
ms.openlocfilehash: 3d0f93a732739b94832a5e411580fb80958b27c4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558495"
---
# <span data-ttu-id="b5365-101">Get-AzureRmCdnProfileResourceUsage</span><span class="sxs-lookup"><span data-stu-id="b5365-101">Get-AzureRmCdnProfileResourceUsage</span></span>

## <span data-ttu-id="b5365-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b5365-102">SYNOPSIS</span></span>
<span data-ttu-id="b5365-103">Возвращает данные об использовании ресурсов в профиле CDN.</span><span class="sxs-lookup"><span data-stu-id="b5365-103">Gets the resource usage of a CDN profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b5365-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b5365-104">SYNTAX</span></span>

### <span data-ttu-id="b5365-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b5365-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzureRmCdnProfileResourceUsage -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b5365-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b5365-106">ByObjectParameterSet</span></span>
```
Get-AzureRmCdnProfileResourceUsage -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b5365-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b5365-107">DESCRIPTION</span></span>
<span data-ttu-id="b5365-108">{Заполнение в описании}}</span><span class="sxs-lookup"><span data-stu-id="b5365-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="b5365-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b5365-109">EXAMPLES</span></span>

### <span data-ttu-id="b5365-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b5365-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="b5365-111">{{Добавить пример описания}}</span><span class="sxs-lookup"><span data-stu-id="b5365-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="b5365-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b5365-112">PARAMETERS</span></span>

### <span data-ttu-id="b5365-113">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="b5365-113">-CdnProfile</span></span>
<span data-ttu-id="b5365-114">Объект профиля CDN в службе Azure.</span><span class="sxs-lookup"><span data-stu-id="b5365-114">The Azure CDN profile object.</span></span>

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

### <span data-ttu-id="b5365-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5365-115">-DefaultProfile</span></span>
<span data-ttu-id="b5365-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="b5365-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b5365-117">-Имя_профиля</span><span class="sxs-lookup"><span data-stu-id="b5365-117">-ProfileName</span></span>
<span data-ttu-id="b5365-118">Имя профиля.</span><span class="sxs-lookup"><span data-stu-id="b5365-118">The name of the profile.</span></span>

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

### <span data-ttu-id="b5365-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5365-119">-ResourceGroupName</span></span>
<span data-ttu-id="b5365-120">Группа ресурсов, к которой относится профиль.</span><span class="sxs-lookup"><span data-stu-id="b5365-120">The resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="b5365-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5365-121">CommonParameters</span></span>
<span data-ttu-id="b5365-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b5365-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5365-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5365-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5365-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b5365-124">INPUTS</span></span>

### <span data-ttu-id="b5365-125">Microsoft. Azure. Commands. CDN. Models. Profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="b5365-125">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>
<span data-ttu-id="b5365-126">Параметры: CdnProfile (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b5365-126">Parameters: CdnProfile (ByValue)</span></span>

## <span data-ttu-id="b5365-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b5365-127">OUTPUTS</span></span>

### <span data-ttu-id="b5365-128">Microsoft. Azure. Commands. CDN. Models. PSResourceUsage</span><span class="sxs-lookup"><span data-stu-id="b5365-128">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span></span>

## <span data-ttu-id="b5365-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="b5365-129">NOTES</span></span>

## <span data-ttu-id="b5365-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b5365-130">RELATED LINKS</span></span>
