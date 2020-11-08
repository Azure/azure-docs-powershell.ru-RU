---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/remove-azsqlvmgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzSqlVMGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzSqlVMGroup.md
ms.openlocfilehash: fec35992f96940dc69cdb6d1777d43ca151688bc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94077536"
---
# <span data-ttu-id="48d48-101">Remove-AzSqlVMGroup</span><span class="sxs-lookup"><span data-stu-id="48d48-101">Remove-AzSqlVMGroup</span></span>

## <span data-ttu-id="48d48-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="48d48-102">SYNOPSIS</span></span>
<span data-ttu-id="48d48-103">Удаляет группу виртуальных машин SQL.</span><span class="sxs-lookup"><span data-stu-id="48d48-103">Deletes a sql virtual machine group.</span></span>

## <span data-ttu-id="48d48-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="48d48-104">SYNTAX</span></span>

### <span data-ttu-id="48d48-105">ParamaterList (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="48d48-105">ParamaterList (Default)</span></span>
```
Remove-AzSqlVMGroup [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="48d48-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="48d48-106">InputObject</span></span>
```
Remove-AzSqlVMGroup [-InputObject] <AzureSqlVMGroupModel> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48d48-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="48d48-107">ResourceId</span></span>
```
Remove-AzSqlVMGroup [-ResourceId] <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48d48-108">Псевдоним</span><span class="sxs-lookup"><span data-stu-id="48d48-108">Name</span></span>
```
Remove-AzSqlVMGroup [-AsJob] [-PassThru] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="48d48-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="48d48-109">DESCRIPTION</span></span>
<span data-ttu-id="48d48-110">Командлет Remove-AzSqlVMGroup удаляет группу виртуальных машин SQL.</span><span class="sxs-lookup"><span data-stu-id="48d48-110">The Remove-AzSqlVMGroup cmdlet deletes a sql virtual machine group.</span></span>

## <span data-ttu-id="48d48-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="48d48-111">EXAMPLES</span></span>

### <span data-ttu-id="48d48-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="48d48-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSqlVMGroup -ResourceGroupName "ResourceGroup01" -Name "test-group"
```

<span data-ttu-id="48d48-113">Удаляет группу виртуальных машин SQL Azure "тест-группа" в группе ресурсов ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="48d48-113">Deletes the Azure SQL virtual machine group "test-group" in the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="48d48-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="48d48-114">PARAMETERS</span></span>

### <span data-ttu-id="48d48-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="48d48-115">-AsJob</span></span>
<span data-ttu-id="48d48-116">Запустите командлет в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="48d48-116">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="48d48-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48d48-117">-DefaultProfile</span></span>
<span data-ttu-id="48d48-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="48d48-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="48d48-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="48d48-119">-InputObject</span></span>
<span data-ttu-id="48d48-120">Объект виртуальной машины SQL.</span><span class="sxs-lookup"><span data-stu-id="48d48-120">SQL virtual machine object.</span></span>

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

### <span data-ttu-id="48d48-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="48d48-121">-Name</span></span>
<span data-ttu-id="48d48-122">Имя группы виртуальной машины SQL.</span><span class="sxs-lookup"><span data-stu-id="48d48-122">SQL virtual machine group name.</span></span>

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

### <span data-ttu-id="48d48-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="48d48-123">-PassThru</span></span>
<span data-ttu-id="48d48-124">Указывает, следует ли выводить удаленный ресурс при завершении выполнения командлета.</span><span class="sxs-lookup"><span data-stu-id="48d48-124">Specifies whether to output the deleted resource at end of cmdlet execution.</span></span>

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

### <span data-ttu-id="48d48-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48d48-125">-ResourceGroupName</span></span>
<span data-ttu-id="48d48-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="48d48-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="48d48-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="48d48-127">-ResourceId</span></span>
<span data-ttu-id="48d48-128">Идентификатор ресурса группы виртуальной машины SQL.</span><span class="sxs-lookup"><span data-stu-id="48d48-128">SQL virtual machine group resource id.</span></span>

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

### <span data-ttu-id="48d48-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="48d48-129">-Confirm</span></span>
<span data-ttu-id="48d48-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="48d48-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48d48-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48d48-131">-WhatIf</span></span>
<span data-ttu-id="48d48-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="48d48-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="48d48-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="48d48-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48d48-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48d48-134">CommonParameters</span></span>
<span data-ttu-id="48d48-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="48d48-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48d48-136">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="48d48-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48d48-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="48d48-137">INPUTS</span></span>

### <span data-ttu-id="48d48-138">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="48d48-138">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

### <span data-ttu-id="48d48-139">System. String</span><span class="sxs-lookup"><span data-stu-id="48d48-139">System.String</span></span>

## <span data-ttu-id="48d48-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="48d48-140">OUTPUTS</span></span>

### <span data-ttu-id="48d48-141">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="48d48-141">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="48d48-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="48d48-142">NOTES</span></span>

## <span data-ttu-id="48d48-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="48d48-143">RELATED LINKS</span></span>
