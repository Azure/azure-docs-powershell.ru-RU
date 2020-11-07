---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 60BED40A-EEA4-4667-93E9-8A9B35037726
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Move-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Move-AzureRmResource.md
ms.openlocfilehash: 4a40b3fd0045a48d6a69c76970b3835ef2d685c8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733329"
---
# <span data-ttu-id="f6b70-101">Move-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="f6b70-101">Move-AzureRmResource</span></span>

## <span data-ttu-id="f6b70-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f6b70-102">SYNOPSIS</span></span>
<span data-ttu-id="f6b70-103">Перемещает ресурс в другую группу ресурсов или подписку.</span><span class="sxs-lookup"><span data-stu-id="f6b70-103">Moves a resource to a different resource group or subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f6b70-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f6b70-104">SYNTAX</span></span>

```
Move-AzureRmResource -DestinationResourceGroupName <String> [-DestinationSubscriptionId <Guid>]
 -ResourceId <String[]> [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f6b70-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f6b70-105">DESCRIPTION</span></span>
<span data-ttu-id="f6b70-106">Командлет **Move-AzureRmResource** перемещает существующие ресурсы в другую группу ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f6b70-106">The **Move-AzureRmResource** cmdlet moves existing resources to a different resource group.</span></span>
<span data-ttu-id="f6b70-107">Эта группа ресурсов может входить в другую подписку.</span><span class="sxs-lookup"><span data-stu-id="f6b70-107">That resource group can be in a different subscription.</span></span>

## <span data-ttu-id="f6b70-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f6b70-108">EXAMPLES</span></span>

### <span data-ttu-id="f6b70-109">Пример 1: перемещение ресурса в группу ресурсов</span><span class="sxs-lookup"><span data-stu-id="f6b70-109">Example 1: Move a resource to a resource group</span></span>
```
PS C:\>$Resource = Get-AzureRmResource -ResourceType "Microsoft.ClassicCompute/storageAccounts" -ResourceName "ContosoStorageAccount"
PS C:\> Move-AzureRmResource -ResourceId $Resource.ResourceId -DestinationResourceGroupName "ResourceGroup14"
```

<span data-ttu-id="f6b70-110">Первая команда получает ресурс с именем ContosoStorageAccount с помощью командлета Get-AzureRmResource и сохраняет этот ресурс в переменной $Resource.</span><span class="sxs-lookup"><span data-stu-id="f6b70-110">The first command gets a resource named ContosoStorageAccount by using the Get-AzureRmResource cmdlet, and then stores that resource in the $Resource variable.</span></span>

<span data-ttu-id="f6b70-111">Вторая команда перемещает этот ресурс в группу ресурсов с именем ResourceGroup14.</span><span class="sxs-lookup"><span data-stu-id="f6b70-111">The second command moves that resource into the resource group named ResourceGroup14.</span></span>
<span data-ttu-id="f6b70-112">Команда определяет ресурс для перемещения с помощью свойства **ResourceId** для $Resource.</span><span class="sxs-lookup"><span data-stu-id="f6b70-112">The command identifies the resource to move by using the **ResourceId** property of $Resource.</span></span>

## <span data-ttu-id="f6b70-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f6b70-113">PARAMETERS</span></span>

### <span data-ttu-id="f6b70-114">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="f6b70-114">-ApiVersion</span></span>
<span data-ttu-id="f6b70-115">Указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f6b70-115">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="f6b70-116">Если вы не укажете версию, этот командлет использует последнюю доступную версию.</span><span class="sxs-lookup"><span data-stu-id="f6b70-116">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="f6b70-117">-DestinationResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6b70-117">-DestinationResourceGroupName</span></span>
<span data-ttu-id="f6b70-118">Указывает имя группы ресурсов, в которую этот командлет перемещает ресурсы.</span><span class="sxs-lookup"><span data-stu-id="f6b70-118">Specifies the name of the resource group into which this cmdlet moves resources.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TargetResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6b70-119">-DestinationSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f6b70-119">-DestinationSubscriptionId</span></span>
<span data-ttu-id="f6b70-120">Указывает идентификатор подписки, в которую этот командлет перемещает ресурсы.</span><span class="sxs-lookup"><span data-stu-id="f6b70-120">Specifies the ID of the subscription into which this cmdlet moves resources .</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: (All)
Aliases: Id, SubscriptionId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6b70-121">-Force</span><span class="sxs-lookup"><span data-stu-id="f6b70-121">-Force</span></span>
<span data-ttu-id="f6b70-122">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="f6b70-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f6b70-123">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="f6b70-123">-InformationAction</span></span>
<span data-ttu-id="f6b70-124">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="f6b70-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="f6b70-125">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="f6b70-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f6b70-126">Продолжал</span><span class="sxs-lookup"><span data-stu-id="f6b70-126">Continue</span></span>
- <span data-ttu-id="f6b70-127">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="f6b70-127">Ignore</span></span>
- <span data-ttu-id="f6b70-128">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="f6b70-128">Inquire</span></span>
- <span data-ttu-id="f6b70-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="f6b70-129">SilentlyContinue</span></span>
- <span data-ttu-id="f6b70-130">Остановить</span><span class="sxs-lookup"><span data-stu-id="f6b70-130">Stop</span></span>
- <span data-ttu-id="f6b70-131">Рвать</span><span class="sxs-lookup"><span data-stu-id="f6b70-131">Suspend</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6b70-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="f6b70-132">-InformationVariable</span></span>
<span data-ttu-id="f6b70-133">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="f6b70-133">Specifies an information variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6b70-134">-Pre</span><span class="sxs-lookup"><span data-stu-id="f6b70-134">-Pre</span></span>
<span data-ttu-id="f6b70-135">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="f6b70-135">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="f6b70-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f6b70-136">-ResourceId</span></span>
<span data-ttu-id="f6b70-137">Задает массив идентификаторов ресурсов, перемещаемых этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="f6b70-137">Specifies an array of IDs of the resources that this cmdlet moves.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f6b70-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f6b70-138">-Confirm</span></span>
<span data-ttu-id="f6b70-139">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f6b70-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6b70-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6b70-140">-WhatIf</span></span>
<span data-ttu-id="f6b70-141">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f6b70-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f6b70-142">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f6b70-142">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6b70-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6b70-143">-DefaultProfile</span></span>
<span data-ttu-id="f6b70-144">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f6b70-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f6b70-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6b70-145">CommonParameters</span></span>
<span data-ttu-id="f6b70-146">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f6b70-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6b70-147">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6b70-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6b70-148">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f6b70-148">INPUTS</span></span>

### <span data-ttu-id="f6b70-149">String []</span><span class="sxs-lookup"><span data-stu-id="f6b70-149">String[]</span></span>
<span data-ttu-id="f6b70-150">Параметр ResourceId принимает значение типа String [] из конвейера.</span><span class="sxs-lookup"><span data-stu-id="f6b70-150">Parameter 'ResourceId' accepts value of type 'String[]' from the pipeline</span></span>

## <span data-ttu-id="f6b70-151">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f6b70-151">OUTPUTS</span></span>

### <span data-ttu-id="f6b70-152">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f6b70-152">System.Boolean</span></span>

## <span data-ttu-id="f6b70-153">Пуск</span><span class="sxs-lookup"><span data-stu-id="f6b70-153">NOTES</span></span>

## <span data-ttu-id="f6b70-154">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f6b70-154">RELATED LINKS</span></span>

[<span data-ttu-id="f6b70-155">Find-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="f6b70-155">Find-AzureRmResource</span></span>](./Find-AzureRmResource.md)

[<span data-ttu-id="f6b70-156">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="f6b70-156">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="f6b70-157">New-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="f6b70-157">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="f6b70-158">Remove-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="f6b70-158">Remove-AzureRmResource</span></span>](./Remove-AzureRmResource.md)

[<span data-ttu-id="f6b70-159">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="f6b70-159">Set-AzureRmResource</span></span>](./Set-AzureRmResource.md)


