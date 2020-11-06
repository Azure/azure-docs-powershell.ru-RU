---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 60BED40A-EEA4-4667-93E9-8A9B35037726
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/move-azurermresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Move-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Move-AzureRmResource.md
ms.openlocfilehash: 4562c217a771f53995a531a3ca72066da672a144
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566914"
---
# <span data-ttu-id="dd569-101">Move-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="dd569-101">Move-AzureRmResource</span></span>

## <span data-ttu-id="dd569-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dd569-102">SYNOPSIS</span></span>
<span data-ttu-id="dd569-103">Перемещает ресурс в другую группу ресурсов или подписку.</span><span class="sxs-lookup"><span data-stu-id="dd569-103">Moves a resource to a different resource group or subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dd569-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dd569-104">SYNTAX</span></span>

```
Move-AzureRmResource -DestinationResourceGroupName <String> [-DestinationSubscriptionId <Guid>]
 -ResourceId <String[]> [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dd569-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dd569-105">DESCRIPTION</span></span>
<span data-ttu-id="dd569-106">Командлет **Move-AzureRmResource** перемещает существующие ресурсы в другую группу ресурсов.</span><span class="sxs-lookup"><span data-stu-id="dd569-106">The **Move-AzureRmResource** cmdlet moves existing resources to a different resource group.</span></span>
<span data-ttu-id="dd569-107">Эта группа ресурсов может входить в другую подписку.</span><span class="sxs-lookup"><span data-stu-id="dd569-107">That resource group can be in a different subscription.</span></span>

## <span data-ttu-id="dd569-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dd569-108">EXAMPLES</span></span>

### <span data-ttu-id="dd569-109">Пример 1: перемещение ресурса в группу ресурсов</span><span class="sxs-lookup"><span data-stu-id="dd569-109">Example 1: Move a resource to a resource group</span></span>
```
PS C:\>$Resource = Get-AzureRmResource -ResourceType "Microsoft.ClassicCompute/storageAccounts" -ResourceName "ContosoStorageAccount"
PS C:\> Move-AzureRmResource -ResourceId $Resource.ResourceId -DestinationResourceGroupName "ResourceGroup14"
```

<span data-ttu-id="dd569-110">Первая команда получает ресурс с именем ContosoStorageAccount с помощью командлета Get-AzureRmResource и сохраняет этот ресурс в переменной $Resource.</span><span class="sxs-lookup"><span data-stu-id="dd569-110">The first command gets a resource named ContosoStorageAccount by using the Get-AzureRmResource cmdlet, and then stores that resource in the $Resource variable.</span></span>

<span data-ttu-id="dd569-111">Вторая команда перемещает этот ресурс в группу ресурсов с именем ResourceGroup14.</span><span class="sxs-lookup"><span data-stu-id="dd569-111">The second command moves that resource into the resource group named ResourceGroup14.</span></span>
<span data-ttu-id="dd569-112">Команда определяет ресурс для перемещения с помощью свойства **ResourceId** для $Resource.</span><span class="sxs-lookup"><span data-stu-id="dd569-112">The command identifies the resource to move by using the **ResourceId** property of $Resource.</span></span>

## <span data-ttu-id="dd569-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dd569-113">PARAMETERS</span></span>

### <span data-ttu-id="dd569-114">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="dd569-114">-ApiVersion</span></span>
<span data-ttu-id="dd569-115">Указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="dd569-115">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="dd569-116">Если вы не укажете версию, этот командлет использует последнюю доступную версию.</span><span class="sxs-lookup"><span data-stu-id="dd569-116">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="dd569-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd569-117">-DefaultProfile</span></span>
<span data-ttu-id="dd569-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="dd569-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dd569-119">-DestinationResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd569-119">-DestinationResourceGroupName</span></span>
<span data-ttu-id="dd569-120">Указывает имя группы ресурсов, в которую этот командлет перемещает ресурсы.</span><span class="sxs-lookup"><span data-stu-id="dd569-120">Specifies the name of the resource group into which this cmdlet moves resources.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: TargetResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd569-121">-DestinationSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="dd569-121">-DestinationSubscriptionId</span></span>
<span data-ttu-id="dd569-122">Указывает идентификатор подписки, в которую этот командлет перемещает ресурсы.</span><span class="sxs-lookup"><span data-stu-id="dd569-122">Specifies the ID of the subscription into which this cmdlet moves resources .</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: Id, SubscriptionId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd569-123">-Force</span><span class="sxs-lookup"><span data-stu-id="dd569-123">-Force</span></span>
<span data-ttu-id="dd569-124">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="dd569-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="dd569-125">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="dd569-125">-InformationAction</span></span>
<span data-ttu-id="dd569-126">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="dd569-126">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="dd569-127">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="dd569-127">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="dd569-128">Продолжал</span><span class="sxs-lookup"><span data-stu-id="dd569-128">Continue</span></span>
- <span data-ttu-id="dd569-129">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="dd569-129">Ignore</span></span>
- <span data-ttu-id="dd569-130">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="dd569-130">Inquire</span></span>
- <span data-ttu-id="dd569-131">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="dd569-131">SilentlyContinue</span></span>
- <span data-ttu-id="dd569-132">Остановить</span><span class="sxs-lookup"><span data-stu-id="dd569-132">Stop</span></span>
- <span data-ttu-id="dd569-133">Рвать</span><span class="sxs-lookup"><span data-stu-id="dd569-133">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd569-134">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="dd569-134">-InformationVariable</span></span>
<span data-ttu-id="dd569-135">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="dd569-135">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd569-136">-Pre</span><span class="sxs-lookup"><span data-stu-id="dd569-136">-Pre</span></span>
<span data-ttu-id="dd569-137">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="dd569-137">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="dd569-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dd569-138">-ResourceId</span></span>
<span data-ttu-id="dd569-139">Задает массив идентификаторов ресурсов, перемещаемых этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="dd569-139">Specifies an array of IDs of the resources that this cmdlet moves.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dd569-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dd569-140">-Confirm</span></span>
<span data-ttu-id="dd569-141">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="dd569-141">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd569-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd569-142">-WhatIf</span></span>
<span data-ttu-id="dd569-143">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="dd569-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd569-144">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="dd569-144">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd569-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd569-145">CommonParameters</span></span>
<span data-ttu-id="dd569-146">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dd569-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd569-147">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd569-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd569-148">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dd569-148">INPUTS</span></span>

### <span data-ttu-id="dd569-149">String []</span><span class="sxs-lookup"><span data-stu-id="dd569-149">String[]</span></span>
<span data-ttu-id="dd569-150">Параметр ResourceId принимает значение типа String [] из конвейера.</span><span class="sxs-lookup"><span data-stu-id="dd569-150">Parameter 'ResourceId' accepts value of type 'String[]' from the pipeline</span></span>

## <span data-ttu-id="dd569-151">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dd569-151">OUTPUTS</span></span>

### <span data-ttu-id="dd569-152">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="dd569-152">System.Boolean</span></span>

## <span data-ttu-id="dd569-153">Пуск</span><span class="sxs-lookup"><span data-stu-id="dd569-153">NOTES</span></span>

## <span data-ttu-id="dd569-154">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dd569-154">RELATED LINKS</span></span>

[<span data-ttu-id="dd569-155">Find-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="dd569-155">Find-AzureRmResource</span></span>](./Find-AzureRmResource.md)

[<span data-ttu-id="dd569-156">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="dd569-156">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="dd569-157">New-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="dd569-157">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="dd569-158">Remove-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="dd569-158">Remove-AzureRmResource</span></span>](./Remove-AzureRmResource.md)

[<span data-ttu-id="dd569-159">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="dd569-159">Set-AzureRmResource</span></span>](./Set-AzureRmResource.md)


