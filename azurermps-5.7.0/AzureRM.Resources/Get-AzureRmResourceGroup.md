---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 5B17A241-BF36-48A6-BC29-4C32C08F5F94
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceGroup.md
ms.openlocfilehash: f3924115d68d7e844503e076a214c95bf3d2239d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567947"
---
# <span data-ttu-id="311da-101">Get-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="311da-101">Get-AzureRmResourceGroup</span></span>

## <span data-ttu-id="311da-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="311da-102">SYNOPSIS</span></span>
<span data-ttu-id="311da-103">Возвращает группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="311da-103">Gets resource groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="311da-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="311da-104">SYNTAX</span></span>

### <span data-ttu-id="311da-105">GetByResourceGroupName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="311da-105">GetByResourceGroupName (Default)</span></span>
```
Get-AzureRmResourceGroup [-Name <String>] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="311da-106">GetByResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="311da-106">GetByResourceGroupId</span></span>
```
Get-AzureRmResourceGroup [-Location <String>] [-Id <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="311da-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="311da-107">DESCRIPTION</span></span>
<span data-ttu-id="311da-108">Командлет **Get-AzureRmResourceGroup** получает группы ресурсов Azure в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="311da-108">The **Get-AzureRmResourceGroup** cmdlet gets Azure resource groups in the current subscription.</span></span>
<span data-ttu-id="311da-109">Вы можете получить доступ ко всем группам ресурсов или указать группу ресурсов по имени или по другим параметрам.</span><span class="sxs-lookup"><span data-stu-id="311da-109">You can get all resource groups, or specify a resource group by name or by other properties.</span></span>
<span data-ttu-id="311da-110">По умолчанию этот командлет получает все группы ресурсов в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="311da-110">By default, this cmdlet gets all resource groups in the current subscription.</span></span>

<span data-ttu-id="311da-111">Дополнительные сведения о ресурсах Azure и группах ресурсов Azure можно найти в командлете New-AzureRmResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="311da-111">For more information about Azure resources and Azure resource groups, see the New-AzureRmResourceGroup cmdlet.</span></span>

## <span data-ttu-id="311da-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="311da-112">EXAMPLES</span></span>

### <span data-ttu-id="311da-113">Пример 1: получение группы ресурсов по имени</span><span class="sxs-lookup"><span data-stu-id="311da-113">Example 1: Get a resource group by name</span></span>
```
PS C:\>Get-AzureRmResourceGroup -Name "EngineerBlog"
```

<span data-ttu-id="311da-114">Эта команда получает группу ресурсов Azure в подписке с именем EngineerBlog.</span><span class="sxs-lookup"><span data-stu-id="311da-114">This command gets the Azure resource group in your subscription named EngineerBlog.</span></span>

### <span data-ttu-id="311da-115">Пример 2: получение всех тегов в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="311da-115">Example 2: Get all tags of a resource group</span></span>
```
PS C:\>(Get-AzureRmResourceGroup -Name "ContosoRG").Tags
```

<span data-ttu-id="311da-116">Эта команда получает группу ресурсов с именем ContosoRG и отображает теги, связанные с этой группой.</span><span class="sxs-lookup"><span data-stu-id="311da-116">This command gets the resource group named ContosoRG, and displays the tags associated with that group.</span></span>

### <span data-ttu-id="311da-117">Пример 3: отображение групп ресурсов по расположению</span><span class="sxs-lookup"><span data-stu-id="311da-117">Example 3: Show the Resource groups by location</span></span>
```
PS C:\> Get-AzureRmResourceGroup |
  Sort Location,ResourceGroupName |
  Format-Table -GroupBy Location ResourceGroupName,ProvisioningState,Tags
```

### <span data-ttu-id="311da-118">Пример 4: Отображение имен всех групп ресурсов в определенном расположении</span><span class="sxs-lookup"><span data-stu-id="311da-118">Example 4: Show the names of all the Resource groups in a particular location</span></span>
```
PS C:\> Get-AzureRmResourceGroup -Location westus2 |
   Sort ResourceGroupName | 
   Format-Wide ResourceGroupName -Column 4
```

### <span data-ttu-id="311da-119">Пример 5: отображение групп ресурсов, имена которых начинаются с сервера</span><span class="sxs-lookup"><span data-stu-id="311da-119">Example 5: Show the Resource groups whose names begin with WebServer</span></span>
```
PS C:\> Get-AzureRmResourceGroup | Where ResourceGroupName -like WebServer*
```

## <span data-ttu-id="311da-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="311da-120">PARAMETERS</span></span>

### <span data-ttu-id="311da-121">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="311da-121">-ApiVersion</span></span>
<span data-ttu-id="311da-122">Указывает версию API, поддерживаемую поставщиком ресурсов.</span><span class="sxs-lookup"><span data-stu-id="311da-122">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="311da-123">Вы можете выбрать версию, отличную от версии по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="311da-123">You can specify a different version than the default version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="311da-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="311da-124">-DefaultProfile</span></span>
<span data-ttu-id="311da-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="311da-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="311da-126">-ID</span><span class="sxs-lookup"><span data-stu-id="311da-126">-Id</span></span>
<span data-ttu-id="311da-127">Указывает идентификатор получаемой группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="311da-127">Specifies the ID of the resource group to get.</span></span>
<span data-ttu-id="311da-128">Подстановочные знаки не разрешены.</span><span class="sxs-lookup"><span data-stu-id="311da-128">Wildcard characters are not permitted.</span></span>

```yaml
Type: String
Parameter Sets: GetByResourceGroupId
Aliases: ResourceGroupId, ResourceId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="311da-129">-Location</span><span class="sxs-lookup"><span data-stu-id="311da-129">-Location</span></span>
<span data-ttu-id="311da-130">Указывает расположение группы ресурсов, которую нужно получить.</span><span class="sxs-lookup"><span data-stu-id="311da-130">Specifies the location of the resource group to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="311da-131">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="311da-131">-Name</span></span>
<span data-ttu-id="311da-132">Указывает имя группы ресурсов, которую требуется получить.</span><span class="sxs-lookup"><span data-stu-id="311da-132">Specifies the name of the resource group to get.</span></span>
<span data-ttu-id="311da-133">Подстановочные знаки не разрешены.</span><span class="sxs-lookup"><span data-stu-id="311da-133">Wildcard characters are not permitted.</span></span>

```yaml
Type: String
Parameter Sets: GetByResourceGroupName
Aliases: ResourceGroupName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="311da-134">-Pre</span><span class="sxs-lookup"><span data-stu-id="311da-134">-Pre</span></span>
<span data-ttu-id="311da-135">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="311da-135">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="311da-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="311da-136">CommonParameters</span></span>
<span data-ttu-id="311da-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="311da-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="311da-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="311da-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="311da-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="311da-139">INPUTS</span></span>

### <span data-ttu-id="311da-140">Подстрок</span><span class="sxs-lookup"><span data-stu-id="311da-140">String</span></span>
<span data-ttu-id="311da-141">Вы можете передать входные данные командлету по имени свойства, но не по значению.</span><span class="sxs-lookup"><span data-stu-id="311da-141">You can pipe input to the cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="311da-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="311da-142">OUTPUTS</span></span>

### <span data-ttu-id="311da-143">Microsoft. Azure. Commands. ResourceManagement. PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="311da-143">Microsoft.Azure.Commands.ResourceManagement.PSResourceGroup</span></span>
<span data-ttu-id="311da-144">Этот командлет возвращает группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="311da-144">This cmdlet returns resource groups.</span></span>

## <span data-ttu-id="311da-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="311da-145">NOTES</span></span>

## <span data-ttu-id="311da-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="311da-146">RELATED LINKS</span></span>

[<span data-ttu-id="311da-147">New-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="311da-147">New-AzureRmResourceGroup</span></span>](./New-AzureRmResourceGroup.md)

[<span data-ttu-id="311da-148">Remove-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="311da-148">Remove-AzureRmResourceGroup</span></span>](./Remove-AzureRmResourceGroup.md)

[<span data-ttu-id="311da-149">Set-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="311da-149">Set-AzureRmResourceGroup</span></span>](./Set-AzureRmResourceGroup.md)


