---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityAssessmentMetadata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAssessmentMetadata.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAssessmentMetadata.md
ms.openlocfilehash: 6b2819041b9fd136ee1ecc65b9d8b36132af5317
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249462"
---
# <span data-ttu-id="d2fab-101">Get-AzSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="d2fab-101">Get-AzSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="d2fab-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d2fab-102">SYNOPSIS</span></span>
<span data-ttu-id="d2fab-103">Возвращает оценки и metadta в подписке.</span><span class="sxs-lookup"><span data-stu-id="d2fab-103">Gets security assessments types and metadta in a subscription.</span></span>

## <span data-ttu-id="d2fab-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d2fab-104">SYNTAX</span></span>

### <span data-ttu-id="d2fab-105">SubscriptionScope (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d2fab-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityAssessmentMetadata [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d2fab-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="d2fab-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityAssessmentMetadata -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d2fab-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="d2fab-107">ResourceId</span></span>
```
Get-AzSecurityAssessmentMetadata -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d2fab-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d2fab-108">DESCRIPTION</span></span>
<span data-ttu-id="d2fab-109">Возвращает оценки и metadta в подписке.</span><span class="sxs-lookup"><span data-stu-id="d2fab-109">Gets security assessments types and metadta in a subscription.</span></span> <span data-ttu-id="d2fab-110">Метаданные оценки безопасности включают оценки Built-In и пользовательские типы оценки, которые пользователь может определять.</span><span class="sxs-lookup"><span data-stu-id="d2fab-110">Security Assessment metadata include Built-In assessments and custom assessment types that the user can define.</span></span>

## <span data-ttu-id="d2fab-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d2fab-111">EXAMPLES</span></span>

### <span data-ttu-id="d2fab-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d2fab-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAssessmentMetadata
```

<span data-ttu-id="d2fab-113">Получает все встроенные оценки и пользовательские оценки, настроенные для текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="d2fab-113">Gets all the built in assessments and the custom assessments that were configured on the current subscription.</span></span>

## <span data-ttu-id="d2fab-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d2fab-114">PARAMETERS</span></span>

### <span data-ttu-id="d2fab-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2fab-115">-DefaultProfile</span></span>
<span data-ttu-id="d2fab-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d2fab-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2fab-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d2fab-117">-Name</span></span>
<span data-ttu-id="d2fab-118">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="d2fab-118">Resource name.</span></span>

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

### <span data-ttu-id="d2fab-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d2fab-119">-ResourceId</span></span>
<span data-ttu-id="d2fab-120">Идентификатор ресурса безопасности, для которого нужно вызвать команду.</span><span class="sxs-lookup"><span data-stu-id="d2fab-120">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="d2fab-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2fab-121">CommonParameters</span></span>
<span data-ttu-id="d2fab-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d2fab-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2fab-123">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d2fab-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2fab-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d2fab-124">INPUTS</span></span>

### <span data-ttu-id="d2fab-125">System. String</span><span class="sxs-lookup"><span data-stu-id="d2fab-125">System.String</span></span>

## <span data-ttu-id="d2fab-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d2fab-126">OUTPUTS</span></span>

### <span data-ttu-id="d2fab-127">Microsoft. Azure. Commands. Security. Models. AssessmentMetadata. PSSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="d2fab-127">Microsoft.Azure.Commands.Security.Models.AssessmentMetadata.PSSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="d2fab-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="d2fab-128">NOTES</span></span>

## <span data-ttu-id="d2fab-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d2fab-129">RELATED LINKS</span></span>
