---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/remove-azpeeringserviceprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeeringServicePrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeeringServicePrefix.md
ms.openlocfilehash: 36003d1fbca7566ae663a1d878386f3d8d67f484
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93904581"
---
# <span data-ttu-id="ee48a-101">Remove-AzPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="ee48a-101">Remove-AzPeeringServicePrefix</span></span>

## <span data-ttu-id="ee48a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ee48a-102">SYNOPSIS</span></span>
<span data-ttu-id="ee48a-103">Удаление нового префикса службы пиринга</span><span class="sxs-lookup"><span data-stu-id="ee48a-103">Removes a new peering service prefix</span></span>

## <span data-ttu-id="ee48a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ee48a-104">SYNTAX</span></span>

### <span data-ttu-id="ee48a-105">ByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ee48a-105">ByName (Default)</span></span>
```
Remove-AzPeeringServicePrefix [-ResourceGroupName] <String> [-Name] <String> [-PeeringServiceName] <String>
 [-Force] [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ee48a-106">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="ee48a-106">Default</span></span>
```
Remove-AzPeeringServicePrefix -InputObject <PSPeeringServicePrefix> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee48a-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ee48a-107">ByResourceId</span></span>
```
Remove-AzPeeringServicePrefix [-ResourceId] <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee48a-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ee48a-108">DESCRIPTION</span></span>
<span data-ttu-id="ee48a-109">Удаляет префикс службы пиринга из службы пиринга.</span><span class="sxs-lookup"><span data-stu-id="ee48a-109">Removes a peering service prefix from a peering service.</span></span>

## <span data-ttu-id="ee48a-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ee48a-110">EXAMPLES</span></span>

### <span data-ttu-id="ee48a-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ee48a-111">Example 1</span></span>
```powershell
PS C:\> Get-AzPeeringService -ResourceGroupName $rgName -Name $peeringServiceName | Remove-AzPeeringServicePrefix -Name $prefixName
```

<span data-ttu-id="ee48a-112">Удаление префикса из объекта службы пиринга</span><span class="sxs-lookup"><span data-stu-id="ee48a-112">Remove a prefix from a peering service object</span></span>

### <span data-ttu-id="ee48a-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="ee48a-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzPeeringServicePrefix -ResourceId $peeringServiceResourceId -Name $prefixName -PassThru

True
```

<span data-ttu-id="ee48a-114">Удаление префикса из идентификатора ресурса службы пиринга.</span><span class="sxs-lookup"><span data-stu-id="ee48a-114">Remove a prefix from a peering service resource id.</span></span>

### <span data-ttu-id="ee48a-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="ee48a-115">Example 3</span></span>
```powershell
PS C:\> Remove-AzPeeringServicePrefix -ResourceGroupName $peeringServiceGroup -PeeringServiceName $peeringServiceName -Name $prefixName -PassThru

True
```

<span data-ttu-id="ee48a-116">Удаление префикса из имени и имени группы ресурсов службы пиринга</span><span class="sxs-lookup"><span data-stu-id="ee48a-116">Remove a prefix from a peering service resource group name and name</span></span>

## <span data-ttu-id="ee48a-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ee48a-117">PARAMETERS</span></span>

### <span data-ttu-id="ee48a-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ee48a-118">-AsJob</span></span>
<span data-ttu-id="ee48a-119">Выполнение в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="ee48a-119">Run in the background.</span></span>

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

### <span data-ttu-id="ee48a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee48a-120">-DefaultProfile</span></span>
<span data-ttu-id="ee48a-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ee48a-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee48a-122">-Force</span><span class="sxs-lookup"><span data-stu-id="ee48a-122">-Force</span></span>
<span data-ttu-id="ee48a-123">Принудительно завершить операцию</span><span class="sxs-lookup"><span data-stu-id="ee48a-123">Force the operation to complete</span></span>

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

### <span data-ttu-id="ee48a-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ee48a-124">-InputObject</span></span>
<span data-ttu-id="ee48a-125">Использование Get-AzPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="ee48a-125">Use a Get-AzPeeringServicePrefix</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix
Parameter Sets: Default
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ee48a-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ee48a-126">-Name</span></span>
<span data-ttu-id="ee48a-127">Уникальное имя PSPeering.</span><span class="sxs-lookup"><span data-stu-id="ee48a-127">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="ee48a-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ee48a-128">-PassThru</span></span>
<span data-ttu-id="ee48a-129">Возвращает значение истина для аргумента успешно или ложь для ошибки.</span><span class="sxs-lookup"><span data-stu-id="ee48a-129">Returns true for success or false for failed.</span></span>

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

### <span data-ttu-id="ee48a-130">-PeeringServiceName</span><span class="sxs-lookup"><span data-stu-id="ee48a-130">-PeeringServiceName</span></span>
<span data-ttu-id="ee48a-131">Уникальное имя PSPeering.</span><span class="sxs-lookup"><span data-stu-id="ee48a-131">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="ee48a-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee48a-132">-ResourceGroupName</span></span>
<span data-ttu-id="ee48a-133">Создание или использование существующего имени группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ee48a-133">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="ee48a-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ee48a-134">-ResourceId</span></span>
<span data-ttu-id="ee48a-135">Имя строки идентификатора ресурса.</span><span class="sxs-lookup"><span data-stu-id="ee48a-135">The resource id string name.</span></span>

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

### <span data-ttu-id="ee48a-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ee48a-136">-Confirm</span></span>
<span data-ttu-id="ee48a-137">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ee48a-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee48a-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee48a-138">-WhatIf</span></span>
<span data-ttu-id="ee48a-139">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ee48a-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee48a-140">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ee48a-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee48a-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee48a-141">CommonParameters</span></span>
<span data-ttu-id="ee48a-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ee48a-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee48a-143">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ee48a-143">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee48a-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ee48a-144">INPUTS</span></span>

### <span data-ttu-id="ee48a-145">Microsoft. Azure. PowerShell. командлеты. Peer (Models. PSPeeringServicePrefix)</span><span class="sxs-lookup"><span data-stu-id="ee48a-145">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span></span>

### <span data-ttu-id="ee48a-146">System. String</span><span class="sxs-lookup"><span data-stu-id="ee48a-146">System.String</span></span>

## <span data-ttu-id="ee48a-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ee48a-147">OUTPUTS</span></span>

### <span data-ttu-id="ee48a-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ee48a-148">System.Boolean</span></span>

## <span data-ttu-id="ee48a-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="ee48a-149">NOTES</span></span>

## <span data-ttu-id="ee48a-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ee48a-150">RELATED LINKS</span></span>
