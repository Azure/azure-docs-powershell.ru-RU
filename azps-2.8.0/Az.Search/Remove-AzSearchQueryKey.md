---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/remove-azsearchquerykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchQueryKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchQueryKey.md
ms.openlocfilehash: ae781b4c53e373cdbd8338f4db75d6913c863bfd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93903933"
---
# <span data-ttu-id="349a3-101">Remove-AzSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="349a3-101">Remove-AzSearchQueryKey</span></span>

## <span data-ttu-id="349a3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="349a3-102">SYNOPSIS</span></span>
<span data-ttu-id="349a3-103">Удалите ключ запроса из службы поиска Azure.</span><span class="sxs-lookup"><span data-stu-id="349a3-103">Remove the query key from the Azure Search service.</span></span>

## <span data-ttu-id="349a3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="349a3-104">SYNTAX</span></span>

### <span data-ttu-id="349a3-105">ResourceNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="349a3-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzSearchQueryKey [-ResourceGroupName] <String> [-ServiceName] <String> -KeyValue <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="349a3-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="349a3-106">ParentObjectParameterSet</span></span>
```
Remove-AzSearchQueryKey [-ParentObject] <PSSearchService> -KeyValue <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="349a3-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="349a3-107">ParentResourceIdParameterSet</span></span>
```
Remove-AzSearchQueryKey [-ParentResourceId] <String> -KeyValue <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="349a3-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="349a3-108">DESCRIPTION</span></span>
<span data-ttu-id="349a3-109">Командлет **Remove-AzSearchQueryKey** удаляет ключ запроса из службы поиска Azure.</span><span class="sxs-lookup"><span data-stu-id="349a3-109">The **Remove-AzSearchQueryKey** cmdlet removes the query key from the Azure Search service.</span></span>

## <span data-ttu-id="349a3-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="349a3-110">EXAMPLES</span></span>

### <span data-ttu-id="349a3-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="349a3-111">Example 1</span></span>
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

<span data-ttu-id="349a3-112">В примере удаляется ключ запроса из службы поиска Azure.</span><span class="sxs-lookup"><span data-stu-id="349a3-112">The example removes the query key from the Azure Search service.</span></span>

## <span data-ttu-id="349a3-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="349a3-113">PARAMETERS</span></span>

### <span data-ttu-id="349a3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="349a3-114">-DefaultProfile</span></span>
<span data-ttu-id="349a3-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="349a3-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="349a3-116">-Force</span><span class="sxs-lookup"><span data-stu-id="349a3-116">-Force</span></span>
<span data-ttu-id="349a3-117">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="349a3-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="349a3-118">-KeyValue</span><span class="sxs-lookup"><span data-stu-id="349a3-118">-KeyValue</span></span>
<span data-ttu-id="349a3-119">Значение ключа запроса службы поиска.</span><span class="sxs-lookup"><span data-stu-id="349a3-119">Search Service query key value.</span></span>

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

### <span data-ttu-id="349a3-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="349a3-120">-ParentObject</span></span>
<span data-ttu-id="349a3-121">Объект ввода службы поиска.</span><span class="sxs-lookup"><span data-stu-id="349a3-121">Search Service Input Object.</span></span>

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

### <span data-ttu-id="349a3-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="349a3-122">-ParentResourceId</span></span>
<span data-ttu-id="349a3-123">Идентификатор ресурса службы поиска.</span><span class="sxs-lookup"><span data-stu-id="349a3-123">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="349a3-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="349a3-124">-PassThru</span></span>
<span data-ttu-id="349a3-125">Этот командлет не возвращает объект по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="349a3-125">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="349a3-126">Если этот параметр указан, функция возвращает значение истина, если операция завершилась успешно.</span><span class="sxs-lookup"><span data-stu-id="349a3-126">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="349a3-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="349a3-127">-ResourceGroupName</span></span>
<span data-ttu-id="349a3-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="349a3-128">Resource Group name.</span></span>

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

### <span data-ttu-id="349a3-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="349a3-129">-ServiceName</span></span>
<span data-ttu-id="349a3-130">Имя службы поиска.</span><span class="sxs-lookup"><span data-stu-id="349a3-130">Search Service name.</span></span>

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

### <span data-ttu-id="349a3-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="349a3-131">-Confirm</span></span>
<span data-ttu-id="349a3-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="349a3-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="349a3-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="349a3-133">-WhatIf</span></span>
<span data-ttu-id="349a3-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="349a3-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="349a3-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="349a3-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="349a3-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="349a3-136">CommonParameters</span></span>
<span data-ttu-id="349a3-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="349a3-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="349a3-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="349a3-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="349a3-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="349a3-139">INPUTS</span></span>

### <span data-ttu-id="349a3-140">Microsoft. Azure. Commands. Management. Search. Models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="349a3-140">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="349a3-141">System. String</span><span class="sxs-lookup"><span data-stu-id="349a3-141">System.String</span></span>

## <span data-ttu-id="349a3-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="349a3-142">OUTPUTS</span></span>

### <span data-ttu-id="349a3-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="349a3-143">System.Boolean</span></span>

## <span data-ttu-id="349a3-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="349a3-144">NOTES</span></span>

## <span data-ttu-id="349a3-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="349a3-145">RELATED LINKS</span></span>

[<span data-ttu-id="349a3-146">New-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="349a3-146">New-AzSearchQueryKey.md</span></span>](./New-AzSearchQueryKey.md)

[<span data-ttu-id="349a3-147">Get-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="349a3-147">Get-AzSearchQueryKey.md</span></span>](./Get-AzSearchQueryKey.md)
