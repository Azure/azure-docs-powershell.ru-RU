---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C2C608E5-3351-4D01-8533-9668B2E9F1D1
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResource.md
ms.openlocfilehash: 92a9e1820af2e850af6c3abaca71a7be1f15ed5f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101950995"
---
# <span data-ttu-id="977e2-101">Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="977e2-101">Get-AzResource</span></span>

## <span data-ttu-id="977e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="977e2-102">SYNOPSIS</span></span>

<span data-ttu-id="977e2-103">Ресурсы.</span><span class="sxs-lookup"><span data-stu-id="977e2-103">Gets resources.</span></span>

## <span data-ttu-id="977e2-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="977e2-104">SYNTAX</span></span>

### <span data-ttu-id="977e2-105">ByTagNameValueParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="977e2-105">ByTagNameValueParameterSet (Default)</span></span>
```
Get-AzResource [-Name <String>] [-ResourceType <String>] [-ODataQuery <String>] [-ResourceGroupName <String>]
 [-TagName <String>] [-TagValue <String>] [-ExpandProperties] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="977e2-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="977e2-106">ByResourceId</span></span>
```
Get-AzResource -ResourceId <String> [-ODataQuery <String>] [-ExpandProperties] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="977e2-107">ByTagObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="977e2-107">ByTagObjectParameterSet</span></span>
```
Get-AzResource [-Name <String>] [-ResourceType <String>] [-ODataQuery <String>] [-ResourceGroupName <String>]
 -Tag <Hashtable> [-ExpandProperties] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="977e2-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="977e2-108">DESCRIPTION</span></span>

<span data-ttu-id="977e2-109">Для получения ресурсов Azure можно **использовать cmdlet Get-AzResource.**</span><span class="sxs-lookup"><span data-stu-id="977e2-109">The **Get-AzResource** cmdlet gets Azure resources.</span></span>

## <span data-ttu-id="977e2-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="977e2-110">EXAMPLES</span></span>

### <span data-ttu-id="977e2-111">Пример 1. Получить все ресурсы в текущей подписке</span><span class="sxs-lookup"><span data-stu-id="977e2-111">Example 1: Get all resources in the current subscription</span></span>

```
PS C:\> Get-AzResource | ft

Name    ResourceGroupName  ResourceType                            Location
----    -----------------  ------------                            --------
testVM  testRG             Microsoft.Compute/virtualMachines       westus
disk    testRG             Microsoft.Compute/disks                 westus
nic     testRG             Microsoft.Network/networkInterfaces     westus
nsg     testRG             Microsoft.Network/networkSecurityGroups westus
ip      testRG             Microsoft.Network/publicIPAddresses     westus
vnet    testRG             Microsoft.Network/virtualNetworks       westus
testKV  otherRG            Microsoft.KeyVault/vaults               eastus
storage otherResourceGroup Microsoft.Storage/storageAccounts       eastus
testVM2 otherResourceGroup Microsoft.Compute/virtualMachines       eastus
```

<span data-ttu-id="977e2-112">Эта команда получает все ресурсы в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="977e2-112">This command gets all of the resources in the current subscription.</span></span>

### <span data-ttu-id="977e2-113">Пример 2. Получить все ресурсы в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="977e2-113">Example 2: Get all resources in a resource group</span></span>

```
PS C:\> Get-AzResource -ResourceGroupName testRG | ft

Name   ResourceGroupName ResourceType                            Location
----   ----------------- ------------                            --------
testVM testRG            Microsoft.Compute/virtualMachines       westus
disk   testRG            Microsoft.Compute/disks                 westus
nic    testRG            Microsoft.Network/networkInterfaces     westus
nsg    testRG            Microsoft.Network/networkSecurityGroups westus
ip     testRG            Microsoft.Network/publicIPAddresses     westus
vnet   testRG            Microsoft.Network/virtualNetworks       westus
```

<span data-ttu-id="977e2-114">Эта команда получает все ресурсы из группы ресурсов TestRG.</span><span class="sxs-lookup"><span data-stu-id="977e2-114">This command gets all of the resources in the resource group "testRG".</span></span>

### <span data-ttu-id="977e2-115">Пример 3. Получить все ресурсы, группа ресурсов которых соответствует предоставленной подгруппе</span><span class="sxs-lookup"><span data-stu-id="977e2-115">Example 3: Get all resources whose resource group matches the provided wildcard</span></span>

```
PS C:\> Get-AzResource -ResourceGroupName other* | ft

