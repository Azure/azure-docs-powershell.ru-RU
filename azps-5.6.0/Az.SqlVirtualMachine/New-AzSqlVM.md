---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/powershell/module/az.sqlvirtualmachine/new-azsqlvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVM.md
ms.openlocfilehash: f7afae369258a30a156ff0439407fb4e4e4ef732
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008312"
---
# <span data-ttu-id="2eb9f-101">New-AzSqlVM</span><span class="sxs-lookup"><span data-stu-id="2eb9f-101">New-AzSqlVM</span></span>

## <span data-ttu-id="2eb9f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2eb9f-102">SYNOPSIS</span></span>
<span data-ttu-id="2eb9f-103">Создает новую виртуальную машину SQL.</span><span class="sxs-lookup"><span data-stu-id="2eb9f-103">Creates a new sql virtual machine.</span></span>

## <span data-ttu-id="2eb9f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2eb9f-104">SYNTAX</span></span>

### <span data-ttu-id="2eb9f-105">NameParamaterList (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2eb9f-105">NameParamaterList (Default)</span></span>
```
New-AzSqlVM [-ResourceGroupName] <String> [-Name] <String> [-LicenseType] <String> -Location <String> [-AsJob]
 [-Offer <String>] [-Sku <String>] [-SqlManagementType <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2eb9f-106">NameInputObject</span><span class="sxs-lookup"><span data-stu-id="2eb9f-106">NameInputObject</span></span>
```
New-AzSqlVM [-ResourceGroupName] <String> [-Name] <String> [-SqlVM] <AzureSqlVMModel> -Location <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2eb9f-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2eb9f-107">DESCRIPTION</span></span>
<span data-ttu-id="2eb9f-108">С New-AzSqlVM-клиент создается виртуальная SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="2eb9f-108">The New-AzSqlVM cmdlet creates an Azure SQL virtual machine.</span></span>

## <span data-ttu-id="2eb9f-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2eb9f-109">EXAMPLES</span></span>

### <span data-ttu-id="2eb9f-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2eb9f-110">Example 1</span></span>
```powershell
PS C:\> New-AzSqlVM  New-AzSqlVM -ResourceGroupName ResourceGroup01 -Name vm -LicenseType 'PAYG' -Sku Developer
Name ResourceGroupName  LicenseType Sku       Offer          SqlManagementType
---- -----------------  ----------- ---       -----          -----------------
vm   ResourceGroup01    PAYG        Developer SQL2017-WS2016 Full
```

<span data-ttu-id="2eb9f-111">Создание новой виртуальной машины Azure SQL с именем vm в группе ресурсов ResourceGroup01</span><span class="sxs-lookup"><span data-stu-id="2eb9f-111">Creates a new Azure SQL virtual machine with name vm in the resource group ResourceGroup01</span></span> 

## <span data-ttu-id="2eb9f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2eb9f-112">PARAMETERS</span></span>

### <span data-ttu-id="2eb9f-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2eb9f-113">-AsJob</span></span>
<span data-ttu-id="2eb9f-114">Запустите cmdlet в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="2eb9f-114">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="2eb9f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2eb9f-115">-DefaultProfile</span></span>
<span data-ttu-id="2eb9f-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2eb9f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2eb9f-117">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="2eb9f-117">-LicenseType</span></span>
<span data-ttu-id="2eb9f-118">SQL тип лицензии виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="2eb9f-118">SQL virtual machine license type.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParamaterList
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2eb9f-119">-Location</span><span class="sxs-lookup"><span data-stu-id="2eb9f-119">-Location</span></span>
<span data-ttu-id="2eb9f-120">SQL расположение виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="2eb9f-120">SQL virtual machine location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2eb9f-121">-Name</span><span class="sxs-lookup"><span data-stu-id="2eb9f-121">-Name</span></span>
<span data-ttu-id="2eb9f-122">SQL имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="2eb9f-122">SQL virtual machine name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SqlVMName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2eb9f-123">-Offer</span><span class="sxs-lookup"><span data-stu-id="2eb9f-123">-Offer</span></span>
<span data-ttu-id="2eb9f-124">SQL виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="2eb9f-124">SQL virtual machine offer.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParamaterList
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2eb9f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2eb9f-125">-ResourceGroupName</span></span>
<span data-ttu-id="2eb9f-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2eb9f-126">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2eb9f-127">-SKU</span><span class="sxs-lookup"><span data-stu-id="2eb9f-127">-Sku</span></span>
<span data-ttu-id="2eb9f-128">SQL выпуска виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="2eb9f-128">SQL virtual machine edition type.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParamaterList
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2eb9f-129">-SqlManagementType</span><span class="sxs-lookup"><span data-stu-id="2eb9f-129">-SqlManagementType</span></span>
<span data-ttu-id="2eb9f-130">SQL типа управления виртуальными компьютерами.</span><span class="sxs-lookup"><span data-stu-id="2eb9f-130">SQL virtual machine management type.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParamaterList
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2eb9f-131">-SqlVM</span><span class="sxs-lookup"><span data-stu-id="2eb9f-131">-SqlVM</span></span>
<span data-ttu-id="2eb9f-132">SQL виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="2eb9f-132">SQL virtual machine object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel
Parameter Sets: NameInputObject
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2eb9f-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="2eb9f-133">-Tag</span></span>
<span data-ttu-id="2eb9f-134">Теги, которые нужно связать с виртуальной SQL компьютера</span><span class="sxs-lookup"><span data-stu-id="2eb9f-134">The tags to associate with the SQL virtual machine</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: NameParamaterList
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2eb9f-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2eb9f-135">-Confirm</span></span>
<span data-ttu-id="2eb9f-136">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2eb9f-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2eb9f-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2eb9f-137">-WhatIf</span></span>
<span data-ttu-id="2eb9f-138">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2eb9f-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2eb9f-139">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="2eb9f-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2eb9f-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2eb9f-140">CommonParameters</span></span>
<span data-ttu-id="2eb9f-141">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2eb9f-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2eb9f-142">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2eb9f-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2eb9f-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2eb9f-143">INPUTS</span></span>

### <span data-ttu-id="2eb9f-144">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMavire.Model.AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="2eb9f-144">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="2eb9f-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2eb9f-145">OUTPUTS</span></span>

### <span data-ttu-id="2eb9f-146">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMavire.Model.AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="2eb9f-146">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="2eb9f-147">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2eb9f-147">NOTES</span></span>

## <span data-ttu-id="2eb9f-148">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2eb9f-148">RELATED LINKS</span></span>
