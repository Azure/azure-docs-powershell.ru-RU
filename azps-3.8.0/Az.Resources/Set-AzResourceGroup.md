---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 4E5C059B-36F3-41C8-9FDB-69F5318CF39B
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResourceGroup.md
ms.openlocfilehash: 0523041357becb38475bb496c94ba1fd48c5acaf
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066188"
---
# <span data-ttu-id="0b6e4-101">Set-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="0b6e4-101">Set-AzResourceGroup</span></span>

## <span data-ttu-id="0b6e4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0b6e4-102">SYNOPSIS</span></span>
<span data-ttu-id="0b6e4-103">Изменяет группу ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0b6e4-103">Modifies a resource group.</span></span>

## <span data-ttu-id="0b6e4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0b6e4-104">SYNTAX</span></span>

### <span data-ttu-id="0b6e4-105">SetByResourceGroupName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0b6e4-105">SetByResourceGroupName (Default)</span></span>
```
Set-AzResourceGroup -Name <String> [-Tag] <Hashtable> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0b6e4-106">SetByResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="0b6e4-106">SetByResourceGroupId</span></span>
```
Set-AzResourceGroup [-Tag] <Hashtable> -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0b6e4-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0b6e4-107">DESCRIPTION</span></span>
<span data-ttu-id="0b6e4-108">Командлет **Set-AzResourceGroup** изменяет свойства группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0b6e4-108">The **Set-AzResourceGroup** cmdlet modifies the properties of a resource group.</span></span>
<span data-ttu-id="0b6e4-109">Вы можете использовать этот командлет для добавления, изменения или удаления тегов Azure, примененных к группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0b6e4-109">You can use this cmdlet to add, change, or delete the Azure tags applied to a resource group.</span></span>
<span data-ttu-id="0b6e4-110">Укажите параметр *Name (имя* ), чтобы определить группу ресурсов и параметр *Tag* , чтобы изменить теги.</span><span class="sxs-lookup"><span data-stu-id="0b6e4-110">Specify the *Name* parameter to identify the resource group and the *Tag* parameter to modify the tags.</span></span>
<span data-ttu-id="0b6e4-111">Вы не можете использовать этот командлет для изменения имени группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0b6e4-111">You cannot use this cmdlet to change the name of a resource group.</span></span>

## <span data-ttu-id="0b6e4-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0b6e4-112">EXAMPLES</span></span>

### <span data-ttu-id="0b6e4-113">Пример 1: применение тега к группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="0b6e4-113">Example 1: Apply a tag to a resource group</span></span>
```
PS C:\>Set-AzResourceGroup -Name "ContosoRG" -Tag @{Department="IT"}
```

<span data-ttu-id="0b6e4-114">Эта команда применяет к группе ресурсов тег подразделения со значением, не имеющей существующих тегов.</span><span class="sxs-lookup"><span data-stu-id="0b6e4-114">This command applies a Department tag with a value of IT to a resource group that has no existing tags.</span></span>

### <span data-ttu-id="0b6e4-115">Пример 2: Добавление тегов в группу ресурсов</span><span class="sxs-lookup"><span data-stu-id="0b6e4-115">Example 2: Add tags to a resource group</span></span>
```
PS C:\>$Tags = (Get-AzResourceGroup -Name "ContosoRG").Tags
PS C:\> $Tags
PS C:\> $Tags += @{"Status"="Approved"; "FY2016"=$null}
PS C:\> Set-AzResourceGroup -Name "ContosoRG" -Tag $Tags
PS C:> (Get-AzResourceGroup -Name "ContosoRG").Tags
```

