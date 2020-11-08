---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/remove-azsqlvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzSqlVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzSqlVM.md
ms.openlocfilehash: 4478ec96cd7354a404a736ddd0f305cba5675b26
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245643"
---
# <span data-ttu-id="14384-101">Remove-AzSqlVM</span><span class="sxs-lookup"><span data-stu-id="14384-101">Remove-AzSqlVM</span></span>

## <span data-ttu-id="14384-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="14384-102">SYNOPSIS</span></span>
<span data-ttu-id="14384-103">Удаление виртуальной машины SQL.</span><span class="sxs-lookup"><span data-stu-id="14384-103">Deletes a sql virtual machine.</span></span>

## <span data-ttu-id="14384-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="14384-104">SYNTAX</span></span>

### <span data-ttu-id="14384-105">Имя (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="14384-105">Name (Default)</span></span>
```
Remove-AzSqlVM [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14384-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="14384-106">InputObject</span></span>
```
Remove-AzSqlVM [-InputObject] <AzureSqlVMModel> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14384-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="14384-107">ResourceId</span></span>
```
Remove-AzSqlVM [-ResourceId] <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="14384-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="14384-108">DESCRIPTION</span></span>
<span data-ttu-id="14384-109">Командлет Remove-AzSqlVM удаляет виртуальную машину SQL.</span><span class="sxs-lookup"><span data-stu-id="14384-109">The Remove-AzSqlVM cmdlet deletes a sql virtual machine.</span></span>

## <span data-ttu-id="14384-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="14384-110">EXAMPLES</span></span>

### <span data-ttu-id="14384-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="14384-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSqlVM -ResourceGroupName "ResourceGroup01" -Name "vm"
```

<span data-ttu-id="14384-112">Удаление виртуальной машины Azure SQL "VM" в группе ресурсов ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="14384-112">Deletes the Azure SQL virtual machine "vm" in the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="14384-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="14384-113">PARAMETERS</span></span>

### <span data-ttu-id="14384-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="14384-114">-AsJob</span></span>
<span data-ttu-id="14384-115">Запустите командлет в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="14384-115">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="14384-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14384-116">-DefaultProfile</span></span>
<span data-ttu-id="14384-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="14384-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14384-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="14384-118">-InputObject</span></span>
<span data-ttu-id="14384-119">Объект виртуальной машины SQL.</span><span class="sxs-lookup"><span data-stu-id="14384-119">SQL virtual machine object.</span></span>

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

### <span data-ttu-id="14384-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="14384-120">-Name</span></span>
<span data-ttu-id="14384-121">Имя виртуальной машины SQL.</span><span class="sxs-lookup"><span data-stu-id="14384-121">SQL virtual machine name.</span></span>

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

### <span data-ttu-id="14384-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="14384-122">-PassThru</span></span>
<span data-ttu-id="14384-123">Указывает, следует ли выводить удаленный ресурс при завершении выполнения командлета.</span><span class="sxs-lookup"><span data-stu-id="14384-123">Specifies whether to output the deleted resource at end of cmdlet execution.</span></span>

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

### <span data-ttu-id="14384-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14384-124">-ResourceGroupName</span></span>
<span data-ttu-id="14384-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="14384-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="14384-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="14384-126">-ResourceId</span></span>
<span data-ttu-id="14384-127">Идентификатор ресурса виртуальной машины SQL.</span><span class="sxs-lookup"><span data-stu-id="14384-127">SQL virtual machine resource id.</span></span>

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

### <span data-ttu-id="14384-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="14384-128">-Confirm</span></span>
<span data-ttu-id="14384-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="14384-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14384-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14384-130">-WhatIf</span></span>
<span data-ttu-id="14384-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="14384-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14384-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="14384-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14384-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14384-133">CommonParameters</span></span>
<span data-ttu-id="14384-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="14384-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14384-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="14384-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14384-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="14384-136">INPUTS</span></span>

### <span data-ttu-id="14384-137">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="14384-137">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="14384-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="14384-138">OUTPUTS</span></span>

### <span data-ttu-id="14384-139">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="14384-139">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="14384-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="14384-140">NOTES</span></span>

## <span data-ttu-id="14384-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="14384-141">RELATED LINKS</span></span>
