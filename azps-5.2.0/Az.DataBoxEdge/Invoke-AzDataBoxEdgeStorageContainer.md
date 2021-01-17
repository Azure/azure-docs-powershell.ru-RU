---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/invoke-azdataboxedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Invoke-AzDataBoxEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Invoke-AzDataBoxEdgeStorageContainer.md
ms.openlocfilehash: f897c2adfe4154aeff5bd370437ea8b23e4efd36
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98411060"
---
# <span data-ttu-id="7bbc0-101">Invoke-AzDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="7bbc0-101">Invoke-AzDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="7bbc0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7bbc0-102">SYNOPSIS</span></span>
<span data-ttu-id="7bbc0-103">Вызывает определенные действия с контейнером хранилища.</span><span class="sxs-lookup"><span data-stu-id="7bbc0-103">Invokes specific actions on a storage container</span></span>

## <span data-ttu-id="7bbc0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7bbc0-104">SYNTAX</span></span>

### <span data-ttu-id="7bbc0-105">InvokeByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7bbc0-105">InvokeByNameParameterSet (Default)</span></span>
```
Invoke-AzDataBoxEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-RefreshData] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7bbc0-106">InvokeByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7bbc0-106">InvokeByResourceIdParameterSet</span></span>
```
Invoke-AzDataBoxEdgeStorageContainer [-ResourceId] <String> [-RefreshData] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7bbc0-107">InvokeByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7bbc0-107">InvokeByInputObjectParameterSet</span></span>
```
Invoke-AzDataBoxEdgeStorageContainer [-RefreshData] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 -InputObject <PSDataBoxEdgeStorageContainer> [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7bbc0-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7bbc0-108">DESCRIPTION</span></span>
<span data-ttu-id="7bbc0-109">**Cmdlet Invoke-AzDataBoxEdgeStorageContainer** вызывает действия для обновления данных в контейнере хранилища на устройстве Edge Data Box.</span><span class="sxs-lookup"><span data-stu-id="7bbc0-109">The **Invoke-AzDataBoxEdgeStorageContainer** cmdlet invokes actions to refresh the data on a storage container on a Data Box Edge device.</span></span> 

## <span data-ttu-id="7bbc0-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7bbc0-110">EXAMPLES</span></span>

### <span data-ttu-id="7bbc0-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7bbc0-111">Example 1</span></span>
```powershell
PS C:\> Invoke-AzDataBoxEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName deviceName -EdgeStorageAccountName edgestorageaccount1 -Name container1 -PassThru
PS C:\> true
```

### <span data-ttu-id="7bbc0-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="7bbc0-112">Example 2</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName deviceName -EdgeStorageAccountName edgestorageaccount1 -Name container1 | Invoke-AzDataBoxEdgeStorageContainer
```

## <span data-ttu-id="7bbc0-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7bbc0-113">PARAMETERS</span></span>

### <span data-ttu-id="7bbc0-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7bbc0-114">-AsJob</span></span>
<span data-ttu-id="7bbc0-115">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="7bbc0-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7bbc0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bbc0-116">-DefaultProfile</span></span>
<span data-ttu-id="7bbc0-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7bbc0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7bbc0-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="7bbc0-118">-DeviceName</span></span>
<span data-ttu-id="7bbc0-119">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="7bbc0-119">Device Name</span></span>

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

### <span data-ttu-id="7bbc0-120">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="7bbc0-120">-EdgeStorageAccountName</span></span>
<span data-ttu-id="7bbc0-121">Название ресурса</span><span class="sxs-lookup"><span data-stu-id="7bbc0-121">Resource Name</span></span>

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

### <span data-ttu-id="7bbc0-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7bbc0-122">-InputObject</span></span>
<span data-ttu-id="7bbc0-123">Предоставление существующего объекта EdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7bbc0-123">Provide existing EdgeStorageAccount Object</span></span>

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

### <span data-ttu-id="7bbc0-124">-Name</span><span class="sxs-lookup"><span data-stu-id="7bbc0-124">-Name</span></span>
<span data-ttu-id="7bbc0-125">Название ресурса</span><span class="sxs-lookup"><span data-stu-id="7bbc0-125">Resource Name</span></span>

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

### <span data-ttu-id="7bbc0-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7bbc0-126">-PassThru</span></span>
<span data-ttu-id="7bbc0-127">Возвращает "Истина" в случае успеха.</span><span class="sxs-lookup"><span data-stu-id="7bbc0-127">returns true if successful</span></span>

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

### <span data-ttu-id="7bbc0-128">-RefreshData</span><span class="sxs-lookup"><span data-stu-id="7bbc0-128">-RefreshData</span></span>
<span data-ttu-id="7bbc0-129">Обновление метаданных контейнера с данными из облака</span><span class="sxs-lookup"><span data-stu-id="7bbc0-129">Refresh Container Metadata with the data from the cloud</span></span>

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

### <span data-ttu-id="7bbc0-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7bbc0-130">-ResourceGroupName</span></span>
<span data-ttu-id="7bbc0-131">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="7bbc0-131">Resource Group Name</span></span>

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

### <span data-ttu-id="7bbc0-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7bbc0-132">-ResourceId</span></span>
<span data-ttu-id="7bbc0-133">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="7bbc0-133">Azure ResourceId</span></span>

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

### <span data-ttu-id="7bbc0-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7bbc0-134">-Confirm</span></span>
<span data-ttu-id="7bbc0-135">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7bbc0-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7bbc0-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7bbc0-136">-WhatIf</span></span>
<span data-ttu-id="7bbc0-137">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7bbc0-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7bbc0-138">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="7bbc0-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7bbc0-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bbc0-139">CommonParameters</span></span>
<span data-ttu-id="7bbc0-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7bbc0-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bbc0-141">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7bbc0-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bbc0-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7bbc0-142">INPUTS</span></span>

### <span data-ttu-id="7bbc0-143">System.String</span><span class="sxs-lookup"><span data-stu-id="7bbc0-143">System.String</span></span>

### <span data-ttu-id="7bbc0-144">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDAtaBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="7bbc0-144">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="7bbc0-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7bbc0-145">OUTPUTS</span></span>

### <span data-ttu-id="7bbc0-146">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDAtaBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="7bbc0-146">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="7bbc0-147">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7bbc0-147">NOTES</span></span>

## <span data-ttu-id="7bbc0-148">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7bbc0-148">RELATED LINKS</span></span>
