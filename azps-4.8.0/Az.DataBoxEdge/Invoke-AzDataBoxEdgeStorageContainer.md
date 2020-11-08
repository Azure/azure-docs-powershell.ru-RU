---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/invoke-azdataboxedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Invoke-AzDataBoxEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Invoke-AzDataBoxEdgeStorageContainer.md
ms.openlocfilehash: f897c2adfe4154aeff5bd370437ea8b23e4efd36
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244188"
---
# <span data-ttu-id="2cd1d-101">Invoke-AzDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="2cd1d-101">Invoke-AzDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="2cd1d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2cd1d-102">SYNOPSIS</span></span>
<span data-ttu-id="2cd1d-103">Вызывает определенные действия в контейнере хранилища.</span><span class="sxs-lookup"><span data-stu-id="2cd1d-103">Invokes specific actions on a storage container</span></span>

## <span data-ttu-id="2cd1d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2cd1d-104">SYNTAX</span></span>

### <span data-ttu-id="2cd1d-105">InvokeByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2cd1d-105">InvokeByNameParameterSet (Default)</span></span>
```
Invoke-AzDataBoxEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-RefreshData] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2cd1d-106">InvokeByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2cd1d-106">InvokeByResourceIdParameterSet</span></span>
```
Invoke-AzDataBoxEdgeStorageContainer [-ResourceId] <String> [-RefreshData] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2cd1d-107">InvokeByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2cd1d-107">InvokeByInputObjectParameterSet</span></span>
```
Invoke-AzDataBoxEdgeStorageContainer [-RefreshData] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 -InputObject <PSDataBoxEdgeStorageContainer> [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2cd1d-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2cd1d-108">DESCRIPTION</span></span>
<span data-ttu-id="2cd1d-109">Командлет **Invoke-AzDataBoxEdgeStorageContainer** вызывает действия для обновления данных в контейнере хранилища на пограничном устройстве поля данных.</span><span class="sxs-lookup"><span data-stu-id="2cd1d-109">The **Invoke-AzDataBoxEdgeStorageContainer** cmdlet invokes actions to refresh the data on a storage container on a Data Box Edge device.</span></span> 

## <span data-ttu-id="2cd1d-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2cd1d-110">EXAMPLES</span></span>

### <span data-ttu-id="2cd1d-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2cd1d-111">Example 1</span></span>
```powershell
PS C:\> Invoke-AzDataBoxEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName deviceName -EdgeStorageAccountName edgestorageaccount1 -Name container1 -PassThru
PS C:\> true
```

### <span data-ttu-id="2cd1d-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="2cd1d-112">Example 2</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName deviceName -EdgeStorageAccountName edgestorageaccount1 -Name container1 | Invoke-AzDataBoxEdgeStorageContainer
```

## <span data-ttu-id="2cd1d-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2cd1d-113">PARAMETERS</span></span>

### <span data-ttu-id="2cd1d-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2cd1d-114">-AsJob</span></span>
<span data-ttu-id="2cd1d-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="2cd1d-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2cd1d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cd1d-116">-DefaultProfile</span></span>
<span data-ttu-id="2cd1d-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2cd1d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2cd1d-118">-Имя_устройства</span><span class="sxs-lookup"><span data-stu-id="2cd1d-118">-DeviceName</span></span>
<span data-ttu-id="2cd1d-119">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="2cd1d-119">Device Name</span></span>

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

### <span data-ttu-id="2cd1d-120">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="2cd1d-120">-EdgeStorageAccountName</span></span>
<span data-ttu-id="2cd1d-121">Название ресурса</span><span class="sxs-lookup"><span data-stu-id="2cd1d-121">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2cd1d-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2cd1d-122">-InputObject</span></span>
<span data-ttu-id="2cd1d-123">Предоставить существующий объект EdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2cd1d-123">Provide existing EdgeStorageAccount Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer
Parameter Sets: InvokeByInputObjectParameterSet
Aliases: EdgeContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2cd1d-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2cd1d-124">-Name</span></span>
<span data-ttu-id="2cd1d-125">Название ресурса</span><span class="sxs-lookup"><span data-stu-id="2cd1d-125">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases: EdgeContainerName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2cd1d-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2cd1d-126">-PassThru</span></span>
<span data-ttu-id="2cd1d-127">Возвращает значение истина, если выполнено успешно</span><span class="sxs-lookup"><span data-stu-id="2cd1d-127">returns true if successful</span></span>

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

### <span data-ttu-id="2cd1d-128">-RefreshData</span><span class="sxs-lookup"><span data-stu-id="2cd1d-128">-RefreshData</span></span>
<span data-ttu-id="2cd1d-129">Обновление метаданных контейнера с использованием данных из облака</span><span class="sxs-lookup"><span data-stu-id="2cd1d-129">Refresh Container Metadata with the data from the cloud</span></span>

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

### <span data-ttu-id="2cd1d-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2cd1d-130">-ResourceGroupName</span></span>
<span data-ttu-id="2cd1d-131">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="2cd1d-131">Resource Group Name</span></span>

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

### <span data-ttu-id="2cd1d-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2cd1d-132">-ResourceId</span></span>
<span data-ttu-id="2cd1d-133">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="2cd1d-133">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2cd1d-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2cd1d-134">-Confirm</span></span>
<span data-ttu-id="2cd1d-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2cd1d-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2cd1d-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2cd1d-136">-WhatIf</span></span>
<span data-ttu-id="2cd1d-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2cd1d-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2cd1d-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2cd1d-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2cd1d-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cd1d-139">CommonParameters</span></span>
<span data-ttu-id="2cd1d-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2cd1d-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cd1d-141">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2cd1d-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cd1d-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2cd1d-142">INPUTS</span></span>

### <span data-ttu-id="2cd1d-143">System. String</span><span class="sxs-lookup"><span data-stu-id="2cd1d-143">System.String</span></span>

### <span data-ttu-id="2cd1d-144">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="2cd1d-144">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="2cd1d-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2cd1d-145">OUTPUTS</span></span>

### <span data-ttu-id="2cd1d-146">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="2cd1d-146">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="2cd1d-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="2cd1d-147">NOTES</span></span>

## <span data-ttu-id="2cd1d-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2cd1d-148">RELATED LINKS</span></span>
