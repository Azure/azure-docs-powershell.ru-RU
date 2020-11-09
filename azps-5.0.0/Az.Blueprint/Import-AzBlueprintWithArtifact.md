---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/import-azblueprintwithartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Import-AzBlueprintWithArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Import-AzBlueprintWithArtifact.md
ms.openlocfilehash: 43877ecb7fe7e90f0619a26a54eea534ac1390b3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246110"
---
# <span data-ttu-id="f0218-101">Import-AzBlueprintWithArtifact</span><span class="sxs-lookup"><span data-stu-id="f0218-101">Import-AzBlueprintWithArtifact</span></span>

## <span data-ttu-id="f0218-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f0218-102">SYNOPSIS</span></span>
<span data-ttu-id="f0218-103">Импортируйте файл в формате JSON в объект чертежа и сохраните его в указанной подписке или группе управления.</span><span class="sxs-lookup"><span data-stu-id="f0218-103">Import a blueprint file in JSON format to a blueprint object and save it within the specified subscription or management group.</span></span>

## <span data-ttu-id="f0218-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f0218-104">SYNTAX</span></span>

```
Import-AzBlueprintWithArtifact -Name <String> [-SubscriptionId <String>] [-ManagementGroupId <String>]
 -InputPath <String> [-IncludeSubFolders] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0218-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f0218-105">DESCRIPTION</span></span>
<span data-ttu-id="f0218-106">Импортируйте определение чертежа с его артефактами.</span><span class="sxs-lookup"><span data-stu-id="f0218-106">Import a blueprint definition with its artifacts.</span></span> 

## <span data-ttu-id="f0218-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f0218-107">EXAMPLES</span></span>

### <span data-ttu-id="f0218-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f0218-108">Example 1</span></span>
```powershell
PS C:\> Import-AzBlueprintWithArtifact -Name MySimpleBlueprint -SubscriptionId 00000000-1111-0000-1111-000000000000 -InputPath  C:\Blueprints\SimpleBlueprint
```

<span data-ttu-id="f0218-109">Импортируйте определение чертежа с артефактами и сохраните его в рамках подписки.</span><span class="sxs-lookup"><span data-stu-id="f0218-109">Import a blueprint definition with its artifacts and save within a subscription.</span></span>

## <span data-ttu-id="f0218-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f0218-110">PARAMETERS</span></span>

### <span data-ttu-id="f0218-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0218-111">-DefaultProfile</span></span>
<span data-ttu-id="f0218-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f0218-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f0218-113">-Force</span><span class="sxs-lookup"><span data-stu-id="f0218-113">-Force</span></span>
<span data-ttu-id="f0218-114">Если задано значение "true", при выполнении не будет запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="f0218-114">When set to true, execution will not ask for a confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0218-115">-IncludeSubFolders</span><span class="sxs-lookup"><span data-stu-id="f0218-115">-IncludeSubFolders</span></span>
<span data-ttu-id="f0218-116">Если установлено значение true, артефакты во вложенных папках будут включены.</span><span class="sxs-lookup"><span data-stu-id="f0218-116">When set to true, artifact in the subfolders will be included.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0218-117">-InputPath</span><span class="sxs-lookup"><span data-stu-id="f0218-117">-InputPath</span></span>
<span data-ttu-id="f0218-118">Путь к JSON-файлу, который планируется на диске.</span><span class="sxs-lookup"><span data-stu-id="f0218-118">Path to a Blueprint JSON file on disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0218-119">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="f0218-119">-ManagementGroupId</span></span>
<span data-ttu-id="f0218-120">Идентификатор группы управления, в которой должно быть сохранено определение.</span><span class="sxs-lookup"><span data-stu-id="f0218-120">Management Group Id where the blueprint definition is or will be saved.</span></span>

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

### <span data-ttu-id="f0218-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f0218-121">-Name</span></span>
<span data-ttu-id="f0218-122">Имя определения чертежа.</span><span class="sxs-lookup"><span data-stu-id="f0218-122">Blueprint definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0218-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f0218-123">-PassThru</span></span>
<span data-ttu-id="f0218-124">При установке командлет возвращает объект, который представляет собой импортированное определение собственного чертежа.</span><span class="sxs-lookup"><span data-stu-id="f0218-124">When set, the cmdlet will return an object representing the imported blueprint definition.</span></span> <span data-ttu-id="f0218-125">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="f0218-125">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0218-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f0218-126">-SubscriptionId</span></span>
<span data-ttu-id="f0218-127">Идентификатор подписки, в которой должно быть сохранено определение.</span><span class="sxs-lookup"><span data-stu-id="f0218-127">Subscription Id where the blueprint definition is or will be saved.</span></span>

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

### <span data-ttu-id="f0218-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f0218-128">-Confirm</span></span>
<span data-ttu-id="f0218-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f0218-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0218-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0218-130">-WhatIf</span></span>
<span data-ttu-id="f0218-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f0218-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f0218-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f0218-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0218-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0218-133">CommonParameters</span></span>
<span data-ttu-id="f0218-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f0218-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0218-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f0218-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0218-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f0218-136">INPUTS</span></span>

### <span data-ttu-id="f0218-137">System. String</span><span class="sxs-lookup"><span data-stu-id="f0218-137">System.String</span></span>

## <span data-ttu-id="f0218-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f0218-138">OUTPUTS</span></span>

### <span data-ttu-id="f0218-139">System. String</span><span class="sxs-lookup"><span data-stu-id="f0218-139">System.String</span></span>

## <span data-ttu-id="f0218-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="f0218-140">NOTES</span></span>

## <span data-ttu-id="f0218-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f0218-141">RELATED LINKS</span></span>