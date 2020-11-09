---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/invoke-azdataboxedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Invoke-AzDataBoxEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Invoke-AzDataBoxEdgeShare.md
ms.openlocfilehash: c3fa71b6fb54f359f035f4f6c2f18789ff24b3ac
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244184"
---
# <span data-ttu-id="3f9a3-101">Invoke-AzDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="3f9a3-101">Invoke-AzDataBoxEdgeShare</span></span>

## <span data-ttu-id="3f9a3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3f9a3-102">SYNOPSIS</span></span>
<span data-ttu-id="3f9a3-103">Вызывает определенные действия в общем доступе.</span><span class="sxs-lookup"><span data-stu-id="3f9a3-103">Invokes specific actions on a share.</span></span>

## <span data-ttu-id="3f9a3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3f9a3-104">SYNTAX</span></span>

### <span data-ttu-id="3f9a3-105">InvokeByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3f9a3-105">InvokeByNameParameterSet (Default)</span></span>
```
Invoke-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-RefreshData] [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3f9a3-106">InvokeByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3f9a3-106">InvokeByResourceIdParameterSet</span></span>
```
Invoke-AzDataBoxEdgeShare -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-RefreshData] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f9a3-107">InvokeByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3f9a3-107">InvokeByInputObjectParameterSet</span></span>
```
Invoke-AzDataBoxEdgeShare [-AsJob] [-DefaultProfile <IAzureContextContainer>] -InputObject <PSDataBoxEdgeShare>
 [-RefreshData] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3f9a3-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3f9a3-108">DESCRIPTION</span></span>
<span data-ttu-id="3f9a3-109">Командлет **Invoke-AzDataBoxEdgeShare** вызывает действие для обновления данных в общем доступе на пограничном устройстве поля данных.</span><span class="sxs-lookup"><span data-stu-id="3f9a3-109">The **Invoke-AzDataBoxEdgeShare** cmdlet invokes action to refresh data on a share on a Data Box Edge device.</span></span>

## <span data-ttu-id="3f9a3-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3f9a3-110">EXAMPLES</span></span>

### <span data-ttu-id="3f9a3-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3f9a3-111">Example 1</span></span>
```powershell
PS C:\> Invoke-AzDataBoxEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName -Name share1 -PassThru
PS C:\> true
```

### <span data-ttu-id="3f9a3-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="3f9a3-112">Example 2</span></span>
```powershell
PS C:\> Invoke-AzDataBoxEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName -Name share1 | Invoke-AzDataBoxEdgeShare
```

## <span data-ttu-id="3f9a3-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3f9a3-113">PARAMETERS</span></span>

### <span data-ttu-id="3f9a3-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3f9a3-114">-AsJob</span></span>
<span data-ttu-id="3f9a3-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="3f9a3-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3f9a3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f9a3-116">-DefaultProfile</span></span>
<span data-ttu-id="3f9a3-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3f9a3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f9a3-118">-Имя_устройства</span><span class="sxs-lookup"><span data-stu-id="3f9a3-118">-DeviceName</span></span>
<span data-ttu-id="3f9a3-119">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="3f9a3-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f9a3-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3f9a3-120">-InputObject</span></span>
<span data-ttu-id="3f9a3-121">Объект input</span><span class="sxs-lookup"><span data-stu-id="3f9a3-121">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare
Parameter Sets: InvokeByInputObjectParameterSet
Aliases: EdgeShare

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3f9a3-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3f9a3-122">-Name</span></span>
<span data-ttu-id="3f9a3-123">Название ресурса</span><span class="sxs-lookup"><span data-stu-id="3f9a3-123">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases: EdgeShareName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f9a3-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3f9a3-124">-PassThru</span></span>
<span data-ttu-id="3f9a3-125">Возвращает значение истина, если выполнено успешно</span><span class="sxs-lookup"><span data-stu-id="3f9a3-125">returns true if successful</span></span>

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

### <span data-ttu-id="3f9a3-126">-RefreshData</span><span class="sxs-lookup"><span data-stu-id="3f9a3-126">-RefreshData</span></span>
<span data-ttu-id="3f9a3-127">Обновление метаданных общего доступа с данными из облака</span><span class="sxs-lookup"><span data-stu-id="3f9a3-127">Refresh Share Metadata with the data from the cloud</span></span>

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

### <span data-ttu-id="3f9a3-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f9a3-128">-ResourceGroupName</span></span>
<span data-ttu-id="3f9a3-129">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="3f9a3-129">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f9a3-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3f9a3-130">-ResourceId</span></span>
<span data-ttu-id="3f9a3-131">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="3f9a3-131">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f9a3-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3f9a3-132">-Confirm</span></span>
<span data-ttu-id="3f9a3-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3f9a3-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f9a3-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f9a3-134">-WhatIf</span></span>
<span data-ttu-id="3f9a3-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3f9a3-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3f9a3-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3f9a3-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f9a3-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f9a3-137">CommonParameters</span></span>
<span data-ttu-id="3f9a3-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3f9a3-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f9a3-139">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3f9a3-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f9a3-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3f9a3-140">INPUTS</span></span>

### <span data-ttu-id="3f9a3-141">System. String</span><span class="sxs-lookup"><span data-stu-id="3f9a3-141">System.String</span></span>

### <span data-ttu-id="3f9a3-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="3f9a3-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span></span>

## <span data-ttu-id="3f9a3-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3f9a3-143">OUTPUTS</span></span>

### <span data-ttu-id="3f9a3-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3f9a3-144">System.Boolean</span></span>

## <span data-ttu-id="3f9a3-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="3f9a3-145">NOTES</span></span>

## <span data-ttu-id="3f9a3-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3f9a3-146">RELATED LINKS</span></span>