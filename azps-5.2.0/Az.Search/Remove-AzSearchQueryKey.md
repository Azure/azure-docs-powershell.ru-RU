---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/remove-azsearchquerykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchQueryKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchQueryKey.md
ms.openlocfilehash: e7a74fcc6d5e1a80282cfb365070df1b339aea45
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98406911"
---
# <span data-ttu-id="d50a1-101">Remove-AzSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="d50a1-101">Remove-AzSearchQueryKey</span></span>

## <span data-ttu-id="d50a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d50a1-102">SYNOPSIS</span></span>
<span data-ttu-id="d50a1-103">Удалите ключ запроса из службы поиска Azure.</span><span class="sxs-lookup"><span data-stu-id="d50a1-103">Remove the query key from the Azure Search service.</span></span>

## <span data-ttu-id="d50a1-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d50a1-104">SYNTAX</span></span>

### <span data-ttu-id="d50a1-105">ResourceNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d50a1-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzSearchQueryKey [-ResourceGroupName] <String> [-ServiceName] <String> -KeyValue <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d50a1-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d50a1-106">ParentObjectParameterSet</span></span>
```
Remove-AzSearchQueryKey [-ParentObject] <PSSearchService> -KeyValue <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d50a1-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d50a1-107">ParentResourceIdParameterSet</span></span>
```
Remove-AzSearchQueryKey [-ParentResourceId] <String> -KeyValue <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d50a1-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d50a1-108">DESCRIPTION</span></span>
<span data-ttu-id="d50a1-109">При **нажатии на клавишу Remove-AzSearchQueryKey** ключ запроса удаляется из службы поиска Azure.</span><span class="sxs-lookup"><span data-stu-id="d50a1-109">The **Remove-AzSearchQueryKey** cmdlet removes the query key from the Azure Search service.</span></span>

## <span data-ttu-id="d50a1-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d50a1-110">EXAMPLES</span></span>

### <span data-ttu-id="d50a1-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d50a1-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSearchQueryKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01"

Name         Key                             
----         ---                             
             D260F448EA192EBC19D59F7E5670E8BB
NewQueryKey1 B4C13E3F6FA76100D3488673CFDCD438

PS C:\> Remove-AzSearchQueryKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01" -KeyValue B4C13E3F6FA76100D3488673CFDCD438

Confirm
Are you sure you want to remove query key 'B4C13E3F6FA76100D3488673CFDCD438'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
PS C:\>
```

<span data-ttu-id="d50a1-112">В этом примере ключ запроса удаляется из службы поиска Azure.</span><span class="sxs-lookup"><span data-stu-id="d50a1-112">The example removes the query key from the Azure Search service.</span></span>

## <span data-ttu-id="d50a1-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d50a1-113">PARAMETERS</span></span>

### <span data-ttu-id="d50a1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d50a1-114">-DefaultProfile</span></span>
<span data-ttu-id="d50a1-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d50a1-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d50a1-116">-Force</span><span class="sxs-lookup"><span data-stu-id="d50a1-116">-Force</span></span>
<span data-ttu-id="d50a1-117">Не спрашивайте подтверждения.</span><span class="sxs-lookup"><span data-stu-id="d50a1-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="d50a1-118">-KeyValue</span><span class="sxs-lookup"><span data-stu-id="d50a1-118">-KeyValue</span></span>
<span data-ttu-id="d50a1-119">Значение ключа запроса службы поиска.</span><span class="sxs-lookup"><span data-stu-id="d50a1-119">Search Service query key value.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d50a1-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="d50a1-120">-ParentObject</span></span>
<span data-ttu-id="d50a1-121">Объект ввода службы поиска.</span><span class="sxs-lookup"><span data-stu-id="d50a1-121">Search Service Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSearchService
Parameter Sets: ParentObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d50a1-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="d50a1-122">-ParentResourceId</span></span>
<span data-ttu-id="d50a1-123">ИД ресурса службы поиска.</span><span class="sxs-lookup"><span data-stu-id="d50a1-123">Search Service Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ParentResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d50a1-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d50a1-124">-PassThru</span></span>
<span data-ttu-id="d50a1-125">Этот cmdlet не возвращает объект по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d50a1-125">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="d50a1-126">Если этот переключатель задан, возвращается истина, если он успешен.</span><span class="sxs-lookup"><span data-stu-id="d50a1-126">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="d50a1-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d50a1-127">-ResourceGroupName</span></span>
<span data-ttu-id="d50a1-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d50a1-128">Resource Group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d50a1-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="d50a1-129">-ServiceName</span></span>
<span data-ttu-id="d50a1-130">Название службы поиска.</span><span class="sxs-lookup"><span data-stu-id="d50a1-130">Search Service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d50a1-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d50a1-131">-Confirm</span></span>
<span data-ttu-id="d50a1-132">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d50a1-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d50a1-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d50a1-133">-WhatIf</span></span>
<span data-ttu-id="d50a1-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d50a1-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d50a1-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="d50a1-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d50a1-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d50a1-136">CommonParameters</span></span>
<span data-ttu-id="d50a1-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d50a1-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d50a1-138">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d50a1-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d50a1-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d50a1-139">INPUTS</span></span>

### <span data-ttu-id="d50a1-140">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="d50a1-140">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="d50a1-141">System.String</span><span class="sxs-lookup"><span data-stu-id="d50a1-141">System.String</span></span>

## <span data-ttu-id="d50a1-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d50a1-142">OUTPUTS</span></span>

### <span data-ttu-id="d50a1-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d50a1-143">System.Boolean</span></span>

## <span data-ttu-id="d50a1-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d50a1-144">NOTES</span></span>

## <span data-ttu-id="d50a1-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d50a1-145">RELATED LINKS</span></span>

[<span data-ttu-id="d50a1-146">New-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="d50a1-146">New-AzSearchQueryKey.md</span></span>](./New-AzSearchQueryKey.md)

[<span data-ttu-id="d50a1-147">Get-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="d50a1-147">Get-AzSearchQueryKey.md</span></span>](./Get-AzSearchQueryKey.md)
