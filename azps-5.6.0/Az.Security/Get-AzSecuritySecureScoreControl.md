---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzSecuritySecureScoreControl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySecureScoreControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySecureScoreControl.md
ms.openlocfilehash: 497865446e943fc34f45f6c98713d559086cca84
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979304"
---
# <span data-ttu-id="cce3c-101">Get-AzSecuritySecureScoreControl</span><span class="sxs-lookup"><span data-stu-id="cce3c-101">Get-AzSecuritySecureScoreControl</span></span>

## <span data-ttu-id="cce3c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cce3c-102">SYNOPSIS</span></span>
<span data-ttu-id="cce3c-103">Получает средства контроля оценки безопасности и их результаты по подписке</span><span class="sxs-lookup"><span data-stu-id="cce3c-103">Gets security secure score controls and their results on a subscription</span></span>

## <span data-ttu-id="cce3c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="cce3c-104">SYNTAX</span></span>

### <span data-ttu-id="cce3c-105">SubscriptionScope (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cce3c-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecuritySecureScoreControl [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cce3c-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="cce3c-106">SubscriptionLevelResource</span></span>
```
Get-AzSecuritySecureScoreControl -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cce3c-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="cce3c-107">EXAMPLES</span></span>

### <span data-ttu-id="cce3c-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="cce3c-108">Example 1</span></span>
```powershell
PS C:\> Get-AzSecuritySecureScoreControl
```

<span data-ttu-id="cce3c-109">Получает все оценки безопасности в подписке</span><span class="sxs-lookup"><span data-stu-id="cce3c-109">Gets all the security secure scores in a subscription</span></span>

## <span data-ttu-id="cce3c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cce3c-110">PARAMETERS</span></span>

### <span data-ttu-id="cce3c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cce3c-111">-DefaultProfile</span></span>
<span data-ttu-id="cce3c-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cce3c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cce3c-113">-Name</span><span class="sxs-lookup"><span data-stu-id="cce3c-113">-Name</span></span>
<span data-ttu-id="cce3c-114">Имя оценки безопасности.</span><span class="sxs-lookup"><span data-stu-id="cce3c-114">Secure score name.</span></span>

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

### <span data-ttu-id="cce3c-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cce3c-115">CommonParameters</span></span>
<span data-ttu-id="cce3c-116">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cce3c-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cce3c-117">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cce3c-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cce3c-118">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cce3c-118">INPUTS</span></span>

### <span data-ttu-id="cce3c-119">System.String</span><span class="sxs-lookup"><span data-stu-id="cce3c-119">System.String</span></span>

## <span data-ttu-id="cce3c-120">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="cce3c-120">OUTPUTS</span></span>

### <span data-ttu-id="cce3c-121">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecuritySecureScoreControl</span><span class="sxs-lookup"><span data-stu-id="cce3c-121">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecuritySecureScoreControl</span></span>

## <span data-ttu-id="cce3c-122">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="cce3c-122">NOTES</span></span>

## <span data-ttu-id="cce3c-123">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cce3c-123">RELATED LINKS</span></span>
