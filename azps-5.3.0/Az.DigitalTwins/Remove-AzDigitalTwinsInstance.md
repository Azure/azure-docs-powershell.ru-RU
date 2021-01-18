---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/en-us/powershell/module/az.digitaltwins/remove-azdigitaltwinsinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Remove-AzDigitalTwinsInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Remove-AzDigitalTwinsInstance.md
ms.openlocfilehash: 495fecf922bc27eb43849b7ba6e44793c572b8cd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506307"
---
# <span data-ttu-id="c21ae-101">Remove-AzDigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="c21ae-101">Remove-AzDigitalTwinsInstance</span></span>

## <span data-ttu-id="c21ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c21ae-102">SYNOPSIS</span></span>
<span data-ttu-id="c21ae-103">Удаление DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="c21ae-103">Delete a DigitalTwinsInstance.</span></span>

## <span data-ttu-id="c21ae-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c21ae-104">SYNTAX</span></span>

### <span data-ttu-id="c21ae-105">Delete (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c21ae-105">Delete (Default)</span></span>
```
Remove-AzDigitalTwinsInstance -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c21ae-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="c21ae-106">DeleteViaIdentity</span></span>
```
Remove-AzDigitalTwinsInstance -InputObject <IDigitalTwinsIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c21ae-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c21ae-107">DESCRIPTION</span></span>
<span data-ttu-id="c21ae-108">Удаление DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="c21ae-108">Delete a DigitalTwinsInstance.</span></span>

## <span data-ttu-id="c21ae-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c21ae-109">EXAMPLES</span></span>

### <span data-ttu-id="c21ae-110">Пример 1. Удаление azDigitalTwinsInstance по имени</span><span class="sxs-lookup"><span data-stu-id="c21ae-110">Example 1: Remove an AzDigitalTwinsInstance by name</span></span>
```powershell
PS C:\> Remove-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwin


```

<span data-ttu-id="c21ae-111">Эта команда удаляет azDigitalTwinsInstance по имени.</span><span class="sxs-lookup"><span data-stu-id="c21ae-111">This command removes an AzDigitalTwinsInstance by name</span></span>

### <span data-ttu-id="c21ae-112">Пример 2. Удаление azDigitalTwinsInstance с помощью InputObject</span><span class="sxs-lookup"><span data-stu-id="c21ae-112">Example 2: Remove an AzDigitalTwinsInstance by InputObject</span></span>
```powershell
PS C:\> $GetAzDigitalTwins =  Get-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest
Remove-AzDigitalTwinsInstance -InputObject $GetAzDigitalTwins


```

<span data-ttu-id="c21ae-113">Эта команда удаляет azDigitalTwinsInstance по имени.</span><span class="sxs-lookup"><span data-stu-id="c21ae-113">This command removes an AzDigitalTwinsInstance by name</span></span>

## <span data-ttu-id="c21ae-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c21ae-114">PARAMETERS</span></span>

### <span data-ttu-id="c21ae-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c21ae-115">-AsJob</span></span>
<span data-ttu-id="c21ae-116">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="c21ae-116">Run the command as a job</span></span>

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

### <span data-ttu-id="c21ae-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c21ae-117">-DefaultProfile</span></span>
<span data-ttu-id="c21ae-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c21ae-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c21ae-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c21ae-119">-InputObject</span></span>
<span data-ttu-id="c21ae-120">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="c21ae-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c21ae-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="c21ae-121">-NoWait</span></span>
<span data-ttu-id="c21ae-122">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="c21ae-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="c21ae-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c21ae-123">-PassThru</span></span>
<span data-ttu-id="c21ae-124">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="c21ae-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="c21ae-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c21ae-125">-ResourceGroupName</span></span>
<span data-ttu-id="c21ae-126">Имя группы ресурсов, которая содержит digitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="c21ae-126">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c21ae-127">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="c21ae-127">-ResourceName</span></span>
<span data-ttu-id="c21ae-128">Имя digitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="c21ae-128">The name of the DigitalTwinsInstance.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c21ae-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c21ae-129">-SubscriptionId</span></span>
<span data-ttu-id="c21ae-130">Идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="c21ae-130">The subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c21ae-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c21ae-131">-Confirm</span></span>
<span data-ttu-id="c21ae-132">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="c21ae-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c21ae-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c21ae-133">-WhatIf</span></span>
<span data-ttu-id="c21ae-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c21ae-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c21ae-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="c21ae-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c21ae-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c21ae-136">CommonParameters</span></span>
<span data-ttu-id="c21ae-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c21ae-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c21ae-138">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c21ae-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c21ae-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c21ae-139">INPUTS</span></span>

### <span data-ttu-id="c21ae-140">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="c21ae-140">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span></span>

## <span data-ttu-id="c21ae-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c21ae-141">OUTPUTS</span></span>

### <span data-ttu-id="c21ae-142">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span><span class="sxs-lookup"><span data-stu-id="c21ae-142">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span></span>

## <span data-ttu-id="c21ae-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c21ae-143">NOTES</span></span>

<span data-ttu-id="c21ae-144">ALIASES</span><span class="sxs-lookup"><span data-stu-id="c21ae-144">ALIASES</span></span>

<span data-ttu-id="c21ae-145">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="c21ae-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c21ae-146">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="c21ae-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c21ae-147">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c21ae-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c21ae-148">INPUTOBJECT <IDigitalTwinsIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="c21ae-148">INPUTOBJECT <IDigitalTwinsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c21ae-149">`[EndpointName <String>]`: Имя ресурса конечной точки.</span><span class="sxs-lookup"><span data-stu-id="c21ae-149">`[EndpointName <String>]`: Name of Endpoint Resource.</span></span>
  - <span data-ttu-id="c21ae-150">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="c21ae-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c21ae-151">`[Location <String>]`: Расположение DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="c21ae-151">`[Location <String>]`: Location of DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="c21ae-152">`[ResourceGroupName <String>]`: Имя группы ресурсов, которая содержит DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="c21ae-152">`[ResourceGroupName <String>]`: The name of the resource group that contains the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="c21ae-153">`[ResourceName <String>]`: Имя DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="c21ae-153">`[ResourceName <String>]`: The name of the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="c21ae-154">`[SubscriptionId <String>]`: идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="c21ae-154">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="c21ae-155">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c21ae-155">RELATED LINKS</span></span>

