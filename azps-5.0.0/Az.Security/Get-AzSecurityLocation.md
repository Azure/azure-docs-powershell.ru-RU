---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityLocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityLocation.md
ms.openlocfilehash: 77f9283b16aa605da066780165c2fe7b42b1830b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94317597"
---
# <span data-ttu-id="fa788-101">Get-AzSecurityLocation</span><span class="sxs-lookup"><span data-stu-id="fa788-101">Get-AzSecurityLocation</span></span>

## <span data-ttu-id="fa788-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fa788-102">SYNOPSIS</span></span>
<span data-ttu-id="fa788-103">Возвращает расположение, в котором центр безопасности Azure будет автоматически сохранять данные для конкретной подписки.</span><span class="sxs-lookup"><span data-stu-id="fa788-103">Gets the location where Azure Security Center will automatically save data for the specific subscription</span></span>

## <span data-ttu-id="fa788-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fa788-104">SYNTAX</span></span>

### <span data-ttu-id="fa788-105">SubscriptionScope (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fa788-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityLocation [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fa788-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="fa788-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityLocation -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fa788-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="fa788-107">ResourceId</span></span>
```
Get-AzSecurityLocation -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fa788-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fa788-108">DESCRIPTION</span></span>
<span data-ttu-id="fa788-109">Центр безопасности Azure будет автоматически определять расположение для сохранения некоторых данных.</span><span class="sxs-lookup"><span data-stu-id="fa788-109">Azure Security Center will automatically decide on a location to save some of your data.</span></span>
<span data-ttu-id="fa788-110">Используйте этот командлет, чтобы найти это расположение.</span><span class="sxs-lookup"><span data-stu-id="fa788-110">Use this cmdlet to discover that location.</span></span>

## <span data-ttu-id="fa788-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fa788-111">EXAMPLES</span></span>

### <span data-ttu-id="fa788-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="fa788-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityLocation
Id                                                                                                   Name
--                                                                                                   ----
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/locations/centralus centralus
```

<span data-ttu-id="fa788-113">Возвращает расположение, в котором центр безопасности Azure сохраняет вычисляемые данные безопасности.</span><span class="sxs-lookup"><span data-stu-id="fa788-113">Gets the location where Azure Security Center saves the calculated security data.</span></span>

## <span data-ttu-id="fa788-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fa788-114">PARAMETERS</span></span>

### <span data-ttu-id="fa788-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa788-115">-DefaultProfile</span></span>
<span data-ttu-id="fa788-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fa788-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fa788-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="fa788-117">-Name</span></span>
<span data-ttu-id="fa788-118">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="fa788-118">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa788-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fa788-119">-ResourceId</span></span>
<span data-ttu-id="fa788-120">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="fa788-120">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa788-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa788-121">CommonParameters</span></span>
<span data-ttu-id="fa788-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fa788-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa788-123">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fa788-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa788-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fa788-124">INPUTS</span></span>

### <span data-ttu-id="fa788-125">System. String</span><span class="sxs-lookup"><span data-stu-id="fa788-125">System.String</span></span>

## <span data-ttu-id="fa788-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fa788-126">OUTPUTS</span></span>

### <span data-ttu-id="fa788-127">Microsoft. Azure. Commands. Security. Models. местонахождения. PSSecurityLocation</span><span class="sxs-lookup"><span data-stu-id="fa788-127">Microsoft.Azure.Commands.Security.Models.Locations.PSSecurityLocation</span></span>

## <span data-ttu-id="fa788-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="fa788-128">NOTES</span></span>

## <span data-ttu-id="fa788-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fa788-129">RELATED LINKS</span></span>
