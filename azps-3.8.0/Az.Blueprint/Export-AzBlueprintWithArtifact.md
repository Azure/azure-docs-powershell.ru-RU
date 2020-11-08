---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/export-azblueprintwithartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Export-AzBlueprintWithArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Export-AzBlueprintWithArtifact.md
ms.openlocfilehash: 2136a224a5d187951b77c6f48e0b610b48b021b4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066848"
---
# <span data-ttu-id="4e300-101">Export-AzBlueprintWithArtifact</span><span class="sxs-lookup"><span data-stu-id="4e300-101">Export-AzBlueprintWithArtifact</span></span>

## <span data-ttu-id="4e300-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4e300-102">SYNOPSIS</span></span>
<span data-ttu-id="4e300-103">Экспортировать определение указанного чертежа в указанное расположение выходных файлов в виде JSON-файла.</span><span class="sxs-lookup"><span data-stu-id="4e300-103">Export specified blueprint definition to the specified output location as a JSON file.</span></span> 

## <span data-ttu-id="4e300-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4e300-104">SYNTAX</span></span>

```
Export-AzBlueprintWithArtifact -Blueprint <PSBlueprintBase> -OutputPath <String> [-Version <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4e300-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4e300-105">DESCRIPTION</span></span>
<span data-ttu-id="4e300-106">Экспортируйте определение чертежа вместе с артефактами и сохраните его на диск.</span><span class="sxs-lookup"><span data-stu-id="4e300-106">Export a blueprint definition with its artifacts and save to disk.</span></span> <span data-ttu-id="4e300-107">Этот командлет экспортирует последнюю версию проекта (черновика или опубликована).</span><span class="sxs-lookup"><span data-stu-id="4e300-107">This cmdlet exports the latest version(draft or published) of the blueprint.</span></span>

## <span data-ttu-id="4e300-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4e300-108">EXAMPLES</span></span>

### <span data-ttu-id="4e300-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4e300-109">Example 1</span></span>
```powershell
PS C:\> $bp = Get-AzBlueprint -Name SimpleBlueprint
PS C:\> Export-AzBlueprintWithArtifact -Blueprint $bp -Version 1.0 -OutputPath C:\Blueprints
```

<span data-ttu-id="4e300-110">Экспортируйте определение чертежа вместе с артефактами и сохраните его на диск.</span><span class="sxs-lookup"><span data-stu-id="4e300-110">Export a blueprint definition with its artifacts and save to disk.</span></span>

## <span data-ttu-id="4e300-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4e300-111">PARAMETERS</span></span>

### <span data-ttu-id="4e300-112">-Чертеж</span><span class="sxs-lookup"><span data-stu-id="4e300-112">-Blueprint</span></span>
<span data-ttu-id="4e300-113">Объект определения чертежей, который нужно экспортировать.</span><span class="sxs-lookup"><span data-stu-id="4e300-113">The blueprint definition object to export.</span></span>

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

### <span data-ttu-id="4e300-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e300-114">-DefaultProfile</span></span>
<span data-ttu-id="4e300-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4e300-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e300-116">-Force</span><span class="sxs-lookup"><span data-stu-id="4e300-116">-Force</span></span>
<span data-ttu-id="4e300-117">Если задано значение "true", при выполнении не будет запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="4e300-117">When set to true, execution will not ask for a confirmation.</span></span>

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

### <span data-ttu-id="4e300-118">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="4e300-118">-OutputPath</span></span>
<span data-ttu-id="4e300-119">Путь к файлу на диске, на который нужно экспортировать определение чертежа в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="4e300-119">Path to a file on disk where to export the Blueprint definition in JSON format.</span></span>

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

### <span data-ttu-id="4e300-120">-Version</span><span class="sxs-lookup"><span data-stu-id="4e300-120">-Version</span></span>
<span data-ttu-id="4e300-121">Версия определений опубликованных чертежей.</span><span class="sxs-lookup"><span data-stu-id="4e300-121">Published blueprint definition version.</span></span>

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

### <span data-ttu-id="4e300-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e300-122">CommonParameters</span></span>
<span data-ttu-id="4e300-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4e300-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="4e300-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e300-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e300-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4e300-125">INPUTS</span></span>

### <span data-ttu-id="4e300-126">Microsoft. Azure. Commands. чертеж. Models. PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="4e300-126">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="4e300-127">System. String</span><span class="sxs-lookup"><span data-stu-id="4e300-127">System.String</span></span>

## <span data-ttu-id="4e300-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4e300-128">OUTPUTS</span></span>

### <span data-ttu-id="4e300-129">System. String</span><span class="sxs-lookup"><span data-stu-id="4e300-129">System.String</span></span>

## <span data-ttu-id="4e300-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="4e300-130">NOTES</span></span>

## <span data-ttu-id="4e300-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4e300-131">RELATED LINKS</span></span>
