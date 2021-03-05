---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzSecuritySecureScoreControlDefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySecureScoreControlDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySecureScoreControlDefinition.md
ms.openlocfilehash: e8ec0073eef8b8db95197e19f2bfd61d0bbcdafd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995910"
---
# <span data-ttu-id="fa3ab-101">Get-AzSecuritySecureScoreControlDefinition</span><span class="sxs-lookup"><span data-stu-id="fa3ab-101">Get-AzSecuritySecureScoreControlDefinition</span></span>

## <span data-ttu-id="fa3ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa3ab-102">SYNOPSIS</span></span>
<span data-ttu-id="fa3ab-103">Получает определения оценки безопасности в подписке</span><span class="sxs-lookup"><span data-stu-id="fa3ab-103">Gets security secure score control definitions on a subscription</span></span>

## <span data-ttu-id="fa3ab-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="fa3ab-104">SYNTAX</span></span>

### <span data-ttu-id="fa3ab-105">SubscriptionScope (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fa3ab-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecuritySecureScoreControlDefinition [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fa3ab-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="fa3ab-106">SubscriptionLevelResource</span></span>
```
Get-AzSecuritySecureScoreControlDefinition -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fa3ab-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="fa3ab-107">EXAMPLES</span></span>

### <span data-ttu-id="fa3ab-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="fa3ab-108">Example 1</span></span>
```powershell
PS C:\> Get-AzSecuritySecureScoreControlDefinition
```

<span data-ttu-id="fa3ab-109">Все определения оценки безопасности в подписке</span><span class="sxs-lookup"><span data-stu-id="fa3ab-109">Gets all the security secure score control definitions in a subscription</span></span>

## <span data-ttu-id="fa3ab-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fa3ab-110">PARAMETERS</span></span>

### <span data-ttu-id="fa3ab-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa3ab-111">-DefaultProfile</span></span>
<span data-ttu-id="fa3ab-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fa3ab-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fa3ab-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa3ab-113">CommonParameters</span></span>
<span data-ttu-id="fa3ab-114">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa3ab-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa3ab-115">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fa3ab-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa3ab-116">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fa3ab-116">INPUTS</span></span>

### <span data-ttu-id="fa3ab-117">System.String</span><span class="sxs-lookup"><span data-stu-id="fa3ab-117">System.String</span></span>

## <span data-ttu-id="fa3ab-118">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="fa3ab-118">OUTPUTS</span></span>

### <span data-ttu-id="fa3ab-119">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecuritySecureScoreControlDefinition</span><span class="sxs-lookup"><span data-stu-id="fa3ab-119">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecuritySecureScoreControlDefinition</span></span>

## <span data-ttu-id="fa3ab-120">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="fa3ab-120">NOTES</span></span>

## <span data-ttu-id="fa3ab-121">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fa3ab-121">RELATED LINKS</span></span>
