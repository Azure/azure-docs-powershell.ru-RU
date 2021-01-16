---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeStorageContainer.md
ms.openlocfilehash: 0e952ba845398fcd221ca7e5f4177a103b1f6155
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98411796"
---
# <span data-ttu-id="ccd7a-101">Remove-AzDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="ccd7a-101">Remove-AzDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="ccd7a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ccd7a-102">SYNOPSIS</span></span>
<span data-ttu-id="ccd7a-103">Удаляет контейнер хранилища для учетной записи Edge Storage на устройстве.</span><span class="sxs-lookup"><span data-stu-id="ccd7a-103">Removes a storage container for the Edge Storage account on a device.</span></span>

## <span data-ttu-id="ccd7a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ccd7a-104">SYNTAX</span></span>

### <span data-ttu-id="ccd7a-105">DeleteByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ccd7a-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ccd7a-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ccd7a-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeStorageContainer -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ccd7a-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ccd7a-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeStorageContainer -InputObject <PSDataBoxEdgeStorageContainer> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ccd7a-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ccd7a-108">DESCRIPTION</span></span>
<span data-ttu-id="ccd7a-109">С его учетной записью **на** устройстве Edge удаляется связанный контейнер хранилища для учетной записи Edge Storage.</span><span class="sxs-lookup"><span data-stu-id="ccd7a-109">The **Remove-AzDataBoxEdgeStorageContainer** cmdlet removes an associated storage container for the Edge Storage account on a Data Box Edge device.</span></span> <span data-ttu-id="ccd7a-110">В качестве параметра можно указать имя удаляемого контейнера хранилища.</span><span class="sxs-lookup"><span data-stu-id="ccd7a-110">You can specify the name of the storage container to be removed as a parameter.</span></span>

## <span data-ttu-id="ccd7a-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ccd7a-111">EXAMPLES</span></span>

### <span data-ttu-id="ccd7a-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ccd7a-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName deviceName -EdgeStorageAccountName edgestorageaccountname -Name container1
```

## <span data-ttu-id="ccd7a-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ccd7a-113">PARAMETERS</span></span>

### <span data-ttu-id="ccd7a-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ccd7a-114">-AsJob</span></span>
<span data-ttu-id="ccd7a-115">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="ccd7a-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ccd7a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccd7a-116">-DefaultProfile</span></span>
<span data-ttu-id="ccd7a-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ccd7a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ccd7a-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="ccd7a-118">-DeviceName</span></span>
<span data-ttu-id="ccd7a-119">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="ccd7a-119">Device Name</span></span>

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

### <span data-ttu-id="ccd7a-120">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="ccd7a-120">-EdgeStorageAccountName</span></span>
<span data-ttu-id="ccd7a-121">Укайм существующее имя EdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ccd7a-121">Provide existing EdgeStorageAccount's Name</span></span>

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

### <span data-ttu-id="ccd7a-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ccd7a-122">-InputObject</span></span>
<span data-ttu-id="ccd7a-123">Объект Input</span><span class="sxs-lookup"><span data-stu-id="ccd7a-123">Input Object</span></span>

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

### <span data-ttu-id="ccd7a-124">-Name</span><span class="sxs-lookup"><span data-stu-id="ccd7a-124">-Name</span></span>
<span data-ttu-id="ccd7a-125">Название ресурса</span><span class="sxs-lookup"><span data-stu-id="ccd7a-125">Resource Name</span></span>

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

### <span data-ttu-id="ccd7a-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ccd7a-126">-PassThru</span></span>
<span data-ttu-id="ccd7a-127">Возвращает "Истина" в случае успеха.</span><span class="sxs-lookup"><span data-stu-id="ccd7a-127">returns true if successful</span></span>

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

### <span data-ttu-id="ccd7a-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ccd7a-128">-ResourceGroupName</span></span>
<span data-ttu-id="ccd7a-129">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="ccd7a-129">Resource Group Name</span></span>

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

### <span data-ttu-id="ccd7a-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ccd7a-130">-ResourceId</span></span>
<span data-ttu-id="ccd7a-131">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="ccd7a-131">Azure ResourceId</span></span>

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

### <span data-ttu-id="ccd7a-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ccd7a-132">-Confirm</span></span>
<span data-ttu-id="ccd7a-133">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="ccd7a-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ccd7a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ccd7a-134">-WhatIf</span></span>
<span data-ttu-id="ccd7a-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ccd7a-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ccd7a-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="ccd7a-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ccd7a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccd7a-137">CommonParameters</span></span>
<span data-ttu-id="ccd7a-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ccd7a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccd7a-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ccd7a-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccd7a-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ccd7a-140">INPUTS</span></span>

### <span data-ttu-id="ccd7a-141">System.String</span><span class="sxs-lookup"><span data-stu-id="ccd7a-141">System.String</span></span>

### <span data-ttu-id="ccd7a-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDAtaBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="ccd7a-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="ccd7a-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ccd7a-143">OUTPUTS</span></span>

### <span data-ttu-id="ccd7a-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ccd7a-144">System.Boolean</span></span>

## <span data-ttu-id="ccd7a-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ccd7a-145">NOTES</span></span>

## <span data-ttu-id="ccd7a-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ccd7a-146">RELATED LINKS</span></span>
