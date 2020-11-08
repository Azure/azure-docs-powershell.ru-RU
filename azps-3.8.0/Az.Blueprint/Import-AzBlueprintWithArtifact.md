---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/import-azblueprintwithartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Import-AzBlueprintWithArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Import-AzBlueprintWithArtifact.md
ms.openlocfilehash: 7a1778ce107e9753f78876aff3a2dfba19e138e8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073686"
---
# <span data-ttu-id="72db3-101">Import-AzBlueprintWithArtifact</span><span class="sxs-lookup"><span data-stu-id="72db3-101">Import-AzBlueprintWithArtifact</span></span>

## <span data-ttu-id="72db3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="72db3-102">SYNOPSIS</span></span>
<span data-ttu-id="72db3-103">Импортируйте файл в формате JSON в объект чертежа и сохраните его в указанной подписке или группе управления.</span><span class="sxs-lookup"><span data-stu-id="72db3-103">Import a blueprint file in JSON format to a blueprint object and save it within the specified subscription or management group.</span></span>

## <span data-ttu-id="72db3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="72db3-104">SYNTAX</span></span>

```
Import-AzBlueprintWithArtifact -Name <String> [-SubscriptionId <String>] [-ManagementGroupId <String>]
 -InputPath <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="72db3-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="72db3-105">DESCRIPTION</span></span>
<span data-ttu-id="72db3-106">Импортируйте определение чертежа с его артефактами.</span><span class="sxs-lookup"><span data-stu-id="72db3-106">Import a blueprint definition with its artifacts.</span></span> 

## <span data-ttu-id="72db3-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="72db3-107">EXAMPLES</span></span>

### <span data-ttu-id="72db3-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="72db3-108">Example 1</span></span>
```powershell
PS C:\> Import-AzBlueprintWithArtifact -Name MySimpleBlueprint -SubscriptionId 00000000-1111-0000-1111-000000000000 -InputPath  C:\Blueprints\SimpleBlueprint
```

<span data-ttu-id="72db3-109">Импортируйте определение чертежа с артефактами и сохраните его в рамках подписки.</span><span class="sxs-lookup"><span data-stu-id="72db3-109">Import a blueprint definition with its artifacts and save within a subscription.</span></span>

## <span data-ttu-id="72db3-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="72db3-110">PARAMETERS</span></span>

### <span data-ttu-id="72db3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72db3-111">-DefaultProfile</span></span>
<span data-ttu-id="72db3-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="72db3-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="72db3-113">-Force</span><span class="sxs-lookup"><span data-stu-id="72db3-113">-Force</span></span>
<span data-ttu-id="72db3-114">Если задано значение "true", при выполнении не будет запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="72db3-114">When set to true, execution will not ask for a confirmation.</span></span>

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

### <span data-ttu-id="72db3-115">-IncludeSubFolders</span><span class="sxs-lookup"><span data-stu-id="72db3-115">-IncludeSubFolders</span></span>
<span data-ttu-id="72db3-116">Если установлено значение true, артефакты во вложенных папках будут включены.</span><span class="sxs-lookup"><span data-stu-id="72db3-116">When set to true, artifact in the subfolders will be included.</span></span>

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

### <span data-ttu-id="72db3-117">-InputPath</span><span class="sxs-lookup"><span data-stu-id="72db3-117">-InputPath</span></span>
<span data-ttu-id="72db3-118">Путь к JSON-файлу, который планируется на диске.</span><span class="sxs-lookup"><span data-stu-id="72db3-118">Path to a Blueprint JSON file on disk.</span></span>

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

### <span data-ttu-id="72db3-119">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="72db3-119">-ManagementGroupId</span></span>
<span data-ttu-id="72db3-120">Идентификатор группы управления, в которой должно быть сохранено определение.</span><span class="sxs-lookup"><span data-stu-id="72db3-120">Management Group Id where the blueprint definition is or will be saved.</span></span>

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

### <span data-ttu-id="72db3-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="72db3-121">-Name</span></span>
<span data-ttu-id="72db3-122">Имя определения чертежа.</span><span class="sxs-lookup"><span data-stu-id="72db3-122">Blueprint definition name.</span></span>

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

### <span data-ttu-id="72db3-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="72db3-123">-SubscriptionId</span></span>
<span data-ttu-id="72db3-124">Идентификатор подписки, в которой должно быть сохранено определение.</span><span class="sxs-lookup"><span data-stu-id="72db3-124">Subscription Id where the blueprint definition is or will be saved.</span></span>

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

### <span data-ttu-id="72db3-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72db3-125">CommonParameters</span></span>
<span data-ttu-id="72db3-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="72db3-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="72db3-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72db3-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72db3-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="72db3-128">INPUTS</span></span>

### <span data-ttu-id="72db3-129">System. String</span><span class="sxs-lookup"><span data-stu-id="72db3-129">System.String</span></span>

## <span data-ttu-id="72db3-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="72db3-130">OUTPUTS</span></span>

### <span data-ttu-id="72db3-131">System. String</span><span class="sxs-lookup"><span data-stu-id="72db3-131">System.String</span></span>

## <span data-ttu-id="72db3-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="72db3-132">NOTES</span></span>

## <span data-ttu-id="72db3-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="72db3-133">RELATED LINKS</span></span>
