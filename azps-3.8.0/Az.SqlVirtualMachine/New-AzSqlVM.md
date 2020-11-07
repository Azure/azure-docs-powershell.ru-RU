---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/new-azsqlvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVM.md
ms.openlocfilehash: 764312c64ae9887a6ef4243cc20b04535afcf81f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93912460"
---
# <span data-ttu-id="7a2b2-101">New-AzSqlVM</span><span class="sxs-lookup"><span data-stu-id="7a2b2-101">New-AzSqlVM</span></span>

## <span data-ttu-id="7a2b2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7a2b2-102">SYNOPSIS</span></span>
<span data-ttu-id="7a2b2-103">Создание новой виртуальной машины SQL.</span><span class="sxs-lookup"><span data-stu-id="7a2b2-103">Creates a new sql virtual machine.</span></span>

## <span data-ttu-id="7a2b2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7a2b2-104">SYNTAX</span></span>

### <span data-ttu-id="7a2b2-105">NameParamaterList (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7a2b2-105">NameParamaterList (Default)</span></span>
```
New-AzSqlVM [-ResourceGroupName] <String> [-Name] <String> [-LicenseType] <String> -Location <String> [-AsJob]
 [-Offer <String>] [-Sku <String>] [-SqlManagementType <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a2b2-106">NameInputObject</span><span class="sxs-lookup"><span data-stu-id="7a2b2-106">NameInputObject</span></span>
```
New-AzSqlVM [-ResourceGroupName] <String> [-Name] <String> [-SqlVM] <AzureSqlVMModel> -Location <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a2b2-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7a2b2-107">DESCRIPTION</span></span>
<span data-ttu-id="7a2b2-108">Командлет New-AzSqlVM создает виртуальную машину Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="7a2b2-108">The New-AzSqlVM cmdlet creates an Azure SQL virtual machine.</span></span>

## <span data-ttu-id="7a2b2-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7a2b2-109">EXAMPLES</span></span>

### <span data-ttu-id="7a2b2-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7a2b2-110">Example 1</span></span>
```powershell
PS C:\> New-AzSqlVM  New-AzSqlVM -ResourceGroupName ResourceGroup01 -Name vm -LicenseType 'PAYG' -Sku Developer
Name ResourceGroupName  LicenseType Sku       Offer          SqlManagementType
---- -----------------  ----------- ---       -----          -----------------
vm   ResourceGroup01    PAYG        Developer SQL2017-WS2016 Full
```

<span data-ttu-id="7a2b2-111">Создание новой виртуальной машины Azure SQL с именем VM в группе ресурсов ResourceGroup01</span><span class="sxs-lookup"><span data-stu-id="7a2b2-111">Creates a new Azure SQL virtual machine with name vm in the resource group ResourceGroup01</span></span> 

## <span data-ttu-id="7a2b2-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7a2b2-112">PARAMETERS</span></span>

### <span data-ttu-id="7a2b2-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7a2b2-113">-AsJob</span></span>
<span data-ttu-id="7a2b2-114">Запустите командлет в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="7a2b2-114">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="7a2b2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a2b2-115">-DefaultProfile</span></span>
<span data-ttu-id="7a2b2-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7a2b2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a2b2-117">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="7a2b2-117">-LicenseType</span></span>
<span data-ttu-id="7a2b2-118">Тип лицензии виртуальной машины SQL.</span><span class="sxs-lookup"><span data-stu-id="7a2b2-118">SQL virtual machine license type.</span></span>

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

### <span data-ttu-id="7a2b2-119">-Location</span><span class="sxs-lookup"><span data-stu-id="7a2b2-119">-Location</span></span>
<span data-ttu-id="7a2b2-120">Расположение виртуальной машины SQL.</span><span class="sxs-lookup"><span data-stu-id="7a2b2-120">SQL virtual machine location.</span></span>

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

### <span data-ttu-id="7a2b2-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7a2b2-121">-Name</span></span>
<span data-ttu-id="7a2b2-122">Имя виртуальной машины SQL.</span><span class="sxs-lookup"><span data-stu-id="7a2b2-122">SQL virtual machine name.</span></span>

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

### <span data-ttu-id="7a2b2-123">-Предложение</span><span class="sxs-lookup"><span data-stu-id="7a2b2-123">-Offer</span></span>
<span data-ttu-id="7a2b2-124">Предложение виртуальной машины SQL.</span><span class="sxs-lookup"><span data-stu-id="7a2b2-124">SQL virtual machine offer.</span></span>

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

### <span data-ttu-id="7a2b2-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a2b2-125">-ResourceGroupName</span></span>
<span data-ttu-id="7a2b2-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7a2b2-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="7a2b2-127">-SKU</span><span class="sxs-lookup"><span data-stu-id="7a2b2-127">-Sku</span></span>
<span data-ttu-id="7a2b2-128">Тип выпусков виртуальной машины SQL.</span><span class="sxs-lookup"><span data-stu-id="7a2b2-128">SQL virtual machine edition type.</span></span>

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

### <span data-ttu-id="7a2b2-129">-SqlManagementType</span><span class="sxs-lookup"><span data-stu-id="7a2b2-129">-SqlManagementType</span></span>
<span data-ttu-id="7a2b2-130">Тип управления виртуальными машинами SQL.</span><span class="sxs-lookup"><span data-stu-id="7a2b2-130">SQL virtual machine management type.</span></span>

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

### <span data-ttu-id="7a2b2-131">-SqlVM</span><span class="sxs-lookup"><span data-stu-id="7a2b2-131">-SqlVM</span></span>
<span data-ttu-id="7a2b2-132">Объект виртуальной машины SQL.</span><span class="sxs-lookup"><span data-stu-id="7a2b2-132">SQL virtual machine object.</span></span>

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

### <span data-ttu-id="7a2b2-133">-Тег</span><span class="sxs-lookup"><span data-stu-id="7a2b2-133">-Tag</span></span>
<span data-ttu-id="7a2b2-134">Теги, связываемые с виртуальной машиной SQL</span><span class="sxs-lookup"><span data-stu-id="7a2b2-134">The tags to associate with the SQL virtual machine</span></span>

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

### <span data-ttu-id="7a2b2-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7a2b2-135">-Confirm</span></span>
<span data-ttu-id="7a2b2-136">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7a2b2-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a2b2-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a2b2-137">-WhatIf</span></span>
<span data-ttu-id="7a2b2-138">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7a2b2-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a2b2-139">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7a2b2-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a2b2-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a2b2-140">CommonParameters</span></span>
<span data-ttu-id="7a2b2-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7a2b2-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a2b2-142">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7a2b2-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a2b2-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7a2b2-143">INPUTS</span></span>

### <span data-ttu-id="7a2b2-144">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="7a2b2-144">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="7a2b2-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7a2b2-145">OUTPUTS</span></span>

### <span data-ttu-id="7a2b2-146">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="7a2b2-146">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="7a2b2-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="7a2b2-147">NOTES</span></span>

## <span data-ttu-id="7a2b2-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7a2b2-148">RELATED LINKS</span></span>
