---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/powershell/module/az.policyinsights/get-azpolicymetadata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyMetadata.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyMetadata.md
ms.openlocfilehash: 85a5c38038116d89e7cab1e6efe2718d4c5a697b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989148"
---
# <span data-ttu-id="b2e45-101">Get-AzPolicyMetadata</span><span class="sxs-lookup"><span data-stu-id="b2e45-101">Get-AzPolicyMetadata</span></span>

## <span data-ttu-id="b2e45-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b2e45-102">SYNOPSIS</span></span>
<span data-ttu-id="b2e45-103">Ресурсы по метаданным политики</span><span class="sxs-lookup"><span data-stu-id="b2e45-103">Gets Policy Metadata resources</span></span>

## <span data-ttu-id="b2e45-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b2e45-104">SYNTAX</span></span>

```
Get-AzPolicyMetadata [-Name <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b2e45-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b2e45-105">DESCRIPTION</span></span>
<span data-ttu-id="b2e45-106">С **помощью cmdlet Get-AzPolicyRemediation** можно получить все ресурсы метаданных политики или определенный ресурс метаданных политики.</span><span class="sxs-lookup"><span data-stu-id="b2e45-106">The **Get-AzPolicyRemediation** cmdlet gets all policy metadata resources or a particular policy metadata resource.</span></span>

## <span data-ttu-id="b2e45-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b2e45-107">EXAMPLES</span></span>

### <span data-ttu-id="b2e45-108">Пример 1. Получить все ресурсы метаданных политики</span><span class="sxs-lookup"><span data-stu-id="b2e45-108">Example 1: Get all policy metadata resources</span></span>
```powershell
PS C:\> Get-AzPolicyMetadata
```

<span data-ttu-id="b2e45-109">Эта команда получает все ресурсы метаданных политики.</span><span class="sxs-lookup"><span data-stu-id="b2e45-109">This command gets all policy metadata resources</span></span>

### <span data-ttu-id="b2e45-110">Пример 2. Получить набор из 10 ресурсов метаданных политики</span><span class="sxs-lookup"><span data-stu-id="b2e45-110">Example 2: Get a collection of 10 policy metadata resources</span></span>
```powershell
PS C:\> Get-AzPolicyMetadata -Top 10
```

<span data-ttu-id="b2e45-111">Эта команда получает набор из 10 ресурсов метаданных политики.</span><span class="sxs-lookup"><span data-stu-id="b2e45-111">This command gets a collection of 10 policy metadata resources</span></span>

### <span data-ttu-id="b2e45-112">Пример 3. Получить один ресурс метаданных политики с именем ACF1348</span><span class="sxs-lookup"><span data-stu-id="b2e45-112">Example 3: Get a single policy metadata resource with the name 'ACF1348'</span></span>
```powershell
PS C:\> Get-AzPolicyMetadata -Name ACF1348
```

<span data-ttu-id="b2e45-113">Эта команда получает один ресурс метаданных политики с именем ACF1348.</span><span class="sxs-lookup"><span data-stu-id="b2e45-113">This command gets a single policy metadata resource with the name 'ACF1348'</span></span>

## <span data-ttu-id="b2e45-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b2e45-114">PARAMETERS</span></span>

### <span data-ttu-id="b2e45-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2e45-115">-DefaultProfile</span></span>
<span data-ttu-id="b2e45-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b2e45-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b2e45-117">-Name</span><span class="sxs-lookup"><span data-stu-id="b2e45-117">-Name</span></span>
<span data-ttu-id="b2e45-118">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="b2e45-118">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2e45-119">-Top</span><span class="sxs-lookup"><span data-stu-id="b2e45-119">-Top</span></span>
<span data-ttu-id="b2e45-120">Максимальное количество возвращаемых ресурсов метаданных политики.</span><span class="sxs-lookup"><span data-stu-id="b2e45-120">Maximum number of policy metadata resources to return.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2e45-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2e45-121">CommonParameters</span></span>
<span data-ttu-id="b2e45-122">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2e45-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2e45-123">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b2e45-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2e45-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b2e45-124">INPUTS</span></span>

### <span data-ttu-id="b2e45-125">System.String</span><span class="sxs-lookup"><span data-stu-id="b2e45-125">System.String</span></span>

## <span data-ttu-id="b2e45-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b2e45-126">OUTPUTS</span></span>

### <span data-ttu-id="b2e45-127">Microsoft.Azure.Commands.PolicyInsights.Models.PSPolicyMetadata</span><span class="sxs-lookup"><span data-stu-id="b2e45-127">Microsoft.Azure.Commands.PolicyInsights.Models.PSPolicyMetadata</span></span>

## <span data-ttu-id="b2e45-128">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b2e45-128">NOTES</span></span>

## <span data-ttu-id="b2e45-129">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b2e45-129">RELATED LINKS</span></span>
