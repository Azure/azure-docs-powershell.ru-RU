---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 5B17A241-BF36-48A6-BC29-4C32C08F5F94
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroup.md
ms.openlocfilehash: b8e74a0c349ea058d05ef044648e836fddc1f7b3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236416"
---
# <span data-ttu-id="8e107-101">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8e107-101">Get-AzResourceGroup</span></span>

## <span data-ttu-id="8e107-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8e107-102">SYNOPSIS</span></span>
<span data-ttu-id="8e107-103">Возвращает группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8e107-103">Gets resource groups.</span></span>

## <span data-ttu-id="8e107-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8e107-104">SYNTAX</span></span>

### <span data-ttu-id="8e107-105">GetByResourceGroupName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8e107-105">GetByResourceGroupName (Default)</span></span>
```
Get-AzResourceGroup [[-Name] <String>] [[-Location] <String>] [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8e107-106">GetByResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="8e107-106">GetByResourceGroupId</span></span>
```
Get-AzResourceGroup [[-Location] <String>] [-Id <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8e107-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8e107-107">DESCRIPTION</span></span>
<span data-ttu-id="8e107-108">Командлет **Get-AzResourceGroup** получает группы ресурсов Azure в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="8e107-108">The **Get-AzResourceGroup** cmdlet gets Azure resource groups in the current subscription.</span></span>
<span data-ttu-id="8e107-109">Вы можете получить доступ ко всем группам ресурсов или указать группу ресурсов по имени или по другим параметрам.</span><span class="sxs-lookup"><span data-stu-id="8e107-109">You can get all resource groups, or specify a resource group by name or by other properties.</span></span>
<span data-ttu-id="8e107-110">По умолчанию этот командлет получает все группы ресурсов в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="8e107-110">By default, this cmdlet gets all resource groups in the current subscription.</span></span>
<span data-ttu-id="8e107-111">Дополнительные сведения о ресурсах Azure и группах ресурсов Azure можно найти в командлете New-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="8e107-111">For more information about Azure resources and Azure resource groups, see the New-AzResourceGroup cmdlet.</span></span>

## <span data-ttu-id="8e107-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8e107-112">EXAMPLES</span></span>

### <span data-ttu-id="8e107-113">Пример 1: получение группы ресурсов по имени</span><span class="sxs-lookup"><span data-stu-id="8e107-113">Example 1: Get a resource group by name</span></span>
```
PS C:\> Get-AzResourceGroup -Name "EngineerBlog"
```

<span data-ttu-id="8e107-114">Эта команда получает группу ресурсов Azure в подписке с именем EngineerBlog.</span><span class="sxs-lookup"><span data-stu-id="8e107-114">This command gets the Azure resource group in your subscription named EngineerBlog.</span></span>

### <span data-ttu-id="8e107-115">Пример 2: получение всех тегов в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="8e107-115">Example 2: Get all tags of a resource group</span></span>
```
PS C:\> (Get-AzResourceGroup -Name "ContosoRG").Tags
```

<span data-ttu-id="8e107-116">Эта команда получает группу ресурсов с именем ContosoRG и отображает теги, связанные с этой группой.</span><span class="sxs-lookup"><span data-stu-id="8e107-116">This command gets the resource group named ContosoRG, and displays the tags associated with that group.</span></span>

### <span data-ttu-id="8e107-117">Пример 3: получение групп ресурсов на основе тега</span><span class="sxs-lookup"><span data-stu-id="8e107-117">Example 3: Get resource groups based on tag</span></span>
```
PS C:\> Get-AzResourceGroup -Tag @{'environment'='prod'}
```

### <span data-ttu-id="8e107-118">Пример 4: отображение групп ресурсов по расположению</span><span class="sxs-lookup"><span data-stu-id="8e107-118">Example 4: Show the Resource groups by location</span></span>
```
PS C:\> Get-AzResourceGroup |
  Sort Location,ResourceGroupName |
  Format-Table -GroupBy Location ResourceGroupName,ProvisioningState,Tags
```

### <span data-ttu-id="8e107-119">Пример 5: Отображение имен всех групп ресурсов в определенном расположении</span><span class="sxs-lookup"><span data-stu-id="8e107-119">Example 5: Show the names of all the Resource groups in a particular location</span></span>
```
PS C:\> Get-AzResourceGroup -Location westus2 |
   Sort ResourceGroupName | 
   Format-Wide ResourceGroupName -Column 4
```

### <span data-ttu-id="8e107-120">Пример 6: отображение групп ресурсов, имена которых начинаются с сервера</span><span class="sxs-lookup"><span data-stu-id="8e107-120">Example 6: Show the Resource groups whose names begin with WebServer</span></span>
```
PS C:\> Get-AzResourceGroup -Name WebServer*
```

## <span data-ttu-id="8e107-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8e107-121">PARAMETERS</span></span>

### <span data-ttu-id="8e107-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="8e107-122">-ApiVersion</span></span>
<span data-ttu-id="8e107-123">Указывает версию API, поддерживаемую поставщиком ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8e107-123">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="8e107-124">Вы можете выбрать версию, отличную от версии по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8e107-124">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="8e107-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e107-125">-DefaultProfile</span></span>
<span data-ttu-id="8e107-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="8e107-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8e107-127">-ID</span><span class="sxs-lookup"><span data-stu-id="8e107-127">-Id</span></span>
<span data-ttu-id="8e107-128">Указывает идентификатор получаемой группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8e107-128">Specifies the ID of the resource group to get.</span></span>
<span data-ttu-id="8e107-129">Подстановочные знаки не разрешены.</span><span class="sxs-lookup"><span data-stu-id="8e107-129">Wildcard characters are not permitted.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupId
Aliases: ResourceGroupId, ResourceId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e107-130">-Location</span><span class="sxs-lookup"><span data-stu-id="8e107-130">-Location</span></span>
<span data-ttu-id="8e107-131">Указывает расположение группы ресурсов, которую нужно получить.</span><span class="sxs-lookup"><span data-stu-id="8e107-131">Specifies the location of the resource group to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e107-132">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8e107-132">-Name</span></span>
<span data-ttu-id="8e107-133">Указывает имя группы ресурсов, которую требуется получить.</span><span class="sxs-lookup"><span data-stu-id="8e107-133">Specifies the name of the resource group to get.</span></span> <span data-ttu-id="8e107-134">Этот параметр поддерживает подстановочные знаки в начале и (или) конце строки.</span><span class="sxs-lookup"><span data-stu-id="8e107-134">This parameter supports wildcards at the beginning and/or the end of the string.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupName
Aliases: ResourceGroupName

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="8e107-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="8e107-135">-Pre</span></span>
<span data-ttu-id="8e107-136">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="8e107-136">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="8e107-137">-Тег</span><span class="sxs-lookup"><span data-stu-id="8e107-137">-Tag</span></span>
<span data-ttu-id="8e107-138">Хэш-таблица тегов, по которой нужно отфильтровать группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8e107-138">The tag hashtable to filter resource groups by.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: GetByResourceGroupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e107-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e107-139">CommonParameters</span></span>
<span data-ttu-id="8e107-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8e107-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e107-141">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8e107-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e107-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8e107-142">INPUTS</span></span>

### <span data-ttu-id="8e107-143">System. String</span><span class="sxs-lookup"><span data-stu-id="8e107-143">System.String</span></span>

### <span data-ttu-id="8e107-144">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="8e107-144">System.Collections.Hashtable</span></span>

## <span data-ttu-id="8e107-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8e107-145">OUTPUTS</span></span>

### <span data-ttu-id="8e107-146">Microsoft. Azure. Commands. ResourceManager. командлеты. SdkModels. PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8e107-146">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroup</span></span>

## <span data-ttu-id="8e107-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="8e107-147">NOTES</span></span>

## <span data-ttu-id="8e107-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8e107-148">RELATED LINKS</span></span>

[<span data-ttu-id="8e107-149">New-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8e107-149">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="8e107-150">Remove-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8e107-150">Remove-AzResourceGroup</span></span>](./Remove-AzResourceGroup.md)

[<span data-ttu-id="8e107-151">Set-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8e107-151">Set-AzResourceGroup</span></span>](./Set-AzResourceGroup.md)