Name    ResourceGroupName  ResourceType                      Location
----    -----------------  ------------                      --------
testKV  otherRG            Microsoft.KeyVault/vaults         eastus
storage otherResourceGroup Microsoft.Storage/storageAccounts eastus
testVM2 otherResourceGroup Microsoft.Compute/virtualMachines eastus
```

<span data-ttu-id="977e2-116">Эта команда возвращает все ресурсы, группа которых относится к компании, с "другими".</span><span class="sxs-lookup"><span data-stu-id="977e2-116">This command gets all of the resources whose resource group they belong in beings with "other".</span></span>

### <span data-ttu-id="977e2-117">Пример 4. Получить все ресурсы с заданным именем</span><span class="sxs-lookup"><span data-stu-id="977e2-117">Example 4: Get all resources with a given name</span></span>

```
PS C:\> Get-AzResource -Name testVM | fl

Name              : testVM
ResourceGroupName : testRG
ResourceType      : Microsoft.Compute/virtualMachines
Location          : westus
ResourceId        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testRG/providers/Microsoft.Compute/virtualMachines/testVM
Tags              :
                    Name    Value
                    ======  ========
                    Dept    IT
                    Year    2002
                    Status  Approved
```

<span data-ttu-id="977e2-118">Эта команда возвращает все ресурсы с именем testVM.</span><span class="sxs-lookup"><span data-stu-id="977e2-118">This command gets all of the resources whose resource name is "testVM".</span></span>

### <span data-ttu-id="977e2-119">Пример 5. Получить все ресурсы, имена которых совпадают с предоставленными поддиавными знаками</span><span class="sxs-lookup"><span data-stu-id="977e2-119">Example 5: Get all resources whose name matches the provided wildcard</span></span>

```
PS C:\> Get-AzResource -Name test* | ft

Name    ResourceGroupName  ResourceType                      Location
----    -----------------  ------------                      --------
testVM  testRG             Microsoft.Compute/virtualMachines westus
testKV  otherRG            Microsoft.KeyVault/vaults         eastus
testVM2 otherResourceGroup Microsoft.Compute/virtualMachines eastus
```

<span data-ttu-id="977e2-120">Эта команда возвращает все ресурсы, название которых начинается с "проверка".</span><span class="sxs-lookup"><span data-stu-id="977e2-120">This command gets all of the resources whose resource name begins with "test".</span></span>

### <span data-ttu-id="977e2-121">Пример 6. Получить все ресурсы заданного типа ресурсов</span><span class="sxs-lookup"><span data-stu-id="977e2-121">Example 6: Get all resources of a given resource type</span></span>

```
PS C:\> Get-AzResource -ResourceType Microsoft.Compute/virtualMachines | ft

Name    ResourceGroupName  ResourceType                      Location
----    -----------------  ------------                      --------
testVM  testRG             Microsoft.Compute/virtualMachines westus
testVM2 otherResourceGroup Microsoft.Compute/virtualMachines eastus
```

<span data-ttu-id="977e2-122">Эта команда возвращает все ресурсы из текущих подписок, которые являются виртуальными компьютерами.</span><span class="sxs-lookup"><span data-stu-id="977e2-122">This command gets all of the resources in the current subscriptions that are virtual machines.</span></span>

### <span data-ttu-id="977e2-123">Пример 7. Поимка ресурса по его ид</span><span class="sxs-lookup"><span data-stu-id="977e2-123">Example 7: Get a resource by resource id</span></span>

```
PS C:\> Get-AzResource -ResourceId /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testRG/providers/Microsoft.Compute/virtualMachines/testVM

