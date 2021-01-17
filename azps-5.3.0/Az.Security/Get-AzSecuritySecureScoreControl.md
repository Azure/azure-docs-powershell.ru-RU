---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecuritySecureScoreControl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySecureScoreControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySecureScoreControl.md
ms.openlocfilehash: 6f3b932ae4d8aad746eb1586525326ba9453af9a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98420972"
---
# <span data-ttu-id="2eef6-101">Get-AzSecuritySecureScoreControl</span><span class="sxs-lookup"><span data-stu-id="2eef6-101">Get-AzSecuritySecureScoreControl</span></span>

## <span data-ttu-id="2eef6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2eef6-102">SYNOPSIS</span></span>
<span data-ttu-id="2eef6-103">Получает средства контроля оценки безопасности и их результаты по подписке</span><span class="sxs-lookup"><span data-stu-id="2eef6-103">Gets security secure score controls and their results on a subscription</span></span>

## <span data-ttu-id="2eef6-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2eef6-104">SYNTAX</span></span>

### <span data-ttu-id="2eef6-105">SubscriptionScope (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2eef6-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecuritySecureScoreControl [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2eef6-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="2eef6-106">SubscriptionLevelResource</span></span>
```
Get-AzSecuritySecureScoreControl -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2eef6-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2eef6-107">EXAMPLES</span></span>

### <span data-ttu-id="2eef6-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2eef6-108">Example 1</span></span>
```powershell
PS C:\> Get-AzSecuritySecureScoreControl
```

<span data-ttu-id="2eef6-109">Все оценки безопасности в подписке</span><span class="sxs-lookup"><span data-stu-id="2eef6-109">Gets all the security secure scores in a subscription</span></span>

## <span data-ttu-id="2eef6-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2eef6-110">PARAMETERS</span></span>

### <span data-ttu-id="2eef6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2eef6-111">-DefaultProfile</span></span>
<span data-ttu-id="2eef6-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2eef6-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2eef6-113">-Name</span><span class="sxs-lookup"><span data-stu-id="2eef6-113">-Name</span></span>
<span data-ttu-id="2eef6-114">Имя оценки безопасности.</span><span class="sxs-lookup"><span data-stu-id="2eef6-114">Secure score name.</span></span>

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

### <span data-ttu-id="2eef6-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2eef6-115">CommonParameters</span></span>
<span data-ttu-id="2eef6-116">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2eef6-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2eef6-117">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2eef6-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2eef6-118">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2eef6-118">INPUTS</span></span>

### <span data-ttu-id="2eef6-119">System.String</span><span class="sxs-lookup"><span data-stu-id="2eef6-119">System.String</span></span>

## <span data-ttu-id="2eef6-120">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2eef6-120">OUTPUTS</span></span>

### <span data-ttu-id="2eef6-121">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecuritySecureScoreControl</span><span class="sxs-lookup"><span data-stu-id="2eef6-121">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecuritySecureScoreControl</span></span>

## <span data-ttu-id="2eef6-122">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2eef6-122">NOTES</span></span>

## <span data-ttu-id="2eef6-123">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2eef6-123">RELATED LINKS</span></span>
