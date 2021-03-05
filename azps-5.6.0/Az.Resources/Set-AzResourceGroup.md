---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 4E5C059B-36F3-41C8-9FDB-69F5318CF39B
online version: https://docs.microsoft.com/powershell/module/az.resources/set-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResourceGroup.md
ms.openlocfilehash: f344c3cd08fb717d1229fb0abb4386c8a2d39d5f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995991"
---
# <span data-ttu-id="01710-101">Set-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="01710-101">Set-AzResourceGroup</span></span>

## <span data-ttu-id="01710-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01710-102">SYNOPSIS</span></span>
<span data-ttu-id="01710-103">Изменяет группу ресурсов.</span><span class="sxs-lookup"><span data-stu-id="01710-103">Modifies a resource group.</span></span>

## <span data-ttu-id="01710-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="01710-104">SYNTAX</span></span>

### <span data-ttu-id="01710-105">SetByResourceGroupName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="01710-105">SetByResourceGroupName (Default)</span></span>
```
Set-AzResourceGroup -Name <String> [-Tag] <Hashtable> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="01710-106">SetByResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="01710-106">SetByResourceGroupId</span></span>
```
Set-AzResourceGroup [-Tag] <Hashtable> -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="01710-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="01710-107">DESCRIPTION</span></span>
<span data-ttu-id="01710-108">При **этом свойства группы** ресурсов изменяется с их свойствами.</span><span class="sxs-lookup"><span data-stu-id="01710-108">The **Set-AzResourceGroup** cmdlet modifies the properties of a resource group.</span></span>
<span data-ttu-id="01710-109">С помощью этого командлета можно добавлять, изменять и удалять теги Azure, примененные к группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="01710-109">You can use this cmdlet to add, change, or delete the Azure tags applied to a resource group.</span></span>
<span data-ttu-id="01710-110">Укажите *параметр Name,* чтобы идентифицировать группу ресурсов, и параметр *Tag,* чтобы изменить теги.</span><span class="sxs-lookup"><span data-stu-id="01710-110">Specify the *Name* parameter to identify the resource group and the *Tag* parameter to modify the tags.</span></span>
<span data-ttu-id="01710-111">С помощью этого cmdlet невозможно изменить имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="01710-111">You cannot use this cmdlet to change the name of a resource group.</span></span>

## <span data-ttu-id="01710-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="01710-112">EXAMPLES</span></span>

### <span data-ttu-id="01710-113">Пример 1. Применение тега к группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="01710-113">Example 1: Apply a tag to a resource group</span></span>
```
PS C:\>Set-AzResourceGroup -Name "ContosoRG" -Tag @{Department="IT"}
```

<span data-ttu-id="01710-114">Эта команда применяет тег Department со значением ИТ к группе ресурсов, у нее нет тегов.</span><span class="sxs-lookup"><span data-stu-id="01710-114">This command applies a Department tag with a value of IT to a resource group that has no existing tags.</span></span>

### <span data-ttu-id="01710-115">Пример 2. Добавление тегов в группу ресурсов</span><span class="sxs-lookup"><span data-stu-id="01710-115">Example 2: Add tags to a resource group</span></span>
```
PS C:\>$Tags = (Get-AzResourceGroup -Name "ContosoRG").Tags
PS C:\> $Tags
PS C:\> $Tags += @{"Status"="Approved"; "FY2016"=$null}
PS C:\> Set-AzResourceGroup -Name "ContosoRG" -Tag $Tags
PS C:> (Get-AzResourceGroup -Name "ContosoRG").Tags
```

