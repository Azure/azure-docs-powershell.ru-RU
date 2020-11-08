---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/remove-azpeeringserviceprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeeringServicePrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeeringServicePrefix.md
ms.openlocfilehash: 0fbf44e9a68a5cfaaea4138ec17caa2960a41e67
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247216"
---
# <span data-ttu-id="b5f14-101">Remove-AzPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="b5f14-101">Remove-AzPeeringServicePrefix</span></span>

## <span data-ttu-id="b5f14-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b5f14-102">SYNOPSIS</span></span>
<span data-ttu-id="b5f14-103">Удаление нового префикса службы пиринга</span><span class="sxs-lookup"><span data-stu-id="b5f14-103">Removes a new peering service prefix</span></span>

## <span data-ttu-id="b5f14-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b5f14-104">SYNTAX</span></span>

### <span data-ttu-id="b5f14-105">ByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b5f14-105">ByName (Default)</span></span>
```
Remove-AzPeeringServicePrefix [-ResourceGroupName] <String> [-Name] <String> [-PrefixName] <String> [-Force]
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5f14-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="b5f14-106">InputObject</span></span>
```
Remove-AzPeeringServicePrefix [-InputObject] <PSPeeringServicePrefix> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5f14-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b5f14-107">ByResourceId</span></span>
```
Remove-AzPeeringServicePrefix [-ResourceId] <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b5f14-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b5f14-108">DESCRIPTION</span></span>
<span data-ttu-id="b5f14-109">Удаляет префикс службы пиринга из службы пиринга.</span><span class="sxs-lookup"><span data-stu-id="b5f14-109">Removes a peering service prefix from a peering service.</span></span>

## <span data-ttu-id="b5f14-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b5f14-110">EXAMPLES</span></span>

### <span data-ttu-id="b5f14-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b5f14-111">Example 1</span></span>
```powershell
PS C:\> Get-AzPeeringService -ResourceGroupName $rgName -Name $peeringServiceName | Remove-AzPeeringServicePrefix -Name $prefixName
```

<span data-ttu-id="b5f14-112">Удаление префикса из объекта службы пиринга</span><span class="sxs-lookup"><span data-stu-id="b5f14-112">Remove a prefix from a peering service object</span></span>

### <span data-ttu-id="b5f14-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="b5f14-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzPeeringServicePrefix -ResourceId $peeringServiceResourceId -Name $prefixName -PassThru

True
```

<span data-ttu-id="b5f14-114">Удаление префикса из идентификатора ресурса службы пиринга.</span><span class="sxs-lookup"><span data-stu-id="b5f14-114">Remove a prefix from a peering service resource id.</span></span>

### <span data-ttu-id="b5f14-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="b5f14-115">Example 3</span></span>
```powershell
PS C:\> Remove-AzPeeringServicePrefix -ResourceGroupName $peeringServiceGroup -PeeringServiceName $peeringServiceName -Name $prefixName -PassThru

True
```

<span data-ttu-id="b5f14-116">Удаление префикса из имени и имени группы ресурсов службы пиринга</span><span class="sxs-lookup"><span data-stu-id="b5f14-116">Remove a prefix from a peering service resource group name and name</span></span>

## <span data-ttu-id="b5f14-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b5f14-117">PARAMETERS</span></span>

### <span data-ttu-id="b5f14-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b5f14-118">-AsJob</span></span>
<span data-ttu-id="b5f14-119">Выполнение в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="b5f14-119">Run in the background.</span></span>

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

### <span data-ttu-id="b5f14-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5f14-120">-DefaultProfile</span></span>
<span data-ttu-id="b5f14-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b5f14-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b5f14-122">-Force</span><span class="sxs-lookup"><span data-stu-id="b5f14-122">-Force</span></span>
<span data-ttu-id="b5f14-123">Принудительно завершить операцию</span><span class="sxs-lookup"><span data-stu-id="b5f14-123">Force the operation to complete</span></span>

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

### <span data-ttu-id="b5f14-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b5f14-124">-InputObject</span></span>
<span data-ttu-id="b5f14-125">Использование Get-AzPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="b5f14-125">Use a Get-AzPeeringServicePrefix</span></span>

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

### <span data-ttu-id="b5f14-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b5f14-126">-Name</span></span>
<span data-ttu-id="b5f14-127">Уникальное имя PSPeering.</span><span class="sxs-lookup"><span data-stu-id="b5f14-127">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="b5f14-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b5f14-128">-PassThru</span></span>
<span data-ttu-id="b5f14-129">Возвращает значение истина для аргумента успешно или ложь для ошибки.</span><span class="sxs-lookup"><span data-stu-id="b5f14-129">Returns true for success or false for failed.</span></span>

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

### <span data-ttu-id="b5f14-130">-PrefixName</span><span class="sxs-lookup"><span data-stu-id="b5f14-130">-PrefixName</span></span>
<span data-ttu-id="b5f14-131">Имя префикса.</span><span class="sxs-lookup"><span data-stu-id="b5f14-131">The name of prefix.</span></span>

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

### <span data-ttu-id="b5f14-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5f14-132">-ResourceGroupName</span></span>
<span data-ttu-id="b5f14-133">Создание или использование существующего имени группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b5f14-133">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="b5f14-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b5f14-134">-ResourceId</span></span>
<span data-ttu-id="b5f14-135">Имя строки идентификатора ресурса.</span><span class="sxs-lookup"><span data-stu-id="b5f14-135">The resource id string name.</span></span>

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

### <span data-ttu-id="b5f14-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b5f14-136">-Confirm</span></span>
<span data-ttu-id="b5f14-137">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b5f14-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5f14-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5f14-138">-WhatIf</span></span>
<span data-ttu-id="b5f14-139">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b5f14-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5f14-140">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b5f14-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5f14-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5f14-141">CommonParameters</span></span>
<span data-ttu-id="b5f14-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b5f14-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5f14-143">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b5f14-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5f14-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b5f14-144">INPUTS</span></span>

### <span data-ttu-id="b5f14-145">Microsoft. Azure. PowerShell. командлеты. Peer (Models. PSPeeringServicePrefix)</span><span class="sxs-lookup"><span data-stu-id="b5f14-145">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span></span>

### <span data-ttu-id="b5f14-146">System. String</span><span class="sxs-lookup"><span data-stu-id="b5f14-146">System.String</span></span>

## <span data-ttu-id="b5f14-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b5f14-147">OUTPUTS</span></span>

### <span data-ttu-id="b5f14-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b5f14-148">System.Boolean</span></span>

## <span data-ttu-id="b5f14-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="b5f14-149">NOTES</span></span>

## <span data-ttu-id="b5f14-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b5f14-150">RELATED LINKS</span></span>
