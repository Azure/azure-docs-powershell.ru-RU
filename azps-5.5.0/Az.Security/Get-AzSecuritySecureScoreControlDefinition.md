---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecuritySecureScoreControlDefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySecureScoreControlDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySecureScoreControlDefinition.md
ms.openlocfilehash: 557e048dcce528b4c84f6d1b74915d81d6c6f0c8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100223209"
---
# <span data-ttu-id="f1911-101">Get-AzSecuritySecureScoreControlDefinition</span><span class="sxs-lookup"><span data-stu-id="f1911-101">Get-AzSecuritySecureScoreControlDefinition</span></span>

## <span data-ttu-id="f1911-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1911-102">SYNOPSIS</span></span>
<span data-ttu-id="f1911-103">Получает определения оценки безопасности в подписке</span><span class="sxs-lookup"><span data-stu-id="f1911-103">Gets security secure score control definitions on a subscription</span></span>

## <span data-ttu-id="f1911-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f1911-104">SYNTAX</span></span>

### <span data-ttu-id="f1911-105">SubscriptionScope (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f1911-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecuritySecureScoreControlDefinition [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f1911-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="f1911-106">SubscriptionLevelResource</span></span>
```
Get-AzSecuritySecureScoreControlDefinition -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f1911-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f1911-107">EXAMPLES</span></span>

### <span data-ttu-id="f1911-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f1911-108">Example 1</span></span>
```powershell
PS C:\> Get-AzSecuritySecureScoreControlDefinition
```

<span data-ttu-id="f1911-109">Все определения оценки безопасности в подписке</span><span class="sxs-lookup"><span data-stu-id="f1911-109">Gets all the security secure score control definitions in a subscription</span></span>

## <span data-ttu-id="f1911-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f1911-110">PARAMETERS</span></span>

### <span data-ttu-id="f1911-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1911-111">-DefaultProfile</span></span>
<span data-ttu-id="f1911-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f1911-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1911-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1911-113">CommonParameters</span></span>
<span data-ttu-id="f1911-114">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1911-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1911-115">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f1911-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1911-116">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f1911-116">INPUTS</span></span>

### <span data-ttu-id="f1911-117">System.String</span><span class="sxs-lookup"><span data-stu-id="f1911-117">System.String</span></span>

## <span data-ttu-id="f1911-118">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f1911-118">OUTPUTS</span></span>

### <span data-ttu-id="f1911-119">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecuritySecureScoreControlDefinition</span><span class="sxs-lookup"><span data-stu-id="f1911-119">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecuritySecureScoreControlDefinition</span></span>

## <span data-ttu-id="f1911-120">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f1911-120">NOTES</span></span>

## <span data-ttu-id="f1911-121">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f1911-121">RELATED LINKS</span></span>
