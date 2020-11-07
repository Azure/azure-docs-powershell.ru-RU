---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/update-azsqlvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Update-AzSqlVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Update-AzSqlVM.md
ms.openlocfilehash: bfc64aeb344e9913bf72ae7b51559bb613209994
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93906821"
---
# <span data-ttu-id="55e1a-101">Update-AzSqlVM</span><span class="sxs-lookup"><span data-stu-id="55e1a-101">Update-AzSqlVM</span></span>

## <span data-ttu-id="55e1a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="55e1a-102">SYNOPSIS</span></span>
<span data-ttu-id="55e1a-103">Обновляет виртуальную машину SQL.</span><span class="sxs-lookup"><span data-stu-id="55e1a-103">Updates a sql virtual machine.</span></span>

## <span data-ttu-id="55e1a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="55e1a-104">SYNTAX</span></span>

### <span data-ttu-id="55e1a-105">NameParamaterList (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="55e1a-105">NameParamaterList (Default)</span></span>
```
Update-AzSqlVM [-ResourceGroupName] <String> [-Name] <String> [-LicenseType <String>] [-Offer <String>]
 [-Sku <String>] [-SqlManagementType <String>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55e1a-106">NameInputObject</span><span class="sxs-lookup"><span data-stu-id="55e1a-106">NameInputObject</span></span>
```
Update-AzSqlVM [-ResourceGroupName] <String> [-Name] <String> [-InputObject] <AzureSqlVMModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55e1a-107">ResourceIdParamaterList</span><span class="sxs-lookup"><span data-stu-id="55e1a-107">ResourceIdParamaterList</span></span>
```
Update-AzSqlVM [-LicenseType <String>] [-Offer <String>] [-Sku <String>] [-SqlManagementType <String>]
 [-Tag <Hashtable>] [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55e1a-108">ResourceIdInputObject</span><span class="sxs-lookup"><span data-stu-id="55e1a-108">ResourceIdInputObject</span></span>
```
Update-AzSqlVM [-InputObject] <AzureSqlVMModel> [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55e1a-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="55e1a-109">DESCRIPTION</span></span>
<span data-ttu-id="55e1a-110">Командлет Update-AzSqlVM обновляет виртуальную машину SQL.</span><span class="sxs-lookup"><span data-stu-id="55e1a-110">The Update-AzSqlVM cmdlet updates a sql virtual machine.</span></span>

## <span data-ttu-id="55e1a-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="55e1a-111">EXAMPLES</span></span>

### <span data-ttu-id="55e1a-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="55e1a-112">Example 1</span></span>
```powershell
PS C:\> $tags = @{'key'='value'}
PS C:\> $vm = Update-AzSqlVM -InputObject $vm -Tags $tags
PS C:\> $group.Tags
Name                           Value
----                           -----
key                            value
```

<span data-ttu-id="55e1a-113">Обновляет Теги виртуальной машины SQL.</span><span class="sxs-lookup"><span data-stu-id="55e1a-113">Updates the tags of a sql virtual machine.</span></span>

## <span data-ttu-id="55e1a-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="55e1a-114">PARAMETERS</span></span>

### <span data-ttu-id="55e1a-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="55e1a-115">-AsJob</span></span>
<span data-ttu-id="55e1a-116">Запустите командлет в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="55e1a-116">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="55e1a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55e1a-117">-DefaultProfile</span></span>
<span data-ttu-id="55e1a-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="55e1a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="55e1a-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="55e1a-119">-InputObject</span></span>
<span data-ttu-id="55e1a-120">Объект виртуальной машины SQL.</span><span class="sxs-lookup"><span data-stu-id="55e1a-120">SQL virtual machine object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel
Parameter Sets: NameInputObject, ResourceIdInputObject
Aliases: SqlVM

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="55e1a-121">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="55e1a-121">-LicenseType</span></span>
<span data-ttu-id="55e1a-122">Тип лицензии виртуальной машины SQL.</span><span class="sxs-lookup"><span data-stu-id="55e1a-122">SQL virtual machine license type.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParamaterList, ResourceIdParamaterList
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55e1a-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="55e1a-123">-Name</span></span>
<span data-ttu-id="55e1a-124">Имя виртуальной машины SQL.</span><span class="sxs-lookup"><span data-stu-id="55e1a-124">SQL virtual machine name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParamaterList, NameInputObject
Aliases: SqlVMName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55e1a-125">-Предложение</span><span class="sxs-lookup"><span data-stu-id="55e1a-125">-Offer</span></span>
<span data-ttu-id="55e1a-126">Предложение виртуальной машины SQL.</span><span class="sxs-lookup"><span data-stu-id="55e1a-126">SQL virtual machine offer.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParamaterList, ResourceIdParamaterList
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55e1a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55e1a-127">-ResourceGroupName</span></span>
<span data-ttu-id="55e1a-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="55e1a-128">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParamaterList, NameInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55e1a-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="55e1a-129">-ResourceId</span></span>
<span data-ttu-id="55e1a-130">Идентификатор ресурса виртуальной машины SQL.</span><span class="sxs-lookup"><span data-stu-id="55e1a-130">SQL virtual machine resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParamaterList, ResourceIdInputObject
Aliases: SqlVMId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55e1a-131">-SKU</span><span class="sxs-lookup"><span data-stu-id="55e1a-131">-Sku</span></span>
<span data-ttu-id="55e1a-132">Тип выпусков виртуальной машины SQL.</span><span class="sxs-lookup"><span data-stu-id="55e1a-132">SQL virtual machine edition type.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParamaterList, ResourceIdParamaterList
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55e1a-133">-SqlManagementType</span><span class="sxs-lookup"><span data-stu-id="55e1a-133">-SqlManagementType</span></span>
<span data-ttu-id="55e1a-134">Тип управления виртуальными машинами SQL.</span><span class="sxs-lookup"><span data-stu-id="55e1a-134">SQL virtual machine management type.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParamaterList, ResourceIdParamaterList
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55e1a-135">-Тег</span><span class="sxs-lookup"><span data-stu-id="55e1a-135">-Tag</span></span>
<span data-ttu-id="55e1a-136">Теги, связываемые с виртуальной машиной SQL</span><span class="sxs-lookup"><span data-stu-id="55e1a-136">The tags to associate with the SQL virtual machine</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: NameParamaterList, ResourceIdParamaterList
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55e1a-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="55e1a-137">-Confirm</span></span>
<span data-ttu-id="55e1a-138">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="55e1a-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55e1a-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55e1a-139">-WhatIf</span></span>
<span data-ttu-id="55e1a-140">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="55e1a-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55e1a-141">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="55e1a-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55e1a-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55e1a-142">CommonParameters</span></span>
<span data-ttu-id="55e1a-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="55e1a-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55e1a-144">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="55e1a-144">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55e1a-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="55e1a-145">INPUTS</span></span>

### <span data-ttu-id="55e1a-146">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="55e1a-146">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="55e1a-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="55e1a-147">OUTPUTS</span></span>

### <span data-ttu-id="55e1a-148">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="55e1a-148">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="55e1a-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="55e1a-149">NOTES</span></span>

## <span data-ttu-id="55e1a-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="55e1a-150">RELATED LINKS</span></span>
