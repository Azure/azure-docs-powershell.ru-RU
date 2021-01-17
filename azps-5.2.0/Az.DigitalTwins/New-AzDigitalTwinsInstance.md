---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/en-us/powershell/module/az.digitaltwins/new-azdigitaltwinsinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/New-AzDigitalTwinsInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/New-AzDigitalTwinsInstance.md
ms.openlocfilehash: d6a748897b956759ad64056b0d9b83a6e82e91fc
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98402455"
---
# <span data-ttu-id="68d6b-101">New-AzDigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="68d6b-101">New-AzDigitalTwinsInstance</span></span>

## <span data-ttu-id="68d6b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="68d6b-102">SYNOPSIS</span></span>
<span data-ttu-id="68d6b-103">Создание или обновление метаданных digitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="68d6b-103">Create or update the metadata of a DigitalTwinsInstance.</span></span>
<span data-ttu-id="68d6b-104">Обычно для изменения свойства требуется извлечь данные DigitalTwinsInstance и метаданные безопасности, а затем объединить их с измененными значениями в новом теле для обновления DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="68d6b-104">The usual pattern to modify a property is to retrieve the DigitalTwinsInstance and security metadata, and then combine them with the modified values in a new body to update the DigitalTwinsInstance.</span></span>

## <span data-ttu-id="68d6b-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="68d6b-105">SYNTAX</span></span>

### <span data-ttu-id="68d6b-106">CreateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="68d6b-106">CreateExpanded (Default)</span></span>
```
New-AzDigitalTwinsInstance -ResourceGroupName <String> -ResourceName <String> -Location <String>
 [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="68d6b-107">"Создать"</span><span class="sxs-lookup"><span data-stu-id="68d6b-107">Create</span></span>
```
New-AzDigitalTwinsInstance -ResourceGroupName <String> -ResourceName <String>
 -DigitalTwinsCreate <IDigitalTwinsDescription> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="68d6b-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="68d6b-108">DESCRIPTION</span></span>
<span data-ttu-id="68d6b-109">Создание или обновление метаданных digitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="68d6b-109">Create or update the metadata of a DigitalTwinsInstance.</span></span>
<span data-ttu-id="68d6b-110">Обычно для изменения свойства требуется извлечь данные DigitalTwinsInstance и метаданные безопасности, а затем объединить их с измененными значениями в новом теле для обновления DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="68d6b-110">The usual pattern to modify a property is to retrieve the DigitalTwinsInstance and security metadata, and then combine them with the modified values in a new body to update the DigitalTwinsInstance.</span></span>

## <span data-ttu-id="68d6b-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="68d6b-111">EXAMPLES</span></span>

### <span data-ttu-id="68d6b-112">Пример 1. Создание по умолчанию azDigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="68d6b-112">Example 1: Create an AzDigitalTwinsInstance by default.</span></span>
```powershell
PS C:\> New-AzDigitalTwinsInstance -ResourceGroupName youritest -ResourceName youriDigitalTwin -Location eastus

Location Name             SkuName Type
-------- ----             ------- ----
eastus   youriDigitalTwin S1      Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="68d6b-113">Создание azDigitalTwinsInstance по умолчанию</span><span class="sxs-lookup"><span data-stu-id="68d6b-113">Create an AzDigitalTwinsInstance by default</span></span>

### <span data-ttu-id="68d6b-114">Пример 2. Создание объекта AzDigitalTwinsInstance объектом AzDigitalTwins.</span><span class="sxs-lookup"><span data-stu-id="68d6b-114">Example 2: Create an AzDigitalTwinsInstance by AzDigitalTwins Object.</span></span>
```powershell
PS C:\> $GetAzDigTwin = Get-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest
New-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest01 -DigitalTwinsCreate $getAzdigitalTwins

Location Name                    Type
-------- ----                    ----
eastus   youriDigitalTwinsTest01 Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="68d6b-115">Создание azDigitalTwinsInstance объекта AzDigitalTwins</span><span class="sxs-lookup"><span data-stu-id="68d6b-115">Create an AzDigitalTwinsInstance by AzDigitalTwins Object</span></span>

## <span data-ttu-id="68d6b-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="68d6b-116">PARAMETERS</span></span>

### <span data-ttu-id="68d6b-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="68d6b-117">-AsJob</span></span>
<span data-ttu-id="68d6b-118">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="68d6b-118">Run the command as a job</span></span>

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

