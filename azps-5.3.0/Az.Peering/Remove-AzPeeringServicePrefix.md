---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/remove-azpeeringserviceprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeeringServicePrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeeringServicePrefix.md
ms.openlocfilehash: 0fbf44e9a68a5cfaaea4138ec17caa2960a41e67
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98424855"
---
# <span data-ttu-id="baf27-101">Remove-AzPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="baf27-101">Remove-AzPeeringServicePrefix</span></span>

## <span data-ttu-id="baf27-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="baf27-102">SYNOPSIS</span></span>
<span data-ttu-id="baf27-103">Удаление нового префикса службы пиринга</span><span class="sxs-lookup"><span data-stu-id="baf27-103">Removes a new peering service prefix</span></span>

## <span data-ttu-id="baf27-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="baf27-104">SYNTAX</span></span>

### <span data-ttu-id="baf27-105">ByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="baf27-105">ByName (Default)</span></span>
```
Remove-AzPeeringServicePrefix [-ResourceGroupName] <String> [-Name] <String> [-PrefixName] <String> [-Force]
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="baf27-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="baf27-106">InputObject</span></span>
```
Remove-AzPeeringServicePrefix [-InputObject] <PSPeeringServicePrefix> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="baf27-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="baf27-107">ByResourceId</span></span>
```
Remove-AzPeeringServicePrefix [-ResourceId] <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="baf27-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="baf27-108">DESCRIPTION</span></span>
<span data-ttu-id="baf27-109">Удаляет префикс службы пиринга из службы пиринга.</span><span class="sxs-lookup"><span data-stu-id="baf27-109">Removes a peering service prefix from a peering service.</span></span>

## <span data-ttu-id="baf27-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="baf27-110">EXAMPLES</span></span>

### <span data-ttu-id="baf27-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="baf27-111">Example 1</span></span>
```powershell
PS C:\> Get-AzPeeringService -ResourceGroupName $rgName -Name $peeringServiceName | Remove-AzPeeringServicePrefix -Name $prefixName
```

<span data-ttu-id="baf27-112">Удаление префикса из объекта службы пиринга</span><span class="sxs-lookup"><span data-stu-id="baf27-112">Remove a prefix from a peering service object</span></span>

### <span data-ttu-id="baf27-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="baf27-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzPeeringServicePrefix -ResourceId $peeringServiceResourceId -Name $prefixName -PassThru

True
```

<span data-ttu-id="baf27-114">Удалите префикс из ид ресурса службы пиринга.</span><span class="sxs-lookup"><span data-stu-id="baf27-114">Remove a prefix from a peering service resource id.</span></span>

### <span data-ttu-id="baf27-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="baf27-115">Example 3</span></span>
```powershell
PS C:\> Remove-AzPeeringServicePrefix -ResourceGroupName $peeringServiceGroup -PeeringServiceName $peeringServiceName -Name $prefixName -PassThru

True
```

<span data-ttu-id="baf27-116">Удаление префикса из имени и имени группы ресурсов службы пиринга</span><span class="sxs-lookup"><span data-stu-id="baf27-116">Remove a prefix from a peering service resource group name and name</span></span>

## <span data-ttu-id="baf27-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="baf27-117">PARAMETERS</span></span>

### <span data-ttu-id="baf27-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="baf27-118">-AsJob</span></span>
<span data-ttu-id="baf27-119">Запускать в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="baf27-119">Run in the background.</span></span>

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

### <span data-ttu-id="baf27-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="baf27-120">-DefaultProfile</span></span>
<span data-ttu-id="baf27-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="baf27-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="baf27-122">-Force</span><span class="sxs-lookup"><span data-stu-id="baf27-122">-Force</span></span>
<span data-ttu-id="baf27-123">Принудительное завершение операции</span><span class="sxs-lookup"><span data-stu-id="baf27-123">Force the operation to complete</span></span>

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

### <span data-ttu-id="baf27-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="baf27-124">-InputObject</span></span>
<span data-ttu-id="baf27-125">Использование Get-AzPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="baf27-125">Use a Get-AzPeeringServicePrefix</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="baf27-126">-Name</span><span class="sxs-lookup"><span data-stu-id="baf27-126">-Name</span></span>
<span data-ttu-id="baf27-127">Уникальное имя PSPeering.</span><span class="sxs-lookup"><span data-stu-id="baf27-127">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="baf27-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="baf27-128">-PassThru</span></span>
<span data-ttu-id="baf27-129">Возвращает "Истина" для неудачи или ложь.</span><span class="sxs-lookup"><span data-stu-id="baf27-129">Returns true for success or false for failed.</span></span>

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

### <span data-ttu-id="baf27-130">-PrefixName</span><span class="sxs-lookup"><span data-stu-id="baf27-130">-PrefixName</span></span>
<span data-ttu-id="baf27-131">Имя префикса.</span><span class="sxs-lookup"><span data-stu-id="baf27-131">The name of prefix.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="baf27-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="baf27-132">-ResourceGroupName</span></span>
<span data-ttu-id="baf27-133">Создание или использование существующего имени группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="baf27-133">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="baf27-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="baf27-134">-ResourceId</span></span>
<span data-ttu-id="baf27-135">Имя строки "ИД ресурса".</span><span class="sxs-lookup"><span data-stu-id="baf27-135">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="baf27-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="baf27-136">-Confirm</span></span>
<span data-ttu-id="baf27-137">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="baf27-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="baf27-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="baf27-138">-WhatIf</span></span>
<span data-ttu-id="baf27-139">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="baf27-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="baf27-140">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="baf27-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="baf27-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="baf27-141">CommonParameters</span></span>
<span data-ttu-id="baf27-142">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="baf27-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="baf27-143">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="baf27-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="baf27-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="baf27-144">INPUTS</span></span>

### <span data-ttu-id="baf27-145">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="baf27-145">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span></span>

### <span data-ttu-id="baf27-146">System.String</span><span class="sxs-lookup"><span data-stu-id="baf27-146">System.String</span></span>

## <span data-ttu-id="baf27-147">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="baf27-147">OUTPUTS</span></span>

### <span data-ttu-id="baf27-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="baf27-148">System.Boolean</span></span>

## <span data-ttu-id="baf27-149">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="baf27-149">NOTES</span></span>

## <span data-ttu-id="baf27-150">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="baf27-150">RELATED LINKS</span></span>
