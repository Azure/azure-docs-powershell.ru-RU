---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C2C608E5-3351-4D01-8533-9668B2E9F1D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResource.md
ms.openlocfilehash: eb2779f2717091e09a3737ef437fa9f9615d201c
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/08/2020
ms.locfileid: "94077366"
---
# <span data-ttu-id="bfdca-101">Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="bfdca-101">Get-AzResource</span></span>

## <span data-ttu-id="bfdca-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bfdca-102">SYNOPSIS</span></span>

<span data-ttu-id="bfdca-103">Возвращает ресурсы.</span><span class="sxs-lookup"><span data-stu-id="bfdca-103">Gets resources.</span></span>

## <span data-ttu-id="bfdca-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bfdca-104">SYNTAX</span></span>

### <span data-ttu-id="bfdca-105">ByTagNameValueParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="bfdca-105">ByTagNameValueParameterSet (Default)</span></span>
```
Get-AzResource [-Name <String>] [-ResourceType <String>] [-ODataQuery <String>] [-ResourceGroupName <String>]
 [-TagName <String>] [-TagValue <String>] [-ExpandProperties] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bfdca-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="bfdca-106">ByResourceId</span></span>
```
Get-AzResource -ResourceId <String> [-ODataQuery <String>] [-ExpandProperties] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bfdca-107">ByTagObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bfdca-107">ByTagObjectParameterSet</span></span>
```
Get-AzResource [-Name <String>] [-ResourceType <String>] [-ODataQuery <String>] [-ResourceGroupName <String>]
 -Tag <Hashtable> [-ExpandProperties] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bfdca-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bfdca-108">DESCRIPTION</span></span>

<span data-ttu-id="bfdca-109">Командлет **Get-AzResource** получает ресурсы Azure.</span><span class="sxs-lookup"><span data-stu-id="bfdca-109">The **Get-AzResource** cmdlet gets Azure resources.</span></span>

## <span data-ttu-id="bfdca-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bfdca-110">EXAMPLES</span></span>

### <span data-ttu-id="bfdca-111">Пример 1: получение всех ресурсов в текущей подписке</span><span class="sxs-lookup"><span data-stu-id="bfdca-111">Example 1: Get all resources in the current subscription</span></span>

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

<span data-ttu-id="bfdca-112">Эта команда получает все ресурсы в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="bfdca-112">This command gets all of the resources in the current subscription.</span></span>

### <span data-ttu-id="bfdca-113">Пример 2: получение всех ресурсов в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="bfdca-113">Example 2: Get all resources in a resource group</span></span>

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

<span data-ttu-id="bfdca-114">Эта команда получает все ресурсы в группе ресурсов "testRG".</span><span class="sxs-lookup"><span data-stu-id="bfdca-114">This command gets all of the resources in the resource group "testRG".</span></span>

### <span data-ttu-id="bfdca-115">Пример 3: получение всех ресурсов, для которых Группа ресурсов соответствует указанному подстановочному знаку</span><span class="sxs-lookup"><span data-stu-id="bfdca-115">Example 3: Get all resources whose resource group matches the provided wildcard</span></span>

```
PS C:\> Get-AzResource -ResourceGroupName other* | ft

Name    ResourceGroupName  ResourceType                      Location
----    -----------------  ------------                      --------
testKV  otherRG            Microsoft.KeyVault/vaults         eastus
storage otherResourceGroup Microsoft.Storage/storageAccounts eastus
testVM2 otherResourceGroup Microsoft.Compute/virtualMachines eastus
```

<span data-ttu-id="bfdca-116">Эта команда получает все ресурсы, в которых Группа ресурсов принадлежит к людей, с "другим".</span><span class="sxs-lookup"><span data-stu-id="bfdca-116">This command gets all of the resources whose resource group they belong in beings with "other".</span></span>

### <span data-ttu-id="bfdca-117">Пример 4: получение всех ресурсов с заданным именем</span><span class="sxs-lookup"><span data-stu-id="bfdca-117">Example 4: Get all resources with a given name</span></span>

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

<span data-ttu-id="bfdca-118">Эта команда получает все ресурсы, имя ресурса которых равно "testVM".</span><span class="sxs-lookup"><span data-stu-id="bfdca-118">This command gets all of the resources whose resource name is "testVM".</span></span>

### <span data-ttu-id="bfdca-119">Пример 5: получение всех ресурсов, имена которых соответствуют указанному подстановочному знаку</span><span class="sxs-lookup"><span data-stu-id="bfdca-119">Example 5: Get all resources whose name matches the provided wildcard</span></span>

```
PS C:\> Get-AzResource -Name test* | ft

