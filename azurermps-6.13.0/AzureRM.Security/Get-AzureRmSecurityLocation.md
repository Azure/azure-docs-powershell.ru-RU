---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityLocation.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityLocation.md
ms.openlocfilehash: 034681ad8ce4fbd30b10b959eda024f1a375c366
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558275"
---
# <span data-ttu-id="637d7-101">Get-AzureRmSecurityLocation</span><span class="sxs-lookup"><span data-stu-id="637d7-101">Get-AzureRmSecurityLocation</span></span>

## <span data-ttu-id="637d7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="637d7-102">SYNOPSIS</span></span>
<span data-ttu-id="637d7-103">Возвращает расположение, в котором центр безопасности Azure будет автоматически сохранять данные для конкретной подписки.</span><span class="sxs-lookup"><span data-stu-id="637d7-103">Gets the location where Azure Security Center will automatically save data for the specific subscription</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="637d7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="637d7-104">SYNTAX</span></span>

### <span data-ttu-id="637d7-105">SubscriptionScope (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="637d7-105">SubscriptionScope (Default)</span></span>
```
Get-AzureRmSecurityLocation [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="637d7-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="637d7-106">SubscriptionLevelResource</span></span>
```
Get-AzureRmSecurityLocation -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="637d7-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="637d7-107">ResourceId</span></span>
```
Get-AzureRmSecurityLocation -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="637d7-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="637d7-108">DESCRIPTION</span></span>
<span data-ttu-id="637d7-109">Центр безопасности Azure будет автоматически определять расположение для сохранения некоторых данных.</span><span class="sxs-lookup"><span data-stu-id="637d7-109">Azure Security Center will automatically decide on a location to save some of your data.</span></span>
<span data-ttu-id="637d7-110">Используйте этот командлет, чтобы найти это расположение.</span><span class="sxs-lookup"><span data-stu-id="637d7-110">Use this cmdlet to discover that location.</span></span>

## <span data-ttu-id="637d7-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="637d7-111">EXAMPLES</span></span>

### <span data-ttu-id="637d7-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="637d7-112">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmSecurityLocation
Id                                                                                                   Name
--                                                                                                   ----
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/locations/centralus centralus
```

<span data-ttu-id="637d7-113">Возвращает расположение, в котором центр безопасности Azure сохраняет вычисляемые данные безопасности.</span><span class="sxs-lookup"><span data-stu-id="637d7-113">Gets the location where Azure Security Center saves the calculated security data.</span></span>

## <span data-ttu-id="637d7-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="637d7-114">PARAMETERS</span></span>

### <span data-ttu-id="637d7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="637d7-115">-DefaultProfile</span></span>
<span data-ttu-id="637d7-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="637d7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="637d7-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="637d7-117">-Name</span></span>
<span data-ttu-id="637d7-118">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="637d7-118">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="637d7-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="637d7-119">-ResourceId</span></span>
<span data-ttu-id="637d7-120">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="637d7-120">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="637d7-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="637d7-121">CommonParameters</span></span>
<span data-ttu-id="637d7-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="637d7-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="637d7-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="637d7-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="637d7-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="637d7-124">INPUTS</span></span>

### <span data-ttu-id="637d7-125">System. String</span><span class="sxs-lookup"><span data-stu-id="637d7-125">System.String</span></span>

## <span data-ttu-id="637d7-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="637d7-126">OUTPUTS</span></span>

### <span data-ttu-id="637d7-127">Microsoft. Azure. Commands. Security. Models. местонахождения. PSSecurityLocation</span><span class="sxs-lookup"><span data-stu-id="637d7-127">Microsoft.Azure.Commands.Security.Models.Locations.PSSecurityLocation</span></span>

## <span data-ttu-id="637d7-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="637d7-128">NOTES</span></span>

## <span data-ttu-id="637d7-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="637d7-129">RELATED LINKS</span></span>
