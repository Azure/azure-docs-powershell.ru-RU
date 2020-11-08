---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeShare.md
ms.openlocfilehash: 3f5855d329daba44b26e2c79cbc07608222db5f9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246176"
---
# <span data-ttu-id="965f3-101">Remove-AzStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="965f3-101">Remove-AzStackEdgeShare</span></span>

## <span data-ttu-id="965f3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="965f3-102">SYNOPSIS</span></span>
<span data-ttu-id="965f3-103">Удаление общего доступа с устройства.</span><span class="sxs-lookup"><span data-stu-id="965f3-103">Removes a share from the device.</span></span>

## <span data-ttu-id="965f3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="965f3-104">SYNTAX</span></span>

### <span data-ttu-id="965f3-105">DeleteByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="965f3-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="965f3-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="965f3-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeShare [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="965f3-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="965f3-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeShare [-InputObject] <PSStackEdgeShare> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="965f3-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="965f3-108">DESCRIPTION</span></span>
<span data-ttu-id="965f3-109">Командлет **Remove-AzStackEdgeEdgeShare** удаляет связанные общие ресурсы Edge для краевого устройства стека.</span><span class="sxs-lookup"><span data-stu-id="965f3-109">The **Remove-AzStackEdgeEdgeShare** cmdlet removes the associated edge shares for a Stack Edge device.</span></span>

## <span data-ttu-id="965f3-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="965f3-110">EXAMPLES</span></span>

### <span data-ttu-id="965f3-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="965f3-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName -Name shareName
```

## <span data-ttu-id="965f3-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="965f3-112">PARAMETERS</span></span>

### <span data-ttu-id="965f3-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="965f3-113">-AsJob</span></span>
<span data-ttu-id="965f3-114">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="965f3-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="965f3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="965f3-115">-DefaultProfile</span></span>
<span data-ttu-id="965f3-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="965f3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="965f3-117">-Имя_устройства</span><span class="sxs-lookup"><span data-stu-id="965f3-117">-DeviceName</span></span>
<span data-ttu-id="965f3-118">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="965f3-118">Device Name</span></span>

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

### <span data-ttu-id="965f3-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="965f3-119">-InputObject</span></span>
<span data-ttu-id="965f3-120">Объект input</span><span class="sxs-lookup"><span data-stu-id="965f3-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: EdgeShare

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="965f3-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="965f3-121">-Name</span></span>
<span data-ttu-id="965f3-122">Название ресурса</span><span class="sxs-lookup"><span data-stu-id="965f3-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: EdgeShareName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="965f3-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="965f3-123">-PassThru</span></span>
<span data-ttu-id="965f3-124">Возвращает значение истина, если выполнено успешно</span><span class="sxs-lookup"><span data-stu-id="965f3-124">returns true if successful</span></span>

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

### <span data-ttu-id="965f3-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="965f3-125">-ResourceGroupName</span></span>
<span data-ttu-id="965f3-126">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="965f3-126">Resource Group Name</span></span>

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

### <span data-ttu-id="965f3-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="965f3-127">-ResourceId</span></span>
<span data-ttu-id="965f3-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="965f3-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="965f3-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="965f3-129">-Confirm</span></span>
<span data-ttu-id="965f3-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="965f3-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="965f3-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="965f3-131">-WhatIf</span></span>
<span data-ttu-id="965f3-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="965f3-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="965f3-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="965f3-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="965f3-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="965f3-134">CommonParameters</span></span>
<span data-ttu-id="965f3-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="965f3-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="965f3-136">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="965f3-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="965f3-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="965f3-137">INPUTS</span></span>

### <span data-ttu-id="965f3-138">System. String</span><span class="sxs-lookup"><span data-stu-id="965f3-138">System.String</span></span>

### <span data-ttu-id="965f3-139">Microsoft. Azure. PowerShell. командлеты. StackEdge. Models. PSStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="965f3-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare</span></span>

## <span data-ttu-id="965f3-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="965f3-140">OUTPUTS</span></span>

### <span data-ttu-id="965f3-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="965f3-141">System.Boolean</span></span>

## <span data-ttu-id="965f3-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="965f3-142">NOTES</span></span>

## <span data-ttu-id="965f3-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="965f3-143">RELATED LINKS</span></span>
