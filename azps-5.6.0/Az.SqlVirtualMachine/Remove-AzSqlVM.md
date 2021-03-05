---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/powershell/module/az.sqlvirtualmachine/remove-azsqlvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzSqlVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzSqlVM.md
ms.openlocfilehash: 741db1ddd4d2cce236d5a1d6787ea25179aa373f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101978003"
---
# <span data-ttu-id="6090c-101">Remove-AzSqlVM</span><span class="sxs-lookup"><span data-stu-id="6090c-101">Remove-AzSqlVM</span></span>

## <span data-ttu-id="6090c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6090c-102">SYNOPSIS</span></span>
<span data-ttu-id="6090c-103">Удаляет виртуальную машину SQL.</span><span class="sxs-lookup"><span data-stu-id="6090c-103">Deletes a sql virtual machine.</span></span>

## <span data-ttu-id="6090c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6090c-104">SYNTAX</span></span>

### <span data-ttu-id="6090c-105">Имя (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6090c-105">Name (Default)</span></span>
```
Remove-AzSqlVM [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6090c-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="6090c-106">InputObject</span></span>
```
Remove-AzSqlVM [-InputObject] <AzureSqlVMModel> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6090c-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="6090c-107">ResourceId</span></span>
```
Remove-AzSqlVM [-ResourceId] <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6090c-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6090c-108">DESCRIPTION</span></span>
<span data-ttu-id="6090c-109">Новый Remove-AzSqlVM удаляет виртуальную машину SQL.</span><span class="sxs-lookup"><span data-stu-id="6090c-109">The Remove-AzSqlVM cmdlet deletes a sql virtual machine.</span></span>

## <span data-ttu-id="6090c-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6090c-110">EXAMPLES</span></span>

### <span data-ttu-id="6090c-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6090c-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSqlVM -ResourceGroupName "ResourceGroup01" -Name "vm"
```

<span data-ttu-id="6090c-112">Удаляет виртуальную машину Azure SQL "vm" в группе ресурсов ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="6090c-112">Deletes the Azure SQL virtual machine "vm" in the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="6090c-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6090c-113">PARAMETERS</span></span>

### <span data-ttu-id="6090c-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6090c-114">-AsJob</span></span>
<span data-ttu-id="6090c-115">Запустите cmdlet в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="6090c-115">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="6090c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6090c-116">-DefaultProfile</span></span>
<span data-ttu-id="6090c-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6090c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6090c-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6090c-118">-InputObject</span></span>
<span data-ttu-id="6090c-119">SQL виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="6090c-119">SQL virtual machine object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel
Parameter Sets: InputObject
Aliases: SqlVM

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6090c-120">-Name</span><span class="sxs-lookup"><span data-stu-id="6090c-120">-Name</span></span>
<span data-ttu-id="6090c-121">SQL имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="6090c-121">SQL virtual machine name.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: SqlVMName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6090c-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6090c-122">-PassThru</span></span>
<span data-ttu-id="6090c-123">Определяет, следует ли вы выводить удаленный ресурс в конце выполнения выполнения cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6090c-123">Specifies whether to output the deleted resource at end of cmdlet execution.</span></span>

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

### <span data-ttu-id="6090c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6090c-124">-ResourceGroupName</span></span>
<span data-ttu-id="6090c-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6090c-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6090c-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6090c-126">-ResourceId</span></span>
<span data-ttu-id="6090c-127">SQL виртуальных машинных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6090c-127">SQL virtual machine resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases: SqlVMId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6090c-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6090c-128">-Confirm</span></span>
<span data-ttu-id="6090c-129">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="6090c-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6090c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6090c-130">-WhatIf</span></span>
<span data-ttu-id="6090c-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6090c-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6090c-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="6090c-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6090c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6090c-133">CommonParameters</span></span>
<span data-ttu-id="6090c-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6090c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6090c-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6090c-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6090c-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6090c-136">INPUTS</span></span>

### <span data-ttu-id="6090c-137">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMavire.Model.AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="6090c-137">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="6090c-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6090c-138">OUTPUTS</span></span>

### <span data-ttu-id="6090c-139">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMavire.Model.AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="6090c-139">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="6090c-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6090c-140">NOTES</span></span>

## <span data-ttu-id="6090c-141">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6090c-141">RELATED LINKS</span></span>
