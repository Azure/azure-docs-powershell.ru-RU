---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/get-azpolicymetadata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyMetadata.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyMetadata.md
ms.openlocfilehash: cfd32e7ee70ffb387bd1d2a52fdbf5eb60f2e148
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100227244"
---
# <span data-ttu-id="31a9f-101">Get-AzPolicyMetadata</span><span class="sxs-lookup"><span data-stu-id="31a9f-101">Get-AzPolicyMetadata</span></span>

## <span data-ttu-id="31a9f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="31a9f-102">SYNOPSIS</span></span>
<span data-ttu-id="31a9f-103">Ресурсы по метаданным политики.</span><span class="sxs-lookup"><span data-stu-id="31a9f-103">Gets Policy Metadata resources</span></span>

## <span data-ttu-id="31a9f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="31a9f-104">SYNTAX</span></span>

```
Get-AzPolicyMetadata [-Name <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="31a9f-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="31a9f-105">DESCRIPTION</span></span>
<span data-ttu-id="31a9f-106">С **помощью cmdlet Get-AzPolicyRemediation** можно получить все ресурсы метаданных политики или определенный ресурс метаданных политики.</span><span class="sxs-lookup"><span data-stu-id="31a9f-106">The **Get-AzPolicyRemediation** cmdlet gets all policy metadata resources or a particular policy metadata resource.</span></span>

## <span data-ttu-id="31a9f-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="31a9f-107">EXAMPLES</span></span>

### <span data-ttu-id="31a9f-108">Пример 1. Получить все ресурсы метаданных политики</span><span class="sxs-lookup"><span data-stu-id="31a9f-108">Example 1: Get all policy metadata resources</span></span>
```powershell
PS C:\> Get-AzPolicyMetadata
```

<span data-ttu-id="31a9f-109">Эта команда получает все ресурсы метаданных политики.</span><span class="sxs-lookup"><span data-stu-id="31a9f-109">This command gets all policy metadata resources</span></span>

### <span data-ttu-id="31a9f-110">Пример 2. Получить набор из 10 ресурсов метаданных политики</span><span class="sxs-lookup"><span data-stu-id="31a9f-110">Example 2: Get a collection of 10 policy metadata resources</span></span>
```powershell
PS C:\> Get-AzPolicyMetadata -Top 10
```

<span data-ttu-id="31a9f-111">Эта команда получает набор из 10 ресурсов метаданных политики.</span><span class="sxs-lookup"><span data-stu-id="31a9f-111">This command gets a collection of 10 policy metadata resources</span></span>

### <span data-ttu-id="31a9f-112">Пример 3. Получить один ресурс метаданных политики с именем ACF1348</span><span class="sxs-lookup"><span data-stu-id="31a9f-112">Example 3: Get a single policy metadata resource with the name 'ACF1348'</span></span>
```powershell
PS C:\> Get-AzPolicyMetadata -Name ACF1348
```

<span data-ttu-id="31a9f-113">Эта команда получает один ресурс метаданных политики с именем ACF1348.</span><span class="sxs-lookup"><span data-stu-id="31a9f-113">This command gets a single policy metadata resource with the name 'ACF1348'</span></span>

## <span data-ttu-id="31a9f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="31a9f-114">PARAMETERS</span></span>

### <span data-ttu-id="31a9f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31a9f-115">-DefaultProfile</span></span>
<span data-ttu-id="31a9f-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="31a9f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="31a9f-117">-Name</span><span class="sxs-lookup"><span data-stu-id="31a9f-117">-Name</span></span>
<span data-ttu-id="31a9f-118">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="31a9f-118">Resource name.</span></span>

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

### <span data-ttu-id="31a9f-119">-Top</span><span class="sxs-lookup"><span data-stu-id="31a9f-119">-Top</span></span>
<span data-ttu-id="31a9f-120">Максимальное количество возвращаемых ресурсов метаданных политики.</span><span class="sxs-lookup"><span data-stu-id="31a9f-120">Maximum number of policy metadata resources to return.</span></span>

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

### <span data-ttu-id="31a9f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31a9f-121">CommonParameters</span></span>
<span data-ttu-id="31a9f-122">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31a9f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31a9f-123">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="31a9f-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31a9f-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="31a9f-124">INPUTS</span></span>

### <span data-ttu-id="31a9f-125">System.String</span><span class="sxs-lookup"><span data-stu-id="31a9f-125">System.String</span></span>

## <span data-ttu-id="31a9f-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="31a9f-126">OUTPUTS</span></span>

### <span data-ttu-id="31a9f-127">Microsoft.Azure.Commands.PolicyInsights.Models.PSPolicyMetadata</span><span class="sxs-lookup"><span data-stu-id="31a9f-127">Microsoft.Azure.Commands.PolicyInsights.Models.PSPolicyMetadata</span></span>

## <span data-ttu-id="31a9f-128">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="31a9f-128">NOTES</span></span>

## <span data-ttu-id="31a9f-129">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="31a9f-129">RELATED LINKS</span></span>
