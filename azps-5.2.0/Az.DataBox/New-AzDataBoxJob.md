---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBox.dll-Help.xml
Module Name: Az.DataBox
online version: https://docs.microsoft.com/en-us/powershell/module/az.databox/new-azdataboxjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/New-AzDataBoxJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/New-AzDataBoxJob.md
ms.openlocfilehash: 4402eaed4b76ce6e769141748b043598bdfd099a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98406383"
---
# <span data-ttu-id="c3b28-101">New-AzDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="c3b28-101">New-AzDataBoxJob</span></span>

## <span data-ttu-id="c3b28-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c3b28-102">SYNOPSIS</span></span>
<span data-ttu-id="c3b28-103">Создание задания создания почтового ящика с использованием указанных параметров</span><span class="sxs-lookup"><span data-stu-id="c3b28-103">Creates a new databox job using the specified parameters</span></span>

## <span data-ttu-id="c3b28-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c3b28-104">SYNTAX</span></span>

```
New-AzDataBoxJob -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 -Location <String> [-AddressType <AddressType>] [-CompanyName <String>] -StreetAddress1 <String>
 [-StreetAddress2 <String>] [-StreetAddress3 <String>] -PostalCode <String> -City <String>
 -StateOrProvinceCode <String> -CountryCode <String> -EmailId <String[]> -PhoneNumber <String>
 -ContactName <String> -StorageAccountResourceId <String[]> -DataBoxType <String>
 [-ExpectedDataSizeInTeraBytes <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3b28-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c3b28-105">DESCRIPTION</span></span>
<span data-ttu-id="c3b28-106">Для создания нового задания в почтовом ящике используется cmdlet **New-AzDataBoxJob,** указав сведения, необходимые для его создания.</span><span class="sxs-lookup"><span data-stu-id="c3b28-106">The **New-AzDataBoxJob** cmdlet is used to create a new databox job by specifying the details required for the creation of the job.</span></span>

## <span data-ttu-id="c3b28-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c3b28-107">EXAMPLES</span></span>

### <span data-ttu-id="c3b28-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c3b28-108">Example 1</span></span>
```powershell
PS C:\> $s1 = <Storage Account Resource Id>
PS C:\> New-AzDataBoxJob -Location 'WestUS' -StreetAddress1 '16 TOWNSEND ST' -PostalCode 94107 -City 'San Francisco' -StateOrProvinceCode 'CA' -CountryCode 'US' -EmailId 'abc@outlook.com' -PhoneNumber 1234567891 -ContactName 'John' -StorageAccount $s1 -DataBoxType DataBox -ResourceGroupName TestRg -Name OrderTest

