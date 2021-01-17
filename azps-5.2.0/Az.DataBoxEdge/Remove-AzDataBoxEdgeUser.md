---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeUser.md
ms.openlocfilehash: cecfa3e009f6d6fbc7167c4b8f1ca110d547b5b7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98406068"
---
# <span data-ttu-id="2804b-101">Remove-AzDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="2804b-101">Remove-AzDataBoxEdgeUser</span></span>

## <span data-ttu-id="2804b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2804b-102">SYNOPSIS</span></span>
<span data-ttu-id="2804b-103">Удаляет пользователя на устройстве.</span><span class="sxs-lookup"><span data-stu-id="2804b-103">Removes a user on a device.</span></span>

## <span data-ttu-id="2804b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2804b-104">SYNTAX</span></span>

### <span data-ttu-id="2804b-105">DeleteByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2804b-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2804b-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2804b-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeUser [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2804b-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2804b-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeUser [-InputObject] <PSDataBoxEdgeUser> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2804b-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2804b-108">DESCRIPTION</span></span>
<span data-ttu-id="2804b-109">С **его учетной** записи удаляется пользователь на устройстве Edge Box Data Box.</span><span class="sxs-lookup"><span data-stu-id="2804b-109">The **Remove-AzDataBoxEdgeUser** cmdlet removes a user on the Data Box Edge device.</span></span> <span data-ttu-id="2804b-110">Поддерживается создание только пользователей `Share` разных типов.</span><span class="sxs-lookup"><span data-stu-id="2804b-110">Creation of only users of type `Share` is supported.</span></span>

## <span data-ttu-id="2804b-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2804b-111">EXAMPLES</span></span>

### <span data-ttu-id="2804b-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2804b-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
```

## <span data-ttu-id="2804b-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2804b-113">PARAMETERS</span></span>

### <span data-ttu-id="2804b-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2804b-114">-AsJob</span></span>
<span data-ttu-id="2804b-115">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="2804b-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2804b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2804b-116">-DefaultProfile</span></span>
<span data-ttu-id="2804b-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2804b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2804b-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="2804b-118">-DeviceName</span></span>
<span data-ttu-id="2804b-119">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="2804b-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2804b-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2804b-120">-InputObject</span></span>
<span data-ttu-id="2804b-121">Объект Input</span><span class="sxs-lookup"><span data-stu-id="2804b-121">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2804b-122">-Name</span><span class="sxs-lookup"><span data-stu-id="2804b-122">-Name</span></span>
<span data-ttu-id="2804b-123">Имя пользователя</span><span class="sxs-lookup"><span data-stu-id="2804b-123">Username</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2804b-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2804b-124">-PassThru</span></span>
<span data-ttu-id="2804b-125">Возвращает "Истина" в случае успеха.</span><span class="sxs-lookup"><span data-stu-id="2804b-125">returns true if successful</span></span>

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

### <span data-ttu-id="2804b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2804b-126">-ResourceGroupName</span></span>
<span data-ttu-id="2804b-127">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="2804b-127">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2804b-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2804b-128">-ResourceId</span></span>
<span data-ttu-id="2804b-129">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="2804b-129">Azure ResourceId</span></span>

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

### <span data-ttu-id="2804b-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2804b-130">-Confirm</span></span>
<span data-ttu-id="2804b-131">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="2804b-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2804b-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2804b-132">-WhatIf</span></span>
<span data-ttu-id="2804b-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2804b-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2804b-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="2804b-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2804b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2804b-135">CommonParameters</span></span>
<span data-ttu-id="2804b-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2804b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2804b-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2804b-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2804b-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2804b-138">INPUTS</span></span>

### <span data-ttu-id="2804b-139">System.String</span><span class="sxs-lookup"><span data-stu-id="2804b-139">System.String</span></span>

### <span data-ttu-id="2804b-140">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDAtaBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="2804b-140">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span></span>

## <span data-ttu-id="2804b-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2804b-141">OUTPUTS</span></span>

### <span data-ttu-id="2804b-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="2804b-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="2804b-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2804b-143">NOTES</span></span>

## <span data-ttu-id="2804b-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2804b-144">RELATED LINKS</span></span>
