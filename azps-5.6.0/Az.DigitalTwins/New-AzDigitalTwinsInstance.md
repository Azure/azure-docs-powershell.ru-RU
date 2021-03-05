---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/powershell/module/az.digitaltwins/new-azdigitaltwinsinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/New-AzDigitalTwinsInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/New-AzDigitalTwinsInstance.md
ms.openlocfilehash: 54fdbcfe83dd93101030d92f9f3eec19d1a2564f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984934"
---
# <span data-ttu-id="316fb-101">New-AzDigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="316fb-101">New-AzDigitalTwinsInstance</span></span>

## <span data-ttu-id="316fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="316fb-102">SYNOPSIS</span></span>
<span data-ttu-id="316fb-103">Создание или обновление метаданных digitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="316fb-103">Create or update the metadata of a DigitalTwinsInstance.</span></span>
<span data-ttu-id="316fb-104">Обычно для изменения свойства требуется извлечь данные DigitalTwinsInstance и метаданные безопасности, а затем объединить их с измененными значениями в новом теле для обновления DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="316fb-104">The usual pattern to modify a property is to retrieve the DigitalTwinsInstance and security metadata, and then combine them with the modified values in a new body to update the DigitalTwinsInstance.</span></span>

## <span data-ttu-id="316fb-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="316fb-105">SYNTAX</span></span>

### <span data-ttu-id="316fb-106">CreateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="316fb-106">CreateExpanded (Default)</span></span>
```
New-AzDigitalTwinsInstance -ResourceGroupName <String> -ResourceName <String> -Location <String>
 [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="316fb-107">"Создать"</span><span class="sxs-lookup"><span data-stu-id="316fb-107">Create</span></span>
```
New-AzDigitalTwinsInstance -ResourceGroupName <String> -ResourceName <String>
 -DigitalTwinsCreate <IDigitalTwinsDescription> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="316fb-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="316fb-108">DESCRIPTION</span></span>
<span data-ttu-id="316fb-109">Создание или обновление метаданных digitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="316fb-109">Create or update the metadata of a DigitalTwinsInstance.</span></span>
<span data-ttu-id="316fb-110">Обычно для изменения свойства требуется извлечь данные DigitalTwinsInstance и метаданные безопасности, а затем объединить их с измененными значениями в новом теле для обновления DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="316fb-110">The usual pattern to modify a property is to retrieve the DigitalTwinsInstance and security metadata, and then combine them with the modified values in a new body to update the DigitalTwinsInstance.</span></span>

## <span data-ttu-id="316fb-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="316fb-111">EXAMPLES</span></span>

### <span data-ttu-id="316fb-112">Пример 1. Создание по умолчанию azDigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="316fb-112">Example 1: Create an AzDigitalTwinsInstance by default.</span></span>
```powershell
PS C:\> New-AzDigitalTwinsInstance -ResourceGroupName youritest -ResourceName youriDigitalTwin -Location eastus

Location Name             SkuName Type
-------- ----             ------- ----
eastus   youriDigitalTwin S1      Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="316fb-113">Создание azDigitalTwinsInstance по умолчанию</span><span class="sxs-lookup"><span data-stu-id="316fb-113">Create an AzDigitalTwinsInstance by default</span></span>

### <span data-ttu-id="316fb-114">Пример 2. Создание объекта AzDigitalTwinsInstance объектом AzDigitalTwins.</span><span class="sxs-lookup"><span data-stu-id="316fb-114">Example 2: Create an AzDigitalTwinsInstance by AzDigitalTwins Object.</span></span>
```powershell
PS C:\> $GetAzDigTwin = Get-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest
New-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest01 -DigitalTwinsCreate $getAzdigitalTwins

Location Name                    Type
-------- ----                    ----
eastus   youriDigitalTwinsTest01 Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="316fb-115">Создание azDigitalTwinsInstance объекта AzDigitalTwins</span><span class="sxs-lookup"><span data-stu-id="316fb-115">Create an AzDigitalTwinsInstance by AzDigitalTwins Object</span></span>

## <span data-ttu-id="316fb-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="316fb-116">PARAMETERS</span></span>

### <span data-ttu-id="316fb-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="316fb-117">-AsJob</span></span>
<span data-ttu-id="316fb-118">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="316fb-118">Run the command as a job</span></span>

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