jobResource.Name jobResource.Sku.Name jobResource.Status jobResource.StartTime jobResource.Location ResourceGroup
---------------- -------------------- ------------------ --------------------- -------------------- -------------
OrderTest       DataBox              DeviceOrdered      05-07-2019 05:25:30   westus               TestRg
```

<span data-ttu-id="c3b28-109">Для создания задания обработки данных с помощью cmdlet будут заданы все необходимые параметры и некоторые необязательные параметры.</span><span class="sxs-lookup"><span data-stu-id="c3b28-109">The cmdlet takes all the required parameters and some optional parameters to create the databox job.</span></span>

## <span data-ttu-id="c3b28-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c3b28-110">PARAMETERS</span></span>

### <span data-ttu-id="c3b28-111">-AddressType</span><span class="sxs-lookup"><span data-stu-id="c3b28-111">-AddressType</span></span>
<span data-ttu-id="c3b28-112">Тип адреса.</span><span class="sxs-lookup"><span data-stu-id="c3b28-112">Type of Address.</span></span> <span data-ttu-id="c3b28-113">Доступные значения: AddressType.None (по умолчанию), AddressType.Веха, AddressType.Commercial</span><span class="sxs-lookup"><span data-stu-id="c3b28-113">Available values : AddressType.None (default), AddressType.Residential, AddressType.Commercial</span></span>

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

### <span data-ttu-id="c3b28-114">-Город</span><span class="sxs-lookup"><span data-stu-id="c3b28-114">-City</span></span>
<span data-ttu-id="c3b28-115">Название города.</span><span class="sxs-lookup"><span data-stu-id="c3b28-115">Name of the City.</span></span> <span data-ttu-id="c3b28-116">Ex : San Francisco</span><span class="sxs-lookup"><span data-stu-id="c3b28-116">Ex : San Francisco</span></span>

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

### <span data-ttu-id="c3b28-117">-CompanyName</span><span class="sxs-lookup"><span data-stu-id="c3b28-117">-CompanyName</span></span>
<span data-ttu-id="c3b28-118">Название компании</span><span class="sxs-lookup"><span data-stu-id="c3b28-118">Name of the company</span></span>

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

### <span data-ttu-id="c3b28-119">-ContactName</span><span class="sxs-lookup"><span data-stu-id="c3b28-119">-ContactName</span></span>
<span data-ttu-id="c3b28-120">Имя контакта</span><span class="sxs-lookup"><span data-stu-id="c3b28-120">Contact Name</span></span>

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

### <span data-ttu-id="c3b28-121">-CountryCode</span><span class="sxs-lookup"><span data-stu-id="c3b28-121">-CountryCode</span></span>
<span data-ttu-id="c3b28-122">Код страны.</span><span class="sxs-lookup"><span data-stu-id="c3b28-122">Country Code.</span></span> <span data-ttu-id="c3b28-123">Ex: US</span><span class="sxs-lookup"><span data-stu-id="c3b28-123">Ex: US</span></span>

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

### <span data-ttu-id="c3b28-124">-DataBoxType</span><span class="sxs-lookup"><span data-stu-id="c3b28-124">-DataBoxType</span></span>
<span data-ttu-id="c3b28-125">Тип данных SKU.</span><span class="sxs-lookup"><span data-stu-id="c3b28-125">Sku type of Databox.</span></span>  <span data-ttu-id="c3b28-126">Доступные значения: DataBoxDisk, Databox, DataBoxHeavy</span><span class="sxs-lookup"><span data-stu-id="c3b28-126">Available values : DataBoxDisk, Databox, DataBoxHeavy</span></span>

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

### <span data-ttu-id="c3b28-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3b28-127">-DefaultProfile</span></span>
<span data-ttu-id="c3b28-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c3b28-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3b28-129">-EmailId</span><span class="sxs-lookup"><span data-stu-id="c3b28-129">-EmailId</span></span>
<span data-ttu-id="c3b28-130">Вы можете получить список emailIds.</span><span class="sxs-lookup"><span data-stu-id="c3b28-130">List of EmailIds can be provided.</span></span> <span data-ttu-id="c3b28-131">Atleast one является обязательным</span><span class="sxs-lookup"><span data-stu-id="c3b28-131">Atleast one is mandatory</span></span>

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

### <span data-ttu-id="c3b28-132">-ExpectedDataSizeInTeraBytes</span><span class="sxs-lookup"><span data-stu-id="c3b28-132">-ExpectedDataSizeInTeraBytes</span></span>
<span data-ttu-id="c3b28-133">Для заказа DataBoxDisk нужно указать ожидаемые данные в терабайтах.</span><span class="sxs-lookup"><span data-stu-id="c3b28-133">For DataBoxDisk order, specifying the expected data in terabytes is mandatory.</span></span>

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

### <span data-ttu-id="c3b28-134">-Location</span><span class="sxs-lookup"><span data-stu-id="c3b28-134">-Location</span></span>
<span data-ttu-id="c3b28-135">Расположение подписки</span><span class="sxs-lookup"><span data-stu-id="c3b28-135">Location of the subscription</span></span>

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

### <span data-ttu-id="c3b28-136">-Name</span><span class="sxs-lookup"><span data-stu-id="c3b28-136">-Name</span></span>
<span data-ttu-id="c3b28-137">Имя созда создаемого задания создания почтового ящика</span><span class="sxs-lookup"><span data-stu-id="c3b28-137">Name of the databox job to be created</span></span>

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

### <span data-ttu-id="c3b28-138">-PhoneNumber</span><span class="sxs-lookup"><span data-stu-id="c3b28-138">-PhoneNumber</span></span>
<span data-ttu-id="c3b28-139">Номер контакта</span><span class="sxs-lookup"><span data-stu-id="c3b28-139">Contact Number</span></span> 

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

### <span data-ttu-id="c3b28-140">-PostalCode</span><span class="sxs-lookup"><span data-stu-id="c3b28-140">-PostalCode</span></span>
<span data-ttu-id="c3b28-141">Почтовый индекс</span><span class="sxs-lookup"><span data-stu-id="c3b28-141">Postal Code</span></span>

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

### <span data-ttu-id="c3b28-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3b28-142">-ResourceGroupName</span></span>
<span data-ttu-id="c3b28-143">Имя группы ресурсов, под которой должно быть создано задание для создания почтового ящика.</span><span class="sxs-lookup"><span data-stu-id="c3b28-143">Resource Group Name under which the databox job has to be created.</span></span>

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

### <span data-ttu-id="c3b28-144">-StateOrProvinceCode</span><span class="sxs-lookup"><span data-stu-id="c3b28-144">-StateOrProvinceCode</span></span>
<span data-ttu-id="c3b28-145">Ввести код области или провинции.</span><span class="sxs-lookup"><span data-stu-id="c3b28-145">Input the state or province code.</span></span> <span data-ttu-id="c3b28-146">Like CA - California; Fl - Fl - Fl; NY - New York</span><span class="sxs-lookup"><span data-stu-id="c3b28-146">Like CA - California; FL - Florida; NY - New York</span></span>

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

### <span data-ttu-id="c3b28-147">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="c3b28-147">-StorageAccountResourceId</span></span>
<span data-ttu-id="c3b28-148">Список ИД ресурсов для учетных записей хранения.</span><span class="sxs-lookup"><span data-stu-id="c3b28-148">List of Resource Ids of Storage Accounts.</span></span> <span data-ttu-id="c3b28-149">Atleast one является обязательным.</span><span class="sxs-lookup"><span data-stu-id="c3b28-149">Atleast one is mandatory.</span></span>

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

### <span data-ttu-id="c3b28-150">-StreetAddress1</span><span class="sxs-lookup"><span data-stu-id="c3b28-150">-StreetAddress1</span></span>
<span data-ttu-id="c3b28-151">Адрес</span><span class="sxs-lookup"><span data-stu-id="c3b28-151">Street Address</span></span>

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

### <span data-ttu-id="c3b28-152">-StreetAddress2</span><span class="sxs-lookup"><span data-stu-id="c3b28-152">-StreetAddress2</span></span>
<span data-ttu-id="c3b28-153">Дополнительный адрес</span><span class="sxs-lookup"><span data-stu-id="c3b28-153">Additional Street Address</span></span>

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

### <span data-ttu-id="c3b28-154">-StreetAddress3</span><span class="sxs-lookup"><span data-stu-id="c3b28-154">-StreetAddress3</span></span>
<span data-ttu-id="c3b28-155">Дополнительный адрес</span><span class="sxs-lookup"><span data-stu-id="c3b28-155">Additional Street Address</span></span>

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

### <span data-ttu-id="c3b28-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c3b28-156">-Confirm</span></span>
<span data-ttu-id="c3b28-157">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c3b28-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3b28-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3b28-158">-WhatIf</span></span>
<span data-ttu-id="c3b28-159">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c3b28-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c3b28-160">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="c3b28-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3b28-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3b28-161">CommonParameters</span></span>
<span data-ttu-id="c3b28-162">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3b28-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3b28-163">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c3b28-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3b28-164">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c3b28-164">INPUTS</span></span>

### <span data-ttu-id="c3b28-165">System.String[]</span><span class="sxs-lookup"><span data-stu-id="c3b28-165">System.String[]</span></span>

## <span data-ttu-id="c3b28-166">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c3b28-166">OUTPUTS</span></span>

### <span data-ttu-id="c3b28-167">Microsoft.Azure.PowerShell.Cmdlets.DataBox.Models.PSDAtaBoxJob</span><span class="sxs-lookup"><span data-stu-id="c3b28-167">Microsoft.Azure.PowerShell.Cmdlets.DataBox.Models.PSDataBoxJob</span></span>

## <span data-ttu-id="c3b28-168">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c3b28-168">NOTES</span></span>

## <span data-ttu-id="c3b28-169">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c3b28-169">RELATED LINKS</span></span>
