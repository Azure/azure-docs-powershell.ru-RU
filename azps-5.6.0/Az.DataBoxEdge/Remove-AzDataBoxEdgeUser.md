---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/remove-azdataboxedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeUser.md
ms.openlocfilehash: 8c977c61f332ccdc927dd3f0e070d635e6095acf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983240"
---
# <span data-ttu-id="6601a-101">Remove-AzDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="6601a-101">Remove-AzDataBoxEdgeUser</span></span>

## <span data-ttu-id="6601a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6601a-102">SYNOPSIS</span></span>
<span data-ttu-id="6601a-103">Удаляет пользователя на устройстве.</span><span class="sxs-lookup"><span data-stu-id="6601a-103">Removes a user on a device.</span></span>

## <span data-ttu-id="6601a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6601a-104">SYNTAX</span></span>

### <span data-ttu-id="6601a-105">DeleteByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6601a-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6601a-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6601a-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeUser [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6601a-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6601a-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeUser [-InputObject] <PSDataBoxEdgeUser> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6601a-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6601a-108">DESCRIPTION</span></span>
<span data-ttu-id="6601a-109">С **его учетной** записи удаляется пользователь с устройства Edge Box Data Box.</span><span class="sxs-lookup"><span data-stu-id="6601a-109">The **Remove-AzDataBoxEdgeUser** cmdlet removes a user on the Data Box Edge device.</span></span> <span data-ttu-id="6601a-110">Поддерживается создание только пользователей `Share` разных типов.</span><span class="sxs-lookup"><span data-stu-id="6601a-110">Creation of only users of type `Share` is supported.</span></span>

## <span data-ttu-id="6601a-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6601a-111">EXAMPLES</span></span>

### <span data-ttu-id="6601a-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6601a-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
```

## <span data-ttu-id="6601a-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6601a-113">PARAMETERS</span></span>

### <span data-ttu-id="6601a-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6601a-114">-AsJob</span></span>
<span data-ttu-id="6601a-115">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="6601a-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6601a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6601a-116">-DefaultProfile</span></span>
<span data-ttu-id="6601a-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6601a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6601a-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="6601a-118">-DeviceName</span></span>
<span data-ttu-id="6601a-119">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="6601a-119">Device Name</span></span>

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

### <span data-ttu-id="6601a-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6601a-120">-InputObject</span></span>
<span data-ttu-id="6601a-121">Объект Input</span><span class="sxs-lookup"><span data-stu-id="6601a-121">Input Object</span></span>

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

### <span data-ttu-id="6601a-122">-Name</span><span class="sxs-lookup"><span data-stu-id="6601a-122">-Name</span></span>
<span data-ttu-id="6601a-123">Имя пользователя</span><span class="sxs-lookup"><span data-stu-id="6601a-123">Username</span></span>

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

### <span data-ttu-id="6601a-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6601a-124">-PassThru</span></span>
<span data-ttu-id="6601a-125">Возвращает "Истина" в случае успеха.</span><span class="sxs-lookup"><span data-stu-id="6601a-125">returns true if successful</span></span>

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

### <span data-ttu-id="6601a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6601a-126">-ResourceGroupName</span></span>
<span data-ttu-id="6601a-127">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="6601a-127">Resource Group Name</span></span>

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

### <span data-ttu-id="6601a-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6601a-128">-ResourceId</span></span>
<span data-ttu-id="6601a-129">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="6601a-129">Azure ResourceId</span></span>

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

### <span data-ttu-id="6601a-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6601a-130">-Confirm</span></span>
<span data-ttu-id="6601a-131">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="6601a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6601a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6601a-132">-WhatIf</span></span>
<span data-ttu-id="6601a-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6601a-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6601a-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="6601a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6601a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6601a-135">CommonParameters</span></span>
<span data-ttu-id="6601a-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6601a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6601a-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6601a-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6601a-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6601a-138">INPUTS</span></span>

### <span data-ttu-id="6601a-139">System.String</span><span class="sxs-lookup"><span data-stu-id="6601a-139">System.String</span></span>

### <span data-ttu-id="6601a-140">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDAtaBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="6601a-140">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span></span>

## <span data-ttu-id="6601a-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6601a-141">OUTPUTS</span></span>

### <span data-ttu-id="6601a-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="6601a-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="6601a-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6601a-143">NOTES</span></span>

## <span data-ttu-id="6601a-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6601a-144">RELATED LINKS</span></span>