Name    ResourceGroupName  ResourceType                      Location
----    -----------------  ------------                      --------
testVM  testRG             Microsoft.Compute/virtualMachines westus
testKV  otherRG            Microsoft.KeyVault/vaults         eastus
testVM2 otherResourceGroup Microsoft.Compute/virtualMachines eastus
```

<span data-ttu-id="bfdca-120">Эта команда получает все ресурсы, имя ресурса которых начинается с "Test".</span><span class="sxs-lookup"><span data-stu-id="bfdca-120">This command gets all of the resources whose resource name begins with "test".</span></span>

### <span data-ttu-id="bfdca-121">Пример 6: получение всех ресурсов определенного типа ресурсов</span><span class="sxs-lookup"><span data-stu-id="bfdca-121">Example 6: Get all resources of a given resource type</span></span>

```
PS C:\> Get-AzResource -ResourceType Microsoft.Compute/virtualMachines | ft

Name    ResourceGroupName  ResourceType                      Location
----    -----------------  ------------                      --------
testVM  testRG             Microsoft.Compute/virtualMachines westus
testVM2 otherResourceGroup Microsoft.Compute/virtualMachines eastus
```

<span data-ttu-id="bfdca-122">Эта команда получает все ресурсы из текущих подписок, которые представляют собой виртуальные машины.</span><span class="sxs-lookup"><span data-stu-id="bfdca-122">This command gets all of the resources in the current subscriptions that are virtual machines.</span></span>

### <span data-ttu-id="bfdca-123">Пример 7: получение ресурса по идентификатору ресурса</span><span class="sxs-lookup"><span data-stu-id="bfdca-123">Example 7: Get a resource by resource id</span></span>

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

<span data-ttu-id="bfdca-124">Эта команда получает ресурс с предоставленным идентификатором ресурса, который является виртуальной машиной с именем "testVM" в группе ресурсов "testRG".</span><span class="sxs-lookup"><span data-stu-id="bfdca-124">This command gets the resource with the provided resource id, which is a virtual machine called "testVM" in the resource group "testRG".</span></span>

## <span data-ttu-id="bfdca-125">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bfdca-125">PARAMETERS</span></span>

### <span data-ttu-id="bfdca-126">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="bfdca-126">-ApiVersion</span></span>

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

### <span data-ttu-id="bfdca-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfdca-127">-DefaultProfile</span></span>
<span data-ttu-id="bfdca-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="bfdca-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bfdca-129">-ExpandProperties</span><span class="sxs-lookup"><span data-stu-id="bfdca-129">-ExpandProperties</span></span>
<span data-ttu-id="bfdca-130">При задании этого параметра развертываются свойства ресурса.</span><span class="sxs-lookup"><span data-stu-id="bfdca-130">When specified, expands the properties of the resource.</span></span>

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

### <span data-ttu-id="bfdca-131">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="bfdca-131">-Name</span></span>
<span data-ttu-id="bfdca-132">Имена извлекаемых ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bfdca-132">The name of the resource(s) to be retrieved.</span></span> <span data-ttu-id="bfdca-133">Этот параметр поддерживает подстановочные знаки в начале и (или) конце строки.</span><span class="sxs-lookup"><span data-stu-id="bfdca-133">This parameter supports wildcards at the beginning and/or end of the string.</span></span>

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

### <span data-ttu-id="bfdca-134">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="bfdca-134">-ODataQuery</span></span>

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

### <span data-ttu-id="bfdca-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="bfdca-135">-Pre</span></span>

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

### <span data-ttu-id="bfdca-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bfdca-136">-ResourceGroupName</span></span>
<span data-ttu-id="bfdca-137">Группа ресурсов, к которой относятся извлеченные ресурсы.</span><span class="sxs-lookup"><span data-stu-id="bfdca-137">The resource group the resource(s) that is retrieved belongs in.</span></span> <span data-ttu-id="bfdca-138">Этот параметр поддерживает подстановочные знаки в начале и (или) конце строки.</span><span class="sxs-lookup"><span data-stu-id="bfdca-138">This parameter supports wildcards at the beginning and/or end of the string.</span></span>

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

### <span data-ttu-id="bfdca-139">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bfdca-139">-ResourceId</span></span>
<span data-ttu-id="bfdca-140">Указывает полный ИД ресурса, как показано в следующем примере. `/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/providers/Microsoft.Compute/virtualMachines`</span><span class="sxs-lookup"><span data-stu-id="bfdca-140">Specifies the fully qualified resource ID, as in the following example `/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/providers/Microsoft.Compute/virtualMachines`</span></span>

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

### <span data-ttu-id="bfdca-141">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="bfdca-141">-ResourceType</span></span>
<span data-ttu-id="bfdca-142">Тип ресурса для извлекаемых ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bfdca-142">The resource type of the resource(s) to be retrieved.</span></span> <span data-ttu-id="bfdca-143">Например, Microsoft. COMPUTE/virtualMachines</span><span class="sxs-lookup"><span data-stu-id="bfdca-143">For example, Microsoft.Compute/virtualMachines</span></span>

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

### <span data-ttu-id="bfdca-144">-Тег</span><span class="sxs-lookup"><span data-stu-id="bfdca-144">-Tag</span></span>

<span data-ttu-id="bfdca-145">Возвращает ресурсы с указанным тегом Azure.</span><span class="sxs-lookup"><span data-stu-id="bfdca-145">Gets resources that have the specified Azure tag.</span></span> <span data-ttu-id="bfdca-146">Введите хэш-таблицу с ключом имени или именем и ключом.</span><span class="sxs-lookup"><span data-stu-id="bfdca-146">Enter a hash table with a Name key or Name and Value keys.</span></span> <span data-ttu-id="bfdca-147">Подстановочные знаки не поддерживаются. "Тег" — это пара "имя-значение", которую можно применять к ресурсам и группам ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bfdca-147">Wildcard characters are not supported.A "tag" is a name-value pair that you can apply to resources and resource groups.</span></span> <span data-ttu-id="bfdca-148">Используйте теги для классификации ресурсов, таких как отдел или центр затрат, а также для отслеживания заметок и примечаний к ресурсам.</span><span class="sxs-lookup"><span data-stu-id="bfdca-148">Use tags to categorize your resources, such as by department or cost center, or to track notes or comments about the resources.</span></span> <span data-ttu-id="bfdca-149">Чтобы добавить тег к ресурсу, используйте параметр tag командлетов New-AzResource или Set-AzResource.</span><span class="sxs-lookup"><span data-stu-id="bfdca-149">To add a tag to a resource, use the Tag parameter of the New-AzResource or Set-AzResource cmdlets.</span></span> <span data-ttu-id="bfdca-150">Чтобы создать предопределенный тег, используйте командлет New-AzTag.</span><span class="sxs-lookup"><span data-stu-id="bfdca-150">To create a predefined tag, use the New-AzTag cmdlet.</span></span> <span data-ttu-id="bfdca-151">Чтобы получить справку по хэш-таблицам в Windows PowerShell, выполните "Get-Help about_Hashtables".</span><span class="sxs-lookup"><span data-stu-id="bfdca-151">For help with hash tables in Windows PowerShell, run 'Get-Help about_Hashtables'.</span></span>

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

### <span data-ttu-id="bfdca-152">-TagName</span><span class="sxs-lookup"><span data-stu-id="bfdca-152">-TagName</span></span>
<span data-ttu-id="bfdca-153">Ключ тега для извлекаемых ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bfdca-153">The key in the tag of the resource(s) to be retrieved.</span></span>

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

### <span data-ttu-id="bfdca-154">-TagValue</span><span class="sxs-lookup"><span data-stu-id="bfdca-154">-TagValue</span></span>
<span data-ttu-id="bfdca-155">Значение в теге извлекаемого ресурса.</span><span class="sxs-lookup"><span data-stu-id="bfdca-155">The value in the tag of the resource(s) to be retrieved.</span></span>

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

### <span data-ttu-id="bfdca-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfdca-156">CommonParameters</span></span>
<span data-ttu-id="bfdca-157">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bfdca-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfdca-158">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bfdca-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfdca-159">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bfdca-159">INPUTS</span></span>

### <span data-ttu-id="bfdca-160">System. String</span><span class="sxs-lookup"><span data-stu-id="bfdca-160">System.String</span></span>

## <span data-ttu-id="bfdca-161">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bfdca-161">OUTPUTS</span></span>

### <span data-ttu-id="bfdca-162">Microsoft. Azure. Commands. ResourceManager. командлеты. SdkModels. PSResource</span><span class="sxs-lookup"><span data-stu-id="bfdca-162">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResource</span></span>

## <span data-ttu-id="bfdca-163">Пуск</span><span class="sxs-lookup"><span data-stu-id="bfdca-163">NOTES</span></span>

## <span data-ttu-id="bfdca-164">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bfdca-164">RELATED LINKS</span></span>

[<span data-ttu-id="bfdca-165">Move-AzResource</span><span class="sxs-lookup"><span data-stu-id="bfdca-165">Move-AzResource</span></span>](./Move-AzResource.md)

[<span data-ttu-id="bfdca-166">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="bfdca-166">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="bfdca-167">Remove-AzResource</span><span class="sxs-lookup"><span data-stu-id="bfdca-167">Remove-AzResource</span></span>](./Remove-AzResource.md)

[<span data-ttu-id="bfdca-168">Set-AzResource</span><span class="sxs-lookup"><span data-stu-id="bfdca-168">Set-AzResource</span></span>](./Set-AzResource.md)
