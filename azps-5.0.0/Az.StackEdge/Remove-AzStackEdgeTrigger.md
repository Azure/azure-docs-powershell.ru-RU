---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeTrigger.md
ms.openlocfilehash: ad2761e4e0fba3ef7dbb7a28b15477a649891042
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246359"
---
# <span data-ttu-id="b63e9-101">Remove-AzStackEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="b63e9-101">Remove-AzStackEdgeTrigger</span></span>

## <span data-ttu-id="b63e9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b63e9-102">SYNOPSIS</span></span>
<span data-ttu-id="b63e9-103">Удаляет существующий триггер на устройстве.</span><span class="sxs-lookup"><span data-stu-id="b63e9-103">Removes an existing trigger on the device.</span></span>

## <span data-ttu-id="b63e9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b63e9-104">SYNTAX</span></span>

### <span data-ttu-id="b63e9-105">DeleteByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b63e9-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b63e9-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b63e9-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeTrigger [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b63e9-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b63e9-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeTrigger [-InputObject] <PSStackEdgeTrigger> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b63e9-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b63e9-108">DESCRIPTION</span></span>
<span data-ttu-id="b63e9-109">Командлет **Remove-AzStackEdgeTrigger** удаляет существующий триггер на пограничном устройстве стека.</span><span class="sxs-lookup"><span data-stu-id="b63e9-109">The **Remove-AzStackEdgeTrigger** cmdlet removes an existing trigger on the Stack Edge device.</span></span>

## <span data-ttu-id="b63e9-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b63e9-110">EXAMPLES</span></span>

### <span data-ttu-id="b63e9-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b63e9-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeTrigger -ResourceGroupName resourceGroupName -DeviceName deviceName -Name triggerName
```

## <span data-ttu-id="b63e9-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b63e9-112">PARAMETERS</span></span>

### <span data-ttu-id="b63e9-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b63e9-113">-AsJob</span></span>
<span data-ttu-id="b63e9-114">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="b63e9-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b63e9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b63e9-115">-DefaultProfile</span></span>
<span data-ttu-id="b63e9-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b63e9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b63e9-117">-Имя_устройства</span><span class="sxs-lookup"><span data-stu-id="b63e9-117">-DeviceName</span></span>
<span data-ttu-id="b63e9-118">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="b63e9-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b63e9-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b63e9-119">-InputObject</span></span>
<span data-ttu-id="b63e9-120">Объект input</span><span class="sxs-lookup"><span data-stu-id="b63e9-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeTrigger
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: Trigger

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b63e9-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b63e9-121">-Name</span></span>
<span data-ttu-id="b63e9-122">Название ресурса</span><span class="sxs-lookup"><span data-stu-id="b63e9-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b63e9-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b63e9-123">-PassThru</span></span>
<span data-ttu-id="b63e9-124">Возвращает значение истина, если выполнено успешно</span><span class="sxs-lookup"><span data-stu-id="b63e9-124">returns true if successful</span></span>

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

### <span data-ttu-id="b63e9-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b63e9-125">-ResourceGroupName</span></span>
<span data-ttu-id="b63e9-126">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="b63e9-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b63e9-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b63e9-127">-ResourceId</span></span>
<span data-ttu-id="b63e9-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="b63e9-128">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b63e9-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b63e9-129">-Confirm</span></span>
<span data-ttu-id="b63e9-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b63e9-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b63e9-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b63e9-131">-WhatIf</span></span>
<span data-ttu-id="b63e9-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b63e9-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b63e9-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b63e9-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b63e9-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b63e9-134">CommonParameters</span></span>
<span data-ttu-id="b63e9-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b63e9-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b63e9-136">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b63e9-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b63e9-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b63e9-137">INPUTS</span></span>

### <span data-ttu-id="b63e9-138">System. String</span><span class="sxs-lookup"><span data-stu-id="b63e9-138">System.String</span></span>

### <span data-ttu-id="b63e9-139">Microsoft. Azure. PowerShell. командлеты. StackEdge. Models. PSStackEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="b63e9-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeTrigger</span></span>

## <span data-ttu-id="b63e9-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b63e9-140">OUTPUTS</span></span>

### <span data-ttu-id="b63e9-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b63e9-141">System.Boolean</span></span>

## <span data-ttu-id="b63e9-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="b63e9-142">NOTES</span></span>

## <span data-ttu-id="b63e9-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b63e9-143">RELATED LINKS</span></span>