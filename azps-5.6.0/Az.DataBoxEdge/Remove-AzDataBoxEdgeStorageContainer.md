---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/remove-azdataboxedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeStorageContainer.md
ms.openlocfilehash: a83880c9b5a2e300a5ad2aaef01ac540edfb8666
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004307"
---
# <span data-ttu-id="0e6d7-101">Remove-AzDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="0e6d7-101">Remove-AzDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="0e6d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0e6d7-102">SYNOPSIS</span></span>
<span data-ttu-id="0e6d7-103">Удаляет контейнер хранилища для учетной записи Edge Storage на устройстве.</span><span class="sxs-lookup"><span data-stu-id="0e6d7-103">Removes a storage container for the Edge Storage account on a device.</span></span>

## <span data-ttu-id="0e6d7-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="0e6d7-104">SYNTAX</span></span>

### <span data-ttu-id="0e6d7-105">DeleteByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0e6d7-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e6d7-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0e6d7-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeStorageContainer -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e6d7-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0e6d7-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeStorageContainer -InputObject <PSDataBoxEdgeStorageContainer> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e6d7-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0e6d7-108">DESCRIPTION</span></span>
<span data-ttu-id="0e6d7-109">С его учетной записью **на** устройстве Edge удаляется связанный контейнер хранилища для учетной записи Edge.</span><span class="sxs-lookup"><span data-stu-id="0e6d7-109">The **Remove-AzDataBoxEdgeStorageContainer** cmdlet removes an associated storage container for the Edge Storage account on a Data Box Edge device.</span></span> <span data-ttu-id="0e6d7-110">В качестве параметра можно указать имя удаляемого контейнера хранилища.</span><span class="sxs-lookup"><span data-stu-id="0e6d7-110">You can specify the name of the storage container to be removed as a parameter.</span></span>

## <span data-ttu-id="0e6d7-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="0e6d7-111">EXAMPLES</span></span>

### <span data-ttu-id="0e6d7-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0e6d7-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName deviceName -EdgeStorageAccountName edgestorageaccountname -Name container1
```

## <span data-ttu-id="0e6d7-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0e6d7-113">PARAMETERS</span></span>

### <span data-ttu-id="0e6d7-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0e6d7-114">-AsJob</span></span>
<span data-ttu-id="0e6d7-115">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="0e6d7-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0e6d7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e6d7-116">-DefaultProfile</span></span>
<span data-ttu-id="0e6d7-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0e6d7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0e6d7-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="0e6d7-118">-DeviceName</span></span>
<span data-ttu-id="0e6d7-119">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="0e6d7-119">Device Name</span></span>

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

### <span data-ttu-id="0e6d7-120">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="0e6d7-120">-EdgeStorageAccountName</span></span>
<span data-ttu-id="0e6d7-121">Укайм существующее имя EdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0e6d7-121">Provide existing EdgeStorageAccount's Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e6d7-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0e6d7-122">-InputObject</span></span>
<span data-ttu-id="0e6d7-123">Объект Input</span><span class="sxs-lookup"><span data-stu-id="0e6d7-123">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0e6d7-124">-Name</span><span class="sxs-lookup"><span data-stu-id="0e6d7-124">-Name</span></span>
<span data-ttu-id="0e6d7-125">Название ресурса</span><span class="sxs-lookup"><span data-stu-id="0e6d7-125">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e6d7-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0e6d7-126">-PassThru</span></span>
<span data-ttu-id="0e6d7-127">возвращает "Истина" в случае успеха.</span><span class="sxs-lookup"><span data-stu-id="0e6d7-127">returns true if successful</span></span>

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

### <span data-ttu-id="0e6d7-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e6d7-128">-ResourceGroupName</span></span>
<span data-ttu-id="0e6d7-129">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="0e6d7-129">Resource Group Name</span></span>

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

### <span data-ttu-id="0e6d7-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0e6d7-130">-ResourceId</span></span>
<span data-ttu-id="0e6d7-131">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="0e6d7-131">Azure ResourceId</span></span>

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

### <span data-ttu-id="0e6d7-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0e6d7-132">-Confirm</span></span>
<span data-ttu-id="0e6d7-133">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0e6d7-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e6d7-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e6d7-134">-WhatIf</span></span>
<span data-ttu-id="0e6d7-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0e6d7-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0e6d7-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="0e6d7-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e6d7-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e6d7-137">CommonParameters</span></span>
<span data-ttu-id="0e6d7-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e6d7-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e6d7-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0e6d7-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e6d7-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0e6d7-140">INPUTS</span></span>

### <span data-ttu-id="0e6d7-141">System.String</span><span class="sxs-lookup"><span data-stu-id="0e6d7-141">System.String</span></span>

### <span data-ttu-id="0e6d7-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDAtaBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="0e6d7-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="0e6d7-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0e6d7-143">OUTPUTS</span></span>

### <span data-ttu-id="0e6d7-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0e6d7-144">System.Boolean</span></span>

## <span data-ttu-id="0e6d7-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="0e6d7-145">NOTES</span></span>

## <span data-ttu-id="0e6d7-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0e6d7-146">RELATED LINKS</span></span>
