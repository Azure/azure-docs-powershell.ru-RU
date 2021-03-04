---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBox.dll-Help.xml
Module Name: Az.DataBox
online version: https://docs.microsoft.com/powershell/module/az.databox/new-azdataboxjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/New-AzDataBoxJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/New-AzDataBoxJob.md
ms.openlocfilehash: 2c78f8b40621ba58b84169f2bd9022399fce80b7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101998679"
---
# <span data-ttu-id="d167b-101">New-AzDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="d167b-101">New-AzDataBoxJob</span></span>

## <span data-ttu-id="d167b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d167b-102">SYNOPSIS</span></span>
<span data-ttu-id="d167b-103">Создание задания для почтового ящика с использованием указанных параметров</span><span class="sxs-lookup"><span data-stu-id="d167b-103">Creates a new databox job using the specified parameters</span></span>

## <span data-ttu-id="d167b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d167b-104">SYNTAX</span></span>

```
New-AzDataBoxJob -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 -Location <String> [-AddressType <AddressType>] [-CompanyName <String>] -StreetAddress1 <String>
 [-StreetAddress2 <String>] [-StreetAddress3 <String>] -PostalCode <String> -City <String>
 -StateOrProvinceCode <String> -CountryCode <String> -EmailId <String[]> -PhoneNumber <String>
 -ContactName <String> -StorageAccountResourceId <String[]> -DataBoxType <String>
 [-ExpectedDataSizeInTeraBytes <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d167b-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d167b-105">DESCRIPTION</span></span>
<span data-ttu-id="d167b-106">Для создания нового задания в почтовом ящике используется cmdlet **New-AzDataBoxJob,** указав сведения, необходимые для его создания.</span><span class="sxs-lookup"><span data-stu-id="d167b-106">The **New-AzDataBoxJob** cmdlet is used to create a new databox job by specifying the details required for the creation of the job.</span></span>

## <span data-ttu-id="d167b-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d167b-107">EXAMPLES</span></span>

### <span data-ttu-id="d167b-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d167b-108">Example 1</span></span>
```powershell
PS C:\> $s1 = <Storage Account Resource Id>
PS C:\> New-AzDataBoxJob -Location 'WestUS' -StreetAddress1 '16 TOWNSEND ST' -PostalCode 94107 -City 'San Francisco' -StateOrProvinceCode 'CA' -CountryCode 'US' -EmailId 'abc@outlook.com' -PhoneNumber 1234567891 -ContactName 'John' -StorageAccount $s1 -DataBoxType DataBox -ResourceGroupName TestRg -Name OrderTest

jobResource.Name jobResource.Sku.Name jobResource.Status jobResource.StartTime jobResource.Location ResourceGroup
---------------- -------------------- ------------------ --------------------- -------------------- -------------
OrderTest       DataBox              DeviceOrdered      05-07-2019 05:25:30   westus               TestRg
```

<span data-ttu-id="d167b-109">Для создания задания обработки данных с помощью cmdlet будут заданы все необходимые параметры и некоторые необязательные параметры.</span><span class="sxs-lookup"><span data-stu-id="d167b-109">The cmdlet takes all the required parameters and some optional parameters to create the databox job.</span></span>

## <span data-ttu-id="d167b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d167b-110">PARAMETERS</span></span>

### <span data-ttu-id="d167b-111">-AddressType</span><span class="sxs-lookup"><span data-stu-id="d167b-111">-AddressType</span></span>
<span data-ttu-id="d167b-112">Тип адреса.</span><span class="sxs-lookup"><span data-stu-id="d167b-112">Type of Address.</span></span> <span data-ttu-id="d167b-113">Доступные значения: AddressType.None (по умолчанию), AddressType.Веха, AddressType.Commercial</span><span class="sxs-lookup"><span data-stu-id="d167b-113">Available values : AddressType.None (default), AddressType.Residential, AddressType.Commercial</span></span>

```yaml
Type: Microsoft.Azure.Management.DataBox.Models.AddressType
Parameter Sets: (All)
Aliases:
Accepted values: None, Residential, Commercial

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d167b-114">-Город</span><span class="sxs-lookup"><span data-stu-id="d167b-114">-City</span></span>
<span data-ttu-id="d167b-115">Название города.</span><span class="sxs-lookup"><span data-stu-id="d167b-115">Name of the City.</span></span> <span data-ttu-id="d167b-116">Ex : San Francisco</span><span class="sxs-lookup"><span data-stu-id="d167b-116">Ex : San Francisco</span></span>

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