<span data-ttu-id="01710-116">В этом примере тег состояния со значением "Утверждено" и тегом "ФГ2016" добавляется в группу ресурсов, которая имеет теги.</span><span class="sxs-lookup"><span data-stu-id="01710-116">This example adds a Status tag with a value of Approved and an FY2016 tag to a resource group that has existing tags.</span></span> <span data-ttu-id="01710-117">Поскольку эти теги заменяют существующие, необходимо включить существующие теги в новую коллекцию тегов или потерять их.</span><span class="sxs-lookup"><span data-stu-id="01710-117">Because the tags you specify replace the existing tags, you must include the existing tags in the new tag collection or you will lose them.</span></span>
<span data-ttu-id="01710-118">Первая команда получает группу ресурсов ContosoRG и использует метод точки, чтобы получить значение свойства "Теги".</span><span class="sxs-lookup"><span data-stu-id="01710-118">The first command gets the ContosoRG resource group and uses the dot method to get the value of its Tags property.</span></span> <span data-ttu-id="01710-119">Команда сохраняет теги в переменной $Tags.</span><span class="sxs-lookup"><span data-stu-id="01710-119">The command stores the tags in the $Tags variable.</span></span>
<span data-ttu-id="01710-120">Вторая команда получает теги в переменной $Tags.</span><span class="sxs-lookup"><span data-stu-id="01710-120">The second command gets the tags in the $Tags variable.</span></span>
<span data-ttu-id="01710-121">Третья команда использует оператор назначения += для добавления тегов состояния и FY2016 в массив тегов в переменной $Tags.</span><span class="sxs-lookup"><span data-stu-id="01710-121">The third command uses the += assignment operator to add the Status and FY2016 tags to the array of tags in the $Tags variable.</span></span>
<span data-ttu-id="01710-122">Четвертая команда использует параметр *Tag* группы **Set-AzResourceGroup** для применения тегов переменной $Tags к группе ресурсов ContosoRG.</span><span class="sxs-lookup"><span data-stu-id="01710-122">The fourth command uses the *Tag* parameter of **Set-AzResourceGroup** to apply the tags in the $Tags variable to the ContosoRG resource group.</span></span>
<span data-ttu-id="01710-123">Пятая команда получает все теги, примененные к группе ресурсов ContosoRG.</span><span class="sxs-lookup"><span data-stu-id="01710-123">The fifth command gets all of the tags applied to the ContosoRG resource group.</span></span> <span data-ttu-id="01710-124">Выходные данные показывают, что группа ресурсов имеет тег "Отдел" и два новых тега: "Состояние" и "ФГ2015".</span><span class="sxs-lookup"><span data-stu-id="01710-124">The output shows that the resource group has the Department tag and the two new tags, Status and FY2015.</span></span>

### <span data-ttu-id="01710-125">Пример 3. Удаление всех тегов для группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="01710-125">Example 3: Delete all tags for a resource group</span></span>
```
PS C:\>Set-AzResourceGroup -Name "ContosoRG" -Tag @{}
```

<span data-ttu-id="01710-126">Эта команда определяет параметр *Tag* с пустым значением для hash table, чтобы удалить все теги из группы ресурсов ContosoRG.</span><span class="sxs-lookup"><span data-stu-id="01710-126">This command specifies the *Tag* parameter with an empty hash table value to delete all tags from the ContosoRG resource group.</span></span>

## <span data-ttu-id="01710-127">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="01710-127">PARAMETERS</span></span>

### <span data-ttu-id="01710-128">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="01710-128">-ApiVersion</span></span>
<span data-ttu-id="01710-129">Указывает версию API, которая поддерживается поставщиком ресурсов.</span><span class="sxs-lookup"><span data-stu-id="01710-129">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="01710-130">Вы можете указать другую версию, чем версия по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="01710-130">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="01710-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01710-131">-DefaultProfile</span></span>
<span data-ttu-id="01710-132">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="01710-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="01710-133">-Id</span><span class="sxs-lookup"><span data-stu-id="01710-133">-Id</span></span>
<span data-ttu-id="01710-134">Определяет код группы ресурсов, который нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="01710-134">Specifies the ID of the resource group to modify.</span></span>

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

### <span data-ttu-id="01710-135">-Name</span><span class="sxs-lookup"><span data-stu-id="01710-135">-Name</span></span>
<span data-ttu-id="01710-136">Имя группы ресурсов, которая будет изменяться.</span><span class="sxs-lookup"><span data-stu-id="01710-136">Specifies the name of the resource group to modify.</span></span>

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

