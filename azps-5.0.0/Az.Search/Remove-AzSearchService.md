---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/remove-azsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchService.md
ms.openlocfilehash: 62b8dff0b2d5fc52b080b35e4a205ad2bb00ea52
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248187"
---
# <span data-ttu-id="8dfd8-101">Remove-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="8dfd8-101">Remove-AzSearchService</span></span>

## <span data-ttu-id="8dfd8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8dfd8-102">SYNOPSIS</span></span>
<span data-ttu-id="8dfd8-103">Удалите службу поиска Azure.</span><span class="sxs-lookup"><span data-stu-id="8dfd8-103">Remove an Azure Search service.</span></span>

## <span data-ttu-id="8dfd8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8dfd8-104">SYNTAX</span></span>

### <span data-ttu-id="8dfd8-105">ResourceNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8dfd8-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzSearchService [-ResourceGroupName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8dfd8-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8dfd8-106">InputObjectParameterSet</span></span>
```
Remove-AzSearchService [-InputObject] <PSSearchService> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8dfd8-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8dfd8-107">ResourceIdParameterSet</span></span>
```
Remove-AzSearchService [-ResourceId] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8dfd8-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8dfd8-108">DESCRIPTION</span></span>
<span data-ttu-id="8dfd8-109">Командлет **Remove-AzSearchService** Удаляет службу поиска Azure с указанными параметрами.</span><span class="sxs-lookup"><span data-stu-id="8dfd8-109">The **Remove-AzSearchService** cmdlet removes an Azure Search service with specified parameters.</span></span>

## <span data-ttu-id="8dfd8-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8dfd8-110">EXAMPLES</span></span>

### <span data-ttu-id="8dfd8-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8dfd8-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSearchService -ResourceGroupName "TestAzureSearchPsGroup" -Name "pstestazuresearch01"

Confirm
Are you sure you want to remove Search Service 'pstestazuresearch01'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
PS C:\>
```

<span data-ttu-id="8dfd8-112">В примере удаляется служба поиска Azure.</span><span class="sxs-lookup"><span data-stu-id="8dfd8-112">The example removes an Azure Search service.</span></span>

## <span data-ttu-id="8dfd8-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8dfd8-113">PARAMETERS</span></span>

### <span data-ttu-id="8dfd8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8dfd8-114">-DefaultProfile</span></span>
<span data-ttu-id="8dfd8-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8dfd8-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8dfd8-116">-Force</span><span class="sxs-lookup"><span data-stu-id="8dfd8-116">-Force</span></span>
<span data-ttu-id="8dfd8-117">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="8dfd8-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="8dfd8-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8dfd8-118">-InputObject</span></span>
<span data-ttu-id="8dfd8-119">Объект ввода службы поиска.</span><span class="sxs-lookup"><span data-stu-id="8dfd8-119">Search Service Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSearchService
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8dfd8-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8dfd8-120">-Name</span></span>
<span data-ttu-id="8dfd8-121">Имя службы поиска.</span><span class="sxs-lookup"><span data-stu-id="8dfd8-121">Search Service name.</span></span>

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

### <span data-ttu-id="8dfd8-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8dfd8-122">-PassThru</span></span>
<span data-ttu-id="8dfd8-123">Этот командлет не возвращает объект по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8dfd8-123">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="8dfd8-124">Если этот параметр указан, функция возвращает значение истина, если операция завершилась успешно.</span><span class="sxs-lookup"><span data-stu-id="8dfd8-124">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="8dfd8-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8dfd8-125">-ResourceGroupName</span></span>
<span data-ttu-id="8dfd8-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8dfd8-126">Resource Group name.</span></span>

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

### <span data-ttu-id="8dfd8-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8dfd8-127">-ResourceId</span></span>
<span data-ttu-id="8dfd8-128">Идентификатор ресурса службы поиска.</span><span class="sxs-lookup"><span data-stu-id="8dfd8-128">Search Service Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8dfd8-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8dfd8-129">-Confirm</span></span>
<span data-ttu-id="8dfd8-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8dfd8-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8dfd8-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8dfd8-131">-WhatIf</span></span>
<span data-ttu-id="8dfd8-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8dfd8-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8dfd8-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8dfd8-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8dfd8-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8dfd8-134">CommonParameters</span></span>
<span data-ttu-id="8dfd8-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8dfd8-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8dfd8-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8dfd8-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8dfd8-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8dfd8-137">INPUTS</span></span>

### <span data-ttu-id="8dfd8-138">Microsoft. Azure. Commands. Management. Search. Models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="8dfd8-138">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="8dfd8-139">System. String</span><span class="sxs-lookup"><span data-stu-id="8dfd8-139">System.String</span></span>

## <span data-ttu-id="8dfd8-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8dfd8-140">OUTPUTS</span></span>

### <span data-ttu-id="8dfd8-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8dfd8-141">System.Boolean</span></span>

## <span data-ttu-id="8dfd8-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="8dfd8-142">NOTES</span></span>

## <span data-ttu-id="8dfd8-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8dfd8-143">RELATED LINKS</span></span>

[<span data-ttu-id="8dfd8-144">New-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="8dfd8-144">New-AzSearchService</span></span>](./New-AzSearchService.md)

[<span data-ttu-id="8dfd8-145">Get-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="8dfd8-145">Get-AzSearchService</span></span>](./Get-AzSearchService.md)

[<span data-ttu-id="8dfd8-146">Set-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="8dfd8-146">Set-AzSearchService</span></span>](./Set-AzSearchService.md)

