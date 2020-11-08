---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/get-azpolicymetadata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyMetadata.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyMetadata.md
ms.openlocfilehash: cfd32e7ee70ffb387bd1d2a52fdbf5eb60f2e148
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244287"
---
# <span data-ttu-id="8ff8d-101">Get-AzPolicyMetadata</span><span class="sxs-lookup"><span data-stu-id="8ff8d-101">Get-AzPolicyMetadata</span></span>

## <span data-ttu-id="8ff8d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8ff8d-102">SYNOPSIS</span></span>
<span data-ttu-id="8ff8d-103">Получение ресурсов метаданных политики</span><span class="sxs-lookup"><span data-stu-id="8ff8d-103">Gets Policy Metadata resources</span></span>

## <span data-ttu-id="8ff8d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8ff8d-104">SYNTAX</span></span>

```
Get-AzPolicyMetadata [-Name <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8ff8d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8ff8d-105">DESCRIPTION</span></span>
<span data-ttu-id="8ff8d-106">Командлет **Get-AzPolicyRemediation** получает все ресурсы метаданных политики или конкретный ресурс метаданных политики.</span><span class="sxs-lookup"><span data-stu-id="8ff8d-106">The **Get-AzPolicyRemediation** cmdlet gets all policy metadata resources or a particular policy metadata resource.</span></span>

## <span data-ttu-id="8ff8d-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8ff8d-107">EXAMPLES</span></span>

### <span data-ttu-id="8ff8d-108">Пример 1: получение всех ресурсов метаданных политики</span><span class="sxs-lookup"><span data-stu-id="8ff8d-108">Example 1: Get all policy metadata resources</span></span>
```powershell
PS C:\> Get-AzPolicyMetadata
```

<span data-ttu-id="8ff8d-109">Эта команда получает ресурсы метаданных политики</span><span class="sxs-lookup"><span data-stu-id="8ff8d-109">This command gets all policy metadata resources</span></span>

### <span data-ttu-id="8ff8d-110">Пример 2: получение коллекции ресурсов метаданных политики 10</span><span class="sxs-lookup"><span data-stu-id="8ff8d-110">Example 2: Get a collection of 10 policy metadata resources</span></span>
```powershell
PS C:\> Get-AzPolicyMetadata -Top 10
```

<span data-ttu-id="8ff8d-111">Эта команда получает коллекцию ресурсов метаданных политики из 10</span><span class="sxs-lookup"><span data-stu-id="8ff8d-111">This command gets a collection of 10 policy metadata resources</span></span>

### <span data-ttu-id="8ff8d-112">Пример 3: получение ресурса метаданных одной политики с именем "ACF1348"</span><span class="sxs-lookup"><span data-stu-id="8ff8d-112">Example 3: Get a single policy metadata resource with the name 'ACF1348'</span></span>
```powershell
PS C:\> Get-AzPolicyMetadata -Name ACF1348
```

<span data-ttu-id="8ff8d-113">Эта команда получает ресурс метаданных одной политики с именем "ACF1348".</span><span class="sxs-lookup"><span data-stu-id="8ff8d-113">This command gets a single policy metadata resource with the name 'ACF1348'</span></span>

## <span data-ttu-id="8ff8d-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8ff8d-114">PARAMETERS</span></span>

### <span data-ttu-id="8ff8d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ff8d-115">-DefaultProfile</span></span>
<span data-ttu-id="8ff8d-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8ff8d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8ff8d-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8ff8d-117">-Name</span></span>
<span data-ttu-id="8ff8d-118">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="8ff8d-118">Resource name.</span></span>

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

### <span data-ttu-id="8ff8d-119">-Top</span><span class="sxs-lookup"><span data-stu-id="8ff8d-119">-Top</span></span>
<span data-ttu-id="8ff8d-120">Максимальное количество возвращаемых ресурсов для метаданных политики.</span><span class="sxs-lookup"><span data-stu-id="8ff8d-120">Maximum number of policy metadata resources to return.</span></span>

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

### <span data-ttu-id="8ff8d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ff8d-121">CommonParameters</span></span>
<span data-ttu-id="8ff8d-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8ff8d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ff8d-123">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8ff8d-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ff8d-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8ff8d-124">INPUTS</span></span>

### <span data-ttu-id="8ff8d-125">System. String</span><span class="sxs-lookup"><span data-stu-id="8ff8d-125">System.String</span></span>

## <span data-ttu-id="8ff8d-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8ff8d-126">OUTPUTS</span></span>

### <span data-ttu-id="8ff8d-127">Microsoft. Azure. Commands. PolicyInsights. Models. PSPolicyMetadata</span><span class="sxs-lookup"><span data-stu-id="8ff8d-127">Microsoft.Azure.Commands.PolicyInsights.Models.PSPolicyMetadata</span></span>

## <span data-ttu-id="8ff8d-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="8ff8d-128">NOTES</span></span>

## <span data-ttu-id="8ff8d-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8ff8d-129">RELATED LINKS</span></span>
