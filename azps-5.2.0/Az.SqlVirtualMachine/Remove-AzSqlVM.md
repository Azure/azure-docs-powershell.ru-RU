---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/remove-azsqlvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzSqlVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzSqlVM.md
ms.openlocfilehash: 4478ec96cd7354a404a736ddd0f305cba5675b26
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98394076"
---
# <span data-ttu-id="ffb2e-101">Remove-AzSqlVM</span><span class="sxs-lookup"><span data-stu-id="ffb2e-101">Remove-AzSqlVM</span></span>

## <span data-ttu-id="ffb2e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ffb2e-102">SYNOPSIS</span></span>
<span data-ttu-id="ffb2e-103">Удаляет виртуальную машину SQL.</span><span class="sxs-lookup"><span data-stu-id="ffb2e-103">Deletes a sql virtual machine.</span></span>

## <span data-ttu-id="ffb2e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ffb2e-104">SYNTAX</span></span>

### <span data-ttu-id="ffb2e-105">Имя (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ffb2e-105">Name (Default)</span></span>
```
Remove-AzSqlVM [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ffb2e-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="ffb2e-106">InputObject</span></span>
```
Remove-AzSqlVM [-InputObject] <AzureSqlVMModel> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ffb2e-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="ffb2e-107">ResourceId</span></span>
```
Remove-AzSqlVM [-ResourceId] <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ffb2e-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ffb2e-108">DESCRIPTION</span></span>
<span data-ttu-id="ffb2e-109">Новый Remove-AzSqlVM удаляет виртуальную машину SQL.</span><span class="sxs-lookup"><span data-stu-id="ffb2e-109">The Remove-AzSqlVM cmdlet deletes a sql virtual machine.</span></span>

## <span data-ttu-id="ffb2e-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ffb2e-110">EXAMPLES</span></span>

### <span data-ttu-id="ffb2e-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ffb2e-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSqlVM -ResourceGroupName "ResourceGroup01" -Name "vm"
```

<span data-ttu-id="ffb2e-112">Удаляет виртуальную машину Azure SQL "vm" в группе ресурсов ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="ffb2e-112">Deletes the Azure SQL virtual machine "vm" in the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="ffb2e-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ffb2e-113">PARAMETERS</span></span>

### <span data-ttu-id="ffb2e-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ffb2e-114">-AsJob</span></span>
<span data-ttu-id="ffb2e-115">Запустите cmdlet в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="ffb2e-115">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="ffb2e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffb2e-116">-DefaultProfile</span></span>
<span data-ttu-id="ffb2e-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ffb2e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ffb2e-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ffb2e-118">-InputObject</span></span>
<span data-ttu-id="ffb2e-119">SQL виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="ffb2e-119">SQL virtual machine object.</span></span>

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

### <span data-ttu-id="ffb2e-120">-Name</span><span class="sxs-lookup"><span data-stu-id="ffb2e-120">-Name</span></span>
<span data-ttu-id="ffb2e-121">SQL имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="ffb2e-121">SQL virtual machine name.</span></span>

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

### <span data-ttu-id="ffb2e-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ffb2e-122">-PassThru</span></span>
<span data-ttu-id="ffb2e-123">Определяет, следует ли вы выводить удаленный ресурс в конце выполнения cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ffb2e-123">Specifies whether to output the deleted resource at end of cmdlet execution.</span></span>

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

### <span data-ttu-id="ffb2e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ffb2e-124">-ResourceGroupName</span></span>
<span data-ttu-id="ffb2e-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ffb2e-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="ffb2e-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ffb2e-126">-ResourceId</span></span>
<span data-ttu-id="ffb2e-127">SQL ресурса виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="ffb2e-127">SQL virtual machine resource id.</span></span>

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

### <span data-ttu-id="ffb2e-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ffb2e-128">-Confirm</span></span>
<span data-ttu-id="ffb2e-129">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ffb2e-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ffb2e-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ffb2e-130">-WhatIf</span></span>
<span data-ttu-id="ffb2e-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ffb2e-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ffb2e-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="ffb2e-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ffb2e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffb2e-133">CommonParameters</span></span>
<span data-ttu-id="ffb2e-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ffb2e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffb2e-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ffb2e-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffb2e-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ffb2e-136">INPUTS</span></span>

### <span data-ttu-id="ffb2e-137">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMavire.Model.AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="ffb2e-137">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="ffb2e-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ffb2e-138">OUTPUTS</span></span>

### <span data-ttu-id="ffb2e-139">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMavire.Model.AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="ffb2e-139">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="ffb2e-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ffb2e-140">NOTES</span></span>

## <span data-ttu-id="ffb2e-141">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ffb2e-141">RELATED LINKS</span></span>