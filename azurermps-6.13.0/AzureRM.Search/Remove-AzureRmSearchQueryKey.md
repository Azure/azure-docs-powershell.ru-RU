---
external help file: Microsoft.Azure.Commands.Management.Search.dll-Help.xml
Module Name: AzureRM.Search
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.search/remove-azurermsearchquerykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/Remove-AzureRmSearchQueryKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/Remove-AzureRmSearchQueryKey.md
ms.openlocfilehash: 1dbdf342335ca204287ccfd2efea737f2eb747fe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566766"
---
# <span data-ttu-id="1e175-101">Remove-AzureRmSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="1e175-101">Remove-AzureRmSearchQueryKey</span></span>

## <span data-ttu-id="1e175-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1e175-102">SYNOPSIS</span></span>
<span data-ttu-id="1e175-103">Удалите ключ запроса из службы поиска Azure.</span><span class="sxs-lookup"><span data-stu-id="1e175-103">Remove the query key from the Azure Search service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1e175-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1e175-104">SYNTAX</span></span>

### <span data-ttu-id="1e175-105">ResourceNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1e175-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzureRmSearchQueryKey [-ResourceGroupName] <String> [-ServiceName] <String> -KeyValue <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e175-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1e175-106">ParentObjectParameterSet</span></span>
```
Remove-AzureRmSearchQueryKey [-ParentObject] <PSSearchService> -KeyValue <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e175-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1e175-107">ParentResourceIdParameterSet</span></span>
```
Remove-AzureRmSearchQueryKey [-ParentResourceId] <String> -KeyValue <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e175-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1e175-108">DESCRIPTION</span></span>
<span data-ttu-id="1e175-109">Командлет **Remove-AzureRmSearchQueryKey** удаляет ключ запроса из службы поиска Azure.</span><span class="sxs-lookup"><span data-stu-id="1e175-109">The **Remove-AzureRmSearchQueryKey** cmdlet removes the query key from the Azure Search service.</span></span>

## <span data-ttu-id="1e175-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1e175-110">EXAMPLES</span></span>

### <span data-ttu-id="1e175-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1e175-111">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmSearchQueryKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01"

Name         Key                             
----         ---                             
             D260F448EA192EBC19D59F7E5670E8BB
NewQueryKey1 B4C13E3F6FA76100D3488673CFDCD438

PS C:\> Remove-AzureRmSearchQueryKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01" -KeyValue B4C13E3F6FA76100D3488673CFDCD438

Confirm
Are you sure you want to remove query key 'B4C13E3F6FA76100D3488673CFDCD438'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
PS C:\>
```

<span data-ttu-id="1e175-112">В примере удаляется ключ запроса из службы поиска Azure.</span><span class="sxs-lookup"><span data-stu-id="1e175-112">The example removes the query key from the Azure Search service.</span></span>

## <span data-ttu-id="1e175-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1e175-113">PARAMETERS</span></span>

### <span data-ttu-id="1e175-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e175-114">-DefaultProfile</span></span>
<span data-ttu-id="1e175-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1e175-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e175-116">-Force</span><span class="sxs-lookup"><span data-stu-id="1e175-116">-Force</span></span>
<span data-ttu-id="1e175-117">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="1e175-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="1e175-118">-KeyValue</span><span class="sxs-lookup"><span data-stu-id="1e175-118">-KeyValue</span></span>
<span data-ttu-id="1e175-119">Значение ключа запроса службы поиска.</span><span class="sxs-lookup"><span data-stu-id="1e175-119">Search Service query key value.</span></span>

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

### <span data-ttu-id="1e175-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="1e175-120">-ParentObject</span></span>
<span data-ttu-id="1e175-121">Объект ввода службы поиска.</span><span class="sxs-lookup"><span data-stu-id="1e175-121">Search Service Input Object.</span></span>

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

### <span data-ttu-id="1e175-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="1e175-122">-ParentResourceId</span></span>
<span data-ttu-id="1e175-123">Идентификатор ресурса службы поиска.</span><span class="sxs-lookup"><span data-stu-id="1e175-123">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="1e175-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1e175-124">-PassThru</span></span>
<span data-ttu-id="1e175-125">Этот командлет не возвращает объект по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1e175-125">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="1e175-126">Если этот параметр указан, функция возвращает значение истина, если операция завершилась успешно.</span><span class="sxs-lookup"><span data-stu-id="1e175-126">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="1e175-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e175-127">-ResourceGroupName</span></span>
<span data-ttu-id="1e175-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1e175-128">Resource Group name.</span></span>

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

### <span data-ttu-id="1e175-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="1e175-129">-ServiceName</span></span>
<span data-ttu-id="1e175-130">Имя службы поиска.</span><span class="sxs-lookup"><span data-stu-id="1e175-130">Search Service name.</span></span>

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

### <span data-ttu-id="1e175-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1e175-131">-Confirm</span></span>
<span data-ttu-id="1e175-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1e175-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e175-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e175-133">-WhatIf</span></span>
<span data-ttu-id="1e175-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1e175-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e175-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1e175-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e175-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e175-136">CommonParameters</span></span>
<span data-ttu-id="1e175-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1e175-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e175-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e175-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e175-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1e175-139">INPUTS</span></span>

### <span data-ttu-id="1e175-140">Microsoft. Azure. Commands. Management. Search. Models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="1e175-140">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>
<span data-ttu-id="1e175-141">Параметры: ParentObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="1e175-141">Parameters: ParentObject (ByValue)</span></span>

### <span data-ttu-id="1e175-142">System. String</span><span class="sxs-lookup"><span data-stu-id="1e175-142">System.String</span></span>

## <span data-ttu-id="1e175-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1e175-143">OUTPUTS</span></span>

### <span data-ttu-id="1e175-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1e175-144">System.Boolean</span></span>

## <span data-ttu-id="1e175-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="1e175-145">NOTES</span></span>

## <span data-ttu-id="1e175-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1e175-146">RELATED LINKS</span></span>

[<span data-ttu-id="1e175-147">New-AzureRmSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="1e175-147">New-AzureRmSearchQueryKey.md</span></span>](./New-AzureRmSearchQueryKey.md)

[<span data-ttu-id="1e175-148">Get-AzureRmSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="1e175-148">Get-AzureRmSearchQueryKey.md</span></span>](./Get-AzureRmSearchQueryKey.md)
