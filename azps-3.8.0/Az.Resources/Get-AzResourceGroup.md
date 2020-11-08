---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 5B17A241-BF36-48A6-BC29-4C32C08F5F94
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroup.md
ms.openlocfilehash: dc619aacd4089ce854eb5d342c2308a38a60cb28
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073916"
---
# <span data-ttu-id="66691-101">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="66691-101">Get-AzResourceGroup</span></span>

## <span data-ttu-id="66691-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="66691-102">SYNOPSIS</span></span>
<span data-ttu-id="66691-103">Возвращает группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="66691-103">Gets resource groups.</span></span>

## <span data-ttu-id="66691-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="66691-104">SYNTAX</span></span>

### <span data-ttu-id="66691-105">GetByResourceGroupName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="66691-105">GetByResourceGroupName (Default)</span></span>
```
Get-AzResourceGroup [[-Name] <String>] [[-Location] <String>] [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="66691-106">GetByResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="66691-106">GetByResourceGroupId</span></span>
```
Get-AzResourceGroup [[-Location] <String>] [-Id <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="66691-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="66691-107">DESCRIPTION</span></span>
<span data-ttu-id="66691-108">Командлет **Get-AzResourceGroup** получает группы ресурсов Azure в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="66691-108">The **Get-AzResourceGroup** cmdlet gets Azure resource groups in the current subscription.</span></span>
<span data-ttu-id="66691-109">Вы можете получить доступ ко всем группам ресурсов или указать группу ресурсов по имени или по другим параметрам.</span><span class="sxs-lookup"><span data-stu-id="66691-109">You can get all resource groups, or specify a resource group by name or by other properties.</span></span>
<span data-ttu-id="66691-110">По умолчанию этот командлет получает все группы ресурсов в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="66691-110">By default, this cmdlet gets all resource groups in the current subscription.</span></span>
<span data-ttu-id="66691-111">Дополнительные сведения о ресурсах Azure и группах ресурсов Azure можно найти в командлете New-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="66691-111">For more information about Azure resources and Azure resource groups, see the New-AzResourceGroup cmdlet.</span></span>

## <span data-ttu-id="66691-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="66691-112">EXAMPLES</span></span>

### <span data-ttu-id="66691-113">Пример 1: получение группы ресурсов по имени</span><span class="sxs-lookup"><span data-stu-id="66691-113">Example 1: Get a resource group by name</span></span>
```
PS C:\>Get-AzResourceGroup -Name "EngineerBlog"
```

<span data-ttu-id="66691-114">Эта команда получает группу ресурсов Azure в подписке с именем EngineerBlog.</span><span class="sxs-lookup"><span data-stu-id="66691-114">This command gets the Azure resource group in your subscription named EngineerBlog.</span></span>

### <span data-ttu-id="66691-115">Пример 2: получение всех тегов в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="66691-115">Example 2: Get all tags of a resource group</span></span>
```
PS C:\>(Get-AzResourceGroup -Name "ContosoRG").Tags
```

<span data-ttu-id="66691-116">Эта команда получает группу ресурсов с именем ContosoRG и отображает теги, связанные с этой группой.</span><span class="sxs-lookup"><span data-stu-id="66691-116">This command gets the resource group named ContosoRG, and displays the tags associated with that group.</span></span>

### <span data-ttu-id="66691-117">Пример 3: отображение групп ресурсов по расположению</span><span class="sxs-lookup"><span data-stu-id="66691-117">Example 3: Show the Resource groups by location</span></span>
```
PS C:\> Get-AzResourceGroup |
  Sort Location,ResourceGroupName |
  Format-Table -GroupBy Location ResourceGroupName,ProvisioningState,Tags
```

### <span data-ttu-id="66691-118">Пример 4: Отображение имен всех групп ресурсов в определенном расположении</span><span class="sxs-lookup"><span data-stu-id="66691-118">Example 4: Show the names of all the Resource groups in a particular location</span></span>
```
PS C:\> Get-AzResourceGroup -Location westus2 |
   Sort ResourceGroupName | 
   Format-Wide ResourceGroupName -Column 4
```

### <span data-ttu-id="66691-119">Пример 5: отображение групп ресурсов, имена которых начинаются с сервера</span><span class="sxs-lookup"><span data-stu-id="66691-119">Example 5: Show the Resource groups whose names begin with WebServer</span></span>
```
PS C:\> Get-AzResourceGroup | Where ResourceGroupName -like WebServer*
```

### <span data-ttu-id="66691-120">Пример 6: получение группы ресурсов по имени</span><span class="sxs-lookup"><span data-stu-id="66691-120">Example 6: Get a resource group by name</span></span>
```
PS C:\> Get-AzResourceGroup -Name "EngineerBlog*"
```

<span data-ttu-id="66691-121">Эта команда получает группу ресурсов Azure в подписке, которая начинается с "EngineerBlog".</span><span class="sxs-lookup"><span data-stu-id="66691-121">This command gets the Azure resource group in your subscription that start with "EngineerBlog".</span></span>

## <span data-ttu-id="66691-122">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="66691-122">PARAMETERS</span></span>

### <span data-ttu-id="66691-123">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="66691-123">-ApiVersion</span></span>
<span data-ttu-id="66691-124">Указывает версию API, поддерживаемую поставщиком ресурсов.</span><span class="sxs-lookup"><span data-stu-id="66691-124">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="66691-125">Вы можете выбрать версию, отличную от версии по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="66691-125">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="66691-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66691-126">-DefaultProfile</span></span>
<span data-ttu-id="66691-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="66691-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="66691-128">-ID</span><span class="sxs-lookup"><span data-stu-id="66691-128">-Id</span></span>
<span data-ttu-id="66691-129">Указывает идентификатор получаемой группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="66691-129">Specifies the ID of the resource group to get.</span></span>
<span data-ttu-id="66691-130">Подстановочные знаки не разрешены.</span><span class="sxs-lookup"><span data-stu-id="66691-130">Wildcard characters are not permitted.</span></span>

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

### <span data-ttu-id="66691-131">-Location</span><span class="sxs-lookup"><span data-stu-id="66691-131">-Location</span></span>
<span data-ttu-id="66691-132">Указывает расположение группы ресурсов, которую нужно получить.</span><span class="sxs-lookup"><span data-stu-id="66691-132">Specifies the location of the resource group to get.</span></span>

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

### <span data-ttu-id="66691-133">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="66691-133">-Name</span></span>
<span data-ttu-id="66691-134">Указывает имя группы ресурсов, которую требуется получить.</span><span class="sxs-lookup"><span data-stu-id="66691-134">Specifies the name of the resource group to get.</span></span> <span data-ttu-id="66691-135">Этот параметр поддерживает подстановочные знаки в начале и (или) конце строки.</span><span class="sxs-lookup"><span data-stu-id="66691-135">This parameter supports wildcards at the beginning and/or the end of the string.</span></span>

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

### <span data-ttu-id="66691-136">-Pre</span><span class="sxs-lookup"><span data-stu-id="66691-136">-Pre</span></span>
<span data-ttu-id="66691-137">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="66691-137">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="66691-138">-Тег</span><span class="sxs-lookup"><span data-stu-id="66691-138">-Tag</span></span>
<span data-ttu-id="66691-139">Хэш-таблица тегов, по которой нужно отфильтровать группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="66691-139">The tag hashtable to filter resource groups by.</span></span>

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

### <span data-ttu-id="66691-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66691-140">CommonParameters</span></span>
<span data-ttu-id="66691-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="66691-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66691-142">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="66691-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66691-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="66691-143">INPUTS</span></span>

### <span data-ttu-id="66691-144">System. String</span><span class="sxs-lookup"><span data-stu-id="66691-144">System.String</span></span>

### <span data-ttu-id="66691-145">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="66691-145">System.Collections.Hashtable</span></span>

## <span data-ttu-id="66691-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="66691-146">OUTPUTS</span></span>

### <span data-ttu-id="66691-147">Microsoft. Azure. Commands. ResourceManager. командлеты. SdkModels. PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="66691-147">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroup</span></span>

## <span data-ttu-id="66691-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="66691-148">NOTES</span></span>

## <span data-ttu-id="66691-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="66691-149">RELATED LINKS</span></span>

[<span data-ttu-id="66691-150">New-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="66691-150">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="66691-151">Remove-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="66691-151">Remove-AzResourceGroup</span></span>](./Remove-AzResourceGroup.md)

[<span data-ttu-id="66691-152">Set-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="66691-152">Set-AzResourceGroup</span></span>](./Set-AzResourceGroup.md)


