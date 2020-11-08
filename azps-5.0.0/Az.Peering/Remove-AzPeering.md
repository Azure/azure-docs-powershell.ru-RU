---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/remove-azpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeering.md
ms.openlocfilehash: 414a732dd80850a31a87f88d3dfdbf091cb4a6a6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249185"
---
# <span data-ttu-id="55200-101">Remove-AzPeering</span><span class="sxs-lookup"><span data-stu-id="55200-101">Remove-AzPeering</span></span>

## <span data-ttu-id="55200-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="55200-102">SYNOPSIS</span></span>
<span data-ttu-id="55200-103">Удаление и удаление одноранговых элементов.</span><span class="sxs-lookup"><span data-stu-id="55200-103">Delete or remove a peering.</span></span> <span data-ttu-id="55200-104">Будут удалены все дочерние ресурсы и уведомления о ресурсе.</span><span class="sxs-lookup"><span data-stu-id="55200-104">This will delete all child resources or alerting on the resource.</span></span>

## <span data-ttu-id="55200-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="55200-105">SYNTAX</span></span>

### <span data-ttu-id="55200-106">ByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="55200-106">ByName (Default)</span></span>
```
Remove-AzPeering [-ResourceGroupName] <String> [-Name] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55200-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="55200-107">InputObject</span></span>
```
Remove-AzPeering [-InputObject] <PSPeering> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55200-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="55200-108">ByResourceId</span></span>
```
Remove-AzPeering -ResourceId <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55200-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="55200-109">DESCRIPTION</span></span>
<span data-ttu-id="55200-110">Perminently удалить ресурс пиринга.</span><span class="sxs-lookup"><span data-stu-id="55200-110">Perminently delete a peering resource.</span></span>

## <span data-ttu-id="55200-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="55200-111">EXAMPLES</span></span>

### <span data-ttu-id="55200-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="55200-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzPeering -ResourceId $resourceId
```

<span data-ttu-id="55200-113">Удаление однорангового соединения по идентификатору ресурса.</span><span class="sxs-lookup"><span data-stu-id="55200-113">Remove a peering by resource id.</span></span>

## <span data-ttu-id="55200-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="55200-114">PARAMETERS</span></span>

### <span data-ttu-id="55200-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="55200-115">-AsJob</span></span>
<span data-ttu-id="55200-116">Выполнение в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="55200-116">Run in the background.</span></span>

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

### <span data-ttu-id="55200-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55200-117">-DefaultProfile</span></span>
<span data-ttu-id="55200-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="55200-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="55200-119">-Force</span><span class="sxs-lookup"><span data-stu-id="55200-119">-Force</span></span>
<span data-ttu-id="55200-120">Принудительно завершить операцию</span><span class="sxs-lookup"><span data-stu-id="55200-120">Force the operation to complete</span></span>

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

### <span data-ttu-id="55200-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="55200-121">-InputObject</span></span>
<span data-ttu-id="55200-122">Чтобы получить этот объект, используйте Get-AzPeering.</span><span class="sxs-lookup"><span data-stu-id="55200-122">Use Get-AzPeering to retrieve this object.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="55200-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="55200-123">-Name</span></span>
<span data-ttu-id="55200-124">Уникальное имя PSPeering.</span><span class="sxs-lookup"><span data-stu-id="55200-124">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55200-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="55200-125">-PassThru</span></span>
<span data-ttu-id="55200-126">Возвращает значение истина, если завершено</span><span class="sxs-lookup"><span data-stu-id="55200-126">Return true if complete</span></span>

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

### <span data-ttu-id="55200-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55200-127">-ResourceGroupName</span></span>
<span data-ttu-id="55200-128">Создание или использование существующего имени группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="55200-128">The create or use an existing resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55200-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="55200-129">-ResourceId</span></span>
<span data-ttu-id="55200-130">Имя строки идентификатора ресурса.</span><span class="sxs-lookup"><span data-stu-id="55200-130">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55200-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="55200-131">-Confirm</span></span>
<span data-ttu-id="55200-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="55200-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55200-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55200-133">-WhatIf</span></span>
<span data-ttu-id="55200-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="55200-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55200-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="55200-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55200-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55200-136">CommonParameters</span></span>
<span data-ttu-id="55200-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="55200-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55200-138">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="55200-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55200-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="55200-139">INPUTS</span></span>

### <span data-ttu-id="55200-140">Microsoft. Azure. PowerShell. командлеты. Peer (Models. PSPeering)</span><span class="sxs-lookup"><span data-stu-id="55200-140">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="55200-141">System. String</span><span class="sxs-lookup"><span data-stu-id="55200-141">System.String</span></span>

## <span data-ttu-id="55200-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="55200-142">OUTPUTS</span></span>

### <span data-ttu-id="55200-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="55200-143">System.Boolean</span></span>

## <span data-ttu-id="55200-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="55200-144">NOTES</span></span>

## <span data-ttu-id="55200-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="55200-145">RELATED LINKS</span></span>
