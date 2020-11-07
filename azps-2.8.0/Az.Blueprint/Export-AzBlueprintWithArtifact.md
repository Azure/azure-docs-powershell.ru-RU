---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/export-azblueprintwithartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Export-AzBlueprintWithArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Export-AzBlueprintWithArtifact.md
ms.openlocfilehash: 2c349d99e8a3529d4f1423a43bd31ab2500664c1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93727652"
---
# <span data-ttu-id="b3fe6-101">Export-AzBlueprintWithArtifact</span><span class="sxs-lookup"><span data-stu-id="b3fe6-101">Export-AzBlueprintWithArtifact</span></span>

## <span data-ttu-id="b3fe6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b3fe6-102">SYNOPSIS</span></span>
<span data-ttu-id="b3fe6-103">Экспортировать определение указанного чертежа в указанное расположение выходных файлов в виде JSON-файла.</span><span class="sxs-lookup"><span data-stu-id="b3fe6-103">Export specified blueprint definition to the specified output location as a JSON file.</span></span> 

## <span data-ttu-id="b3fe6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b3fe6-104">SYNTAX</span></span>

```
Export-AzBlueprintWithArtifact -Blueprint <PSBlueprintBase> -OutputPath <String> [-Version <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b3fe6-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b3fe6-105">DESCRIPTION</span></span>
<span data-ttu-id="b3fe6-106">Экспортируйте определение чертежа вместе с артефактами и сохраните его на диск.</span><span class="sxs-lookup"><span data-stu-id="b3fe6-106">Export a blueprint definition with its artifacts and save to disk.</span></span> <span data-ttu-id="b3fe6-107">Этот командлет экспортирует последнюю версию проекта (черновика или опубликована).</span><span class="sxs-lookup"><span data-stu-id="b3fe6-107">This cmdlet exports the latest version(draft or published) of the blueprint.</span></span>

## <span data-ttu-id="b3fe6-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b3fe6-108">EXAMPLES</span></span>

### <span data-ttu-id="b3fe6-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b3fe6-109">Example 1</span></span>
```powershell
PS C:\> $bp = Get-AzBlueprint -Name SimpleBlueprint
PS C:\> Export-AzBlueprintWithArtifact -Blueprint $bp -Version 1.0 -OutputPath C:\Blueprints
```

<span data-ttu-id="b3fe6-110">Экспортируйте определение чертежа вместе с артефактами и сохраните его на диск.</span><span class="sxs-lookup"><span data-stu-id="b3fe6-110">Export a blueprint definition with its artifacts and save to disk.</span></span>

## <span data-ttu-id="b3fe6-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b3fe6-111">PARAMETERS</span></span>

### <span data-ttu-id="b3fe6-112">-Чертеж</span><span class="sxs-lookup"><span data-stu-id="b3fe6-112">-Blueprint</span></span>
<span data-ttu-id="b3fe6-113">Объект определения чертежей, который нужно экспортировать.</span><span class="sxs-lookup"><span data-stu-id="b3fe6-113">The blueprint definition object to export.</span></span>

```yaml
Type: PSBlueprintBase
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b3fe6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3fe6-114">-DefaultProfile</span></span>
<span data-ttu-id="b3fe6-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b3fe6-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3fe6-116">-Force</span><span class="sxs-lookup"><span data-stu-id="b3fe6-116">-Force</span></span>
<span data-ttu-id="b3fe6-117">Если задано значение "true", при выполнении не будет запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="b3fe6-117">When set to true, execution will not ask for a confirmation.</span></span>

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

### <span data-ttu-id="b3fe6-118">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="b3fe6-118">-OutputPath</span></span>
<span data-ttu-id="b3fe6-119">Путь к файлу на диске, на который нужно экспортировать определение чертежа в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="b3fe6-119">Path to a file on disk where to export the Blueprint definition in JSON format.</span></span>

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

### <span data-ttu-id="b3fe6-120">-Version</span><span class="sxs-lookup"><span data-stu-id="b3fe6-120">-Version</span></span>
<span data-ttu-id="b3fe6-121">Версия определений опубликованных чертежей.</span><span class="sxs-lookup"><span data-stu-id="b3fe6-121">Published blueprint definition version.</span></span>

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

### <span data-ttu-id="b3fe6-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3fe6-122">CommonParameters</span></span>
<span data-ttu-id="b3fe6-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b3fe6-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="b3fe6-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3fe6-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3fe6-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b3fe6-125">INPUTS</span></span>

### <span data-ttu-id="b3fe6-126">Microsoft. Azure. Commands. чертеж. Models. PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="b3fe6-126">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="b3fe6-127">System. String</span><span class="sxs-lookup"><span data-stu-id="b3fe6-127">System.String</span></span>

## <span data-ttu-id="b3fe6-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b3fe6-128">OUTPUTS</span></span>

### <span data-ttu-id="b3fe6-129">System. String</span><span class="sxs-lookup"><span data-stu-id="b3fe6-129">System.String</span></span>

## <span data-ttu-id="b3fe6-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="b3fe6-130">NOTES</span></span>

## <span data-ttu-id="b3fe6-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b3fe6-131">RELATED LINKS</span></span>
