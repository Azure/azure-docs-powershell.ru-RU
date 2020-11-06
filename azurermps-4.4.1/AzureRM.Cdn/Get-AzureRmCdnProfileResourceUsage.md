---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnProfileResourceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnProfileResourceUsage.md
ms.openlocfilehash: f8b85088ac05cb118cf443eb54f28508727bd335
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93570104"
---
# <span data-ttu-id="8c372-101">Get-AzureRmCdnProfileResourceUsage</span><span class="sxs-lookup"><span data-stu-id="8c372-101">Get-AzureRmCdnProfileResourceUsage</span></span>

## <span data-ttu-id="8c372-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8c372-102">SYNOPSIS</span></span>
<span data-ttu-id="8c372-103">{Заполнение кратких описаний}</span><span class="sxs-lookup"><span data-stu-id="8c372-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8c372-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8c372-104">SYNTAX</span></span>

### <span data-ttu-id="8c372-105">Параметры, заданные для параметров полей (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8c372-105">Parameter Set for fields parameters (Default)</span></span>
```
Get-AzureRmCdnProfileResourceUsage -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8c372-106">Параметр, заданный для параметров объекта</span><span class="sxs-lookup"><span data-stu-id="8c372-106">Parameter Set for object parameters</span></span>
```
Get-AzureRmCdnProfileResourceUsage -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8c372-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8c372-107">DESCRIPTION</span></span>
<span data-ttu-id="8c372-108">{Заполнение в описании}}</span><span class="sxs-lookup"><span data-stu-id="8c372-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="8c372-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8c372-109">EXAMPLES</span></span>

### <span data-ttu-id="8c372-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8c372-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="8c372-111">{{Добавить пример описания}}</span><span class="sxs-lookup"><span data-stu-id="8c372-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="8c372-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8c372-112">PARAMETERS</span></span>

### <span data-ttu-id="8c372-113">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="8c372-113">-CdnProfile</span></span>
<span data-ttu-id="8c372-114">Объект профиля CDN в службе Azure.</span><span class="sxs-lookup"><span data-stu-id="8c372-114">The Azure CDN profile object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile
Parameter Sets: Parameter Set for object parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8c372-115">-Имя_профиля</span><span class="sxs-lookup"><span data-stu-id="8c372-115">-ProfileName</span></span>
<span data-ttu-id="8c372-116">Имя профиля.</span><span class="sxs-lookup"><span data-stu-id="8c372-116">The name of the profile.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c372-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c372-117">-ResourceGroupName</span></span>
<span data-ttu-id="8c372-118">Группа ресурсов, к которой относится профиль.</span><span class="sxs-lookup"><span data-stu-id="8c372-118">The resource group to which the profile belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c372-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c372-119">-DefaultProfile</span></span>
<span data-ttu-id="8c372-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8c372-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8c372-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c372-121">CommonParameters</span></span>
<span data-ttu-id="8c372-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8c372-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c372-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c372-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c372-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8c372-124">INPUTS</span></span>

### <span data-ttu-id="8c372-125">Microsoft. Azure. Commands. CDN. Models. Profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="8c372-125">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="8c372-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8c372-126">OUTPUTS</span></span>

### <span data-ttu-id="8c372-127">Microsoft. Azure. Commands. CDN. Models. PSResourceUsage</span><span class="sxs-lookup"><span data-stu-id="8c372-127">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span></span>

## <span data-ttu-id="8c372-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="8c372-128">NOTES</span></span>

## <span data-ttu-id="8c372-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8c372-129">RELATED LINKS</span></span>