### <span data-ttu-id="d167b-117">-CompanyName</span><span class="sxs-lookup"><span data-stu-id="d167b-117">-CompanyName</span></span>
<span data-ttu-id="d167b-118">Название компании</span><span class="sxs-lookup"><span data-stu-id="d167b-118">Name of the company</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d167b-119">-ContactName</span><span class="sxs-lookup"><span data-stu-id="d167b-119">-ContactName</span></span>
<span data-ttu-id="d167b-120">Имя контакта</span><span class="sxs-lookup"><span data-stu-id="d167b-120">Contact Name</span></span>

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

### <span data-ttu-id="d167b-121">-CountryCode</span><span class="sxs-lookup"><span data-stu-id="d167b-121">-CountryCode</span></span>
<span data-ttu-id="d167b-122">Код страны.</span><span class="sxs-lookup"><span data-stu-id="d167b-122">Country Code.</span></span> <span data-ttu-id="d167b-123">Ex: US</span><span class="sxs-lookup"><span data-stu-id="d167b-123">Ex: US</span></span>

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

### <span data-ttu-id="d167b-124">-DataBoxType</span><span class="sxs-lookup"><span data-stu-id="d167b-124">-DataBoxType</span></span>
<span data-ttu-id="d167b-125">Тип данных "SKU".</span><span class="sxs-lookup"><span data-stu-id="d167b-125">Sku type of Databox.</span></span>  <span data-ttu-id="d167b-126">Доступные значения: DataBoxDisk, Databox, DataBoxHeavy</span><span class="sxs-lookup"><span data-stu-id="d167b-126">Available values : DataBoxDisk, Databox, DataBoxHeavy</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: DataBoxDisk, Databox, DataBoxHeavy

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d167b-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d167b-127">-DefaultProfile</span></span>
<span data-ttu-id="d167b-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d167b-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d167b-129">-EmailId</span><span class="sxs-lookup"><span data-stu-id="d167b-129">-EmailId</span></span>
<span data-ttu-id="d167b-130">Вы можете получить список emailIds.</span><span class="sxs-lookup"><span data-stu-id="d167b-130">List of EmailIds can be provided.</span></span> <span data-ttu-id="d167b-131">Atleast one является обязательным</span><span class="sxs-lookup"><span data-stu-id="d167b-131">Atleast one is mandatory</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d167b-132">-ExpectedDataSizeInTeraBytes</span><span class="sxs-lookup"><span data-stu-id="d167b-132">-ExpectedDataSizeInTeraBytes</span></span>
<span data-ttu-id="d167b-133">Для заказа DataBoxDisk нужно указать ожидаемые данные в терабайтах.</span><span class="sxs-lookup"><span data-stu-id="d167b-133">For DataBoxDisk order, specifying the expected data in terabytes is mandatory.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d167b-134">-Location</span><span class="sxs-lookup"><span data-stu-id="d167b-134">-Location</span></span>
<span data-ttu-id="d167b-135">Расположение подписки</span><span class="sxs-lookup"><span data-stu-id="d167b-135">Location of the subscription</span></span>

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

### <span data-ttu-id="d167b-136">-Name</span><span class="sxs-lookup"><span data-stu-id="d167b-136">-Name</span></span>
<span data-ttu-id="d167b-137">Имя создаемого задания для создания почтового ящика</span><span class="sxs-lookup"><span data-stu-id="d167b-137">Name of the databox job to be created</span></span>

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

### <span data-ttu-id="d167b-138">-PhoneNumber</span><span class="sxs-lookup"><span data-stu-id="d167b-138">-PhoneNumber</span></span>
<span data-ttu-id="d167b-139">Номер контакта</span><span class="sxs-lookup"><span data-stu-id="d167b-139">Contact Number</span></span> 

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