### <span data-ttu-id="68d6b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68d6b-119">-DefaultProfile</span></span>
<span data-ttu-id="68d6b-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="68d6b-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68d6b-121">-DigitalTwinsCreate</span><span class="sxs-lookup"><span data-stu-id="68d6b-121">-DigitalTwinsCreate</span></span>
<span data-ttu-id="68d6b-122">Описание службы DigitalTwins.</span><span class="sxs-lookup"><span data-stu-id="68d6b-122">The description of the DigitalTwins service.</span></span>
<span data-ttu-id="68d6b-123">Чтобы построить новую таблицу, см. раздел "ЗАМЕТКИ" для свойств DIGITALTWINSCREATE и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="68d6b-123">To construct, see NOTES section for DIGITALTWINSCREATE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription
Parameter Sets: Create
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="68d6b-124">-Location</span><span class="sxs-lookup"><span data-stu-id="68d6b-124">-Location</span></span>
<span data-ttu-id="68d6b-125">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="68d6b-125">The resource location.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68d6b-126">-NoWait</span><span class="sxs-lookup"><span data-stu-id="68d6b-126">-NoWait</span></span>
<span data-ttu-id="68d6b-127">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="68d6b-127">Run the command asynchronously</span></span>

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

### <span data-ttu-id="68d6b-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68d6b-128">-ResourceGroupName</span></span>
<span data-ttu-id="68d6b-129">Имя группы ресурсов, которая содержит digitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="68d6b-129">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68d6b-130">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="68d6b-130">-ResourceName</span></span>
<span data-ttu-id="68d6b-131">Имя digitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="68d6b-131">The name of the DigitalTwinsInstance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68d6b-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="68d6b-132">-SubscriptionId</span></span>
<span data-ttu-id="68d6b-133">Идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="68d6b-133">The subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68d6b-134">-Tag</span><span class="sxs-lookup"><span data-stu-id="68d6b-134">-Tag</span></span>
<span data-ttu-id="68d6b-135">Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="68d6b-135">The resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68d6b-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="68d6b-136">-Confirm</span></span>
<span data-ttu-id="68d6b-137">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="68d6b-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68d6b-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68d6b-138">-WhatIf</span></span>
<span data-ttu-id="68d6b-139">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="68d6b-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="68d6b-140">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="68d6b-140">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68d6b-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68d6b-141">CommonParameters</span></span>
<span data-ttu-id="68d6b-142">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68d6b-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68d6b-143">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="68d6b-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68d6b-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="68d6b-144">INPUTS</span></span>

### <span data-ttu-id="68d6b-145">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span><span class="sxs-lookup"><span data-stu-id="68d6b-145">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span></span>

## <span data-ttu-id="68d6b-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="68d6b-146">OUTPUTS</span></span>

### <span data-ttu-id="68d6b-147">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span><span class="sxs-lookup"><span data-stu-id="68d6b-147">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span></span>

## <span data-ttu-id="68d6b-148">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="68d6b-148">NOTES</span></span>

<span data-ttu-id="68d6b-149">ALIASES</span><span class="sxs-lookup"><span data-stu-id="68d6b-149">ALIASES</span></span>

<span data-ttu-id="68d6b-150">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="68d6b-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="68d6b-151">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="68d6b-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="68d6b-152">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="68d6b-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="68d6b-153">DIGITALTWINSCREATE: <IDigitalTwinsDescription> описание службы DigitalTwins.</span><span class="sxs-lookup"><span data-stu-id="68d6b-153">DIGITALTWINSCREATE <IDigitalTwinsDescription>: The description of the DigitalTwins service.</span></span>
  - <span data-ttu-id="68d6b-154">`Location <String>`. Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="68d6b-154">`Location <String>`: The resource location.</span></span>
  - <span data-ttu-id="68d6b-155">`[Tag <IDigitalTwinsResourceTags>]`Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="68d6b-155">`[Tag <IDigitalTwinsResourceTags>]`: The resource tags.</span></span>
    - <span data-ttu-id="68d6b-156">`[(Any) <String>]`— это означает, что к этому объекту можно добавить любое свойство.</span><span class="sxs-lookup"><span data-stu-id="68d6b-156">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>

## <span data-ttu-id="68d6b-157">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="68d6b-157">RELATED LINKS</span></span>