### <span data-ttu-id="01710-137">-Pre</span><span class="sxs-lookup"><span data-stu-id="01710-137">-Pre</span></span>
<span data-ttu-id="01710-138">Указывает на то, что этот cmdlet рассматривает предварительные версии API при автоматическом определении используемой версии.</span><span class="sxs-lookup"><span data-stu-id="01710-138">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="01710-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="01710-139">-Tag</span></span>
<span data-ttu-id="01710-140">Пары значений ключа в виде hash table.</span><span class="sxs-lookup"><span data-stu-id="01710-140">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="01710-141">Например: @{key0="value0";key1=$null;key2="value2"} Тег — это пара "имя-значение", которую можно создать и применить к ресурсам и группам ресурсов.</span><span class="sxs-lookup"><span data-stu-id="01710-141">For example: @{key0="value0";key1=$null;key2="value2"} A tag is a name-value pair that you can create and apply to resources and resource groups.</span></span> <span data-ttu-id="01710-142">После назначения тегов ресурсам и группам можно  использовать параметр "Тег" в Get-AzResource и Get-AzResourceGroup для поиска ресурсов и групп по имени или имени и значению тега.</span><span class="sxs-lookup"><span data-stu-id="01710-142">After you assign tags to resources and groups, you can use the *Tag* parameter of Get-AzResource and Get-AzResourceGroup to search for resources and groups by tag name or name and value.</span></span> <span data-ttu-id="01710-143">С помощью тегов можно классифицировать ресурсы,например по отделам или затратам, а также для отслеживания заметок и примечаний к ресурсам.</span><span class="sxs-lookup"><span data-stu-id="01710-143">You can use tags to categorize your resources, such as by department or cost center, or to track notes or comments about the resources.</span></span>
<span data-ttu-id="01710-144">Чтобы добавить или изменить тег, необходимо заменить коллекцию тегов для группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="01710-144">To add or change a tag, you must replace the collection of tags for the resource group.</span></span> <span data-ttu-id="01710-145">Чтобы удалить тег, введите в качестве тега из **Get-AzResourceGroup** таблицу со всеми тегами, которые в данный момент применены к группе ресурсов, кроме тега, который вы хотите удалить.</span><span class="sxs-lookup"><span data-stu-id="01710-145">To delete a tag, enter a hash table with all tags currently applied to the resource group, from **Get-AzResourceGroup**, except for the tag you want to delete.</span></span> <span data-ttu-id="01710-146">Чтобы удалить все теги из группы ресурсов, укажите пустую `@{}` таблицу:</span><span class="sxs-lookup"><span data-stu-id="01710-146">To delete all tags from a resource group, specify an empty hash table: `@{}`.</span></span>

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

### <span data-ttu-id="01710-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01710-147">CommonParameters</span></span>
<span data-ttu-id="01710-148">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01710-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01710-149">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="01710-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01710-150">INPUTS</span><span class="sxs-lookup"><span data-stu-id="01710-150">INPUTS</span></span>

### <span data-ttu-id="01710-151">System.String</span><span class="sxs-lookup"><span data-stu-id="01710-151">System.String</span></span>

### <span data-ttu-id="01710-152">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="01710-152">System.Collections.Hashtable</span></span>

## <span data-ttu-id="01710-153">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="01710-153">OUTPUTS</span></span>

### <span data-ttu-id="01710-154">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="01710-154">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroup</span></span>

## <span data-ttu-id="01710-155">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="01710-155">NOTES</span></span>

## <span data-ttu-id="01710-156">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="01710-156">RELATED LINKS</span></span>

[<span data-ttu-id="01710-157">Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="01710-157">Get-AzResource</span></span>](./Get-AzResource.md)

[<span data-ttu-id="01710-158">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="01710-158">Get-AzResourceGroup</span></span>](./Get-AzResourceGroup.md)

[<span data-ttu-id="01710-159">New-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="01710-159">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="01710-160">Remove-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="01710-160">Remove-AzResourceGroup</span></span>](./Remove-AzResourceGroup.md)
