---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/import-azblueprintwithartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Import-AzBlueprintWithArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Import-AzBlueprintWithArtifact.md
ms.openlocfilehash: 3853cc1785ca0e9f087b1e30870d17d304666df4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93727640"
---
# <span data-ttu-id="58a87-101">Import-AzBlueprintWithArtifact</span><span class="sxs-lookup"><span data-stu-id="58a87-101">Import-AzBlueprintWithArtifact</span></span>

## <span data-ttu-id="58a87-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="58a87-102">SYNOPSIS</span></span>
<span data-ttu-id="58a87-103">Импортируйте файл в формате JSON в объект чертежа и сохраните его в указанной подписке или группе управления.</span><span class="sxs-lookup"><span data-stu-id="58a87-103">Import a blueprint file in JSON format to a blueprint object and save it within the specified subscription or management group.</span></span>

## <span data-ttu-id="58a87-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="58a87-104">SYNTAX</span></span>

```
Import-AzBlueprintWithArtifact -Name <String> [-SubscriptionId <String>] [-ManagementGroupId <String>]
 -InputPath <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="58a87-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="58a87-105">DESCRIPTION</span></span>
<span data-ttu-id="58a87-106">Импортируйте определение чертежа с его артефактами.</span><span class="sxs-lookup"><span data-stu-id="58a87-106">Import a blueprint definition with its artifacts.</span></span> 

## <span data-ttu-id="58a87-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="58a87-107">EXAMPLES</span></span>

### <span data-ttu-id="58a87-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="58a87-108">Example 1</span></span>
```powershell
PS C:\> Import-AzBlueprintWithArtifact -Name MySimpleBlueprint -SubscriptionId 00000000-1111-0000-1111-000000000000 -InputPath  C:\Blueprints\SimpleBlueprint
```

<span data-ttu-id="58a87-109">Импортируйте определение чертежа с артефактами и сохраните его в рамках подписки.</span><span class="sxs-lookup"><span data-stu-id="58a87-109">Import a blueprint definition with its artifacts and save within a subscription.</span></span>

## <span data-ttu-id="58a87-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="58a87-110">PARAMETERS</span></span>

### <span data-ttu-id="58a87-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58a87-111">-DefaultProfile</span></span>
<span data-ttu-id="58a87-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="58a87-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58a87-113">-Force</span><span class="sxs-lookup"><span data-stu-id="58a87-113">-Force</span></span>
<span data-ttu-id="58a87-114">Если задано значение "true", при выполнении не будет запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="58a87-114">When set to true, execution will not ask for a confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58a87-115">-InputPath</span><span class="sxs-lookup"><span data-stu-id="58a87-115">-InputPath</span></span>
<span data-ttu-id="58a87-116">Путь к JSON-файлу, который планируется на диске.</span><span class="sxs-lookup"><span data-stu-id="58a87-116">Path to a Blueprint JSON file on disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58a87-117">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="58a87-117">-ManagementGroupId</span></span>
<span data-ttu-id="58a87-118">Идентификатор группы управления, в которой должно быть сохранено определение.</span><span class="sxs-lookup"><span data-stu-id="58a87-118">Management Group Id where the blueprint definition is or will be saved.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58a87-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="58a87-119">-Name</span></span>
<span data-ttu-id="58a87-120">Имя определения чертежа.</span><span class="sxs-lookup"><span data-stu-id="58a87-120">Blueprint definition name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58a87-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="58a87-121">-SubscriptionId</span></span>
<span data-ttu-id="58a87-122">Идентификатор подписки, в которой должно быть сохранено определение.</span><span class="sxs-lookup"><span data-stu-id="58a87-122">Subscription Id where the blueprint definition is or will be saved.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58a87-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58a87-123">CommonParameters</span></span>
<span data-ttu-id="58a87-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="58a87-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="58a87-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58a87-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58a87-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="58a87-126">INPUTS</span></span>

### <span data-ttu-id="58a87-127">System. String</span><span class="sxs-lookup"><span data-stu-id="58a87-127">System.String</span></span>

## <span data-ttu-id="58a87-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="58a87-128">OUTPUTS</span></span>

### <span data-ttu-id="58a87-129">System. String</span><span class="sxs-lookup"><span data-stu-id="58a87-129">System.String</span></span>

## <span data-ttu-id="58a87-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="58a87-130">NOTES</span></span>

## <span data-ttu-id="58a87-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="58a87-131">RELATED LINKS</span></span>
