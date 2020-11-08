---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/new-azsqlvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVM.md
ms.openlocfilehash: 764312c64ae9887a6ef4243cc20b04535afcf81f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246950"
---
# <span data-ttu-id="37446-101">New-AzSqlVM</span><span class="sxs-lookup"><span data-stu-id="37446-101">New-AzSqlVM</span></span>

## <span data-ttu-id="37446-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="37446-102">SYNOPSIS</span></span>
<span data-ttu-id="37446-103">Создание новой виртуальной машины SQL.</span><span class="sxs-lookup"><span data-stu-id="37446-103">Creates a new sql virtual machine.</span></span>

## <span data-ttu-id="37446-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="37446-104">SYNTAX</span></span>

### <span data-ttu-id="37446-105">NameParamaterList (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="37446-105">NameParamaterList (Default)</span></span>
```
New-AzSqlVM [-ResourceGroupName] <String> [-Name] <String> [-LicenseType] <String> -Location <String> [-AsJob]
 [-Offer <String>] [-Sku <String>] [-SqlManagementType <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37446-106">NameInputObject</span><span class="sxs-lookup"><span data-stu-id="37446-106">NameInputObject</span></span>
```
New-AzSqlVM [-ResourceGroupName] <String> [-Name] <String> [-SqlVM] <AzureSqlVMModel> -Location <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37446-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="37446-107">DESCRIPTION</span></span>
<span data-ttu-id="37446-108">Командлет New-AzSqlVM создает виртуальную машину Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="37446-108">The New-AzSqlVM cmdlet creates an Azure SQL virtual machine.</span></span>

## <span data-ttu-id="37446-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="37446-109">EXAMPLES</span></span>

### <span data-ttu-id="37446-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="37446-110">Example 1</span></span>
```powershell
PS C:\> New-AzSqlVM  New-AzSqlVM -ResourceGroupName ResourceGroup01 -Name vm -LicenseType 'PAYG' -Sku Developer
Name ResourceGroupName  LicenseType Sku       Offer          SqlManagementType
---- -----------------  ----------- ---       -----          -----------------
vm   ResourceGroup01    PAYG        Developer SQL2017-WS2016 Full
```

<span data-ttu-id="37446-111">Создание новой виртуальной машины Azure SQL с именем VM в группе ресурсов ResourceGroup01</span><span class="sxs-lookup"><span data-stu-id="37446-111">Creates a new Azure SQL virtual machine with name vm in the resource group ResourceGroup01</span></span> 

## <span data-ttu-id="37446-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="37446-112">PARAMETERS</span></span>

### <span data-ttu-id="37446-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="37446-113">-AsJob</span></span>
<span data-ttu-id="37446-114">Запустите командлет в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="37446-114">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="37446-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37446-115">-DefaultProfile</span></span>
<span data-ttu-id="37446-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="37446-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37446-117">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="37446-117">-LicenseType</span></span>
<span data-ttu-id="37446-118">Тип лицензии виртуальной машины SQL.</span><span class="sxs-lookup"><span data-stu-id="37446-118">SQL virtual machine license type.</span></span>

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

### <span data-ttu-id="37446-119">-Location</span><span class="sxs-lookup"><span data-stu-id="37446-119">-Location</span></span>
<span data-ttu-id="37446-120">Расположение виртуальной машины SQL.</span><span class="sxs-lookup"><span data-stu-id="37446-120">SQL virtual machine location.</span></span>

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

### <span data-ttu-id="37446-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="37446-121">-Name</span></span>
<span data-ttu-id="37446-122">Имя виртуальной машины SQL.</span><span class="sxs-lookup"><span data-stu-id="37446-122">SQL virtual machine name.</span></span>

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

### <span data-ttu-id="37446-123">-Предложение</span><span class="sxs-lookup"><span data-stu-id="37446-123">-Offer</span></span>
<span data-ttu-id="37446-124">Предложение виртуальной машины SQL.</span><span class="sxs-lookup"><span data-stu-id="37446-124">SQL virtual machine offer.</span></span>

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

### <span data-ttu-id="37446-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37446-125">-ResourceGroupName</span></span>
<span data-ttu-id="37446-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="37446-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="37446-127">-SKU</span><span class="sxs-lookup"><span data-stu-id="37446-127">-Sku</span></span>
<span data-ttu-id="37446-128">Тип выпусков виртуальной машины SQL.</span><span class="sxs-lookup"><span data-stu-id="37446-128">SQL virtual machine edition type.</span></span>

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

### <span data-ttu-id="37446-129">-SqlManagementType</span><span class="sxs-lookup"><span data-stu-id="37446-129">-SqlManagementType</span></span>
<span data-ttu-id="37446-130">Тип управления виртуальными машинами SQL.</span><span class="sxs-lookup"><span data-stu-id="37446-130">SQL virtual machine management type.</span></span>

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

### <span data-ttu-id="37446-131">-SqlVM</span><span class="sxs-lookup"><span data-stu-id="37446-131">-SqlVM</span></span>
<span data-ttu-id="37446-132">Объект виртуальной машины SQL.</span><span class="sxs-lookup"><span data-stu-id="37446-132">SQL virtual machine object.</span></span>

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

### <span data-ttu-id="37446-133">-Тег</span><span class="sxs-lookup"><span data-stu-id="37446-133">-Tag</span></span>
<span data-ttu-id="37446-134">Теги, связываемые с виртуальной машиной SQL</span><span class="sxs-lookup"><span data-stu-id="37446-134">The tags to associate with the SQL virtual machine</span></span>

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

### <span data-ttu-id="37446-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="37446-135">-Confirm</span></span>
<span data-ttu-id="37446-136">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="37446-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37446-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37446-137">-WhatIf</span></span>
<span data-ttu-id="37446-138">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="37446-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37446-139">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="37446-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37446-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37446-140">CommonParameters</span></span>
<span data-ttu-id="37446-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="37446-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37446-142">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="37446-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37446-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="37446-143">INPUTS</span></span>

### <span data-ttu-id="37446-144">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="37446-144">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="37446-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="37446-145">OUTPUTS</span></span>

### <span data-ttu-id="37446-146">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="37446-146">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="37446-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="37446-147">NOTES</span></span>

## <span data-ttu-id="37446-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="37446-148">RELATED LINKS</span></span>
