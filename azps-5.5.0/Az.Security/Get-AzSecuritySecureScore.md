---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecuritySecureScore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySecureScore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySecureScore.md
ms.openlocfilehash: 5b14298f48c5723b4d84b0f22d799ac0a21699e0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100223241"
---
# <span data-ttu-id="868a7-101">Get-AzSecuritySecureScore</span><span class="sxs-lookup"><span data-stu-id="868a7-101">Get-AzSecuritySecureScore</span></span>

## <span data-ttu-id="868a7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="868a7-102">SYNOPSIS</span></span>
<span data-ttu-id="868a7-103">Оценка безопасности и результаты по подписке</span><span class="sxs-lookup"><span data-stu-id="868a7-103">Gets security secure scores and their results on a subscription</span></span>

## <span data-ttu-id="868a7-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="868a7-104">SYNTAX</span></span>

### <span data-ttu-id="868a7-105">SubscriptionScope (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="868a7-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecuritySecureScore [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="868a7-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="868a7-106">SubscriptionLevelResource</span></span>
```
Get-AzSecuritySecureScore -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="868a7-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="868a7-107">EXAMPLES</span></span>

### <span data-ttu-id="868a7-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="868a7-108">Example 1</span></span>
```powershell
PS C:\> Get-AzSecuritySecureScore
```

<span data-ttu-id="868a7-109">Получает все оценки безопасности в подписке</span><span class="sxs-lookup"><span data-stu-id="868a7-109">Gets all the security secure scores in a subscription</span></span>

## <span data-ttu-id="868a7-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="868a7-110">PARAMETERS</span></span>

### <span data-ttu-id="868a7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="868a7-111">-DefaultProfile</span></span>
<span data-ttu-id="868a7-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="868a7-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="868a7-113">-Name</span><span class="sxs-lookup"><span data-stu-id="868a7-113">-Name</span></span>
<span data-ttu-id="868a7-114">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="868a7-114">Resource name.</span></span>

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

### <span data-ttu-id="868a7-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="868a7-115">CommonParameters</span></span>
<span data-ttu-id="868a7-116">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="868a7-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="868a7-117">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="868a7-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="868a7-118">INPUTS</span><span class="sxs-lookup"><span data-stu-id="868a7-118">INPUTS</span></span>

### <span data-ttu-id="868a7-119">System.String</span><span class="sxs-lookup"><span data-stu-id="868a7-119">System.String</span></span>

## <span data-ttu-id="868a7-120">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="868a7-120">OUTPUTS</span></span>

### <span data-ttu-id="868a7-121">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecuritySecureScore</span><span class="sxs-lookup"><span data-stu-id="868a7-121">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecuritySecureScore</span></span>

## <span data-ttu-id="868a7-122">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="868a7-122">NOTES</span></span>

## <span data-ttu-id="868a7-123">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="868a7-123">RELATED LINKS</span></span>
