---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 5B17A241-BF36-48A6-BC29-4C32C08F5F94
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceGroup.md
ms.openlocfilehash: 0963d439efd4ab65a2117773cb6b7bb97043972c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733333"
---
# <span data-ttu-id="68d66-101">Get-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="68d66-101">Get-AzureRmResourceGroup</span></span>

## <span data-ttu-id="68d66-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="68d66-102">SYNOPSIS</span></span>
<span data-ttu-id="68d66-103">Возвращает группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="68d66-103">Gets resource groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="68d66-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="68d66-104">SYNTAX</span></span>

### <span data-ttu-id="68d66-105">Отображает группу ресурсов на основе имени.</span><span class="sxs-lookup"><span data-stu-id="68d66-105">Lists the resource group based on the name.</span></span> <span data-ttu-id="68d66-106">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="68d66-106">(Default)</span></span>
```
Get-AzureRmResourceGroup [-Name <String>] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="68d66-107">Выводит группу ресурсов на основе идентификатора.</span><span class="sxs-lookup"><span data-stu-id="68d66-107">Lists the resource group based on the Id.</span></span>
```
Get-AzureRmResourceGroup [-Location <String>] [-Id <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="68d66-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="68d66-108">DESCRIPTION</span></span>
<span data-ttu-id="68d66-109">Командлет **Get-AzureRmResourceGroup** получает группы ресурсов Azure в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="68d66-109">The **Get-AzureRmResourceGroup** cmdlet gets Azure resource groups in the current subscription.</span></span>
<span data-ttu-id="68d66-110">Вы можете получить доступ ко всем группам ресурсов или указать группу ресурсов по имени или по другим параметрам.</span><span class="sxs-lookup"><span data-stu-id="68d66-110">You can get all resource groups, or specify a resource group by name or by other properties.</span></span>
<span data-ttu-id="68d66-111">По умолчанию этот командлет получает все группы ресурсов в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="68d66-111">By default, this cmdlet gets all resource groups in the current subscription.</span></span>

<span data-ttu-id="68d66-112">Дополнительные сведения о ресурсах Azure и группах ресурсов Azure можно найти в командлете New-AzureRmResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="68d66-112">For more information about Azure resources and Azure resource groups, see the New-AzureRmResourceGroup cmdlet.</span></span>

## <span data-ttu-id="68d66-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="68d66-113">EXAMPLES</span></span>

### <span data-ttu-id="68d66-114">Пример 1: получение группы ресурсов по имени</span><span class="sxs-lookup"><span data-stu-id="68d66-114">Example 1: Get a resource group by name</span></span>
```
PS C:\>Get-AzureRmResourceGroup -Name "EngineerBlog"
```

<span data-ttu-id="68d66-115">Эта команда получает группу ресурсов Azure в подписке с именем EngineerBlog.</span><span class="sxs-lookup"><span data-stu-id="68d66-115">This command gets the Azure resource group in your subscription named EngineerBlog.</span></span>

### <span data-ttu-id="68d66-116">Пример 2: получение всех тегов в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="68d66-116">Example 2: Get all tags of a resource group</span></span>
```
PS C:\>(Get-AzureRmResourceGroup -Name "ContosoRG").Tags
```

<span data-ttu-id="68d66-117">Эта команда получает группу ресурсов с именем ContosoRG и отображает теги, связанные с этой группой.</span><span class="sxs-lookup"><span data-stu-id="68d66-117">This command gets the resource group named ContosoRG, and displays the tags associated with that group.</span></span>

## <span data-ttu-id="68d66-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="68d66-118">PARAMETERS</span></span>

### <span data-ttu-id="68d66-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="68d66-119">-ApiVersion</span></span>
<span data-ttu-id="68d66-120">Указывает версию API, поддерживаемую поставщиком ресурсов.</span><span class="sxs-lookup"><span data-stu-id="68d66-120">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="68d66-121">Вы можете выбрать версию, отличную от версии по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="68d66-121">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="68d66-122">-ID</span><span class="sxs-lookup"><span data-stu-id="68d66-122">-Id</span></span>
<span data-ttu-id="68d66-123">Указывает идентификатор получаемой группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="68d66-123">Specifies the ID of the resource group to get.</span></span>
<span data-ttu-id="68d66-124">Подстановочные знаки не разрешены.</span><span class="sxs-lookup"><span data-stu-id="68d66-124">Wildcard characters are not permitted.</span></span>

```yaml
Type: System.String
Parameter Sets: Lists the resource group based on the Id.
Aliases: ResourceGroupId, ResourceId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68d66-125">-Location</span><span class="sxs-lookup"><span data-stu-id="68d66-125">-Location</span></span>
<span data-ttu-id="68d66-126">Указывает расположение группы ресурсов, которую нужно получить.</span><span class="sxs-lookup"><span data-stu-id="68d66-126">Specifies the location of the resource group to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68d66-127">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="68d66-127">-Name</span></span>
<span data-ttu-id="68d66-128">Указывает имя группы ресурсов, которую требуется получить.</span><span class="sxs-lookup"><span data-stu-id="68d66-128">Specifies the name of the resource group to get.</span></span>
<span data-ttu-id="68d66-129">Подстановочные знаки не разрешены.</span><span class="sxs-lookup"><span data-stu-id="68d66-129">Wildcard characters are not permitted.</span></span>

```yaml
Type: System.String
Parameter Sets: Lists the resource group based on the name.
Aliases: ResourceGroupName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68d66-130">-Pre</span><span class="sxs-lookup"><span data-stu-id="68d66-130">-Pre</span></span>
<span data-ttu-id="68d66-131">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="68d66-131">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="68d66-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68d66-132">-DefaultProfile</span></span>
<span data-ttu-id="68d66-133">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="68d66-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68d66-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68d66-134">CommonParameters</span></span>
<span data-ttu-id="68d66-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="68d66-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68d66-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68d66-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68d66-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="68d66-137">INPUTS</span></span>

### <span data-ttu-id="68d66-138">Подстрок</span><span class="sxs-lookup"><span data-stu-id="68d66-138">String</span></span>
<span data-ttu-id="68d66-139">Вы можете передать входные данные командлету по имени свойства, но не по значению.</span><span class="sxs-lookup"><span data-stu-id="68d66-139">You can pipe input to the cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="68d66-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="68d66-140">OUTPUTS</span></span>

### <span data-ttu-id="68d66-141">Microsoft. Azure. Commands. ResourceManagement. PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="68d66-141">Microsoft.Azure.Commands.ResourceManagement.PSResourceGroup</span></span>
<span data-ttu-id="68d66-142">Этот командлет возвращает группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="68d66-142">This cmdlet returns resource groups.</span></span>

## <span data-ttu-id="68d66-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="68d66-143">NOTES</span></span>

## <span data-ttu-id="68d66-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="68d66-144">RELATED LINKS</span></span>

[<span data-ttu-id="68d66-145">New-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="68d66-145">New-AzureRmResourceGroup</span></span>](./New-AzureRmResourceGroup.md)

[<span data-ttu-id="68d66-146">Remove-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="68d66-146">Remove-AzureRmResourceGroup</span></span>](./Remove-AzureRmResourceGroup.md)

[<span data-ttu-id="68d66-147">Set-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="68d66-147">Set-AzureRmResourceGroup</span></span>](./Set-AzureRmResourceGroup.md)


