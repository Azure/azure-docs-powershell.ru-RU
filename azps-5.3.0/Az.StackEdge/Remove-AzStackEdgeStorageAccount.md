---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgestorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeStorageAccount.md
ms.openlocfilehash: d4b815e0caa85bee26086f475f86e1757b690fbd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98420135"
---
# <span data-ttu-id="57163-101">Remove-AzStackEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="57163-101">Remove-AzStackEdgeStorageAccount</span></span>

## <span data-ttu-id="57163-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57163-102">SYNOPSIS</span></span>
<span data-ttu-id="57163-103">Удаляет учетную запись edge Storage для устройства.</span><span class="sxs-lookup"><span data-stu-id="57163-103">Removes the Edge Storage account for a device.</span></span>

## <span data-ttu-id="57163-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="57163-104">SYNTAX</span></span>

### <span data-ttu-id="57163-105">DeleteByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="57163-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57163-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="57163-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeStorageAccount [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57163-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="57163-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeStorageAccount [-InputObject] <PSStackEdgeStorageAccount> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="57163-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="57163-108">DESCRIPTION</span></span>
<span data-ttu-id="57163-109">Для устройства Stack Edge с его учетной записью удаляется связанная учетная запись хранилищ **AzStackEdgeStorageAccount.**</span><span class="sxs-lookup"><span data-stu-id="57163-109">The **Remove-AzStackEdgeStorageAccount** cmdlet removes an associated Edge Storage Account for a Stack Edge device.</span></span> <span data-ttu-id="57163-110">Вы можете указать имя учетной записи edge Storage, которая будет удалена в качестве параметра в cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57163-110">You can specify the name of the Edge Storage Account to be removed as a parameter in the cmdlet.</span></span>

## <span data-ttu-id="57163-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="57163-111">EXAMPLES</span></span>

### <span data-ttu-id="57163-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="57163-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeStorageAccount -ResourceGroupName resourceGroupName -DeviceName deviceName -Name edgestorageaccountname
```

## <span data-ttu-id="57163-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="57163-113">PARAMETERS</span></span>

### <span data-ttu-id="57163-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="57163-114">-AsJob</span></span>
<span data-ttu-id="57163-115">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="57163-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="57163-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57163-116">-DefaultProfile</span></span>
<span data-ttu-id="57163-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="57163-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57163-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="57163-118">-DeviceName</span></span>
<span data-ttu-id="57163-119">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="57163-119">Device Name</span></span>

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

### <span data-ttu-id="57163-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="57163-120">-InputObject</span></span>
<span data-ttu-id="57163-121">Объект Input</span><span class="sxs-lookup"><span data-stu-id="57163-121">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: EdgeStorageAccount

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="57163-122">-Name</span><span class="sxs-lookup"><span data-stu-id="57163-122">-Name</span></span>
<span data-ttu-id="57163-123">Название ресурса</span><span class="sxs-lookup"><span data-stu-id="57163-123">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: EdgeStorageAccountName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57163-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="57163-124">-PassThru</span></span>
<span data-ttu-id="57163-125">возвращает "Истина" в случае успеха.</span><span class="sxs-lookup"><span data-stu-id="57163-125">returns true if successful</span></span>

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

### <span data-ttu-id="57163-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57163-126">-ResourceGroupName</span></span>
<span data-ttu-id="57163-127">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="57163-127">Resource Group Name</span></span>

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

### <span data-ttu-id="57163-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="57163-128">-ResourceId</span></span>
<span data-ttu-id="57163-129">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="57163-129">Azure ResourceId</span></span>

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

### <span data-ttu-id="57163-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="57163-130">-Confirm</span></span>
<span data-ttu-id="57163-131">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57163-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57163-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57163-132">-WhatIf</span></span>
<span data-ttu-id="57163-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57163-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="57163-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="57163-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57163-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57163-135">CommonParameters</span></span>
<span data-ttu-id="57163-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57163-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57163-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="57163-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57163-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="57163-138">INPUTS</span></span>

### <span data-ttu-id="57163-139">System.String</span><span class="sxs-lookup"><span data-stu-id="57163-139">System.String</span></span>

### <span data-ttu-id="57163-140">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="57163-140">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount</span></span>

## <span data-ttu-id="57163-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="57163-141">OUTPUTS</span></span>

### <span data-ttu-id="57163-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="57163-142">System.Boolean</span></span>

## <span data-ttu-id="57163-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="57163-143">NOTES</span></span>

## <span data-ttu-id="57163-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="57163-144">RELATED LINKS</span></span>