<span data-ttu-id="0b6e4-116">В этом примере в группу ресурсов, имеющую существующие теги, добавляется тег Status со значением утвержденный и тег FY2016.</span><span class="sxs-lookup"><span data-stu-id="0b6e4-116">This example adds a Status tag with a value of Approved and an FY2016 tag to a resource group that has existing tags.</span></span> <span data-ttu-id="0b6e4-117">Так как указанные Теги заменяют существующие теги, необходимо включить существующие теги в новую коллекцию тегов, иначе они будут потеряны.</span><span class="sxs-lookup"><span data-stu-id="0b6e4-117">Because the tags you specify replace the existing tags, you must include the existing tags in the new tag collection or you will lose them.</span></span>
<span data-ttu-id="0b6e4-118">Первая команда получает группу ресурсов ContosoRG и использует метод Dot для получения значения свойства Tags.</span><span class="sxs-lookup"><span data-stu-id="0b6e4-118">The first command gets the ContosoRG resource group and uses the dot method to get the value of its Tags property.</span></span> <span data-ttu-id="0b6e4-119">Команды хранят теги в переменной $Tags.</span><span class="sxs-lookup"><span data-stu-id="0b6e4-119">The command stores the tags in the $Tags variable.</span></span>
<span data-ttu-id="0b6e4-120">Вторая команда получает теги в переменной $Tags.</span><span class="sxs-lookup"><span data-stu-id="0b6e4-120">The second command gets the tags in the $Tags variable.</span></span>
<span data-ttu-id="0b6e4-121">Третья команда использует оператор присваивания + = для добавления тегов status и FY2016 в массив тегов в переменной $Tags.</span><span class="sxs-lookup"><span data-stu-id="0b6e4-121">The third command uses the += assignment operator to add the Status and FY2016 tags to the array of tags in the $Tags variable.</span></span>
<span data-ttu-id="0b6e4-122">Четвертая команда использует параметр *Tag* для **Set-AzResourceGroup** , чтобы применить теги в переменной $Tags к группе ресурсов ContosoRG.</span><span class="sxs-lookup"><span data-stu-id="0b6e4-122">The fourth command uses the *Tag* parameter of **Set-AzResourceGroup** to apply the tags in the $Tags variable to the ContosoRG resource group.</span></span>
<span data-ttu-id="0b6e4-123">Пятая команда получает все теги, примененные к группе ресурсов ContosoRG.</span><span class="sxs-lookup"><span data-stu-id="0b6e4-123">The fifth command gets all of the tags applied to the ContosoRG resource group.</span></span> <span data-ttu-id="0b6e4-124">В выходных данных показано, что группа ресурсов содержит тег отдела и два новых тега, Status и FY2015.</span><span class="sxs-lookup"><span data-stu-id="0b6e4-124">The output shows that the resource group has the Department tag and the two new tags, Status and FY2015.</span></span>

### <span data-ttu-id="0b6e4-125">Пример 3: удаление всех тегов для группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="0b6e4-125">Example 3: Delete all tags for a resource group</span></span>
```
PS C:\>Set-AzResourceGroup -Name "ContosoRG" -Tag @{}
```

<span data-ttu-id="0b6e4-126">Эта команда задает параметр *тега* с пустым значением хэш-таблицы для удаления всех тегов из группы ресурсов ContosoRG.</span><span class="sxs-lookup"><span data-stu-id="0b6e4-126">This command specifies the *Tag* parameter with an empty hash table value to delete all tags from the ContosoRG resource group.</span></span>

## <span data-ttu-id="0b6e4-127">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0b6e4-127">PARAMETERS</span></span>