Name              : testVM
ResourceGroupName : testRG
ResourceType      : Microsoft.Compute/virtualMachines
Location          : westus
ResourceId        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testRG/providers/Microsoft.Compute/virtualMachines/testVM
Tags              :
                    Name    Value
                    ======  ========
                    Dept    IT
                    Year    2002
                    Status  Approved
```

<span data-ttu-id="977e2-124">Эта команда возвращает ресурсу предоставленный ид ресурса — виртуальную машину с искомой машиной testVM в группе ресурсов testRG.</span><span class="sxs-lookup"><span data-stu-id="977e2-124">This command gets the resource with the provided resource id, which is a virtual machine called "testVM" in the resource group "testRG".</span></span>

## <span data-ttu-id="977e2-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="977e2-125">PARAMETERS</span></span>

### <span data-ttu-id="977e2-126">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="977e2-126">-ApiVersion</span></span>

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

### <span data-ttu-id="977e2-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="977e2-127">-DefaultProfile</span></span>
<span data-ttu-id="977e2-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="977e2-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="977e2-129">-ExpandProperties</span><span class="sxs-lookup"><span data-stu-id="977e2-129">-ExpandProperties</span></span>
<span data-ttu-id="977e2-130">Если задан этот вариант, расширяет свойства ресурса.</span><span class="sxs-lookup"><span data-stu-id="977e2-130">When specified, expands the properties of the resource.</span></span>

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

### <span data-ttu-id="977e2-131">-Name</span><span class="sxs-lookup"><span data-stu-id="977e2-131">-Name</span></span>
<span data-ttu-id="977e2-132">Имена извлекаемого ресурса.</span><span class="sxs-lookup"><span data-stu-id="977e2-132">The name of the resource(s) to be retrieved.</span></span> <span data-ttu-id="977e2-133">Этот параметр поддерживает поддиавные знаки в начале или в конце строки.</span><span class="sxs-lookup"><span data-stu-id="977e2-133">This parameter supports wildcards at the beginning and/or end of the string.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTagNameValueParameterSet, ByTagObjectParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="977e2-134">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="977e2-134">-ODataQuery</span></span>

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

### <span data-ttu-id="977e2-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="977e2-135">-Pre</span></span>

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

### <span data-ttu-id="977e2-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="977e2-136">-ResourceGroupName</span></span>
<span data-ttu-id="977e2-137">Группа извлекаемой ресурсов.</span><span class="sxs-lookup"><span data-stu-id="977e2-137">The resource group the resource(s) that is retrieved belongs in.</span></span> <span data-ttu-id="977e2-138">Этот параметр поддерживает поддиавные знаки в начале или в конце строки.</span><span class="sxs-lookup"><span data-stu-id="977e2-138">This parameter supports wildcards at the beginning and/or end of the string.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTagNameValueParameterSet, ByTagObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="977e2-139">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="977e2-139">-ResourceId</span></span>
<span data-ttu-id="977e2-140">Указывает полностью определенный ИД ресурса, как по следующему примеру. `/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/providers/Microsoft.Compute/virtualMachines`</span><span class="sxs-lookup"><span data-stu-id="977e2-140">Specifies the fully qualified resource ID, as in the following example `/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/providers/Microsoft.Compute/virtualMachines`</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="977e2-141">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="977e2-141">-ResourceType</span></span>
<span data-ttu-id="977e2-142">Тип извлекаемого ресурса.</span><span class="sxs-lookup"><span data-stu-id="977e2-142">The resource type of the resource(s) to be retrieved.</span></span> <span data-ttu-id="977e2-143">Например, Microsoft.Compute/virtualMaоes</span><span class="sxs-lookup"><span data-stu-id="977e2-143">For example, Microsoft.Compute/virtualMachines</span></span>

```yaml
Type: System.String
Parameter Sets: ByTagNameValueParameterSet, ByTagObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="977e2-144">-Tag</span><span class="sxs-lookup"><span data-stu-id="977e2-144">-Tag</span></span>

