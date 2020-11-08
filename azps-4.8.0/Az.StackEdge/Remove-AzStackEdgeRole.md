---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeRole.md
ms.openlocfilehash: 7e462c7f6d22a071217a7279a44114c3a95504bd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243818"
---
# <span data-ttu-id="fae79-101">Remove-AzStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="fae79-101">Remove-AzStackEdgeRole</span></span>

## <span data-ttu-id="fae79-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fae79-102">SYNOPSIS</span></span>
<span data-ttu-id="fae79-103">Удаляет соответствующую роль IoT для устройства.</span><span class="sxs-lookup"><span data-stu-id="fae79-103">Removes the associated IoT role for a device.</span></span>

## <span data-ttu-id="fae79-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fae79-104">SYNTAX</span></span>

### <span data-ttu-id="fae79-105">DeleteByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fae79-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fae79-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fae79-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeRole -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fae79-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fae79-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeRole -InputObject <PSStackEdgeRole> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fae79-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fae79-108">DESCRIPTION</span></span>
<span data-ttu-id="fae79-109">Командлет **Remove-AzStackEdgeRole** удаляет соответствующую роль IOT для краевого устройства стека.</span><span class="sxs-lookup"><span data-stu-id="fae79-109">The **Remove-AzStackEdgeRole** cmdlet removes the associated IoT role for a Stack Edge device.</span></span>

## <span data-ttu-id="fae79-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fae79-110">EXAMPLES</span></span>

### <span data-ttu-id="fae79-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="fae79-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name roleName
```

## <span data-ttu-id="fae79-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fae79-112">PARAMETERS</span></span>

### <span data-ttu-id="fae79-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fae79-113">-AsJob</span></span>
<span data-ttu-id="fae79-114">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="fae79-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fae79-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fae79-115">-DefaultProfile</span></span>
<span data-ttu-id="fae79-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fae79-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fae79-117">-Имя_устройства</span><span class="sxs-lookup"><span data-stu-id="fae79-117">-DeviceName</span></span>
<span data-ttu-id="fae79-118">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="fae79-118">Device Name</span></span>

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

### <span data-ttu-id="fae79-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fae79-119">-InputObject</span></span>
<span data-ttu-id="fae79-120">Объект input</span><span class="sxs-lookup"><span data-stu-id="fae79-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: Role

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fae79-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="fae79-121">-Name</span></span>
<span data-ttu-id="fae79-122">Название ресурса</span><span class="sxs-lookup"><span data-stu-id="fae79-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: RoleName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fae79-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fae79-123">-PassThru</span></span>
<span data-ttu-id="fae79-124">Возвращает значение истина, если выполнено успешно</span><span class="sxs-lookup"><span data-stu-id="fae79-124">returns true if successful</span></span>

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

### <span data-ttu-id="fae79-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fae79-125">-ResourceGroupName</span></span>
<span data-ttu-id="fae79-126">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="fae79-126">Resource Group Name</span></span>

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

### <span data-ttu-id="fae79-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fae79-127">-ResourceId</span></span>
<span data-ttu-id="fae79-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="fae79-128">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fae79-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fae79-129">-Confirm</span></span>
<span data-ttu-id="fae79-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="fae79-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fae79-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fae79-131">-WhatIf</span></span>
<span data-ttu-id="fae79-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="fae79-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fae79-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="fae79-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fae79-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fae79-134">CommonParameters</span></span>
<span data-ttu-id="fae79-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fae79-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fae79-136">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fae79-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fae79-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fae79-137">INPUTS</span></span>

### <span data-ttu-id="fae79-138">System. String</span><span class="sxs-lookup"><span data-stu-id="fae79-138">System.String</span></span>

### <span data-ttu-id="fae79-139">Microsoft. Azure. PowerShell. командлеты. StackEdge. Models. PSStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="fae79-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span></span>

## <span data-ttu-id="fae79-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fae79-140">OUTPUTS</span></span>

### <span data-ttu-id="fae79-141">Microsoft. Azure. PowerShell. командлеты. StackEdge. Models. PSStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="fae79-141">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span></span>

## <span data-ttu-id="fae79-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="fae79-142">NOTES</span></span>

## <span data-ttu-id="fae79-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fae79-143">RELATED LINKS</span></span>