### <span data-ttu-id="0b6e4-128">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="0b6e4-128">-ApiVersion</span></span>
<span data-ttu-id="0b6e4-129">Указывает версию API, поддерживаемую поставщиком ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0b6e4-129">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="0b6e4-130">Вы можете выбрать версию, отличную от версии по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0b6e4-130">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="0b6e4-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b6e4-131">-DefaultProfile</span></span>
<span data-ttu-id="0b6e4-132">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="0b6e4-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0b6e4-133">-ID</span><span class="sxs-lookup"><span data-stu-id="0b6e4-133">-Id</span></span>
<span data-ttu-id="0b6e4-134">Указывает идентификатор группы ресурсов, которую нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="0b6e4-134">Specifies the ID of the resource group to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceGroupId
Aliases: ResourceGroupId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b6e4-135">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0b6e4-135">-Name</span></span>
<span data-ttu-id="0b6e4-136">Указывает имя группы ресурсов, которую нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="0b6e4-136">Specifies the name of the resource group to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceGroupName
Aliases: ResourceGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b6e4-137">-Pre</span><span class="sxs-lookup"><span data-stu-id="0b6e4-137">-Pre</span></span>
<span data-ttu-id="0b6e4-138">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="0b6e4-138">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="0b6e4-139">-Тег</span><span class="sxs-lookup"><span data-stu-id="0b6e4-139">-Tag</span></span>
<span data-ttu-id="0b6e4-140">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="0b6e4-140">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="0b6e4-141">Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"} тег — это пара "имя-значение", которую можно создать и применить к ресурсам и группам ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0b6e4-141">For example: @{key0="value0";key1=$null;key2="value2"} A tag is a name-value pair that you can create and apply to resources and resource groups.</span></span> <span data-ttu-id="0b6e4-142">После того как вы назначьте Теги ресурсам и группам, вы можете использовать параметр *Tag* Get-AzResource и Get-AzResourceGroup для поиска ресурсов и групп по имени или имени и значению тега.</span><span class="sxs-lookup"><span data-stu-id="0b6e4-142">After you assign tags to resources and groups, you can use the *Tag* parameter of Get-AzResource and Get-AzResourceGroup to search for resources and groups by tag name or name and value.</span></span> <span data-ttu-id="0b6e4-143">Теги можно использовать для классификации ресурсов, таких как отдел или центр затрат, а также для отслеживания заметок и примечаний к ресурсам.</span><span class="sxs-lookup"><span data-stu-id="0b6e4-143">You can use tags to categorize your resources, such as by department or cost center, or to track notes or comments about the resources.</span></span>
<span data-ttu-id="0b6e4-144">Чтобы добавить или изменить тег, необходимо заменить коллекцию тегов для группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0b6e4-144">To add or change a tag, you must replace the collection of tags for the resource group.</span></span> <span data-ttu-id="0b6e4-145">Чтобы удалить тег, введите хэш-таблицу со всеми тегами, которые в настоящее время применены к группе ресурсов из **Get-AzResourceGroup** , за исключением тега, который вы хотите удалить.</span><span class="sxs-lookup"><span data-stu-id="0b6e4-145">To delete a tag, enter a hash table with all tags currently applied to the resource group, from **Get-AzResourceGroup** , except for the tag you want to delete.</span></span> <span data-ttu-id="0b6e4-146">Чтобы удалить все теги из группы ресурсов, укажите пустую хэш- `@{}` таблицу.</span><span class="sxs-lookup"><span data-stu-id="0b6e4-146">To delete all tags from a resource group, specify an empty hash table: `@{}`.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b6e4-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b6e4-147">CommonParameters</span></span>
<span data-ttu-id="0b6e4-148">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0b6e4-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b6e4-149">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0b6e4-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b6e4-150">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0b6e4-150">INPUTS</span></span>

### <span data-ttu-id="0b6e4-151">System. String</span><span class="sxs-lookup"><span data-stu-id="0b6e4-151">System.String</span></span>

### <span data-ttu-id="0b6e4-152">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="0b6e4-152">System.Collections.Hashtable</span></span>

## <span data-ttu-id="0b6e4-153">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0b6e4-153">OUTPUTS</span></span>

### <span data-ttu-id="0b6e4-154">Microsoft. Azure. Commands. ResourceManager. командлеты. SdkModels. PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="0b6e4-154">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroup</span></span>

## <span data-ttu-id="0b6e4-155">Пуск</span><span class="sxs-lookup"><span data-stu-id="0b6e4-155">NOTES</span></span>

## <span data-ttu-id="0b6e4-156">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0b6e4-156">RELATED LINKS</span></span>

[<span data-ttu-id="0b6e4-157">Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="0b6e4-157">Get-AzResource</span></span>](./Get-AzResource.md)

[<span data-ttu-id="0b6e4-158">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="0b6e4-158">Get-AzResourceGroup</span></span>](./Get-AzResourceGroup.md)

[<span data-ttu-id="0b6e4-159">New-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="0b6e4-159">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="0b6e4-160">Remove-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="0b6e4-160">Remove-AzResourceGroup</span></span>](./Remove-AzResourceGroup.md)
