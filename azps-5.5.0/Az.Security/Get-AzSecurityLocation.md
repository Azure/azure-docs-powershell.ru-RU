---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityLocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityLocation.md
ms.openlocfilehash: 77f9283b16aa605da066780165c2fe7b42b1830b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100223257"
---
# <span data-ttu-id="07c90-101">Get-AzSecurityLocation</span><span class="sxs-lookup"><span data-stu-id="07c90-101">Get-AzSecurityLocation</span></span>

## <span data-ttu-id="07c90-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07c90-102">SYNOPSIS</span></span>
<span data-ttu-id="07c90-103">Расположение, в котором Центр безопасности Azure будет автоматически сохранять данные для конкретной подписки</span><span class="sxs-lookup"><span data-stu-id="07c90-103">Gets the location where Azure Security Center will automatically save data for the specific subscription</span></span>

## <span data-ttu-id="07c90-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="07c90-104">SYNTAX</span></span>

### <span data-ttu-id="07c90-105">SubscriptionScope (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="07c90-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityLocation [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="07c90-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="07c90-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityLocation -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="07c90-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="07c90-107">ResourceId</span></span>
```
Get-AzSecurityLocation -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="07c90-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="07c90-108">DESCRIPTION</span></span>
<span data-ttu-id="07c90-109">Центр безопасности Azure автоматически определит расположение для сохранения некоторых данных.</span><span class="sxs-lookup"><span data-stu-id="07c90-109">Azure Security Center will automatically decide on a location to save some of your data.</span></span>
<span data-ttu-id="07c90-110">Используйте этот cmdlet, чтобы найти это расположение.</span><span class="sxs-lookup"><span data-stu-id="07c90-110">Use this cmdlet to discover that location.</span></span>

## <span data-ttu-id="07c90-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="07c90-111">EXAMPLES</span></span>

### <span data-ttu-id="07c90-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="07c90-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityLocation
Id                                                                                                   Name
--                                                                                                   ----
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/locations/centralus centralus
```

<span data-ttu-id="07c90-113">Возвращает расположение, в котором Центр безопасности Azure сохраняет вычислимые данные безопасности.</span><span class="sxs-lookup"><span data-stu-id="07c90-113">Gets the location where Azure Security Center saves the calculated security data.</span></span>

## <span data-ttu-id="07c90-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="07c90-114">PARAMETERS</span></span>

### <span data-ttu-id="07c90-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07c90-115">-DefaultProfile</span></span>
<span data-ttu-id="07c90-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="07c90-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="07c90-117">-Name</span><span class="sxs-lookup"><span data-stu-id="07c90-117">-Name</span></span>
<span data-ttu-id="07c90-118">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="07c90-118">Resource name.</span></span>

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

### <span data-ttu-id="07c90-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="07c90-119">-ResourceId</span></span>
<span data-ttu-id="07c90-120">ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="07c90-120">Resource ID.</span></span>

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

### <span data-ttu-id="07c90-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07c90-121">CommonParameters</span></span>
<span data-ttu-id="07c90-122">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07c90-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07c90-123">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="07c90-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07c90-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="07c90-124">INPUTS</span></span>

### <span data-ttu-id="07c90-125">System.String</span><span class="sxs-lookup"><span data-stu-id="07c90-125">System.String</span></span>

## <span data-ttu-id="07c90-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="07c90-126">OUTPUTS</span></span>

### <span data-ttu-id="07c90-127">Microsoft.Azure.Commands.Security.Models.Locations.PSSecurityLocation</span><span class="sxs-lookup"><span data-stu-id="07c90-127">Microsoft.Azure.Commands.Security.Models.Locations.PSSecurityLocation</span></span>

## <span data-ttu-id="07c90-128">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="07c90-128">NOTES</span></span>

## <span data-ttu-id="07c90-129">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="07c90-129">RELATED LINKS</span></span>
