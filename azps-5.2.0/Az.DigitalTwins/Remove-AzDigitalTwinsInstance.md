---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/en-us/powershell/module/az.digitaltwins/remove-azdigitaltwinsinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Remove-AzDigitalTwinsInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Remove-AzDigitalTwinsInstance.md
ms.openlocfilehash: 495fecf922bc27eb43849b7ba6e44793c572b8cd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98402436"
---
# <span data-ttu-id="19439-101">Remove-AzDigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="19439-101">Remove-AzDigitalTwinsInstance</span></span>

## <span data-ttu-id="19439-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19439-102">SYNOPSIS</span></span>
<span data-ttu-id="19439-103">Удаление DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="19439-103">Delete a DigitalTwinsInstance.</span></span>

## <span data-ttu-id="19439-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="19439-104">SYNTAX</span></span>

### <span data-ttu-id="19439-105">Delete (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="19439-105">Delete (Default)</span></span>
```
Remove-AzDigitalTwinsInstance -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="19439-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="19439-106">DeleteViaIdentity</span></span>
```
Remove-AzDigitalTwinsInstance -InputObject <IDigitalTwinsIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="19439-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="19439-107">DESCRIPTION</span></span>
<span data-ttu-id="19439-108">Удаление DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="19439-108">Delete a DigitalTwinsInstance.</span></span>

## <span data-ttu-id="19439-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="19439-109">EXAMPLES</span></span>

### <span data-ttu-id="19439-110">Пример 1. Удаление azDigitalTwinsInstance по имени</span><span class="sxs-lookup"><span data-stu-id="19439-110">Example 1: Remove an AzDigitalTwinsInstance by name</span></span>
```powershell
PS C:\> Remove-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwin


```

<span data-ttu-id="19439-111">Эта команда удаляет azDigitalTwinsInstance по имени.</span><span class="sxs-lookup"><span data-stu-id="19439-111">This command removes an AzDigitalTwinsInstance by name</span></span>

### <span data-ttu-id="19439-112">Пример 2. Удаление AzDigitalTwinsInstance путем InputObject</span><span class="sxs-lookup"><span data-stu-id="19439-112">Example 2: Remove an AzDigitalTwinsInstance by InputObject</span></span>
```powershell
PS C:\> $GetAzDigitalTwins =  Get-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest
Remove-AzDigitalTwinsInstance -InputObject $GetAzDigitalTwins


```

<span data-ttu-id="19439-113">Эта команда удаляет azDigitalTwinsInstance по имени.</span><span class="sxs-lookup"><span data-stu-id="19439-113">This command removes an AzDigitalTwinsInstance by name</span></span>

## <span data-ttu-id="19439-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="19439-114">PARAMETERS</span></span>

### <span data-ttu-id="19439-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="19439-115">-AsJob</span></span>
<span data-ttu-id="19439-116">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="19439-116">Run the command as a job</span></span>

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

### <span data-ttu-id="19439-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19439-117">-DefaultProfile</span></span>
<span data-ttu-id="19439-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="19439-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="19439-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="19439-119">-InputObject</span></span>
<span data-ttu-id="19439-120">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="19439-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="19439-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="19439-121">-NoWait</span></span>
<span data-ttu-id="19439-122">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="19439-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="19439-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="19439-123">-PassThru</span></span>
<span data-ttu-id="19439-124">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="19439-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="19439-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19439-125">-ResourceGroupName</span></span>
<span data-ttu-id="19439-126">Имя группы ресурсов, которая содержит digitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="19439-126">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="19439-127">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="19439-127">-ResourceName</span></span>
<span data-ttu-id="19439-128">Имя digitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="19439-128">The name of the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="19439-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="19439-129">-SubscriptionId</span></span>
<span data-ttu-id="19439-130">Идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="19439-130">The subscription identifier.</span></span>

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

### <span data-ttu-id="19439-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="19439-131">-Confirm</span></span>
<span data-ttu-id="19439-132">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="19439-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19439-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19439-133">-WhatIf</span></span>
<span data-ttu-id="19439-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="19439-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="19439-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="19439-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19439-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19439-136">CommonParameters</span></span>
<span data-ttu-id="19439-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19439-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19439-138">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="19439-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19439-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="19439-139">INPUTS</span></span>

### <span data-ttu-id="19439-140">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="19439-140">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span></span>

## <span data-ttu-id="19439-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="19439-141">OUTPUTS</span></span>

### <span data-ttu-id="19439-142">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span><span class="sxs-lookup"><span data-stu-id="19439-142">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span></span>

## <span data-ttu-id="19439-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="19439-143">NOTES</span></span>

<span data-ttu-id="19439-144">ALIASES</span><span class="sxs-lookup"><span data-stu-id="19439-144">ALIASES</span></span>

<span data-ttu-id="19439-145">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="19439-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="19439-146">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="19439-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="19439-147">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="19439-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="19439-148">INPUTOBJECT <IDigitalTwinsIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="19439-148">INPUTOBJECT <IDigitalTwinsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="19439-149">`[EndpointName <String>]`: Имя ресурса конечной точки.</span><span class="sxs-lookup"><span data-stu-id="19439-149">`[EndpointName <String>]`: Name of Endpoint Resource.</span></span>
  - <span data-ttu-id="19439-150">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="19439-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="19439-151">`[Location <String>]`: Расположение DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="19439-151">`[Location <String>]`: Location of DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="19439-152">`[ResourceGroupName <String>]`: Имя группы ресурсов, которая содержит DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="19439-152">`[ResourceGroupName <String>]`: The name of the resource group that contains the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="19439-153">`[ResourceName <String>]`: Имя DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="19439-153">`[ResourceName <String>]`: The name of the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="19439-154">`[SubscriptionId <String>]`: идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="19439-154">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="19439-155">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="19439-155">RELATED LINKS</span></span>