### <span data-ttu-id="316fb-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="316fb-119">-DefaultProfile</span></span>
<span data-ttu-id="316fb-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="316fb-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="316fb-121">-DigitalTwinsCreate</span><span class="sxs-lookup"><span data-stu-id="316fb-121">-DigitalTwinsCreate</span></span>
<span data-ttu-id="316fb-122">Описание службы DigitalTwins.</span><span class="sxs-lookup"><span data-stu-id="316fb-122">The description of the DigitalTwins service.</span></span>
<span data-ttu-id="316fb-123">Чтобы построить новую таблицу, см. раздел "ЗАМЕТКИ" для свойств DIGITALTWINSCREATE и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="316fb-123">To construct, see NOTES section for DIGITALTWINSCREATE properties and create a hash table.</span></span>

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

### <span data-ttu-id="316fb-124">-Location</span><span class="sxs-lookup"><span data-stu-id="316fb-124">-Location</span></span>
<span data-ttu-id="316fb-125">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="316fb-125">The resource location.</span></span>

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

### <span data-ttu-id="316fb-126">-NoWait</span><span class="sxs-lookup"><span data-stu-id="316fb-126">-NoWait</span></span>
<span data-ttu-id="316fb-127">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="316fb-127">Run the command asynchronously</span></span>

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

### <span data-ttu-id="316fb-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="316fb-128">-ResourceGroupName</span></span>
<span data-ttu-id="316fb-129">Имя группы ресурсов, которая содержит digitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="316fb-129">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="316fb-130">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="316fb-130">-ResourceName</span></span>
<span data-ttu-id="316fb-131">Имя digitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="316fb-131">The name of the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="316fb-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="316fb-132">-SubscriptionId</span></span>
<span data-ttu-id="316fb-133">Идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="316fb-133">The subscription identifier.</span></span>

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

### <span data-ttu-id="316fb-134">-Tag</span><span class="sxs-lookup"><span data-stu-id="316fb-134">-Tag</span></span>
<span data-ttu-id="316fb-135">Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="316fb-135">The resource tags.</span></span>

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

### <span data-ttu-id="316fb-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="316fb-136">-Confirm</span></span>
<span data-ttu-id="316fb-137">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="316fb-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="316fb-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="316fb-138">-WhatIf</span></span>
<span data-ttu-id="316fb-139">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="316fb-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="316fb-140">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="316fb-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="316fb-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="316fb-141">CommonParameters</span></span>
<span data-ttu-id="316fb-142">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="316fb-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="316fb-143">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="316fb-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="316fb-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="316fb-144">INPUTS</span></span>

### <span data-ttu-id="316fb-145">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span><span class="sxs-lookup"><span data-stu-id="316fb-145">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span></span>

## <span data-ttu-id="316fb-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="316fb-146">OUTPUTS</span></span>

### <span data-ttu-id="316fb-147">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span><span class="sxs-lookup"><span data-stu-id="316fb-147">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span></span>

## <span data-ttu-id="316fb-148">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="316fb-148">NOTES</span></span>

<span data-ttu-id="316fb-149">ALIASES</span><span class="sxs-lookup"><span data-stu-id="316fb-149">ALIASES</span></span>

<span data-ttu-id="316fb-150">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="316fb-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="316fb-151">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="316fb-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="316fb-152">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="316fb-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="316fb-153">DIGITALTWINSCREATE: <IDigitalTwinsDescription> описание службы DigitalTwins.</span><span class="sxs-lookup"><span data-stu-id="316fb-153">DIGITALTWINSCREATE <IDigitalTwinsDescription>: The description of the DigitalTwins service.</span></span>
  - <span data-ttu-id="316fb-154">`Location <String>`. Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="316fb-154">`Location <String>`: The resource location.</span></span>
  - <span data-ttu-id="316fb-155">`[Tag <IDigitalTwinsResourceTags>]`Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="316fb-155">`[Tag <IDigitalTwinsResourceTags>]`: The resource tags.</span></span>
    - <span data-ttu-id="316fb-156">`[(Any) <String>]`— это означает, что к этому объекту можно добавить любое свойство.</span><span class="sxs-lookup"><span data-stu-id="316fb-156">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>

## <span data-ttu-id="316fb-157">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="316fb-157">RELATED LINKS</span></span>

