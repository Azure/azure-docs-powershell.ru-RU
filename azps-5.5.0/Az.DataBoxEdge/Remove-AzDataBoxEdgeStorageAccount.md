---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgestorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeStorageAccount.md
ms.openlocfilehash: 1f8e20b826a477778de5325ff147cbd7ad28a9fb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100242848"
---
# <span data-ttu-id="caad4-101">Remove-AzDataBoxEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="caad4-101">Remove-AzDataBoxEdgeStorageAccount</span></span>

## <span data-ttu-id="caad4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="caad4-102">SYNOPSIS</span></span>
<span data-ttu-id="caad4-103">Удаляет учетную запись edge Storage для устройства.</span><span class="sxs-lookup"><span data-stu-id="caad4-103">Removes the Edge Storage account for a device.</span></span>

## <span data-ttu-id="caad4-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="caad4-104">SYNTAX</span></span>

### <span data-ttu-id="caad4-105">DeleteByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="caad4-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="caad4-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="caad4-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeStorageAccount [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="caad4-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="caad4-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeStorageAccount [-InputObject] <PSDataBoxEdgeStorageAccount> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="caad4-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="caad4-108">DESCRIPTION</span></span>
<span data-ttu-id="caad4-109">С **его учетной** записью удаляется связанная учетная запись хранилищ Edge для устройства Edge Data Box.</span><span class="sxs-lookup"><span data-stu-id="caad4-109">The **Remove-AzDataBoxEdgeStorageAccount** cmdlet removes an associated Edge Storage Account for a Data Box Edge device.</span></span> <span data-ttu-id="caad4-110">Вы можете указать имя учетной записи edge Storage, которая будет удалена в качестве параметра в cmdlet.</span><span class="sxs-lookup"><span data-stu-id="caad4-110">You can specify the name of the Edge Storage Account to be removed as a parameter in the cmdlet.</span></span>

## <span data-ttu-id="caad4-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="caad4-111">EXAMPLES</span></span>

### <span data-ttu-id="caad4-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="caad4-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeStorageAccount -ResourceGroupName resourceGroupName -DeviceName deviceName -Name edgestorageaccountname
```

## <span data-ttu-id="caad4-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="caad4-113">PARAMETERS</span></span>

### <span data-ttu-id="caad4-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="caad4-114">-AsJob</span></span>
<span data-ttu-id="caad4-115">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="caad4-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="caad4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="caad4-116">-DefaultProfile</span></span>
<span data-ttu-id="caad4-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="caad4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="caad4-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="caad4-118">-DeviceName</span></span>
<span data-ttu-id="caad4-119">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="caad4-119">Device Name</span></span>

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

### <span data-ttu-id="caad4-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="caad4-120">-InputObject</span></span>
<span data-ttu-id="caad4-121">Объект Input</span><span class="sxs-lookup"><span data-stu-id="caad4-121">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="caad4-122">-Name</span><span class="sxs-lookup"><span data-stu-id="caad4-122">-Name</span></span>
<span data-ttu-id="caad4-123">Название ресурса</span><span class="sxs-lookup"><span data-stu-id="caad4-123">Resource Name</span></span>

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

### <span data-ttu-id="caad4-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="caad4-124">-PassThru</span></span>
<span data-ttu-id="caad4-125">возвращает "Истина" в случае успеха.</span><span class="sxs-lookup"><span data-stu-id="caad4-125">returns true if successful</span></span>

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

### <span data-ttu-id="caad4-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="caad4-126">-ResourceGroupName</span></span>
<span data-ttu-id="caad4-127">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="caad4-127">Resource Group Name</span></span>

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

### <span data-ttu-id="caad4-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="caad4-128">-ResourceId</span></span>
<span data-ttu-id="caad4-129">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="caad4-129">Azure ResourceId</span></span>

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

### <span data-ttu-id="caad4-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="caad4-130">-Confirm</span></span>
<span data-ttu-id="caad4-131">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="caad4-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="caad4-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="caad4-132">-WhatIf</span></span>
<span data-ttu-id="caad4-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="caad4-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="caad4-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="caad4-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="caad4-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="caad4-135">CommonParameters</span></span>
<span data-ttu-id="caad4-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="caad4-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="caad4-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="caad4-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="caad4-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="caad4-138">INPUTS</span></span>

### <span data-ttu-id="caad4-139">System.String</span><span class="sxs-lookup"><span data-stu-id="caad4-139">System.String</span></span>

### <span data-ttu-id="caad4-140">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDAtaBoxEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="caad4-140">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount</span></span>

## <span data-ttu-id="caad4-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="caad4-141">OUTPUTS</span></span>

### <span data-ttu-id="caad4-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="caad4-142">System.Boolean</span></span>

## <span data-ttu-id="caad4-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="caad4-143">NOTES</span></span>

## <span data-ttu-id="caad4-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="caad4-144">RELATED LINKS</span></span>
