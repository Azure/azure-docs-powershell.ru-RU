---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/remove-azsqlvmgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzSqlVMGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzSqlVMGroup.md
ms.openlocfilehash: fec35992f96940dc69cdb6d1777d43ca151688bc
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98394055"
---
# <span data-ttu-id="57165-101">Remove-AzSqlVMGroup</span><span class="sxs-lookup"><span data-stu-id="57165-101">Remove-AzSqlVMGroup</span></span>

## <span data-ttu-id="57165-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57165-102">SYNOPSIS</span></span>
<span data-ttu-id="57165-103">Удаляет группу виртуальных машин SQL.</span><span class="sxs-lookup"><span data-stu-id="57165-103">Deletes a sql virtual machine group.</span></span>

## <span data-ttu-id="57165-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="57165-104">SYNTAX</span></span>

### <span data-ttu-id="57165-105">Список paramaterList (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="57165-105">ParamaterList (Default)</span></span>
```
Remove-AzSqlVMGroup [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="57165-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="57165-106">InputObject</span></span>
```
Remove-AzSqlVMGroup [-InputObject] <AzureSqlVMGroupModel> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57165-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="57165-107">ResourceId</span></span>
```
Remove-AzSqlVMGroup [-ResourceId] <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57165-108">Имя</span><span class="sxs-lookup"><span data-stu-id="57165-108">Name</span></span>
```
Remove-AzSqlVMGroup [-AsJob] [-PassThru] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="57165-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="57165-109">DESCRIPTION</span></span>
<span data-ttu-id="57165-110">Этот Remove-AzSqlVMGroup удаляет группу виртуальных машин SQL.</span><span class="sxs-lookup"><span data-stu-id="57165-110">The Remove-AzSqlVMGroup cmdlet deletes a sql virtual machine group.</span></span>

## <span data-ttu-id="57165-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="57165-111">EXAMPLES</span></span>

### <span data-ttu-id="57165-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="57165-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSqlVMGroup -ResourceGroupName "ResourceGroup01" -Name "test-group"
```

<span data-ttu-id="57165-113">Удаляет группу виртуальных SQL Azure в группе ресурсов ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="57165-113">Deletes the Azure SQL virtual machine group "test-group" in the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="57165-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="57165-114">PARAMETERS</span></span>

### <span data-ttu-id="57165-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="57165-115">-AsJob</span></span>
<span data-ttu-id="57165-116">Запустите cmdlet в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="57165-116">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="57165-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57165-117">-DefaultProfile</span></span>
<span data-ttu-id="57165-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="57165-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57165-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="57165-119">-InputObject</span></span>
<span data-ttu-id="57165-120">SQL виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="57165-120">SQL virtual machine object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel
Parameter Sets: InputObject
Aliases: SqlVMGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="57165-121">-Name</span><span class="sxs-lookup"><span data-stu-id="57165-121">-Name</span></span>
<span data-ttu-id="57165-122">SQL группы виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="57165-122">SQL virtual machine group name.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: SqlVMGroupName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57165-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="57165-123">-PassThru</span></span>
<span data-ttu-id="57165-124">Определяет, следует ли вы выводить удаленный ресурс в конце выполнения cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57165-124">Specifies whether to output the deleted resource at end of cmdlet execution.</span></span>

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

### <span data-ttu-id="57165-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57165-125">-ResourceGroupName</span></span>
<span data-ttu-id="57165-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="57165-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="57165-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="57165-127">-ResourceId</span></span>
<span data-ttu-id="57165-128">SQL ресурса группы виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="57165-128">SQL virtual machine group resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases: SqlVMGroupId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57165-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="57165-129">-Confirm</span></span>
<span data-ttu-id="57165-130">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="57165-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57165-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57165-131">-WhatIf</span></span>
<span data-ttu-id="57165-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57165-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57165-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="57165-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57165-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57165-134">CommonParameters</span></span>
<span data-ttu-id="57165-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57165-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57165-136">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="57165-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57165-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="57165-137">INPUTS</span></span>

### <span data-ttu-id="57165-138">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMavire.Model.AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="57165-138">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

### <span data-ttu-id="57165-139">System.String</span><span class="sxs-lookup"><span data-stu-id="57165-139">System.String</span></span>

## <span data-ttu-id="57165-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="57165-140">OUTPUTS</span></span>

### <span data-ttu-id="57165-141">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMavire.Model.AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="57165-141">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="57165-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="57165-142">NOTES</span></span>

## <span data-ttu-id="57165-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="57165-143">RELATED LINKS</span></span>