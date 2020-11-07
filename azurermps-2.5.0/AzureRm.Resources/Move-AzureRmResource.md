---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 60BED40A-EEA4-4667-93E9-8A9B35037726
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/move-azurermresource
schema: 2.0.0
ms.openlocfilehash: 4f50aea600fe930de62a65d566b6a6ec723fc8de
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914369"
---
# <span data-ttu-id="225e6-101">Move-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="225e6-101">Move-AzureRmResource</span></span>

## <span data-ttu-id="225e6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="225e6-102">SYNOPSIS</span></span>
<span data-ttu-id="225e6-103">Перемещает ресурс в другую группу ресурсов или подписку.</span><span class="sxs-lookup"><span data-stu-id="225e6-103">Moves a resource to a different resource group or subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="225e6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="225e6-104">SYNTAX</span></span>

```
Move-AzureRmResource -DestinationResourceGroupName <String> [-DestinationSubscriptionId <Guid>]
 -ResourceId <String[]> [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="225e6-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="225e6-105">DESCRIPTION</span></span>
<span data-ttu-id="225e6-106">Командлет **Move-AzureRmResource** перемещает существующие ресурсы в другую группу ресурсов.</span><span class="sxs-lookup"><span data-stu-id="225e6-106">The **Move-AzureRmResource** cmdlet moves existing resources to a different resource group.</span></span>
<span data-ttu-id="225e6-107">Эта группа ресурсов может входить в другую подписку.</span><span class="sxs-lookup"><span data-stu-id="225e6-107">That resource group can be in a different subscription.</span></span>

## <span data-ttu-id="225e6-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="225e6-108">EXAMPLES</span></span>

### <span data-ttu-id="225e6-109">Пример 1: перемещение ресурса в группу ресурсов</span><span class="sxs-lookup"><span data-stu-id="225e6-109">Example 1: Move a resource to a resource group</span></span>
```
PS C:\>$Resource = Get-AzureRmResource -ResourceType "Microsoft.ClassicCompute/storageAccounts" -ResourceName "ContosoStorageAccount"
PS C:\> Move-AzureRmResource -ResourceId $Resource.ResourceId -DestinationResourceGroupName "ResourceGroup14"
```

<span data-ttu-id="225e6-110">Первая команда получает ресурс с именем ContosoStorageAccount с помощью командлета Get-AzureRmResource и сохраняет этот ресурс в переменной $Resource.</span><span class="sxs-lookup"><span data-stu-id="225e6-110">The first command gets a resource named ContosoStorageAccount by using the Get-AzureRmResource cmdlet, and then stores that resource in the $Resource variable.</span></span>
<span data-ttu-id="225e6-111">Вторая команда перемещает этот ресурс в группу ресурсов с именем ResourceGroup14.</span><span class="sxs-lookup"><span data-stu-id="225e6-111">The second command moves that resource into the resource group named ResourceGroup14.</span></span>
<span data-ttu-id="225e6-112">Команда определяет ресурс для перемещения с помощью свойства **ResourceId** для $Resource.</span><span class="sxs-lookup"><span data-stu-id="225e6-112">The command identifies the resource to move by using the **ResourceId** property of $Resource.</span></span>

## <span data-ttu-id="225e6-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="225e6-113">PARAMETERS</span></span>

### <span data-ttu-id="225e6-114">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="225e6-114">-ApiVersion</span></span>
<span data-ttu-id="225e6-115">Указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="225e6-115">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="225e6-116">Если вы не укажете версию, этот командлет использует последнюю доступную версию.</span><span class="sxs-lookup"><span data-stu-id="225e6-116">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="225e6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="225e6-117">-DefaultProfile</span></span>
<span data-ttu-id="225e6-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="225e6-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="225e6-119">-DestinationResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="225e6-119">-DestinationResourceGroupName</span></span>
<span data-ttu-id="225e6-120">Указывает имя группы ресурсов, в которую этот командлет перемещает ресурсы.</span><span class="sxs-lookup"><span data-stu-id="225e6-120">Specifies the name of the resource group into which this cmdlet moves resources.</span></span>

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

### <span data-ttu-id="225e6-121">-DestinationSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="225e6-121">-DestinationSubscriptionId</span></span>
<span data-ttu-id="225e6-122">Указывает идентификатор подписки, в которую этот командлет перемещает ресурсы.</span><span class="sxs-lookup"><span data-stu-id="225e6-122">Specifies the ID of the subscription into which this cmdlet moves resources .</span></span>

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

### <span data-ttu-id="225e6-123">-Force</span><span class="sxs-lookup"><span data-stu-id="225e6-123">-Force</span></span>
<span data-ttu-id="225e6-124">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="225e6-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="225e6-125">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="225e6-125">-InformationAction</span></span>
<span data-ttu-id="225e6-126">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="225e6-126">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="225e6-127">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="225e6-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="225e6-128">Продолжал</span><span class="sxs-lookup"><span data-stu-id="225e6-128">Continue</span></span>
- <span data-ttu-id="225e6-129">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="225e6-129">Ignore</span></span>
- <span data-ttu-id="225e6-130">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="225e6-130">Inquire</span></span>
- <span data-ttu-id="225e6-131">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="225e6-131">SilentlyContinue</span></span>
- <span data-ttu-id="225e6-132">Остановить</span><span class="sxs-lookup"><span data-stu-id="225e6-132">Stop</span></span>
- <span data-ttu-id="225e6-133">Рвать</span><span class="sxs-lookup"><span data-stu-id="225e6-133">Suspend</span></span>

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

### <span data-ttu-id="225e6-134">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="225e6-134">-InformationVariable</span></span>
<span data-ttu-id="225e6-135">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="225e6-135">Specifies an information variable.</span></span>

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

### <span data-ttu-id="225e6-136">-Pre</span><span class="sxs-lookup"><span data-stu-id="225e6-136">-Pre</span></span>
<span data-ttu-id="225e6-137">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="225e6-137">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="225e6-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="225e6-138">-ResourceId</span></span>
<span data-ttu-id="225e6-139">Задает массив идентификаторов ресурсов, перемещаемых этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="225e6-139">Specifies an array of IDs of the resources that this cmdlet moves.</span></span>

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

### <span data-ttu-id="225e6-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="225e6-140">-Confirm</span></span>
<span data-ttu-id="225e6-141">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="225e6-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="225e6-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="225e6-142">-WhatIf</span></span>
<span data-ttu-id="225e6-143">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="225e6-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="225e6-144">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="225e6-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="225e6-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="225e6-145">CommonParameters</span></span>
<span data-ttu-id="225e6-146">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="225e6-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="225e6-147">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="225e6-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="225e6-148">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="225e6-148">INPUTS</span></span>

## <span data-ttu-id="225e6-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="225e6-149">OUTPUTS</span></span>

## <span data-ttu-id="225e6-150">Пуск</span><span class="sxs-lookup"><span data-stu-id="225e6-150">NOTES</span></span>

## <span data-ttu-id="225e6-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="225e6-151">RELATED LINKS</span></span>



[<span data-ttu-id="225e6-152">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="225e6-152">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="225e6-153">New-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="225e6-153">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="225e6-154">Remove-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="225e6-154">Remove-AzureRmResource</span></span>](./Remove-AzureRmResource.md)

[<span data-ttu-id="225e6-155">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="225e6-155">Set-AzureRmResource</span></span>](./Set-AzureRmResource.md)


