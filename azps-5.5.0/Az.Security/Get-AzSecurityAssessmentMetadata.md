---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityAssessmentMetadata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAssessmentMetadata.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAssessmentMetadata.md
ms.openlocfilehash: 6b2819041b9fd136ee1ecc65b9d8b36132af5317
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100232004"
---
# <span data-ttu-id="87b4f-101">Get-AzSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="87b4f-101">Get-AzSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="87b4f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="87b4f-102">SYNOPSIS</span></span>
<span data-ttu-id="87b4f-103">Возвращает типы оценок безопасности и метаданные в подписке.</span><span class="sxs-lookup"><span data-stu-id="87b4f-103">Gets security assessments types and metadta in a subscription.</span></span>

## <span data-ttu-id="87b4f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="87b4f-104">SYNTAX</span></span>

### <span data-ttu-id="87b4f-105">SubscriptionScope (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="87b4f-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityAssessmentMetadata [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="87b4f-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="87b4f-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityAssessmentMetadata -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="87b4f-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="87b4f-107">ResourceId</span></span>
```
Get-AzSecurityAssessmentMetadata -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="87b4f-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="87b4f-108">DESCRIPTION</span></span>
<span data-ttu-id="87b4f-109">Возвращает типы оценок безопасности и метаданные в подписке.</span><span class="sxs-lookup"><span data-stu-id="87b4f-109">Gets security assessments types and metadta in a subscription.</span></span> <span data-ttu-id="87b4f-110">Метаданные оценки безопасности включают Built-In оценки и пользовательские типы оценок, которые пользователь может определить.</span><span class="sxs-lookup"><span data-stu-id="87b4f-110">Security Assessment metadata include Built-In assessments and custom assessment types that the user can define.</span></span>

## <span data-ttu-id="87b4f-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="87b4f-111">EXAMPLES</span></span>

### <span data-ttu-id="87b4f-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="87b4f-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAssessmentMetadata
```

<span data-ttu-id="87b4f-113">Все встроенные оценки и настраиваемые оценки, настроенные в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="87b4f-113">Gets all the built in assessments and the custom assessments that were configured on the current subscription.</span></span>

## <span data-ttu-id="87b4f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="87b4f-114">PARAMETERS</span></span>

### <span data-ttu-id="87b4f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87b4f-115">-DefaultProfile</span></span>
<span data-ttu-id="87b4f-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="87b4f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="87b4f-117">-Name</span><span class="sxs-lookup"><span data-stu-id="87b4f-117">-Name</span></span>
<span data-ttu-id="87b4f-118">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="87b4f-118">Resource name.</span></span>

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

### <span data-ttu-id="87b4f-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="87b4f-119">-ResourceId</span></span>
<span data-ttu-id="87b4f-120">ИД ресурса безопасности, для который требуется вызвать команду.</span><span class="sxs-lookup"><span data-stu-id="87b4f-120">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="87b4f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87b4f-121">CommonParameters</span></span>
<span data-ttu-id="87b4f-122">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87b4f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87b4f-123">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="87b4f-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87b4f-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="87b4f-124">INPUTS</span></span>

### <span data-ttu-id="87b4f-125">System.String</span><span class="sxs-lookup"><span data-stu-id="87b4f-125">System.String</span></span>

## <span data-ttu-id="87b4f-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="87b4f-126">OUTPUTS</span></span>

### <span data-ttu-id="87b4f-127">Microsoft.Azure.Commands.Security.Models.AssessmentMetadata.PSSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="87b4f-127">Microsoft.Azure.Commands.Security.Models.AssessmentMetadata.PSSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="87b4f-128">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="87b4f-128">NOTES</span></span>

## <span data-ttu-id="87b4f-129">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="87b4f-129">RELATED LINKS</span></span>