<span data-ttu-id="977e2-145">Возвращает ресурсы с указанным тегом Azure.</span><span class="sxs-lookup"><span data-stu-id="977e2-145">Gets resources that have the specified Azure tag.</span></span> <span data-ttu-id="977e2-146">Введите hash table with a Name key or Name and Value keys.</span><span class="sxs-lookup"><span data-stu-id="977e2-146">Enter a hash table with a Name key or Name and Value keys.</span></span> <span data-ttu-id="977e2-147">Поддиавные знаки не поддерживаются. Тег — это пара "имя-значение", которую можно применять к ресурсам и группам ресурсов.</span><span class="sxs-lookup"><span data-stu-id="977e2-147">Wildcard characters are not supported.A "tag" is a name-value pair that you can apply to resources and resource groups.</span></span> <span data-ttu-id="977e2-148">С помощью тегов можно классифицировать ресурсы( например, по отделам или затратам), а также отслеживать заметки и комментарии о ресурсах.</span><span class="sxs-lookup"><span data-stu-id="977e2-148">Use tags to categorize your resources, such as by department or cost center, or to track notes or comments about the resources.</span></span> <span data-ttu-id="977e2-149">Чтобы добавить тег на ресурс, используйте параметр "Тег" New-AzResource или Set-AzResource командлетов.</span><span class="sxs-lookup"><span data-stu-id="977e2-149">To add a tag to a resource, use the Tag parameter of the New-AzResource or Set-AzResource cmdlets.</span></span> <span data-ttu-id="977e2-150">Чтобы создать предопределный тег, воспользуйтесь New-AzTag командлетом.</span><span class="sxs-lookup"><span data-stu-id="977e2-150">To create a predefined tag, use the New-AzTag cmdlet.</span></span> <span data-ttu-id="977e2-151">Для получения справки по hash таблицам в Windows PowerShell запустите get-help about_Hashtables.</span><span class="sxs-lookup"><span data-stu-id="977e2-151">For help with hash tables in Windows PowerShell, run 'Get-Help about_Hashtables'.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByTagObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="977e2-152">-TagName</span><span class="sxs-lookup"><span data-stu-id="977e2-152">-TagName</span></span>
<span data-ttu-id="977e2-153">Ключ в теге извлекаемого ресурса.</span><span class="sxs-lookup"><span data-stu-id="977e2-153">The key in the tag of the resource(s) to be retrieved.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTagNameValueParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="977e2-154">-TagValue</span><span class="sxs-lookup"><span data-stu-id="977e2-154">-TagValue</span></span>
<span data-ttu-id="977e2-155">Значение в теге извлекаемого ресурса.</span><span class="sxs-lookup"><span data-stu-id="977e2-155">The value in the tag of the resource(s) to be retrieved.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTagNameValueParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="977e2-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="977e2-156">CommonParameters</span></span>
<span data-ttu-id="977e2-157">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="977e2-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="977e2-158">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="977e2-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="977e2-159">INPUTS</span><span class="sxs-lookup"><span data-stu-id="977e2-159">INPUTS</span></span>

### <span data-ttu-id="977e2-160">System.String</span><span class="sxs-lookup"><span data-stu-id="977e2-160">System.String</span></span>

## <span data-ttu-id="977e2-161">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="977e2-161">OUTPUTS</span></span>

### <span data-ttu-id="977e2-162">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResource</span><span class="sxs-lookup"><span data-stu-id="977e2-162">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResource</span></span>

## <span data-ttu-id="977e2-163">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="977e2-163">NOTES</span></span>

## <span data-ttu-id="977e2-164">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="977e2-164">RELATED LINKS</span></span>

[<span data-ttu-id="977e2-165">Move-AzResource</span><span class="sxs-lookup"><span data-stu-id="977e2-165">Move-AzResource</span></span>](./Move-AzResource.md)

[<span data-ttu-id="977e2-166">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="977e2-166">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="977e2-167">Remove-AzResource</span><span class="sxs-lookup"><span data-stu-id="977e2-167">Remove-AzResource</span></span>](./Remove-AzResource.md)

[<span data-ttu-id="977e2-168">Set-AzResource</span><span class="sxs-lookup"><span data-stu-id="977e2-168">Set-AzResource</span></span>](./Set-AzResource.md)