### <span data-ttu-id="d167b-140">-PostalCode</span><span class="sxs-lookup"><span data-stu-id="d167b-140">-PostalCode</span></span>
<span data-ttu-id="d167b-141">Почтовый индекс</span><span class="sxs-lookup"><span data-stu-id="d167b-141">Postal Code</span></span>

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

### <span data-ttu-id="d167b-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d167b-142">-ResourceGroupName</span></span>
<span data-ttu-id="d167b-143">Имя группы ресурсов, под которой должно быть создано задание для создания почтового ящика.</span><span class="sxs-lookup"><span data-stu-id="d167b-143">Resource Group Name under which the databox job has to be created.</span></span>

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

### <span data-ttu-id="d167b-144">-StateOrProvinceCode</span><span class="sxs-lookup"><span data-stu-id="d167b-144">-StateOrProvinceCode</span></span>
<span data-ttu-id="d167b-145">Ввести код области или провинции.</span><span class="sxs-lookup"><span data-stu-id="d167b-145">Input the state or province code.</span></span> <span data-ttu-id="d167b-146">Like CA - California; Fl - Fl - Fl; NY - New York</span><span class="sxs-lookup"><span data-stu-id="d167b-146">Like CA - California; FL - Florida; NY - New York</span></span>

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

### <span data-ttu-id="d167b-147">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="d167b-147">-StorageAccountResourceId</span></span>
<span data-ttu-id="d167b-148">Список ИД ресурсов для учетных записей хранения.</span><span class="sxs-lookup"><span data-stu-id="d167b-148">List of Resource Ids of Storage Accounts.</span></span> <span data-ttu-id="d167b-149">Atleast one является обязательным.</span><span class="sxs-lookup"><span data-stu-id="d167b-149">Atleast one is mandatory.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d167b-150">-StreetAddress1</span><span class="sxs-lookup"><span data-stu-id="d167b-150">-StreetAddress1</span></span>
<span data-ttu-id="d167b-151">Адрес</span><span class="sxs-lookup"><span data-stu-id="d167b-151">Street Address</span></span>

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

### <span data-ttu-id="d167b-152">-StreetAddress2</span><span class="sxs-lookup"><span data-stu-id="d167b-152">-StreetAddress2</span></span>
<span data-ttu-id="d167b-153">Дополнительный адрес</span><span class="sxs-lookup"><span data-stu-id="d167b-153">Additional Street Address</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d167b-154">-StreetAddress3</span><span class="sxs-lookup"><span data-stu-id="d167b-154">-StreetAddress3</span></span>
<span data-ttu-id="d167b-155">Дополнительный адрес</span><span class="sxs-lookup"><span data-stu-id="d167b-155">Additional Street Address</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d167b-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d167b-156">-Confirm</span></span>
<span data-ttu-id="d167b-157">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d167b-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d167b-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d167b-158">-WhatIf</span></span>
<span data-ttu-id="d167b-159">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d167b-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d167b-160">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="d167b-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d167b-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d167b-161">CommonParameters</span></span>
<span data-ttu-id="d167b-162">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d167b-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d167b-163">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d167b-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d167b-164">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d167b-164">INPUTS</span></span>

### <span data-ttu-id="d167b-165">System.String[]</span><span class="sxs-lookup"><span data-stu-id="d167b-165">System.String[]</span></span>

## <span data-ttu-id="d167b-166">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d167b-166">OUTPUTS</span></span>

### <span data-ttu-id="d167b-167">Microsoft.Azure.PowerShell.Cmdlets.DataBox.Models.PSDAtaBoxJob</span><span class="sxs-lookup"><span data-stu-id="d167b-167">Microsoft.Azure.PowerShell.Cmdlets.DataBox.Models.PSDataBoxJob</span></span>

## <span data-ttu-id="d167b-168">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d167b-168">NOTES</span></span>

## <span data-ttu-id="d167b-169">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d167b-169">RELATED LINKS</span></span>
